---
title: Inscrever seu dispositivo móvel no Office 365
ms.author: brendonb
author: brendonb
manager: laurawi
ms.date: 6/25/2018
ms.audience: Admin
ms.topic: get-started-article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
- MED150
- MBS150
ms.assetid: c8ac722d-dcaf-4135-8345-3e6327f5d3c5
description: Antes de poder usar serviços do Office 365 com o seu dispositivo, talvez seja necessário que você siga estas etapas para se inscrever em gerenciamento de dispositivos móveis para o Office 365 (MDM). Você fazer isso quando você adiciona seu trabalho ou escola a conta de email para seu dispositivo pela primeira vez.
ms.openlocfilehash: 63e4052d42007d97928f158a704beb9721758a44
ms.sourcegitcommit: c31424cafbf1953f2864d7e2ceb95b329a694edb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/29/2018
ms.locfileid: "23272296"
---
# <a name="enroll-your-mobile-device-in-office-365"></a><span data-ttu-id="04e32-104">Inscrever seu dispositivo móvel no Office 365</span><span class="sxs-lookup"><span data-stu-id="04e32-104">Enroll your mobile device in Office 365</span></span>

<span data-ttu-id="04e32-p102">Usando seu telefone, tablet e outros dispositivos móveis para o trabalho é uma ótima maneira permaneçam informados e trabalhar em projetos de negócios enquanto você estiver fora do escritório. Antes de poder usar serviços do Office 365 com o seu dispositivo, talvez seja necessário primeiro registrar-se-lo no gerenciamento de dispositivos móveis para o Office 365 (MDM) usando o Portal do Microsoft Intune empresa.</span><span class="sxs-lookup"><span data-stu-id="04e32-p102">Using your phone, tablet, and other mobile devices for work is a great way to stay informed and work on business projects while you're away from the office. Before you can use Office 365 services with your device, you may need to first enroll it in Mobile Device Management for Office 365 (MDM) using Microsoft Intune Company Portal.</span></span>
  
<span data-ttu-id="04e32-p103">Organizações escolhem MDM para que os funcionários possam usar seus dispositivos móveis para acessar com segurança o email de trabalho, calendários e documentos enquanto a empresa protege dados importantes e atende aos seus requisitos de conformidade. [Saiba mais sobre MDM no Office 365](https://go.microsoft.com/fwlink/?LinkId=615142).</span><span class="sxs-lookup"><span data-stu-id="04e32-p103">Organizations choose MDM so that employees can use their mobile devices to securely access work email, calendars, and documents while the business secures important data and meets their compliance requirements. [Learn about MDM in Office 365](https://go.microsoft.com/fwlink/?LinkId=615142).</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="04e32-p104">Quando você registrar seu dispositivo no MDM para o Office 365, você talvez precise configurar uma senha, junto com permitindo a opção para sua organização de trabalho para apagar o dispositivo. Uma limpeza de dispositivo pode ser executada (a partir do Centro de administração do Office 365), por exemplo, para remover todos os dados do dispositivo, se a senha for digitada incorretamente muitas vezes ou termos de uso serão desfeitos.</span><span class="sxs-lookup"><span data-stu-id="04e32-p104">When you enroll your device in MDM for Office 365, you might be required to set up a password, together with allowing the option for your work organization to wipe the device. A device wipe can be performed (from the Office 365 admin center), for example, to remove all data from the device if the password is entered incorrectly too many times or if usage terms are broken.</span></span> 
  
 <span data-ttu-id="04e32-111">**Dispositivos suportados**</span><span class="sxs-lookup"><span data-stu-id="04e32-111">**Supported devices**</span></span>
  
<span data-ttu-id="04e32-p105">MDM e InTune funciona com a maioria dos, mas nem todos os dispositivos móveis. A seguir é compatíveis com o MDM para o Office 365.</span><span class="sxs-lookup"><span data-stu-id="04e32-p105">MDM and InTune works with most, but not all, mobile devices. The following are supported with MDM for Office 365.</span></span>
  
- <span data-ttu-id="04e32-114">iOS 7.1 ou posterior</span><span class="sxs-lookup"><span data-stu-id="04e32-114">iOS 7.1 or later</span></span>
    
- <span data-ttu-id="04e32-115">Android 4 ou posterior</span><span class="sxs-lookup"><span data-stu-id="04e32-115">Android 4 or later</span></span>
    
- <span data-ttu-id="04e32-116">Windows 8.1 (telefone e PC) ou posterior para incluir Windows 10</span><span class="sxs-lookup"><span data-stu-id="04e32-116">Windows 8.1 (Phone and PC) and later to include Windows 10</span></span>
    
- <span data-ttu-id="04e32-117">Windows 10</span><span class="sxs-lookup"><span data-stu-id="04e32-117">Windows 10</span></span>
    
<span data-ttu-id="04e32-118">Se o dispositivo não estiver listado acima, e você precisa usá-lo com MDM e Intune, contate o administrador de trabalho ou da escola.</span><span class="sxs-lookup"><span data-stu-id="04e32-118">If your device is not listed above, and you need to use it with MDM and Intune, contact your work or school administrator.</span></span>
  
> [!TIP]
> <span data-ttu-id="04e32-119">Se você estiver tendo problemas inscrevendo seu dispositivo, consulte: [Troubleshoot o registro do dispositivo com o MDM para o Office 365](troubleshoot-mdm.md).</span><span class="sxs-lookup"><span data-stu-id="04e32-119">If you're having trouble enrolling your device, see: [Troubleshoot device enrollment with MDM for Office 365](troubleshoot-mdm.md).</span></span> 
  
## <a name="set-up-your-mobile-device-with-intune-and-mdm-for-office-365"></a><span data-ttu-id="04e32-120">Configurar o seu dispositivo móvel com Intune e MDM para Office 365</span><span class="sxs-lookup"><span data-stu-id="04e32-120">Set up your mobile device with Intune and MDM for Office 365</span></span>

<span data-ttu-id="04e32-121">O Portal da empresa Intune permite que um dispositivo a serem gerenciados pelo Office 365 e MDM.</span><span class="sxs-lookup"><span data-stu-id="04e32-121">The Intune Company Portal enables a device to be managed by Office 365 and MDM.</span></span>
  
### <a name="iphone-or-ipad"></a><span data-ttu-id="04e32-122">iPhone ou iPad</span><span class="sxs-lookup"><span data-stu-id="04e32-122">iPhone or iPad</span></span>

> [!TIP]
> <span data-ttu-id="04e32-123">Você não poderá enviar e receber emails, até que você conclua esta etapa.</span><span class="sxs-lookup"><span data-stu-id="04e32-123">You won't be able to send and receive email until you complete this step.</span></span> 
  
> <span data-ttu-id="04e32-124">Vá para o repositório de App Apple, baixe e instale o Intune Portal da empresa.</span><span class="sxs-lookup"><span data-stu-id="04e32-124">Go to the Apple App Store, download and install Intune Company Portal.</span></span>
    
> <span data-ttu-id="04e32-125">[Siga estas etapas para configurar e se conectar](https://go.microsoft.com/fwlink/?linkid=875316) seu telefone iOS ou tablet com o portal de empresa para o Office 365.</span><span class="sxs-lookup"><span data-stu-id="04e32-125">[Follow these steps to configure and connect](https://go.microsoft.com/fwlink/?linkid=875316) your iOS phone or tablet with the Company portal to Office 365.</span></span> 
    
### <a name="android-phone-or-tablet"></a><span data-ttu-id="04e32-126">Telefone Android ou tablet</span><span class="sxs-lookup"><span data-stu-id="04e32-126">Android phone or tablet</span></span>

> [!TIP]
> <span data-ttu-id="04e32-127">Você não poderá enviar e receber emails, até que você conclua esta etapa.</span><span class="sxs-lookup"><span data-stu-id="04e32-127">You won't be able to send and receive email until you complete this step.</span></span> 
  
> <span data-ttu-id="04e32-128">Vá para o repositório do Google Play, baixe e instale o Intune Portal da empresa.</span><span class="sxs-lookup"><span data-stu-id="04e32-128">Go to the Google Play store, download and install Intune Company Portal.</span></span>
    
> <span data-ttu-id="04e32-129">[Siga estas etapas para configurar e se conectar](https://go.microsoft.com/fwlink/?linkid=875317) seu telefone Android ou tablet com o portal de empresa para o Office 365.</span><span class="sxs-lookup"><span data-stu-id="04e32-129">[Follow these steps to configure and connect](https://go.microsoft.com/fwlink/?linkid=875317) your Android phone or tablet with the Company portal to Office 365.</span></span> 
    
## <a name="whats-next"></a><span data-ttu-id="04e32-130">Qual é a próxima</span><span class="sxs-lookup"><span data-stu-id="04e32-130">What's next</span></span>

<span data-ttu-id="04e32-131">Depois que o seu dispositivo está inscrito no MDM para o Office 365, você pode iniciar usando os aplicativos do Office no seu dispositivo para trabalhar com email, calendário, contatos e documentos.</span><span class="sxs-lookup"><span data-stu-id="04e32-131">After your device is enrolled in MDM for Office 365, you can start using Office apps on your device to work with email, calendar, contacts, and documents.</span></span>
  

