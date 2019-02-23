---
title: Exibir informações sobre arquivos mal-intencionados detectados no SharePoint, no OneDrive ou no Microsoft Teams
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 5ed8abf1-c0e9-4e5b-a5b7-2059cea50b61
description: Saiba onde ir para exibir informações sobre arquivos mal-intencionados detectados no SharePoint, no OneDrive ou no Microsoft Teams e como executar ações nesses arquivos.
ms.openlocfilehash: 6f44cd82241b4cd883fbd80e1b1dc2ea115e10af
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30219561"
---
# <a name="view-information-about-malicious-files-detected-in-sharepoint-onedrive-or-microsoft-teams"></a><span data-ttu-id="a80b8-103">Exibir informações sobre arquivos mal-intencionados detectados no SharePoint, no OneDrive ou no Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="a80b8-103">View information about malicious files detected in SharePoint, OneDrive, or Microsoft Teams</span></span>

<span data-ttu-id="a80b8-p101">O [Office 365 ATP para SharePoint, onedrive e Microsoft Teams](atp-for-spo-odb-and-teams.md) protege sua organização de arquivos mal-intencionados em bibliotecas de documentos e sites de equipe. Quando um arquivo mal-intencionado é detectado, esse arquivo é bloqueado para que ninguém possa abri-lo, copiá-lo ou compartilhá-lo até que outras ações sejam executadas pela equipe de segurança da organização. Leia este artigo para saber como exibir informações sobre arquivos detectados e quais ações executar.</span><span class="sxs-lookup"><span data-stu-id="a80b8-p101">[Office 365 ATP for SharePoint, OneDrive, and Microsoft Teams](atp-for-spo-odb-and-teams.md) protects your organization from malicious files in document libraries and team sites. When a malicious file is detected, that file is blocked so that no one can open, copy, move, or share it until further actions are taken by the organization's security team. Read this article to learn how to view information about detected files and what actions to take.</span></span> 

<span data-ttu-id="a80b8-107">Para executar as tarefas descritas neste artigo, você deve ter as [permissões necessárias para o centro de conformidade de segurança &amp; do Office 365](permissions-in-the-security-and-compliance-center.md).</span><span class="sxs-lookup"><span data-stu-id="a80b8-107">In order to perform the tasks described in this article, you must have the necessary [permissions for the Office 365 Security &amp; Compliance Center](permissions-in-the-security-and-compliance-center.md).</span></span> 
  
## <a name="view-reports-with-information-about-detected-files"></a><span data-ttu-id="a80b8-108">Exibir relatórios com informações sobre arquivos detectados</span><span class="sxs-lookup"><span data-stu-id="a80b8-108">View reports with information about detected files</span></span>

<span data-ttu-id="a80b8-109">Para exibir o status e informações detalhadas sobre arquivos detectados pelo Office 365 ATP, você pode usar o relatório de status de proteção contra ameaças.</span><span class="sxs-lookup"><span data-stu-id="a80b8-109">To view status and detailed information about files that were detected by Office 365 ATP, you can use the Threat Protection Status report.</span></span>
  
1. <span data-ttu-id="a80b8-110">no [centro de conformidade de &amp; segurança do Office 365](https://protection.office.com), escolha **painel** \> de **relatórios** \> **Status da proteção contra ameaças**.</span><span class="sxs-lookup"><span data-stu-id="a80b8-110">In the [Office 365 Security &amp; Compliance Center](https://protection.office.com), choose **Reports** \> **Dashboard** \> **Threat Protection Status**.</span></span>
    
2. <span data-ttu-id="a80b8-111">No canto superior direito do relatório, escolha **Exibir tabela de detalhes**.</span><span class="sxs-lookup"><span data-stu-id="a80b8-111">In the upper right corner of the report, choose **View details table**.</span></span>
    
3. <span data-ttu-id="a80b8-112">Exiba a lista de arquivos que foram detectados no relatório.</span><span class="sxs-lookup"><span data-stu-id="a80b8-112">View the list of files that were detected in the report.</span></span>
    
4. <span data-ttu-id="a80b8-113">Selecione um item na lista para exibir informações detalhadas, incluindo ações executadas, o nome do arquivo, o caminho do arquivo e muito mais.</span><span class="sxs-lookup"><span data-stu-id="a80b8-113">Select an item in the list to view detailed information, including actions taken, the file name, the file path, and more.</span></span>
    
5. <span data-ttu-id="a80b8-114">Escolha a guia **análise avançada** para exibir informações, como comportamento observado e detalhes da análise.</span><span class="sxs-lookup"><span data-stu-id="a80b8-114">Choose the **Advanced Analysis** tab to view information, such as observed behavior and analysis details.</span></span> 
  
## <a name="view-and-take-action-on-files-in-quarantine"></a><span data-ttu-id="a80b8-115">Exibir e executar ação em arquivos em quarentena</span><span class="sxs-lookup"><span data-stu-id="a80b8-115">View and take action on files in quarantine</span></span>

1. <span data-ttu-id="a80b8-116">no centro de conformidade de &amp; segurança do Office 365, escolha **quarentena**de **análise** \> de **gerenciamento** \> de ameaças.</span><span class="sxs-lookup"><span data-stu-id="a80b8-116">In the Office 365 Security &amp; Compliance Center, choose **Threat management** \> **Review** \> **Quarantine**.</span></span>
    
2. <span data-ttu-id="a80b8-117">No canto superior esquerdo, altere o filtro de **email** para **conteúdo**.</span><span class="sxs-lookup"><span data-stu-id="a80b8-117">In the upper left corner, change the filter from **Email** to **Content**.</span></span>
    
3. <span data-ttu-id="a80b8-118">Selecione um item na lista para exibir informações detalhadas, incluindo a URL do arquivo.</span><span class="sxs-lookup"><span data-stu-id="a80b8-118">Select an item in the list to view detailed information, including the file's URL.</span></span>
    
4. <span data-ttu-id="a80b8-119">Escolha uma ação disponível.</span><span class="sxs-lookup"><span data-stu-id="a80b8-119">Choose an available action.</span></span>
    
  - <span data-ttu-id="a80b8-120">Escolha **relatório &amp; de lançamento** para desbloquear o arquivo.</span><span class="sxs-lookup"><span data-stu-id="a80b8-120">Choose **Release &amp; report** to unblock the file.</span></span> 
    
    <span data-ttu-id="a80b8-121">Selecione **Enviar relatório para a Microsoft** para relatar o arquivo como um falso positivo para a Microsoft.</span><span class="sxs-lookup"><span data-stu-id="a80b8-121">Select **Send report to Microsoft** to report the file as a false positive to Microsoft.</span></span> 
    
  - <span data-ttu-id="a80b8-122">Escolha **baixar arquivo** para investigar o arquivo.</span><span class="sxs-lookup"><span data-stu-id="a80b8-122">Choose **Download file** to investigate the file further.</span></span> 
    
  - <span data-ttu-id="a80b8-p102">Escolha **excluir** para remover o arquivo da lista de itens em quarentena. Se você escolher essa opção, também deverá excluir o arquivo de sua respectiva biblioteca no SharePoint Online, no OneDrive for Business ou no Microsoft Teams. Essa opção não desbloqueia um arquivo de ser aberto ou compartilhado.</span><span class="sxs-lookup"><span data-stu-id="a80b8-p102">Choose **Delete** to remove the file from the list of quarantined items. If you choose this option, you must also delete the file from its respective library in SharePoint Online, OneDrive for Business, or Microsoft Teams. This option does not unblock a file from being opened or shared.</span></span> 
    
5. <span data-ttu-id="a80b8-126">Escolha **fechar** para fechar os detalhes de um item selecionado.</span><span class="sxs-lookup"><span data-stu-id="a80b8-126">Choose **Close** to close the details for a selected item.</span></span> 
  
  

