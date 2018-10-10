---
title: Exibir informações sobre arquivos mal-intencionados detectada no SharePoint, OneDrive ou Teams da Microsoft
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
ms.assetid: 5ed8abf1-c0e9-4e5b-a5b7-2059cea50b61
description: Saiba como tirar ação nesses arquivos e aonde ir para exibir informações sobre arquivos mal-intencionados detectada no SharePoint, OneDrive ou equipes.
ms.openlocfilehash: 370e5e3d4d7fd5f35caa8ef993f6245d15ee9999
ms.sourcegitcommit: 099bbfb1d16b251fd5cf18ec6515faaf9a989176
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25454268"
---
# <a name="view-information-about-malicious-files-detected-in-sharepoint-onedrive-or-microsoft-teams"></a><span data-ttu-id="03ca8-103">Exibir informações sobre arquivos mal-intencionados detectada no SharePoint, OneDrive ou Teams da Microsoft</span><span class="sxs-lookup"><span data-stu-id="03ca8-103">View information about malicious files detected in SharePoint, OneDrive, or Microsoft Teams</span></span>

<span data-ttu-id="03ca8-p101">[ATP do Office 365 para SharePoint, OneDrive e as equipes da Microsoft](atp-for-spo-odb-and-teams.md) protege a sua organização contra mal-intencionado arquivos em bibliotecas de documentos e sites de equipe. Quando um arquivo mal-intencionado é detectado, esse arquivo está bloqueado para que ninguém pode abrir, copiar, mover ou compartilhá-la até que outras ações são executadas pela equipe de segurança da organização. Leia este artigo para saber como exibir informações sobre arquivos detectados e quais ações tomar.</span><span class="sxs-lookup"><span data-stu-id="03ca8-p101">[Office 365 ATP for SharePoint, OneDrive, and Microsoft Teams](atp-for-spo-odb-and-teams.md) protects your organization from malicious files in document libraries and team sites. When a malicious file is detected, that file is blocked so that no one can open, copy, move, or share it until further actions are taken by the organization's security team. Read this article to learn how to view information about detected files and what actions to take.</span></span> 

<span data-ttu-id="03ca8-107">Para executar as tarefas descritas neste artigo, você deve ter o necessário [permissões atribuídas no Office 365 Security &amp; Centro de conformidade](permissions-in-the-security-and-compliance-center.md).</span><span class="sxs-lookup"><span data-stu-id="03ca8-107">In order to perform the tasks described in this article, you must have the necessary [permissions assigned in the Office 365 Security &amp; Compliance Center](permissions-in-the-security-and-compliance-center.md).</span></span> 
  
## <a name="view-reports-with-information-about-detected-files"></a><span data-ttu-id="03ca8-108">Exibir relatórios com informações sobre arquivos detectados</span><span class="sxs-lookup"><span data-stu-id="03ca8-108">View reports with information about detected files</span></span>

<span data-ttu-id="03ca8-109">Para exibir o status e informações detalhadas sobre arquivos que foram detectados pelo Office 365 ATP, você pode usar o relatório de status de proteção de ameaça.</span><span class="sxs-lookup"><span data-stu-id="03ca8-109">To view status and detailed information about files that were detected by Office 365 ATP, you can use the Threat protection status report.</span></span>
  
1. <span data-ttu-id="03ca8-110">No Office 365 Security &amp; Centro de conformidade, escolha **relatórios** \> **painel** \> **o status de proteção de ameaça**.</span><span class="sxs-lookup"><span data-stu-id="03ca8-110">In the Office 365 Security &amp; Compliance Center, choose **Reports** \> **Dashboard** \> **Threat protection status**.</span></span>
    
2. <span data-ttu-id="03ca8-111">No canto superior direito do relatório, escolha **tabela do modo de exibição detalhes**.</span><span class="sxs-lookup"><span data-stu-id="03ca8-111">In the upper right corner of the report, choose **View details table**.</span></span>
    
3. <span data-ttu-id="03ca8-112">Exiba a lista de arquivos que foram detectados no relatório.</span><span class="sxs-lookup"><span data-stu-id="03ca8-112">View the list of files that were detected in the report.</span></span>
    
4. <span data-ttu-id="03ca8-113">Selecione um item na lista para exibir informações detalhadas, incluindo as ações realizadas, o nome do arquivo, o caminho do arquivo e muito mais.</span><span class="sxs-lookup"><span data-stu-id="03ca8-113">Select an item in the list to view detailed information, including actions taken, the file name, the file path, and more.</span></span>
    
5. <span data-ttu-id="03ca8-114">Escolha a guia **Advanced Analysis** para exibir informações, como detalhes de análise e comportamento observados.</span><span class="sxs-lookup"><span data-stu-id="03ca8-114">Choose the **Advanced Analysis** tab to view information, such as observed behavior and analysis details.</span></span> 
  
## <a name="view-and-take-action-on-files-in-quarantine"></a><span data-ttu-id="03ca8-115">Exibir e agir em arquivos em quarentena</span><span class="sxs-lookup"><span data-stu-id="03ca8-115">View and take action on files in quarantine</span></span>

1. <span data-ttu-id="03ca8-116">No Office 365 Security &amp; Centro de conformidade, escolha **gerenciamento de ameaça** \> **revisão** \> **quarentena**.</span><span class="sxs-lookup"><span data-stu-id="03ca8-116">In the Office 365 Security &amp; Compliance Center, choose **Threat management** \> **Review** \> **Quarantine**.</span></span>
    
2. <span data-ttu-id="03ca8-117">No canto superior esquerdo, altere o filtro de **Email** para o **conteúdo**.</span><span class="sxs-lookup"><span data-stu-id="03ca8-117">In the upper left corner, change the filter from **Email** to **Content**.</span></span>
    
3. <span data-ttu-id="03ca8-118">Selecione um item na lista para exibir informações detalhadas, incluindo a URL do arquivo.</span><span class="sxs-lookup"><span data-stu-id="03ca8-118">Select an item in the list to view detailed information, including the file's URL.</span></span>
    
4. <span data-ttu-id="03ca8-119">Escolha uma ação disponível.</span><span class="sxs-lookup"><span data-stu-id="03ca8-119">Choose an available action.</span></span>
    
  - <span data-ttu-id="03ca8-120">Escolha **versão &amp; relatório** para desbloquear o arquivo.</span><span class="sxs-lookup"><span data-stu-id="03ca8-120">Choose **Release &amp; report** to unblock the file.</span></span> 
    
    <span data-ttu-id="03ca8-121">Selecione **enviar o relatório para a Microsoft** para relatar o arquivo como um falso positivo para a Microsoft.</span><span class="sxs-lookup"><span data-stu-id="03ca8-121">Select **Send report to Microsoft** to report the file as a false positive to Microsoft.</span></span> 
    
  - <span data-ttu-id="03ca8-122">Escolha a **baixar o arquivo** para investigar ainda mais o arquivo.</span><span class="sxs-lookup"><span data-stu-id="03ca8-122">Choose **Download file** to investigate the file further.</span></span> 
    
  - <span data-ttu-id="03ca8-p102">Escolha **Excluir** para remover o arquivo da lista de itens em quarentena. Se você escolher essa opção, você também deve excluir o arquivo de seu respectiva biblioteca no SharePoint Online, OneDrive para negócios ou Teams da Microsoft. Essa opção não desbloquear um arquivo sejam abertos ou compartilhado.</span><span class="sxs-lookup"><span data-stu-id="03ca8-p102">Choose **Delete** to remove the file from the list of quarantined items. If you choose this option, you must also delete the file from its respective library in SharePoint Online, OneDrive for Business, or Microsoft Teams. This option does not unblock a file from being opened or shared.</span></span> 
    
5. <span data-ttu-id="03ca8-126">Escolha **Fechar** para fechar os detalhes para um item selecionado.</span><span class="sxs-lookup"><span data-stu-id="03ca8-126">Choose **Close** to close the details for a selected item.</span></span> 
  
## <a name="related-topics"></a><span data-ttu-id="03ca8-127">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="03ca8-127">Related topics</span></span>

<span data-ttu-id="03ca8-128">[Proteção Avançada contra Ameaças do Office 365](office-365-atp.md) </span><span class="sxs-lookup"><span data-stu-id="03ca8-128">[Office 365 Advanced Threat Protection](office-365-atp.md)</span></span>
  
[<span data-ttu-id="03ca8-129">Exibir os relatórios de proteção de ameaça avançadas do Office 365</span><span class="sxs-lookup"><span data-stu-id="03ca8-129">View the reports for Office 365 Advanced Threat Protection</span></span>](view-reports-for-atp.md)
  
[<span data-ttu-id="03ca8-130">Permissões de segurança do Office 365 &amp; Centro de conformidade</span><span class="sxs-lookup"><span data-stu-id="03ca8-130">Permissions in the Office 365 Security &amp; Compliance Center</span></span>](permissions-in-the-security-and-compliance-center.md)

[<span data-ttu-id="03ca8-131">Gerenciar arquivos e mensagens em quarentena como um administrador no Office 365</span><span class="sxs-lookup"><span data-stu-id="03ca8-131">Manage quarantined messages and files as an administrator in Office 365</span></span>](manage-quarantined-messages-and-files.md)
  

