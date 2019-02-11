---
title: Integrar a Inteligência Contra Ameaças do Office 365 com a Proteção Avançada contra Ameaças do Windows Defender
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 01/22/2019
ms.audience: ITPro
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 414fa693-d7b7-4a1d-a387-ebc3b6a52889
description: Integre a proteção de ameaça avançadas do Office 365 Windows Defender avançada proteção contra ameaças para ver as informações mais detalhadas de gerenciamento de ameaça.
ms.openlocfilehash: e5070e003972ae5308415dcdcca85b069d1163ac
ms.sourcegitcommit: 7e2a0185cadea7f3a6afc5ddc445eac2e1ce22eb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/11/2019
ms.locfileid: "29382534"
---
# <a name="integrate-office-365-threat-intelligence-with-windows-defender-advanced-threat-protection"></a><span data-ttu-id="4468b-103">Integrar a Inteligência Contra Ameaças do Office 365 com a Proteção Avançada contra Ameaças do Windows Defender</span><span class="sxs-lookup"><span data-stu-id="4468b-103">Integrate Office 365 Threat Intelligence with Windows Defender Advanced Threat Protection</span></span>

<span data-ttu-id="4468b-p101">Se você fizer parte da equipe de segurança da sua organização, você poderá integrar os recursos de proteção de ameaça avançadas do Office 365 e inteligência de ameaça com a proteção de ameaça avançado do Windows Defender. Isso pode ajudá-lo a entender rapidamente se máquinas dos usuários estão em risco quando estiver investigando ameaças no Office 365. Por exemplo, quando integração estiver habilitada, você poderá ver uma lista das máquinas que são usadas pelos destinatários de uma mensagem de e-mail detectado, assim como a esses aparelhos de muitos alertas recentes têm na proteção de ameaça avançado do Windows Defender.</span><span class="sxs-lookup"><span data-stu-id="4468b-p101">If you are part of your organization's security team, you can integrate Office 365 Advanced Threat Protection and Threat Intelligence features with Windows Defender Advanced Threat Protection. This can help you quickly understand if users' machines are at risk when you are investigating threats in Office 365. For example, once integration is enabled, you will be able to see a list of machines that are used by the recipients of a detected email message, as well as how many recent alerts those machines have in Windows Defender Advanced Threat Protection.</span></span>
  
<span data-ttu-id="4468b-107">A imagem a seguir mostra a guia **dispositivos** que você verá quando tem integração de proteção de ameaça avançado do Windows Defender habilitada:</span><span class="sxs-lookup"><span data-stu-id="4468b-107">The following image shows the **Devices** tab that you'll see when have Windows Defender Advanced Threat Protection integration enabled:</span></span> 
  
![Quando o Windows Defender ATP estiver habilitado, você pode ver uma lista das máquinas com alertas.](media/fec928ea-8f0c-44d7-80b9-a2e0a8cd4e89.PNG)
  
<span data-ttu-id="4468b-p102">Neste exemplo, você pode ver que os destinatários da mensagem de email têm quatro dispositivos e um terá um alerta. Clicar no link para um dispositivo abre sua página no portal de proteção de ameaça avançado do Windows Defender.</span><span class="sxs-lookup"><span data-stu-id="4468b-p102">In this example, you can see that the recipients of the email message have four devices and one has an alert. Clicking the link for a device opens its page in the Windows Defender Advanced Threat Protection portal.</span></span>
  
## <a name="requirements"></a><span data-ttu-id="4468b-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4468b-111">Requirements</span></span>

- <span data-ttu-id="4468b-112">Sua organização deve ter inteligência de ameaça do Office 365 e Windows Defender ATP.</span><span class="sxs-lookup"><span data-stu-id="4468b-112">Your organization must have Office 365 Threat Intelligence and Windows Defender ATP.</span></span>
    
- <span data-ttu-id="4468b-p103">Você deve ser um Administrador Global do Office 365 ou ter uma função de administrador de segurança (como administrador de segurança) atribuída no [segurança &amp; Centro de conformidade](https://protection.office.com). (Consulte [Permissions in a segurança do Office 365 &amp; Centro de conformidade](permissions-in-the-security-and-compliance-center.md))</span><span class="sxs-lookup"><span data-stu-id="4468b-p103">You must be an Office 365 Global Administrator or have a security administrator role (such as Security Administrator) assigned in the [Security &amp; Compliance Center](https://protection.office.com). (See [Permissions in the Office 365 Security &amp; Compliance Center](permissions-in-the-security-and-compliance-center.md))</span></span>
    
- <span data-ttu-id="4468b-115">Você deve ter acesso ao Office 365 Threat Intelligence e o portal de proteção de ameaça avançado do Windows Defender.</span><span class="sxs-lookup"><span data-stu-id="4468b-115">You must have access to both Office 365 Threat Intelligence and the Windows Defender Advanced Threat Protection portal.</span></span>
    
## <a name="to-integrate-office-365-threat-intelligence-with-windows-defender-atp"></a><span data-ttu-id="4468b-116">Para integrar o Office 365 Threat Intelligence com Windows Defender ATP</span><span class="sxs-lookup"><span data-stu-id="4468b-116">To integrate Office 365 Threat Intelligence with Windows Defender ATP</span></span>

<span data-ttu-id="4468b-117">Integrando o Office 365 Threat Intelligence com a proteção de ameaça avançado do Windows Defender é definida por meio de ambas as & de segurança do Office 365 Centro de conformidade e o portal de proteção de ameaça avançado do Windows Defender.</span><span class="sxs-lookup"><span data-stu-id="4468b-117">Integrating Office 365 Threat Intelligence with Windows Defender Advanced Threat Protection is set up by using both the Office 365 Security & Compliance Center AND the Windows Defender Advanced Threat Protection portal.</span></span>
  
1. <span data-ttu-id="4468b-118">Como um administrador global do Office 365 ou um administrador de segurança, vá para [https://protection.office.com](https://protection.office.com) e entre com sua conta de trabalho ou da escola para o Office 365.</span><span class="sxs-lookup"><span data-stu-id="4468b-118">As an Office 365 global administrator or a security administrator, go to [https://protection.office.com](https://protection.office.com) and sign in with your work or school account for Office 365.</span></span> 
    
2. <span data-ttu-id="4468b-119">Escolha **gerenciamento de ameaça** \> **Explorer**.</span><span class="sxs-lookup"><span data-stu-id="4468b-119">Choose **Threat management** \> **Explorer**.</span></span><br><span data-ttu-id="4468b-120">![Explorer no menu gerenciamento de ameaça](media/ThreatMgmt-Explorer-nav.png)</span><span class="sxs-lookup"><span data-stu-id="4468b-120">![Explorer in Threat Management menu](media/ThreatMgmt-Explorer-nav.png)</span></span><br>
    
3. <span data-ttu-id="4468b-121">No canto superior direito da tela, escolha **Configurações de WDATP**.</span><span class="sxs-lookup"><span data-stu-id="4468b-121">In the upper right corner of the screen, choose **WDATP Settings**.</span></span>
    
4. <span data-ttu-id="4468b-122">Na caixa de diálogo conexão do Windows Defender ATP, ative conectar ao Windows ATP.</span><span class="sxs-lookup"><span data-stu-id="4468b-122">In the Windows Defender ATP connection dialog box, turn on Connect to Windows ATP.</span></span><br>![Conexão do Windows Defender ATP](media/Explorer-WDATPConnection-dialog.png)<br>
    
5. <span data-ttu-id="4468b-p104">Habilite a conexão na proteção de ameaça avançado do Windows Defender. Consulte o [uso do portal de proteção de ameaça avançado do Windows Defender](https://go.microsoft.com/fwlink/?linkid=859690).</span><span class="sxs-lookup"><span data-stu-id="4468b-p104">Enable the connection in Windows Defender Advanced Threat Protection. See [Use the Windows Defender Advanced Threat Protection portal](https://go.microsoft.com/fwlink/?linkid=859690).</span></span>

  
## <a name="related-topics"></a><span data-ttu-id="4468b-126">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="4468b-126">Related topics</span></span>

[<span data-ttu-id="4468b-127">Inteligência Contra Ameaças do Office 365</span><span class="sxs-lookup"><span data-stu-id="4468b-127">Office 365 Threat Intelligence</span></span>](office-365-ti.md)
  
<span data-ttu-id="4468b-128">[Proteção Avançada contra Ameaças do Office 365](office-365-atp.md) </span><span class="sxs-lookup"><span data-stu-id="4468b-128">[Office 365 Advanced Threat Protection](office-365-atp.md)</span></span>
  

