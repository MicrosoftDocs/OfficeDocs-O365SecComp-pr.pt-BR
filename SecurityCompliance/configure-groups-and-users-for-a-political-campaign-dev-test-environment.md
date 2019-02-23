---
title: Defina grupos e usuários para um ambiente de desenvolvimento/teste de uma campanha política
ms.author: josephd
author: JoeDavies-MSFT
manager: laurawi
ms.date: 12/15/2017
ms.audience: ITPro
ms.topic: article
ms.collection:
- Ent_O365
- Strat_O365_Enterprise
ms.service: O365-seccomp
localization_priority: Priority
search.appverid:
- MET150
ms.assetid: 0e22bcf3-bad3-42a4-b44f-276e0cf4790f
description: 'Resumo: Crie assinaturas de teste do Office 365 e Enterprise Mobility + Security (EMS) com usuários e grupos para um ambiente de desenvolvimento/teste de campanha política.'
ms.openlocfilehash: 098ae2c3005e0c6ba7939c52260b1a2c49dc557e
ms.sourcegitcommit: a80bd8626720fabdf592b84e4424cd3a83d08280
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30223700"
---
# <a name="configure-groups-and-users-for-a-political-campaign-devtest-environment"></a><span data-ttu-id="20e2c-103">Defina grupos e usuários para um ambiente de desenvolvimento/teste de uma campanha política</span><span class="sxs-lookup"><span data-stu-id="20e2c-103">Configure groups and users for a political campaign dev/test environment</span></span>

 <span data-ttu-id="20e2c-104">**Resumo:** Crie assinaturas de teste do Office 365 e Enterprise Mobility + Security (EMS) com usuários e grupos para um ambiente de desenvolvimento/teste de campanha política.</span><span class="sxs-lookup"><span data-stu-id="20e2c-104">**Summary:** Create Office 365 and Enterprise Mobility + Security (EMS) trial subscriptions with users and groups for a political campaign dev/test environment.</span></span>
  
<span data-ttu-id="20e2c-105">Use as instruções deste artigo para criar um ambiente de desenvolvimento/de teste que inclui grupos e contas de usuário simplificadas para a solução [Diretrizes de segurança da Microsoft para campanhas políticas, instituições sem fins lucrativos e outras organizações Agile](microsoft-security-guidance-for-political-campaigns-nonprofits-and-other-agile-o.md).</span><span class="sxs-lookup"><span data-stu-id="20e2c-105">Use the instructions in this article to create a dev/test environment that includes simplified user accounts and groups for the [Microsoft Security Guidance for Political Campaigns, Nonprofits, and Other Agile Organizations](microsoft-security-guidance-for-political-campaigns-nonprofits-and-other-agile-o.md) solution.</span></span>
  
## <a name="phase-1-create-your-office-365-devtest-environment"></a><span data-ttu-id="20e2c-106">Fase 1: Criar seu ambiente de desenvolvimento/teste do Office 365</span><span class="sxs-lookup"><span data-stu-id="20e2c-106">Phase 1: Create your Office 365 dev/test environment</span></span>

<span data-ttu-id="20e2c-107">Nesta fase, você deve obter assinaturas de avaliação do Office 365 E5 e do Enterprise Mobility + Security (EMS) E5 para uma organização fictícia que representa uma campanha política.</span><span class="sxs-lookup"><span data-stu-id="20e2c-107">In this phase, you obtain trial subscriptions for Office 365 E5 and Enterprise Mobility + Security (EMS) E5 for a fictional organization that represents a political campaign.</span></span>
  
<span data-ttu-id="20e2c-108">Primeiro, siga as instruções na **Fase 2** do [ambiente de desenvolvimento/de teste do Office 365](https://docs.microsoft.com/office365/enterprise/office-365-dev-test-environment).</span><span class="sxs-lookup"><span data-stu-id="20e2c-108">First, follow the instructions in **Phase 2** of the [Office 365 dev/test environment](https://docs.microsoft.com/office365/enterprise/office-365-dev-test-environment).</span></span>
  
<span data-ttu-id="20e2c-109">Em seguida, inscreva-se para a assinatura de avaliação do EMS E5 e adicione-a à mesma organização de sua assinatura de avaliação do Office 365.</span><span class="sxs-lookup"><span data-stu-id="20e2c-109">Next, sign up for the EMS E5 trial subscription and add it to the same organization as your Office 365 trial subscription.</span></span>
  
1. <span data-ttu-id="20e2c-p101">Se necessário, entre no Portal do Office 365 com as credenciais da conta de administrador global da sua assinatura de avaliação. Para obter ajuda, consulte [Onde entrar no Office 365](https://support.office.com/Article/Where-to-sign-in-to-Office-365-e9eb7d51-5430-4929-91ab-6157c5a050b4).</span><span class="sxs-lookup"><span data-stu-id="20e2c-p101">If needed, sign in to the Office 365 portal with the credentials of the global administrator account of your trial subscription. For help, see [Where to sign in to Office 365](https://support.office.com/Article/Where-to-sign-in-to-Office-365-e9eb7d51-5430-4929-91ab-6157c5a050b4).</span></span>
    
2. <span data-ttu-id="20e2c-112">Clique no bloco de **Administração**.</span><span class="sxs-lookup"><span data-stu-id="20e2c-112">Click the **Admin** tile.</span></span>
    
3. <span data-ttu-id="20e2c-113">Na guia **Centro de Administração do Office** no navegador, no painel de navegação esquerdo, clique em **Cobrança > Comprar serviços**.</span><span class="sxs-lookup"><span data-stu-id="20e2c-113">On the **Office Admin center** tab in your browser, in the left navigation, click **Billing > Purchase services**.</span></span>
    
4. <span data-ttu-id="20e2c-p102">Na página **Comprar serviços**, encontre o item **Enterprise Mobility + Security E5**. Passe o ponteiro do mouse sobre ele e clique em **Iniciar avaliação gratuita**.</span><span class="sxs-lookup"><span data-stu-id="20e2c-p102">On the **Purchase services** page, find the **Enterprise Mobility + Security E5** item. Hover your mouse pointer over it and click **Start free trial**.</span></span>
    
5. <span data-ttu-id="20e2c-116">Na página **Confirmar seu pedido**, clique em **Experimentar agora**.</span><span class="sxs-lookup"><span data-stu-id="20e2c-116">On the **Confirm your order** page, click **Try now**.</span></span>
    
6. <span data-ttu-id="20e2c-117">Na página **Recibo do pedido**, clique em **Continuar**.</span><span class="sxs-lookup"><span data-stu-id="20e2c-117">On the **Order receipt** page, click **Continue**.</span></span>
    
<span data-ttu-id="20e2c-118">Em seguida, habilite a licença do EMS E5 para a sua conta de administrador global.</span><span class="sxs-lookup"><span data-stu-id="20e2c-118">Next, enable the EMS E5 license for your global administrator account.</span></span>
  
1. <span data-ttu-id="20e2c-119">Na guia **Centro de administração do Office 365** do navegador, no painel de navegação esquerdo, clique em **Usuários > Usuários ativos**.</span><span class="sxs-lookup"><span data-stu-id="20e2c-119">On the **Office 365 Admin center** tab in your browser, in the left navigation, click **Users > Active users**.</span></span>
    
2. <span data-ttu-id="20e2c-120">Clique em sua conta de administrador global e, em seguida, clique em **Editar** para **Licenças de produto**.</span><span class="sxs-lookup"><span data-stu-id="20e2c-120">Click your global administrator account, and then click **Edit** for **Product licenses**.</span></span>
    
3. <span data-ttu-id="20e2c-121">No painel **Licenças de produto**, mude a licença de produto de **Enterprise Mobility + Security E5** para **Ativada**, clique em **Salvar** e clique em **Fechar** duas vezes.</span><span class="sxs-lookup"><span data-stu-id="20e2c-121">On the **Product licenses** pane, turn the product license for **Enterprise Mobility + Security E5** to **On**, click **Save,** and then click **Close** twice.</span></span>
    
## <a name="phase-2-create-and-configure-your-azure-active-directory-ad-groups"></a><span data-ttu-id="20e2c-122">Fase 2: Criar e configurar seus grupos do Azure Active Directory (AD) (Active Directory)</span><span class="sxs-lookup"><span data-stu-id="20e2c-122">Phase 2: Create and configure your Azure Active Directory (AD) groups</span></span>

<span data-ttu-id="20e2c-123">Nesta fase, você cria e configura os grupos do Azure AD para a sua empresa.</span><span class="sxs-lookup"><span data-stu-id="20e2c-123">In this phase, you create and configure the Azure AD groups for your campaign.</span></span>
  
<span data-ttu-id="20e2c-124">Primeiro, crie um conjunto de grupos para uma campanha política com o Portal do Azure.</span><span class="sxs-lookup"><span data-stu-id="20e2c-124">First, create a set of groups for a typical political campaign with the Azure portal.</span></span>
  
1. <span data-ttu-id="20e2c-p103">Em uma guia separada no navegador, vá ao Portal do Azure em [https://portal.azure.com](https://portal.azure.com). Se necessário, entre com as credenciais da conta de administrador global da sua assinatura de avaliação do Office 365 E5.</span><span class="sxs-lookup"><span data-stu-id="20e2c-p103">On a separate tab in your browser, go to the Azure portal at [https://portal.azure.com](https://portal.azure.com). If needed, sign in with the credentials of the global administrator account for your Office 365 E5 trial subscription.</span></span>
    
2. <span data-ttu-id="20e2c-127">No Portal do Azure, clique em **Azure Active Directory > Usuários e grupos > Todos os grupos**.</span><span class="sxs-lookup"><span data-stu-id="20e2c-127">In the Azure portal, click **Azure Active Directory > Users and groups > All groups**.</span></span>
    
3. <span data-ttu-id="20e2c-128">Siga as seguintes etapas para cada nome do grupo nesta lista:</span><span class="sxs-lookup"><span data-stu-id="20e2c-128">Do the following steps for each group name in this list:</span></span>
    
  - <span data-ttu-id="20e2c-129">Equipe estratégica e sênior</span><span class="sxs-lookup"><span data-stu-id="20e2c-129">Senior and strategic staff</span></span>
    
  - <span data-ttu-id="20e2c-130">Equipe de TI</span><span class="sxs-lookup"><span data-stu-id="20e2c-130">IT staff</span></span>
    
  - <span data-ttu-id="20e2c-131">Equipe de análise</span><span class="sxs-lookup"><span data-stu-id="20e2c-131">Analytics staff</span></span>
    
  - <span data-ttu-id="20e2c-132">Equipe principal regular</span><span class="sxs-lookup"><span data-stu-id="20e2c-132">Regular core staff</span></span>
    
  - <span data-ttu-id="20e2c-133">Equipe de operações</span><span class="sxs-lookup"><span data-stu-id="20e2c-133">Operations staff</span></span>
    
  - <span data-ttu-id="20e2c-134">Equipe de campo</span><span class="sxs-lookup"><span data-stu-id="20e2c-134">Field staff</span></span>
    
1. <span data-ttu-id="20e2c-135">Na folha **Todos os grupos**, clique em **+ Novo grupo**.</span><span class="sxs-lookup"><span data-stu-id="20e2c-135">On the **All groups** blade, click **+ New group**.</span></span>
    
2. <span data-ttu-id="20e2c-136">Digite o nome do grupo na lista em **Nome**.</span><span class="sxs-lookup"><span data-stu-id="20e2c-136">Type the group name from the list in **Name**.</span></span>
    
3. <span data-ttu-id="20e2c-137">Selecione **Usuário dinâmico** em **Associação**.</span><span class="sxs-lookup"><span data-stu-id="20e2c-137">Select **Dynamic user** in **Membership**.</span></span>
    
4. <span data-ttu-id="20e2c-138">Selecione **Sim** para **Habilitar recursos do Office**.</span><span class="sxs-lookup"><span data-stu-id="20e2c-138">Click **Yes** for **Enable Office features**.</span></span>
    
5. <span data-ttu-id="20e2c-139">Clique em **Adicionar consulta dinâmica**.</span><span class="sxs-lookup"><span data-stu-id="20e2c-139">Click **Add dynamic query**.</span></span>
    
6. <span data-ttu-id="20e2c-140">Em **Adicionar usuários onde**, selecione **departamento**.</span><span class="sxs-lookup"><span data-stu-id="20e2c-140">In **Add users where**, select **department**.</span></span>
    
7. <span data-ttu-id="20e2c-141">No campo seguinte, selecione **Igual a**.</span><span class="sxs-lookup"><span data-stu-id="20e2c-141">In the next field, select **Equals**.</span></span>
    
8. <span data-ttu-id="20e2c-142">No campo seguinte, digite o nome do grupo na lista.</span><span class="sxs-lookup"><span data-stu-id="20e2c-142">In the next field, type the group name from the list.</span></span>
    
9. <span data-ttu-id="20e2c-143">Clique em **Adicionar consulta** e, em seguida, clique em **Criar**.</span><span class="sxs-lookup"><span data-stu-id="20e2c-143">Click **Add query**, and then click **Create**.</span></span>
    
10. <span data-ttu-id="20e2c-144">Clique em **Usuários e grupos – Todos os grupos**.</span><span class="sxs-lookup"><span data-stu-id="20e2c-144">Click **Users and groups - All groups**.</span></span>
    
<span data-ttu-id="20e2c-145">Em seguida, configure os grupos para que os membros tenham licenças do Office 365 E5 e EMS E5 atribuídas automaticamente.</span><span class="sxs-lookup"><span data-stu-id="20e2c-145">Next, you configure the groups so that members are automatically assigned Office 365 E5 and EMS E5 licenses.</span></span>
  
1. <span data-ttu-id="20e2c-146">No Portal do Azure, clique em **Azure Active Directory > Licenças > Todos os produtos**.</span><span class="sxs-lookup"><span data-stu-id="20e2c-146">In the Azure portal, click **Azure Active Directory > Licenses > All products**.</span></span>
    
2. <span data-ttu-id="20e2c-147">Na lista, selecione **Enterprise Mobility + Security E5** e **Office 365 Enterprise E5** e clique em **Atribuir+**.</span><span class="sxs-lookup"><span data-stu-id="20e2c-147">In the list, select **Enterprise Mobility + Security E5** and **Office 365 Enterprise E5**, and then click **+ Assign**.</span></span>
    
3. <span data-ttu-id="20e2c-148">Na folha **Atribuir licença**, clique em **Usuários e grupos**.</span><span class="sxs-lookup"><span data-stu-id="20e2c-148">In the **Assign license** blade, click **Users and groups**.</span></span>
    
4. <span data-ttu-id="20e2c-149">Na lista de grupos, selecione o seguinte:</span><span class="sxs-lookup"><span data-stu-id="20e2c-149">In the list of groups, select the following:</span></span>
    
  - <span data-ttu-id="20e2c-150">Equipe de análise</span><span class="sxs-lookup"><span data-stu-id="20e2c-150">Analytics staff</span></span>
    
  - <span data-ttu-id="20e2c-151">Equipe de campo</span><span class="sxs-lookup"><span data-stu-id="20e2c-151">Field staff</span></span>
    
  - <span data-ttu-id="20e2c-152">Equipe de TI</span><span class="sxs-lookup"><span data-stu-id="20e2c-152">IT staff</span></span>
    
  - <span data-ttu-id="20e2c-153">Equipe de operações</span><span class="sxs-lookup"><span data-stu-id="20e2c-153">Operations staff</span></span>
    
  - <span data-ttu-id="20e2c-154">Equipe principal regular</span><span class="sxs-lookup"><span data-stu-id="20e2c-154">Regular core staff</span></span>
    
  - <span data-ttu-id="20e2c-155">Equipe estratégica e sênior</span><span class="sxs-lookup"><span data-stu-id="20e2c-155">Senior and strategic staff</span></span>
    
5. <span data-ttu-id="20e2c-156">Clique em **Selecionar** e clique em **Atribuir**.</span><span class="sxs-lookup"><span data-stu-id="20e2c-156">Click **Select**, and then click **Assign**.</span></span>
    
6. <span data-ttu-id="20e2c-157">Feche a guia do Portal do Azure no navegador.</span><span class="sxs-lookup"><span data-stu-id="20e2c-157">Close the Azure portal tab in your browser.</span></span>
    
## <a name="phase-3-add-your-user-accounts"></a><span data-ttu-id="20e2c-158">Fase 3: Adicionar as suas conta de usuário</span><span class="sxs-lookup"><span data-stu-id="20e2c-158">Phase 3: Add your user accounts</span></span>

<span data-ttu-id="20e2c-159">Nesta fase, adicione exemplos de contas de usuário para a sua campanha política.</span><span class="sxs-lookup"><span data-stu-id="20e2c-159">In this phase, you add the example user accounts for your political campaign.</span></span>
  
<span data-ttu-id="20e2c-160">Primeiro, você deve se [Conectar ao módulo PowerShell do Azure Active Directory V2](https://go.microsoft.com/fwlink/?linkid=842218).</span><span class="sxs-lookup"><span data-stu-id="20e2c-160">First, you [Connect with the Azure Active Directory V2 PowerShell module](https://go.microsoft.com/fwlink/?linkid=842218).</span></span>
  
<span data-ttu-id="20e2c-161">Em seguida, preencha o nome de sua organização, o local e uma senha comum e, em seguida, execute esses comandos desde o prompt de comando do PowerShell ou Ambiente de Script Integrado (ISE):</span><span class="sxs-lookup"><span data-stu-id="20e2c-161">Next, you fill in your organization name, your location, and a common password, and then run these commands from the PowerShell command prompt or Integrated Script Environment (ISE):</span></span>
  
```
$orgName="<organization name, such as contoso for the contoso.onmicrosoft.com trial subscription domain name>"
$location="<the ISO ALPHA2 country code, such as US for the United States>"
$commonPassword="<common password for all the new accounts>"

$PasswordProfile=New-Object -TypeName Microsoft.Open.AzureAD.Model.PasswordProfile
$PasswordProfile.Password=$commonPassword

$deptName="Senior and strategic staff"
$userNames=@("Candidate","ChiefOfStaff","Strategic1") 
foreach ($element in $userNames){ New-AzureADUser -DisplayName $element -PasswordProfile $PasswordProfile -UserPrincipalName ($element + "@" + $orgName + ".onmicrosoft.com") -AccountEnabled $true -MailNickName $element -Department $deptName -UsageLocation $location }
$deptName="IT staff"
$userNames=@("ITAdmin1","ITAdmin2") 
foreach ($element in $userNames){ New-AzureADUser -DisplayName $element -PasswordProfile $PasswordProfile -UserPrincipalName ($element + "@" + $orgName + ".onmicrosoft.com") -AccountEnabled $true -MailNickName $element -Department $deptName -UsageLocation $location }
$deptName="Analytics staff"
$userNames=@("DataScientist1") 
foreach ($element in $userNames){ New-AzureADUser -DisplayName $element -PasswordProfile $PasswordProfile -UserPrincipalName ($element + "@" + $orgName + ".onmicrosoft.com") -AccountEnabled $true -MailNickName $element -Department $deptName -UsageLocation $location }
$deptName="Regular core staff"
$userNames=@("Regular1","Regular2") 
foreach ($element in $userNames){ New-AzureADUser -DisplayName $element -PasswordProfile $PasswordProfile -UserPrincipalName ($element + "@" + $orgName + ".onmicrosoft.com") -AccountEnabled $true -MailNickName $element -Department $deptName -UsageLocation $location }
$deptName="Operations staff"
$userNames=@("Operations1") 
foreach ($element in $userNames){ New-AzureADUser -DisplayName $element -PasswordProfile $PasswordProfile -UserPrincipalName ($element + "@" + $orgName + ".onmicrosoft.com") -AccountEnabled $true -MailNickName $element -Department $deptName -UsageLocation $location }
$deptName="Field staff"
$userNames=@("FieldConsultant1") 
foreach ($element in $userNames){ New-AzureADUser -DisplayName $element -PasswordProfile $PasswordProfile -UserPrincipalName ($element + "@" + $orgName + ".onmicrosoft.com") -AccountEnabled $true -MailNickName $element -Department $deptName -UsageLocation $location }

```

> [!IMPORTANT]
> <span data-ttu-id="20e2c-p104">O uso de uma senha comum aqui serve para a automação e a facilidade da configuração para um ambiente de desenvolvimento/de teste. Isso não é recomendável para assinaturas de produção. Ao entrar com cada uma dessas novas contas de usuário, você deverá alterar a senha.</span><span class="sxs-lookup"><span data-stu-id="20e2c-p104">The use of a common password here is for automation and ease of configuration for a dev/test environment. This is not recommended for production subscriptions. As you sign in with each of these new user accounts, you will be prompted to change the password.</span></span> 
  
<span data-ttu-id="20e2c-165">Use estas etapas para verificar se a associação de grupo dinâmico e o licenciamento com base em grupo estão funcionando corretamente.</span><span class="sxs-lookup"><span data-stu-id="20e2c-165">Use these steps to verify that dynamic group membership and group-based licensing are working correctly.</span></span>
  
1. <span data-ttu-id="20e2c-166">Na guia **Microsoft Office Home** do navegador, clique no bloco **Administração**.</span><span class="sxs-lookup"><span data-stu-id="20e2c-166">From the **Microsoft Office Home** tab of your browser, click the **Admin** tile.</span></span>
    
2. <span data-ttu-id="20e2c-167">Na nova guia **Centro de Administração do Office** do navegador, clique em **Usuários**.</span><span class="sxs-lookup"><span data-stu-id="20e2c-167">From the new **Office Admin center** tab of your browser, click **Users**.</span></span>
    
3. <span data-ttu-id="20e2c-168">Na lista de usuários, clique em **Candidato**.</span><span class="sxs-lookup"><span data-stu-id="20e2c-168">In the list of users, click **Candidate**.</span></span>
    
4. <span data-ttu-id="20e2c-169">No painel que lista as propriedades da conta de usuário **Candidato**, verifique se:</span><span class="sxs-lookup"><span data-stu-id="20e2c-169">In the pane that lists the properties of the **Candidate** user account, verify that:</span></span>
    
  - <span data-ttu-id="20e2c-170">É um membro do grupo **Equipe estratégica e sênior** (em **Associações de grupo**).</span><span class="sxs-lookup"><span data-stu-id="20e2c-170">It is a member of the **Senior and strategic staff** group (in **Group memberships**).</span></span>
    
  - <span data-ttu-id="20e2c-171">Foram-lhe atribuídas as licenças do **Enterprise Mobility + Security E5** e do **Office 365 Enterprise E5** (nas **Licenças de produto**).</span><span class="sxs-lookup"><span data-stu-id="20e2c-171">It has been assigned the **Enterprise Mobility + Security E5** and **Office 365 Enterprise E5** licenses (in **Product licenses**).</span></span>
    
5. <span data-ttu-id="20e2c-172">Feche o painel da conta de usuário do **Candidato**.</span><span class="sxs-lookup"><span data-stu-id="20e2c-172">Close the **Candidate** user account pane.</span></span>
    
## <a name="record-values-for-future-reference"></a><span data-ttu-id="20e2c-173">Valores de registro para referência futura</span><span class="sxs-lookup"><span data-stu-id="20e2c-173">Record values for future reference</span></span>

<span data-ttu-id="20e2c-174">Grave esses valores para trabalhar com as assinaturas de avaliação do Office 365 e do EMS para o ambiente de desenvolvimento/de teste:</span><span class="sxs-lookup"><span data-stu-id="20e2c-174">Record these values for working with the Office 365 and EMS trial subscriptions for this dev/test environment:</span></span>
  
- <span data-ttu-id="20e2c-175">Nome da sua organização de assinatura de avaliação: ![](./media/Common-Images/TableLine.png)</span><span class="sxs-lookup"><span data-stu-id="20e2c-175">Your trial subscription organization name: ![](./media/Common-Images/TableLine.png)</span></span> 
    
    <span data-ttu-id="20e2c-176">Por exemplo, para o nome de domínio de assinatura de avaliação contoso.onmicrosoft.com, o nome da organização é "contoso".</span><span class="sxs-lookup"><span data-stu-id="20e2c-176">For example, for the trial subscription domain name of contoso.onmicrosoft.com, the organization name is "contoso".</span></span>
    
- <span data-ttu-id="20e2c-177">O nome de administrador global do Office 365: ![](./media/Common-Images/TableLine.png).onmicrosoft.com</span><span class="sxs-lookup"><span data-stu-id="20e2c-177">The Office 365 global administrator name: ![](./media/Common-Images/TableLine.png).onmicrosoft.com</span></span>
    
    <span data-ttu-id="20e2c-178">Grave a senha dessa conta e a senha inicial comum das outras contas de usuário em um local seguro.</span><span class="sxs-lookup"><span data-stu-id="20e2c-178">Record the password for this account and the common initial password for the other user accounts in a secure location.</span></span>
    
## <a name="next-step"></a><span data-ttu-id="20e2c-179">Próxima etapa</span><span class="sxs-lookup"><span data-stu-id="20e2c-179">Next step</span></span>

<span data-ttu-id="20e2c-180">Criar os quatro diferentes tipos de sites de equipe do SharePoint Online neste ambiente de desenvolvimento/de teste com [Criar sites de equipe em um ambiente de desenvolvimento/de teste de campanha política](create-team-sites-in-a-political-campaign-dev-test-environment.md).</span><span class="sxs-lookup"><span data-stu-id="20e2c-180">Build the four different types of SharePoint Online team sites in this dev/test environment with [Create team sites in a political campaign dev/test environment](create-team-sites-in-a-political-campaign-dev-test-environment.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="20e2c-181">Confira também</span><span class="sxs-lookup"><span data-stu-id="20e2c-181">See also</span></span>

[<span data-ttu-id="20e2c-182">Diretrizes de segurança da Microsoft para campanhas políticas, instituições sem fins lucrativos e outras organizações Agile</span><span class="sxs-lookup"><span data-stu-id="20e2c-182">Microsoft Security Guidance for Political Campaigns, Nonprofits, and Other Agile Organizations</span></span>](microsoft-security-guidance-for-political-campaigns-nonprofits-and-other-agile-o.md)
  
[<span data-ttu-id="20e2c-183">Criar sites de equipe em um ambiente de desenvolvimento/teste de campanha política</span><span class="sxs-lookup"><span data-stu-id="20e2c-183">Create team sites in a political campaign dev/test environment</span></span>](create-team-sites-in-a-political-campaign-dev-test-environment.md)
  
[<span data-ttu-id="20e2c-184">Guias do Laboratório de Teste (TLGs) para adoção de nuvem</span><span class="sxs-lookup"><span data-stu-id="20e2c-184">Cloud adoption Test Lab Guides (TLGs)</span></span>](https://docs.microsoft.com/office365/enterprise/cloud-adoption-test-lab-guides-tlgs)
  
[<span data-ttu-id="20e2c-185">Adoção da nuvem e de soluções híbridas</span><span class="sxs-lookup"><span data-stu-id="20e2c-185">Cloud adoption and hybrid solutions</span></span>](https://docs.microsoft.com/office365/enterprise/cloud-adoption-and-hybrid-solutions)




