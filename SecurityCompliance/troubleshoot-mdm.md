---
title: Solucionar problemas de inscrição de dispositivo com o MDM para Office 365
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 11/17/2015
ms.audience: Admin
ms.topic: get-started-article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MOE150
- MED150
- MBS150
- MET150
ms.assetid: c863b2bf-45f3-483a-ba05-29fc7f4d6434
description: Se você estiver executando nestes problemas ao tentar registrar um dispositivo Mobile Device Management (MDM) para o Office 365, siga as etapas listadas aqui para rastrear o problema. Se as etapas gerais não corrigir o problema, consulte uma das seções posteriores com as etapas específicas para o seu tipo de dispositivo.
ms.openlocfilehash: 490259fc623b38ab5ad6cf8553c5074c77b77426
ms.sourcegitcommit: c31424cafbf1953f2864d7e2ceb95b329a694edb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/29/2018
ms.locfileid: "23272106"
---
# <a name="troubleshoot-device-enrollment-with-mdm-for-office-365"></a><span data-ttu-id="3d2ac-104">Solucionar problemas de inscrição de dispositivo com o MDM para Office 365</span><span class="sxs-lookup"><span data-stu-id="3d2ac-104">Troubleshoot device enrollment with MDM for Office 365</span></span>

<span data-ttu-id="3d2ac-p102">Se você estiver executando nestes problemas ao tentar registrar um dispositivo Mobile Device Management (MDM) para o Office 365, siga as etapas listadas aqui para rastrear o problema. Se as etapas gerais não corrigir o problema, consulte uma das seções posteriores com as etapas específicas para o seu tipo de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="3d2ac-p102">If you're running into issues when you try to enroll a device in Mobile Device Management (MDM) for Office 365, try the steps listed here to track down the problem. If the general steps don't fix the issue, see one of the later sections with specific steps for your device type.</span></span>
  
## <a name="steps-to-try-first"></a><span data-ttu-id="3d2ac-107">Etapas para tentar primeiro</span><span class="sxs-lookup"><span data-stu-id="3d2ac-107">Steps to try first</span></span>

<span data-ttu-id="3d2ac-108">Para começar, verifique o seguinte:</span><span class="sxs-lookup"><span data-stu-id="3d2ac-108">To start, check the following:</span></span>
  
- <span data-ttu-id="3d2ac-109">Certifique-se de que o dispositivo não está inscrito já com outro provedor de gerenciamento de dispositivo móvel, como Intune.</span><span class="sxs-lookup"><span data-stu-id="3d2ac-109">Make sure that the device is not already enrolled with another mobile device management provider, such as Intune.</span></span>
    
- <span data-ttu-id="3d2ac-110">Certifique-se de que o dispositivo está definido como a data e hora correta.</span><span class="sxs-lookup"><span data-stu-id="3d2ac-110">Make sure that the device is set to the correct date and time.</span></span>
    
- <span data-ttu-id="3d2ac-111">Alternar para um Wi-Fi diferente ou a rede celular no dispositivo.</span><span class="sxs-lookup"><span data-stu-id="3d2ac-111">Switch to a different Wi-Fi or cellular network on the device.</span></span>
    
- <span data-ttu-id="3d2ac-112">Para dispositivos Android ou iOS, desinstale e reinstale o aplicativo de Portal da empresa Intune no dispositivo.</span><span class="sxs-lookup"><span data-stu-id="3d2ac-112">For Android or iOS devices, uninstall and reinstall the Intune Company Portal app on the device.</span></span>
    
## <a name="ios-phone-or-tablet"></a><span data-ttu-id="3d2ac-113">iOS celular ou tablet</span><span class="sxs-lookup"><span data-stu-id="3d2ac-113">iOS phone or tablet</span></span>

- <span data-ttu-id="3d2ac-114">Certifique-se de que você tiver que [Configurar um certificado APNs](https://support.office.com/article/522b43f4-a2ff-46f6-962a-dd4f47e546a7).</span><span class="sxs-lookup"><span data-stu-id="3d2ac-114">Make sure that you've [set up an APNs certificate](https://support.office.com/article/522b43f4-a2ff-46f6-962a-dd4f47e546a7).</span></span>
    
- <span data-ttu-id="3d2ac-p103">Nas **configurações** \> **Geral** \> **perfil** (ou **Device Management**), certifique-se de que um **Perfil de gerenciamento** já não está instalado. Se estiver, removê-lo.</span><span class="sxs-lookup"><span data-stu-id="3d2ac-p103">In **Settings** \> **General** \> **Profile** (or **Device Management**), make sure that a **Management Profile** is not already installed. If it is, remove it.</span></span> 
    
- <span data-ttu-id="3d2ac-117">Se você vir a mensagem de erro "Falha de dispositivo que se inscrevam," entrar no Office 365 e certifique-se de que uma licença que inclui o Exchange Online tiver sido atribuída ao usuário que está conectado ao dispositivo.</span><span class="sxs-lookup"><span data-stu-id="3d2ac-117">If you see the error message, "Device failed to enroll," sign in to Office 365 and make sure that a license that includes Exchange Online has been assigned to the user who is signed in to the device.</span></span>
    
- <span data-ttu-id="3d2ac-118">Se você vir a mensagem de erro "Falha de perfil instalar," Tente um destes procedimentos:</span><span class="sxs-lookup"><span data-stu-id="3d2ac-118">If you see the error message, "Profile failed to install," try one of the following:</span></span>
    
  - <span data-ttu-id="3d2ac-119">Certifique-se de que o Safari é o navegador padrão no dispositivo e que os cookies não estejam desabilitados.</span><span class="sxs-lookup"><span data-stu-id="3d2ac-119">Make sure that Safari is the default browser on the device, and that cookies are not disabled.</span></span>
    
  - <span data-ttu-id="3d2ac-120">Reinicializar o dispositivo, e em seguida, navegue até portal.manage.microsoft.com, entrar com sua ID de usuário do Office 365 e senha e tente instalar o perfil manualmente.</span><span class="sxs-lookup"><span data-stu-id="3d2ac-120">Reboot the device, then navigate to portal.manage.microsoft.com, sign in with your Office 365 user ID and password, and attempt to install the profile manually.</span></span>
    
## <a name="windows-rt-tablet"></a><span data-ttu-id="3d2ac-121">Tablet do Windows RT</span><span class="sxs-lookup"><span data-stu-id="3d2ac-121">Windows RT tablet</span></span>

- <span data-ttu-id="3d2ac-122">Certifique-se de que seu domínio é [configurado no Office 365 para funcionar com MDM](set-up-mobile-device-management.md).</span><span class="sxs-lookup"><span data-stu-id="3d2ac-122">Make sure that your domain is [set up in Office 365 to work with MDM](set-up-mobile-device-management.md).</span></span>
    
- <span data-ttu-id="3d2ac-123">Certifique-se de que o usuário está escolhendo **Turn On** em vez de escolhendo **ingressar**.</span><span class="sxs-lookup"><span data-stu-id="3d2ac-123">Make sure that the user is choosing **Turn On** rather than choosing **Join**.</span></span>
    
## <a name="windows-phone"></a><span data-ttu-id="3d2ac-124">Windows Phone</span><span class="sxs-lookup"><span data-stu-id="3d2ac-124">Windows Phone</span></span>

- <span data-ttu-id="3d2ac-125">Certifique-se de que seu domínio é [configurado no Office 365 para funcionar com MDM](set-up-mobile-device-management.md).</span><span class="sxs-lookup"><span data-stu-id="3d2ac-125">Make sure that your domain is [set up in Office 365 to work with MDM](set-up-mobile-device-management.md).</span></span>
    
- <span data-ttu-id="3d2ac-126">Verifique se que o dispositivo está executando o Windows 8.1 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="3d2ac-126">Make sure the device is running Windows 8.1 or later.</span></span>
    
## <a name="android-phone-or-tablet"></a><span data-ttu-id="3d2ac-127">Telefone Android ou tablet</span><span class="sxs-lookup"><span data-stu-id="3d2ac-127">Android phone or tablet</span></span>

- <span data-ttu-id="3d2ac-128">Verifique se que o dispositivo está executando o Android 4.0 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="3d2ac-128">Make sure the device is running Android 4.0 or later.</span></span>
    
- <span data-ttu-id="3d2ac-129">Se você vir a mensagem de erro, "Nós não pôde registrar este dispositivo," entrar no Office 365 e certifique-se de que uma licença que inclui o Exchange Online tiver sido atribuída ao usuário que está conectado ao dispositivo.</span><span class="sxs-lookup"><span data-stu-id="3d2ac-129">If you see the error message, "We couldn't enroll this device," sign in to Office 365 and make sure that a license that includes Exchange Online has been assigned to the user who is signed in to the device.</span></span>
    
- <span data-ttu-id="3d2ac-130">Verifique se a **Área de notificação** no dispositivo para ver se quaisquer ações do usuário final necessários estão pendentes e se eles forem, conclua as ações.</span><span class="sxs-lookup"><span data-stu-id="3d2ac-130">Check the **Notification Area** on the device to see if any required end-user actions are pending, and if they are, complete the actions.</span></span> 
    

