---
title: Office 365 ATP para SharePoint, OneDrive e Microsoft Teams
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 6/18/2018
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 26261670-db33-4c53-b125-af0662c34607
description: Estenda a proteção de ameaça avançadas do Office 365 para arquivos no SharePoint Online, o OneDrive for Business e Teams da Microsoft habilitar a colaboração mais segura para sua organização.
ms.openlocfilehash: ea1c77273be70ce27f60bfaeae3544d605553a32
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22524478"
---
# <a name="office-365-atp-for-sharepoint-onedrive-and-microsoft-teams"></a><span data-ttu-id="05342-103">Office 365 ATP para SharePoint, OneDrive e Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="05342-103">Office 365 ATP for SharePoint, OneDrive, and Microsoft Teams</span></span>

<span data-ttu-id="05342-p101">Compartilhar arquivos de pessoas regularmente e colaborar através do SharePoint, OneDrive e Teams da Microsoft. Com [A proteção de ameaça avançadas do Office 365](office-365-atp.md) (ATP), sua organização pode colaborar de maneira mais segura. ATP ajuda a detectar e bloquear arquivos que são identificados como sendo maliciosas em bibliotecas de documentos e sites de equipe. Leia este artigo para obter uma visão geral dos ATP para SharePoint Online, o OneDrive for Business e Teams da Microsoft e, em seguida, siga as próximas etapas.</span><span class="sxs-lookup"><span data-stu-id="05342-p101">People regularly share files and collaborate using SharePoint, OneDrive, and Microsoft Teams. With [Office 365 Advanced Threat Protection](office-365-atp.md) (ATP), your organization can collaborate in a safer manner. ATP helps detect and block files that are identified as malicious in team sites and document libraries. Read this article to get an overview of ATP for SharePoint Online, OneDrive for Business, and Microsoft Teams, and then take your next steps.</span></span> 
  
> [!TIP]
> <span data-ttu-id="05342-p102">Para executar as tarefas descritas neste artigo, você deve ser um administrador global do Office 365 ou um administrador de segurança. Consulte [Permissions in a segurança do Office 365 &amp; Centro de conformidade](permissions-in-the-security-and-compliance-center.md).</span><span class="sxs-lookup"><span data-stu-id="05342-p102">In order to perform the tasks described in this article, you must be an Office 365 global administrator or a security administrator. See [Permissions in the Office 365 Security &amp; Compliance Center](permissions-in-the-security-and-compliance-center.md).</span></span> 
  
## <a name="how-it-works"></a><span data-ttu-id="05342-110">Como funciona</span><span class="sxs-lookup"><span data-stu-id="05342-110">How it works</span></span>

<span data-ttu-id="05342-p103">Quando um arquivo no SharePoint Online, o OneDrive for Business e Teams da Microsoft foi identificado como sendo maliciosas, ATP integra-se diretamente com os repositórios de arquivos de bloqueio de arquivo. A imagem a seguir mostra um exemplo de um arquivo mal-intencionado detectado em uma biblioteca.</span><span class="sxs-lookup"><span data-stu-id="05342-p103">When a file in SharePoint Online, OneDrive for Business, and Microsoft Teams has been identified as malicious, ATP directly integrates with the file stores to lock that file. The following image shows an example of a malicious file detected in a library.</span></span>
  
<span data-ttu-id="05342-113">[![Captura de tela de arquivos no OneDrive for Business com um detectada como mal-intencionado](media/2bba71cc-7ad1-4799-8b9d-d56f923db3a7.png)](https://support.office.com/article/01e902ad-a903-4e0f-b093-1e1ac0c37ad2)</span><span class="sxs-lookup"><span data-stu-id="05342-113">[![Screenshot of files in OneDrive for Business with one detected as malicious](media/2bba71cc-7ad1-4799-8b9d-d56f923db3a7.png)](https://support.office.com/article/01e902ad-a903-4e0f-b093-1e1ac0c37ad2)</span></span>
  
<span data-ttu-id="05342-p104">Embora os arquivos bloqueados ainda está listado na biblioteca de documentos e web, aplicativos móveis ou de mesa, os arquivos bloqueados não podem ser aberto, copiado, movido ou shared. Pessoas podem, no entanto, excluir um arquivo bloqueado. Aqui está um exemplo de quais que se parece com no dispositivo móvel de um usuário:</span><span class="sxs-lookup"><span data-stu-id="05342-p104">Although the blocked file is still listed in the document library and web, mobile, or desktop applications, the blocked file cannot be opened, copied, moved, or shared. People can, however, delete a blocked file. Here's an example of what that looks like on a user's mobile device:</span></span>
  
<span data-ttu-id="05342-117">[![Captura de tela da exclusão de um arquivo bloqueado do OneDrive for Business do app móvel OneDrive](media/cb1c1705-fd0a-45b8-9a26-c22503011d54.png)](https://support.office.com/article/01e902ad-a903-4e0f-b093-1e1ac0c37ad2)</span><span class="sxs-lookup"><span data-stu-id="05342-117">[![Screenshot of deleting a blocked file from OneDrive for Business from the OneDrive mobile app](media/cb1c1705-fd0a-45b8-9a26-c22503011d54.png)](https://support.office.com/article/01e902ad-a903-4e0f-b093-1e1ac0c37ad2)</span></span>
  
<span data-ttu-id="05342-p105">Dependendo de como o Office 365 é configurada, as pessoas podem ou podem não ter a capacidade de fazer o download de um arquivo bloqueado. Aqui está o download de arquivos bloqueados aparência no dispositivo móvel de um usuário:</span><span class="sxs-lookup"><span data-stu-id="05342-p105">Depending on how Office 365 is configured, people might or might not have the ability to download a blocked file. Here's what downloading a blocked file looks like on a user's mobile device:</span></span>
  
<span data-ttu-id="05342-120">[![Captura de tela de download de arquivos bloqueados no OneDrive for Business](media/be288a82-bdd8-4371-93d8-1783db3b61bc.png)](https://support.office.com/article/01e902ad-a903-4e0f-b093-1e1ac0c37ad2)</span><span class="sxs-lookup"><span data-stu-id="05342-120">[![Screenshot of downloading a blocked file in OneDrive for Business](media/be288a82-bdd8-4371-93d8-1783db3b61bc.png)](https://support.office.com/article/01e902ad-a903-4e0f-b093-1e1ac0c37ad2)</span></span>
  
<span data-ttu-id="05342-121">Para saber mais, consulte [Ativar ATP do Office 365 para SharePoint, OneDrive e as equipes da Microsoft](turn-on-atp-for-spo-odb-and-teams.md).</span><span class="sxs-lookup"><span data-stu-id="05342-121">To learn more, see [Turn on Office 365 ATP for SharePoint, OneDrive, and Microsoft Teams](turn-on-atp-for-spo-odb-and-teams.md).</span></span>
  
### <a name="keep-the-following-points-in-mind"></a><span data-ttu-id="05342-122">Tenha em mente os seguintes pontos</span><span class="sxs-lookup"><span data-stu-id="05342-122">Keep the following points in mind</span></span>

- <span data-ttu-id="05342-p106">ATP não examinará cada arquivo no SharePoint Online, OneDrive para negócios ou Teams da Microsoft. Isso ocorre por design. Os arquivos são examinados assincronamente, por meio de um processo que usa os eventos de atividade de compartilhamento e de convidado, juntamente com os sinais de ameaça e heurístico inteligente para identificar arquivos mal-intencionados.</span><span class="sxs-lookup"><span data-stu-id="05342-p106">ATP will not scan every single file in SharePoint Online, OneDrive for Business, or Microsoft Teams. This is by design. Files are scanned asynchronously, through a process that uses sharing and guest activity events along with smart heuristics and threat signals to identify malicious files.</span></span>
    
- <span data-ttu-id="05342-126">Arquivos que são identificados como mal-intencionado no SharePoint Online, OneDrive for Business ou Microsoft Teams serão exibidas nos [relatórios de proteção de ameaça avançadas do Office 365](view-reports-for-atp.md) e no Explorer de ameaça (parte do [Office 365 Threat Intelligence](office-365-ti.md)).</span><span class="sxs-lookup"><span data-stu-id="05342-126">Files that are identified as malicious in SharePoint Online, OneDrive for Business, or Microsoft Teams will show up in [reports for Office 365 Advanced Threat Protection](view-reports-for-atp.md) and in Threat Explorer (part of [Office 365 Threat Intelligence](office-365-ti.md)).</span></span>
    
- <span data-ttu-id="05342-p107">ATP é parte da estratégia geral de ameaça proteção sua organização, que inclui recursos anti-spam e proteção contra malware, bem como Links seguros e anexos seguros. Para saber mais, consulte [proteger contra ameaças no Office 365](protect-against-threats.md).</span><span class="sxs-lookup"><span data-stu-id="05342-p107">ATP is part of your organization's overall threat protection strategy, which includes anti-spam and anti-malware protection, as well as Safe Links and Safe Attachments. To learn more, see [Protect against threats in Office 365](protect-against-threats.md).</span></span>
    
- <span data-ttu-id="05342-p108">Um administrador do SharePoint Online pode determinar se deseja habilitar pessoas baixar arquivos que são detectados como sendo maliciosas. Isso é feito executando o cmdlet Set-SPOTenant PowerShell usando um parâmetro de DisallowInfectedFileDownload (consulte [ativem ATP do Office 365 para SharePoint, OneDrive e as equipes da Microsoft](turn-on-atp-for-spo-odb-and-teams.md)).</span><span class="sxs-lookup"><span data-stu-id="05342-p108">A SharePoint Online administrator can determine whether to enable people to download files that are detected as malicious. This is done by running the Set-SPOTenant PowerShell cmdlet using a DisallowInfectedFileDownload parameter (see [Turn on Office 365 ATP for SharePoint, OneDrive, and Microsoft Teams](turn-on-atp-for-spo-odb-and-teams.md)).</span></span>
    
## <a name="new-quarantine-in-atp-for-sharepoint-online-onedrive-for-business-and-microsoft-teams"></a><span data-ttu-id="05342-131">(Novo)! Quarentena no ATP para SharePoint Online, o OneDrive for Business e equipes da Microsoft</span><span class="sxs-lookup"><span data-stu-id="05342-131">(New!) Quarantine in ATP for SharePoint Online, OneDrive for Business, and Microsoft Teams</span></span>

 <span data-ttu-id="05342-132">* * Iniciando no tardia de 2018 de maio, recursos de [quarentena](quarantine-email-messages.md) na segurança &amp; Centro de conformidade estão sendo estendidas para ATP para SharePoint Online, OneDrive for Business e Teams da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="05342-132">**Beginning in late May 2018, [quarantine](quarantine-email-messages.md) capabilities in the Security &amp; Compliance Center are being extended to ATP for SharePoint Online, OneDrive for Business, and Microsoft Teams.</span></span> **
  
<span data-ttu-id="05342-p109">Quando um arquivo no SharePoint Online, o OneDrive for Business ou Teams da Microsoft é identificado como mal-intencionado, além de ATP bloqueando o arquivo de ser aberto ou compartilhado, esse arquivo está incluído em uma lista de itens em quarentena. (Na segurança &amp; Centro de conformidade, vá para **gerenciamento de ameaça** \> **revisão** \> **quarentena** e filtro de conteúdo.)</span><span class="sxs-lookup"><span data-stu-id="05342-p109">When a file in SharePoint Online, OneDrive for Business, or Microsoft Teams is identified as malicious, in addition to ATP blocking the file from being opened or shared, that file is included in a list of quarantined items. (In the Security &amp; Compliance Center, go to **Threat management** \> **Review** \> **Quarantine** and filter for Content.)</span></span> 
  
<span data-ttu-id="05342-135">Caso você seja parte da equipe de segurança do Office 365 da sua organização e tem os necessários [permissões atribuídas no Office 365 Security &amp; Centro de conformidade](permissions-in-the-security-and-compliance-center.md), você pode baixar, versão, relatar e exclua arquivos que são detectados como sendo maliciosas pelo ATP da quarentena.</span><span class="sxs-lookup"><span data-stu-id="05342-135">If you're part of your organization's Office 365 security team and have the necessary [permissions assigned in the Office 365 Security &amp; Compliance Center](permissions-in-the-security-and-compliance-center.md), you can download, release, report, and delete files that are detected as malicious by ATP from quarantine.</span></span>
  
- <span data-ttu-id="05342-p110">**Liberando e relatórios de** um arquivo remove o bloco de ATP no arquivo a respectivos team site ou biblioteca de documentos do SharePoint, OneDrive ou Teams da Microsoft. Os usuários são então capazes de abrir, compartilhar e baixe o arquivo. E, quando a opção **enviar o relatório para a Microsoft** está selecionada, o arquivo é relatado como um falso positivo para a Microsoft.</span><span class="sxs-lookup"><span data-stu-id="05342-p110">**Releasing and reporting** a file removes the ATP block on the file in the respective team site or document library for SharePoint, OneDrive, or Microsoft Teams. Users are then able to open, share, and download the file. And, when the **Send report to Microsoft** option is selected, the file is reported as a false positive to Microsoft.</span></span> 
    
- <span data-ttu-id="05342-p111">**Excluir um arquivo** remove o arquivo da quarentena; No entanto, o arquivo ainda está bloqueado sejam abertos ou compartilhado. O arquivo também deve ser excluído em seu respectivos biblioteca ou equipe site de documentos (SharePoint Online, OneDrive for Business ou Teams da Microsoft).</span><span class="sxs-lookup"><span data-stu-id="05342-p111">**Deleting a file** removes the file from quarantine; however, the file is still blocked from being opened or shared. The file must also be deleted in its respective document library or team site (SharePoint Online, OneDrive for Business, or Microsoft Teams).</span></span> 
    
- <span data-ttu-id="05342-141">**Download de um arquivo** permite que você baixe e analisar o arquivo para qualquer falsos positivos.</span><span class="sxs-lookup"><span data-stu-id="05342-141">**Downloading a file** enables you to download and analyze the file for any false positives.</span></span> 
    
## <a name="next-steps"></a><span data-ttu-id="05342-142">Próximas etapas</span><span class="sxs-lookup"><span data-stu-id="05342-142">Next steps</span></span>

- [<span data-ttu-id="05342-143">Ativar o Office 365 ATP para SharePoint, OneDrive e equipes da Microsoft</span><span class="sxs-lookup"><span data-stu-id="05342-143">Turn on Office 365 ATP for SharePoint, OneDrive, and Microsoft Teams</span></span>](turn-on-atp-for-spo-odb-and-teams.md)
    
- [<span data-ttu-id="05342-144">Exibir informações sobre arquivos mal-intencionados detectada no SharePoint, OneDrive ou Teams da Microsoft</span><span class="sxs-lookup"><span data-stu-id="05342-144">View information about malicious files detected in SharePoint, OneDrive, or Microsoft Teams</span></span>](malicious-files-detected-in-spo-odb-or-teams.md)
    
## <a name="related-topics"></a><span data-ttu-id="05342-145">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="05342-145">Related topics</span></span>

<span data-ttu-id="05342-146">[Proteção Avançada contra Ameaças do Office 365](office-365-atp.md) </span><span class="sxs-lookup"><span data-stu-id="05342-146">[Office 365 Advanced Threat Protection](office-365-atp.md)</span></span>
  
[<span data-ttu-id="05342-147">Exibir os relatórios de proteção de ameaça avançadas do Office 365</span><span class="sxs-lookup"><span data-stu-id="05342-147">View the reports for Office 365 Advanced Threat Protection</span></span>](view-reports-for-atp.md)
  
[<span data-ttu-id="05342-148">Permissões de segurança do Office 365 &amp; Centro de conformidade</span><span class="sxs-lookup"><span data-stu-id="05342-148">Permissions in the Office 365 Security &amp; Compliance Center</span></span>](permissions-in-the-security-and-compliance-center.md)
  

