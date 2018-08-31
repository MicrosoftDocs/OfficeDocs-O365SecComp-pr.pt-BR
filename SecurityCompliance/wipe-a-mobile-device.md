---
title: Apagar um dispositivo móvel no Office 365
ms.author: dianef
author: dianef77
manager: scotv
ms.date: 6/11/2018
ms.audience: Admin
ms.topic: get-started-article
f1_keywords:
- O365M_WipeDevice
- O365E_WipeDevice
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MOE150
- MED150
- MBS150
- MET150
ms.assetid: 9d727c7d-8b47-4499-bf24-d046b449214c
description: Você pode usar o gerenciamento de dispositivo móvel interna para o Office 365 para realizar uma limpeza seletiva para remover apenas informações organizacionais, ou uma limpeza completa para excluir todas as informações de um dispositivo móvel e restaurá-lo para suas configurações de fábrica.
ms.openlocfilehash: d3eb28575924ca3bb4a647ae9af2f96b55116a53
ms.sourcegitcommit: c31424cafbf1953f2864d7e2ceb95b329a694edb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/29/2018
ms.locfileid: "23272496"
---
# <a name="wipe-a-mobile-device-in-office-365"></a><span data-ttu-id="582c0-103">Apagar um dispositivo móvel no Office 365</span><span class="sxs-lookup"><span data-stu-id="582c0-103">Wipe a mobile device in Office 365</span></span>
  
<span data-ttu-id="582c0-104">Você pode usar o gerenciamento de dispositivo móvel interna para o Office 365 para realizar uma limpeza seletiva para remover apenas informações organizacionais, ou uma limpeza completa para excluir todas as informações de um dispositivo móvel e restaurá-lo para suas configurações de fábrica.</span><span class="sxs-lookup"><span data-stu-id="582c0-104">You can use built-in mobile device management for Office 365 to do a selective wipe to remove only organizational information, or a full wipe to delete all information from a mobile device and restore it to its factory settings.</span></span>
  
## <a name="what-to-know-before-you-begin"></a><span data-ttu-id="582c0-105">O que saber antes de começar</span><span class="sxs-lookup"><span data-stu-id="582c0-105">What to know before you begin</span></span>

- <span data-ttu-id="582c0-p101">Dispositivos móveis podem armazenar informações organizacionais confidenciais e fornecer acesso aos recursos do Office 365 da sua organização. Para ajudar a proteger as informações da sua organização, você pode fazer uma limpeza completa ou uma limpeza seletiva:</span><span class="sxs-lookup"><span data-stu-id="582c0-p101">Mobile devices can store sensitive organizational information and provide access to your organization's Office 365 resources. To help protect your organization's information, you can do a full wipe or a selective wipe:</span></span>
    
  - <span data-ttu-id="582c0-p102">**Apagamento completo**: exclui todos os dados no dispositivo móvel de um usuário, incluindo aplicativos instalados, fotos e informações pessoais. Quando a limpeza estiver concluída, o dispositivo é restaurado para suas configurações de fábrica.</span><span class="sxs-lookup"><span data-stu-id="582c0-p102">**Full wipe**: Deletes all data on a user's mobile device, including installed applications, photos, and personal information. When the wipe is complete, the device is restored to its factory settings.</span></span> 
    
  - <span data-ttu-id="582c0-110">**Apagar seletiva**: remove apenas dados da organização e aplicativos deixará instalado, fotos e informações pessoais no dispositivo móvel de um usuário.</span><span class="sxs-lookup"><span data-stu-id="582c0-110">**Selective wipe**: Removes only organization data and leaves installed applications, photos, and personal information on a user's mobile device.</span></span> 
    
- <span data-ttu-id="582c0-111">Quando um dispositivo é apagado (apagamento completo ou apagamento seletivo), o dispositivo é removido da lista de dispositivos gerenciados.</span><span class="sxs-lookup"><span data-stu-id="582c0-111">When a device is wiped (full wipe or selective wipe), the device is removed from the list of managed devices.</span></span>
    
- <span data-ttu-id="582c0-p103">Você pode configurar uma política de gerenciamento de dispositivo móvel que automaticamente apaga (apagamento completo) um dispositivo após o usuário tenta sem sucesso inserir a senha do dispositivo um número específico de vezes. Siga as etapas em [criar e implantar diretivas de segurança de dispositivo](create-device-security-policies.md).</span><span class="sxs-lookup"><span data-stu-id="582c0-p103">You can set up a mobile device management policy that automatically wipes (full wipe) a device after the user unsuccessfully tries to enter the device's password a specific number of times. Follow the steps in [Create and deploy device security policies](create-device-security-policies.md).</span></span>
    
- <span data-ttu-id="582c0-114">Se você deseja saber o que um usuário observarão quando você apagar seus dispositivos, consulte [qual é o impacto de usuário e o dispositivo?](wipe-a-mobile-device.md#BKMK_Impact).</span><span class="sxs-lookup"><span data-stu-id="582c0-114">If you want to know what a user will experience when you wipe their device, see [What's the user and device impact?](wipe-a-mobile-device.md#BKMK_Impact).</span></span>
    
## <a name="wipe-a-mobile-device"></a><span data-ttu-id="582c0-115">Apagar um dispositivo móvel</span><span class="sxs-lookup"><span data-stu-id="582c0-115">Wipe a mobile device</span></span>

1. <span data-ttu-id="582c0-116">Vá para o [ ![clique aqui para ir para o Centro de administração do Office 365.](media/e00ba917-c3fb-4173-b344-43eb5c7eeb15.png)](https://portal.office.com/adminportal/home).</span><span class="sxs-lookup"><span data-stu-id="582c0-116">Go to the [![Click here to go to the Office 365 admin center.](media/e00ba917-c3fb-4173-b344-43eb5c7eeb15.png)](https://portal.office.com/adminportal/home).</span></span>

2. <span data-ttu-id="582c0-117">Vá para [Ir para a segurança do Office 365 &amp; Centro de conformidade](https://support.office.com/article/7e696a40-b86b-4a20-afcc-559218b7b1b8) \> **prevenção de perda de dados** \> **gerenciamento de dispositivo**.</span><span class="sxs-lookup"><span data-stu-id="582c0-117">Go to [Go to the Office 365 Security &amp; Compliance Center](https://support.office.com/article/7e696a40-b86b-4a20-afcc-559218b7b1b8)\> **Data loss prevention** \> **Device management**.</span></span>
    
3. <span data-ttu-id="582c0-118">Selecione o dispositivo que você deseja limpar.</span><span class="sxs-lookup"><span data-stu-id="582c0-118">Select the device you want to wipe.</span></span>
    
4. <span data-ttu-id="582c0-119">Selecione o tipo de apagamento remoto que você deseja fazer.</span><span class="sxs-lookup"><span data-stu-id="582c0-119">Select the type of remote wipe you want to do.</span></span>
    
  - <span data-ttu-id="582c0-120">Para fazer uma limpeza seletiva e excluir apenas Office 365 informações da organização, no painel direito, selecione **Apagar seletiva**.</span><span class="sxs-lookup"><span data-stu-id="582c0-120">To do a selective wipe and delete only Office 365 organization information, in the right pane, select **Selective wipe**.</span></span>
    
  - <span data-ttu-id="582c0-121">Para fazer uma limpeza completa e restaurar o dispositivo para suas configurações de fábrica, no painel direito, selecione **apagamento completo**.</span><span class="sxs-lookup"><span data-stu-id="582c0-121">To do a full wipe and restore the device to its factory settings, in the right pane, select **Full wipe**.</span></span>
    
![Selecione um dispositivo e, em seguida, escolha o tipo de apagamento fazer.](media/ac940abe-0c4a-404e-a842-a1ad2af13ce3.png)
  
5. <span data-ttu-id="582c0-123">Selecione **Sim** para confirmar.</span><span class="sxs-lookup"><span data-stu-id="582c0-123">Select **Yes** to confirm.</span></span> 
    
<span data-ttu-id="582c0-124">Até que a limpeza estiver concluída, o **status do dispositivo** será exibido como **RetirePending** ou **RetireIssued**.</span><span class="sxs-lookup"><span data-stu-id="582c0-124">Until the wipe finishes, the **Device status** will show as **RetirePending** or **RetireIssued**.</span></span>
  
### <a name="how-do-i-know-it-worked"></a><span data-ttu-id="582c0-125">Como saber se que ele funcionou?</span><span class="sxs-lookup"><span data-stu-id="582c0-125">How do I know it worked?</span></span>

<span data-ttu-id="582c0-126">Não há mais, você verá o dispositivo móvel na lista de dispositivos gerenciados.</span><span class="sxs-lookup"><span data-stu-id="582c0-126">You'll no longer see the mobile device in the list of managed devices.</span></span>
  
## <a name="why-would-you-want-to-wipe-a-device"></a><span data-ttu-id="582c0-127">Por que você deseja limpar um dispositivo?</span><span class="sxs-lookup"><span data-stu-id="582c0-127">Why would you want to wipe a device?</span></span>

<span data-ttu-id="582c0-128">Há vários motivos para apagar dispositivos dispositivos:</span><span class="sxs-lookup"><span data-stu-id="582c0-128">There are several reasons for wiping devices:</span></span>
  
- <span data-ttu-id="582c0-p104">Dispositivos móveis, como smartphones e tablets estão se tornando mais completo sempre. Isso significa que é mais fácil para os usuários armazenar informações corporativas confidenciais (como ou comunicações confidenciais de identificação pessoal) e acessá-lo em trânsito. Se um desses dispositivos móveis é perdido ou roubado, apagar dispositivos o dispositivo imediatamente podem ajudar a impedir que as informações da sua organização terminando em mãos erradas.</span><span class="sxs-lookup"><span data-stu-id="582c0-p104">Mobile devices like smartphones and tablets are becoming more full-featured all the time. This means it's easier for your users to store sensitive corporate information (such as personal identification or confidential communications) and access it on the go. If one of these mobile devices is lost or stolen, wiping the device immediately can help prevent your organization's information from ending up in the wrong hands.</span></span>
    
- <span data-ttu-id="582c0-132">Quando um usuário sai da organização com um dispositivo pessoal que está inscrito no MDM para o Office 365, você pode ajudar a impedir que informações organizacionais indo com esse usuário fazendo uma limpeza seletiva.</span><span class="sxs-lookup"><span data-stu-id="582c0-132">When a user leaves the organization with a personal device that is enrolled in MDM for Office 365, you can help prevent organizational information from going with that user by doing a selective wipe.</span></span>
    
- <span data-ttu-id="582c0-p105">Se sua organização fornece dispositivos móveis aos usuários, você talvez seja necessário reatribuir os dispositivos do tempo. Fazer uma limpeza completa em um dispositivo antes de atribuí-la a um novo ajuda de usuário garante que qualquer informação confidencial do proprietário anterior é excluída.</span><span class="sxs-lookup"><span data-stu-id="582c0-p105">If your organization provides mobile devices to users, you might need to reassign devices from time to time. Doing a full wipe on a device before assigning it to a new user helps ensures that any sensitive information from the previous owner is deleted.</span></span>
    
## <a name="whats-the-user-and-device-impact"></a><span data-ttu-id="582c0-135">O que é o usuário e o impacto de dispositivo?</span><span class="sxs-lookup"><span data-stu-id="582c0-135">What's the user and device impact?</span></span>

<span data-ttu-id="582c0-p106">A limpeza é enviada imediatamente para o dispositivo móvel. O dispositivo também será marcado como não compatível com em AAD.</span><span class="sxs-lookup"><span data-stu-id="582c0-p106">The wipe is sent immediately to the mobile device. The device is also marked as not compliant in AAD.</span></span>
  
<span data-ttu-id="582c0-138">A tabela a seguir descreve o conteúdo que foi removido para cada tipo de dispositivo, quando um dispositivo é apagado seletivamente.</span><span class="sxs-lookup"><span data-stu-id="582c0-138">The following table describes what content is removed for each device type when a device is selectively wiped.</span></span>
  
|<span data-ttu-id="582c0-139">**Impacto de conteúdo**</span><span class="sxs-lookup"><span data-stu-id="582c0-139">**Content impact**</span></span>|<span data-ttu-id="582c0-140">**Windows Phone 8.1**</span><span class="sxs-lookup"><span data-stu-id="582c0-140">**Windows Phone 8.1**</span></span>|<span data-ttu-id="582c0-141">**iOS 7.1 ou posterior**</span><span class="sxs-lookup"><span data-stu-id="582c0-141">**iOS 7.1+**</span></span>|<span data-ttu-id="582c0-142">**Android 4 ou posterior**</span><span class="sxs-lookup"><span data-stu-id="582c0-142">**Android 4+**</span></span>|
|:-----|:-----|:-----|:-----|
|<span data-ttu-id="582c0-143">Aplicativo de Portal da empresa\* é desinstalado.</span><span class="sxs-lookup"><span data-stu-id="582c0-143">Company Portal app\* is uninstalled.</span></span>  <br/> |<span data-ttu-id="582c0-144">N/D</span><span class="sxs-lookup"><span data-stu-id="582c0-144">N/A</span></span>  <br/> |<span data-ttu-id="582c0-145">✔</span><span class="sxs-lookup"><span data-stu-id="582c0-145">✔</span></span>  <br/> |<span data-ttu-id="582c0-146">N/D</span><span class="sxs-lookup"><span data-stu-id="582c0-146">N/A</span></span>  <br/> |
|<span data-ttu-id="582c0-p107">Dados de aplicativo Office 365 hospedados por aplicativos onde o controle de acesso é suportado pelo MDM para Office 365 são removida (Outlook atualmente e OneDrive for Business). Os aplicativos não serão removidos.</span><span class="sxs-lookup"><span data-stu-id="582c0-p107">Office 365 app data hosted by apps where access control is supported by MDM for Office 365 is removed (currently Outlook and OneDrive for Business). The apps are not removed.</span></span>  <br/> <span data-ttu-id="582c0-149">Outlook para Android não remove emails em cache.</span><span class="sxs-lookup"><span data-stu-id="582c0-149">Outlook for Android does not remove cached emails.</span></span>  <br/> |<span data-ttu-id="582c0-150">✔</span><span class="sxs-lookup"><span data-stu-id="582c0-150">✔</span></span>  <br/> |<span data-ttu-id="582c0-151">✔</span><span class="sxs-lookup"><span data-stu-id="582c0-151">✔</span></span>  <br/> |<span data-ttu-id="582c0-152">✔</span><span class="sxs-lookup"><span data-stu-id="582c0-152">✔</span></span>  <br/> |
|<span data-ttu-id="582c0-153">Configurações de diretiva que foram aplicadas por MDM para o Office 365 para dispositivos não são impostas no dispositivo e os usuários podem alterar as configurações.</span><span class="sxs-lookup"><span data-stu-id="582c0-153">Policy settings that were applied by MDM for Office 365 to devices are no longer enforced on the device and users can change the settings.</span></span>  <br/> |<span data-ttu-id="582c0-154">✔</span><span class="sxs-lookup"><span data-stu-id="582c0-154">✔</span></span>  <br/> |<span data-ttu-id="582c0-155">✔</span><span class="sxs-lookup"><span data-stu-id="582c0-155">✔</span></span>  <br/> |<span data-ttu-id="582c0-156">✔</span><span class="sxs-lookup"><span data-stu-id="582c0-156">✔</span></span>  <br/> |
|<span data-ttu-id="582c0-157">Perfis de email criados pelo MDM para o Office 365 são removidos e email em cache no dispositivo será excluído.</span><span class="sxs-lookup"><span data-stu-id="582c0-157">Email profiles created by MDM for Office 365 are removed and cached email on the device is deleted.</span></span>  <br/> |<span data-ttu-id="582c0-158">N/D</span><span class="sxs-lookup"><span data-stu-id="582c0-158">N/A</span></span>  <br/> |<span data-ttu-id="582c0-159">✔</span><span class="sxs-lookup"><span data-stu-id="582c0-159">✔</span></span>  <br/> |<span data-ttu-id="582c0-160">N/D</span><span class="sxs-lookup"><span data-stu-id="582c0-160">N/A</span></span>  <br/> |
   
> [!NOTE]
> <span data-ttu-id="582c0-161">\*Aplicativo de Portal da empresa está disponível na App Store para iOS e o repositório de tocar para dispositivos com Android.</span><span class="sxs-lookup"><span data-stu-id="582c0-161">\* Company Portal app is available at the App Store for iOS and the Play Store for Android devices.</span></span> 
  
## <a name="related-content"></a><span data-ttu-id="582c0-162">Conteúdo relacionado</span><span class="sxs-lookup"><span data-stu-id="582c0-162">Related content</span></span>

[<span data-ttu-id="582c0-163">Gerenciar dispositivos móveis no Office 365</span><span class="sxs-lookup"><span data-stu-id="582c0-163">Manage mobile devices in Office 365</span></span>](set-up-mobile-device-management.md)
  

