---
title: Visão geral do gerenciamento de dispositivos móveis (MDM) para o Office 365
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 6/29/2018
ms.audience: Admin
ms.topic: overview
f1_keywords:
- O365M_MDMConfigDomains
- O365E_MDMConfigDomains
- ms.o365.cc.DevicePolicy
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: faa7d8e5-645d-4d59-839c-c8d4c1869e4a
description: Você pode gerenciar e proteger dispositivos móveis se estivessem conectados à sua organização do Office 365 usando o gerenciamento de dispositivos móveis para o Office 365. Dispositivos móveis, como smartphones e tablets que são usados para acessar o trabalho de email, calendário, contatos e documentos ter um papel importante no certificando-se de que os funcionários realizar seus trabalhos a qualquer momento, em qualquer lugar. Isso é muito importante que você ajudar a proteger informações da sua organização, quando as pessoas usam dispositivos. Você pode usar o MDM para o Office 365 para definir regras de acesso e políticas de segurança de dispositivo e apagar dispositivos móveis se eles estiver perdidos ou roubados.
ms.openlocfilehash: f06cef11b68ee0673f13c54738f07f4556495fdd
ms.sourcegitcommit: c31424cafbf1953f2864d7e2ceb95b329a694edb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/29/2018
ms.locfileid: "23272486"
---
# <a name="overview-of-mobile-device-management-mdm-for-office-365"></a><span data-ttu-id="ecb74-106">Visão geral do gerenciamento de dispositivos móveis (MDM) para o Office 365</span><span class="sxs-lookup"><span data-stu-id="ecb74-106">Overview of Mobile Device Management (MDM) for Office 365</span></span>

<span data-ttu-id="ecb74-p102">Você pode gerenciar e proteger dispositivos móveis se estivessem conectados à sua organização do Office 365 usando o gerenciamento de dispositivos móveis para o Office 365. Dispositivos móveis, como smartphones e tablets que são usados para acessar o trabalho de email, calendário, contatos e documentos ter um papel importante no certificando-se de que os funcionários realizar seus trabalhos a qualquer momento, em qualquer lugar. Isso é muito importante que você ajudar a proteger informações da sua organização, quando as pessoas usam dispositivos. Você pode usar o MDM para o Office 365 para definir regras de acesso e políticas de segurança de dispositivo e apagar dispositivos móveis se eles estiver perdidos ou roubados.</span><span class="sxs-lookup"><span data-stu-id="ecb74-p102">You can manage and secure mobile devices when they're connected to your Office 365 organization by using Mobile Device Management for Office 365. Mobile devices like smartphones and tablets that are used to access work email, calendar, contacts, and documents play a big part in making sure that employees get their work done anytime, from anywhere. So it's critical that you help protect your organization's information when people use devices. You can use MDM for Office 365 to set device security policies and access rules, and to wipe mobile devices if they're lost or stolen.</span></span>
  
![MDM no telefone Android](media/69b9a9f6-13ac-4e36-99ca-95e82e0375aa.png)
  
## <a name="what-types-of-devices-can-you-manage"></a><span data-ttu-id="ecb74-112">Que tipos de dispositivos você pode gerenciar?</span><span class="sxs-lookup"><span data-stu-id="ecb74-112">What types of devices can you manage?</span></span>

<span data-ttu-id="ecb74-p103">Você pode usar o MDM para o Office 365 para gerenciar muitos tipos de dispositivos móveis, como Android, Windows Phone, iPhone e iPad. Para gerenciar os dispositivos móveis usados pelas pessoas em sua organização, cada pessoa deve ter uma licença do Office 365 aplicável e seus dispositivos devem ser registrados em MDM para o Office 365.</span><span class="sxs-lookup"><span data-stu-id="ecb74-p103">You can use MDM for Office 365 to manage many types of mobile devices like Windows Phone, Android, iPhone, and iPad. To manage mobile devices used by people in your organization, each person must have an applicable Office 365 license and their device must be enrolled in MDM for Office 365.</span></span> 
  
<span data-ttu-id="ecb74-115">Para ver o que MDM para o Office 365 suporta para cada tipo de dispositivo, consulte [Os recursos de gerenciamento de dispositivos móveis para o Office 365](capabilities-of-mobile-device-management.md).</span><span class="sxs-lookup"><span data-stu-id="ecb74-115">To see what MDM for Office 365 supports for each type of device, see [Capabilities of Mobile Device Management for Office 365](capabilities-of-mobile-device-management.md).</span></span>
  
## <a name="setup-steps-for-mdm"></a><span data-ttu-id="ecb74-116">Etapas de configuração para MDM</span><span class="sxs-lookup"><span data-stu-id="ecb74-116">Setup steps for MDM</span></span>

<span data-ttu-id="ecb74-p104">Um administrador global do Office 365 deve concluir as seguintes etapas para ativar e configurar o MDM para Office 365. Siga as orientações no tópico na [configuração do MDM para o Office 365](set-up-mobile-device-management.md) para ver as etapas detalhadas. Aqui está um resumo rápido:</span><span class="sxs-lookup"><span data-stu-id="ecb74-p104">An Office 365 global admin must complete the following steps to activate and set up MDM for Office 365. Follow the guidance in the topic on [setting up MDM for Office 365](set-up-mobile-device-management.md) to see detailed steps. Here's a quick summary:</span></span> 
  
> <span data-ttu-id="ecb74-120">Etapa 1: Ative MDM para o Office 365, seguindo as etapas no [conjunto de backup Mobile Device Management (MDM) no Office 365](set-up-mobile-device-management.md).</span><span class="sxs-lookup"><span data-stu-id="ecb74-120">Step 1: Activate MDM for Office 365 by following steps in the [Set up Mobile Device Management (MDM) in Office 365](set-up-mobile-device-management.md).</span></span>
    
> <span data-ttu-id="ecb74-121">Etapa 2: Configure MDM para o Office 365, por exemplo, criar um certificado APNs para gerenciar dispositivos iOS e adicionar um registro de sistema de nome de domínio (DNS) para seu domínio dar suporte ao Windows phones.</span><span class="sxs-lookup"><span data-stu-id="ecb74-121">Step 2: Set up MDM for Office 365 by, for example, creating an APNs certificate to manage iOS devices and adding a Domain Name System (DNS) record for your domain to support Windows phones.</span></span>
    
> <span data-ttu-id="ecb74-p105">Etapa 3: Criar políticas de dispositivo e aplicá-las a grupos de usuários. Quando você fizer isso, os usuários receberá uma [mensagem de inscrição no dispositivo](enroll-your-mobile-device.md). E quando concluírem a inscrição, seus dispositivos serão restritos pelas políticas que você configurou para eles.</span><span class="sxs-lookup"><span data-stu-id="ecb74-p105">Step 3: Create device policies and apply them to groups of users. When you do this, your users will get an [enrollment message on their device](enroll-your-mobile-device.md). And when they've completed enrollment, their devices will be restricted by the policies you've set up for them.</span></span>
    
    ![Creating an MDN device policy under Device security policies](media/fbcdbecd-0016-42f1-81a9-9fbad610da90.png)
  
## <a name="device-management-tasks"></a><span data-ttu-id="ecb74-125">Tarefas de gerenciamento de dispositivo</span><span class="sxs-lookup"><span data-stu-id="ecb74-125">Device management tasks</span></span>

<span data-ttu-id="ecb74-p106">Depois que você acaba de criar MDM para o Office 365, configurar e os usuários tenham sido registrados seus dispositivos, você pode gerenciar os dispositivos, bloqueie o acesso ou apagar um dispositivo, se necessário. Saiba mais sobre [algumas tarefas comuns de gerenciamento de dispositivo](manage-devices-in-mdm.md), incluindo where concluir as tarefas.</span><span class="sxs-lookup"><span data-stu-id="ecb74-p106">After you've got MDM for Office 365 set up and your users have enrolled their devices, you can manage the devices, block access, or wipe a device, if needed. Learn more about [some common device management tasks](manage-devices-in-mdm.md), including where to complete the tasks.</span></span>
  
## <a name="other-ways-to-manage-devices-and-apps"></a><span data-ttu-id="ecb74-128">Outras maneiras de gerenciar os aplicativos e dispositivos</span><span class="sxs-lookup"><span data-stu-id="ecb74-128">Other ways to manage devices and apps</span></span>

<span data-ttu-id="ecb74-129">Se precisar de mais funcionalidade do que MDM para o Office 365 inclui, confira desta [comparação dos recursos MDM e Microsoft Intune](choose-between-mdm-and-intune.md) para ver se uma assinatura Intune seria atender às necessidades da sua organização.</span><span class="sxs-lookup"><span data-stu-id="ecb74-129">If you need more functionality than MDM for Office 365 includes, check out this [comparison of MDM and Microsoft Intune features](choose-between-mdm-and-intune.md) to see if an Intune subscription would meet your organization's needs.</span></span> 
  
<span data-ttu-id="ecb74-p107">Se você precisa apenas de gerenciamento de aplicativo móvel (MAM), talvez para pessoas Atualizando projetos de trabalho em seus próprios dispositivos, Intune fornece outra opção além inscrevendo e gerenciamento de dispositivos. Uma assinatura Intune permite que você defina as políticas MAM usando o portal do Azure, mesmo se os dispositivos de pessoas não estão inscritos no Intune. Consulte a [proteger os dados de aplicativo usando diretivas MAM](https://go.microsoft.com/fwlink/?LinkId=825439).</span><span class="sxs-lookup"><span data-stu-id="ecb74-p107">If you just need mobile app management (MAM), perhaps for people updating work projects on their own devices, Intune provides another option besides enrolling and managing devices. An Intune subscription allows you to set up MAM policies by using the Azure portal, even if people's devices aren't enrolled in Intune. See [Protect app data using MAM policies](https://go.microsoft.com/fwlink/?LinkId=825439).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="ecb74-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="ecb74-133">See also</span></span>

[<span data-ttu-id="ecb74-134">Obter detalhes sobre os dispositivos gerenciados por MDM</span><span class="sxs-lookup"><span data-stu-id="ecb74-134">Get details about devices managed by MDM</span></span>](get-details-about-mdm-managed-devices.md)

[<span data-ttu-id="ecb74-135">Configurar o MDM para Office 365</span><span class="sxs-lookup"><span data-stu-id="ecb74-135">Set up MDM for Office 365</span></span>](set-up-mobile-device-management.md)
  
[<span data-ttu-id="ecb74-136">Registrar a dispositivos móveis no MDM</span><span class="sxs-lookup"><span data-stu-id="ecb74-136">Enroll mobile devices in MDM</span></span>](enroll-your-mobile-device.md)
  
[<span data-ttu-id="ecb74-137">Gerenciar dispositivos inscritos no MDM</span><span class="sxs-lookup"><span data-stu-id="ecb74-137">Manage devices enrolled in MDM</span></span>](manage-devices-in-mdm.md)

