---
title: Criar um certificado APNs para dispositivos iOS
ms.author: brendonb
author: brendonb
manager: laurawi
ms.date: 8/5/2016
ms.audience: Admin
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
ms.openlocfilehash: 5f82690f0add5f1aae95a089d9cdfc0b320ae596
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30220451"
---
# <a name="create-an-apns-certificate-for-ios-devices"></a><span data-ttu-id="2e691-103">Criar um certificado APNs para dispositivos iOS</span><span class="sxs-lookup"><span data-stu-id="2e691-103">Create an APNs Certificate for iOS devices</span></span>

 <span data-ttu-id="2e691-104">Para gerenciar dispositivos iOS como iPad e iPhones no gerenciamento de dispositivos móveis para o Office 365, você deve criar um certificado APNs.</span><span class="sxs-lookup"><span data-stu-id="2e691-104">To manage iOS devices like iPad and iPhones in Mobile Device Management for Office 365 you must create an APNs certificate.</span></span> 
  
<span data-ttu-id="2e691-p101">Para fazer isso, siga as etapas do link **Configurar** na página do Portal. ( \> Acesse gerenciamento de **dispositivos** de **políticas** \> de segurança do \> **centro de conformidade de &amp; segurança** **gerenciar configurações**.)</span><span class="sxs-lookup"><span data-stu-id="2e691-p101">To do this, follow the steps from the **Set up** link on the portal page. (Go to **Security &amp; Compliance Center** \> **Security policies** \> **Device management** \> **Manage settings**.)</span></span>
  
![Configurar o gerenciamento de dispositivo móvel necessário e as etapas recomendadas](media/d71e3c76-b6b9-4549-ade6-cbfab846d908.png)
  
1. <span data-ttu-id="2e691-108">Ao lado de **configurar um certificado APNs para dispositivos IOS**, selecione **Configurar**.</span><span class="sxs-lookup"><span data-stu-id="2e691-108">Next to **Configure a APNs Certificate for iOS devices**, select **Set up**.</span></span>
    
2. <span data-ttu-id="2e691-109">Selecione **baixar seu arquivo CSR** e salvar a solicitação de assinatura de certificado em algum lugar no seu computador que você se lembrará.</span><span class="sxs-lookup"><span data-stu-id="2e691-109">Select **Download your CSR file** and save the Certificate signing request to a somewhere on your computer that you'll remember.</span></span> 
    
    ![Caixa de diálogo Instalar certificado APN](media/03aa8a24-e95c-4077-9b6b-ef76a86bafd7.png)
  
3. <span data-ttu-id="2e691-111">Selecione **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="2e691-111">Select **Next**.</span></span>
    
4. <span data-ttu-id="2e691-112">Criar um certificado APN.</span><span class="sxs-lookup"><span data-stu-id="2e691-112">Create an APN certificate.</span></span>
    
  - <span data-ttu-id="2e691-113">Selecione **portal Apple APNS** para abrir o portal Apple Push Certificates.</span><span class="sxs-lookup"><span data-stu-id="2e691-113">Select **Apple APNS Portal** to open the Apple Push Certificates Portal.</span></span> 
    
    ![Instalar a caixa de diálogo de certificado de notificação APN com o portal Apple APNS selecionado](media/ce19f53c-f44a-470b-baf3-9278dfda2ba5.png)
  
  - <span data-ttu-id="2e691-115">Entre com uma ID da Apple.</span><span class="sxs-lookup"><span data-stu-id="2e691-115">Sign in with an Apple ID.</span></span>
    
    > [!IMPORTANT]
    > <span data-ttu-id="2e691-p102">Use uma ID da Apple associada a uma conta de email que permanecerá com sua organização, mesmo que o usuário que gerencia a conta saia. Salve esta ID porque você precisará usar a mesma ID quando for hora de renovar o certificado.</span><span class="sxs-lookup"><span data-stu-id="2e691-p102">Use a company Apple ID associated with an email account that will remain with your organization even if the user who manages the account leaves. Save this ID because you'll need to use the same ID when it's time to renew the certificate.</span></span> 
  
  - <span data-ttu-id="2e691-118">Selecione **criar um certificado** e aceitar os **termos de uso**.</span><span class="sxs-lookup"><span data-stu-id="2e691-118">Select **Create a Certificate** and accept the **Terms of Use**.</span></span>
    
  - <span data-ttu-id="2e691-119">**Navegue** até a solicitação de assinatura de certificado que você baixou para seu computador no Office 365 e selecione **carregar**.</span><span class="sxs-lookup"><span data-stu-id="2e691-119">**Browse** to the Certificate signing request you downloaded to your computer from Office 365 and select **Upload**.</span></span>
    
  - <span data-ttu-id="2e691-120">**Baixe** o certificado APN criado pelo portal de certificado por push da Apple no seu computador.</span><span class="sxs-lookup"><span data-stu-id="2e691-120">**Download** the APN certificate created by the Apple Push Certificate Portal to your computer.</span></span> 
    
    > [!TIP]
    > <span data-ttu-id="2e691-121">Se você estiver tendo problemas para baixar o certificado, atualize seu navegador.</span><span class="sxs-lookup"><span data-stu-id="2e691-121">If you're having trouble downloading the certificate, refresh your browser.</span></span> 
  
5. <span data-ttu-id="2e691-122">Volte para o Office 365 e selecione **Avançar** para acessar a página **carregar certificado APNS** .</span><span class="sxs-lookup"><span data-stu-id="2e691-122">Go back to Office 365 and select **Next** to get to the **Upload APNS certificate** page.</span></span> 
    
6. <span data-ttu-id="2e691-123">Navegue até o certificado APN que você baixou do portal de certificados por push da Apple.</span><span class="sxs-lookup"><span data-stu-id="2e691-123">Browse to the APN certificate you downloaded from the Apple Push Certificates Portal.</span></span>
    
    ![Clique no botão procurar para selecionar o certificado APNS baixado da Apple](media/afe2849d-af23-4c55-9009-d8f25edaf6c0.png)
  
7. <span data-ttu-id="2e691-125">Selecione **concluir**.</span><span class="sxs-lookup"><span data-stu-id="2e691-125">Select **Finish**.</span></span>
    
<span data-ttu-id="2e691-126">Voltar ao \> centro de \*\*conformidade de segurança &amp; \*\* **as políticas** \> de segurança **Gerenciamento** \> de dispositivos **gerenciar configurações** para concluir a instalação.</span><span class="sxs-lookup"><span data-stu-id="2e691-126">Go back to **Security &amp; Compliance Center** \> **Security policies** \> **Device management** \> **Manage settings** to complete setup.</span></span> 
  

