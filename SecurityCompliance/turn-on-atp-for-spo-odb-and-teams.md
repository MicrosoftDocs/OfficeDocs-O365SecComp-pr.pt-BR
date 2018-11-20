---
title: Ativar o Office 365 ATP para SharePoint, OneDrive e equipes da Microsoft
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.audience: ITPro
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 07e76024-0c80-40dc-8c48-1dd0d0f863cb
description: Saiba como ativar ATP para o SharePoint, OneDrive e equipes, incluindo como configurar alertas para arquivos detectados.
ms.openlocfilehash: d70c574f002ca7e70ab6f9a4abad3ea5ef21a20f
ms.sourcegitcommit: 147768bbe44c8c98c02fa29ae9d882cee4ec2d6b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/09/2018
ms.locfileid: "26238413"
---
# <a name="turn-on-office-365-atp-for-sharepoint-onedrive-and-microsoft-teams"></a>Ativar o Office 365 ATP para SharePoint, OneDrive e equipes da Microsoft

[ATP do Office 365 para SharePoint, OneDrive e as equipes da Microsoft](atp-for-spo-odb-and-teams.md) protege a sua organização contra inadvertidamente compartilhamento de arquivos mal-intencionados. Quando um arquivo mal-intencionado é detectado, esse arquivo está bloqueado para que ninguém pode abrir, copiar, mover ou compartilhá-la até que outras ações são executadas pela equipe de segurança da organização. Leia este artigo para ativar ATP para SharePoint, OneDrive e equipes, configure os alertas para ser notificado sobre arquivos detectados e siga as próximas etapas. 
  
Para executar as tarefas descritas neste artigo, você deve ter as permissões necessárias atribuídas no Office 365 e na segurança &amp; Centro de conformidade.
  
## <a name="turn-on-atp-for-sharepoint-onedrive-and-microsoft-teams"></a>Ativar a ATP para SharePoint, OneDrive e Microsoft Teams

 **Antes de começar esse procedimento, certifique-se de que os logs de auditoria já esteja ativado para o seu ambiente do Office 365**. Normalmente, isso é feito por alguém que tenha a função de Logs de auditoria atribuída no Exchange Online. Para obter mais informações, consulte [Ativar o Office 365 pesquisa de log de auditoria ativado ou desativado](turn-audit-log-search-on-or-off.md).
  
1. Como administrador global ou administrador de segurança, vá para [https://protection.office.com](https://protection.office.com)e entre com sua conta do trabalho ou da escola.
    
2. No Office 365 Security &amp; Centro de conformidade, no painel de navegação à esquerda, em **gerenciamento de ameaça**, escolha **política** \> **Anexos seguros**. <br/>![Na segurança &amp; Centro de conformidade, escolha gerenciamento de ameaça \> política](media/08849c91-f043-4cd1-a55e-d440c86442f2.png)
  
3. Selecione **Ativar ATP para SharePoint, OneDrive e as equipes da Microsoft**.<br/>![Ativar proteção contra ameaças avançado para SharePoint Online, o OneDrive for Business e equipes da Microsoft](media/48cfaace-59cc-4e60-bf86-05ff6b99bdbf.png)
  
4. Clique em **Salvar**.
    
5. Revise (e, conforme apropriado, edite) as [políticas de Links seguros](set-up-atp-safe-links-policies.md)e as [políticas de segurança de anexos](set-up-atp-safe-attachments-policies.md) da sua organização.
    
6. (Recomendado) Como um administrador global ou um administrador do SharePoint Online, execute o cmdlet **[Set-SPOTenant](https://docs.microsoft.com/powershell/module/sharepoint-online/Set-SPOTenant?view=sharepoint-ps)** com o parâmetro **DisallowInfectedFileDownload** definido como *true*. <br/>
  - Definindo o parâmetro para *true* bloqueia todas as ações (exceto excluir) para arquivos de detectados. As pessoas não podem abrir, mover, copiar ou compartilhar arquivos detectados.
  - Configuração do parâmetro como *false* bloqueia todas as ações, exceto excluir e Download. Pessoas podem optar por aceitar o risco e baixar um arquivo detectado.  
   
7. Permitir até 30 minutos para que suas alterações à difusão em todos os centros de dados do Office 365.
    
8. (Recomendado) Vá para configurar alertas para arquivos detectados.
    
Para saber mais sobre como usar o PowerShell com o Office 365, consulte [Gerenciar o Office 365 com o PowerShell](https://docs.microsoft.com/office365/enterprise/powershell/manage-office-365-with-office-365-powershell). > Para saber mais sobre a experiência do usuário quando um arquivo foi detectado como mal-intencionado, consulte [o que fazer quando um arquivo mal-intencionado é encontrado no SharePoint Online, OneDrive ou equipes da Microsoft](https://support.office.com/article/01e902ad-a903-4e0f-b093-1e1ac0c37ad2). 
  
## <a name="set-up-alerts-for-detected-files"></a>Configurar alertas para arquivos detectados

Para receber uma notificação quando um arquivo no SharePoint Online, OneDrive para negócios ou Microsoft Teams tenha sido identificado como mal-intencionado, você pode configurar um alerta.
  
1. No Office 365 Security &amp; Centro de conformidade, escolha **alertas** \> **Gerenciar alertas**.
    
2. Escolha **nova política de alerta**.
    
3. Especifique um nome para o alerta. Por exemplo, você pode digitar arquivos mal-intencionados nas bibliotecas.
    
4. Digite uma descrição para o alerta. Por exemplo, você pode digitar emite admins quando arquivos mal-intencionados forem detectados no SharePoint Online, OneDrive ou Teams da Microsoft.
    
5. Na seção **enviar esse alerta quando …** , faça o seguinte: 
    
  - Na lista de **atividades** , escolha **malware detectado no arquivo**.
    
  - Deixe o campo de **usuários** vazio. 
    
6. Na seção **enviar esse alerta para …** , selecione um ou mais administradores globais, os administradores de segurança ou leitores de segurança que devem receber uma notificação quando um arquivo mal-intencionado é detectado. 
    
7. Clique em **Salvar**.
    
Para saber mais sobre alertas, consulte [criar alertas de atividade no Office 365 Security &amp; Centro de conformidade](create-activity-alerts.md). 
  
## <a name="next-steps"></a>Próximas etapas

1. [Exibir informações sobre arquivos mal-intencionados detectada no SharePoint, OneDrive ou Teams da Microsoft](malicious-files-detected-in-spo-odb-or-teams.md)
    
2. [Gerenciar arquivos e mensagens em quarentena como um administrador no Office 365](manage-quarantined-messages-and-files.md)
    

  

