---
title: Detecção de vírus no SharePoint Online
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 4/17/2018
ms.audience: Admin
ms.topic: reference
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- SPO160
- MOE150
- MET150
ms.assetid: e3c6df61-8513-499d-ad8e-8a91770bff63
description: O Office 365 pode ajudar a proteger seu ambiente contra malware detectando vírus em arquivos que os usuários carregam no SharePoint Online. Arquivos de verificação de vírus depois que eles são carregados. Se um arquivo for encontrado para serem infectados, uma propriedade é definida para que os usuários não podem fazer download ou sincronizar o arquivo.
ms.openlocfilehash: 22e983d35283ff96e1469fdf913e25b8d1d1c485
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22524311"
---
# <a name="virus-detection-in-sharepoint-online"></a><span data-ttu-id="2c80b-105">Detecção de vírus no SharePoint Online</span><span class="sxs-lookup"><span data-stu-id="2c80b-105">Virus detection in SharePoint Online</span></span>

<span data-ttu-id="2c80b-p102">O Office 365 pode ajudar a proteger seu ambiente contra malware detectando vírus em arquivos que os usuários carregam no SharePoint Online. Arquivos de verificação de vírus depois que eles são carregados. Se um arquivo for encontrado para serem infectados, uma propriedade é definida para que os usuários não podem fazer download ou sincronizar o arquivo.</span><span class="sxs-lookup"><span data-stu-id="2c80b-p102">Office 365 can help protect your environment from malware by detecting viruses in files that users upload to SharePoint Online. Files are scanned for viruses after they are uploaded. If a file is found to be infected, a property is set so that users can't download or sync the file.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="2c80b-p103">Esses recursos antivírus no SharePoint Online são uma maneira de conter vírus. Eles não são serve como um ponto único de defesa contra malware para seu ambiente. Recomendamos que todos os clientes para avaliar e implementar a proteção antimalware em diversas camadas e aplicar as práticas recomendadas para proteger sua infraestrutura empresarial. Para obter mais informações sobre as estratégias e práticas recomendadas, consulte [práticas recomendadas de segurança para o Office 365](security-best-practices.md).</span><span class="sxs-lookup"><span data-stu-id="2c80b-p103">These antivirus capabilities in SharePoint Online are a way to contain viruses. They aren't intended as a single point of defense against malware for your environment. We encourage all customers to assess and implement antimalware protection at various layers and apply best practices for securing your enterprise infrastructure. For more information about strategies and best practices, see [Security best practices for Office 365](security-best-practices.md).</span></span> 
  
## <a name="what-happens-when-an-infected-file-is-uploaded-to-sharepoint-online"></a><span data-ttu-id="2c80b-113">O que acontece quando um arquivo infectado é carregado no SharePoint Online?</span><span class="sxs-lookup"><span data-stu-id="2c80b-113">What happens when an infected file is uploaded to SharePoint Online?</span></span>

<span data-ttu-id="2c80b-p104">O Office 365 usa um mecanismo de detecção de vírus comuns. O mecanismo executa de forma assíncrona dentro do SharePoint Online e examina arquivos após terem sido carregadas. Quando um arquivo é encontrado contém um vírus, ela será sinalizada para que ele não pode ser baixado novamente. Em abril de 2018, removemos o limite de 25 MB para arquivos examinados.</span><span class="sxs-lookup"><span data-stu-id="2c80b-p104">Office 365 uses a common virus detection engine. The engine runs asynchronously within SharePoint Online, and scans files after they're uploaded. When a file is found to contain a virus, it's flagged so that it can't be downloaded again. In April 2018, we removed the 25 MB limit for scanned files.</span></span>
  
<span data-ttu-id="2c80b-118">Aqui está o que acontece:</span><span class="sxs-lookup"><span data-stu-id="2c80b-118">Here's what happens:</span></span>
  
1. <span data-ttu-id="2c80b-119">Um usuário carrega um arquivo para o SharePoint Online.</span><span class="sxs-lookup"><span data-stu-id="2c80b-119">A user uploads a file to SharePoint Online.</span></span>
    
2. <span data-ttu-id="2c80b-120">O mecanismo de detecção de vírus varre o arquivo.</span><span class="sxs-lookup"><span data-stu-id="2c80b-120">The virus detection engine scans the file.</span></span>
    
3. <span data-ttu-id="2c80b-121">Se for encontrado um vírus, o mecanismo de vírus define uma propriedade no arquivo indicando que infectados.</span><span class="sxs-lookup"><span data-stu-id="2c80b-121">If a virus is found, the virus engine sets a property on the file indicating that it is infected.</span></span>
    
## <a name="what-happens-when-a-user-tries-to-download-an-infected-file-by-using-the-browser"></a><span data-ttu-id="2c80b-122">O que acontece quando um usuário tentar baixar um arquivo infectado usando o navegador?</span><span class="sxs-lookup"><span data-stu-id="2c80b-122">What happens when a user tries to download an infected file by using the browser?</span></span>

<span data-ttu-id="2c80b-123">Se um arquivo é infectado com vírus, os usuários não podem baixar o arquivo do SharePoint Online usando o navegador.</span><span class="sxs-lookup"><span data-stu-id="2c80b-123">If a file is infected with a virus, users can't download the file from SharePoint Online by using the browser.</span></span>
  
<span data-ttu-id="2c80b-124">Aqui está o que acontece:</span><span class="sxs-lookup"><span data-stu-id="2c80b-124">Here's what happens:</span></span>
  
1. <span data-ttu-id="2c80b-125">Um usuário abre um navegador da web e tenta baixar um arquivo infectado do SharePoint Online.</span><span class="sxs-lookup"><span data-stu-id="2c80b-125">A user opens a web browser and tries to download an infected file from SharePoint Online.</span></span>
    
2. <span data-ttu-id="2c80b-126">O usuário recebe um aviso de que um vírus foi detectado e tem a opção para baixar o arquivo e tente limpá-la usando seu próprio software de vírus.</span><span class="sxs-lookup"><span data-stu-id="2c80b-126">The user is given a warning that a virus has been detected, and is given the option to download the file and attempt to clean it using their own virus software.</span></span>
    
## <a name="what-happens-when-the-onedrive-sync-client-tries-to-sync-an-infected-file"></a><span data-ttu-id="2c80b-127">O que acontece quando o cliente de sincronização do OneDrive tenta sincronizar um arquivo infectado?</span><span class="sxs-lookup"><span data-stu-id="2c80b-127">What happens when the OneDrive sync client tries to sync an infected file?</span></span>

<span data-ttu-id="2c80b-p105">Se os usuários sincronizar arquivos com o novo cliente de sincronização do OneDrive (OneDrive.exe) ou o OneDrive anterior para o cliente de sincronização de negócios (Groove.exe), se um arquivo contém um vírus, o cliente de sincronização não baixá-lo. O cliente de sincronização exibirá uma notificação que o arquivo não pode ser sincronizado.</span><span class="sxs-lookup"><span data-stu-id="2c80b-p105">Whether users sync files with the new OneDrive sync client (OneDrive.exe) or the previous OneDrive for Business sync client (Groove.exe), if a file contains a virus, the sync client won't download it. The sync client will display a notification that the file can't be synced.</span></span>
  

