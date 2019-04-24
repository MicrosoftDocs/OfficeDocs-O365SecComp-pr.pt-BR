---
title: Proteção contra ameaças no Office 365
ms.author: tracyp
author: msfttracyp
manager: laurawi
ms.audience: Admin
ms.topic: hub-page
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: b10023f6-f30f-45d3-b3ad-b71aa4aa0d58
ms.collection:
- M365-security-compliance
description: Use este artigo como guia para configurar seus recursos de proteção contra ameaças agora.
ms.openlocfilehash: 065071999130f209d63bcafc09ad72daceceac04
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32261629"
---
# <a name="protect-against-threats-in-office-365"></a><span data-ttu-id="b21ff-103">Proteção contra ameaças no Office 365</span><span class="sxs-lookup"><span data-stu-id="b21ff-103">Protect against threats in Office 365</span></span>

<span data-ttu-id="b21ff-104">O Office 365 inclui vários recursos de proteção contra ameaças.</span><span class="sxs-lookup"><span data-stu-id="b21ff-104">Office 365 includes a variety of threat protection features.</span></span> <span data-ttu-id="b21ff-105">Este é um guia de início rápido que você pode usar como uma lista de verificação para garantir que seus recursos de proteção contra ameaças estejam configurados para sua organização.</span><span class="sxs-lookup"><span data-stu-id="b21ff-105">Here's a quick-start guide you can use as a checklist to make sure your threat protection features are set up for your organization.</span></span> <span data-ttu-id="b21ff-106">Se você é novo em recursos de proteção contra ameaças no Office 365, ou se não tem certeza de onde começar, use a seguinte orientação como ponto de partida.</span><span class="sxs-lookup"><span data-stu-id="b21ff-106">If you're new to threat protection features in Office 365, or you're just not sure where to begin, use the following guidance as a starting point.</span></span> 

> [!IMPORTANT]
> <span data-ttu-id="b21ff-107">**As configurações iniciais recomendadas são incluídas para cada tipo de política; no entanto, muitas opções estão disponíveis e você pode ajustar suas configurações para atender às necessidades específicas da sua organização**.</span><span class="sxs-lookup"><span data-stu-id="b21ff-107">**Initial recommended settings are included for each kind of policy; however, many options are available, and you can adjust your settings to meet your specific organization's needs**.</span></span> <span data-ttu-id="b21ff-108">Aguarde aproximadamente 30 minutos para que as políticas ou as alterações funcionem da mesma forma por meio do datacenter.</span><span class="sxs-lookup"><span data-stu-id="b21ff-108">Allow approximately 30 minutes for your policies or changes to work their way through your datacenter.</span></span>

## <a name="requirements"></a><span data-ttu-id="b21ff-109">Requirements</span><span class="sxs-lookup"><span data-stu-id="b21ff-109">Requirements</span></span>

### <a name="licenses"></a><span data-ttu-id="b21ff-110">Licenças</span><span class="sxs-lookup"><span data-stu-id="b21ff-110">Licenses</span></span>

<span data-ttu-id="b21ff-111">Os recursos de proteção contra ameaças estão incluídos em todas as assinaturas do Office 365; no entanto, algumas assinaturas incluem recursos mais avançados, como as da proteção avançada contra ameaças do Office 365.</span><span class="sxs-lookup"><span data-stu-id="b21ff-111">Threat protection features are included in all Office 365 subscriptions; however, some subscriptions include more advanced features, such as those in Office 365 Advanced Threat Protection.</span></span> <span data-ttu-id="b21ff-112">Neste artigo, incluímos os requisitos de assinatura de cada área de proteção.</span><span class="sxs-lookup"><span data-stu-id="b21ff-112">In this article we include subscription requirements for each protection area.</span></span>

<span data-ttu-id="b21ff-113">Para saber mais sobre os recursos de proteção contra ameaças e o subsriptions, consulte os seguintes recursos:</span><span class="sxs-lookup"><span data-stu-id="b21ff-113">To learn more about threat protection features and subsriptions, see the following resources:</span></span>
- [<span data-ttu-id="b21ff-114">Descrição do Serviço da Proteção Avançada contra Ameaças do Office 365</span><span class="sxs-lookup"><span data-stu-id="b21ff-114">Office 365 Advanced Threat Protection Service Description</span></span>](https://docs.microsoft.com/office365/servicedescriptions/office-365-advanced-threat-protection-service-description)
- [<span data-ttu-id="b21ff-115">Descrição do Serviço do Exchange Online Protection</span><span class="sxs-lookup"><span data-stu-id="b21ff-115">Exchange Online Protection Service Description</span></span>](https://docs.microsoft.com/en-us/office365/servicedescriptions/exchange-online-protection-service-description/exchange-online-protection-service-description)
- [<span data-ttu-id="b21ff-116">Centro de Conformidade e Segurança do Office 365</span><span class="sxs-lookup"><span data-stu-id="b21ff-116">Office 365 Security & Compliance Center</span></span>](https://docs.microsoft.com/office365/servicedescriptions/office-365-platform-service-description/office-365-securitycompliance-center)

### <a name="roles-and-permissions"></a><span data-ttu-id="b21ff-117">Funções e permissões</span><span class="sxs-lookup"><span data-stu-id="b21ff-117">Roles and permissions</span></span>

<span data-ttu-id="b21ff-118">Você deve receber uma função apropriada para configurar políticas no centro de [conformidade do & de segurança](https://docs.microsoft.com/office365/servicedescriptions/office-365-platform-service-description/office-365-securitycompliance-center).</span><span class="sxs-lookup"><span data-stu-id="b21ff-118">You must be assigned an appropriate role to configure policies in the [Security & Compliance Center](https://docs.microsoft.com/office365/servicedescriptions/office-365-platform-service-description/office-365-securitycompliance-center).</span></span> <span data-ttu-id="b21ff-119">A tabela a seguir inclui alguns exemplos:</span><span class="sxs-lookup"><span data-stu-id="b21ff-119">The following table includes some examples:</span></span> 

|<span data-ttu-id="b21ff-120">Função ou grupo de função</span><span class="sxs-lookup"><span data-stu-id="b21ff-120">Role or role group</span></span>  |<span data-ttu-id="b21ff-121">Onde saber mais</span><span class="sxs-lookup"><span data-stu-id="b21ff-121">Where to learn more</span></span>  |
|---------|---------|
|<span data-ttu-id="b21ff-122">Administrador global do Office 365</span><span class="sxs-lookup"><span data-stu-id="b21ff-122">Office 365 Global Administrator</span></span> |[<span data-ttu-id="b21ff-123">Tudo sobre as funções de administrador do Office 365</span><span class="sxs-lookup"><span data-stu-id="b21ff-123">About Office 365 admin roles</span></span>](https://docs.microsoft.com/office365/admin/add-users/about-admin-roles)|
|<span data-ttu-id="b21ff-124">Administrador de segurança</span><span class="sxs-lookup"><span data-stu-id="b21ff-124">Security Administrator</span></span> |[<span data-ttu-id="b21ff-125">Permissões de função de administrador no Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="b21ff-125">Administrator role permissions in Azure Active Directory</span></span>](https://docs.microsoft.com/en-us/azure/active-directory/users-groups-roles/directory-assign-admin-roles)|
|<span data-ttu-id="b21ff-126">Gerenciamento da organização do Exchange Online</span><span class="sxs-lookup"><span data-stu-id="b21ff-126">Exchange Online Organization Management</span></span> |[<span data-ttu-id="b21ff-127">Permissões no Exchange Online</span><span class="sxs-lookup"><span data-stu-id="b21ff-127">Permissions in Exchange Online</span></span>](https://docs.microsoft.com/en-us/exchange/permissions-exo/permissions-exo) <br><span data-ttu-id="b21ff-128">e</span><span class="sxs-lookup"><span data-stu-id="b21ff-128">and</span></span><br> [<span data-ttu-id="b21ff-129">Exchange Online PowerShell</span><span class="sxs-lookup"><span data-stu-id="b21ff-129">Exchange Online PowerShell</span></span>](https://docs.microsoft.com/powershell/exchange/exchange-online/exchange-online-powershell?view=exchange-ps)|

<span data-ttu-id="b21ff-130">Para saber mais, confira [permissões no centro de conformidade &amp; de segurança do Office 365](permissions-in-the-security-and-compliance-center.md).</span><span class="sxs-lookup"><span data-stu-id="b21ff-130">To learn more, see [Permissions in the Office 365 Security &amp; Compliance Center](permissions-in-the-security-and-compliance-center.md).</span></span>

## <a name="part-1---anti-malware"></a><span data-ttu-id="b21ff-131">Parte 1-anti-malware</span><span class="sxs-lookup"><span data-stu-id="b21ff-131">Part 1 - Anti-malware</span></span>

<span data-ttu-id="b21ff-132">A [proteção Antimalware](anti-malware-protection.md) está disponível em assinaturas que incluem o [Exchange Online Protection](https://docs.microsoft.com/office365/servicedescriptions/exchange-online-protection-service-description) (EOP).</span><span class="sxs-lookup"><span data-stu-id="b21ff-132">[Anti-malware protection](anti-malware-protection.md) is available in subscriptions that include [Exchange Online Protection](https://docs.microsoft.com/office365/servicedescriptions/exchange-online-protection-service-description) (EOP).</span></span> 

1. <span data-ttu-id="b21ff-133">No [centro de conformidade do & de segurança](https://protection.office.com), escolha**anti-malware**de**política** > de **Gerenciamento** > de ameaças.</span><span class="sxs-lookup"><span data-stu-id="b21ff-133">In the [Security & Compliance Center](https://protection.office.com), choose **Threat management** > **Policy** > **Anti-malware**.</span></span>

2. <span data-ttu-id="b21ff-134">Clique duas vezes na política **padrão** e, em seguida, escolha **configurações**.</span><span class="sxs-lookup"><span data-stu-id="b21ff-134">Double-click the **Default** policy, and then choose **settings**.</span></span>

3. <span data-ttu-id="b21ff-135">Especifique as seguintes configurações:</span><span class="sxs-lookup"><span data-stu-id="b21ff-135">Specify the following settings:</span></span>
    
    - <span data-ttu-id="b21ff-136">Na seção **resposta de detecção de malware** , mantenha a configuração padrão **no**.</span><span class="sxs-lookup"><span data-stu-id="b21ff-136">In the **Malware Detection Response** section, keep the default setting of **No**.</span></span>
   
    - <span data-ttu-id="b21ff-137">Na seção **filtro de tipos de anexo comuns** , escolha **ativado**.</span><span class="sxs-lookup"><span data-stu-id="b21ff-137">In the **Common Attachment Types Filter** section, choose **On**.</span></span>

4. <span data-ttu-id="b21ff-138">Clique em **Salvar**.</span><span class="sxs-lookup"><span data-stu-id="b21ff-138">Click **Save**.</span></span>

<span data-ttu-id="b21ff-139">Para saber mais sobre opções de política Antimalware, consulte [Configure anti-malware Policies](configure-anti-malware-policies.md).</span><span class="sxs-lookup"><span data-stu-id="b21ff-139">To learn more about anti-malware policy options, see [Configure anti-malware policies](configure-anti-malware-policies.md).</span></span>

## <a name="part-2---zero-day-protection"></a><span data-ttu-id="b21ff-140">Parte 2-proteção de dia zero</span><span class="sxs-lookup"><span data-stu-id="b21ff-140">Part 2 - Zero-day protection</span></span>

<span data-ttu-id="b21ff-141">A proteção de dia zero está disponível em assinaturas que incluem a [proteção avançada contra ameaças (ATP) do Office 365](https://docs.microsoft.com/office365/servicedescriptions/office-365-advanced-threat-protection-service-description) e é configurada por meio de [anexos seguros ATP](atp-safe-attachments.md) e políticas de [links seguros de ATP](atp-safe-links.md) .</span><span class="sxs-lookup"><span data-stu-id="b21ff-141">Zero-day protection is available in subscriptions that include [Office 365 Advanced Threat Protection](https://docs.microsoft.com/office365/servicedescriptions/office-365-advanced-threat-protection-service-description) (ATP), and is set up through [ATP Safe Attachments](atp-safe-attachments.md) and [ATP Safe Links](atp-safe-links.md) policies.</span></span>

### <a name="atp-safe-attachments-policies"></a><span data-ttu-id="b21ff-142">Políticas de anexos seguros de ATP</span><span class="sxs-lookup"><span data-stu-id="b21ff-142">ATP Safe Attachments policies</span></span>

<span data-ttu-id="b21ff-143">Para configurar [anexos de segurança ATP](atp-safe-attachments.md), você deve definir pelo menos uma política de anexos seguros de ATP.</span><span class="sxs-lookup"><span data-stu-id="b21ff-143">To set up [ATP Safe Attachments](atp-safe-attachments.md), you must define at least one ATP Safe Attachments policy.</span></span> 

1. <span data-ttu-id="b21ff-144">No [centro de conformidade do & de segurança](https://protection.office.com), escolha a**política** > de **Gerenciamento** > de ameaça**anexos seguros de ATP**.</span><span class="sxs-lookup"><span data-stu-id="b21ff-144">In the [Security & Compliance Center](https://protection.office.com), choose **Threat management** > **Policy** > **ATP safe attachments**.</span></span>

2. <span data-ttu-id="b21ff-145">Selecione a opção **ativar a ATP para SharePoint, onedrive e Microsoft Teams**.</span><span class="sxs-lookup"><span data-stu-id="b21ff-145">Select the option **Turn on ATP for SharePoint, OneDrive, and Microsoft Teams**.</span></span>

3. <span data-ttu-id="b21ff-146">Na seção **proteger anexos de email** , clique no sinal de mais**+**().</span><span class="sxs-lookup"><span data-stu-id="b21ff-146">In the **Protect email attachments** section, click the plus sign (**+**).</span></span>

4. <span data-ttu-id="b21ff-147">Especifique as seguintes configurações:</span><span class="sxs-lookup"><span data-stu-id="b21ff-147">Specify the following settings:</span></span>

    - <span data-ttu-id="b21ff-148">Na caixa **nome** , digite `Block malware`.</span><span class="sxs-lookup"><span data-stu-id="b21ff-148">In the **Name** box, type `Block malware`.</span></span>

    - <span data-ttu-id="b21ff-149">Na seção resposta, escolha **Bloquear**.</span><span class="sxs-lookup"><span data-stu-id="b21ff-149">In the response section, choose **Block**.</span></span>

    - <span data-ttu-id="b21ff-150">Na seção **redirecionar anexo** , selecione a opção **habilitar**redirecionamento e, em seguida, especifique o endereço de email para o administrador ou operador de segurança da sua organização que examinará os arquivos detectados.</span><span class="sxs-lookup"><span data-stu-id="b21ff-150">In the **Redirect attachment** section, select the option **Enable redirect**, and then specify the email address for your organization's security administrator or operator who will review detected files.</span></span>

    - <span data-ttu-id="b21ff-151">Na seção **aplica-se** a, escolha **o domínio do destinatário**.</span><span class="sxs-lookup"><span data-stu-id="b21ff-151">In the **Applied to** section, choose **The recipient domain is**.</span></span> <span data-ttu-id="b21ff-152">Em seguida, selecione o seu domínio, escolha **Adicionar**e clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="b21ff-152">Then, select your domain, choose **Add**, and then click **OK**.</span></span>

5. <span data-ttu-id="b21ff-153">Clique em **Salvar**.</span><span class="sxs-lookup"><span data-stu-id="b21ff-153">Click **Save**.</span></span>

6. <span data-ttu-id="b21ff-154">(**Etapa adicional recomendada**) Como um administrador global ou um administrador do SharePoint Online, execute o cmdlet **[set-SPOTenant](https://docs.microsoft.com/powershell/module/sharepoint-online/Set-SPOTenant?view=sharepoint-ps)** com o parâmetro **DisallowInfectedFileDownload** definido como *true* para o seu ambiente do Office 365.</span><span class="sxs-lookup"><span data-stu-id="b21ff-154">(**Recommended additional step**) As a global administrator or a SharePoint Online administrator run the **[Set-SPOTenant](https://docs.microsoft.com/powershell/module/sharepoint-online/Set-SPOTenant?view=sharepoint-ps)** cmdlet with the **DisallowInfectedFileDownload** parameter set to  *true* for your Office 365 environment.</span></span> <span data-ttu-id="b21ff-155">(Isso impede que as pessoas abram, movam, copiem ou compartilhem arquivos detectados como mal-intencionados.)</span><span class="sxs-lookup"><span data-stu-id="b21ff-155">(This prevents people from opening, moving, copying, or sharing files that are detected as malicious.)</span></span>  

<span data-ttu-id="b21ff-156">Para saber mais, confira:</span><span class="sxs-lookup"><span data-stu-id="b21ff-156">To learn more, see:</span></span> 
- [<span data-ttu-id="b21ff-157">Configurar políticas de anexos seguros de ATP do Office 365</span><span class="sxs-lookup"><span data-stu-id="b21ff-157">Set up Office 365 ATP Safe Attachments policies</span></span>](set-up-atp-safe-attachments-policies.md)
- [<span data-ttu-id="b21ff-158">Ativar o Office 365 ATP para SharePoint, OneDrive e Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="b21ff-158">Turn on Office 365 ATP for SharePoint, OneDrive, and Microsoft Teams</span></span>](turn-on-atp-for-spo-odb-and-teams.md)

### <a name="atp-safe-links-policies"></a><span data-ttu-id="b21ff-159">Políticas de links seguros de ATP</span><span class="sxs-lookup"><span data-stu-id="b21ff-159">ATP Safe Links policies</span></span>

<span data-ttu-id="b21ff-160">Para configurar [links de ATP seguros](atp-safe-links.md), revise e edite sua política padrão e adicione uma política para usuários específicos.</span><span class="sxs-lookup"><span data-stu-id="b21ff-160">To set up [ATP Safe Links](atp-safe-links.md), review and edit your default policy, and add a policy for specific users.</span></span>

1. <span data-ttu-id="b21ff-161">No [centro de conformidade do & de segurança](https://protection.office.com), escolha links de segurança**ATP**da**política** > de **Gerenciamento** > de ameaças.</span><span class="sxs-lookup"><span data-stu-id="b21ff-161">In the [Security & Compliance Center](https://protection.office.com), choose **Threat management** > **Policy** > **ATP Safe Links**.</span></span>

2. <span data-ttu-id="b21ff-162">Clique duas vezes na política **padrão** .</span><span class="sxs-lookup"><span data-stu-id="b21ff-162">Double-click the **Default** policy.</span></span>

3. <span data-ttu-id="b21ff-163">Na seção **usar links seguros em** , selecione a opção **Office 365 ProPlus, Office para IOS e Android**e clique em **salvar**.</span><span class="sxs-lookup"><span data-stu-id="b21ff-163">In the **Use safe links in** section, select the option **Office 365 ProPlus, Office for iOS and Android**, and then click **Save**.</span></span>

4. <span data-ttu-id="b21ff-164">Na seção **políticas que se aplicam a destinatários específicos** , clique no sinal de**+** mais ().</span><span class="sxs-lookup"><span data-stu-id="b21ff-164">In the **Policies that apply to specific recipients** section, click the plus sign (**+**).</span></span>

5. <span data-ttu-id="b21ff-165">Especifique as seguintes configurações:</span><span class="sxs-lookup"><span data-stu-id="b21ff-165">Specify the following settings:</span></span>

    - <span data-ttu-id="b21ff-166">Na caixa **nome** , digite um nome, como `Safe Links`.</span><span class="sxs-lookup"><span data-stu-id="b21ff-166">In the **Name** box, type a name, such as `Safe Links`.</span></span>

    - <span data-ttu-id="b21ff-167">Na seção **Selecionar ação** , escolha **ativado**.</span><span class="sxs-lookup"><span data-stu-id="b21ff-167">In the **Select the action** section, choose **On**.</span></span>

    - <span data-ttu-id="b21ff-168">Selecione estas opções:</span><span class="sxs-lookup"><span data-stu-id="b21ff-168">Select these options:</span></span>

        - <span data-ttu-id="b21ff-169">**Usar anexos seguros para examinar Conteúdo baixável**</span><span class="sxs-lookup"><span data-stu-id="b21ff-169">**Use safe attachments to scan downloadable content**</span></span> 

        - <span data-ttu-id="b21ff-170">**Aplicar links seguros a mensagens de email enviadas dentro da organização**</span><span class="sxs-lookup"><span data-stu-id="b21ff-170">**Apply safe links to email messages sent within the organization**</span></span>

        - <span data-ttu-id="b21ff-171">**Não permitir que os usuários cliquem por meio de links seguros para a URL original**</span><span class="sxs-lookup"><span data-stu-id="b21ff-171">**Do not let users click through safe links to original URL**</span></span>

    - <span data-ttu-id="b21ff-172">Na seção **aplica-se** a, escolha **o domínio do destinatário**.</span><span class="sxs-lookup"><span data-stu-id="b21ff-172">In the **Applied to** section, choose **The recipient domain is**.</span></span> <span data-ttu-id="b21ff-173">Em seguida, selecione o seu domínio, escolha **Adicionar**e clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="b21ff-173">Then, select your domain, choose **Add**, and then click **OK**.</span></span>

6. <span data-ttu-id="b21ff-174">Clique em **Salvar**.</span><span class="sxs-lookup"><span data-stu-id="b21ff-174">Click **Save**.</span></span>

<span data-ttu-id="b21ff-175">Para saber mais, confira [configurar as políticas de links seguros de ATP do Office 365](set-up-atp-safe-links-policies.md).</span><span class="sxs-lookup"><span data-stu-id="b21ff-175">To learn more, see [Set up Office 365 ATP Safe Links policies](set-up-atp-safe-links-policies.md).</span></span> 

## <a name="part-3---anti-phishing"></a><span data-ttu-id="b21ff-176">Parte 3-anti-phishing</span><span class="sxs-lookup"><span data-stu-id="b21ff-176">Part 3 - Anti-phishing</span></span> 

<span data-ttu-id="b21ff-177">A [proteção contra phishing](anti-phishing-protection.md) está disponível em assinaturas que incluem [EOP](https://docs.microsoft.com/office365/servicedescriptions/exchange-online-protection-service-description).</span><span class="sxs-lookup"><span data-stu-id="b21ff-177">[Anti-phishing protection](anti-phishing-protection.md) is available in subscriptions that include [EOP](https://docs.microsoft.com/office365/servicedescriptions/exchange-online-protection-service-description).</span></span> <span data-ttu-id="b21ff-178">A proteção contra phishing avançada está disponível na [ATP](https://docs.microsoft.com/office365/servicedescriptions/office-365-advanced-threat-protection-service-description).</span><span class="sxs-lookup"><span data-stu-id="b21ff-178">Advanced anti-phishing protection is available in [ATP](https://docs.microsoft.com/office365/servicedescriptions/office-365-advanced-threat-protection-service-description).</span></span> <span data-ttu-id="b21ff-179">O procedimento a seguir descreve como configurar uma política anti-phishing do ATP.</span><span class="sxs-lookup"><span data-stu-id="b21ff-179">The following procedure describes how to configure an ATP anti-phishing policy.</span></span> <span data-ttu-id="b21ff-180">As etapas são semelhantes à configuração de uma política anti-phishing (sem ATP).</span><span class="sxs-lookup"><span data-stu-id="b21ff-180">The steps are similar for configuring an anti-phishing policy (without ATP).</span></span>

1. <span data-ttu-id="b21ff-181">No [centro de conformidade do & de segurança](https://protection.office.com), escolha**anti-phishing**da**política** > de **Gerenciamento** > de ameaças.</span><span class="sxs-lookup"><span data-stu-id="b21ff-181">In the [Security & Compliance Center](https://protection.office.com), choose **Threat management** > **Policy** > **ATP anti-phishing**.</span></span>

2. <span data-ttu-id="b21ff-182">Clique em **política padrão**.</span><span class="sxs-lookup"><span data-stu-id="b21ff-182">Click **Default policy**.</span></span>

3. <span data-ttu-id="b21ff-183">Na seção **representação** , clique em **Editar**e especifique as seguintes configurações:</span><span class="sxs-lookup"><span data-stu-id="b21ff-183">In the **Impersonation** section, click **Edit**, and then specify the following settings:</span></span>

    -  <span data-ttu-id="b21ff-184">Na guia **Adicionar usuários para proteger** , ative a proteção.</span><span class="sxs-lookup"><span data-stu-id="b21ff-184">On the **Add users to protect** tab, turn protection on.</span></span> <span data-ttu-id="b21ff-185">Em seguida, adicione usuários, como os membros da diretoria da sua organização, seu CEO, CFO e outros líderes seniores.</span><span class="sxs-lookup"><span data-stu-id="b21ff-185">Then add users, such as your organization's board members, your CEO, CFO, and other senior leaders.</span></span> <span data-ttu-id="b21ff-186">(Você pode digitar um endereço de email individual ou clicar para exibir uma lista.)</span><span class="sxs-lookup"><span data-stu-id="b21ff-186">(You can type an individual email address, or click to display a list.)</span></span>

    - <span data-ttu-id="b21ff-187">Na guia **adicionar domínios para proteger** , ative **automaticamente os domínios que eu sou proprietário**.</span><span class="sxs-lookup"><span data-stu-id="b21ff-187">On the **Add domains to protect** tab, turn on **Automatically include the domains I own**.</span></span> <span data-ttu-id="b21ff-188">Se você tiver domínios personalizados, adicione-os também.</span><span class="sxs-lookup"><span data-stu-id="b21ff-188">If you have custom domains, add those as well.</span></span>

    - <span data-ttu-id="b21ff-189">Na guia **ações** , selecione **mover mensagem para as pastas de lixo eletrônico dos destinatários para o** usuário representado e o domínio representado e ative as dicas de segurança.</span><span class="sxs-lookup"><span data-stu-id="b21ff-189">On the **Actions** tab, select **Move message to the recipients' Junk Email folders** for both impersonated user and impersonated domain, and turn on safety tips.</span></span>

    - <span data-ttu-id="b21ff-190">Na guia **inteligência de caixa de correio** , verifique se a inteligência de caixa de correio está ativada.</span><span class="sxs-lookup"><span data-stu-id="b21ff-190">On the **Mailbox intelligence** tab, make sure mailbox intelligence is turned on.</span></span>

    - <span data-ttu-id="b21ff-191">Na guia **revise Your Settings** , depois de revisar as configurações, clique em **salvar**.</span><span class="sxs-lookup"><span data-stu-id="b21ff-191">On the **Review your settings** tab, after you have reviewed your settings, click **Save**.</span></span>

4. <span data-ttu-id="b21ff-192">Na seção **spoof** , clique em **Editar**e especifique as seguintes configurações:</span><span class="sxs-lookup"><span data-stu-id="b21ff-192">In the **Spoof** section, click **Edit**, and then specify the following settings:</span></span>

    - <span data-ttu-id="b21ff-193">Na guia **configurações de filtro** de falsificação, verifique se a proteção contra falsificação está ativada.</span><span class="sxs-lookup"><span data-stu-id="b21ff-193">On the **Spoofing filter settings** tab, make sure anti-spoofing protection is turned on.</span></span>

    - <span data-ttu-id="b21ff-194">Na guia **ações** , escolha mover mensagem para as pastas de lixo eletrônico dos destinatários.</span><span class="sxs-lookup"><span data-stu-id="b21ff-194">On the **Actions** tab, choose Move message to the recipients' Junk Email folders.</span></span>

    - <span data-ttu-id="b21ff-195">Na guia **revise Your Settings** , depois de revisar as configurações, clique em **salvar**.</span><span class="sxs-lookup"><span data-stu-id="b21ff-195">On the **Review your settings** tab, after you have reviewed your settings, click **Save**.</span></span> <span data-ttu-id="b21ff-196">Se não fizer alterações, clique em **Cancelar**.</span><span class="sxs-lookup"><span data-stu-id="b21ff-196">(If you didn't make any changes, click **Cancel**.)</span></span>

5. <span data-ttu-id="b21ff-197">Feche a página de configurações de política padrão.</span><span class="sxs-lookup"><span data-stu-id="b21ff-197">Close the default policy settings page.</span></span>

<span data-ttu-id="b21ff-198">Para saber mais sobre suas opções de política anti-phishing, consulte [set up anti-phishing Policies](set-up-anti-phishing-policies.md).</span><span class="sxs-lookup"><span data-stu-id="b21ff-198">To learn more about your anti-phishing policy options, see [Set up anti-phishing policies](set-up-anti-phishing-policies.md).</span></span>

## <a name="part-4---anti-spam"></a><span data-ttu-id="b21ff-199">Parte 4-antispam</span><span class="sxs-lookup"><span data-stu-id="b21ff-199">Part 4 - Anti-spam</span></span>

<span data-ttu-id="b21ff-200">A [proteção](anti-spam-protection.md) antispam está disponível em assinaturas que incluem [EOP](https://docs.microsoft.com/office365/servicedescriptions/exchange-online-protection-service-description).</span><span class="sxs-lookup"><span data-stu-id="b21ff-200">[Anti-spam protection](anti-spam-protection.md) is available in subscriptions that include [EOP](https://docs.microsoft.com/office365/servicedescriptions/exchange-online-protection-service-description).</span></span>

1. <span data-ttu-id="b21ff-201">No [centro de conformidade do & de segurança](https://protection.office.com), escolha**anti-spam**de**política** > de **Gerenciamento** > de ameaças.</span><span class="sxs-lookup"><span data-stu-id="b21ff-201">In the [Security & Compliance Center](https://protection.office.com), choose **Threat management** > **Policy** > **Anti-spam**.</span></span>

2. <span data-ttu-id="b21ff-202">Na guia **Personalizar** , ative **as configurações personalizadas** .</span><span class="sxs-lookup"><span data-stu-id="b21ff-202">On the **Custom** tab, turn **Custom settings** on.</span></span>

3. <span data-ttu-id="b21ff-203">Expanda **política de filtro de spam padrão**, clique em **Editar política**e especifique as seguintes configurações:</span><span class="sxs-lookup"><span data-stu-id="b21ff-203">Expand **Default spam filter policy**, click **Edit policy**, and then specify the following settings:</span></span>

    - <span data-ttu-id="b21ff-204">Na seção **ações de spam e em massa** , defina o limite para um valor de 5 ou 6.</span><span class="sxs-lookup"><span data-stu-id="b21ff-204">In the **Spam and bulk actions** section, set the threshold to a value of 5 or 6.</span></span>

    - <span data-ttu-id="b21ff-205">Na seção **permitir listas** , revise (e, se necessário, edite) seus remetentes e domínios permitidos.</span><span class="sxs-lookup"><span data-stu-id="b21ff-205">In the **Allow lists** section, review (and if necessary, edit) your allowed senders and domains.</span></span>

4. <span data-ttu-id="b21ff-206">Clique em **Salvar**.</span><span class="sxs-lookup"><span data-stu-id="b21ff-206">Click **Save**.</span></span>

<span data-ttu-id="b21ff-207">Para saber mais sobre suas opções de política antispam, consulte [Configure the anti-spam Policies](configure-the-anti-spam-policies.md).</span><span class="sxs-lookup"><span data-stu-id="b21ff-207">To learn more about your anti-spam policy options, see [Configure the anti-spam policies](configure-the-anti-spam-policies.md).</span></span>

## <a name="part-5---service-wide-settings"></a><span data-ttu-id="b21ff-208">Parte 5 – configurações de nível de serviço</span><span class="sxs-lookup"><span data-stu-id="b21ff-208">Part 5 - Service-wide settings</span></span>

### <a name="zero-hour-auto-purge"></a><span data-ttu-id="b21ff-209">Limpeza automática de zero horas</span><span class="sxs-lookup"><span data-stu-id="b21ff-209">Zero-hour auto purge</span></span>

<span data-ttu-id="b21ff-210">[Limpeza automática de zero horas](zero-hour-auto-purge.md) (ZAP) está disponível em assinaturas que incluem [EOP](https://docs.microsoft.com/office365/servicedescriptions/exchange-online-protection-service-description).</span><span class="sxs-lookup"><span data-stu-id="b21ff-210">[Zero-hour auto purge](zero-hour-auto-purge.md) (ZAP) is available in subscriptions that include [EOP](https://docs.microsoft.com/office365/servicedescriptions/exchange-online-protection-service-description).</span></span> <span data-ttu-id="b21ff-211">Essa proteção é ativada por padrão; no entanto, as seguintes condições devem ser atendidas para que a proteção entre em vigor:</span><span class="sxs-lookup"><span data-stu-id="b21ff-211">This protection is turned on by default; however, the following conditions must be met for protection to be in effect:</span></span>

- <span data-ttu-id="b21ff-212">As ações de spam são definidas para **mover mensagens para a pasta lixo eletrônico** em [políticas antispam](anti-spam-protection.md).</span><span class="sxs-lookup"><span data-stu-id="b21ff-212">Spam actions are set to **Move message to Junk Email folder** in [anti-spam policies](anti-spam-protection.md).</span></span>

- <span data-ttu-id="b21ff-213">Os usuários mantiveram suas [configurações de lixo eletrônico](ensure-that-spam-is-routed-to-each-user-s-junk-email-folder.md)padrão e não desativaram a proteção de lixo eletrônico.</span><span class="sxs-lookup"><span data-stu-id="b21ff-213">Users have kept their default [junk email settings](ensure-that-spam-is-routed-to-each-user-s-junk-email-folder.md), and have not turned off junk email protection.</span></span>

<span data-ttu-id="b21ff-214">Para saber mais, confira [exclusão automática de zero horas-proteção contra spam e malware](zero-hour-auto-purge.md).</span><span class="sxs-lookup"><span data-stu-id="b21ff-214">To learn more, see [Zero-hour auto purge - protection against spam and malware](zero-hour-auto-purge.md).</span></span>

### <a name="audit-logging"></a><span data-ttu-id="b21ff-215">Registro em log de auditoria</span><span class="sxs-lookup"><span data-stu-id="b21ff-215">Audit logging</span></span>

<span data-ttu-id="b21ff-216">O log de auditoria está disponível em assinaturas que incluem o [Exchange Online](https://docs.microsoft.com/office365/servicedescriptions/exchange-online-service-description).</span><span class="sxs-lookup"><span data-stu-id="b21ff-216">Audit logging is available in subscriptions that include [Exchange Online](https://docs.microsoft.com/office365/servicedescriptions/exchange-online-service-description).</span></span> <span data-ttu-id="b21ff-217">Para exibir dados em relatórios de proteção contra ameaças, como o [painel de segurança](security-dashboard.md), [relatórios de segurança de email](view-email-security-reports.md)e [Explorer](use-explorer-in-security-and-compliance.md), o log de auditoria deve estar ativado para sua organização.</span><span class="sxs-lookup"><span data-stu-id="b21ff-217">In order to view data in threat protection reports, such as the [Security Dashboard](security-dashboard.md), [email security reports](view-email-security-reports.md), and [Explorer](use-explorer-in-security-and-compliance.md), audit logging must be turned on for your organization.</span></span> <span data-ttu-id="b21ff-218">Para saber mais, confira [Ativar ou desativar a pesquisa de log de auditoria do Office 365](turn-audit-log-search-on-or-off.md).</span><span class="sxs-lookup"><span data-stu-id="b21ff-218">To learn more, see [Turn Office 365 audit log search on or off](turn-audit-log-search-on-or-off.md).</span></span>

## <a name="post-setup-tasks"></a><span data-ttu-id="b21ff-219">Tarefas pós-instalação</span><span class="sxs-lookup"><span data-stu-id="b21ff-219">Post-setup tasks</span></span>

### <a name="watch-for-new-features-and-service-updates"></a><span data-ttu-id="b21ff-220">Assista a novos recursos e atualizações de serviço</span><span class="sxs-lookup"><span data-stu-id="b21ff-220">Watch for new features and service updates</span></span>

- [<span data-ttu-id="b21ff-221">Configurar as opções de lançamento padrão ou direcionadas</span><span class="sxs-lookup"><span data-stu-id="b21ff-221">Set up the Standard or Targeted release options</span></span>](https://docs.microsoft.com/office365/admin/manage/release-options-in-office-365?view=o365-worldwide)

- [<span data-ttu-id="b21ff-222">Vá para o seu centro de mensagens para exibir comunicados de recursos</span><span class="sxs-lookup"><span data-stu-id="b21ff-222">Go to your Message center to view feature announcements</span></span>](https://docs.microsoft.com/office365/admin/manage/message-center?view=o365-worldwide) 

- [<span data-ttu-id="b21ff-223">Visite o Microsoft 365 Roadmap para ver o status dos novos recursos</span><span class="sxs-lookup"><span data-stu-id="b21ff-223">Visit the Microsoft 365 Roadmap to see status of new features</span></span>](https://www.microsoft.com/microsoft-365/roadmap?filters=&searchterms=advanced%2Cthreat%2Cprotection)

- [<span data-ttu-id="b21ff-224">Examinar as descrições de serviço do Office 365</span><span class="sxs-lookup"><span data-stu-id="b21ff-224">Review the Office 365 Service Descriptions</span></span>](https://docs.microsoft.com/office365/servicedescriptions/office-365-service-descriptions-technet-library)

### <a name="see-how-threat-protection-features-are-working-for-your-organization"></a><span data-ttu-id="b21ff-225">Veja como os recursos de proteção contra ameaças estão funcionando para sua organização</span><span class="sxs-lookup"><span data-stu-id="b21ff-225">See how threat protection features are working for your organization</span></span>

- [<span data-ttu-id="b21ff-226">Visite o painel de segurança</span><span class="sxs-lookup"><span data-stu-id="b21ff-226">Visit your security dashboard</span></span>](security-dashboard.md)

- <span data-ttu-id="b21ff-227">[Exibir os relatórios do Office 365 ATP](view-reports-for-atp.md), incluindo o [Explorer](use-explorer-in-security-and-compliance.md)</span><span class="sxs-lookup"><span data-stu-id="b21ff-227">[View the reports for Office 365 ATP](view-reports-for-atp.md), including [Explorer](use-explorer-in-security-and-compliance.md)</span></span>

- [<span data-ttu-id="b21ff-228">Exibir seus relatórios de segurança de email</span><span class="sxs-lookup"><span data-stu-id="b21ff-228">View your email security reports</span></span>](view-email-security-reports.md)

### <a name="periodically-review-and-revise-your-threat-protection-policies"></a><span data-ttu-id="b21ff-229">Revisar e revisar periodicamente suas políticas de proteção contra ameaças</span><span class="sxs-lookup"><span data-stu-id="b21ff-229">Periodically review and revise your threat protection policies</span></span>

- [<span data-ttu-id="b21ff-230">Revise sua pontuação segura</span><span class="sxs-lookup"><span data-stu-id="b21ff-230">Review your Secure Score</span></span>](microsoft-secure-score.md)

- [<span data-ttu-id="b21ff-231">Use seus relatórios inteligentes e insights no centro de &amp; conformidade de segurança</span><span class="sxs-lookup"><span data-stu-id="b21ff-231">Use your smart reports and insights in the Security &amp; Compliance Center</span></span>](reports-and-insights-in-security-and-compliance.md) 

- [<span data-ttu-id="b21ff-232">Mantenha os usuários em segurança com os recursos de investigação e resposta contra ameaças do Office 365</span><span class="sxs-lookup"><span data-stu-id="b21ff-232">Keep users safe with Office 365 threat investigation and response features</span></span>](keep-users-safe-with-office-365-ti.md) 
 