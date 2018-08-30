---
title: Definir backup Mobile Device Management (MDM) no Office 365
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 6/29/2018
ms.audience: Admin
ms.topic: get-started-article
f1_keywords:
- O365M_OverviewMDM
- 'O365E_OverviewMDM '
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MOE150
- MED150
- MBS150
- MET150
ms.assetid: dd892318-bc44-4eb1-af00-9db5430be3cd
description: O gerenciamento de dispositivos móveis internos para o Office 365 ajuda a proteger e gerenciar dispositivos móveis dos usuários, como iPhones, iPads, Androids, e telefones do Windows. Para começar, siga estas etapas para ativar e configurar o gerenciamento de dispositivos móveis para o Office 365.
ms.openlocfilehash: c92290170b2937067e7407787282eaaa368b25b7
ms.sourcegitcommit: c31424cafbf1953f2864d7e2ceb95b329a694edb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/29/2018
ms.locfileid: "23272356"
---
# <a name="set-up-mobile-device-management-mdm-in-office-365"></a><span data-ttu-id="6a424-104">Definir backup Mobile Device Management (MDM) no Office 365</span><span class="sxs-lookup"><span data-stu-id="6a424-104">Set up Mobile Device Management (MDM) in Office 365</span></span>

<span data-ttu-id="6a424-p102">O internas Mobile Device Management (MDM) para o Office 365 ajuda a proteger e gerenciar dispositivos móveis dos usuários, como iPhones, iPads, Androids, e telefones do Windows. Você pode criar e gerenciar diretivas de segurança de dispositivo, remotamente apagar um dispositivo e exibir relatórios detalhados de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="6a424-p102">The built-in Mobile Device Management (MDM) for Office 365 helps you secure and manage your users' mobile devices like iPhones, iPads, Androids, and Windows phones. You can create and manage device security policies, remotely wipe a device, and view detailed device reports.</span></span>
  
<span data-ttu-id="6a424-p103">Tem dúvidas? Nós incluímos [uma FAQ para ajudar a perguntas comuns sobre o endereço](frequently-asked-questions-about-mdm.md). Lembre-se de que você não pode usar um [parceiros: administração delegada de oferta](https://support.office.com/article/26530dc0-ebba-415b-86b1-b55bc06b073e) para gerenciar o gerenciamento de dispositivos móveis para o Office 365.</span><span class="sxs-lookup"><span data-stu-id="6a424-p103">Have questions? We've put together [a FAQ to help address common questions](frequently-asked-questions-about-mdm.md). Be aware that you cannot use a [Partners: Offer delegated administration](https://support.office.com/article/26530dc0-ebba-415b-86b1-b55bc06b073e) to manage Mobile Device Management for Office 365.</span></span> 
  
<span data-ttu-id="6a424-110">Gerenciamento de dispositivo é parte da segurança &amp; Centro de conformidade, portanto você precisará ir para disparar a instalação MDM lá.</span><span class="sxs-lookup"><span data-stu-id="6a424-110">Device management is part of the Security &amp; Compliance Center so you'll need to go there to kick off MDM setup.</span></span>
  
<span data-ttu-id="6a424-111">Para configurar o gerenciamento de dispositivos móveis para o Office 365 você precisará:</span><span class="sxs-lookup"><span data-stu-id="6a424-111">To set up Mobile Device Management for Office 365 you'll need to:</span></span>
  
1. [<span data-ttu-id="6a424-112">Ativar o serviço de gerenciamento de dispositivos móveis</span><span class="sxs-lookup"><span data-stu-id="6a424-112">Activate the Mobile Device Management service</span></span>](#activate-the-mobile-device-management-service)  
2. [<span data-ttu-id="6a424-113">Configurar o gerenciamento de dispositivos móveis</span><span class="sxs-lookup"><span data-stu-id="6a424-113">Set up Mobile Device Management</span></span>](#set-up-mobile-device-management)
3. [<span data-ttu-id="6a424-114">Certifique-se de usuários inscrever seus dispositivos</span><span class="sxs-lookup"><span data-stu-id="6a424-114">Make sure users enroll their devices</span></span>](#step-4-recommended-manage-device-security-policies)
  
## <a name="activate-the-mobile-device-management-service"></a><span data-ttu-id="6a424-115">Ativar o serviço de gerenciamento de dispositivos móveis</span><span class="sxs-lookup"><span data-stu-id="6a424-115">Activate the Mobile Device Management service</span></span>

1. <span data-ttu-id="6a424-116">Entre no Office 365 com sua conta corporativa ou de estudante.</span><span class="sxs-lookup"><span data-stu-id="6a424-116">Sign in to Office 365 with your work or school account.</span></span> 
    
2. <span data-ttu-id="6a424-117">Vá para [segurança &amp; Centro de conformidade](https://protection.office.com).</span><span class="sxs-lookup"><span data-stu-id="6a424-117">Go to [Security &amp; Compliance Center](https://protection.office.com).</span></span>
    
3. <span data-ttu-id="6a424-118">Navegue até a **prevenção de perda de dados** \> **gerenciamento de dispositivo** e clique em **Vamos começar** disparar o processo de ativação.</span><span class="sxs-lookup"><span data-stu-id="6a424-118">Navigate to **Data loss prevention** \> **Device management** and click **Let's get started** to kick off the activation process.</span></span> 
    
    ![Configurar o gerenciamento de dispositivos móveis para o Office 365](media/368e1026-9aa5-431b-a722-8f7cf528f263.png)
  
4. <span data-ttu-id="6a424-p104">Criamos uma política de segurança padrão para você para ajudá-lo a começar. Atualize o nome da diretiva de segurança nesta página e clique em **Iniciar a instalação**.</span><span class="sxs-lookup"><span data-stu-id="6a424-p104">We created a default security policy for you to help you get started. Update the name of the security policy on this page, and then click **Start setup**.</span></span>
    
    ![Definir a diretiva de segurança de gerenciamento de dispositivos móveis](media/5619a2d1-f900-4268-9050-5d7eb57429a5.png)
  
5. <span data-ttu-id="6a424-123">Você verá a tela de instalação que mostra o andamento sobre como configurar o serviço.</span><span class="sxs-lookup"><span data-stu-id="6a424-123">You'll see the setup screen that shows progress on setting up the service.</span></span>
    
    ![Progresso da instalação MDM](media/db45d1bb-d247-4ac0-9deb-1b0c1ace9bfa.png)
  
> [!TIP]
> <span data-ttu-id="6a424-p105">Você também pode localizar **MDM instalação** por meio de pesquisa. No Centro de administração do Office 365 \> página **inicial** , tipo de gerenciamento de dispositivos móveis na caixa **Pesquisar** . > ![Pesquisa para o gerenciamento de dispositivos móveis no Centro de administração](media/cd0ebf15-ef79-4eaa-ab5b-041ac0bd4e5b.png)</span><span class="sxs-lookup"><span data-stu-id="6a424-p105">You can also locate **MDM Setup** through Search. In the Office 365 admin center \> **Home** page, type mobile device management in the **Search** box. > ![Search for mobile device management in the admin center](media/cd0ebf15-ef79-4eaa-ab5b-041ac0bd4e5b.png)</span></span>
  
<span data-ttu-id="6a424-128">Ela pode levar algum tempo para ativar o gerenciamento de dispositivos móveis para o Office 365, mas quando ele estiver concluída, você receberá um email que explica as próximas etapas para usar.</span><span class="sxs-lookup"><span data-stu-id="6a424-128">It can take some time to activate Mobile Device Management for Office 365, but when it finishes, you'll receive an email that explains the next steps to take.</span></span>
  
## <a name="set-up-mobile-device-management"></a><span data-ttu-id="6a424-129">Configurar o gerenciamento de dispositivos móveis</span><span class="sxs-lookup"><span data-stu-id="6a424-129">Set up Mobile Device Management</span></span>

<span data-ttu-id="6a424-p106">Quando o serviço estiver pronto, conclua as quatro etapas a seguintes para concluir a instalação. Você talvez precise clicar em [Gerenciar configurações](https://portal.office.com/EAdmin/Device/IntuneInventory.aspx) na página **gerenciamento de dispositivo** na segurança &amp; Centro de conformidade para ver as configurações a seguir.</span><span class="sxs-lookup"><span data-stu-id="6a424-p106">When the service is ready, complete the following four steps to finish setup. You may need to click [Manage settings](https://portal.office.com/EAdmin/Device/IntuneInventory.aspx) on the **Device management** page in the Security &amp; Compliance Center to see the following settings.</span></span> 
  
![Configurar o gerenciamento de dispositivo móvel etapas obrigatórias e recomendadas](media/d71e3c76-b6b9-4549-ade6-cbfab846d908.png)
  
### <a name="step-1-required-configure-domains-for-mdm"></a><span data-ttu-id="6a424-133">Etapa 1: Domínios de Configure (obrigatório) para MDM</span><span class="sxs-lookup"><span data-stu-id="6a424-133">Step 1: (Required) Configure domains for MDM</span></span>

<span data-ttu-id="6a424-p107">Se você não tiver um domínio personalizado associado com o Office 365 ou se não estiver gerenciando dispositivos do Windows, você poderá ignorar esta seção. Caso contrário, você precisará adicionar registros DNS para o domínio no seu host DNS. Se você adicionou os registros já, como parte da configuração do seu domínio ao Office 365, você all está definido. Depois de adicionar os registros, os usuários do Office 365 em sua organização que entram em seu dispositivo do Windows com um endereço de email que usa seu domínio personalizado serão redirecionados para registrar-se no MDM para o Office 365.</span><span class="sxs-lookup"><span data-stu-id="6a424-p107">If you don't have a custom domain associated with Office 365 or if you're not managing Windows devices, you can skip this section. Otherwise, you'll need to add DNS records for the domain at your DNS host. If you've added the records already, as part of setting up your domain with Office 365, you're all set. After you add the records, Office 365 users in your organization who sign in on their Windows device with an email address that uses your custom domain are redirected to enroll in MDM for Office 365.</span></span>
  
<span data-ttu-id="6a424-p108">Precisa de ajuda para configurar os registros? Encontre seu registrador de domínio na lista fornecida em [criar registros DNS para Office 365 ao gerenciar seus registros DNS](https://support.office.com/article/b0f3fdca-8a80-4e8e-9ef3-61e8a2a9ab23) e selecione o nome do registrador para ir para a ajuda passo a passo para a criação de registros DNS. Use essas instruções para adicionar os dois registros a seguintes:</span><span class="sxs-lookup"><span data-stu-id="6a424-p108">Need help setting up the records? Find your domain registrar in the list provided in [Create DNS records for Office 365 when you manage your DNS records](https://support.office.com/article/b0f3fdca-8a80-4e8e-9ef3-61e8a2a9ab23) and select the registrar name to go to step-by-step help for creating DNS records. Use those instructions to add the following two records:</span></span> 
  
|<span data-ttu-id="6a424-141">**Nome do host**</span><span class="sxs-lookup"><span data-stu-id="6a424-141">**Host name**</span></span>|<span data-ttu-id="6a424-142">**Tipo de registro**</span><span class="sxs-lookup"><span data-stu-id="6a424-142">**Record type**</span></span>|<span data-ttu-id="6a424-143">**Endereço**</span><span class="sxs-lookup"><span data-stu-id="6a424-143">**Address**</span></span>|<span data-ttu-id="6a424-144">**TTL**</span><span class="sxs-lookup"><span data-stu-id="6a424-144">**TTL**</span></span>|
|:-----|:-----|:-----|:-----|
|<span data-ttu-id="6a424-145">EnterpriseEnrollment</span><span class="sxs-lookup"><span data-stu-id="6a424-145">EnterpriseEnrollment</span></span>  <br/> |<span data-ttu-id="6a424-146">CNAME</span><span class="sxs-lookup"><span data-stu-id="6a424-146">CNAME</span></span>  <br/> |<span data-ttu-id="6a424-147">EnterpriseEnrollment.manage.microsoft.com</span><span class="sxs-lookup"><span data-stu-id="6a424-147">EnterpriseEnrollment.manage.microsoft.com</span></span>  <br/> |<span data-ttu-id="6a424-148">3600</span><span class="sxs-lookup"><span data-stu-id="6a424-148">3600</span></span>  <br/> |
|<span data-ttu-id="6a424-149">EnterpriseRegistration</span><span class="sxs-lookup"><span data-stu-id="6a424-149">EnterpriseRegistration</span></span>  <br/> |<span data-ttu-id="6a424-150">CNAME</span><span class="sxs-lookup"><span data-stu-id="6a424-150">CNAME</span></span>  <br/> |<span data-ttu-id="6a424-151">EnterpriseRegistration.windows.net</span><span class="sxs-lookup"><span data-stu-id="6a424-151">EnterpriseRegistration.windows.net</span></span>  <br/> |<span data-ttu-id="6a424-152">3600</span><span class="sxs-lookup"><span data-stu-id="6a424-152">3600</span></span>  <br/> |
   
<span data-ttu-id="6a424-153">Depois de adicionar os dois registros, volte para a segurança &amp; Centro de conformidade e navegue até **gerenciamento de dispositivo** \> **Gerenciar configurações** para concluir a próxima etapa.</span><span class="sxs-lookup"><span data-stu-id="6a424-153">After you add the two records, go back to the Security &amp; Compliance Center and navigate to **Device management** \> **Manage settings** to complete the next step.</span></span> 
  
### <a name="step-2-required-configure-an-apns-certificate-for-ios-devices"></a><span data-ttu-id="6a424-154">Etapa 2: Configure (obrigatório) um certificado APNs para dispositivos iOS</span><span class="sxs-lookup"><span data-stu-id="6a424-154">Step 2: (Required) Configure an APNs Certificate for iOS devices</span></span>

<span data-ttu-id="6a424-155">Para gerenciar dispositivos iOS como iPad e iPhones, você precisará criar um certificado APNs.</span><span class="sxs-lookup"><span data-stu-id="6a424-155">To manage iOS devices like iPad and iPhones, you need to create an APNs certificate.</span></span>
  
<span data-ttu-id="6a424-156">Para fazer isso, siga as etapas nos links **Configurar** na **página de gerenciamento de dispositivo móvel de instalação**.</span><span class="sxs-lookup"><span data-stu-id="6a424-156">To do this, follow the steps from the **Set up** links on the **Setup mobile device management page**.</span></span>
  
1. <span data-ttu-id="6a424-157">Ao lado de **Configurar um certificado de APNs para dispositivos iOS**, selecione **Configurar**.</span><span class="sxs-lookup"><span data-stu-id="6a424-157">Next to **Configure a APNs Certificate for iOS devices**, select **Set up**.</span></span>
    
2. <span data-ttu-id="6a424-158">Selecione **baixar seu arquivo CSR** e salve a solicitação de certificado de assinatura em algum lugar no seu computador que irá se lembrar.</span><span class="sxs-lookup"><span data-stu-id="6a424-158">Select **Download your CSR file** and save the Certificate signing request to a somewhere on your computer that you'll remember.</span></span> 
    
    ![Instalar a caixa de diálogo certificado APN](media/03aa8a24-e95c-4077-9b6b-ef76a86bafd7.png)
  
3. <span data-ttu-id="6a424-160">Selecione **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="6a424-160">Select **Next**.</span></span>
    
4. <span data-ttu-id="6a424-161">Crie um certificado APN.</span><span class="sxs-lookup"><span data-stu-id="6a424-161">Create an APN certificate.</span></span>
    
  - <span data-ttu-id="6a424-162">Selecione **Apple APNS Portal** para abrir o Portal de certificados do Apple Push.</span><span class="sxs-lookup"><span data-stu-id="6a424-162">Select **Apple APNS Portal** to open the Apple Push Certificates Portal.</span></span> 
    
    ![Instalar a caixa de diálogo de cert de notificação de APN com o Portal do Apple APNS selecionado](media/ce19f53c-f44a-470b-baf3-9278dfda2ba5.png)
  
  - <span data-ttu-id="6a424-164">Entrar com uma ID de Apple.</span><span class="sxs-lookup"><span data-stu-id="6a424-164">Sign in with an Apple ID.</span></span>
    
    > [!IMPORTANT]
    > <span data-ttu-id="6a424-p109">Use uma empresa que Apple ID associado a uma conta de email que permanecerão com sua organização, mesmo se deixa o usuário que gerencia a conta. Salve este ID, pois você precisará usar a mesma identificação quando é hora de renovar o certificado.</span><span class="sxs-lookup"><span data-stu-id="6a424-p109">Use a company Apple ID associated with an email account that will remain with your organization even if the user who manages the account leaves. Save this ID because you'll need to use the same ID when it's time to renew the certificate.</span></span> 
  
  - <span data-ttu-id="6a424-167">Selecione **criar um certificado** e aceitar os **Termos de uso**.</span><span class="sxs-lookup"><span data-stu-id="6a424-167">Select **Create a Certificate** and accept the **Terms of Use**.</span></span>
    
  - <span data-ttu-id="6a424-168">**Navegue** para a assinatura de certificado solicitar que você baixou para seu computador do Office 365 e selecione **carregar**.</span><span class="sxs-lookup"><span data-stu-id="6a424-168">**Browse** to the Certificate signing request you downloaded to your computer from Office 365 and select **Upload**.</span></span>
    
  - <span data-ttu-id="6a424-169">**Baixar** o certificado APN criados pelo Portal de certificado do Apple Push ao seu computador.</span><span class="sxs-lookup"><span data-stu-id="6a424-169">**Download** the APN certificate created by the Apple Push Certificate Portal to your computer.</span></span> 
    
    > [!TIP]
    > <span data-ttu-id="6a424-170">Se você estiver tendo problemas baixando o certificado, atualize o navegador.</span><span class="sxs-lookup"><span data-stu-id="6a424-170">If you're having trouble downloading the certificate, refresh your browser.</span></span> 
  
5. <span data-ttu-id="6a424-171">Voltar para o Office 365 e selecione **Avançar** para chegar à página **APNS carregar certificado** .</span><span class="sxs-lookup"><span data-stu-id="6a424-171">Go back to Office 365 and select **Next** to get to the **Upload APNS certificate** page.</span></span> 
    
6. <span data-ttu-id="6a424-172">Navegue até o certificado APN que você baixou a partir do Portal de certificados do Apple Push.</span><span class="sxs-lookup"><span data-stu-id="6a424-172">Browse to the APN certificate you downloaded from the Apple Push Certificates Portal.</span></span>
    
    ![Clique no botão Procurar para selecionar o cert APNS que você baixou da Apple](media/afe2849d-af23-4c55-9009-d8f25edaf6c0.png)
  
7. <span data-ttu-id="6a424-174">Selecione **Concluir**.</span><span class="sxs-lookup"><span data-stu-id="6a424-174">Select **Finish**.</span></span>
    
<span data-ttu-id="6a424-175">Depois de Adicionar certificado APN, volte para a segurança &amp; Centro de conformidade e navegue até **gerenciamento de dispositivo** \> **Gerenciar configurações** para concluir a próxima etapa.</span><span class="sxs-lookup"><span data-stu-id="6a424-175">After you add APN Certificate, go back to the Security &amp; Compliance Center and navigate to **Device management** \> **Manage settings** to complete the next step.</span></span> 
  
### <a name="step-3-recommended-set-up-multi-factor-authentication"></a><span data-ttu-id="6a424-176">Etapa 3: (Recomendado) configurar a autenticação multifator</span><span class="sxs-lookup"><span data-stu-id="6a424-176">Step 3: (Recommended) Set up multi-factor authentication</span></span>

<span data-ttu-id="6a424-p110">Se você não vir a autenticação multifator (MFA) em **etapas recomendado**, você pode ignorar esta seção. Se essa opção estiver listada, recomendamos que você ativar MFA no portal do Azure AD para aumentar a segurança do gerenciamento de dispositivo móvel para o processo de inscrição do Office 365. Ele está desativado por padrão.</span><span class="sxs-lookup"><span data-stu-id="6a424-p110">If you don't see multi-factor authentication (MFA) under **Recommended steps**, you can skip this section. If this option is listed, we recommend you turn on MFA in the Azure AD portal to increase the security of the Mobile Device Management for Office 365 enrollment process. It is turned off by default.</span></span>
  
<span data-ttu-id="6a424-p111">MFA ajuda a proteger o entrar no Office 365 para o registro do dispositivo móvel exigindo uma segunda forma de autenticação. Os usuários são necessários para confirmar a uma chamada telefônica, uma mensagem de texto ou uma notificação de aplicativo em seu dispositivo móvel depois de inserir corretamente suas senhas de conta do trabalho. Eles só podem se inscrever seus dispositivos concluída a essa segunda forma de autenticação. Depois que os dispositivos dos usuários são inscritos no gerenciamento de dispositivos móveis para o Office 365, os usuários podem acessar os recursos do Office 365 com apenas sua conta do trabalho.</span><span class="sxs-lookup"><span data-stu-id="6a424-p111">MFA helps secure the sign in to Office 365 for mobile device enrollment by requiring a second form of authentication. Users are required to acknowledge a phone call, text message, or app notification on their mobile device after correctly entering their work account password. They can only enroll their device after this second form of authentication is completed. After users' devices are enrolled in Mobile Device Management for Office 365, users can access Office 365 resources with just their work account.</span></span>
  
<span data-ttu-id="6a424-p112">Ao lado de **Configurar a autenticação multifator**, selecione **Configurar**. Para saber como ativar MFA no portal do Azure AD, consulte [Configurar a autenticação multifator](https://go.microsoft.com/fwlink/p/?LinkId=519255).</span><span class="sxs-lookup"><span data-stu-id="6a424-p112">Next to **Set up multi-factor authentication**, select **Set up**. To learn how to turn on MFA in the Azure AD portal, see [Set up multi-factor authentication](https://go.microsoft.com/fwlink/p/?LinkId=519255).</span></span>
  
<span data-ttu-id="6a424-186">Depois de configurar MFA, volte para a segurança &amp; Centro de conformidade e navegue até **gerenciamento de dispositivo** \> **Gerenciar configurações** para concluir a próxima etapa.</span><span class="sxs-lookup"><span data-stu-id="6a424-186">After you set up MFA, go back to the Security &amp; Compliance Center and navigate to **Device management** \> **Manage settings** to complete the next step.</span></span> 
  
### <a name="step-4-recommended-manage-device-security-policies"></a><span data-ttu-id="6a424-187">Etapa 4: Diretivas de segurança de dispositivo gerenciar (recomendado)</span><span class="sxs-lookup"><span data-stu-id="6a424-187">Step 4: (Recommended) Manage device security policies</span></span>

<span data-ttu-id="6a424-p113">A próxima etapa é criar e implantar diretivas de segurança de dispositivo para ajudar a proteger os dados do sua organização Office 365. Por exemplo, você pode ajudar a evitar a perda de dados se um usuário perder seus dispositivos criando uma política para dispositivos de bloqueio após cinco minutos de inatividade e ter dispositivos apagada após 3 falhas entrar.</span><span class="sxs-lookup"><span data-stu-id="6a424-p113">The next step is to create and deploy device security policies to help protect your Office 365 organization's data. For example, you can help prevent data loss if a user loses their device by creating a policy to lock devices after 5 minutes of inactivity and have devices wiped after 3 sign-in failures.</span></span>
  
<span data-ttu-id="6a424-190">No **segurança &amp; Centro de conformidade**, acesse **as diretivas de segurança** \> **diretivas de segurança de dispositivo** para criar políticas de segurança de dispositivo e regras de acesso.</span><span class="sxs-lookup"><span data-stu-id="6a424-190">In the **Security &amp; Compliance Center**, go to **Security policies** \> **Device security policies** to create device security policies and access rules.</span></span> 
  
![Adicionar uma diretiva de segurança de dispositivo](media/69a027f5-fbfb-482a-b850-9ccb280b8c62.png)
  
<span data-ttu-id="6a424-192">Para obter instruções passo a passo sobre como criar uma nova política, consulte [criar e implantar diretivas de segurança de dispositivo](create-device-security-policies.md).</span><span class="sxs-lookup"><span data-stu-id="6a424-192">For step by step instructions on how to create a new policy, see [Create and deploy device security policies](create-device-security-policies.md).</span></span>
  
> [!TIP]
>  <span data-ttu-id="6a424-p114">Quando você cria uma nova política, você talvez queira definir a diretiva para permitir que violação de política de acesso e o relatório em que um dispositivo do usuário não é compatível com a política. Isso permite que você veja quantos dispositivos móveis poderiam ser afetados pela política sem bloqueio de acesso para o Office 365. > Antes de implantar uma nova diretiva para todas as pessoas na sua organização, é recomendável que testá-lo nos dispositivos usados por um pequeno número de usuários. > Além disso, antes de implantar políticas, permitem que sua organização Saiba os impactos potenciais da inscrição um dispositivo em MDM para Office 365. Dependendo de como configurar as políticas, os dispositivos que não estão em conformidade com eles (dispositivos incompatíveis) poderiam ser bloqueados acessem o Office 365. Não compatível com dispositivos também podem ter os aplicativos instalados, fotos e outras informações pessoais, que, em um dispositivo registrado, poderiam ser excluídas se o dispositivo é apagado. Mais informações: [Apagar um dispositivo móvel no Office 365](wipe-a-mobile-device.md).</span><span class="sxs-lookup"><span data-stu-id="6a424-p114">When you create a new policy, you might want to set the policy to allow access and report policy violation where a user's device isn't compliant with the policy. This lets you see how many mobile devices would be impacted by the policy without blocking access to Office 365. >  Before you deploy a new policy to everyone in your organization, we recommend you test it on the devices used by a small number of users. >  Also, before you deploy policies, let your organization know the potential impacts of enrolling a device in MDM for Office 365. Depending on how you set up the policies, devices that don't comply with them (non-compliant devices) could be blocked from accessing Office 365. Non-compliant devices might also have apps installed, photos, and other personal information which, on an enrolled device, could be deleted if the device is wiped. More info: [Wipe a mobile device in Office 365](wipe-a-mobile-device.md).</span></span> 
  
## <a name="make-sure-users-enroll-their-devices"></a><span data-ttu-id="6a424-200">Certifique-se de usuários inscrever seus dispositivos</span><span class="sxs-lookup"><span data-stu-id="6a424-200">Make sure users enroll their devices</span></span>

<span data-ttu-id="6a424-p115">Depois que você criou e implantou uma política de gerenciamento de dispositivo móvel, cada usuário licenciado do Office 365 em sua organização que se aplica a política de dispositivo, a receberá uma mensagem de inscrição na próxima vez que entrarem no Office 365 usando seu dispositivo móvel. Eles devem concluir as etapas de inscrição e ativação para poder acessar o email do Office 365 e documentos. Consulte [registrar seu dispositivo móvel para trabalho ou escola](enroll-your-mobile-device.md).</span><span class="sxs-lookup"><span data-stu-id="6a424-p115">After you've created and deployed a mobile device management policy, each licensed Office 365 user in your organization that the device policy applies to will receive an enrollment message the next time they sign into Office 365 from their mobile device. They must complete the enrollment and activation steps before they can access Office 365 email and documents. See [Enroll your mobile device for work or school](enroll-your-mobile-device.md).</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="6a424-p116">Se o idioma de preferência do usuário não é suportado pelo processo de inscrição, os usuários podem receber notificação de inscrição e as etapas em seus dispositivos móveis em outro idioma. Nem todos os idiomas com suporte no Office 365 são suportados atualmente para o processo de inscrição em dispositivos móveis.</span><span class="sxs-lookup"><span data-stu-id="6a424-p116">If a user's preferred language isn't supported by the enrollment process, users may receive enrollment notification and steps on their mobile devices in another language. Not all languages supported in Office 365 are currently supported for the enrollment process on mobile devices.</span></span> 
  
<span data-ttu-id="6a424-206">Usuários com dispositivos Android ou iOS são necessárias para instalar o aplicativo de Portal da empresa como parte do processo de inscrição.</span><span class="sxs-lookup"><span data-stu-id="6a424-206">Users with Android or iOS devices are required to install the Company Portal app as part of the enrollment process.</span></span>
  
## <a name="related-topics"></a><span data-ttu-id="6a424-207">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="6a424-207">Related Topics</span></span>

[<span data-ttu-id="6a424-208">Recursos de gerenciamento de dispositivos móveis</span><span class="sxs-lookup"><span data-stu-id="6a424-208">Capabilities of Mobile Device Management</span></span>](capabilities-of-mobile-device-management.md)
  
[<span data-ttu-id="6a424-209">Criar e implantar políticas de segurança de dispositivo</span><span class="sxs-lookup"><span data-stu-id="6a424-209">Create and deploy device security policies</span></span>](create-device-security-policies.md)
  

