---
title: Proteção contra ameaças no Office 365
ms.author: tracyp
author: msfttracyp
manager: dansimp
audience: Admin
ms.topic: hub-page
ms.service: O365-seccomp
localization_priority: Normal
ms.date: 05/09/2019
search.appverid:
- MOE150
- MET150
ms.assetid: b10023f6-f30f-45d3-b3ad-b71aa4aa0d58
ms.collection:
- M365-security-compliance
description: Use este artigo como guia para configurar seus recursos de proteção contra ameaças agora.
ms.openlocfilehash: 950259bb11446c3b7f27606b69a44f07ad478e79
ms.sourcegitcommit: 32ecff689ae32c59a39b7633ca0f36a304e7516e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/09/2019
ms.locfileid: "35600517"
---
# <a name="protect-against-threats-in-office-365"></a><span data-ttu-id="8b5c8-103">Proteção contra ameaças no Office 365</span><span class="sxs-lookup"><span data-stu-id="8b5c8-103">Protect against threats in Office 365</span></span>

<span data-ttu-id="8b5c8-104">O Office 365 inclui vários recursos de proteção contra ameaças.</span><span class="sxs-lookup"><span data-stu-id="8b5c8-104">Office 365 includes a variety of threat protection features.</span></span> <span data-ttu-id="8b5c8-105">Este é um guia de início rápido que você pode usar como uma lista de verificação para garantir que seus recursos de proteção contra ameaças estejam configurados para sua organização.</span><span class="sxs-lookup"><span data-stu-id="8b5c8-105">Here's a quick-start guide you can use as a checklist to make sure your threat protection features are set up for your organization.</span></span> <span data-ttu-id="8b5c8-106">Se você é novo em recursos de proteção contra ameaças no Office 365, ou se não tem certeza de onde começar, use a seguinte orientação como ponto de partida.</span><span class="sxs-lookup"><span data-stu-id="8b5c8-106">If you're new to threat protection features in Office 365, or you're just not sure where to begin, use the following guidance as a starting point.</span></span> 

> [!IMPORTANT]
> <span data-ttu-id="8b5c8-107">**As configurações iniciais recomendadas são incluídas para cada tipo de política; no entanto, muitas opções estão disponíveis e você pode ajustar suas configurações para atender às necessidades específicas da sua organização**.</span><span class="sxs-lookup"><span data-stu-id="8b5c8-107">**Initial recommended settings are included for each kind of policy; however, many options are available, and you can adjust your settings to meet your specific organization's needs**.</span></span> <span data-ttu-id="8b5c8-108">Aguarde aproximadamente 30 minutos para que as políticas ou as alterações funcionem da mesma forma por meio do datacenter.</span><span class="sxs-lookup"><span data-stu-id="8b5c8-108">Allow approximately 30 minutes for your policies or changes to work their way through your datacenter.</span></span>

## <a name="requirements"></a><span data-ttu-id="8b5c8-109">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8b5c8-109">Requirements</span></span>

### <a name="subscriptions"></a><span data-ttu-id="8b5c8-110">Assinaturas</span><span class="sxs-lookup"><span data-stu-id="8b5c8-110">Subscriptions</span></span>

<span data-ttu-id="8b5c8-111">Os recursos de proteção contra ameaças estão incluídos em todas as assinaturas do Office 365; no entanto, algumas assinaturas incluem recursos mais avançados.</span><span class="sxs-lookup"><span data-stu-id="8b5c8-111">Threat protection features are included in all Office 365 subscriptions; however, some subscriptions include more advanced features.</span></span> <span data-ttu-id="8b5c8-112">A tabela a seguir lista os recursos de proteção incluídos neste artigo junto com os requisitos mínimos de assinatura.</span><span class="sxs-lookup"><span data-stu-id="8b5c8-112">The following table lists the protection features included in this article together with the minimum subscription requirements.</span></span><br/>

|<span data-ttu-id="8b5c8-113">Tipo de proteção</span><span class="sxs-lookup"><span data-stu-id="8b5c8-113">Protection type</span></span>  |<span data-ttu-id="8b5c8-114">Requisito de assinatura</span><span class="sxs-lookup"><span data-stu-id="8b5c8-114">Subscription requirement</span></span>  |
|---------|---------|
|<span data-ttu-id="8b5c8-115">Proteção antimalware</span><span class="sxs-lookup"><span data-stu-id="8b5c8-115">Anti-malware protection</span></span>    | <span data-ttu-id="8b5c8-116">[Proteção do Exchange Online](https://docs.microsoft.com/office365/servicedescriptions/exchange-online-protection-service-description) EOP</span><span class="sxs-lookup"><span data-stu-id="8b5c8-116">[Exchange Online Protection](https://docs.microsoft.com/office365/servicedescriptions/exchange-online-protection-service-description) (EOP)</span></span>        |
|<span data-ttu-id="8b5c8-117">Proteção contra URLs e arquivos mal-intencionados em emails e documentos do Office</span><span class="sxs-lookup"><span data-stu-id="8b5c8-117">Protection from malicious URLs and files in email and Office documents</span></span>    | <span data-ttu-id="8b5c8-118">[Proteção avançada contra ameaças do Office 365](https://docs.microsoft.com/office365/servicedescriptions/office-365-advanced-threat-protection-service-description) ATP</span><span class="sxs-lookup"><span data-stu-id="8b5c8-118">[Office 365 Advanced Threat Protection](https://docs.microsoft.com/office365/servicedescriptions/office-365-advanced-threat-protection-service-description) (ATP)</span></span>       |
|<span data-ttu-id="8b5c8-119">Proteção antiphishing</span><span class="sxs-lookup"><span data-stu-id="8b5c8-119">Anti-phishing protection</span></span>    | [<span data-ttu-id="8b5c8-120">EOP</span><span class="sxs-lookup"><span data-stu-id="8b5c8-120">EOP</span></span>](https://docs.microsoft.com/office365/servicedescriptions/exchange-online-protection-service-description)      |
|<span data-ttu-id="8b5c8-121">Proteção anti-phishing avançada</span><span class="sxs-lookup"><span data-stu-id="8b5c8-121">Advanced anti-phishing protection</span></span>    | [<span data-ttu-id="8b5c8-122">Office 365 ATP</span><span class="sxs-lookup"><span data-stu-id="8b5c8-122">Office 365 ATP</span></span>](https://docs.microsoft.com/office365/servicedescriptions/office-365-advanced-threat-protection-service-description)   |
|<span data-ttu-id="8b5c8-123">Proteção antispam</span><span class="sxs-lookup"><span data-stu-id="8b5c8-123">Anti-spam protection</span></span>     | [<span data-ttu-id="8b5c8-124">EOP</span><span class="sxs-lookup"><span data-stu-id="8b5c8-124">EOP</span></span>](https://docs.microsoft.com/office365/servicedescriptions/exchange-online-protection-service-description)       |
|<span data-ttu-id="8b5c8-125">Limpeza automática de zero horas (para email)</span><span class="sxs-lookup"><span data-stu-id="8b5c8-125">Zero-hour auto purge (for email)</span></span>    | [<span data-ttu-id="8b5c8-126">EOP</span><span class="sxs-lookup"><span data-stu-id="8b5c8-126">EOP</span></span>](https://docs.microsoft.com/office365/servicedescriptions/exchange-online-protection-service-description)        |
|<span data-ttu-id="8b5c8-127">Log de auditoria (usado para fins de relatório)</span><span class="sxs-lookup"><span data-stu-id="8b5c8-127">Audit logging (this is used for reporting purposes)</span></span>    | [<span data-ttu-id="8b5c8-128">Exchange Online</span><span class="sxs-lookup"><span data-stu-id="8b5c8-128">Exchange Online</span></span>](https://docs.microsoft.com/office365/servicedescriptions/exchange-online-service-description)        |

### <a name="roles-and-permissions"></a><span data-ttu-id="8b5c8-129">Funções e permissões</span><span class="sxs-lookup"><span data-stu-id="8b5c8-129">Roles and permissions</span></span>

<span data-ttu-id="8b5c8-130">Você deve receber uma função apropriada para configurar as políticas no [centro de conformidade & segurança](https://docs.microsoft.com/office365/servicedescriptions/office-365-platform-service-description/office-365-securitycompliance-center).</span><span class="sxs-lookup"><span data-stu-id="8b5c8-130">You must be assigned an appropriate role to configure policies in the [Security & Compliance Center](https://docs.microsoft.com/office365/servicedescriptions/office-365-platform-service-description/office-365-securitycompliance-center).</span></span> <span data-ttu-id="8b5c8-131">A tabela a seguir inclui alguns exemplos:</span><span class="sxs-lookup"><span data-stu-id="8b5c8-131">The following table includes some examples:</span></span> 

|<span data-ttu-id="8b5c8-132">Função ou grupo de função</span><span class="sxs-lookup"><span data-stu-id="8b5c8-132">Role or role group</span></span>  |<span data-ttu-id="8b5c8-133">Onde saber mais</span><span class="sxs-lookup"><span data-stu-id="8b5c8-133">Where to learn more</span></span>  |
|---------|---------|
|<span data-ttu-id="8b5c8-134">Administrador global do Office 365</span><span class="sxs-lookup"><span data-stu-id="8b5c8-134">Office 365 Global Administrator</span></span> |[<span data-ttu-id="8b5c8-135">Tudo sobre as funções de administrador do Office 365</span><span class="sxs-lookup"><span data-stu-id="8b5c8-135">About Office 365 admin roles</span></span>](https://docs.microsoft.com/office365/admin/add-users/about-admin-roles)|
|<span data-ttu-id="8b5c8-136">Administrador de segurança</span><span class="sxs-lookup"><span data-stu-id="8b5c8-136">Security Administrator</span></span> |[<span data-ttu-id="8b5c8-137">Permissões de função de administrador no Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="8b5c8-137">Administrator role permissions in Azure Active Directory</span></span>](https://docs.microsoft.com/en-us/azure/active-directory/users-groups-roles/directory-assign-admin-roles)|
|<span data-ttu-id="8b5c8-138">Gerenciamento da organização do Exchange Online</span><span class="sxs-lookup"><span data-stu-id="8b5c8-138">Exchange Online Organization Management</span></span> |[<span data-ttu-id="8b5c8-139">Permissões no Exchange Online</span><span class="sxs-lookup"><span data-stu-id="8b5c8-139">Permissions in Exchange Online</span></span>](https://docs.microsoft.com/en-us/exchange/permissions-exo/permissions-exo) <br><span data-ttu-id="8b5c8-140">e</span><span class="sxs-lookup"><span data-stu-id="8b5c8-140">and</span></span><br> [<span data-ttu-id="8b5c8-141">Exchange Online PowerShell</span><span class="sxs-lookup"><span data-stu-id="8b5c8-141">Exchange Online PowerShell</span></span>](https://docs.microsoft.com/powershell/exchange/exchange-online/exchange-online-powershell?view=exchange-ps)|

<span data-ttu-id="8b5c8-142">Para saber mais, confira [permissões no centro de conformidade &amp; de segurança do Office 365](permissions-in-the-security-and-compliance-center.md).</span><span class="sxs-lookup"><span data-stu-id="8b5c8-142">To learn more, see [Permissions in the Office 365 Security &amp; Compliance Center](permissions-in-the-security-and-compliance-center.md).</span></span>

## <a name="part-1---anti-malware-protection"></a><span data-ttu-id="8b5c8-143">Parte 1-proteção Antimalware</span><span class="sxs-lookup"><span data-stu-id="8b5c8-143">Part 1 - Anti-malware protection</span></span>

<span data-ttu-id="8b5c8-144">A [proteção Antimalware](anti-malware-protection.md) está disponível em assinaturas que incluem [EOP](https://docs.microsoft.com/office365/servicedescriptions/exchange-online-protection-service-description).</span><span class="sxs-lookup"><span data-stu-id="8b5c8-144">[Anti-malware protection](anti-malware-protection.md) is available in subscriptions that include [EOP](https://docs.microsoft.com/office365/servicedescriptions/exchange-online-protection-service-description).</span></span> 

1. <span data-ttu-id="8b5c8-145">No [centro de conformidade & segurança](https://protection.office.com), escolha**anti-malware**de**política** > de **Gerenciamento** > de ameaças.</span><span class="sxs-lookup"><span data-stu-id="8b5c8-145">In the [Security & Compliance Center](https://protection.office.com), choose **Threat management** > **Policy** > **Anti-malware**.</span></span>

2. <span data-ttu-id="8b5c8-146">Clique duas vezes na política **padrão** e, em seguida, escolha **configurações**.</span><span class="sxs-lookup"><span data-stu-id="8b5c8-146">Double-click the **Default** policy, and then choose **settings**.</span></span>

3. <span data-ttu-id="8b5c8-147">Especifique as seguintes configurações:</span><span class="sxs-lookup"><span data-stu-id="8b5c8-147">Specify the following settings:</span></span>

    - <span data-ttu-id="8b5c8-148">Na seção **resposta de detecção de malware** , mantenha a configuração padrão **no**.</span><span class="sxs-lookup"><span data-stu-id="8b5c8-148">In the **Malware Detection Response** section, keep the default setting of **No**.</span></span>

    - <span data-ttu-id="8b5c8-149">Na seção **filtro de tipos de anexo comuns** , escolha **ativado**.</span><span class="sxs-lookup"><span data-stu-id="8b5c8-149">In the **Common Attachment Types Filter** section, choose **On**.</span></span>

4. <span data-ttu-id="8b5c8-150">Clique em **Salvar**.</span><span class="sxs-lookup"><span data-stu-id="8b5c8-150">Click **Save**.</span></span>

<span data-ttu-id="8b5c8-151">Para saber mais sobre opções de política Antimalware, consulte [Configure anti-malware Policies](configure-anti-malware-policies.md).</span><span class="sxs-lookup"><span data-stu-id="8b5c8-151">To learn more about anti-malware policy options, see [Configure anti-malware policies](configure-anti-malware-policies.md).</span></span>

## <a name="part-2---protection-from-malicious-urls-and-files"></a><span data-ttu-id="8b5c8-152">Parte 2: proteção contra arquivos e URLs maliciosos</span><span class="sxs-lookup"><span data-stu-id="8b5c8-152">Part 2 - Protection from malicious URLs and files</span></span>

<span data-ttu-id="8b5c8-153">A proteção de horário de clique de URLs e arquivos mal-intencionados está disponível em assinaturas que incluem o [Office 365 ATP](https://docs.microsoft.com/office365/servicedescriptions/office-365-advanced-threat-protection-service-description) (ATP) e é configurada por meio de [anexos seguros de ATP](atp-safe-attachments.md) e políticas de [links seguros de ATP](atp-safe-links.md) .</span><span class="sxs-lookup"><span data-stu-id="8b5c8-153">Time-of-click protection from malicious URLs and files is available in subscriptions that include [Office 365 ATP](https://docs.microsoft.com/office365/servicedescriptions/office-365-advanced-threat-protection-service-description) (ATP), and is set up through [ATP Safe Attachments](atp-safe-attachments.md) and [ATP Safe Links](atp-safe-links.md) policies.</span></span>

### <a name="atp-safe-attachments-policies"></a><span data-ttu-id="8b5c8-154">Políticas de anexos seguros de ATP</span><span class="sxs-lookup"><span data-stu-id="8b5c8-154">ATP Safe Attachments policies</span></span>

<span data-ttu-id="8b5c8-155">Para configurar [anexos de segurança ATP](atp-safe-attachments.md), você deve definir pelo menos uma política de anexos seguros de ATP.</span><span class="sxs-lookup"><span data-stu-id="8b5c8-155">To set up [ATP Safe Attachments](atp-safe-attachments.md), you must define at least one ATP Safe Attachments policy.</span></span> 

1. <span data-ttu-id="8b5c8-156">No [centro de conformidade & segurança](https://protection.office.com), escolha a**política** > de **Gerenciamento** > de ameaça**anexos seguros de ATP**.</span><span class="sxs-lookup"><span data-stu-id="8b5c8-156">In the [Security & Compliance Center](https://protection.office.com), choose **Threat management** > **Policy** > **ATP safe attachments**.</span></span>

2. <span data-ttu-id="8b5c8-157">Selecione a opção **ativar a ATP para SharePoint, onedrive e Microsoft Teams**.</span><span class="sxs-lookup"><span data-stu-id="8b5c8-157">Select the option **Turn on ATP for SharePoint, OneDrive, and Microsoft Teams**.</span></span>

3. <span data-ttu-id="8b5c8-158">Na seção **proteger anexos de email** , clique no sinal de mais**+**().</span><span class="sxs-lookup"><span data-stu-id="8b5c8-158">In the **Protect email attachments** section, click the plus sign (**+**).</span></span>

4. <span data-ttu-id="8b5c8-159">Especifique as seguintes configurações:</span><span class="sxs-lookup"><span data-stu-id="8b5c8-159">Specify the following settings:</span></span>

    - <span data-ttu-id="8b5c8-160">Na caixa **nome** , digite `Block malware`.</span><span class="sxs-lookup"><span data-stu-id="8b5c8-160">In the **Name** box, type `Block malware`.</span></span>

    - <span data-ttu-id="8b5c8-161">Na seção resposta, escolha **Bloquear**.</span><span class="sxs-lookup"><span data-stu-id="8b5c8-161">In the response section, choose **Block**.</span></span>

    - <span data-ttu-id="8b5c8-162">Na seção **redirecionar anexo** , selecione a opção **habilitar**redirecionamento e, em seguida, especifique o endereço de email para o administrador ou operador de segurança da sua organização que examinará os arquivos detectados.</span><span class="sxs-lookup"><span data-stu-id="8b5c8-162">In the **Redirect attachment** section, select the option **Enable redirect**, and then specify the email address for your organization's security administrator or operator who will review detected files.</span></span>

    - <span data-ttu-id="8b5c8-163">Na seção **aplica-se** a, escolha **o domínio do destinatário**.</span><span class="sxs-lookup"><span data-stu-id="8b5c8-163">In the **Applied to** section, choose **The recipient domain is**.</span></span> <span data-ttu-id="8b5c8-164">Em seguida, selecione o seu domínio, escolha **Adicionar**e clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="8b5c8-164">Then, select your domain, choose **Add**, and then click **OK**.</span></span>

5. <span data-ttu-id="8b5c8-165">Clique em **Salvar**.</span><span class="sxs-lookup"><span data-stu-id="8b5c8-165">Click **Save**.</span></span>

6. <span data-ttu-id="8b5c8-166">(**Etapa adicional recomendada**) Como um administrador global ou um administrador do SharePoint Online, execute o cmdlet **[set-SPOTenant](https://docs.microsoft.com/powershell/module/sharepoint-online/Set-SPOTenant?view=sharepoint-ps)** com o parâmetro **DisallowInfectedFileDownload** definido como *true* para o seu ambiente do Office 365.</span><span class="sxs-lookup"><span data-stu-id="8b5c8-166">(**Recommended additional step**) As a global administrator or a SharePoint Online administrator run the **[Set-SPOTenant](https://docs.microsoft.com/powershell/module/sharepoint-online/Set-SPOTenant?view=sharepoint-ps)** cmdlet with the **DisallowInfectedFileDownload** parameter set to  *true* for your Office 365 environment.</span></span> <span data-ttu-id="8b5c8-167">(Isso impede que as pessoas abram, movam, copiem ou compartilhem arquivos detectados como mal-intencionados.)</span><span class="sxs-lookup"><span data-stu-id="8b5c8-167">(This prevents people from opening, moving, copying, or sharing files that are detected as malicious.)</span></span>  

<span data-ttu-id="8b5c8-168">Para saber mais, confira [configurar as políticas de anexos seguros do Microsoft office 365 ATP](set-up-atp-safe-attachments-policies.md) e [ativar o Office 365 ATP para SharePoint, onedrive e Microsoft Teams](turn-on-atp-for-spo-odb-and-teams.md).</span><span class="sxs-lookup"><span data-stu-id="8b5c8-168">To learn more, see [Set up Office 365 ATP Safe Attachments policies](set-up-atp-safe-attachments-policies.md) and [Turn on Office 365 ATP for SharePoint, OneDrive, and Microsoft Teams](turn-on-atp-for-spo-odb-and-teams.md).</span></span>

### <a name="atp-safe-links-policies"></a><span data-ttu-id="8b5c8-169">Políticas de links seguros de ATP</span><span class="sxs-lookup"><span data-stu-id="8b5c8-169">ATP Safe Links policies</span></span>

<span data-ttu-id="8b5c8-170">Para configurar [links de ATP seguros](atp-safe-links.md), revise e edite sua política padrão e adicione uma política para usuários específicos.</span><span class="sxs-lookup"><span data-stu-id="8b5c8-170">To set up [ATP Safe Links](atp-safe-links.md), review and edit your default policy, and add a policy for specific users.</span></span>

1. <span data-ttu-id="8b5c8-171">No [centro de conformidade & segurança](https://protection.office.com), escolha \*\*\*\* > **política** > de gerenciamento de ameaça**links seguros de ATP**.</span><span class="sxs-lookup"><span data-stu-id="8b5c8-171">In the [Security & Compliance Center](https://protection.office.com), choose **Threat management** > **Policy** > **ATP Safe Links**.</span></span>

2. <span data-ttu-id="8b5c8-172">Clique duas vezes na política **padrão** .</span><span class="sxs-lookup"><span data-stu-id="8b5c8-172">Double-click the **Default** policy.</span></span>

3. <span data-ttu-id="8b5c8-173">Na seção **usar links seguros em** , selecione a opção **Office 365 ProPlus, Office para IOS e Android**e clique em **salvar**.</span><span class="sxs-lookup"><span data-stu-id="8b5c8-173">In the **Use safe links in** section, select the option **Office 365 ProPlus, Office for iOS and Android**, and then click **Save**.</span></span>

4. <span data-ttu-id="8b5c8-174">Na seção **políticas que se aplicam a destinatários específicos** , clique no sinal de**+** mais ().</span><span class="sxs-lookup"><span data-stu-id="8b5c8-174">In the **Policies that apply to specific recipients** section, click the plus sign (**+**).</span></span>

5. <span data-ttu-id="8b5c8-175">Especifique as seguintes configurações:</span><span class="sxs-lookup"><span data-stu-id="8b5c8-175">Specify the following settings:</span></span>

    - <span data-ttu-id="8b5c8-176">Na caixa **nome** , digite um nome, como `Safe Links`.</span><span class="sxs-lookup"><span data-stu-id="8b5c8-176">In the **Name** box, type a name, such as `Safe Links`.</span></span>

    - <span data-ttu-id="8b5c8-177">Na seção **Selecionar ação** , escolha **ativado**.</span><span class="sxs-lookup"><span data-stu-id="8b5c8-177">In the **Select the action** section, choose **On**.</span></span>

    - <span data-ttu-id="8b5c8-178">Selecione estas opções:</span><span class="sxs-lookup"><span data-stu-id="8b5c8-178">Select these options:</span></span>

        - <span data-ttu-id="8b5c8-179">**Usar anexos seguros para examinar Conteúdo baixável**</span><span class="sxs-lookup"><span data-stu-id="8b5c8-179">**Use safe attachments to scan downloadable content**</span></span> 

        - <span data-ttu-id="8b5c8-180">**Aplicar links seguros a mensagens de email enviadas dentro da organização**</span><span class="sxs-lookup"><span data-stu-id="8b5c8-180">**Apply safe links to email messages sent within the organization**</span></span>

        - <span data-ttu-id="8b5c8-181">**Não permitir que os usuários cliquem por meio de links seguros para a URL original**</span><span class="sxs-lookup"><span data-stu-id="8b5c8-181">**Do not let users click through safe links to original URL**</span></span>

    - <span data-ttu-id="8b5c8-182">Na seção **aplica-se** a, escolha **o domínio do destinatário**.</span><span class="sxs-lookup"><span data-stu-id="8b5c8-182">In the **Applied to** section, choose **The recipient domain is**.</span></span> <span data-ttu-id="8b5c8-183">Em seguida, selecione o seu domínio, escolha **Adicionar**e clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="8b5c8-183">Then, select your domain, choose **Add**, and then click **OK**.</span></span>

6. <span data-ttu-id="8b5c8-184">Clique em **Salvar**.</span><span class="sxs-lookup"><span data-stu-id="8b5c8-184">Click **Save**.</span></span>

<span data-ttu-id="8b5c8-185">Para saber mais, confira [configurar as políticas de links seguros de ATP do Office 365](set-up-atp-safe-links-policies.md).</span><span class="sxs-lookup"><span data-stu-id="8b5c8-185">To learn more, see [Set up Office 365 ATP Safe Links policies](set-up-atp-safe-links-policies.md).</span></span> 

## <a name="part-3---anti-phishing-protection"></a><span data-ttu-id="8b5c8-186">Parte 3-proteção contra phishing</span><span class="sxs-lookup"><span data-stu-id="8b5c8-186">Part 3 - Anti-phishing protection</span></span>

<span data-ttu-id="8b5c8-187">A [proteção contra phishing](anti-phishing-protection.md) está disponível em assinaturas que incluem [EOP](https://docs.microsoft.com/office365/servicedescriptions/exchange-online-protection-service-description).</span><span class="sxs-lookup"><span data-stu-id="8b5c8-187">[Anti-phishing protection](anti-phishing-protection.md) is available in subscriptions that include [EOP](https://docs.microsoft.com/office365/servicedescriptions/exchange-online-protection-service-description).</span></span> <span data-ttu-id="8b5c8-188">A proteção contra phishing avançada está disponível na [ATP](https://docs.microsoft.com/office365/servicedescriptions/office-365-advanced-threat-protection-service-description).</span><span class="sxs-lookup"><span data-stu-id="8b5c8-188">Advanced anti-phishing protection is available in [ATP](https://docs.microsoft.com/office365/servicedescriptions/office-365-advanced-threat-protection-service-description).</span></span> <span data-ttu-id="8b5c8-189">O procedimento a seguir descreve como configurar uma política anti-phishing do ATP.</span><span class="sxs-lookup"><span data-stu-id="8b5c8-189">The following procedure describes how to configure an ATP anti-phishing policy.</span></span> <span data-ttu-id="8b5c8-190">As etapas são semelhantes à configuração de uma política anti-phishing (sem ATP).</span><span class="sxs-lookup"><span data-stu-id="8b5c8-190">The steps are similar for configuring an anti-phishing policy (without ATP).</span></span>

1. <span data-ttu-id="8b5c8-191">No [centro de conformidade & segurança](https://protection.office.com), escolha**política** > de **Gerenciamento** > de ameaças**ATP anti-phishing**.</span><span class="sxs-lookup"><span data-stu-id="8b5c8-191">In the [Security & Compliance Center](https://protection.office.com), choose **Threat management** > **Policy** > **ATP anti-phishing**.</span></span>

2. <span data-ttu-id="8b5c8-192">Clique em **política padrão**.</span><span class="sxs-lookup"><span data-stu-id="8b5c8-192">Click **Default policy**.</span></span>

3. <span data-ttu-id="8b5c8-193">Na seção **representação** , clique em **Editar**e especifique as seguintes configurações:</span><span class="sxs-lookup"><span data-stu-id="8b5c8-193">In the **Impersonation** section, click **Edit**, and then specify the following settings:</span></span>

    - <span data-ttu-id="8b5c8-194">Na guia **Adicionar usuários para proteger** , ative a proteção.</span><span class="sxs-lookup"><span data-stu-id="8b5c8-194">On the **Add users to protect** tab, turn protection on.</span></span> <span data-ttu-id="8b5c8-195">Em seguida, adicione usuários, como os membros da diretoria da sua organização, seu CEO, CFO e outros líderes seniores.</span><span class="sxs-lookup"><span data-stu-id="8b5c8-195">Then add users, such as your organization's board members, your CEO, CFO, and other senior leaders.</span></span> <span data-ttu-id="8b5c8-196">(Você pode digitar um endereço de email individual ou clicar para exibir uma lista.)</span><span class="sxs-lookup"><span data-stu-id="8b5c8-196">(You can type an individual email address, or click to display a list.)</span></span>

    - <span data-ttu-id="8b5c8-197">Na guia **adicionar domínios para proteger** , ative **automaticamente os domínios que eu sou proprietário**.</span><span class="sxs-lookup"><span data-stu-id="8b5c8-197">On the **Add domains to protect** tab, turn on **Automatically include the domains I own**.</span></span> <span data-ttu-id="8b5c8-198">Se você tiver domínios personalizados, adicione-os também.</span><span class="sxs-lookup"><span data-stu-id="8b5c8-198">If you have custom domains, add those as well.</span></span>

    - <span data-ttu-id="8b5c8-199">Na guia **ações** , selecione **mover mensagem para as pastas de lixo eletrônico dos destinatários para o** usuário representado e o domínio representado e ative as dicas de segurança.</span><span class="sxs-lookup"><span data-stu-id="8b5c8-199">On the **Actions** tab, select **Move message to the recipients' Junk Email folders** for both impersonated user and impersonated domain, and turn on safety tips.</span></span>

    - <span data-ttu-id="8b5c8-200">Na guia **inteligência de caixa de correio** , verifique se a inteligência de caixa de correio está ativada.</span><span class="sxs-lookup"><span data-stu-id="8b5c8-200">On the **Mailbox intelligence** tab, make sure mailbox intelligence is turned on.</span></span>

    - <span data-ttu-id="8b5c8-201">Na guia **revise Your Settings** , depois de revisar as configurações, clique em **salvar**.</span><span class="sxs-lookup"><span data-stu-id="8b5c8-201">On the **Review your settings** tab, after you have reviewed your settings, click **Save**.</span></span>

4. <span data-ttu-id="8b5c8-202">Na seção **spoof** , clique em **Editar**e especifique as seguintes configurações:</span><span class="sxs-lookup"><span data-stu-id="8b5c8-202">In the **Spoof** section, click **Edit**, and then specify the following settings:</span></span>

    - <span data-ttu-id="8b5c8-203">Na guia **configurações de filtro** de falsificação, verifique se a proteção contra falsificação está ativada.</span><span class="sxs-lookup"><span data-stu-id="8b5c8-203">On the **Spoofing filter settings** tab, make sure anti-spoofing protection is turned on.</span></span>

    - <span data-ttu-id="8b5c8-204">Na guia **ações** , escolha mover mensagem para as pastas de lixo eletrônico dos destinatários.</span><span class="sxs-lookup"><span data-stu-id="8b5c8-204">On the **Actions** tab, choose Move message to the recipients' Junk Email folders.</span></span>

    - <span data-ttu-id="8b5c8-205">Na guia **revise Your Settings** , depois de revisar as configurações, clique em **salvar**.</span><span class="sxs-lookup"><span data-stu-id="8b5c8-205">On the **Review your settings** tab, after you have reviewed your settings, click **Save**.</span></span> <span data-ttu-id="8b5c8-206">Se não fizer alterações, clique em **Cancelar**.</span><span class="sxs-lookup"><span data-stu-id="8b5c8-206">(If you didn't make any changes, click **Cancel**.)</span></span>

5. <span data-ttu-id="8b5c8-207">Feche a página de configurações de política padrão.</span><span class="sxs-lookup"><span data-stu-id="8b5c8-207">Close the default policy settings page.</span></span>

<span data-ttu-id="8b5c8-208">Para saber mais sobre suas opções de política anti-phishing, consulte [set up anti-phishing Policies](set-up-anti-phishing-policies.md).</span><span class="sxs-lookup"><span data-stu-id="8b5c8-208">To learn more about your anti-phishing policy options, see [Set up anti-phishing policies](set-up-anti-phishing-policies.md).</span></span>

## <a name="part-4---anti-spam-protection"></a><span data-ttu-id="8b5c8-209">Parte 4-proteção antispam</span><span class="sxs-lookup"><span data-stu-id="8b5c8-209">Part 4 - Anti-spam protection</span></span>

<span data-ttu-id="8b5c8-210">A [proteção](anti-spam-protection.md) antispam está disponível em assinaturas que incluem [EOP](https://docs.microsoft.com/office365/servicedescriptions/exchange-online-protection-service-description).</span><span class="sxs-lookup"><span data-stu-id="8b5c8-210">[Anti-spam protection](anti-spam-protection.md) is available in subscriptions that include [EOP](https://docs.microsoft.com/office365/servicedescriptions/exchange-online-protection-service-description).</span></span>

1. <span data-ttu-id="8b5c8-211">No [centro de conformidade & segurança](https://protection.office.com), escolha**anti-spam**de**política** > de **Gerenciamento** > de ameaças.</span><span class="sxs-lookup"><span data-stu-id="8b5c8-211">In the [Security & Compliance Center](https://protection.office.com), choose **Threat management** > **Policy** > **Anti-spam**.</span></span>

2. <span data-ttu-id="8b5c8-212">Na guia **Personalizar** , ative **as configurações personalizadas** .</span><span class="sxs-lookup"><span data-stu-id="8b5c8-212">On the **Custom** tab, turn **Custom settings** on.</span></span>

3. <span data-ttu-id="8b5c8-213">Expanda **política de filtro de spam padrão**, clique em **Editar política**e especifique as seguintes configurações:</span><span class="sxs-lookup"><span data-stu-id="8b5c8-213">Expand **Default spam filter policy**, click **Edit policy**, and then specify the following settings:</span></span>

    - <span data-ttu-id="8b5c8-214">Na seção **ações de spam e em massa** , defina o limite para um valor de 5 ou 6.</span><span class="sxs-lookup"><span data-stu-id="8b5c8-214">In the **Spam and bulk actions** section, set the threshold to a value of 5 or 6.</span></span>

    - <span data-ttu-id="8b5c8-215">Na seção **permitir listas** , revise (e, se necessário, edite) seus remetentes e domínios permitidos.</span><span class="sxs-lookup"><span data-stu-id="8b5c8-215">In the **Allow lists** section, review (and if necessary, edit) your allowed senders and domains.</span></span>

4. <span data-ttu-id="8b5c8-216">Clique em **Salvar**.</span><span class="sxs-lookup"><span data-stu-id="8b5c8-216">Click **Save**.</span></span>

<span data-ttu-id="8b5c8-217">Para saber mais sobre suas opções de política antispam, consulte [Configure the anti-spam Policies](configure-the-anti-spam-policies.md).</span><span class="sxs-lookup"><span data-stu-id="8b5c8-217">To learn more about your anti-spam policy options, see [Configure the anti-spam policies](configure-the-anti-spam-policies.md).</span></span>

## <a name="part-5---additional-settings-to-configure"></a><span data-ttu-id="8b5c8-218">Parte 5-configurações adicionais a serem definidas</span><span class="sxs-lookup"><span data-stu-id="8b5c8-218">Part 5 - Additional settings to configure</span></span>

<span data-ttu-id="8b5c8-219">Além de configurar a proteção contra malware, URLs e arquivos mal-intencionados, phishing e spam, recomendamos que você defina as configurações de limpeza automática de zero horas e log de auditoria.</span><span class="sxs-lookup"><span data-stu-id="8b5c8-219">In addition to configuring protection from malware, malicious URLs and files, phishing, and spam, we recommend that you configure your zero-hour auto purge and audit logging settings.</span></span>

### <a name="zero-hour-auto-purge-for-email"></a><span data-ttu-id="8b5c8-220">Limpeza automática de zero horas para email</span><span class="sxs-lookup"><span data-stu-id="8b5c8-220">Zero-hour auto purge for email</span></span>

<span data-ttu-id="8b5c8-221">[Limpeza automática de zero horas](zero-hour-auto-purge.md) (ZAP) está disponível em assinaturas que incluem [EOP](https://docs.microsoft.com/office365/servicedescriptions/exchange-online-protection-service-description).</span><span class="sxs-lookup"><span data-stu-id="8b5c8-221">[Zero-hour auto purge](zero-hour-auto-purge.md) (ZAP) is available in subscriptions that include [EOP](https://docs.microsoft.com/office365/servicedescriptions/exchange-online-protection-service-description).</span></span> <span data-ttu-id="8b5c8-222">Essa proteção é ativada por padrão; no entanto, as seguintes condições devem ser atendidas para que a proteção entre em vigor:</span><span class="sxs-lookup"><span data-stu-id="8b5c8-222">This protection is turned on by default; however, the following conditions must be met for protection to be in effect:</span></span>

- <span data-ttu-id="8b5c8-223">As ações de spam são definidas para **mover mensagens para a pasta lixo eletrônico** em [políticas antispam](anti-spam-protection.md).</span><span class="sxs-lookup"><span data-stu-id="8b5c8-223">Spam actions are set to **Move message to Junk Email folder** in [anti-spam policies](anti-spam-protection.md).</span></span>

- <span data-ttu-id="8b5c8-224">Os usuários mantiveram suas [configurações de lixo eletrônico](ensure-that-spam-is-routed-to-each-user-s-junk-email-folder.md)padrão e não desativaram a proteção de lixo eletrônico.</span><span class="sxs-lookup"><span data-stu-id="8b5c8-224">Users have kept their default [junk email settings](ensure-that-spam-is-routed-to-each-user-s-junk-email-folder.md), and have not turned off junk email protection.</span></span>

<span data-ttu-id="8b5c8-225">Para saber mais, confira [exclusão automática de zero horas-proteção contra spam e malware](zero-hour-auto-purge.md).</span><span class="sxs-lookup"><span data-stu-id="8b5c8-225">To learn more, see [Zero-hour auto purge - protection against spam and malware](zero-hour-auto-purge.md).</span></span>

### <a name="audit-logging-for-reporting-and-investigation"></a><span data-ttu-id="8b5c8-226">Log de auditoria para relatórios e investigação</span><span class="sxs-lookup"><span data-stu-id="8b5c8-226">Audit logging for reporting and investigation</span></span>

<span data-ttu-id="8b5c8-227">O log de auditoria está disponível em assinaturas que incluem o [Exchange Online](https://docs.microsoft.com/office365/servicedescriptions/exchange-online-service-description).</span><span class="sxs-lookup"><span data-stu-id="8b5c8-227">Audit logging is available in subscriptions that include [Exchange Online](https://docs.microsoft.com/office365/servicedescriptions/exchange-online-service-description).</span></span> <span data-ttu-id="8b5c8-228">Para exibir dados em relatórios de proteção contra ameaças, como o [painel de segurança](security-dashboard.md), [relatórios de segurança de email](view-email-security-reports.md)e [Explorer](use-explorer-in-security-and-compliance.md), o log de auditoria deve estar ativado para sua organização.</span><span class="sxs-lookup"><span data-stu-id="8b5c8-228">In order to view data in threat protection reports, such as the [Security Dashboard](security-dashboard.md), [email security reports](view-email-security-reports.md), and [Explorer](use-explorer-in-security-and-compliance.md), audit logging must be turned on for your organization.</span></span> <span data-ttu-id="8b5c8-229">Para saber mais, confira [Ativar ou desativar a pesquisa de log de auditoria do Office 365](turn-audit-log-search-on-or-off.md).</span><span class="sxs-lookup"><span data-stu-id="8b5c8-229">To learn more, see [Turn Office 365 audit log search on or off](turn-audit-log-search-on-or-off.md).</span></span>

## <a name="post-setup-tasks"></a><span data-ttu-id="8b5c8-230">Tarefas pós-instalação</span><span class="sxs-lookup"><span data-stu-id="8b5c8-230">Post-setup tasks</span></span>

<span data-ttu-id="8b5c8-231">Depois de configurar seus recursos de proteção contra ameaças, não deixe de monitorar como esses recursos estão funcionando, revise e revise suas políticas conforme necessário e observe os novos recursos e atualizações de serviço.</span><span class="sxs-lookup"><span data-stu-id="8b5c8-231">After you have configured your threat protection features, make sure to monitor how those features are working, review and revise your policies as needed, and watch for new features and service updates.</span></span>

|<span data-ttu-id="8b5c8-232">O que fazer</span><span class="sxs-lookup"><span data-stu-id="8b5c8-232">What to do</span></span>  |<span data-ttu-id="8b5c8-233">Recursos para saber mais</span><span class="sxs-lookup"><span data-stu-id="8b5c8-233">Resources to learn more</span></span>  |
|---------|---------|
|<span data-ttu-id="8b5c8-234">Veja como os recursos de proteção contra ameaças estão trabalhando para sua organização exibindo relatórios</span><span class="sxs-lookup"><span data-stu-id="8b5c8-234">See how threat protection features are working for your organization by viewing reports</span></span>    |[<span data-ttu-id="8b5c8-235">Painel de segurança</span><span class="sxs-lookup"><span data-stu-id="8b5c8-235">Security dashboard</span></span>](security-dashboard.md)<br/>[<span data-ttu-id="8b5c8-236">Relatórios de segurança de email</span><span class="sxs-lookup"><span data-stu-id="8b5c8-236">Email security reports</span></span>](view-email-security-reports.md)<br/>[<span data-ttu-id="8b5c8-237">Relatórios para o Office 365 ATP</span><span class="sxs-lookup"><span data-stu-id="8b5c8-237">Reports for Office 365 ATP</span></span>](view-reports-for-atp.md)<br/>[<span data-ttu-id="8b5c8-238">Explorador de Ameaças</span><span class="sxs-lookup"><span data-stu-id="8b5c8-238">Threat Explorer</span></span>](use-explorer-in-security-and-compliance.md)    |
|<span data-ttu-id="8b5c8-239">Revisar e revisar periodicamente suas políticas de proteção contra ameaças, conforme necessário</span><span class="sxs-lookup"><span data-stu-id="8b5c8-239">Periodically review and revise your threat protection policies as needed</span></span>    |[<span data-ttu-id="8b5c8-240">Classificação de Segurança</span><span class="sxs-lookup"><span data-stu-id="8b5c8-240">Secure Score</span></span>](microsoft-secure-score.md)<br/>[<span data-ttu-id="8b5c8-241">Relatórios inteligentes e insights</span><span class="sxs-lookup"><span data-stu-id="8b5c8-241">Smart reports and insights</span></span>](reports-and-insights-in-security-and-compliance.md)<br/>[<span data-ttu-id="8b5c8-242">Investigação de ameaças e recursos de resposta do Office 365</span><span class="sxs-lookup"><span data-stu-id="8b5c8-242">Office 365 threat investigation and response features</span></span>](keep-users-safe-with-office-365-ti.md)          |
|<span data-ttu-id="8b5c8-243">Assista a novos recursos e atualizações de serviço</span><span class="sxs-lookup"><span data-stu-id="8b5c8-243">Watch for new features and service updates</span></span>     |[<span data-ttu-id="8b5c8-244">Opções de lançamento direcionado e padrão</span><span class="sxs-lookup"><span data-stu-id="8b5c8-244">Standard and Targeted release options</span></span>](https://docs.microsoft.com/office365/admin/manage/release-options-in-office-365?view=o365-worldwide)<br/>[<span data-ttu-id="8b5c8-245">Centro de Mensagens</span><span class="sxs-lookup"><span data-stu-id="8b5c8-245">Message Center</span></span>](https://docs.microsoft.com/office365/admin/manage/message-center?view=o365-worldwide)<br/>[<span data-ttu-id="8b5c8-246">Roteiro do Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="8b5c8-246">Microsoft 365 Roadmap</span></span>](https://www.microsoft.com/microsoft-365/roadmap?filters=&searchterms=advanced%2Cthreat%2Cprotection)<br/>[<span data-ttu-id="8b5c8-247">Descrições de serviço</span><span class="sxs-lookup"><span data-stu-id="8b5c8-247">Service Descriptions</span></span>](https://docs.microsoft.com/office365/servicedescriptions/office-365-service-descriptions-technet-library)         |
