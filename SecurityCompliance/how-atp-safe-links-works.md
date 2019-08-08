---
title: Como funcionam os links seguros de ATP do Office 365
ms.author: tracyp
author: msfttracyp
manager: dansimp
audience: Admin
ms.date: 05/19/2019
ms.topic: overview
ms.service: O365-seccomp
localization_priority: Normal
ms.collection:
- Strat_O365_IP
- M365-security-compliance
description: O recurso de links seguros oferece verificação de horário de clique de hiperlinks em documentos do Office e em mensagens de email. Leia este artigo para saber como os links seguros de ATP funcionam.
ms.openlocfilehash: 45053b51bb5a91698d90f61567aa7f5577518587
ms.sourcegitcommit: 7a0cb7e1da39fc485fc29e7325b843d16b9808af
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/07/2019
ms.locfileid: "36230485"
---
# <a name="how-office-365-atp-safe-links-works"></a><span data-ttu-id="23184-104">Como funcionam os links seguros de ATP do Office 365</span><span class="sxs-lookup"><span data-stu-id="23184-104">How Office 365 ATP Safe Links works</span></span>
         
## <a name="how-atp-safe-links-works-with-urls-in-email"></a><span data-ttu-id="23184-105">Como os links seguros de ATP funcionam com URLs em email</span><span class="sxs-lookup"><span data-stu-id="23184-105">How ATP Safe Links works with URLs in email</span></span>

<span data-ttu-id="23184-106">Em um nível alto, veja como a proteção de [links de segurança ATP](atp-safe-links.md) funciona para URLs em email (hospedado no Office 365, não no local):</span><span class="sxs-lookup"><span data-stu-id="23184-106">At a high level, here's how [ATP Safe Links](atp-safe-links.md) protection works for URLs in email (hosted in Office 365, not on-premises):</span></span>
  
1. <span data-ttu-id="23184-107">As pessoas recebem mensagens de email, algumas das quais contêm URLs.</span><span class="sxs-lookup"><span data-stu-id="23184-107">People receive email messages, some of which contain URLs.</span></span>
    
2. <span data-ttu-id="23184-108">Todos os emails passam pela proteção do Exchange Online, onde os filtros IP e de envelope, proteção contra malware baseado em assinatura, filtros antispam e antimalware são aplicados.</span><span class="sxs-lookup"><span data-stu-id="23184-108">All email goes through Exchange Online Protection, where internet protocol (IP) and envelope filters, signature-based malware protection, anti-spam and anti-malware filters are applied.</span></span> 
    
3. <span data-ttu-id="23184-109">O email chega nas caixas de entrada de pessoas.</span><span class="sxs-lookup"><span data-stu-id="23184-109">Email arrives in people's inboxes.</span></span>
    
4. <span data-ttu-id="23184-110">Um usuário entra no Office 365 e vai para a caixa de entrada de email.</span><span class="sxs-lookup"><span data-stu-id="23184-110">A user signs in to Office 365, and goes to their email inbox.</span></span>
    
5. <span data-ttu-id="23184-111">O usuário abre uma mensagem de email e clica em uma URL na mensagem de email.</span><span class="sxs-lookup"><span data-stu-id="23184-111">The user opens an email message, and clicks on a URL in the email message.</span></span>
    
6. <span data-ttu-id="23184-112">O recurso de links seguros de ATP verifica imediatamente a URL antes de abrir o site.</span><span class="sxs-lookup"><span data-stu-id="23184-112">The ATP Safe Links feature immediately checks the URL before opening the website.</span></span> <span data-ttu-id="23184-113">A URL é identificada como bloqueada, mal-intencionada ou segura.</span><span class="sxs-lookup"><span data-stu-id="23184-113">The URL is identified as blocked, malicious, or safe.</span></span>
    
    - <span data-ttu-id="23184-114">Se a URL for um site que está incluído em uma [lista de URLs "não reconfigurar" personalizada](set-up-a-custom-do-not-rewrite-urls-list-with-atp.md) para uma política que se aplica ao usuário, o site será aberto.</span><span class="sxs-lookup"><span data-stu-id="23184-114">If the URL is to a website that is included in a [custom "Do not rewrite" URLs list](set-up-a-custom-do-not-rewrite-urls-list-with-atp.md) for a policy that applies to the user, the website opens.</span></span> 
    
    - <span data-ttu-id="23184-115">Se a URL for um site incluído na [lista de URLs bloqueadas](set-up-a-custom-blocked-urls-list-wtih-atp.md)da organização, uma [página de aviso](atp-safe-links-warning-pages.md) será aberta.</span><span class="sxs-lookup"><span data-stu-id="23184-115">If the URL is to a website that is included in the organization's [custom blocked URLs list](set-up-a-custom-blocked-urls-list-wtih-atp.md), a [warning page](atp-safe-links-warning-pages.md) opens.</span></span> 
    
    - <span data-ttu-id="23184-116">Se a URL for um site que foi determinado como mal-intencionado, uma [página de aviso](atp-safe-links-warning-pages.md) será aberta.</span><span class="sxs-lookup"><span data-stu-id="23184-116">If the URL is to a website that has been determined to be malicious, a [warning page](atp-safe-links-warning-pages.md) opens.</span></span> 
    
    - <span data-ttu-id="23184-117">Se a URL for para um arquivo baixável e as políticas de [links seguros ATP](set-up-atp-safe-links-policies.md) da sua organização estiverem configuradas para examinar esse conteúdo, o arquivo baixável será verificado.</span><span class="sxs-lookup"><span data-stu-id="23184-117">If the URL goes to a downloadable file and your organization's [ATP Safe Links policies](set-up-atp-safe-links-policies.md) are configured to scan such content, the downloadable file is checked.</span></span> 
    
    - <span data-ttu-id="23184-118">Se a URL for considerada segura, o site abrirá.</span><span class="sxs-lookup"><span data-stu-id="23184-118">If the URL is determined to be safe, the website opens.</span></span>
    
## <a name="how-atp-safe-links-works-with-urls-in-office-documents"></a><span data-ttu-id="23184-119">Como links seguros de ATP funciona com URLs em documentos do Office</span><span class="sxs-lookup"><span data-stu-id="23184-119">How ATP Safe Links works with URLs in Office documents</span></span>

<span data-ttu-id="23184-120">Em um nível alto, veja como a proteção de [links seguros ATP](atp-safe-links.md) funciona para URLs nos aplicativos do Office 365 ProPlus (versões atuais do Word, Excel e PowerPoint no Windows ou Mac, aplicativos do Office em dispositivos IOS ou Android, Visio no Windows, OneNote em um navegador e Office em um navegador):</span><span class="sxs-lookup"><span data-stu-id="23184-120">At a high level, here's how [ATP Safe Links](atp-safe-links.md) protection works for URLs in Office 365 ProPlus applications (current versions of Word, Excel, and PowerPoint on Windows or Mac, Office apps on iOS or Android devices, Visio on Windows, OneNote in a browser, and Office in a browser):</span></span>
  
1. <span data-ttu-id="23184-121">As pessoas instalaram o Office 365 ProPlus em seus computadores, smartphone ou Tablet.</span><span class="sxs-lookup"><span data-stu-id="23184-121">People have installed Office 365 ProPlus on their computer, smartphone, or tablet.</span></span> <span data-ttu-id="23184-122">(Ou, eles estão usando o Office em seu navegador.)</span><span class="sxs-lookup"><span data-stu-id="23184-122">(Or, they are using Office in their browser.)</span></span>
    
2. <span data-ttu-id="23184-123">Um usuário abre um Word, Excel, PowerPoint ou Visio e entra no Office 365 Enterprise usando sua conta corporativa ou de estudante.</span><span class="sxs-lookup"><span data-stu-id="23184-123">A user opens a Word, Excel, PowerPoint, or Visio, and signs in to Office 365 Enterprise using their work or school account.</span></span> <span data-ttu-id="23184-124">O documento contém URLs.</span><span class="sxs-lookup"><span data-stu-id="23184-124">The document contains URLs.</span></span>
    
3. <span data-ttu-id="23184-125">Quando o usuário clica em uma URL no documento, o link é verificado pelo serviço de links seguros de ATP.</span><span class="sxs-lookup"><span data-stu-id="23184-125">When the user clicks on a URL in the document, the link is checked by the ATP Safe Links service.</span></span>
    
      - <span data-ttu-id="23184-126">Se a URL for um site que está incluído em uma [lista de URLs "não reconfigurar" personalizada](set-up-a-custom-do-not-rewrite-urls-list-with-atp.md) para uma política que se aplica ao usuário, esse usuário será levado ao site.</span><span class="sxs-lookup"><span data-stu-id="23184-126">If the URL is to a website that is included in a [custom "Do not rewrite" URLs list](set-up-a-custom-do-not-rewrite-urls-list-with-atp.md) for a policy that applies to the user, that user is taken to the website.</span></span> 
    
      - <span data-ttu-id="23184-127">Se a URL for um site que está incluído na [lista de URLs bloqueados personalizada](set-up-a-custom-blocked-urls-list-wtih-atp.md)da organização, o usuário será levado para uma [página de aviso](atp-safe-links-warning-pages.md).</span><span class="sxs-lookup"><span data-stu-id="23184-127">If the URL is to a website that is included in the organization's [custom blocked URLs list](set-up-a-custom-blocked-urls-list-wtih-atp.md), the user is taken to a [warning page](atp-safe-links-warning-pages.md).</span></span>
    
      - <span data-ttu-id="23184-128">Se a URL for um site que foi determinado como mal-intencionado, o usuário será levado para uma [página de aviso](atp-safe-links-warning-pages.md).</span><span class="sxs-lookup"><span data-stu-id="23184-128">If the URL is to a website that has been determined to be malicious, the user is taken to a [warning page](atp-safe-links-warning-pages.md).</span></span>
    
      - <span data-ttu-id="23184-129">Se a URL for para um arquivo baixável e as [políticas de links seguros de ATP](set-up-atp-safe-links-policies.md) estiverem configuradas para examinar esses downloads, o arquivo baixável será verificado.</span><span class="sxs-lookup"><span data-stu-id="23184-129">If the URL goes to a downloadable file and the [ATP Safe Links policies](set-up-atp-safe-links-policies.md) are configured to scan such downloads, the downloadable file is checked.</span></span> 
    
      - <span data-ttu-id="23184-130">Se a URL for considerada segura, o usuário será levado para o site.</span><span class="sxs-lookup"><span data-stu-id="23184-130">If the URL is considered safe, the user is taken to the website.</span></span>

