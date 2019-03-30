---
title: Integrar a proteção avançada contra ameaças do Office 365 com a proteção avançada contra ameaças do Windows Defender
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 01/22/2019
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 414fa693-d7b7-4a1d-a387-ebc3b6a52889
ms.collection:
- M365-security-compliance
description: Integre a proteção avançada contra ameaças do Office 365 com a proteção avançada contra ameaças do Windows Defender para ver informações mais detalhadas sobre o gerenciamento de ameaças.
ms.openlocfilehash: 832b9c6bc600366e1ed6b7c6e60442bec8b5002c
ms.sourcegitcommit: e7a776a04ef6ed5e287a33cfdc36aa2d72862b55
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/29/2019
ms.locfileid: "30998954"
---
# <a name="integrate-office-365-advanced-threat-protection-with-windows-defender-advanced-threat-protection"></a><span data-ttu-id="75b67-103">Integrar a proteção avançada contra ameaças do Office 365 com a proteção avançada contra ameaças do Windows Defender</span><span class="sxs-lookup"><span data-stu-id="75b67-103">Integrate Office 365 Advanced Threat Protection with Windows Defender Advanced Threat Protection</span></span>

<span data-ttu-id="75b67-104">Se você fizer parte da equipe de segurança da sua organização, poderá integrar a proteção avançada contra ameaças do Office 365 e os recursos de investigação e resposta relacionados à proteção avançada contra ameaças do Windows Defender.</span><span class="sxs-lookup"><span data-stu-id="75b67-104">If you are part of your organization's security team, you can integrate Office 365 Advanced Threat Protection and related investigation and response features with Windows Defender Advanced Threat Protection.</span></span> <span data-ttu-id="75b67-105">Isso pode ajudá-lo a entender rapidamente se as máquinas dos usuários estão em risco quando você está investigando ameaças no Office 365.</span><span class="sxs-lookup"><span data-stu-id="75b67-105">This can help you quickly understand if users' machines are at risk when you are investigating threats in Office 365.</span></span> <span data-ttu-id="75b67-106">Por exemplo, depois que a integração estiver habilitada, você poderá ver uma lista de máquinas que são usadas pelos destinatários de uma mensagem de email detectada, bem como os alertas recentes que essas máquinas têm na proteção avançada contra ameaças do Windows Defender.</span><span class="sxs-lookup"><span data-stu-id="75b67-106">For example, once integration is enabled, you will be able to see a list of machines that are used by the recipients of a detected email message, as well as how many recent alerts those machines have in Windows Defender Advanced Threat Protection.</span></span>
  
<span data-ttu-id="75b67-107">A imagem a seguir mostra a guia **dispositivos** que você verá quando tiver a integração de proteção avançada contra ameaças do Windows Defender habilitada:</span><span class="sxs-lookup"><span data-stu-id="75b67-107">The following image shows the **Devices** tab that you'll see when have Windows Defender Advanced Threat Protection integration enabled:</span></span> 
  
![Quando o Windows Defender ATP estiver habilitado, você poderá ver uma lista de computadores com alertas.](media/fec928ea-8f0c-44d7-80b9-a2e0a8cd4e89.PNG)
  
<span data-ttu-id="75b67-109">Neste exemplo, você pode ver que os destinatários da mensagem de email têm quatro dispositivos e um tem um alerta.</span><span class="sxs-lookup"><span data-stu-id="75b67-109">In this example, you can see that the recipients of the email message have four devices and one has an alert.</span></span> <span data-ttu-id="75b67-110">Clicar no link de um dispositivo abre sua página no portal de proteção avançada contra ameaças do Windows Defender.</span><span class="sxs-lookup"><span data-stu-id="75b67-110">Clicking the link for a device opens its page in the Windows Defender Advanced Threat Protection portal.</span></span>
  
## <a name="requirements"></a><span data-ttu-id="75b67-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="75b67-111">Requirements</span></span>

- <span data-ttu-id="75b67-112">Sua organização deve ter o plano de proteção avançada contra ameaças do Office 365 (ou o Office 365 E5) e o Windows Defender ATP.</span><span class="sxs-lookup"><span data-stu-id="75b67-112">Your organization must have Office 365 Advanced Threat Protection Plan 2 (or Office 365 E5) and Windows Defender ATP.</span></span>
    
- <span data-ttu-id="75b67-113">Você deve ser um administrador global do Office 365 ou ter uma função de administrador de segurança (como administrador de segurança) atribuída no [centro de conformidade de segurança &amp; ](https://protection.office.com).</span><span class="sxs-lookup"><span data-stu-id="75b67-113">You must be an Office 365 Global Administrator or have a security administrator role (such as Security Administrator) assigned in the [Security &amp; Compliance Center](https://protection.office.com).</span></span> <span data-ttu-id="75b67-114">(Consulte [permissões no centro de conformidade de &amp; segurança do Office 365](permissions-in-the-security-and-compliance-center.md))</span><span class="sxs-lookup"><span data-stu-id="75b67-114">(See [Permissions in the Office 365 Security &amp; Compliance Center](permissions-in-the-security-and-compliance-center.md))</span></span>
    
- <span data-ttu-id="75b67-115">Você deve ter acesso ao Office 365 Threat Explorer no centro de conformidade do & de segurança e do portal de proteção avançada contra ameaças do Windows Defender.</span><span class="sxs-lookup"><span data-stu-id="75b67-115">You must have access to both Office 365 Threat Explorer in the Security & Compliance Center and the Windows Defender Advanced Threat Protection portal.</span></span>
    
## <a name="to-integrate-office-365-advanced-threat-protection-with-windows-defender-atp"></a><span data-ttu-id="75b67-116">Para integrar a proteção avançada contra ameaças do Office 365 com o Windows Defender ATP</span><span class="sxs-lookup"><span data-stu-id="75b67-116">To integrate Office 365 Advanced Threat Protection with Windows Defender ATP</span></span>

<span data-ttu-id="75b67-117">Integrando o Office 365 proteção avançada contra ameaças à proteção avançada contra ameaças do Windows Defender é configurada usando o centro de conformidade do & de segurança e o portal de proteção avançada contra ameaças do Windows Defender.</span><span class="sxs-lookup"><span data-stu-id="75b67-117">Integrating Office 365 Advanced Threat Protection with Windows Defender Advanced Threat Protection is set up by using both the Security & Compliance Center AND the Windows Defender Advanced Threat Protection portal.</span></span>
  
1. <span data-ttu-id="75b67-118">Como um administrador global do Office 365 ou um administrador de segurança, [https://protection.office.com](https://protection.office.com) acesse e entre com sua conta corporativa ou de estudante para o Office 365.</span><span class="sxs-lookup"><span data-stu-id="75b67-118">As an Office 365 global administrator or a security administrator, go to [https://protection.office.com](https://protection.office.com) and sign in with your work or school account for Office 365.</span></span> 
    
2. <span data-ttu-id="75b67-119">Escolha \*\*\*\* \> **Gerenciador**de gerenciamento de ameaças.</span><span class="sxs-lookup"><span data-stu-id="75b67-119">Choose **Threat management** \> **Explorer**.</span></span><br><span data-ttu-id="75b67-120">![Gerenciador no menu de gerenciamento de ameaças](media/ThreatMgmt-Explorer-nav.png)</span><span class="sxs-lookup"><span data-stu-id="75b67-120">![Explorer in Threat Management menu](media/ThreatMgmt-Explorer-nav.png)</span></span><br>
    
3. <span data-ttu-id="75b67-121">No canto superior direito da tela, escolha configurações de **WDATP**.</span><span class="sxs-lookup"><span data-stu-id="75b67-121">In the upper right corner of the screen, choose **WDATP Settings**.</span></span>
    
4. <span data-ttu-id="75b67-122">Na caixa de diálogo conexão ATP do Windows Defender, ative conectar ao Windows ATP.</span><span class="sxs-lookup"><span data-stu-id="75b67-122">In the Windows Defender ATP connection dialog box, turn on Connect to Windows ATP.</span></span><br>![Conexão ATP do Windows Defender](media/Explorer-WDATPConnection-dialog.png)<br>
    
5. <span data-ttu-id="75b67-124">Habilitar a conexão na proteção avançada contra ameaças do Windows Defender.</span><span class="sxs-lookup"><span data-stu-id="75b67-124">Enable the connection in Windows Defender Advanced Threat Protection.</span></span> <span data-ttu-id="75b67-125">Consulte [usar o portal de proteção avançada contra ameaças do Windows Defender](https://go.microsoft.com/fwlink/?linkid=859690).</span><span class="sxs-lookup"><span data-stu-id="75b67-125">See [Use the Windows Defender Advanced Threat Protection portal](https://go.microsoft.com/fwlink/?linkid=859690).</span></span>

  
## <a name="related-topics"></a><span data-ttu-id="75b67-126">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="75b67-126">Related topics</span></span>

[<span data-ttu-id="75b67-127">Investigação e resposta contra ameaças do Office 365</span><span class="sxs-lookup"><span data-stu-id="75b67-127">Office 365 Threat Investigation and Response</span></span>](office-365-ti.md)
  
[<span data-ttu-id="75b67-128">Proteção Avançada contra Ameaças do Office 365</span><span class="sxs-lookup"><span data-stu-id="75b67-128">Office 365 Advanced Threat Protection</span></span>](office-365-atp.md)
  

