---
title: Crie um certificado APNs para dispositivos iOS
ms.author: brendonb
author: brendonb
manager: laurawi
ms.date: 8/5/2016
ms.audience: Admin
ms.topic: get-started-article
f1_keywords:
- O365M_APNCertMDM
- O365E_APNCertMDM
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MOE150
- MED150
- MBS150
- MET150
ms.assetid: 522b43f4-a2ff-46f6-962a-dd4f47e546a7
description: Para gerenciar dispositivos iOS como iPad e iPhones no gerenciamento de dispositivos móveis para o Office 365, siga estas etapas para criar primeiro um certificado APNs.
ms.openlocfilehash: 28e8888d7dd57c3052cdcb5994725f11a5f0445f
ms.sourcegitcommit: c31424cafbf1953f2864d7e2ceb95b329a694edb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/29/2018
ms.locfileid: "23272046"
---
# <a name="create-an-apns-certificate-for-ios-devices"></a><span data-ttu-id="ee2e9-103">Crie um certificado APNs para dispositivos iOS</span><span class="sxs-lookup"><span data-stu-id="ee2e9-103">Create an APNs Certificate for iOS devices</span></span>

 <span data-ttu-id="ee2e9-104">Para gerenciar dispositivos iOS como iPad e iPhones no gerenciamento de dispositivos móveis para o Office 365, você deve criar um certificado APNs.</span><span class="sxs-lookup"><span data-stu-id="ee2e9-104">To manage iOS devices like iPad and iPhones in Mobile Device Management for Office 365 you must create an APNs certificate.</span></span> 
  
<span data-ttu-id="ee2e9-p101">Para fazer isso, siga as etapas no link **Configurar** na página do portal. (Vá para **segurança &amp; Centro de conformidade** \> **diretivas de segurança** \> **Device management** \> **Gerenciar definições**.)</span><span class="sxs-lookup"><span data-stu-id="ee2e9-p101">To do this, follow the steps from the **Set up** link on the portal page. (Go to **Security &amp; Compliance Center** \> **Security policies** \> **Device management** \> **Manage settings**.)</span></span>
  
![Configurar o gerenciamento de dispositivo móvel etapas obrigatórias e recomendadas](media/d71e3c76-b6b9-4549-ade6-cbfab846d908.png)
  
1. <span data-ttu-id="ee2e9-108">Ao lado de **Configurar um certificado de APNs para dispositivos iOS**, selecione **Configurar**.</span><span class="sxs-lookup"><span data-stu-id="ee2e9-108">Next to **Configure a APNs Certificate for iOS devices**, select **Set up**.</span></span>
    
2. <span data-ttu-id="ee2e9-109">Selecione **baixar seu arquivo CSR** e salve a solicitação de certificado de assinatura em algum lugar no seu computador que irá se lembrar.</span><span class="sxs-lookup"><span data-stu-id="ee2e9-109">Select **Download your CSR file** and save the Certificate signing request to a somewhere on your computer that you'll remember.</span></span> 
    
    ![Instalar a caixa de diálogo certificado APN](media/03aa8a24-e95c-4077-9b6b-ef76a86bafd7.png)
  
3. <span data-ttu-id="ee2e9-111">Selecione **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="ee2e9-111">Select **Next**.</span></span>
    
4. <span data-ttu-id="ee2e9-112">Crie um certificado APN.</span><span class="sxs-lookup"><span data-stu-id="ee2e9-112">Create an APN certificate.</span></span>
    
  - <span data-ttu-id="ee2e9-113">Selecione **Apple APNS Portal** para abrir o Portal de certificados do Apple Push.</span><span class="sxs-lookup"><span data-stu-id="ee2e9-113">Select **Apple APNS Portal** to open the Apple Push Certificates Portal.</span></span> 
    
    ![Instalar a caixa de diálogo de cert de notificação de APN com o Portal do Apple APNS selecionado](media/ce19f53c-f44a-470b-baf3-9278dfda2ba5.png)
  
  - <span data-ttu-id="ee2e9-115">Entrar com uma ID de Apple.</span><span class="sxs-lookup"><span data-stu-id="ee2e9-115">Sign in with an Apple ID.</span></span>
    
    > [!IMPORTANT]
    > <span data-ttu-id="ee2e9-p102">Use uma empresa que Apple ID associado a uma conta de email que permanecerão com sua organização, mesmo se deixa o usuário que gerencia a conta. Salve este ID, pois você precisará usar a mesma identificação quando é hora de renovar o certificado.</span><span class="sxs-lookup"><span data-stu-id="ee2e9-p102">Use a company Apple ID associated with an email account that will remain with your organization even if the user who manages the account leaves. Save this ID because you'll need to use the same ID when it's time to renew the certificate.</span></span> 
  
  - <span data-ttu-id="ee2e9-118">Selecione **criar um certificado** e aceitar os **Termos de uso**.</span><span class="sxs-lookup"><span data-stu-id="ee2e9-118">Select **Create a Certificate** and accept the **Terms of Use**.</span></span>
    
  - <span data-ttu-id="ee2e9-119">**Navegue** para a assinatura de certificado solicitar que você baixou para seu computador do Office 365 e selecione **carregar**.</span><span class="sxs-lookup"><span data-stu-id="ee2e9-119">**Browse** to the Certificate signing request you downloaded to your computer from Office 365 and select **Upload**.</span></span>
    
  - <span data-ttu-id="ee2e9-120">**Baixar** o certificado APN criados pelo Portal de certificado do Apple Push ao seu computador.</span><span class="sxs-lookup"><span data-stu-id="ee2e9-120">**Download** the APN certificate created by the Apple Push Certificate Portal to your computer.</span></span> 
    
    > [!TIP]
    > <span data-ttu-id="ee2e9-121">Se você estiver tendo problemas baixando o certificado, atualize o navegador.</span><span class="sxs-lookup"><span data-stu-id="ee2e9-121">If you're having trouble downloading the certificate, refresh your browser.</span></span> 
  
5. <span data-ttu-id="ee2e9-122">Voltar para o Office 365 e selecione **Avançar** para chegar à página **APNS carregar certificado** .</span><span class="sxs-lookup"><span data-stu-id="ee2e9-122">Go back to Office 365 and select **Next** to get to the **Upload APNS certificate** page.</span></span> 
    
6. <span data-ttu-id="ee2e9-123">Navegue até o certificado APN que você baixou a partir do Portal de certificados do Apple Push.</span><span class="sxs-lookup"><span data-stu-id="ee2e9-123">Browse to the APN certificate you downloaded from the Apple Push Certificates Portal.</span></span>
    
    ![Clique no botão Procurar para selecionar o cert APNS que você baixou da Apple](media/afe2849d-af23-4c55-9009-d8f25edaf6c0.png)
  
7. <span data-ttu-id="ee2e9-125">Selecione **Concluir**.</span><span class="sxs-lookup"><span data-stu-id="ee2e9-125">Select **Finish**.</span></span>
    
<span data-ttu-id="ee2e9-126">Volte para **segurança &amp; Centro de conformidade** \> **diretivas de segurança** \> **Device management** \> **Gerenciar configurações** para concluir a instalação.</span><span class="sxs-lookup"><span data-stu-id="ee2e9-126">Go back to **Security &amp; Compliance Center** \> **Security policies** \> **Device management** \> **Manage settings** to complete setup.</span></span> 
  

