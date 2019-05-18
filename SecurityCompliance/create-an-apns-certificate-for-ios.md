---
title: Criar um certificado APNs para dispositivos iOS
ms.author: brendonb
author: brendonb
manager: laurawi
ms.date: 8/5/2016
audience: Admin
ms.topic: article
f1_keywords:
- O365M_APNCertMDM
- O365E_APNCertMDM
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MOE150
- MED150
- MBS150
- MET150
ms.assetid: 522b43f4-a2ff-46f6-962a-dd4f47e546a7
description: Para gerenciar dispositivos iOS como iPad e iPhones no gerenciamento de dispositivos móveis para o Office 365, siga estas etapas para criar primeiro um certificado APNs.
ms.openlocfilehash: 17dae3e02520cdac2b1381039844d1657b12c4eb
ms.sourcegitcommit: 9d67cb52544321a430343d39eb336112c1a11d35
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/17/2019
ms.locfileid: "34153753"
---
# <a name="create-an-apns-certificate-for-ios-devices"></a><span data-ttu-id="74392-103">Criar um certificado APNs para dispositivos iOS</span><span class="sxs-lookup"><span data-stu-id="74392-103">Create an APNs Certificate for iOS devices</span></span>

 <span data-ttu-id="74392-104">Para gerenciar dispositivos iOS como iPad e iPhones no gerenciamento de dispositivos móveis para o Office 365, você deve criar um certificado APNs.</span><span class="sxs-lookup"><span data-stu-id="74392-104">To manage iOS devices like iPad and iPhones in Mobile Device Management for Office 365 you must create an APNs certificate.</span></span> 
  
<span data-ttu-id="74392-105">Para fazer isso, siga as etapas do link **Configurar** na página do Portal.</span><span class="sxs-lookup"><span data-stu-id="74392-105">To do this, follow the steps from the **Set up** link on the portal page.</span></span> <span data-ttu-id="74392-106">( \> Acesse gerenciamento de **dispositivos** de **políticas** \> de segurança do \> **centro de conformidade de &amp; segurança** **gerenciar configurações**.)</span><span class="sxs-lookup"><span data-stu-id="74392-106">(Go to **Security &amp; Compliance Center** \> **Security policies** \> **Device management** \> **Manage settings**.)</span></span>
  
![Configurar o gerenciamento de dispositivo móvel necessário e as etapas recomendadas](media/d71e3c76-b6b9-4549-ade6-cbfab846d908.png)
  
1. <span data-ttu-id="74392-108">Next to **Configure a APNs Certificate for iOS devices**, select **Set up**.</span><span class="sxs-lookup"><span data-stu-id="74392-108">Next to **Configure a APNs Certificate for iOS devices**, select **Set up**.</span></span>
    
2. <span data-ttu-id="74392-109">Select **Download your CSR file** and save the Certificate signing request to a somewhere on your computer that you'll remember.</span><span class="sxs-lookup"><span data-stu-id="74392-109">Select **Download your CSR file** and save the Certificate signing request to a somewhere on your computer that you'll remember.</span></span> 
    
    ![Caixa de diálogo Instalar certificado APN](media/03aa8a24-e95c-4077-9b6b-ef76a86bafd7.png)
  
3. <span data-ttu-id="74392-111"> Select *\*Next*\*. </span><span class="sxs-lookup"><span data-stu-id="74392-111">Select **Next**.</span></span>
    
4. <span data-ttu-id="74392-112"> Create an APN certificate.</span><span class="sxs-lookup"><span data-stu-id="74392-112">Create an APN certificate.</span></span>
    
  - <span data-ttu-id="74392-113">Select **Apple APNS Portal** to open the Apple Push Certificates Portal. </span><span class="sxs-lookup"><span data-stu-id="74392-113">Select **Apple APNS Portal** to open the Apple Push Certificates Portal.</span></span> 
    
    ![Instalar a caixa de diálogo de certificado de notificação APN com o portal Apple APNS selecionado](media/ce19f53c-f44a-470b-baf3-9278dfda2ba5.png)
  
  - <span data-ttu-id="74392-115">Sign in with an Apple ID.</span><span class="sxs-lookup"><span data-stu-id="74392-115">Sign in with an Apple ID.</span></span>
    
    > [!IMPORTANT]
    > <span data-ttu-id="74392-p102">Use a company Apple ID associated with an email account that will remain with your organization even if the user who manages the account leaves. Save this ID because you'll need to use the same ID when it's time to renew the certificate.</span><span class="sxs-lookup"><span data-stu-id="74392-p102">Use a company Apple ID associated with an email account that will remain with your organization even if the user who manages the account leaves. Save this ID because you'll need to use the same ID when it's time to renew the certificate.</span></span> 
  
  - <span data-ttu-id="74392-118">Select **Create a Certificate** and accept the **Terms of Use**.</span><span class="sxs-lookup"><span data-stu-id="74392-118">Select **Create a Certificate** and accept the **Terms of Use**.</span></span>
    
  - <span data-ttu-id="74392-119">**Browse** to the Certificate signing request you downloaded to your computer from Office 365 and select **Upload**.</span><span class="sxs-lookup"><span data-stu-id="74392-119">**Browse** to the Certificate signing request you downloaded to your computer from Office 365 and select **Upload**.</span></span>
    
  - <span data-ttu-id="74392-120">**Download** the APN certificate created by the Apple Push Certificate Portal to your computer.</span><span class="sxs-lookup"><span data-stu-id="74392-120">**Download** the APN certificate created by the Apple Push Certificate Portal to your computer.</span></span> 
    
    > [!TIP]
    > <span data-ttu-id="74392-121">If you're having trouble downloading the certificate, refresh your browser.</span><span class="sxs-lookup"><span data-stu-id="74392-121">If you're having trouble downloading the certificate, refresh your browser.</span></span> 
  
5. <span data-ttu-id="74392-122">Go back to Office 365 and select **Next** to get to the **Upload APNS certificate** page.</span><span class="sxs-lookup"><span data-stu-id="74392-122">Go back to Office 365 and select **Next** to get to the **Upload APNS certificate** page.</span></span> 
    
6. <span data-ttu-id="74392-123"> Browse to the APN certificate you downloaded from the Apple Push Certificates Portal.</span><span class="sxs-lookup"><span data-stu-id="74392-123">Browse to the APN certificate you downloaded from the Apple Push Certificates Portal.</span></span>
    
    ![Clique no botão procurar para selecionar o certificado APNS baixado da Apple](media/afe2849d-af23-4c55-9009-d8f25edaf6c0.png)
  
7. <span data-ttu-id="74392-125">Selecione **Concluir**.</span><span class="sxs-lookup"><span data-stu-id="74392-125">Select **Finish**.</span></span>
    
<span data-ttu-id="74392-126">Voltar ao \> centro de \*\*conformidade de segurança &amp; \*\* **as políticas** \> de segurança **Gerenciamento** \> de dispositivos **gerenciar configurações** para concluir a instalação.</span><span class="sxs-lookup"><span data-stu-id="74392-126">Go back to **Security &amp; Compliance Center** \> **Security policies** \> **Device management** \> **Manage settings** to complete setup.</span></span> 
  

