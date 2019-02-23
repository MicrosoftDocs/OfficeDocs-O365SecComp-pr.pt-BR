---
title: Ativar o Office 365 ATP para SharePoint, OneDrive e Microsoft Teams
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.audience: ITPro
ms.topic: article
ms.date: 02/06/2019
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 07e76024-0c80-40dc-8c48-1dd0d0f863cb
ms.collection: M365-security-compliance
description: Saiba como ativar a ATP para SharePoint, OneDrive e Teams, incluindo como definir alertas para arquivos detectados.
ms.openlocfilehash: 88eae37b0da3df75807436d66a5c80e0c40f82d8
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30220391"
---
# <a name="turn-on-office-365-atp-for-sharepoint-onedrive-and-microsoft-teams"></a><span data-ttu-id="9bfb7-103">Ativar o Office 365 ATP para SharePoint, OneDrive e Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="9bfb7-103">Turn on Office 365 ATP for SharePoint, OneDrive, and Microsoft Teams</span></span>

<span data-ttu-id="9bfb7-p101">O [Office 365 ATP para SharePoint, onedrive e Microsoft Teams](atp-for-spo-odb-and-teams.md) protege sua organização contra o compartilhamento inadvertidamente de arquivos mal-intencionados. Quando um arquivo mal-intencionado é detectado, esse arquivo é bloqueado para que ninguém possa abri-lo, copiá-lo ou compartilhá-lo até que outras ações sejam executadas pela equipe de segurança da organização. Leia este artigo para habilitar a ATP para o SharePoint, o OneDrive e o Microsoft Teams, configure os alertas a serem notificados sobre os arquivos detectados e execute suas próximas etapas.</span><span class="sxs-lookup"><span data-stu-id="9bfb7-p101">[Office 365 ATP for SharePoint, OneDrive, and Microsoft Teams](atp-for-spo-odb-and-teams.md) protects your organization from inadvertently sharing malicious files. When a malicious file is detected, that file is blocked so that no one can open, copy, move, or share it until further actions are taken by the organization's security team. Read this article to turn on ATP for SharePoint, OneDrive, and Teams, set up alerts to be notified about detected files, and take your next steps.</span></span> 
  
<span data-ttu-id="9bfb7-p102">Para definir (ou editar) políticas ATP, você deve ter uma função apropriada atribuída. Alguns exemplos são descritos na tabela a seguir:</span><span class="sxs-lookup"><span data-stu-id="9bfb7-p102">To define (or edit) ATP policies, you must be assigned an appropriate role. Some examples are described in the following table:</span></span>

|<span data-ttu-id="9bfb7-109">Função</span><span class="sxs-lookup"><span data-stu-id="9bfb7-109">Role</span></span>  |<span data-ttu-id="9bfb7-110">Onde/como a atribuição</span><span class="sxs-lookup"><span data-stu-id="9bfb7-110">Where/how assigned</span></span>  |
|---------|---------|
|<span data-ttu-id="9bfb7-111">Administrador global do Office 365</span><span class="sxs-lookup"><span data-stu-id="9bfb7-111">Office 365 Global Administrator</span></span> |<span data-ttu-id="9bfb7-p103">Por padrão, a pessoa que se inscreve para comprar o Office 365 é um administrador global. (ConFira [sobre as funções de administrador do Office 365](https://docs.microsoft.com/office365/admin/add-users/about-admin-roles) para saber mais.)</span><span class="sxs-lookup"><span data-stu-id="9bfb7-p103">The person who signs up to buy Office 365 is a global admin by default. (See [About Office 365 admin roles](https://docs.microsoft.com/office365/admin/add-users/about-admin-roles) to learn more.)</span></span>         |
|<span data-ttu-id="9bfb7-114">Administrador de segurança</span><span class="sxs-lookup"><span data-stu-id="9bfb7-114">Security Administrator</span></span> |<span data-ttu-id="9bfb7-115">Centro de administração do Azure Active[https://aad.portal.azure.com](https://aad.portal.azure.com)Directory ()</span><span class="sxs-lookup"><span data-stu-id="9bfb7-115">Azure Active Directory admin center ([https://aad.portal.azure.com](https://aad.portal.azure.com))</span></span>|
|<span data-ttu-id="9bfb7-116">Gerenciamento da organização do Exchange Online</span><span class="sxs-lookup"><span data-stu-id="9bfb7-116">Exchange Online Organization Management</span></span> |<span data-ttu-id="9bfb7-117">Centro de administração do[https://outlook.office365.com/ecp](https://outlook.office365.com/ecp)Exchange ()</span><span class="sxs-lookup"><span data-stu-id="9bfb7-117">Exchange admin center ([https://outlook.office365.com/ecp](https://outlook.office365.com/ecp))</span></span> <br><span data-ttu-id="9bfb7-118">ou</span><span class="sxs-lookup"><span data-stu-id="9bfb7-118">or</span></span> <br>  <span data-ttu-id="9bfb7-119">Cmdlets do PowerShell (consulte [Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/exchange-online-powershell?view=exchange-ps))</span><span class="sxs-lookup"><span data-stu-id="9bfb7-119">PowerShell cmdlets (See [Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/exchange-online-powershell?view=exchange-ps))</span></span> |
  
## <a name="turn-on-atp-for-sharepoint-onedrive-and-microsoft-teams"></a><span data-ttu-id="9bfb7-120">Ativar a ATP para SharePoint, OneDrive e Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="9bfb7-120">Turn on ATP for SharePoint, OneDrive, and Microsoft Teams</span></span>

<span data-ttu-id="9bfb7-p104">**Antes de iniciar esse procedimento, verifique se o log de auditoria já está ativado para o seu ambiente do Office 365**. Isso geralmente é feito por alguém que tenha a função de logs de auditoria atribuída no Exchange Online. Para obter mais informações, consulte [Ativar ou desativar a pesquisa de log de auditoria do Office 365](turn-audit-log-search-on-or-off.md).</span><span class="sxs-lookup"><span data-stu-id="9bfb7-p104">**Before you begin this procedure, make sure that audit logging is already turned on for your Office 365 environment**. This is typically done by someone who has the Audit Logs role assigned in Exchange Online. For more information, see [Turn Office 365 audit log search on or off](turn-audit-log-search-on-or-off.md).</span></span>
  
1. <span data-ttu-id="9bfb7-124">Vá até [https://protection.office.com](https://protection.office.com)e entre com sua conta corporativa ou de estudante.</span><span class="sxs-lookup"><span data-stu-id="9bfb7-124">Go to [https://protection.office.com](https://protection.office.com), and sign in with your work or school account.</span></span>
    
2. <span data-ttu-id="9bfb7-125">no centro de conformidade com &amp; segurança do Office 365, no painel de navegação esquerdo, em **gerenciamento de ameaças**, escolha **anexos seguros**de **política** \> .</span><span class="sxs-lookup"><span data-stu-id="9bfb7-125">In the Office 365 Security &amp; Compliance Center, in the left navigation pane, under **Threat management**, choose **Policy** \> **Safe Attachments**.</span></span> <br/><span data-ttu-id="9bfb7-126">![No centro de &amp; conformidade de segurança, escolha política \> de gerenciamento de ameaças](media/08849c91-f043-4cd1-a55e-d440c86442f2.png)</span><span class="sxs-lookup"><span data-stu-id="9bfb7-126">![In the Security &amp; Compliance Center, choose Threat management \> Policy](media/08849c91-f043-4cd1-a55e-d440c86442f2.png)</span></span>
  
3. <span data-ttu-id="9bfb7-127">Selecione **Ativar ATP para SharePoint, onedrive e Microsoft Teams**.</span><span class="sxs-lookup"><span data-stu-id="9bfb7-127">Select **Turn on ATP for SharePoint, OneDrive, and Microsoft Teams**.</span></span><br/><span data-ttu-id="9bfb7-128">![Ativar a proteção avançada contra ameaças para o SharePoint Online, o OneDrive for Business e o Microsoft Teams](media/48cfaace-59cc-4e60-bf86-05ff6b99bdbf.png)</span><span class="sxs-lookup"><span data-stu-id="9bfb7-128">![Turn on Advanced Threat Protection for SharePoint Online, OneDrive for Business, and Microsoft Teams](media/48cfaace-59cc-4e60-bf86-05ff6b99bdbf.png)</span></span>
  
4. <span data-ttu-id="9bfb7-129">Clique em **Salvar**.</span><span class="sxs-lookup"><span data-stu-id="9bfb7-129">Click **Save**.</span></span>
    
5. <span data-ttu-id="9bfb7-130">Revise (e, conforme apropriado, edite) as [políticas de anexos seguros](set-up-atp-safe-attachments-policies.md) da sua organização e [as políticas de links seguros](set-up-atp-safe-links-policies.md).</span><span class="sxs-lookup"><span data-stu-id="9bfb7-130">Review (and, as appropriate, edit) your organization's [Safe Attachments policies](set-up-atp-safe-attachments-policies.md) and [Safe Links policies](set-up-atp-safe-links-policies.md).</span></span>
    
6. <span data-ttu-id="9bfb7-131">Recomenda Como administrador global ou administrador do SharePoint Online, execute o cmdlet **[set-SPOTenant](https://docs.microsoft.com/powershell/module/sharepoint-online/Set-SPOTenant?view=sharepoint-ps)** com o parâmetro **DisallowInfectedFileDownload** definido como *true*.</span><span class="sxs-lookup"><span data-stu-id="9bfb7-131">(Recommended) As a global administrator or a SharePoint Online administrator, run the **[Set-SPOTenant](https://docs.microsoft.com/powershell/module/sharepoint-online/Set-SPOTenant?view=sharepoint-ps)** cmdlet with the **DisallowInfectedFileDownload** parameter set to  *true*.</span></span> <br/>
      - <span data-ttu-id="9bfb7-p105">Definir o parâmetro como *true* bloqueia todas as ações (exceto excluir) para arquivos detectados. As pessoas não podem abrir, mover, copiar ou compartilhar arquivos detectados.</span><span class="sxs-lookup"><span data-stu-id="9bfb7-p105">Setting the parameter to *true* blocks all actions (except Delete) for detected files. People cannot open, move, copy, or share detected files.</span></span>
      - <span data-ttu-id="9bfb7-p106">A definição do parâmetro como *false* bloqueia todas as ações, exceto excluir e baixar. As pessoas podem optar por aceitar o risco e baixar um arquivo detectado.</span><span class="sxs-lookup"><span data-stu-id="9bfb7-p106">Setting the parameter to *false* blocks all actions except Delete and Download. People can choose to accept the risk and download a detected file.</span></span>  
   
7. <span data-ttu-id="9bfb7-136">Aguarde até 30 minutos para que as alterações se espalhem para todos os datacenters do Office 365.</span><span class="sxs-lookup"><span data-stu-id="9bfb7-136">Allow up to 30 minutes for your changes to spread to all Office 365 datacenters.</span></span>
    
8. <span data-ttu-id="9bfb7-137">Recomenda Vá para configurar alertas para arquivos detectados.</span><span class="sxs-lookup"><span data-stu-id="9bfb7-137">(Recommended) Proceed to set up alerts for detected files.</span></span>
    
<span data-ttu-id="9bfb7-138">Para saber mais sobre como usar o PowerShell com o Office 365, confira [gerenciar o office 365 com o PowerShell](https://docs.microsoft.com/office365/enterprise/powershell/manage-office-365-with-office-365-powershell).</span><span class="sxs-lookup"><span data-stu-id="9bfb7-138">To learn more about using PowerShell with Office 365, see [Manage Office 365 with PowerShell](https://docs.microsoft.com/office365/enterprise/powershell/manage-office-365-with-office-365-powershell).</span></span> 

<span data-ttu-id="9bfb7-139">Para saber mais sobre a experiência do usuário quando um arquivo foi detectado como mal-intencionado, confira [o que fazer quando um arquivo mal-intencionado é encontrado no SharePoint Online, no onedrive ou no Microsoft Teams](https://support.office.com/article/01e902ad-a903-4e0f-b093-1e1ac0c37ad2).</span><span class="sxs-lookup"><span data-stu-id="9bfb7-139">To learn more about the user experience when a file has been detected as malicious, see [What to do when a malicious file is found in SharePoint Online, OneDrive, or Microsoft Teams](https://support.office.com/article/01e902ad-a903-4e0f-b093-1e1ac0c37ad2).</span></span> 
  
## <a name="set-up-alerts-for-detected-files"></a><span data-ttu-id="9bfb7-140">Configurar alertas para arquivos detectados</span><span class="sxs-lookup"><span data-stu-id="9bfb7-140">Set up alerts for detected files</span></span>

<span data-ttu-id="9bfb7-141">Para receber notificações quando um arquivo no SharePoint Online, no OneDrive for Business ou no Microsoft Teams foi identificado como mal-intencionado, você pode configurar um alerta.</span><span class="sxs-lookup"><span data-stu-id="9bfb7-141">To receive notification when a file in SharePoint Online, OneDrive for Business, or Microsoft Teams has been identified as malicious, you can set up an alert.</span></span>
  
1. <span data-ttu-id="9bfb7-142">no [centro de conformidade de &amp; segurança do Office 365](https://protection.office.com), escolha **alertas** \> **gerenciar alertas**.</span><span class="sxs-lookup"><span data-stu-id="9bfb7-142">In the [Office 365 Security &amp; Compliance Center](https://protection.office.com), choose **Alerts** \> **Manage alerts**.</span></span>
    
2. <span data-ttu-id="9bfb7-143">Escolha **nova política de alerta**.</span><span class="sxs-lookup"><span data-stu-id="9bfb7-143">Choose **New alert policy**.</span></span>
    
3. <span data-ttu-id="9bfb7-p107">Especifique um nome para o alerta. Por exemplo, você pode digitar arquivos mal-intencionados em bibliotecas.</span><span class="sxs-lookup"><span data-stu-id="9bfb7-p107">Specify a name for the alert. For example, you could type Malicious Files in Libraries.</span></span>
    
4. <span data-ttu-id="9bfb7-p108">Digite uma descrição para o alerta. Por exemplo, você pode digitar notifica os administradores quando arquivos mal-intencionados são detectados no SharePoint Online, no OneDrive ou no Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="9bfb7-p108">Type a description for the alert. For example, you could type Notifies admins when malicious files are detected in SharePoint Online, OneDrive, or Microsoft Teams.</span></span>
    
5. <span data-ttu-id="9bfb7-148">Na seção **Enviar este alerta quando...** , faça o seguinte:</span><span class="sxs-lookup"><span data-stu-id="9bfb7-148">In the **Send this alert when...** section, do the following:</span></span> 
    
    <span data-ttu-id="9bfb7-p109">a. na lista **atividades** , escolha **malware detectado em arquivo**.</span><span class="sxs-lookup"><span data-stu-id="9bfb7-p109">a. In the **Activities** list, choose **Detected malware in file**.</span></span>
    
    <span data-ttu-id="9bfb7-p110">b. deixe o campo **usuários** vazio.</span><span class="sxs-lookup"><span data-stu-id="9bfb7-p110">b. Leave the **Users** field empty.</span></span> 
    
6. <span data-ttu-id="9bfb7-153">Na seção **Enviar este alerta para...** , selecione um ou mais administradores globais, administradores de segurança ou leitores de segurança que devem receber notificações quando um arquivo mal-intencionado for detectado.</span><span class="sxs-lookup"><span data-stu-id="9bfb7-153">In the **Send this alert to...** section, select one or more global administrators, security administrators, or security readers who should receive notification when a malicious file is detected.</span></span> 
    
7. <span data-ttu-id="9bfb7-154">Clique em **Salvar**.</span><span class="sxs-lookup"><span data-stu-id="9bfb7-154">Click **Save**.</span></span>
    
<span data-ttu-id="9bfb7-155">Para saber mais sobre alertas, confira [criar alertas de atividade no centro de &amp; conformidade de segurança do Office 365](create-activity-alerts.md).</span><span class="sxs-lookup"><span data-stu-id="9bfb7-155">To learn more about alerts, see [Create activity alerts in the Office 365 Security &amp; Compliance Center](create-activity-alerts.md).</span></span> 
  
## <a name="next-steps"></a><span data-ttu-id="9bfb7-156">Próximas etapas</span><span class="sxs-lookup"><span data-stu-id="9bfb7-156">Next steps</span></span>

1. [<span data-ttu-id="9bfb7-157">Exibir informações sobre arquivos mal-intencionados detectados no SharePoint, no OneDrive ou no Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="9bfb7-157">View information about malicious files detected in SharePoint, OneDrive, or Microsoft Teams</span></span>](malicious-files-detected-in-spo-odb-or-teams.md)
    
2. [<span data-ttu-id="9bfb7-158">Gerenciar arquivos e mensagens em quarentena como um administrador no Office 365</span><span class="sxs-lookup"><span data-stu-id="9bfb7-158">Manage quarantined messages and files as an administrator in Office 365</span></span>](manage-quarantined-messages-and-files.md)
    

  

