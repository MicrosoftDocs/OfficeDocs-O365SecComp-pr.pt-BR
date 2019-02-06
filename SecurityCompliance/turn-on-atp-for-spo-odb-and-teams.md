---
title: Ativar o Office 365 ATP para SharePoint, OneDrive e equipes da Microsoft
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.audience: ITPro
ms.topic: article
ms.date: 02/05/2019
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 07e76024-0c80-40dc-8c48-1dd0d0f863cb
description: Saiba como ativar ATP para o SharePoint, OneDrive e equipes, incluindo como configurar alertas para arquivos detectados.
ms.openlocfilehash: 23eaa4def0fafdcd0df0ae30f8358104c0f877b6
ms.sourcegitcommit: a64af0ebd0b03e4a5e60a33e9108c44c7d74f356
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/05/2019
ms.locfileid: "29741024"
---
# <a name="turn-on-office-365-atp-for-sharepoint-onedrive-and-microsoft-teams"></a><span data-ttu-id="565f8-103">Ativar o Office 365 ATP para SharePoint, OneDrive e equipes da Microsoft</span><span class="sxs-lookup"><span data-stu-id="565f8-103">Turn on Office 365 ATP for SharePoint, OneDrive, and Microsoft Teams</span></span>

<span data-ttu-id="565f8-p101">[ATP do Office 365 para SharePoint, OneDrive e as equipes da Microsoft](atp-for-spo-odb-and-teams.md) protege a sua organização contra inadvertidamente compartilhamento de arquivos mal-intencionados. Quando um arquivo mal-intencionado é detectado, esse arquivo está bloqueado para que ninguém pode abrir, copiar, mover ou compartilhá-la até que outras ações são executadas pela equipe de segurança da organização. Leia este artigo para ativar ATP para SharePoint, OneDrive e equipes, configure os alertas para ser notificado sobre arquivos detectados e siga as próximas etapas.</span><span class="sxs-lookup"><span data-stu-id="565f8-p101">[Office 365 ATP for SharePoint, OneDrive, and Microsoft Teams](atp-for-spo-odb-and-teams.md) protects your organization from inadvertently sharing malicious files. When a malicious file is detected, that file is blocked so that no one can open, copy, move, or share it until further actions are taken by the organization's security team. Read this article to turn on ATP for SharePoint, OneDrive, and Teams, set up alerts to be notified about detected files, and take your next steps.</span></span> 
  
<span data-ttu-id="565f8-107">Para definir (ou editar) políticas ATP, você deve ter uma das funções descritas na tabela a seguir:</span><span class="sxs-lookup"><span data-stu-id="565f8-107">To define (or edit) ATP policies, you must be assigned one of the roles described in the following table:</span></span>

|<span data-ttu-id="565f8-108">Função</span><span class="sxs-lookup"><span data-stu-id="565f8-108">Role</span></span>  |<span data-ttu-id="565f8-109">Onde/como atribuído</span><span class="sxs-lookup"><span data-stu-id="565f8-109">Where/how assigned</span></span>  |
|---------|---------|
|<span data-ttu-id="565f8-110">Administrador Global do Office 365</span><span class="sxs-lookup"><span data-stu-id="565f8-110">Office 365 Global Administrator</span></span> |<span data-ttu-id="565f8-p102">A pessoa que se inscreve para comprar o Office 365 é um administrador global por padrão. (Consulte [funções de administrador do Office 365](https://docs.microsoft.com/office365/admin/add-users/about-admin-roles) para saber mais).</span><span class="sxs-lookup"><span data-stu-id="565f8-p102">The person who signs up to buy Office 365 is a global admin by default. (See [About Office 365 admin roles](https://docs.microsoft.com/office365/admin/add-users/about-admin-roles) to learn more.)</span></span>         |
|<span data-ttu-id="565f8-113">Administrador de segurança do Office 365</span><span class="sxs-lookup"><span data-stu-id="565f8-113">Office 365 Security Administrator</span></span> |<span data-ttu-id="565f8-114">Centro de administração ([https://aka.ms/admincenter](https://aka.ms/admincenter))</span><span class="sxs-lookup"><span data-stu-id="565f8-114">Admin center ([https://aka.ms/admincenter](https://aka.ms/admincenter))</span></span>|
|<span data-ttu-id="565f8-115">Gerenciamento de organização Online do Exchange</span><span class="sxs-lookup"><span data-stu-id="565f8-115">Exchange Online Organization Management</span></span> |<span data-ttu-id="565f8-116">Centro de administração do Exchange ([https://outlook.office365.com/ecp](https://outlook.office365.com/ecp))</span><span class="sxs-lookup"><span data-stu-id="565f8-116">Exchange admin center ([https://outlook.office365.com/ecp](https://outlook.office365.com/ecp))</span></span> <br><span data-ttu-id="565f8-117">ou</span><span class="sxs-lookup"><span data-stu-id="565f8-117">or</span></span> <br>  <span data-ttu-id="565f8-118">Cmdlets do PowerShell (consulte [PowerShell do Exchange Online](https://docs.microsoft.com/powershell/exchange/exchange-online/exchange-online-powershell?view=exchange-ps))</span><span class="sxs-lookup"><span data-stu-id="565f8-118">PowerShell cmdlets (See [Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/exchange-online-powershell?view=exchange-ps))</span></span> |
  
## <a name="turn-on-atp-for-sharepoint-onedrive-and-microsoft-teams"></a><span data-ttu-id="565f8-119">Ativar a ATP para SharePoint, OneDrive e Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="565f8-119">Turn on ATP for SharePoint, OneDrive, and Microsoft Teams</span></span>

<span data-ttu-id="565f8-p103">**Antes de começar esse procedimento, certifique-se de que os logs de auditoria já esteja ativado para o seu ambiente do Office 365**. Normalmente, isso é feito por alguém que tenha a função de Logs de auditoria atribuída no Exchange Online. Para obter mais informações, consulte [Ativar o Office 365 pesquisa de log de auditoria ativado ou desativado](turn-audit-log-search-on-or-off.md).</span><span class="sxs-lookup"><span data-stu-id="565f8-p103">**Before you begin this procedure, make sure that audit logging is already turned on for your Office 365 environment**. This is typically done by someone who has the Audit Logs role assigned in Exchange Online. For more information, see [Turn Office 365 audit log search on or off](turn-audit-log-search-on-or-off.md).</span></span>
  
1. <span data-ttu-id="565f8-123">Vá para [https://protection.office.com](https://protection.office.com)e entre com sua conta do trabalho ou da escola.</span><span class="sxs-lookup"><span data-stu-id="565f8-123">Go to [https://protection.office.com](https://protection.office.com), and sign in with your work or school account.</span></span>
    
2. <span data-ttu-id="565f8-124">No Office 365 Security &amp; Centro de conformidade, no painel de navegação à esquerda, em **gerenciamento de ameaça**, escolha **política** \> **Anexos seguros**.</span><span class="sxs-lookup"><span data-stu-id="565f8-124">In the Office 365 Security &amp; Compliance Center, in the left navigation pane, under **Threat management**, choose **Policy** \> **Safe Attachments**.</span></span> <br/><span data-ttu-id="565f8-125">![Na segurança &amp; Centro de conformidade, escolha gerenciamento de ameaça \> política](media/08849c91-f043-4cd1-a55e-d440c86442f2.png)</span><span class="sxs-lookup"><span data-stu-id="565f8-125">![In the Security &amp; Compliance Center, choose Threat management \> Policy](media/08849c91-f043-4cd1-a55e-d440c86442f2.png)</span></span>
  
3. <span data-ttu-id="565f8-126">Selecione **Ativar ATP para SharePoint, OneDrive e as equipes da Microsoft**.</span><span class="sxs-lookup"><span data-stu-id="565f8-126">Select **Turn on ATP for SharePoint, OneDrive, and Microsoft Teams**.</span></span><br/><span data-ttu-id="565f8-127">![Ativar proteção contra ameaças avançado para SharePoint Online, o OneDrive for Business e equipes da Microsoft](media/48cfaace-59cc-4e60-bf86-05ff6b99bdbf.png)</span><span class="sxs-lookup"><span data-stu-id="565f8-127">![Turn on Advanced Threat Protection for SharePoint Online, OneDrive for Business, and Microsoft Teams](media/48cfaace-59cc-4e60-bf86-05ff6b99bdbf.png)</span></span>
  
4. <span data-ttu-id="565f8-128">Clique em **Salvar**.</span><span class="sxs-lookup"><span data-stu-id="565f8-128">Click **Save**.</span></span>
    
5. <span data-ttu-id="565f8-129">Revise (e, conforme apropriado, edite) as [políticas de Links seguros](set-up-atp-safe-links-policies.md)e as [políticas de segurança de anexos](set-up-atp-safe-attachments-policies.md) da sua organização.</span><span class="sxs-lookup"><span data-stu-id="565f8-129">Review (and, as appropriate, edit) your organization's [Safe Attachments policies](set-up-atp-safe-attachments-policies.md) and [Safe Links policies](set-up-atp-safe-links-policies.md).</span></span>
    
6. <span data-ttu-id="565f8-130">(Recomendado) Como um administrador global ou um administrador do SharePoint Online, execute o cmdlet **[Set-SPOTenant](https://docs.microsoft.com/powershell/module/sharepoint-online/Set-SPOTenant?view=sharepoint-ps)** com o parâmetro **DisallowInfectedFileDownload** definido como *true*.</span><span class="sxs-lookup"><span data-stu-id="565f8-130">(Recommended) As a global administrator or a SharePoint Online administrator, run the **[Set-SPOTenant](https://docs.microsoft.com/powershell/module/sharepoint-online/Set-SPOTenant?view=sharepoint-ps)** cmdlet with the **DisallowInfectedFileDownload** parameter set to  *true*.</span></span> <br/>
      - <span data-ttu-id="565f8-p104">Definindo o parâmetro para *true* bloqueia todas as ações (exceto excluir) para arquivos de detectados. As pessoas não podem abrir, mover, copiar ou compartilhar arquivos detectados.</span><span class="sxs-lookup"><span data-stu-id="565f8-p104">Setting the parameter to *true* blocks all actions (except Delete) for detected files. People cannot open, move, copy, or share detected files.</span></span>
      - <span data-ttu-id="565f8-p105">Configuração do parâmetro como *false* bloqueia todas as ações, exceto excluir e Download. Pessoas podem optar por aceitar o risco e baixar um arquivo detectado.</span><span class="sxs-lookup"><span data-stu-id="565f8-p105">Setting the parameter to *false* blocks all actions except Delete and Download. People can choose to accept the risk and download a detected file.</span></span>  
   
7. <span data-ttu-id="565f8-135">Permitir até 30 minutos para que suas alterações à difusão em todos os centros de dados do Office 365.</span><span class="sxs-lookup"><span data-stu-id="565f8-135">Allow up to 30 minutes for your changes to spread to all Office 365 datacenters.</span></span>
    
8. <span data-ttu-id="565f8-136">(Recomendado) Vá para configurar alertas para arquivos detectados.</span><span class="sxs-lookup"><span data-stu-id="565f8-136">(Recommended) Proceed to set up alerts for detected files.</span></span>
    
<span data-ttu-id="565f8-137">Para saber mais sobre como usar o PowerShell com o Office 365, consulte [Gerenciar o Office 365 com o PowerShell](https://docs.microsoft.com/office365/enterprise/powershell/manage-office-365-with-office-365-powershell).</span><span class="sxs-lookup"><span data-stu-id="565f8-137">To learn more about using PowerShell with Office 365, see [Manage Office 365 with PowerShell](https://docs.microsoft.com/office365/enterprise/powershell/manage-office-365-with-office-365-powershell).</span></span> 

<span data-ttu-id="565f8-138">Para saber mais sobre a experiência do usuário quando um arquivo foi detectado como mal-intencionado, consulte [o que fazer quando um arquivo mal-intencionado é encontrado no SharePoint Online, OneDrive ou equipes da Microsoft](https://support.office.com/article/01e902ad-a903-4e0f-b093-1e1ac0c37ad2).</span><span class="sxs-lookup"><span data-stu-id="565f8-138">To learn more about the user experience when a file has been detected as malicious, see [What to do when a malicious file is found in SharePoint Online, OneDrive, or Microsoft Teams](https://support.office.com/article/01e902ad-a903-4e0f-b093-1e1ac0c37ad2).</span></span> 
  
## <a name="set-up-alerts-for-detected-files"></a><span data-ttu-id="565f8-139">Configurar alertas para arquivos detectados</span><span class="sxs-lookup"><span data-stu-id="565f8-139">Set up alerts for detected files</span></span>

<span data-ttu-id="565f8-140">Para receber uma notificação quando um arquivo no SharePoint Online, OneDrive para negócios ou Microsoft Teams tenha sido identificado como mal-intencionado, você pode configurar um alerta.</span><span class="sxs-lookup"><span data-stu-id="565f8-140">To receive notification when a file in SharePoint Online, OneDrive for Business, or Microsoft Teams has been identified as malicious, you can set up an alert.</span></span>
  
1. <span data-ttu-id="565f8-141">Na [a segurança do Office 365 &amp; Centro de conformidade](https://protection.office.com), escolha **alertas** \> **Gerenciar alertas**.</span><span class="sxs-lookup"><span data-stu-id="565f8-141">In the [Office 365 Security &amp; Compliance Center](https://protection.office.com), choose **Alerts** \> **Manage alerts**.</span></span>
    
2. <span data-ttu-id="565f8-142">Escolha **nova política de alerta**.</span><span class="sxs-lookup"><span data-stu-id="565f8-142">Choose **New alert policy**.</span></span>
    
3. <span data-ttu-id="565f8-p106">Especifique um nome para o alerta. Por exemplo, você pode digitar arquivos mal-intencionados nas bibliotecas.</span><span class="sxs-lookup"><span data-stu-id="565f8-p106">Specify a name for the alert. For example, you could type Malicious Files in Libraries.</span></span>
    
4. <span data-ttu-id="565f8-p107">Digite uma descrição para o alerta. Por exemplo, você pode digitar emite admins quando arquivos mal-intencionados forem detectados no SharePoint Online, OneDrive ou Teams da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="565f8-p107">Type a description for the alert. For example, you could type Notifies admins when malicious files are detected in SharePoint Online, OneDrive, or Microsoft Teams.</span></span>
    
5. <span data-ttu-id="565f8-147">Na seção **enviar esse alerta quando …** , faça o seguinte:</span><span class="sxs-lookup"><span data-stu-id="565f8-147">In the **Send this alert when...** section, do the following:</span></span> 
    
    <span data-ttu-id="565f8-p108">r. na lista de **atividades** , escolha **malware detectado no arquivo**.</span><span class="sxs-lookup"><span data-stu-id="565f8-p108">a. In the **Activities** list, choose **Detected malware in file**.</span></span>
    
    <span data-ttu-id="565f8-p109">b. deixe o campo **usuários** vazio.</span><span class="sxs-lookup"><span data-stu-id="565f8-p109">b. Leave the **Users** field empty.</span></span> 
    
6. <span data-ttu-id="565f8-152">Na seção **enviar esse alerta para …** , selecione um ou mais administradores globais, os administradores de segurança ou leitores de segurança que devem receber uma notificação quando um arquivo mal-intencionado é detectado.</span><span class="sxs-lookup"><span data-stu-id="565f8-152">In the **Send this alert to...** section, select one or more global administrators, security administrators, or security readers who should receive notification when a malicious file is detected.</span></span> 
    
7. <span data-ttu-id="565f8-153">Clique em **Salvar**.</span><span class="sxs-lookup"><span data-stu-id="565f8-153">Click **Save**.</span></span>
    
<span data-ttu-id="565f8-154">Para saber mais sobre alertas, consulte [criar alertas de atividade no Office 365 Security &amp; Centro de conformidade](create-activity-alerts.md).</span><span class="sxs-lookup"><span data-stu-id="565f8-154">To learn more about alerts, see [Create activity alerts in the Office 365 Security &amp; Compliance Center](create-activity-alerts.md).</span></span> 
  
## <a name="next-steps"></a><span data-ttu-id="565f8-155">Próximas etapas</span><span class="sxs-lookup"><span data-stu-id="565f8-155">Next steps</span></span>

1. [<span data-ttu-id="565f8-156">Exibir informações sobre arquivos mal-intencionados detectada no SharePoint, OneDrive ou Teams da Microsoft</span><span class="sxs-lookup"><span data-stu-id="565f8-156">View information about malicious files detected in SharePoint, OneDrive, or Microsoft Teams</span></span>](malicious-files-detected-in-spo-odb-or-teams.md)
    
2. [<span data-ttu-id="565f8-157">Gerenciar arquivos e mensagens em quarentena como um administrador no Office 365</span><span class="sxs-lookup"><span data-stu-id="565f8-157">Manage quarantined messages and files as an administrator in Office 365</span></span>](manage-quarantined-messages-and-files.md)
    

  

