---
title: Configurar novos recursos de Criptografia de Mensagens do Office 365
ms.author: krowley
author: kccross
manager: laurawi
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 7ff0c040-b25c-4378-9904-b1b50210d00e
description: Novos recursos de criptografia de mensagens do Office 365 criados sobre a proteção de informações do Azure, sua organização pode usar comunicação de email protegido com pessoas dentro e fora da sua organização. Os novos recursos do OME funcionam com outras organizações do Office 365, Outlook.com, Gmail e outros serviços de email.
ms.openlocfilehash: 90247a7e3cd7e5978eb144a2b6f66a9de21a8f96
ms.sourcegitcommit: baf23be44f1ed5abbf84f140b5ffa64fce605478
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/26/2019
ms.locfileid: "30296184"
---
# <a name="set-up-new-office-365-message-encryption-capabilities"></a><span data-ttu-id="cdb30-104">Configurar novos recursos de Criptografia de Mensagens do Office 365</span><span class="sxs-lookup"><span data-stu-id="cdb30-104">Set up new Office 365 Message Encryption capabilities</span></span>

<span data-ttu-id="cdb30-p102">Os novos recursos do Office 365 Message Encryption (OME) permitem que as organizações compartilhem emails protegidos com qualquer pessoa em qualquer dispositivo. Os usuários podem trocar mensagens protegidas com outras organizações do Office 365, bem como clientes não-Office 365 que usam o Outlook.com, o Gmail e outros serviços de email.</span><span class="sxs-lookup"><span data-stu-id="cdb30-p102">The new Office 365 Message Encryption (OME) capabilities allow organizations to share protected email with anyone on any device. Users can exchange protected messages with other Office 365 organizations, as well as non-Office 365 customers using Outlook.com, Gmail, and other email services.</span></span>


>[!NOTE]
><span data-ttu-id="cdb30-p103">Este artigo destina-se a administradores e profissionais de ti. Se você for um usuário final, consulte a lista de artigos no [Office 365 Message Encryption (ome)](ome.md) para obter soluções apropriadas.</span><span class="sxs-lookup"><span data-stu-id="cdb30-p103">This article is intended for administrators and IT professionals. If you're an end-user, see the list of articles in [Office 365 Message Encryption (OME)](ome.md) for appropriate solutions.</span></span>

<span data-ttu-id="cdb30-109">Siga as etapas abaixo para garantir que os novos recursos do OME estão disponíveis em seu locatário do Office 365.</span><span class="sxs-lookup"><span data-stu-id="cdb30-109">Follow the steps below to ensure that the New OME capabilities are available in your Office 365 tenant.</span></span> 

## <a name="verify-azure-rights-management-arm-is-active"></a><span data-ttu-id="cdb30-110">Verificar se o Azure Rights Management (ARM) está ativo</span><span class="sxs-lookup"><span data-stu-id="cdb30-110">Verify Azure Rights Management (ARM) is active</span></span>

>[!NOTE]
><span data-ttu-id="cdb30-111">Os novos recursos do OME aproveitam os recursos de proteção na [proteção de informações do Azure](https://docs.microsoft.com/en-us/azure/information-protection/what-is-information-protection), a tecnologia usada pelo [ARM (Azure Rights Management)](https://docs.microsoft.com/en-us/azure/information-protection/what-is-azure-rms).</span><span class="sxs-lookup"><span data-stu-id="cdb30-111">The new OME capabilities leverage the protection features in [Azure Information Protection](https://docs.microsoft.com/en-us/azure/information-protection/what-is-information-protection), the technology used by [Azure Rights Management (ARM)](https://docs.microsoft.com/en-us/azure/information-protection/what-is-azure-rms).</span></span>

<span data-ttu-id="cdb30-p104">O único pré-requisito para usar os novos recursos do OME é que o [Azure Rights Management (ARM)](https://docs.microsoft.com/en-us/azure/information-protection/what-is-azure-rms) deve ser ativado em seu locatário do Office 365. Se for, o Office 365 ativa os novos recursos do OME automaticamente e você não precisa fazer nada.</span><span class="sxs-lookup"><span data-stu-id="cdb30-p104">The only prerequisite for using the new OME capabilities is that [Azure Rights Management (ARM)](https://docs.microsoft.com/en-us/azure/information-protection/what-is-azure-rms) must be activated in your Office 365 tenant. If it is, Office 365 activates the new OME capabilities automatically and you don't need to do anything.</span></span> 

<span data-ttu-id="cdb30-p105">O ARM também é ativado automaticamente para os planos mais qualificados e, portanto, você provavelmente não precisará fazer nada nesse sentido. ConFira ativando o [Azure Rights Management](https://docs.microsoft.com/en-gb/azure/information-protection/activate-service) para mais.</span><span class="sxs-lookup"><span data-stu-id="cdb30-p105">ARM is also activated automatically for most eligible plans, so you probably don't have to do anything in this regard either. See [Activating Azure Rights Management](https://docs.microsoft.com/en-gb/azure/information-protection/activate-service) for more.</span></span>

>[!IMPORTANT]
><span data-ttu-id="cdb30-p106">Se você usar o AD RMS (Active Directory Rights Management Service) com o Exchange Online, precisará [migrar para a proteção de informações do Azure](https://docs.microsoft.com/en-us/azure/information-protection/migrate-from-ad-rms-to-azure-rms) antes de poder usar os novos recursos do ome. O AD RMS não é compatível com o ARM.</span><span class="sxs-lookup"><span data-stu-id="cdb30-p106">If you use Active Directory Rights Management service (AD RMS) with Exchange Online, you need to [migrate to Azure Information Protection](https://docs.microsoft.com/en-us/azure/information-protection/migrate-from-ad-rms-to-azure-rms) before you can use the new OME capabilities. AD RMS is not compatible with ARM.</span></span>  

<span data-ttu-id="cdb30-118">Para saber mais, confira:</span><span class="sxs-lookup"><span data-stu-id="cdb30-118">For more, see:</span></span>

- <span data-ttu-id="cdb30-119">[Quais assinaturas são necessárias para usar os novos recursos do ome?](ome-faq.md#what-subscriptions-do-i-need-to-use-the-new-ome-capabilities) para verificar se o seu plano de assinatura inclui a proteção de informações do Azure (que inclui o ARM).</span><span class="sxs-lookup"><span data-stu-id="cdb30-119">[What subscriptions do I need to use the new OME capabilities?](ome-faq.md#what-subscriptions-do-i-need-to-use-the-new-ome-capabilities) to check whether your subscription plan includes Azure Information Protection (which includes ARM).</span></span>   
-  <span data-ttu-id="cdb30-120">[Proteção de informações do Azure](https://azure.microsoft.com/en-us/services/information-protection/) para obter informações sobre como adquirir uma assinatura qualificada.</span><span class="sxs-lookup"><span data-stu-id="cdb30-120">[Azure Information Protection](https://azure.microsoft.com/en-us/services/information-protection/) for information about purchasing an eligible subscription.</span></span>  

### <a name="manually-activating-arm"></a><span data-ttu-id="cdb30-121">Ativando o braço manualmente</span><span class="sxs-lookup"><span data-stu-id="cdb30-121">Manually activating ARM</span></span>

<span data-ttu-id="cdb30-122">Se você desabilitou o braço, ou se ele não foi ativado automaticamente por algum motivo, você pode ativá-lo manualmente no:</span><span class="sxs-lookup"><span data-stu-id="cdb30-122">If you disabled ARM, or if it was not automatically activated for any reason, you can activated it manually in the :</span></span>

- <span data-ttu-id="cdb30-123">**Centro de administração do office 365**: Confira [como ativar o Azure Rights Management no centro de administração do Office 365](https://docs.microsoft.com/en-us/azure/information-protection/activate-office365) para obter instruções</span><span class="sxs-lookup"><span data-stu-id="cdb30-123">**Office 365 admin center**: See [How to activate Azure Rights Management from the Office 365 admin center](https://docs.microsoft.com/en-us/azure/information-protection/activate-office365) for instructions</span></span>
- <span data-ttu-id="cdb30-124">**Portal do Azure**: Confira [como ativar o Azure Rights Management no portal do Azure](https://docs.microsoft.com/en-gb/azure/information-protection/activate-azure) para obter instruções.</span><span class="sxs-lookup"><span data-stu-id="cdb30-124">**Azure portal**: See [How to activate Azure Rights Management from the Azure portal](https://docs.microsoft.com/en-gb/azure/information-protection/activate-azure) for instructions.</span></span> 


## <a name="configure-management-of-your-azure-information-protection-tenant-key"></a><span data-ttu-id="cdb30-125">Configurar o gerenciamento de sua chave do locatário de proteção de informações do Azure</span><span class="sxs-lookup"><span data-stu-id="cdb30-125">Configure management of your Azure Information Protection tenant key</span></span>

<span data-ttu-id="cdb30-p107">Esta é uma etapa opcional. Permitir que a Microsoft gerencie a chave raiz da proteção de informações do Azure é a configuração padrão e a prática recomendada recomendada para a maioria dos locatários do Office 365. Se esse for o caso, não será necessário fazer nada.</span><span class="sxs-lookup"><span data-stu-id="cdb30-p107">This is an optional step. Allowing Microsoft to manage the root key for Azure Information Protection is the default setting and recommended best practice for most Office 365 tenants. If this is the case, you don't need to do anything.</span></span> 

<span data-ttu-id="cdb30-p108">Há vários motivos, por exemplo, requisitos de conformidade, que podem exigir a geração e o gerenciamento de sua própria chave raiz (também conhecida como trazer sua própria chave (BYOK)). Se esse for o caso, recomendamos que você conclua as etapas necessárias antes de configurar os novos recursos do OME. ConFira [o planejamento e a implementação da chave do locatário de proteção de informações do Azure](https://docs.microsoft.com/information-protection/plan-design/plan-implement-tenant-key) para mais.</span><span class="sxs-lookup"><span data-stu-id="cdb30-p108">There are many reasons, for example compliance requirements, that may necessitate you generating and managing your own root key (also known as bring your own key (BYOK)). If this is the case, we recommend that you complete the required steps before setting up the new OME capabilities. See [Planning and implementing your Azure Information Protection tenant key](https://docs.microsoft.com/information-protection/plan-design/plan-implement-tenant-key) for more.</span></span> 


## <a name="verify-new-ome-configuration-in-exchange-online-powershell"></a><span data-ttu-id="cdb30-132">Verificar a nova configuração do OME no PowerShell do Exchange Online</span><span class="sxs-lookup"><span data-stu-id="cdb30-132">Verify new OME configuration in Exchange Online PowerShell</span></span>

<span data-ttu-id="cdb30-133">Você pode verificar se o seu locatário do Office 365 está configurado corretamente para usar os novos recursos do OME no [PowerShell do Exchange Online](https://docs.microsoft.com/en-us/powershell/exchange/exchange-online/exchange-online-powershell?view=exchange-ps).</span><span class="sxs-lookup"><span data-stu-id="cdb30-133">You can verify that your Office 365 tenant is properly configured to use the new OME capabilities in [Exchange Online PowerShell](https://docs.microsoft.com/en-us/powershell/exchange/exchange-online/exchange-online-powershell?view=exchange-ps).</span></span>
  
1. <span data-ttu-id="cdb30-134">[Conecte-se ao PowerShell do Exchange Online](https://docs.microsoft.com/en-us/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/connect-to-exchange-online-powershell) usando uma conta com permissões de administrador global em seu locatário do Office 365.</span><span class="sxs-lookup"><span data-stu-id="cdb30-134">[Connect to Exchange Online PowerShell](https://docs.microsoft.com/en-us/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/connect-to-exchange-online-powershell) using an account with global administrator permissions in your Office 365 tenant.</span></span>

2. <span data-ttu-id="cdb30-135">Execute o cmdlet Test-IRMConfiguration usando a seguinte sintaxe:</span><span class="sxs-lookup"><span data-stu-id="cdb30-135">Run the Test-IRMConfiguration cmdlet using the following syntax:</span></span>

     ```powershell
     Test-IRMConfiguration [-Sender <email address >]
     ```  

   <span data-ttu-id="cdb30-136">**Exemplo**:</span><span class="sxs-lookup"><span data-stu-id="cdb30-136">**Example**:</span></span> 
   
     ```powershell
     Test-IRMConfiguration -Sender securityadmin@contoso.com
     ```
     
     - <span data-ttu-id="cdb30-p109">Fornecer um email de remetente é opcional, mas obriga o sistema a executar verificações adicionais. Use o endereço de email de qualquer usuário em seu locatário do Office 365.</span><span class="sxs-lookup"><span data-stu-id="cdb30-p109">Providing a sender email is optional, but forces the system to perform additional checks. Use the email address of any user in your Office 365 tenant.</span></span> 
     
    <span data-ttu-id="cdb30-139">Os resultados devem ser semelhantes a:</span><span class="sxs-lookup"><span data-stu-id="cdb30-139">Your results should be similar to:</span></span>

     ```text
    Results : Acquiring RMS Templates ...
                - PASS: RMS Templates acquired.  Templates available: Contoso  - Confidential View Only, Contoso  - Confidential, Do Not 
            Forward.
            Verifying encryption ...
                - PASS: Encryption verified successfully.
            Verifying decryption ...
                - PASS: Decryption verified successfully.
            Verifying IRM is enabled ...
                - PASS: IRM verified successfully.

            OVERALL RESULT: PASS
    ```

   - <span data-ttu-id="cdb30-140">O nome da organização do Office 365 substituirá *contoso*.</span><span class="sxs-lookup"><span data-stu-id="cdb30-140">Your Office 365 organization name will replace *Contoso*.</span></span>

   - <span data-ttu-id="cdb30-p110">Os nomes de modelo padrão podem ser diferentes dos exibidos acima. ConFira conFigurando [e Gerenciando modelos para a proteção de informações do Azure](https://docs.microsoft.com/en-us/azure/information-protection/configure-policy-templates) para mais.</span><span class="sxs-lookup"><span data-stu-id="cdb30-p110">The default template names may be different from those displayed above. See [Configuring and managing templates for Azure Information Protection](https://docs.microsoft.com/en-us/azure/information-protection/configure-policy-templates) for more.</span></span>

3. <span data-ttu-id="cdb30-143">Execute o cmdlet Remove-PSSession para desconectar do serviço de gerenciamento de direitos.</span><span class="sxs-lookup"><span data-stu-id="cdb30-143">Run the Remove-PSSession cmdlet to disconnect from the Rights Management service.</span></span>
    
     ```powershell
     Remove-PSSession $session
     ```

## <a name="update-mail-flow-rules-to-use-new-ome-capabilities"></a><span data-ttu-id="cdb30-144">Atualizar regras de fluxo de email para usar novos recursos do OME</span><span class="sxs-lookup"><span data-stu-id="cdb30-144">Update mail flow rules to use new OME capabilities</span></span>

<span data-ttu-id="cdb30-p111">Se houver [regras de fluxo de email](define-mail-flow-rules-to-encrypt-email.md) configuradas anteriormente para criptografar emails em seu locatário do Office 365, você precisará atualizar essas regras existentes para usar os novos recursos do ome. Para novas implantações, esta etapa não é necessária neste estágio.</span><span class="sxs-lookup"><span data-stu-id="cdb30-p111">If there are previously configured [mail flow rules to encrypt email](define-mail-flow-rules-to-encrypt-email.md) in your Office 365 tenant, you need to update these existing rules to use the new OME capabilities. For new deployments, this step is unnecessary at this stage.</span></span>   

>[!Note]
><span data-ttu-id="cdb30-p112">As regras de fluxo de email definem as condições sob as quais as mensagens de email são criptografadas e quando a criptografia deve ser removida. ConFira [definir regras de fluxo de emails para criptografar mensagens de email no Office 365](define-mail-flow-rules-to-encrypt-email.md) .</span><span class="sxs-lookup"><span data-stu-id="cdb30-p112">Mail flow rules define the conditions under which email messages are encrypted, and when encryption should be removed. See [Define mail flow rules to encrypt email messages in Office 365](define-mail-flow-rules-to-encrypt-email.md) for more.</span></span>

<span data-ttu-id="cdb30-149">Para atualizar as regras existentes para usar os novos recursos do OME:</span><span class="sxs-lookup"><span data-stu-id="cdb30-149">To update existing rules to use the new OME capabilities:</span></span>

1. <span data-ttu-id="cdb30-150">No centro de administração do Office 365, acesse **centros de administração _GT_ Exchange**.</span><span class="sxs-lookup"><span data-stu-id="cdb30-150">In the Office 365 admin center, go to **Admin centers > Exchange**.</span></span>

2. <span data-ttu-id="cdb30-151">No centro de administração do Exchange, acesse **regras de > de fluxo**de emails.</span><span class="sxs-lookup"><span data-stu-id="cdb30-151">In the Exchange admin center, go to **Mail flow > Rules**.</span></span> 
3. <span data-ttu-id="cdb30-152">Para cada regra, em **faça o seguinte**:</span><span class="sxs-lookup"><span data-stu-id="cdb30-152">For each rule, in **Do the following**:</span></span>
    - <span data-ttu-id="cdb30-153">Selecione **Modificar a segurança da mensagem**.</span><span class="sxs-lookup"><span data-stu-id="cdb30-153">Select **Modify the message security**.</span></span>
    - <span data-ttu-id="cdb30-154">Selecione **aplicar a criptografia de mensagem do Office 365 e proteção de direitos**.</span><span class="sxs-lookup"><span data-stu-id="cdb30-154">Select **Apply Office 365 Message Encryption and rights protection**.</span></span>
    - <span data-ttu-id="cdb30-155">Selecionar um modelo do RMS na lista</span><span class="sxs-lookup"><span data-stu-id="cdb30-155">Select an RMS template from the list</span></span>
    - <span data-ttu-id="cdb30-156">Selecione **Salvar**.</span><span class="sxs-lookup"><span data-stu-id="cdb30-156">Select **Save**.</span></span>
    - <span data-ttu-id="cdb30-157">Selecione **OK**.</span><span class="sxs-lookup"><span data-stu-id="cdb30-157">Select **OK**.</span></span>
  
>[!IMPORTANT]
><span data-ttu-id="cdb30-158">Se você não atualizar as regras de fluxo de emails existentes, seus usuários continuarão a receber emails criptografados que usam o formato de anexo HTML anterior, em vez dos novos recursos do OME.</span><span class="sxs-lookup"><span data-stu-id="cdb30-158">If you do not update existing mail flow rules, your users will continue to receive encrypted mail that uses the previous HTML attachment format, instead of the new OME capabilities.</span></span>
