---
title: Integrar a Inteligência Contra Ameaças do Office 365 com a Proteção Avançada contra Ameaças do Windows Defender
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
ms.openlocfilehash: 892d04152d6029c48a52d37c6235d45a8ba67b81
ms.sourcegitcommit: a80bd8626720fabdf592b84e4424cd3a83d08280
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30222810"
---
# <a name="integrate-office-365-threat-intelligence-with-windows-defender-advanced-threat-protection"></a><span data-ttu-id="4f39a-103">Integrar a Inteligência Contra Ameaças do Office 365 com a Proteção Avançada contra Ameaças do Windows Defender</span><span class="sxs-lookup"><span data-stu-id="4f39a-103">Integrate Office 365 Threat Intelligence with Windows Defender Advanced Threat Protection</span></span>

<span data-ttu-id="4f39a-p101">Se você fizer parte da equipe de segurança de sua organização, poderá integrar os recursos de proteção avançada contra ameaças e inteligência de ameaças do Office 365 com a proteção avançada contra ameaças do Windows Defender. Isso pode ajudá-lo a entender rapidamente se as máquinas dos usuários estão em risco quando você está investigando ameaças no Office 365. Por exemplo, depois que a integração estiver habilitada, você poderá ver uma lista de máquinas que são usadas pelos destinatários de uma mensagem de email detectada, bem como os alertas recentes que essas máquinas têm na proteção avançada contra ameaças do Windows Defender.</span><span class="sxs-lookup"><span data-stu-id="4f39a-p101">If you are part of your organization's security team, you can integrate Office 365 Advanced Threat Protection and Threat Intelligence features with Windows Defender Advanced Threat Protection. This can help you quickly understand if users' machines are at risk when you are investigating threats in Office 365. For example, once integration is enabled, you will be able to see a list of machines that are used by the recipients of a detected email message, as well as how many recent alerts those machines have in Windows Defender Advanced Threat Protection.</span></span>
  
<span data-ttu-id="4f39a-107">A imagem a seguir mostra a guia **dispositivos** que você verá quando tiver a integração de proteção avançada contra ameaças do Windows Defender habilitada:</span><span class="sxs-lookup"><span data-stu-id="4f39a-107">The following image shows the **Devices** tab that you'll see when have Windows Defender Advanced Threat Protection integration enabled:</span></span> 
  
![Quando o Windows Defender ATP estiver habilitado, você poderá ver uma lista de computadores com alertas.](media/fec928ea-8f0c-44d7-80b9-a2e0a8cd4e89.PNG)
  
<span data-ttu-id="4f39a-p102">Neste exemplo, você pode ver que os destinatários da mensagem de email têm quatro dispositivos e um tem um alerta. Clicar no link de um dispositivo abre sua página no portal de proteção avançada contra ameaças do Windows Defender.</span><span class="sxs-lookup"><span data-stu-id="4f39a-p102">In this example, you can see that the recipients of the email message have four devices and one has an alert. Clicking the link for a device opens its page in the Windows Defender Advanced Threat Protection portal.</span></span>
  
## <a name="requirements"></a><span data-ttu-id="4f39a-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4f39a-111">Requirements</span></span>

- <span data-ttu-id="4f39a-112">Sua organização deve ter o Office 365 Threat Intelligence e o Windows Defender ATP.</span><span class="sxs-lookup"><span data-stu-id="4f39a-112">Your organization must have Office 365 Threat Intelligence and Windows Defender ATP.</span></span>
    
- <span data-ttu-id="4f39a-p103">Você deve ser um administrador global do Office 365 ou ter uma função de administrador de segurança (como administrador de segurança) atribuída no [centro de conformidade de segurança &amp; ](https://protection.office.com). (Consulte [permissões no centro de conformidade de &amp; segurança do Office 365](permissions-in-the-security-and-compliance-center.md))</span><span class="sxs-lookup"><span data-stu-id="4f39a-p103">You must be an Office 365 Global Administrator or have a security administrator role (such as Security Administrator) assigned in the [Security &amp; Compliance Center](https://protection.office.com). (See [Permissions in the Office 365 Security &amp; Compliance Center](permissions-in-the-security-and-compliance-center.md))</span></span>
    
- <span data-ttu-id="4f39a-115">Você deve ter acesso ao Office 365 Threat Intelligence e ao portal de proteção avançada contra ameaças do Windows Defender.</span><span class="sxs-lookup"><span data-stu-id="4f39a-115">You must have access to both Office 365 Threat Intelligence and the Windows Defender Advanced Threat Protection portal.</span></span>
    
## <a name="to-integrate-office-365-threat-intelligence-with-windows-defender-atp"></a><span data-ttu-id="4f39a-116">Para integrar o Office 365 Threat Intelligence com o Windows Defender ATP</span><span class="sxs-lookup"><span data-stu-id="4f39a-116">To integrate Office 365 Threat Intelligence with Windows Defender ATP</span></span>

<span data-ttu-id="4f39a-117">Integração do Office 365 Threat Intelligence com a proteção avançada contra ameaças do Windows Defender é configurada usando o centro de conformidade do Office 365 Security & e o portal de proteção avançada contra ameaças do Windows Defender.</span><span class="sxs-lookup"><span data-stu-id="4f39a-117">Integrating Office 365 Threat Intelligence with Windows Defender Advanced Threat Protection is set up by using both the Office 365 Security & Compliance Center AND the Windows Defender Advanced Threat Protection portal.</span></span>
  
1. <span data-ttu-id="4f39a-118">Como um administrador global do Office 365 ou um administrador de segurança, [https://protection.office.com](https://protection.office.com) acesse e entre com sua conta corporativa ou de estudante para o Office 365.</span><span class="sxs-lookup"><span data-stu-id="4f39a-118">As an Office 365 global administrator or a security administrator, go to [https://protection.office.com](https://protection.office.com) and sign in with your work or school account for Office 365.</span></span> 
    
2. <span data-ttu-id="4f39a-119">Escolha \*\*\*\* \> **Gerenciador**de gerenciamento de ameaças.</span><span class="sxs-lookup"><span data-stu-id="4f39a-119">Choose **Threat management** \> **Explorer**.</span></span><br><span data-ttu-id="4f39a-120">![Gerenciador no menu de gerenciamento de ameaças](media/ThreatMgmt-Explorer-nav.png)</span><span class="sxs-lookup"><span data-stu-id="4f39a-120">![Explorer in Threat Management menu](media/ThreatMgmt-Explorer-nav.png)</span></span><br>
    
3. <span data-ttu-id="4f39a-121">No canto superior direito da tela, escolha configurações de **WDATP**.</span><span class="sxs-lookup"><span data-stu-id="4f39a-121">In the upper right corner of the screen, choose **WDATP Settings**.</span></span>
    
4. <span data-ttu-id="4f39a-122">Na caixa de diálogo conexão ATP do Windows Defender, ative conectar ao Windows ATP.</span><span class="sxs-lookup"><span data-stu-id="4f39a-122">In the Windows Defender ATP connection dialog box, turn on Connect to Windows ATP.</span></span><br>![Conexão ATP do Windows Defender](media/Explorer-WDATPConnection-dialog.png)<br>
    
5. <span data-ttu-id="4f39a-p104">Habilitar a conexão na proteção avançada contra ameaças do Windows Defender. Consulte [usar o portal de proteção avançada contra ameaças do Windows Defender](https://go.microsoft.com/fwlink/?linkid=859690).</span><span class="sxs-lookup"><span data-stu-id="4f39a-p104">Enable the connection in Windows Defender Advanced Threat Protection. See [Use the Windows Defender Advanced Threat Protection portal](https://go.microsoft.com/fwlink/?linkid=859690).</span></span>

  
## <a name="related-topics"></a><span data-ttu-id="4f39a-126">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="4f39a-126">Related topics</span></span>

[<span data-ttu-id="4f39a-127">Inteligência Contra Ameaças do Office 365</span><span class="sxs-lookup"><span data-stu-id="4f39a-127">Office 365 Threat Intelligence</span></span>](office-365-ti.md)
  
<span data-ttu-id="4f39a-128">[Proteção Avançada contra Ameaças do Office 365](office-365-atp.md) </span><span class="sxs-lookup"><span data-stu-id="4f39a-128">[Office 365 Advanced Threat Protection](office-365-atp.md)</span></span>
  

