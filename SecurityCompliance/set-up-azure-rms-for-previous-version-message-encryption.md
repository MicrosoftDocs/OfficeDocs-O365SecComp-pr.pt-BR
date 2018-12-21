---
title: Configurar o Azure Rights Management para a versão anterior do Office 365 Message Encryption
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 10/30/2018
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 2cba47b3-f09e-4911-9207-ac056fcb9db7
description: A versão anterior do Office 365 Message Encryption depende do Microsoft Azure Rights Management (anteriormente conhecida como Windows Azure Active Directory Rights Management).
ms.openlocfilehash: 994364fd74881e40f97daa3c2d12e31282b421fd
ms.sourcegitcommit: 1c00bba6ddcdd7ead6cc0153c8a2c20de05262ba
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/20/2018
ms.locfileid: "27382920"
---
# <a name="set-up-azure-rights-management-for-the-previous-version-of-office-365-message-encryption"></a><span data-ttu-id="f6eb9-103">Configurar o Azure Rights Management para a versão anterior do Office 365 Message Encryption</span><span class="sxs-lookup"><span data-stu-id="f6eb9-103">Set up Azure Rights Management for the previous version of Office 365 Message Encryption</span></span>

<span data-ttu-id="f6eb9-104">Este tópico descreve as etapas que precisam ser seguidas para ativar e defina o Azure RMS (Rights Management), a parte de proteção de informações do Windows Azure, para uso com a versão anterior do Office 365 Message Encryption (OME).</span><span class="sxs-lookup"><span data-stu-id="f6eb9-104">This topic describes the steps you need to follow in order to activate and then set up Azure Rights Management (RMS), part of Azure Information Protection, for use with the previous version of Office 365 Message Encryption (OME).</span></span>

## <a name="this-article-only-applies-to-the-previous-version-of-ome"></a><span data-ttu-id="f6eb9-105">Este artigo se aplica apenas à versão anterior do OME</span><span class="sxs-lookup"><span data-stu-id="f6eb9-105">This article only applies to the previous version of OME</span></span>
<span data-ttu-id="f6eb9-p101">Se você ainda não migraram sua organização do Office 365 para os novos recursos OME, mas você já implantou OME, as informações neste artigo se aplicam à sua organização. A Microsoft recomenda que você faça um plano para mover-se para as novas capacidades OME tão logo razoáveis para sua organização. Para obter instruções, consulte [configurar novos recursos do Office 365 Message Encryption](set-up-new-message-encryption-capabilities.md). Se você deseja saber mais sobre como as novas capacidades funcionam pela primeira vez, consulte [Criptografia de mensagem do Office 365](ome.md). O restante deste artigo refere-se ao comportamento OME antes do lançamento de novos recursos OME.</span><span class="sxs-lookup"><span data-stu-id="f6eb9-p101">If you haven't yet moved your Office 365 organization to the new OME capabilities, but you have already deployed OME, then the information in this article applies to your organization. Microsoft recommends that you make a plan to move to the new OME capabilities as soon as it is reasonable for your organization. For instructions, see [Set up new Office 365 Message Encryption capabilities](set-up-new-message-encryption-capabilities.md). If you want to find out more about how the new capabilities work first, see [Office 365 Message Encryption](ome.md). The rest of this article refers to OME behavior before the release of the new OME capabilities.</span></span>

## <a name="prerequisites-for-using-the-previous-version-of-office-365-message-encryption"></a><span data-ttu-id="f6eb9-111">Pré-requisitos para usar a versão anterior do Office 365 Message Encryption</span><span class="sxs-lookup"><span data-stu-id="f6eb9-111">Prerequisites for using the previous version of Office 365 Message Encryption</span></span>
<span data-ttu-id="f6eb9-112"><a name="warmprereqs"> </a></span><span class="sxs-lookup"><span data-stu-id="f6eb9-112"></span></span>

<span data-ttu-id="f6eb9-p102">O Office 365 Message Encryption (OME), incluindo o IRM, depende do Azure Rights Management (RMS do Windows Azure). RMS Azure é a tecnologia de proteção usada pela proteção de informações do Windows Azure. Para usar o OME, sua organização do Office 365 deve incluir uma assinatura do Exchange Online ou Exchange Online Protection que, por sua vez, inclui uma assinatura de gerenciamento de direitos do Windows Azure.</span><span class="sxs-lookup"><span data-stu-id="f6eb9-p102">Office 365 Message Encryption (OME), including IRM, depends on Azure Rights Management (Azure RMS). Azure RMS is the protection technology used by Azure Information Protection. To use OME, your Office 365 organization must include an Exchange Online or Exchange Online Protection subscription that, in turn, includes an Azure Rights Management subscription.</span></span>
  
- <span data-ttu-id="f6eb9-116">Se você não tiver certeza sobre o que inclui a sua assinatura, consulte as descrições de serviço Exchange Online para [política de mensagem, recuperação e conformidade](https://technet.microsoft.com/library/exchange-online-message-policy-recovery-and-compliance.aspx).</span><span class="sxs-lookup"><span data-stu-id="f6eb9-116">If you're not sure of what your subscription includes, see the Exchange Online service descriptions for [Message Policy, Recovery, and Compliance](https://technet.microsoft.com/library/exchange-online-message-policy-recovery-and-compliance.aspx).</span></span>

- <span data-ttu-id="f6eb9-117">Se você não tiver uma assinatura do Windows Azure RMS para Exchange Online ou Exchange Online Protection, você deve adquirir uma assinatura e ativá-lo primeiro.</span><span class="sxs-lookup"><span data-stu-id="f6eb9-117">If you don't have an Azure RMS subscription for Exchange Online or Exchange Online Protection, you must purchase a subscription and activate it first.</span></span>

    <span data-ttu-id="f6eb9-p103">Para obter informações sobre como adquirir uma assinatura para o Azure Rights Management, consulte [Gerenciamento de direitos do Windows Azure](https://portal.office.com/Signup/MainSignUp15.aspx?&amp;OfferId=9DF77AF9-DAAE-4d51-8E0E-EEEADD4866B8&amp;dl=RIGHTSMANAGEMENT). A próxima seção fornece informações sobre como ativar o Azure Rights Management.</span><span class="sxs-lookup"><span data-stu-id="f6eb9-p103">For information about purchasing a subscription to Azure Rights Management, see [Azure Rights Management](https://portal.office.com/Signup/MainSignUp15.aspx?&amp;OfferId=9DF77AF9-DAAE-4d51-8E0E-EEEADD4866B8&amp;dl=RIGHTSMANAGEMENT). The next section gives you information about activating Azure Rights Management.</span></span>

- <span data-ttu-id="f6eb9-120">Se você tiver o Azure Rights Management, mas ele não está configurado para o Exchange Online ou Exchange Online Protection, este artigo explica como ativar o Azure Rights Management e, em seguida o descreve a melhor maneira de configurar OME para funcionar com o Azure Rights Management.</span><span class="sxs-lookup"><span data-stu-id="f6eb9-120">If you have Azure Rights Management but it's not set up for Exchange Online or Exchange Online Protection, this article explains how to activate Azure Rights Management and then the describes the best way to set up OME to work with Azure Rights Management.</span></span>

- <span data-ttu-id="f6eb9-p104">Se você já configurou OME para funcionar com o Azure Rights Management para o Exchange Online ou Exchange Online Protection, dependendo de como configurá-lo, você pode estar pronto para começar a usar o OME e seus novos recursos imediatamente. Este artigo explica como determinar se você configurou OME corretamente, o que fazer se você precisar alterar sua instalação e o que acontece se você optar por não alterar sua instalação. Por exemplo, para usar os novos recursos, você deve usar o RMS do Windows Azure com OME. Você não pode usar os novos recursos com um RMS diretório ativo do local.</span><span class="sxs-lookup"><span data-stu-id="f6eb9-p104">If you've already set up OME to work with Azure Rights Management for Exchange Online or Exchange Online Protection, depending on how you set it up, you may be ready to start using OME and its new capabilities right away. This article explains how to determine if you've set OME up correctly, what to do if you need to change your setup, and what happens if you choose not to change your setup. For example, in order to use the new capabilities, you must use Azure RMS with OME. You can't use the new capabilities with an on-premises Active Directory RMS.</span></span>

## <a name="activate-azure-rights-management-for--the-previous-version-of-ome-in-office-365"></a><span data-ttu-id="f6eb9-125">Ativar o Azure Rights Management para a versão anterior do OME no Office 365</span><span class="sxs-lookup"><span data-stu-id="f6eb9-125">Activate Azure Rights Management for  the previous version of OME in Office 365</span></span>

<span data-ttu-id="f6eb9-p105">Você precisa ativar o Azure Rights Management para que os usuários em sua organização possam aplicar proteção de informações para mensagens enviadas por eles e abrir mensagens e arquivos que foram protegidos pelo serviço de gerenciamento de direitos do Windows Azure. Para obter instruções, consulte [Ativar o Azure Rights Management](https://go.microsoft.com/fwlink/p/?LinkId=525775). Depois de ter concluído a ativação, volte aqui e continuar com as tarefas neste artigo.</span><span class="sxs-lookup"><span data-stu-id="f6eb9-p105">You need to activate Azure Rights Management so that the users in your organization can apply information protection to messages that they send, and open messages and files that have been protected by the Azure Rights Management service. For instructions, see [Activating Azure Rights Management](https://go.microsoft.com/fwlink/p/?LinkId=525775). Once you've completed the activation, return here and continue with the tasks in this article.</span></span>
  
## <a name="set-up-the-previous-version-of-ome-to-use-azure-rms-by-importing-trusted-publishing-domains-tpds"></a><span data-ttu-id="f6eb9-129">Configurar a versão anterior do OME para usar o Azure RMS importando domínios de publicação confiáveis (TPDs)</span><span class="sxs-lookup"><span data-stu-id="f6eb9-129">Set up the previous version of OME to use Azure RMS by importing trusted publishing domains (TPDs)</span></span>

<span data-ttu-id="f6eb9-p106">O TPD é um arquivo XML que contém informações sobre configurações de gerenciamento de direitos da sua organização. Por exemplo, o TPD contém informações sobre o certificado de licenciador de servidor (SLC) usado para assinatura e criptografia de certificados e licenças, as URLs usadas para licenciamento e publicação e assim por diante. Você pode importar o TPD para sua organização do Office 365 usando o Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="f6eb9-p106">A TPD is an XML file that contains information about your organization's rights management settings. For example, the TPD contains information about the server licensor certificate (SLC) used for signing and encrypting certificates and licenses, the URLs used for licensing and publishing, and so on. You import the TPD into your Office 365 organization by using Windows PowerShell.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="f6eb9-p107">Anteriormente, você pode optar por importar TPDs do serviço de gerenciamento de direitos do Active Directory (AD RMS) para sua organização do Office 365. No entanto, isso impedirá de usando os novos recursos OME e não é recomendado. Se sua organização estiver no momento do Office 365 configurado dessa forma, a Microsoft recomenda que você crie um plano para migrar do RMS de diretório ativo seu local à proteção de informações do Windows Azure baseados em nuvem. Para obter mais informações, consulte [Migrando do AD RMS à proteção de informações do Windows Azure](https://docs.microsoft.com/information-protection/plan-design/migrate-from-ad-rms-to-azure-rms). Você não poderá usar os novos recursos OME até que tenha concluído a migração à proteção de informações do Windows Azure.</span><span class="sxs-lookup"><span data-stu-id="f6eb9-p107">Previously, you could choose to import TPDs from the Active Directory Rights Management service (AD RMS) into your Office 365 organization. However, doing so will prevent you from using the new OME capabilities and is not recommended. If your Office 365 organization is currently configured this way, Microsoft recommends that you create a plan to migrate from your on-premises Active Directory RMS to cloud-based Azure Information Protection. For more information, see [Migrating from AD RMS to Azure Information Protection](https://docs.microsoft.com/information-protection/plan-design/migrate-from-ad-rms-to-azure-rms). You will not be able to use the new OME capabilities until you have completed the migration to Azure Information Protection.</span></span>
  
 <span data-ttu-id="f6eb9-138">**Para importar TPDs do RMS do Azure**</span><span class="sxs-lookup"><span data-stu-id="f6eb9-138">**To import TPDs from Azure RMS**</span></span>
  
1. <span data-ttu-id="f6eb9-139">[Conecte-se ao Exchange Online usando o PowerShell remoto](https://technet.microsoft.com/library/jj984289%28v=exchg.150%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="f6eb9-139">[Connect to Exchange Online Using Remote PowerShell](https://technet.microsoft.com/library/jj984289%28v=exchg.150%29.aspx).</span></span>

2. <span data-ttu-id="f6eb9-140">Escolha a URL de compartilhamento de chave que corresponde à localização geográfica do sua organização Office 365:</span><span class="sxs-lookup"><span data-stu-id="f6eb9-140">Choose the key-sharing URL that corresponds to your Office 365 organization's geographic location:</span></span>

|<span data-ttu-id="f6eb9-141">**Localização**</span><span class="sxs-lookup"><span data-stu-id="f6eb9-141">**Location**</span></span>|<span data-ttu-id="f6eb9-142">**URL do local de compartilhamento de chave**</span><span class="sxs-lookup"><span data-stu-id="f6eb9-142">**Key sharing location URL**</span></span>|
|:-----|:-----|
|<span data-ttu-id="f6eb9-143">América do Norte</span><span class="sxs-lookup"><span data-stu-id="f6eb9-143">North America</span></span>  <br/> |https://sp-rms.na.aadrm.com/TenantManagement/ServicePartner.svc  <br/> |
|<span data-ttu-id="f6eb9-144">União Europeia</span><span class="sxs-lookup"><span data-stu-id="f6eb9-144">European Union</span></span>  <br/> |https://sp-rms.eu.aadrm.com/TenantManagement/ServicePartner.svc  <br/> |
|<span data-ttu-id="f6eb9-145">Ásia</span><span class="sxs-lookup"><span data-stu-id="f6eb9-145">Asia</span></span>  <br/> |https://sp-rms.ap.aadrm.com/TenantManagement/ServicePartner.svc  <br/> |
|<span data-ttu-id="f6eb9-146">América do Sul</span><span class="sxs-lookup"><span data-stu-id="f6eb9-146">South America</span></span>  <br/> |https://sp-rms.sa.aadrm.com/TenantManagement/ServicePartner.svc  <br/> |
|<span data-ttu-id="f6eb9-147">Office 365 para agências governamentais (Nuvem de Comunidade Governamental)</span><span class="sxs-lookup"><span data-stu-id="f6eb9-147">Office 365 for Government (Government Community Cloud)</span></span>  <br/> <span data-ttu-id="f6eb9-148">Este local de compartilhamento de chave do RMS é reservado para clientes que adquiriram o Office 365 para SKUs do governo.</span><span class="sxs-lookup"><span data-stu-id="f6eb9-148">This RMS key-sharing location is reserved for customers who have purchased Office 365 for Government SKUs.</span></span>  <br/> |https://sp-rms.govus.aadrm.com/TenantManagement/ServicePartner.svc  <br/> |
   
3. <span data-ttu-id="f6eb9-149">Configure o local de compartilhamento de chave, executando o cmdlet [Set-IRMConfiguration](https://technet.microsoft.com/library/dd979792%28v=exchg.160%29.aspx) da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="f6eb9-149">Configure the key-sharing location by running the [Set-IRMConfiguration](https://technet.microsoft.com/library/dd979792%28v=exchg.160%29.aspx) cmdlet as follows:</span></span> 
    
  ```
  Set-IRMConfiguration -RMSOnlineKeySharingLocation "<RMSKeySharingURL >"
  ```

    <span data-ttu-id="f6eb9-150">Por exemplo, para configurar a chave local de compartilhamento se sua organização estiver localizada na América do Norte:</span><span class="sxs-lookup"><span data-stu-id="f6eb9-150">For example, to configure the key sharing location if your organization is located in North America:</span></span>
    
  ```
  Set-IRMConfiguration -RMSOnlineKeySharingLocation "https://sp-rms.na.aadrm.com/TenantManagement/ServicePartner.svc"
  ```

4. <span data-ttu-id="f6eb9-151">Execute o cmdlet [Import-RMSTrustedPublishingDomain](https://technet.microsoft.com/library/jj200724%28v=exchg.150%29.aspx) com a opção - RMSOnline para importar o TPD do gerenciamento de direitos do Windows Azure:</span><span class="sxs-lookup"><span data-stu-id="f6eb9-151">Run the [Import-RMSTrustedPublishingDomain](https://technet.microsoft.com/library/jj200724%28v=exchg.150%29.aspx) cmdlet with the -RMSOnline switch to import the TPD from Azure Rights Management:</span></span> 
    
  ```
  Import-RMSTrustedPublishingDomain -RMSOnline -Name "<TPDName> "
  ```

    <span data-ttu-id="f6eb9-p108">Onde *TPDName* é o nome que você deseja usar para o TPD. Por exemplo, "Contoso North American TPD".</span><span class="sxs-lookup"><span data-stu-id="f6eb9-p108">Where  *TPDName*  is the name you want to use for the TPD. For example, "Contoso North American TPD".</span></span> 
    
5. <span data-ttu-id="f6eb9-154">Para verificar se você configurou com êxito sua organização do Office 365 para usar o serviço de gerenciamento de direitos do Windows Azure, execute o cmdlet [Test-IRMConfiguration](https://technet.microsoft.com/library/dd979798%28v=exchg.160%29.aspx) com a opção - RMSOnline, da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="f6eb9-154">To verify that you successfully configured your Office 365 organization to use the Azure Rights Management service, run the [Test-IRMConfiguration](https://technet.microsoft.com/library/dd979798%28v=exchg.160%29.aspx) cmdlet with the -RMSOnline switch as follows:</span></span> 
    
  ```
  Test-IRMConfiguration -RMSOnline
  ```

    <span data-ttu-id="f6eb9-155">Entre outras coisas, este cmdlet verifica a conectividade com o serviço de gerenciamento de direitos do Windows Azure, baixa o TPD e verifica sua validade.</span><span class="sxs-lookup"><span data-stu-id="f6eb9-155">Among other things, this cmdlet checks connectivity with the Azure Rights Management service, downloads the TPD, and checks its validity.</span></span>
    
6. <span data-ttu-id="f6eb9-156">Execute o cmdlet [Set-IRMConfiguration](https://technet.microsoft.com/library/dd979792%28v=exchg.150%29.aspx) da seguinte maneira para desabilitar os modelos de gerenciamento de direitos do Windows Azure sejam disponíveis no Outlook na web e Outlook:</span><span class="sxs-lookup"><span data-stu-id="f6eb9-156">Run the [Set-IRMConfiguration](https://technet.microsoft.com/library/dd979792%28v=exchg.150%29.aspx) cmdlet as follows to disable Azure Rights Management templates from being available in Outlook on the web and Outlook:</span></span> 
    
  ```
  Set-IRMConfiguration -ClientAccessServerEnabled $false
  ```

7. <span data-ttu-id="f6eb9-157">Execute o cmdlet [Set-IRMConfiguration](https://technet.microsoft.com/library/dd979792%28v=exchg.150%29.aspx) da seguinte maneira para habilitar o Azure Rights Management para a sua organização de email baseada em nuvem e configurá-lo para usar o Azure Rights Management para a criptografia de mensagem do Office 365:</span><span class="sxs-lookup"><span data-stu-id="f6eb9-157">Run the [Set-IRMConfiguration](https://technet.microsoft.com/library/dd979792%28v=exchg.150%29.aspx) cmdlet as follows to enable Azure Rights Management for your cloud-based email organization and configure it to use Azure Rights Management for Office 365 Message Encryption:</span></span> 
    
  ```
  Set-IRMConfiguration -InternalLicensingEnabled $true
  ```

8. <span data-ttu-id="f6eb9-p109">Para verificar que você com êxito importado o TPD e habilitou o Azure Rights Management, use o cmdlet Test-IRMConfiguration para testar a funcionalidade de gerenciamento de direitos do Windows Azure. Para obter detalhes, consulte "Exemplo 1" em [Test-IRMConfiguration](https://technet.microsoft.com/library/dd979798%28v=exchg.150%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="f6eb9-p109">To verify that you have successfully imported the TPD and enabled Azure Rights Management, use the Test-IRMConfiguration cmdlet to test Azure Rights Management functionality. For details, see "Example 1" in [Test-IRMConfiguration](https://technet.microsoft.com/library/dd979798%28v=exchg.150%29.aspx).</span></span>
    
## <a name="i-have-the-previous-version-of-ome-set-up-with-active-directory-rights-management-not-azure-information-protection-what-do-i-do"></a><span data-ttu-id="f6eb9-160">Tenho a versão anterior do OME configurado com o Active Directory Rights Management não proteção de informações do Windows Azure, o que eu faço?</span><span class="sxs-lookup"><span data-stu-id="f6eb9-160">I have the previous version of OME set up with Active Directory Rights Management not Azure Information Protection, what do I do?</span></span>
<span data-ttu-id="f6eb9-161"><a name="importTPDs"> </a></span><span class="sxs-lookup"><span data-stu-id="f6eb9-161"></span></span>

<span data-ttu-id="f6eb9-p110">Você pode continuar a usar suas regras de fluxo de email existentes do Office 365 Message Encryption com gerenciamento de direitos do Active Directory, mas não é possível configurar ou usar os novos recursos OME. Em vez disso, será preciso migrar à proteção de informações do Windows Azure. Para obter informações sobre migração e o que isso significa para sua organização, consulte [Migrando do AD RMS à proteção de informações do Windows Azure](https://docs.microsoft.com/information-protection/deploy-use/prepare-environment-adrms).</span><span class="sxs-lookup"><span data-stu-id="f6eb9-p110">You can continue to use your existing Office 365 Message Encryption mail flow rules with Active Directory Rights Management, but you can't configure or use the new OME capabilities. Instead, you need to migrate to Azure Information Protection. For information about migration and what this means for your organization, see [Migrating from AD RMS to Azure Information Protection](https://docs.microsoft.com/information-protection/deploy-use/prepare-environment-adrms).</span></span>
  
## <a name="next-steps"></a><span data-ttu-id="f6eb9-165">Próximas etapas</span><span class="sxs-lookup"><span data-stu-id="f6eb9-165">Next steps</span></span>
<span data-ttu-id="f6eb9-166"><a name="importTPDs"> </a></span><span class="sxs-lookup"><span data-stu-id="f6eb9-166"></span></span>

<span data-ttu-id="f6eb9-167">Depois que você tiver concluído a instalação do Azure Rights Management, se você deseja habilitar os novos recursos de OME, consulte [configurar novos recursos do Office 365 Message Encryption construídos sobre a proteção de informações do Azure.](https://support.office.com/article/7ff0c040-b25c-4378-9904-b1b50210d00e)</span><span class="sxs-lookup"><span data-stu-id="f6eb9-167">Once you've completed Azure Rights Management setup, if you want to enable the new OME capabilities, see [Set up new Office 365 Message Encryption capabilities built on top of Azure Information Protection.](https://support.office.com/article/7ff0c040-b25c-4378-9904-b1b50210d00e)</span></span>
  
<span data-ttu-id="f6eb9-168">Depois de configurar sua organização para usar os novos recursos OME, você está pronto para [definir regras de fluxo de email para proteger as mensagens de email com os novos recursos OME](define-mail-flow-rules-to-encrypt-email.md).</span><span class="sxs-lookup"><span data-stu-id="f6eb9-168">After you've set up your organization to use the new OME capabilities, you're ready to [Define mail flow rules to protect email messages with new OME capabilities](define-mail-flow-rules-to-encrypt-email.md).</span></span>
  
## <a name="related-topics"></a><span data-ttu-id="f6eb9-169">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="f6eb9-169">Related topics</span></span>
<span data-ttu-id="f6eb9-170"><a name="importTPDs"> </a></span><span class="sxs-lookup"><span data-stu-id="f6eb9-170"></span></span>

[<span data-ttu-id="f6eb9-171">Criptografia no Office 365</span><span class="sxs-lookup"><span data-stu-id="f6eb9-171">Encryption in Office 365</span></span>](encryption.md)
  
[<span data-ttu-id="f6eb9-172">Detalhes de referências técnicas sobre a criptografia no Office 365</span><span class="sxs-lookup"><span data-stu-id="f6eb9-172">Technical reference details about encryption in Office 365</span></span>](technical-reference-details-about-encryption.md)
  
[<span data-ttu-id="f6eb9-173">Qual é o Azure Rights Management?</span><span class="sxs-lookup"><span data-stu-id="f6eb9-173">What is Azure Rights Management?</span></span>](https://docs.microsoft.com/information-protection/understand-explore/what-is-azure-rms)
  

