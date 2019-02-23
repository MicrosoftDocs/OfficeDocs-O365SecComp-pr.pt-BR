---
title: Detecção de vírus no SharePoint Online
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 01/14/2019
ms.audience: Admin
ms.topic: reference
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- SPO160
- MOE150
- MET150
ms.assetid: e3c6df61-8513-499d-ad8e-8a91770bff63
description: O Office 365 pode ajudar a proteger seu ambiente contra malware, detectando vírus em arquivos que os usuários carregam no SharePoint Online. Os arquivos são verificados em busca de vírus após serem carregados. Se um arquivo for infectado, uma propriedade será definida para que os usuários não possam baixar ou sincronizar o arquivo.
ms.openlocfilehash: d39a5be525e25de8206e8d4219d9c83bfa6eaae0
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30212961"
---
# <a name="virus-detection-in-sharepoint-online"></a><span data-ttu-id="3907a-105">Detecção de vírus no SharePoint Online</span><span class="sxs-lookup"><span data-stu-id="3907a-105">Virus detection in SharePoint Online</span></span>

<span data-ttu-id="3907a-p102">O Office 365 pode ajudar a proteger seu ambiente contra malware, detectando vírus em arquivos que os usuários carregam no SharePoint Online. Os arquivos são verificados em busca de vírus após serem carregados. Se um arquivo for infectado, uma propriedade será definida para que os usuários não possam baixar ou sincronizar o arquivo.</span><span class="sxs-lookup"><span data-stu-id="3907a-p102">Office 365 can help protect your environment from malware by detecting viruses in files that users upload to SharePoint Online. Files are scanned for viruses after they are uploaded. If a file is found to be infected, a property is set so that users can't download or sync the file.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="3907a-p103">Esses recursos de antivírus no SharePoint Online são uma maneira de conter vírus. Eles não se destinam a um único ponto de defesa contra malware para seu ambiente. Incentivamos todos os clientes a avaliar e implementar a proteção antimalware em várias camadas e aplicar as práticas recomendadas para proteger sua infraestrutura corporativa. Para obter mais informações sobre estratégias e práticas recomendadas, consulte [Security Best Practices for Office 365](security-best-practices.md).</span><span class="sxs-lookup"><span data-stu-id="3907a-p103">These antivirus capabilities in SharePoint Online are a way to contain viruses. They aren't intended as a single point of defense against malware for your environment. We encourage all customers to assess and implement antimalware protection at various layers and apply best practices for securing your enterprise infrastructure. For more information about strategies and best practices, see [Security best practices for Office 365](security-best-practices.md).</span></span> 
  
## <a name="what-happens-when-an-infected-file-is-uploaded-to-sharepoint-online"></a><span data-ttu-id="3907a-113">O que acontece quando um arquivo infectado é carregado no SharePoint Online?</span><span class="sxs-lookup"><span data-stu-id="3907a-113">What happens when an infected file is uploaded to SharePoint Online?</span></span>

<span data-ttu-id="3907a-p104">O Office 365 usa um mecanismo de detecção de vírus comum. O mecanismo é executado de forma assíncrona no SharePoint Online e verifica os arquivos após serem carregados. Quando um arquivo é encontrado para conter um vírus, ele é sinalizado para que ele não possa ser baixado novamente. Em abril de 2018, removemos o limite de 25 MB dos arquivos examinados.</span><span class="sxs-lookup"><span data-stu-id="3907a-p104">Office 365 uses a common virus detection engine. The engine runs asynchronously within SharePoint Online, and scans files after they're uploaded. When a file is found to contain a virus, it's flagged so that it can't be downloaded again. In April 2018, we removed the 25 MB limit for scanned files.</span></span>
  
<span data-ttu-id="3907a-118">Veja o que acontece:</span><span class="sxs-lookup"><span data-stu-id="3907a-118">Here's what happens:</span></span>
  
1. <span data-ttu-id="3907a-119">Um usuário carrega um arquivo para o SharePoint Online.</span><span class="sxs-lookup"><span data-stu-id="3907a-119">A user uploads a file to SharePoint Online.</span></span>
    
2. <span data-ttu-id="3907a-120">O mecanismo de detecção de vírus examina o arquivo.</span><span class="sxs-lookup"><span data-stu-id="3907a-120">The virus detection engine scans the file.</span></span>
    
3. <span data-ttu-id="3907a-121">Se for encontrado um vírus, o mecanismo de vírus definirá uma propriedade no arquivo indicando que ele está infectado.</span><span class="sxs-lookup"><span data-stu-id="3907a-121">If a virus is found, the virus engine sets a property on the file indicating that it is infected.</span></span>
    
## <a name="what-happens-when-a-user-tries-to-download-an-infected-file-by-using-the-browser"></a><span data-ttu-id="3907a-122">O que acontece quando um usuário tenta baixar um arquivo infectado usando o navegador?</span><span class="sxs-lookup"><span data-stu-id="3907a-122">What happens when a user tries to download an infected file by using the browser?</span></span>

<span data-ttu-id="3907a-123">Se um arquivo estiver infectado por um vírus, os usuários não poderão baixar o arquivo do SharePoint online usando o navegador.</span><span class="sxs-lookup"><span data-stu-id="3907a-123">If a file is infected with a virus, users can't download the file from SharePoint Online by using the browser.</span></span>
  
<span data-ttu-id="3907a-124">Veja o que acontece:</span><span class="sxs-lookup"><span data-stu-id="3907a-124">Here's what happens:</span></span>
  
1. <span data-ttu-id="3907a-125">Um usuário abre um navegador da Web e tenta baixar um arquivo infectado do SharePoint Online.</span><span class="sxs-lookup"><span data-stu-id="3907a-125">A user opens a web browser and tries to download an infected file from SharePoint Online.</span></span>
    
2. <span data-ttu-id="3907a-p105">O usuário recebe um aviso de que um vírus foi detectado. O usuário recebe a opção de baixar o arquivo e tentar limpá-lo usando seu próprio software de vírus.</span><span class="sxs-lookup"><span data-stu-id="3907a-p105">The user is given a warning that a virus has been detected. The user is given the option to download the file and attempt to clean it using their own virus software.</span></span>

> [!NOTE]
> <span data-ttu-id="3907a-p106">Você pode usar o cmdlet Set-SPOTenant com o parâmetro **DisallowInfectedFileDownload** para não permitir que os usuários baixem um arquivo detectado, mesmo na janela de aviso de antivírus. ConFira [DisallowInfectedFileDownload]https://docs.microsoft.com/powershell/module/sharepoint-online/Set-SPOTenant)(.</span><span class="sxs-lookup"><span data-stu-id="3907a-p106">You can use the Set-SPOTenant cmdlet with the **DisallowInfectedFileDownload** parameter to not allow users to download a detected file, even in the anti-virus warning window. See [DisallowInfectedFileDownload] (https://docs.microsoft.com/powershell/module/sharepoint-online/Set-SPOTenant).</span></span>
    
## <a name="what-happens-when-the-onedrive-sync-client-tries-to-sync-an-infected-file"></a><span data-ttu-id="3907a-130">O que acontece quando o cliente de sincronização do OneDrive tenta sincronizar um arquivo infectado?</span><span class="sxs-lookup"><span data-stu-id="3907a-130">What happens when the OneDrive sync client tries to sync an infected file?</span></span>

<span data-ttu-id="3907a-p107">Se os usuários sincronizam arquivos com o novo cliente de sincronização do OneDrive (OneDrive. exe) ou o cliente de sincronização anterior do OneDrive for Business (Groove. exe), se um arquivo contiver um vírus, o cliente de sincronização não o baixará. O cliente de sincronização exibirá uma notificação informando que o arquivo não pode ser sincronizado.</span><span class="sxs-lookup"><span data-stu-id="3907a-p107">Whether users sync files with the new OneDrive sync client (OneDrive.exe) or the previous OneDrive for Business sync client (Groove.exe), if a file contains a virus, the sync client won't download it. The sync client will display a notification that the file can't be synced.</span></span>
  

