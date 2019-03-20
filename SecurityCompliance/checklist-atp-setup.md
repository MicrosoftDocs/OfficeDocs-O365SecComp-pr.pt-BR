---
title: 'Início rápido: configurar a proteção avançada contra ameaças do Office 365'
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 03/19/2019
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.collection:
- M365-security-compliance
description: Aqui está um guia de início rápido que você pode usar para garantir que o Office 365 Advanced Threat Protection (ATP) esteja configurado e configurado para sua organização.
ms.openlocfilehash: 5aecbdb63f30a620812de44907b29dcae838ba36
ms.sourcegitcommit: 0f93b37c39d807dec91f118aa671a3430c47a9ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/20/2019
ms.locfileid: "30693290"
---
# <a name="quick-start-guide-set-up-office-365-advanced-threat-protection"></a><span data-ttu-id="ae587-103">Guia de início rápido: configurar a proteção avançada contra ameaças do Office 365</span><span class="sxs-lookup"><span data-stu-id="ae587-103">Quick Start Guide: Set up Office 365 Advanced Threat Protection</span></span>

<span data-ttu-id="ae587-104">Aqui está um guia de início rápido que você pode usar como uma lista de verificação para garantir que a proteção avançada contra ameaças do Office 365 (ATP) esteja configurada para sua organização.</span><span class="sxs-lookup"><span data-stu-id="ae587-104">Here's a quick-start guide you can use as a checklist to make sure Office 365 Advanced Threat Protection (ATP) is set up for your organization.</span></span> <span data-ttu-id="ae587-105">Se você for novo na proteção contra ameaças no Office 365, ou se não tiver certeza de onde começar, use a seguinte orientação como ponto de partida.</span><span class="sxs-lookup"><span data-stu-id="ae587-105">If you're new to threat protection in Office 365, or you're just not sure where to begin, use the following guidance as a starting point.</span></span> 

> [!IMPORTANT]
> <span data-ttu-id="ae587-106">**As configurações iniciais recomendadas são incluídas para cada tipo de política; no entanto, muitas opções estão disponíveis e você pode ajustar suas configurações para atender às necessidades específicas da sua organização**.</span><span class="sxs-lookup"><span data-stu-id="ae587-106">**Initial recommended settings are included for each kind of policy; however, many options are available, and you can adjust your settings to meet your specific organization's needs**.</span></span> <span data-ttu-id="ae587-107">Aguarde aproximadamente 30 minutos para que as políticas ou as alterações funcionem da mesma forma por meio do datacenter.</span><span class="sxs-lookup"><span data-stu-id="ae587-107">Allow approximately 30 minutes for your policies or changes to work their way through your datacenter.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="ae587-108">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="ae587-108">Prerequisites</span></span>

- <span data-ttu-id="ae587-109">Sua organização deve ter uma assinatura que inclua a [proteção avançada contra ameaças do Office 365](office-365-atp.md) (ATP).</span><span class="sxs-lookup"><span data-stu-id="ae587-109">Your organization must have a subscription that includes [Office 365 Advanced Threat Protection](office-365-atp.md) (ATP).</span></span>

- <span data-ttu-id="ae587-110">Você deve receber uma função apropriada para acessar os recursos de ATP.</span><span class="sxs-lookup"><span data-stu-id="ae587-110">You must be assigned an appropriate role to access ATP features.</span></span> <span data-ttu-id="ae587-111">A tabela a seguir inclui alguns exemplos:</span><span class="sxs-lookup"><span data-stu-id="ae587-111">The following table includes some examples:</span></span> 

    |<span data-ttu-id="ae587-112">Função ou grupo de função</span><span class="sxs-lookup"><span data-stu-id="ae587-112">Role or role group</span></span>  |<span data-ttu-id="ae587-113">Onde saber mais</span><span class="sxs-lookup"><span data-stu-id="ae587-113">Where to learn more</span></span>  |
    |---------|---------|
    |<span data-ttu-id="ae587-114">Administrador global do Office 365</span><span class="sxs-lookup"><span data-stu-id="ae587-114">Office 365 Global Administrator</span></span> |[<span data-ttu-id="ae587-115">Tudo sobre as funções de administrador do Office 365</span><span class="sxs-lookup"><span data-stu-id="ae587-115">About Office 365 admin roles</span></span>](https://docs.microsoft.com/office365/admin/add-users/about-admin-roles)|
    |<span data-ttu-id="ae587-116">Administrador de segurança</span><span class="sxs-lookup"><span data-stu-id="ae587-116">Security Administrator</span></span> |[<span data-ttu-id="ae587-117">Permissões de função de administrador no Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="ae587-117">Administrator role permissions in Azure Active Directory</span></span>](https://docs.microsoft.com/en-us/azure/active-directory/users-groups-roles/directory-assign-admin-roles)|
    |<span data-ttu-id="ae587-118">Gerenciamento da organização do Exchange Online</span><span class="sxs-lookup"><span data-stu-id="ae587-118">Exchange Online Organization Management</span></span> |[<span data-ttu-id="ae587-119">Permissões no Exchange Online</span><span class="sxs-lookup"><span data-stu-id="ae587-119">Permissions in Exchange Online</span></span>](https://docs.microsoft.com/en-us/exchange/permissions-exo/permissions-exo) <br><span data-ttu-id="ae587-120">and</span><span class="sxs-lookup"><span data-stu-id="ae587-120">and</span></span><br> [<span data-ttu-id="ae587-121">Exchange Online PowerShell</span><span class="sxs-lookup"><span data-stu-id="ae587-121">Exchange Online PowerShell</span></span>](https://docs.microsoft.com/powershell/exchange/exchange-online/exchange-online-powershell?view=exchange-ps)|

    <span data-ttu-id="ae587-122">(Consulte [permissões no centro de conformidade de &amp; segurança do Office 365](permissions-in-the-security-and-compliance-center.md).)</span><span class="sxs-lookup"><span data-stu-id="ae587-122">(See [Permissions in the Office 365 Security &amp; Compliance Center](permissions-in-the-security-and-compliance-center.md).)</span></span>

## <a name="part-1---anti-malware"></a><span data-ttu-id="ae587-123">Parte 1-anti-malware</span><span class="sxs-lookup"><span data-stu-id="ae587-123">Part 1 - Anti-malware</span></span>

1. <span data-ttu-id="ae587-124">no [centro de conformidade do & de segurança do Office 365](https://protection.office.com), escolha**Anti-malware**de**política** > de **gerenciamento** > de ameaças.</span><span class="sxs-lookup"><span data-stu-id="ae587-124">In the [Office 365 Security & Compliance Center](https://protection.office.com), choose **Threat management** > **Policy** > **Anti-malware**.</span></span>
2. <span data-ttu-id="ae587-125">Clique duas vezes na política **padrão** e, em seguida, escolha **configurações**.</span><span class="sxs-lookup"><span data-stu-id="ae587-125">Double-click the **Default** policy, and then choose **settings**.</span></span>
3. <span data-ttu-id="ae587-126">Especifique as seguintes configurações:</span><span class="sxs-lookup"><span data-stu-id="ae587-126">Specify the following settings:</span></span>
    - <span data-ttu-id="ae587-127">Na seção **resposta de detecção de malware** , mantenha a configuração padrão **no**.</span><span class="sxs-lookup"><span data-stu-id="ae587-127">In the **Malware Detection Response** section, keep the default setting of **No**.</span></span>
    - <span data-ttu-id="ae587-128">Na seção **filtro de tipos de anexo comuns** , escolha **ativado**.</span><span class="sxs-lookup"><span data-stu-id="ae587-128">In the **Common Attachment Types Filter** section, choose **On**.</span></span>
4. <span data-ttu-id="ae587-129">Clique em **Salvar**.</span><span class="sxs-lookup"><span data-stu-id="ae587-129">Click **Save**.</span></span>

<span data-ttu-id="ae587-130">Para saber mais sobre opções de política Antimalware, consulte [Configure anti-malware Policies](configure-anti-malware-policies.md).</span><span class="sxs-lookup"><span data-stu-id="ae587-130">To learn more about anti-malware policy options, see [Configure anti-malware policies](configure-anti-malware-policies.md).</span></span>

## <a name="part-2---zero-day-protection"></a><span data-ttu-id="ae587-131">Parte 2-proteção de dia zero</span><span class="sxs-lookup"><span data-stu-id="ae587-131">Part 2 - Zero-day protection</span></span>

<span data-ttu-id="ae587-132">A proteção de dia zero é configurada por meio de políticas, como links seguros de ATP e políticas de anexos seguros.</span><span class="sxs-lookup"><span data-stu-id="ae587-132">Zero-day protection is set up through policies, such as ATP Safe Links and Safe Attachments policies.</span></span>

### <a name="atp-safe-attachments-policies"></a><span data-ttu-id="ae587-133">Políticas de anexos seguros de ATP</span><span class="sxs-lookup"><span data-stu-id="ae587-133">ATP Safe Attachments policies</span></span>

1. <span data-ttu-id="ae587-134">no [centro de conformidade do Office 365 Security &](https://protection.office.com), escolha**política** > de **gerenciamento** > de ameaças de**anexos seguros de ATP**.</span><span class="sxs-lookup"><span data-stu-id="ae587-134">In the [Office 365 Security & Compliance Center](https://protection.office.com), choose **Threat management** > **Policy** > **ATP safe attachments**.</span></span>
2. <span data-ttu-id="ae587-135">Selecione a opção **ativar a ATP para SharePoint, onedrive e Microsoft Teams**.</span><span class="sxs-lookup"><span data-stu-id="ae587-135">Select the option **Turn on ATP for SharePoint, OneDrive, and Microsoft Teams**.</span></span>
3. <span data-ttu-id="ae587-136">Na seção **proteger anexos de email** , clique no sinal de mais**+**().</span><span class="sxs-lookup"><span data-stu-id="ae587-136">In the **Protect email attachments** section, click the plus sign (**+**).</span></span>
4. <span data-ttu-id="ae587-137">Especifique as seguintes configurações:</span><span class="sxs-lookup"><span data-stu-id="ae587-137">Specify the following settings:</span></span>
    - <span data-ttu-id="ae587-138">Na caixa **nome** , digite `Block malware`.</span><span class="sxs-lookup"><span data-stu-id="ae587-138">In the **Name** box, type `Block malware`.</span></span>
    - <span data-ttu-id="ae587-139">Na seção resposta, escolha **Bloquear**.</span><span class="sxs-lookup"><span data-stu-id="ae587-139">In the response section, choose **Block**.</span></span>
    - <span data-ttu-id="ae587-140">Na seção **redirecionar anexo** , selecione a opção **habilitar**redirecionamento e, em seguida, especifique o endereço de email para o administrador ou operador de segurança da sua organização que examinará os arquivos detectados.</span><span class="sxs-lookup"><span data-stu-id="ae587-140">In the **Redirect attachment** section, select the option **Enable redirect**, and then specify the email address for your organization's security administrator or operator who will review detected files.</span></span>
    - <span data-ttu-id="ae587-141">Na seção **aplica-se** a, escolha **o domínio do destinatário**.</span><span class="sxs-lookup"><span data-stu-id="ae587-141">In the **Applied to** section, choose **The recipient domain is**.</span></span> <span data-ttu-id="ae587-142">Em seguida, selecione o seu domínio, escolha **Adicionar**e clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="ae587-142">Then, select your domain, choose **Add**, and then click **OK**.</span></span>
5. <span data-ttu-id="ae587-143">Clique em **Salvar**.</span><span class="sxs-lookup"><span data-stu-id="ae587-143">Click **Save**.</span></span>
6. <span data-ttu-id="ae587-144">(Etapa adicional recomendada) Como um administrador global ou um administrador do SharePoint Online, execute o cmdlet **[set-SPOTenant](https://docs.microsoft.com/powershell/module/sharepoint-online/Set-SPOTenant?view=sharepoint-ps)** com o parâmetro **DisallowInfectedFileDownload** definido como *true* para o seu ambiente do Office 365.</span><span class="sxs-lookup"><span data-stu-id="ae587-144">(Recommended additional step) As a global administrator or a SharePoint Online administrator run the **[Set-SPOTenant](https://docs.microsoft.com/powershell/module/sharepoint-online/Set-SPOTenant?view=sharepoint-ps)** cmdlet with the **DisallowInfectedFileDownload** parameter set to  *true* for your Office 365 environment.</span></span> <span data-ttu-id="ae587-145">(Isso impede que as pessoas abram, movam, copiem ou compartilhem arquivos detectados como mal-intencionados.)</span><span class="sxs-lookup"><span data-stu-id="ae587-145">(This prevents people from opening, moving, copying, or sharing files that are detected as malicious.)</span></span>  

<span data-ttu-id="ae587-146">Para saber mais, confira [configurar as políticas de anexos seguros do Microsoft office 365 ATP](set-up-atp-safe-attachments-policies.md) e [ativar o Office 365 ATP para SharePoint, onedrive e Microsoft Teams](turn-on-atp-for-spo-odb-and-teams.md).</span><span class="sxs-lookup"><span data-stu-id="ae587-146">To learn more, see [Set up Office 365 ATP Safe Attachments policies](set-up-atp-safe-attachments-policies.md) and [Turn on Office 365 ATP for SharePoint, OneDrive, and Microsoft Teams](turn-on-atp-for-spo-odb-and-teams.md).</span></span>

### <a name="atp-safe-links-policies"></a><span data-ttu-id="ae587-147">Políticas de links seguros de ATP</span><span class="sxs-lookup"><span data-stu-id="ae587-147">ATP Safe Links policies</span></span>

<span data-ttu-id="ae587-148">Para configurar links de ATP seguros, revise a política padrão e adicione uma política.</span><span class="sxs-lookup"><span data-stu-id="ae587-148">To set up ATP Safe Links, review your default policy and add a policy.</span></span>

1. <span data-ttu-id="ae587-149">no [centro de conformidade do Office 365 Security &](https://protection.office.com), escolha**política** > de **gerenciamento** > de ameaça**Links seguros de ATP**.</span><span class="sxs-lookup"><span data-stu-id="ae587-149">In the [Office 365 Security & Compliance Center](https://protection.office.com), choose **Threat management** > **Policy** > **ATP Safe Links**.</span></span>
2. <span data-ttu-id="ae587-150">Clique duas vezes na política **padrão** .</span><span class="sxs-lookup"><span data-stu-id="ae587-150">Double-click the **Default** policy.</span></span>
3. <span data-ttu-id="ae587-151">Na seção **usar links seguros em** , selecione a opção **Office 365 ProPlus, Office para IOS e Android**e clique em **salvar**.</span><span class="sxs-lookup"><span data-stu-id="ae587-151">In the **Use safe links in** section, select the option **Office 365 ProPlus, Office for iOS and Android**, and then click **Save**.</span></span>
4. <span data-ttu-id="ae587-152">Na seção **políticas que se aplicam a destinatários específicos** , clique no sinal de**+** mais ().</span><span class="sxs-lookup"><span data-stu-id="ae587-152">In the **Policies that apply to specific recipients** section, click the plus sign (**+**).</span></span>
5. <span data-ttu-id="ae587-153">Especifique as seguintes configurações:</span><span class="sxs-lookup"><span data-stu-id="ae587-153">Specify the following settings:</span></span>
    - <span data-ttu-id="ae587-154">Na caixa **nome** , digite um nome, como `Safe Links`.</span><span class="sxs-lookup"><span data-stu-id="ae587-154">In the **Name** box, type a name, such as `Safe Links`.</span></span>
    - <span data-ttu-id="ae587-155">Na seção **Selecionar ação** , escolha **ativado**.</span><span class="sxs-lookup"><span data-stu-id="ae587-155">In the **Select the action** section, choose **On**.</span></span>
    - <span data-ttu-id="ae587-156">Selecione estas opções:</span><span class="sxs-lookup"><span data-stu-id="ae587-156">Select these options:</span></span>
        - <span data-ttu-id="ae587-157">**Usar anexos seguros para examinar Conteúdo baixável**</span><span class="sxs-lookup"><span data-stu-id="ae587-157">**Use safe attachments to scan downloadable content**</span></span> 
        - <span data-ttu-id="ae587-158">**Aplicar links seguros a mensagens de email enviadas dentro da organização**</span><span class="sxs-lookup"><span data-stu-id="ae587-158">**Apply safe links to email messages sent within the organization**</span></span>
        - <span data-ttu-id="ae587-159">**Não permitir que os usuários cliquem por meio de links seguros para a URL original**</span><span class="sxs-lookup"><span data-stu-id="ae587-159">**Do not let users click through safe links to original URL**</span></span>
    - <span data-ttu-id="ae587-160">Na seção **aplica-se** a, escolha **o domínio do destinatário**.</span><span class="sxs-lookup"><span data-stu-id="ae587-160">In the **Applied to** section, choose **The recipient domain is**.</span></span> <span data-ttu-id="ae587-161">Em seguida, selecione o seu domínio, escolha **Adicionar**e clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="ae587-161">Then, select your domain, choose **Add**, and then click **OK**.</span></span>
6. <span data-ttu-id="ae587-162">Clique em **Salvar**.</span><span class="sxs-lookup"><span data-stu-id="ae587-162">Click **Save**.</span></span>

<span data-ttu-id="ae587-163">Para saber mais, confira [configurar as políticas de links seguros de ATP do Office 365](set-up-atp-safe-links-policies.md).</span><span class="sxs-lookup"><span data-stu-id="ae587-163">To learn more, see [Set up Office 365 ATP Safe Links policies](set-up-atp-safe-links-policies.md).</span></span> 

## <a name="part-3---anti-phishing"></a><span data-ttu-id="ae587-164">Parte 3-anti-phishing</span><span class="sxs-lookup"><span data-stu-id="ae587-164">Part 3 - Anti-phishing</span></span> 

1. <span data-ttu-id="ae587-165">no [centro de conformidade do Office 365 Security &](https://protection.office.com), escolha**política** > de **gerenciamento** > de ameaças**ATP anti-phishing**.</span><span class="sxs-lookup"><span data-stu-id="ae587-165">In the [Office 365 Security & Compliance Center](https://protection.office.com), choose **Threat management** > **Policy** > **ATP anti-phishing**.</span></span>
2. <span data-ttu-id="ae587-166">Clique em **política padrão**.</span><span class="sxs-lookup"><span data-stu-id="ae587-166">Click **Default policy**.</span></span>
3. <span data-ttu-id="ae587-167">Na seção **representação** , clique em **Editar**e especifique as seguintes configurações:</span><span class="sxs-lookup"><span data-stu-id="ae587-167">In the **Impersonation** section, click **Edit**, and then specify the following settings:</span></span>
    -  <span data-ttu-id="ae587-168">Na guia **Adicionar usuários para proteger** , ative a proteção.</span><span class="sxs-lookup"><span data-stu-id="ae587-168">On the **Add users to protect** tab, turn protection on.</span></span> <span data-ttu-id="ae587-169">Em seguida, adicione usuários, como os membros da diretoria da sua organização, seu CEO, CFO e outros líderes seniores.</span><span class="sxs-lookup"><span data-stu-id="ae587-169">Then add users, such as your organization's board members, your CEO, CFO, and other senior leaders.</span></span> <span data-ttu-id="ae587-170">(Você pode digitar um endereço de email individual ou clicar para exibir uma lista.)</span><span class="sxs-lookup"><span data-stu-id="ae587-170">(You can type an individual email address, or click to display a list.)</span></span>
    - <span data-ttu-id="ae587-171">Na guia **adicionar domínios para proteger** , ative **automaticamente os domínios que eu sou proprietário**.</span><span class="sxs-lookup"><span data-stu-id="ae587-171">On the **Add domains to protect** tab, turn on **Automatically include the domains I own**.</span></span> <span data-ttu-id="ae587-172">Se você tiver domínios personalizados, adicione-os também.</span><span class="sxs-lookup"><span data-stu-id="ae587-172">If you have custom domains, add those as well.</span></span>
    - <span data-ttu-id="ae587-173">Na guia **ações** , selecione **mover mensagem para as pastas de lixo eletrônico dos destinatários para o** usuário representado e o domínio representado e ative as dicas de segurança.</span><span class="sxs-lookup"><span data-stu-id="ae587-173">On the **Actions** tab, select **Move message to the recipients' Junk Email folders** for both impersonated user and impersonated domain, and turn on safety tips.</span></span>
    - <span data-ttu-id="ae587-174">Na guia **inteligência de caixa de correio** , verifique se a inteligência de caixa de correio está ativada.</span><span class="sxs-lookup"><span data-stu-id="ae587-174">On the **Mailbox intelligence** tab, make sure mailbox intelligence is turned on.</span></span>
    - <span data-ttu-id="ae587-175">Na guia **revise Your Settings** , depois de revisar as configurações, clique em **salvar**.</span><span class="sxs-lookup"><span data-stu-id="ae587-175">On the **Review your settings** tab, after you have reviewed your settings, click **Save**.</span></span>
4. <span data-ttu-id="ae587-176">Na seção **spoof** , clique em **Editar**e especifique as seguintes configurações:</span><span class="sxs-lookup"><span data-stu-id="ae587-176">In the **Spoof** section, click **Edit**, and then specify the following settings:</span></span>
    - <span data-ttu-id="ae587-177">Na guia **configurações de filtro** de falsificação, verifique se a proteção contra falsificação está ativada.</span><span class="sxs-lookup"><span data-stu-id="ae587-177">On the **Spoofing filter settings** tab, make sure anti-spoofing protection is turned on.</span></span>
    - <span data-ttu-id="ae587-178">Na guia **ações** , escolha mover mensagem para as pastas de lixo eletrônico dos destinatários.</span><span class="sxs-lookup"><span data-stu-id="ae587-178">On the **Actions** tab, choose Move message to the recipients' Junk Email folders.</span></span>
    - <span data-ttu-id="ae587-179">Na guia **revise Your Settings** , depois de revisar as configurações, clique em **salvar**.</span><span class="sxs-lookup"><span data-stu-id="ae587-179">On the **Review your settings** tab, after you have reviewed your settings, click **Save**.</span></span> <span data-ttu-id="ae587-180">Se não fizer alterações, clique em **Cancelar**.</span><span class="sxs-lookup"><span data-stu-id="ae587-180">(If you didn't make any changes, click **Cancel**.)</span></span>
5. <span data-ttu-id="ae587-181">Feche a página de configurações de política padrão.</span><span class="sxs-lookup"><span data-stu-id="ae587-181">Close the default policy settings page.</span></span>

<span data-ttu-id="ae587-182">Para saber mais sobre suas opções de política anti-phishing, confira [Configurar políticas de anti-phishing e anti-phishing do Office 365 ATP](set-up-anti-phishing-policies.md).</span><span class="sxs-lookup"><span data-stu-id="ae587-182">To learn more about your anti-phishing policy options, see [Set up Office 365 ATP anti-phishing and anti-phishing policies](set-up-anti-phishing-policies.md).</span></span>

## <a name="part-4---anti-spam"></a><span data-ttu-id="ae587-183">Parte 4-antispam</span><span class="sxs-lookup"><span data-stu-id="ae587-183">Part 4 - Anti-spam</span></span>

1. <span data-ttu-id="ae587-184">no [centro de conformidade do & de segurança do Office 365](https://protection.office.com), escolha**Anti-spam**de**política** > de **gerenciamento** > de ameaças.</span><span class="sxs-lookup"><span data-stu-id="ae587-184">In the [Office 365 Security & Compliance Center](https://protection.office.com), choose **Threat management** > **Policy** > **Anti-spam**.</span></span>
2. <span data-ttu-id="ae587-185">Na guia **Personalizar** , ative **as configurações personalizadas** .</span><span class="sxs-lookup"><span data-stu-id="ae587-185">On the **Custom** tab, turn **Custom settings** on.</span></span>
3. <span data-ttu-id="ae587-186">Expanda **política de filtro de spam padrão**, clique em **Editar política**e especifique as seguintes configurações:</span><span class="sxs-lookup"><span data-stu-id="ae587-186">Expand **Default spam filter policy**, click **Edit policy**, and then specify the following settings:</span></span>
    - <span data-ttu-id="ae587-187">Na seção **ações de spam e em massa** , defina o limite para um valor de 5 ou 6.</span><span class="sxs-lookup"><span data-stu-id="ae587-187">In the **Spam and bulk actions** section, set the threshold to a value of 5 or 6.</span></span>
    - <span data-ttu-id="ae587-188">Na seção **permitir listas** , revise (e, se necessário, edite) seus remetentes e domínios permitidos.</span><span class="sxs-lookup"><span data-stu-id="ae587-188">In the **Allow lists** section, review (and if necessary, edit) your allowed senders and domains.</span></span>
4. <span data-ttu-id="ae587-189">Clique em **Salvar**.</span><span class="sxs-lookup"><span data-stu-id="ae587-189">Click **Save**.</span></span>

<span data-ttu-id="ae587-190">Para saber mais sobre suas opções de política antispam, consulte [Configure the anti-spam Policies](configure-the-anti-spam-policies.md).</span><span class="sxs-lookup"><span data-stu-id="ae587-190">To learn more about your anti-spam policy options, see [Configure the anti-spam policies](configure-the-anti-spam-policies.md).</span></span>

## <a name="part-5---service-wide-settings"></a><span data-ttu-id="ae587-191">Parte 5 – configurações de nível de serviço</span><span class="sxs-lookup"><span data-stu-id="ae587-191">Part 5 - Service-wide settings</span></span>

### <a name="zero-hour-auto-purge"></a><span data-ttu-id="ae587-192">Limpeza automática de zero horas</span><span class="sxs-lookup"><span data-stu-id="ae587-192">Zero-hour auto purge</span></span>

<span data-ttu-id="ae587-193">A limpeza automática de zero horas (ZAP) é ativada por padrão; no entanto, as seguintes condições devem ser atendidas:</span><span class="sxs-lookup"><span data-stu-id="ae587-193">Zero-hour auto purge (ZAP) is turned on by default; however, the following conditions must be met:</span></span>
- <span data-ttu-id="ae587-194">As ações de spam são definidas para **mover mensagens para a pasta lixo eletrônico** em políticas antispam.</span><span class="sxs-lookup"><span data-stu-id="ae587-194">Spam actions are set to **Move message to Junk Email folder** in anti-spam policies.</span></span>
- <span data-ttu-id="ae587-195">Os usuários mantiveram suas configurações de lixo eletrônico padrão e não desativaram a proteção de lixo eletrônico.</span><span class="sxs-lookup"><span data-stu-id="ae587-195">Users have kept their default junk email settings, and have not turned off junk email protection.</span></span>

<span data-ttu-id="ae587-196">Para saber mais, confira [exclusão automática de zero horas-proteção contra spam e malware](zero-hour-auto-purge.md).</span><span class="sxs-lookup"><span data-stu-id="ae587-196">To learn more, see [Zero-hour auto purge - protection against spam and malware](zero-hour-auto-purge.md).</span></span>

### <a name="audit-logging"></a><span data-ttu-id="ae587-197">Registro em log de auditoria</span><span class="sxs-lookup"><span data-stu-id="ae587-197">Audit logging</span></span>

<span data-ttu-id="ae587-198">Para exibir dados em relatórios de proteção contra ameaças, como o [painel de segurança](security-dashboard.md) e o [Explorer](use-explorer-in-security-and-compliance.md), o log de auditoria deve estar ativado para sua organização.</span><span class="sxs-lookup"><span data-stu-id="ae587-198">In order to view data in threat protection reports, such as the [Security Dashboard](security-dashboard.md) and [Explorer](use-explorer-in-security-and-compliance.md), audit logging must be turned on for your organization.</span></span>

<span data-ttu-id="ae587-199">Consulte [Ativar ou desativar a pesquisa de log de auditoria do Office 365](turn-audit-log-search-on-or-off.md).</span><span class="sxs-lookup"><span data-stu-id="ae587-199">See [Turn Office 365 audit log search on or off](turn-audit-log-search-on-or-off.md).</span></span>

## <a name="post-setup-tasks"></a><span data-ttu-id="ae587-200">Tarefas pós-instalação</span><span class="sxs-lookup"><span data-stu-id="ae587-200">Post-setup tasks</span></span>

### <a name="watch-for-new-features-and-service-updates"></a><span data-ttu-id="ae587-201">Assista a novos recursos e atualizações de serviço</span><span class="sxs-lookup"><span data-stu-id="ae587-201">Watch for new features and service updates</span></span>

- [<span data-ttu-id="ae587-202">Visite o mapa do Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="ae587-202">Visit the Microsoft 365 Roadmap</span></span>](https://www.microsoft.com/microsoft-365/roadmap?filters=&searchterms=advanced%2Cthreat%2Cprotection)

- [<span data-ttu-id="ae587-203">Consulte a descrição do serviço de proteção avançada contra ameaças do Office 365</span><span class="sxs-lookup"><span data-stu-id="ae587-203">See the Office 365 Advanced Threat Protection Service Description</span></span>](https://docs.microsoft.com/office365/servicedescriptions/office-365-advanced-threat-protection-service-description#whats-new-in-office-365-advanced-threat-protection-atp)

### <a name="see-how-atp-is-working-for-your-organization"></a><span data-ttu-id="ae587-204">Veja como a ATP está funcionando para sua organização</span><span class="sxs-lookup"><span data-stu-id="ae587-204">See how ATP is working for your organization</span></span>

- [<span data-ttu-id="ae587-205">Exibir relatórios para a proteção avançada contra ameaças do Office 365</span><span class="sxs-lookup"><span data-stu-id="ae587-205">View reports for Office 365 Advanced Threat Protection</span></span>](view-reports-for-atp.md)

- [<span data-ttu-id="ae587-206">Usar o Explorer no centro &amp; de conformidade de segurança</span><span class="sxs-lookup"><span data-stu-id="ae587-206">Use Explorer in the Security &amp; Compliance Center</span></span>](use-explorer-in-security-and-compliance.md)

### <a name="periodically-review-and-revise-your-atp-policies"></a><span data-ttu-id="ae587-207">Revisar e revisar periodicamente suas políticas ATP</span><span class="sxs-lookup"><span data-stu-id="ae587-207">Periodically review and revise your ATP policies</span></span>

- [<span data-ttu-id="ae587-208">Mantenha os usuários do Office 365 seguros com o Office 365 investigação de ameaças e resposta</span><span class="sxs-lookup"><span data-stu-id="ae587-208">Keep your Office 365 users safe with Office 365 threat investigation and response</span></span>](keep-users-safe-with-office-365-ti.md) 

- [<span data-ttu-id="ae587-209">Use os relatórios inteligentes e as ideias no centro de conformidade de segurança &amp; do Office 365</span><span class="sxs-lookup"><span data-stu-id="ae587-209">Use the smart reports and insights in the Office 365 Security &amp; Compliance Center</span></span>](reports-and-insights-in-security-and-compliance.md) 