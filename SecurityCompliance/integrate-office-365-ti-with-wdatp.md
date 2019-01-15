---
title: Integrar a Inteligência Contra Ameaças do Office 365 com a Proteção Avançada contra Ameaças do Windows Defender
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 3/21/2018
ms.audience: ITPro
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 414fa693-d7b7-4a1d-a387-ebc3b6a52889
description: Integre a proteção de ameaça avançadas do Office 365 Windows Defender avançada proteção contra ameaças para ver as informações mais detalhadas de gerenciamento de ameaça.
ms.openlocfilehash: 48e879c1d41b5aa662f5128e234be91eb8225e7b
ms.sourcegitcommit: 9034809b6f308bedc3b8ddcca8242586b5c30f94
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/15/2019
ms.locfileid: "28014763"
---
# <a name="integrate-office-365-threat-intelligence-with-windows-defender-advanced-threat-protection"></a><span data-ttu-id="18dba-103">Integrar a Inteligência Contra Ameaças do Office 365 com a Proteção Avançada contra Ameaças do Windows Defender</span><span class="sxs-lookup"><span data-stu-id="18dba-103">Integrate Office 365 Threat Intelligence with Windows Defender Advanced Threat Protection</span></span>

<span data-ttu-id="18dba-p101">Se você fazem parte da equipe de segurança da sua organização, você poderá integrar o Office 365 com Windows Defender avançadas ameaça proteção (ATP). Isso pode ajudá-lo a entender rapidamente se máquinas dos usuários estão em risco quando estiver investigando ameaças no Office 365. Por exemplo, quando integração estiver habilitada, você poderá ver uma lista de computadores que são usadas pelos destinatários de uma mensagem de e-mail detectado, bem como a esses aparelhos de muitos alertas recentes têm no Windows Defender ATP.</span><span class="sxs-lookup"><span data-stu-id="18dba-p101">If you are part of your organization's security team, you can integrate Office 365 with Windows Defender Advanced Threat Protection (ATP). This can help you quickly understand if users' machines are at risk when you are investigating threats in Office 365. For example, once integration is enabled, you will be able to see a list of machines that are used by the recipients of a detected email message, as well as how many recent alerts those machines have in Windows Defender ATP.</span></span>
  
<span data-ttu-id="18dba-107">A imagem a seguir mostra a guia **dispositivos** que você verá quando tem integração do Windows Defender ATP habilitada:</span><span class="sxs-lookup"><span data-stu-id="18dba-107">The following image shows the **Devices** tab that you'll see when have Windows Defender ATP integration enabled:</span></span> 
  
![Quando o Windows Defender ATP estiver habilitado, você pode ver uma lista das máquinas com alertas.](media/fec928ea-8f0c-44d7-80b9-a2e0a8cd4e89.PNG)
  
<span data-ttu-id="18dba-p102">Neste exemplo, você pode ver que os destinatários da mensagem de email têm quatro máquinas e um terá um alerta no Windows Defender ATP. Clicando no link para uma máquina abre a página de máquina no Windows Defender ATP em uma nova guia.</span><span class="sxs-lookup"><span data-stu-id="18dba-p102">In this example, you can see that the recipients of the email message have four machines and one has an alert in Windows Defender ATP. Clicking the link to a machine opens the machine page in Windows Defender ATP in a new tab.</span></span>
  
## <a name="requirements"></a><span data-ttu-id="18dba-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="18dba-111">Requirements</span></span>

- <span data-ttu-id="18dba-112">Sua organização deve ter inteligência de ameaça do Office 365 e Windows Defender ATP.</span><span class="sxs-lookup"><span data-stu-id="18dba-112">Your organization must have Office 365 Threat Intelligence and Windows Defender ATP.</span></span>
    
- <span data-ttu-id="18dba-p103">Você deve ser um administrador global do Office 365 ou ter uma função de administrador de segurança atribuída no [segurança &amp; Centro de conformidade](https://protection.office.com). (Consulte [Permissions in a segurança do Office 365 &amp; Centro de conformidade](permissions-in-the-security-and-compliance-center.md))</span><span class="sxs-lookup"><span data-stu-id="18dba-p103">You must be an Office 365 global administrator or have a security administrator role assigned in the [Security &amp; Compliance Center](https://protection.office.com). (See [Permissions in the Office 365 Security &amp; Compliance Center](permissions-in-the-security-and-compliance-center.md))</span></span>
    
- <span data-ttu-id="18dba-115">Você deve ter acesso ao Office 365 Threat Intelligence e o portal do Windows Defender ATP.</span><span class="sxs-lookup"><span data-stu-id="18dba-115">You must have access to both Office 365 Threat Intelligence and the Windows Defender ATP portal.</span></span>
    
## <a name="to-integrate-office-365-threat-intelligence-with-windows-defender-atp"></a><span data-ttu-id="18dba-116">Para integrar o Office 365 Threat Intelligence com Windows Defender ATP</span><span class="sxs-lookup"><span data-stu-id="18dba-116">To integrate Office 365 Threat Intelligence with Windows Defender ATP</span></span>

<span data-ttu-id="18dba-117">Integrando o Office 365 Threat Intelligence com Windows Defender ATP é configurado no Office 365 e no portal do Windows Defender ATP.</span><span class="sxs-lookup"><span data-stu-id="18dba-117">Integrating Office 365 Threat Intelligence with Windows Defender ATP is set up both in Office 365 and in the Windows Defender ATP portal.</span></span>
  
1. <span data-ttu-id="18dba-118">Como um global do Office 365 ou um administrador de segurança, vá para [https://protection.office.com](https://protection.office.com) e entre com sua conta de trabalho ou da escola para o Office 365.</span><span class="sxs-lookup"><span data-stu-id="18dba-118">As an Office 365 global or a security administrator, go to [https://protection.office.com](https://protection.office.com) and sign in with your work or school account for Office 365.</span></span> 
    
2. <span data-ttu-id="18dba-119">Escolha **gerenciamento de ameaça** \> **explorer de ameaça**.</span><span class="sxs-lookup"><span data-stu-id="18dba-119">Choose **Threat management** \> **Threat explorer**.</span></span>
    
3. <span data-ttu-id="18dba-120">No menu **mais** , escolha **Configurações de WDATP**.</span><span class="sxs-lookup"><span data-stu-id="18dba-120">On the **More** menu, choose **WDATP Settings**.</span></span>
    
4. <span data-ttu-id="18dba-121">Selecione **conectar-se ao Windows ATP**.</span><span class="sxs-lookup"><span data-stu-id="18dba-121">Select **Connect to Windows ATP**.</span></span>
    
<span data-ttu-id="18dba-p104">Depois de alterar as configurações no Office 365, você deve habilitar a conexão do Windows Defender ATP. Para fazer isso, consulte [usar o portal de proteção de ameaça avançado do Windows Defender](https://go.microsoft.com/fwlink/?linkid=859690).</span><span class="sxs-lookup"><span data-stu-id="18dba-p104">After you have changed the settings in Office 365, you must enable the connection from Windows Defender ATP. To do that, see [Use the Windows Defender Advanced Threat Protection portal](https://go.microsoft.com/fwlink/?linkid=859690).</span></span>
  
## <a name="related-topics"></a><span data-ttu-id="18dba-124">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="18dba-124">Related topics</span></span>

[<span data-ttu-id="18dba-125">Inteligência Contra Ameaças do Office 365</span><span class="sxs-lookup"><span data-stu-id="18dba-125">Office 365 Threat Intelligence</span></span>](office-365-ti.md)
  
<span data-ttu-id="18dba-126">[Proteção Avançada contra Ameaças do Office 365](office-365-atp.md) </span><span class="sxs-lookup"><span data-stu-id="18dba-126">[Office 365 Advanced Threat Protection](office-365-atp.md)</span></span>
  

