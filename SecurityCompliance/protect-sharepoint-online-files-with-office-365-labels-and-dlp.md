---
title: Proteger arquivos do SharePoint Online com DLP e rótulos do Office 365
ms.author: josephd
author: JoeDavies-MSFT
manager: laurawi
ms.date: 12/12/2018
ms.audience: ITPro
ms.topic: article
ms.service: o365-solutions
localization_priority: Priority
search.appverid:
- MET150
ms.collection:
- Ent_O365
- Strat_O365_Enterprise
ms.custom:
- Ent_Solutions
ms.assetid: c9f837af-8d71-4df1-a285-dedb1c5618b3
description: 'Resumo: Aplique rótulos do Office 365 e políticas de DLP (prevenção de perda de dados) aos sites de equipe do SharePoint Online com vários níveis de proteção de informações.'
ms.openlocfilehash: fd2fedf23b4e65bd32642b8528548f8a85533051
ms.sourcegitcommit: 6ff0233b5a1a07595f8b4d55db6b1327bcaa174c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/15/2019
ms.locfileid: "28023427"
---
# <a name="protect-sharepoint-online-files-with-office-365-labels-and-dlp"></a><span data-ttu-id="de91c-103">Proteger arquivos do SharePoint Online com DLP e rótulos do Office 365</span><span class="sxs-lookup"><span data-stu-id="de91c-103">Protect SharePoint Online files with Office 365 labels and DLP</span></span>

 <span data-ttu-id="de91c-104">**Resumo:** Aplique rótulos do Office 365 e políticas de DLP (prevenção de perda de dados) aos sites de equipe do SharePoint Online com vários níveis de proteção de informações.</span><span class="sxs-lookup"><span data-stu-id="de91c-104">**Summary:** Apply Office 365 labels and data loss prevention (DLP) policies for SharePoint Online team sites with various levels of information protection.</span></span>
  
<span data-ttu-id="de91c-p101">Use as etapas neste artigo para projetar e implantar políticas de DLP e rótulos do Office 365 para sites de equipe do SharePoint Online de linha de base, confidenciais e altamente confidenciais. Para obter mais informações sobre essas três camadas de proteção, consulte [Arquivos e sites do SharePoint Online seguros](secure-sharepoint-online-sites-and-files.md).</span><span class="sxs-lookup"><span data-stu-id="de91c-p101">Use the steps in this article to design and deploy Office 365 labels and DLP policies for baseline, sensitive, and highly confidential SharePoint Online team sites. For more information about these three tiers of protection, see [Secure SharePoint Online sites and files](secure-sharepoint-online-sites-and-files.md).</span></span>
  
## <a name="how-this-works"></a><span data-ttu-id="de91c-107">Como isso funciona</span><span class="sxs-lookup"><span data-stu-id="de91c-107">How this works</span></span>
1. <span data-ttu-id="de91c-p102">Crie os rótulos desejados e publique-os. Pode levar até 12 horas para que eles sejam publicados.</span><span class="sxs-lookup"><span data-stu-id="de91c-p102">Create the desired labels and publish these. It can take up to 12 hours for these to be published.</span></span>
2. <span data-ttu-id="de91c-110">Para os sites do SharePoint desejados, edite as configurações de biblioteca de documentos para aplicar um rótulo a itens na biblioteca.</span><span class="sxs-lookup"><span data-stu-id="de91c-110">For the desired SharePoint sites, edit the document library settings to apply a label to items in the library.</span></span>
3. <span data-ttu-id="de91c-111">Crie políticas DLP para agir com base nas etiquetas.</span><span class="sxs-lookup"><span data-stu-id="de91c-111">Create DLP policies to take action based on the labels.</span></span>

<span data-ttu-id="de91c-p103">Quando os usuários adicionam um documento à biblioteca, o documento recebe o rótulo atribuído por padrão. Os usuários podem alterar o rótulo, se necessário. Quando um usuário compartilha um documento para fora da organização, a DLP verifica se um rótulo foi atribuído e toma medidas caso uma política DLP corresponda ao rótulo. A DLP também procura por outras correspondências de política, como a proteção de arquivos com números de cartão de crédito, se esse tipo de política estiver configurado.</span><span class="sxs-lookup"><span data-stu-id="de91c-p103">When users add a document to the library, the document will receive the assigned label by default. Users can change the label, if needed. When a user shares a document outside the organization, DLP will check to see if a label is assigned and take action if a DLP policy matches the label. DLP will look for other policy matches as well, such as protecting files with credit card numbers if this type of policy is configured.</span></span> 

## <a name="office-365-labels-for-your-sharepoint-online-sites"></a><span data-ttu-id="de91c-116">Rótulos do Office 365 para seus sites do SharePoint Online</span><span class="sxs-lookup"><span data-stu-id="de91c-116">Office 365 labels for your SharePoint Online sites</span></span>

<span data-ttu-id="de91c-117">Há três etapas para criar e atribuir rótulos do Office 365 a sites de equipe do SharePoint Online.</span><span class="sxs-lookup"><span data-stu-id="de91c-117">There are three phases to creating and then assigning Office 365 labels to SharePoint Online team sites.</span></span>
  
### <a name="phase-1-determine-the-office-365-label-names"></a><span data-ttu-id="de91c-118">Etapa 1: Determinar os nomes de rótulo do Office 365</span><span class="sxs-lookup"><span data-stu-id="de91c-118">Phase 1: Determine the Office 365 label names</span></span>

<span data-ttu-id="de91c-p104">Nesta fase, você determina os nomes dos rótulos do Office 365 para os quatro níveis de proteção de informações aplicados a sites de equipe do SharePoint Online. A tabela a seguir lista os nomes recomendados para cada nível.</span><span class="sxs-lookup"><span data-stu-id="de91c-p104">In this phase, you determine the names of your Office 365 labels for the four levels of information protection applied to SharePoint Online team sites. The following table lists the recommended names for each level.</span></span>
  
|<span data-ttu-id="de91c-121">**Nível de proteção do site de equipe do SharePoint Online**</span><span class="sxs-lookup"><span data-stu-id="de91c-121">**SharePoint Online team site protection level**</span></span>|<span data-ttu-id="de91c-122">**Nome do rótulo**</span><span class="sxs-lookup"><span data-stu-id="de91c-122">**Label name**</span></span>|
|:-----|:-----|
|<span data-ttu-id="de91c-123">Linha de base público</span><span class="sxs-lookup"><span data-stu-id="de91c-123">Baseline-Public</span></span>  <br/> |<span data-ttu-id="de91c-124">Público interno</span><span class="sxs-lookup"><span data-stu-id="de91c-124">Internal public</span></span>  <br/> |
|<span data-ttu-id="de91c-125">Linha de base privado</span><span class="sxs-lookup"><span data-stu-id="de91c-125">Baseline-Private</span></span>  <br/> |<span data-ttu-id="de91c-126">Private</span><span class="sxs-lookup"><span data-stu-id="de91c-126">Private</span></span>  <br/> |
|<span data-ttu-id="de91c-127">Confidencial</span><span class="sxs-lookup"><span data-stu-id="de91c-127">Sensitive</span></span>  <br/> |<span data-ttu-id="de91c-128">Confidencial</span><span class="sxs-lookup"><span data-stu-id="de91c-128">Sensitive</span></span>  <br/> |
|<span data-ttu-id="de91c-129">Altamente Confidencial</span><span class="sxs-lookup"><span data-stu-id="de91c-129">Highly Confidential</span></span>  <br/> |<span data-ttu-id="de91c-130">Altamente Confidencial</span><span class="sxs-lookup"><span data-stu-id="de91c-130">Highly Confidential</span></span>  <br/> |
   
### <a name="phase-2-create-the-office-365-labels"></a><span data-ttu-id="de91c-131">Fase 2: Criar os rótulos do Office 365</span><span class="sxs-lookup"><span data-stu-id="de91c-131">Phase 2: Create the Office 365 labels</span></span>

<span data-ttu-id="de91c-132">Nesta fase, você cria e publica seus determinados rótulos para os diferentes níveis de proteção de informações.</span><span class="sxs-lookup"><span data-stu-id="de91c-132">In this phase, you create and then publish your determined labels for the different levels of information protection.</span></span>
  
<span data-ttu-id="de91c-133">Para criar os rótulos, você pode usar o Centro de administração do Office 365 ou o Microsoft PowerShell.</span><span class="sxs-lookup"><span data-stu-id="de91c-133">To create the labels, you can use the Office 365 Admin center or Microsoft PowerShell.</span></span>
  
### <a name="create-office-365-labels-with-the-office-365-admin-center"></a><span data-ttu-id="de91c-134">Criar rótulos do Office 365 com o Centro de administração do Office 365</span><span class="sxs-lookup"><span data-stu-id="de91c-134">Create Office 365 labels with the Office 365 Admin center</span></span>

1. <span data-ttu-id="de91c-p105">Entre no Portal do Office 365 com uma conta que tenha a função de Administrador de Segurança ou Administrador da Empresa. Para obter ajuda, consulte [Onde entrar no Office 365](https://support.office.com/Article/Where-to-sign-in-to-Office-365-e9eb7d51-5430-4929-91ab-6157c5a050b4).</span><span class="sxs-lookup"><span data-stu-id="de91c-p105">Sign in to the Office 365 portal with an account that has the Security Administrator or Company Administrator role. For help, see [Where to sign in to Office 365](https://support.office.com/Article/Where-to-sign-in-to-Office-365-e9eb7d51-5430-4929-91ab-6157c5a050b4).</span></span>
    
2. <span data-ttu-id="de91c-137">Na guia **Microsoft Office Home**, clique no bloco **Administração**.</span><span class="sxs-lookup"><span data-stu-id="de91c-137">From the **Microsoft Office Home** tab, click the **Admin** tile.</span></span>
    
3. <span data-ttu-id="de91c-138">Na nova guia **Centro de Administração do Office** do navegador, clique em **Centros de Administração > Segurança&amp; e Conformidade**.</span><span class="sxs-lookup"><span data-stu-id="de91c-138">From the new **Office Admin center** tab of your browser, click **Admin centers > Security &amp; Compliance**.</span></span>
    
4. <span data-ttu-id="de91c-139">Na nova guia **Início – Segurança &amp;e Conformidade** do navegador, clique em **Classificações > Rótulos**.</span><span class="sxs-lookup"><span data-stu-id="de91c-139">From the new **Home - Security &amp; Compliance** tab of your browser, click **Classifications > Labels**.</span></span>
    
5. <span data-ttu-id="de91c-140">No painel **Página inicial > Rótulos**, clique na guia **Retenção** e, em seguida, clique em **Criar um rótulo**.</span><span class="sxs-lookup"><span data-stu-id="de91c-140">From the **Home > Labels** pane, click the **Retention** tab, and then click **Create a label**.</span></span>
    
6. <span data-ttu-id="de91c-141">No painel **Atribuir nome ao seu rótulo**, digite o nome do rótulo e uma descrição para administradores e usuários e, em seguida, clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="de91c-141">On the **Name your label** pane, type the name of the label and a description for admins and users, and then click **Next**.</span></span>

7. <span data-ttu-id="de91c-142">No painel **Configurações do rótulo**, clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="de91c-142">On the **Label settings** pane, click **Next**.</span></span>
    
8. <span data-ttu-id="de91c-143">No painel **Examine as configurações**, clique em **Criar** e em **Fechar**.</span><span class="sxs-lookup"><span data-stu-id="de91c-143">On the **Review your settings** pane, click **Create**, and then click **Close**.</span></span>
    
9. <span data-ttu-id="de91c-144">Repita as etapas de 5 a 8 para os rótulos adicionais.</span><span class="sxs-lookup"><span data-stu-id="de91c-144">Repeat steps 5-8 for your additional labels.</span></span>
    
### <a name="create-office-365-labels-with-powershell"></a><span data-ttu-id="de91c-145">Criar rótulos do Office 365 com o PowerShell</span><span class="sxs-lookup"><span data-stu-id="de91c-145">Create Office 365 labels with PowerShell</span></span>

1. <span data-ttu-id="de91c-146">[Conecte-se ao Centro de Segurança e Conformidade do Office 365 &amp;usando o PowerShell](http://go.microsoft.com/fwlink/?LinkID=799771&amp;clcid=0x409) remoto e especifique as credenciais da conta que têm a função de Administrador de Segurança ou Administrador da Empresa.</span><span class="sxs-lookup"><span data-stu-id="de91c-146">[Connect to the Office 365 Security &amp; Compliance Center using remote PowerShell](http://go.microsoft.com/fwlink/?LinkID=799771&amp;clcid=0x409) and specify the credentials of an account that has the Security Administrator or Company Administrator role.</span></span>
    
2. <span data-ttu-id="de91c-147">Preencha a lista de nomes de rótulo e execute esses comandos no prompt de comando do PowerShell:</span><span class="sxs-lookup"><span data-stu-id="de91c-147">Fill out the list of label names, and then run these commands at the PowerShell command prompt:</span></span>
    
  ```
  $labelNames=@(<list of label names, each enclosed in quotes and separated by commas>)
ForEach ($element in $labelNames){ New-ComplianceTag -Name $element }
  ```

### <a name="publish-your-new-labels"></a><span data-ttu-id="de91c-148">Publicar seus novos rótulos</span><span class="sxs-lookup"><span data-stu-id="de91c-148">Publish your new labels</span></span>

<span data-ttu-id="de91c-149">Em seguida, use estas etapas para publicar os novos rótulos do Office 365.</span><span class="sxs-lookup"><span data-stu-id="de91c-149">Next, use these steps to publish the new Office 365 labels.</span></span>
  
1. <span data-ttu-id="de91c-150">No painel **Início > Rótulos** no Centro de Segurança &amp;e Conformidade, clique na guia **Retenção** e, em seguida, clique em **Publicar rótulos**.</span><span class="sxs-lookup"><span data-stu-id="de91c-150">From the **Home > Labels** pane of the Security &amp; Compliance Center, click the **Retention** tab, and then click **Publish labels**.</span></span>
    
2. <span data-ttu-id="de91c-151">No painel **Escolher rótulos para publicar**, clique em **Escolher rótulos para publicar**.</span><span class="sxs-lookup"><span data-stu-id="de91c-151">On the **Choose labels to publish** pane, click **Choose labels to publish**.</span></span>
    
3. <span data-ttu-id="de91c-152">No painel **Escolher rótulos**, clique em **Adicionar** e selecione todos os quatro rótulos.</span><span class="sxs-lookup"><span data-stu-id="de91c-152">On the **Choose labels** pane, click **Add** and select all four labels.</span></span>
    
4. <span data-ttu-id="de91c-153">Clique em **Concluído**.</span><span class="sxs-lookup"><span data-stu-id="de91c-153">Click **Done**.</span></span>
    
5. <span data-ttu-id="de91c-154">No painel **Escolher rótulos para publicar**, clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="de91c-154">On the **Choose labels to publish** pane, click **Next**.</span></span>
    
6. <span data-ttu-id="de91c-155">No painel **Escolher locais**, clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="de91c-155">On the **Choose locations** pane, click **Next**.</span></span>
    
7. <span data-ttu-id="de91c-156">No painel **Atribuir um nome à política**, digite um nome para o conjunto de rótulos em **Nome** e clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="de91c-156">On the **Name your policy** pane, type a name for your set of labels in **Name**, and then click **Next**.</span></span>
    
8. <span data-ttu-id="de91c-157">No painel **Examine as configurações**, clique em **Publicar rótulos** e clique em **Fechar**.</span><span class="sxs-lookup"><span data-stu-id="de91c-157">On the **Review your settings** pane, click **Publish labels**, and then click **Close**.</span></span>

    
### <a name="phase-3-apply-the-office-365-labels-to-your-sharepoint-online-sites"></a><span data-ttu-id="de91c-158">Etapa 3: Aplicar os rótulos do Office 365 aos sites do SharePoint Online</span><span class="sxs-lookup"><span data-stu-id="de91c-158">Phase 3: Apply the Office 365 labels to your SharePoint Online sites</span></span>

<span data-ttu-id="de91c-159">Use estas etapas para aplicar os rótulos do Office 365 às pastas de documentos de seus sites de equipe do SharePoint Online.</span><span class="sxs-lookup"><span data-stu-id="de91c-159">Use these steps to apply the Office 365 labels to the documents folders of your SharePoint Online team sites.</span></span>
  
1. <span data-ttu-id="de91c-160">Na guia **Microsoft Office Home** do navegador, clique no bloco **SharePoint**.</span><span class="sxs-lookup"><span data-stu-id="de91c-160">From the **Microsoft Office Home** tab of your browser, click the **SharePoint** tile.</span></span>
    
2. <span data-ttu-id="de91c-161">Na nova guia **SharePoint** no navegador, clique em um site que precisa de um rótulo do Office 365 atribuído.</span><span class="sxs-lookup"><span data-stu-id="de91c-161">On the new **SharePoint** tab in your browser, click a site that needs an Office 365 label assigned.</span></span>
    
3. <span data-ttu-id="de91c-162">Na nova guia de site do SharePoint do navegador, clique em **Documentos**.</span><span class="sxs-lookup"><span data-stu-id="de91c-162">In the new SharePoint site tab of your browser, click **Documents**.</span></span>
    
4. <span data-ttu-id="de91c-163">Clique no ícone de configurações e clique em **Configurações de biblioteca**.</span><span class="sxs-lookup"><span data-stu-id="de91c-163">Click the settings icon, and then click **Library settings**.</span></span>
    
5. <span data-ttu-id="de91c-164">Em **Permissões e Gerenciamento**, clique em **Aplicar o rótulo aos itens nessa biblioteca**.</span><span class="sxs-lookup"><span data-stu-id="de91c-164">Under **Permissions and Management**, click **Apply label to items in this library**.</span></span>
    
6. <span data-ttu-id="de91c-165">Em **Configurações – Aplicar Rótulo**, selecione o rótulo adequado e clique em **Salvar**.</span><span class="sxs-lookup"><span data-stu-id="de91c-165">In **Settings-Apply Label**, select the appropriate label, and then click **Save**.</span></span>
    
7. <span data-ttu-id="de91c-166">Feche a guia para o site do SharePoint Online.</span><span class="sxs-lookup"><span data-stu-id="de91c-166">Close the tab for the SharePoint Online site.</span></span>
    
8. <span data-ttu-id="de91c-167">Repita as etapas 3 a 8 acima para atribuir rótulos do Office 365 aos sites adicionais do SharePoint Online.</span><span class="sxs-lookup"><span data-stu-id="de91c-167">Repeat steps 3-8 to assign Office 365 labels to your additional SharePoint Online sites.</span></span>
    
<span data-ttu-id="de91c-168">Esta é a configuração resultante.</span><span class="sxs-lookup"><span data-stu-id="de91c-168">Here is your resulting configuration.</span></span>
  
![Rótulos do Office 365 para os quatro tipos de sites de equipe do SharePoint Online.](media/e0a4fdd2-1c30-4d93-8af4-a6f0c6c29966.png)
  
## <a name="dlp-policies-for-your-sharepoint-online-sites"></a><span data-ttu-id="de91c-170">Políticas DLP para seus sites do SharePoint Online</span><span class="sxs-lookup"><span data-stu-id="de91c-170">DLP policies for your SharePoint Online sites</span></span>

<span data-ttu-id="de91c-171">Use estas etapas para configurar uma política DLP que notifica os usuários quando eles compartilham um documento em um site de equipe confidencial do SharePoint Online fora da organização.</span><span class="sxs-lookup"><span data-stu-id="de91c-171">Use these steps to configure a DLP policy that notifies users when they share a document on a SharePoint Online sensitive team site outside the organization.</span></span>

1. <span data-ttu-id="de91c-172">Na guia **Microsoft Office Home**, clique no bloco **Administração**.</span><span class="sxs-lookup"><span data-stu-id="de91c-172">From the **Microsoft Office Home** tab, click the **Admin** tile.</span></span>
    
2. <span data-ttu-id="de91c-173">Na nova guia **Centro de Administração do Office** do navegador, clique em **Centros de Administração > Segurança&amp; e Conformidade**.</span><span class="sxs-lookup"><span data-stu-id="de91c-173">From the new **Office Admin center** tab of your browser, click **Admin centers > Security &amp; Compliance**.</span></span>
    
3. <span data-ttu-id="de91c-174">Na nova guia **Segurança e&amp; Conformidade** no navegador, clique em **Prevenção de perda de dados > Política**.</span><span class="sxs-lookup"><span data-stu-id="de91c-174">On the new **Security &amp; Compliance** tab in your browser, click **Data loss prevention > Policy**.</span></span>
    
4. <span data-ttu-id="de91c-175">No painel **Prevenção de perda de dados**, clique em **+ Criar uma política**.</span><span class="sxs-lookup"><span data-stu-id="de91c-175">In the **Data loss prevention** pane, click **+ Create a policy**.</span></span>
    
5. <span data-ttu-id="de91c-176">No painel **Iniciar com um modelo ou criar uma política personalizada**, clique em **Personalizado** e clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="de91c-176">In the **Start with a template or create a custom policy** pane, click **Custom**, and then click **Next**.</span></span>
    
5. <span data-ttu-id="de91c-177">No painel **Atribuir um nome à política**, digite o nome da política DLP de nível confidencial em **Nome** e clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="de91c-177">In the **Name your policy** pane, type the name for the sensitive level DLP policy in **Name**, and then click **Next**.</span></span>
    
6. <span data-ttu-id="de91c-178">No painel **Escolher locais**, clique em **Deixe-me escolher locais específicos** e, em seguida, clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="de91c-178">In the **Choose locations** pane, click **Let me choose specific locations**, and then click **Next**.</span></span>
    
7. <span data-ttu-id="de91c-179">Na lista de locais, desabilite os locais **Email do Exchange** e **Contas do OneDrive** e clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="de91c-179">In the list of locations, disable the **Exchange email** and **OneDrive accounts** locations, and then click **Next**.</span></span>
    
8. <span data-ttu-id="de91c-180">Em **personalizar um tipo de conteúdo que deseja proteger** painel, clique em **editar**.</span><span class="sxs-lookup"><span data-stu-id="de91c-180">In the **Customize the types of sensitive info you want to protect** pane, click **Edit**.</span></span>
    
9. <span data-ttu-id="de91c-181">No painel **Escolher os tipos de conteúdo para proteger**, clique em **Adicionar** na caixa suspensa e clique em **Rótulos**.</span><span class="sxs-lookup"><span data-stu-id="de91c-181">In the **Choose the types of content to protect** pane, click **Add** in the drop-down box, and then click **Labels**.</span></span>
    
10. <span data-ttu-id="de91c-182">No painel **Rótulos**, clique em **+ Adicionar**, selecione o rótulo **Confidencial**, clique em **Adicionar** e clique em **Concluído**.</span><span class="sxs-lookup"><span data-stu-id="de91c-182">In the **Labels** pane, click **+ Add**, select the **Sensitive** label, click **Add**, and then click **Done**.</span></span>
    
11. <span data-ttu-id="de91c-183">No painel **Escolher os tipos de conteúdo para proteger**, clique em **Salvar**.</span><span class="sxs-lookup"><span data-stu-id="de91c-183">In the **Choose the types of content to protect** pane, click **Save**.</span></span>
    
12. <span data-ttu-id="de91c-184">No painel **personalizar um tipo de conteúdo que deseja proteger**, clique em **próxima**.</span><span class="sxs-lookup"><span data-stu-id="de91c-184">In the **Customize the types of sensitive info you want to protect** pane, click **Next**.</span></span>

13. <span data-ttu-id="de91c-185">No painel **O que deseja fazer se detectarmos informações confidenciais?**, clique em **Personalizar a dica e o email**.</span><span class="sxs-lookup"><span data-stu-id="de91c-185">In the **What do you want to do if we detect sensitive info?** pane, click **Customize the tip and email**.</span></span>
    
14. <span data-ttu-id="de91c-186">No painel **Personalizar dicas de política e notificações de email**, clique em **Personalizar o texto da dica da política**.</span><span class="sxs-lookup"><span data-stu-id="de91c-186">In the **Customize policy tips and email notifications** pane, click **Customize the policy tip text**.</span></span>
    
15. <span data-ttu-id="de91c-187">Na caixa de texto, digite ou cole uma das dicas a seguir, dependendo de se você implementou a Proteção de Informações do Azure para proteger arquivos altamente confidenciais:</span><span class="sxs-lookup"><span data-stu-id="de91c-187">In the text box, type or paste in one of the following tips, depending on if you implemented Azure Information Protection to protect highly confidential files:</span></span>
    
  - <span data-ttu-id="de91c-p106">Para compartilhar com um usuário de fora da organização, baixe o arquivo e abra-o. Clique em Arquivo, em seguida, Proteger Documento e Criptografar com Senha e especifique uma senha forte. Envie a senha em um email separado ou outros meios de comunicação.</span><span class="sxs-lookup"><span data-stu-id="de91c-p106">To share with a user outside the organization, download the file and then open it. Click File, then Protect Document, and then Encrypt with Password, and then specify a strong password. Send the password in a separate email or other means of communication.</span></span>
  - <span data-ttu-id="de91c-p107">Arquivos altamente confidenciais são protegidos com criptografia. Somente usuários externos que recebam permissões do seu departamento de TI para esses arquivos poderão lê-los.</span><span class="sxs-lookup"><span data-stu-id="de91c-p107">Highly confidential files are protected with encryption. Only external users who are granted permissions to these files by your IT department can read them.</span></span>
    
    <span data-ttu-id="de91c-193">Como alternativa, digite ou cole em sua própria dica de política que instrui os usuários sobre como compartilhar um arquivo fora da organização.</span><span class="sxs-lookup"><span data-stu-id="de91c-193">Alternately, type or paste in your own policy tip that instructs users on how to share a file outside your organization.</span></span>
    
16. <span data-ttu-id="de91c-194">Clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="de91c-194">Click **OK**.</span></span>
    
17. <span data-ttu-id="de91c-195">No painel **O que deseja fazer se detectarmos informações confidenciais?**, clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="de91c-195">In the **What do you want to do if we detect sensitive info?** pane, click **Next**.</span></span>
    
18. <span data-ttu-id="de91c-196">No painel **Deseja ativar a política ou testar primeiro?**, clique em **Sim** para ativá-la imediatamente e clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="de91c-196">In the **Do you want to turn on the policy or test things out first?** pane, click **Yes, turn it on right away**, and then click **Next**.</span></span>
    
19. <span data-ttu-id="de91c-197">No painel **Examine as configurações**, clique em **Criar** e em **Fechar**.</span><span class="sxs-lookup"><span data-stu-id="de91c-197">In the **Review your settings** pane, click **Create**, and then click **Close**.</span></span>
    
<span data-ttu-id="de91c-198">Aqui está a configuração resultante dos sites confidenciais da equipe do SharePoint Online.</span><span class="sxs-lookup"><span data-stu-id="de91c-198">Here is your resulting configuration for sensitive SharePoint Online team sites.</span></span>
  
![A política DLP para um site de equipe isolado do SharePoint Online usando o rótulo Confidencial do Office 365.](media/2ff4cc53-87a8-43e3-b637-3068d88409f3.png)
  
<span data-ttu-id="de91c-200">Em seguida, use estas etapas para configurar uma política DLP que bloqueia os usuários quando eles compartilham um documento em um site de equipe altamente confidencial do SharePoint Online fora da organização.</span><span class="sxs-lookup"><span data-stu-id="de91c-200">Next, use these steps to configure a DLP policy that blocks users when they share a document on a SharePoint Online highly confidential team site outside the organization.</span></span>
  
1. <span data-ttu-id="de91c-201">Na guia **Microsoft Office Home** no navegador, clique no bloco **Segurança&amp; Conformidade**.</span><span class="sxs-lookup"><span data-stu-id="de91c-201">From the **Microsoft Office Home** tab in your browser, click the **Security &amp; Compliance** tile.</span></span>
    
2. <span data-ttu-id="de91c-202">Na nova guia **Segurança e&amp; Conformidade** no navegador, clique em **Prevenção de perda de dados > Política**.</span><span class="sxs-lookup"><span data-stu-id="de91c-202">On the new **Security &amp; Compliance** tab in your browser, click **Data loss prevention > Policy**.</span></span>
    
3. <span data-ttu-id="de91c-203">No painel **Prevenção de perda de dados**, clique em **+ Criar uma política**.</span><span class="sxs-lookup"><span data-stu-id="de91c-203">In the **Data loss prevention** pane, click **+ Create a policy**.</span></span>
    
4. <span data-ttu-id="de91c-204">No painel **Iniciar com um modelo ou criar uma política personalizada**, clique em **Personalizado** e clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="de91c-204">In the **Start with a template or create a custom policy** pane, click **Custom**, and then click **Next**.</span></span>
    
5. <span data-ttu-id="de91c-205">No painel **Atribuir um nome à política**, digite o nome da política DLP de nível altamente confidencial em **Nome** e clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="de91c-205">In the **Name your policy** pane, type the name for the highly sensitive level DLP policy in **Name**, and then click **Next**.</span></span>
    
6. <span data-ttu-id="de91c-206">No painel **Escolher locais**, clique em **Deixe-me escolher locais específicos** e, em seguida, clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="de91c-206">In the **Choose locations** pane, click **Let me choose specific locations**, and then click **Next**.</span></span>
    
7. <span data-ttu-id="de91c-207">Na lista de locais, desabilite os locais **Email do Exchange** e **Contas do OneDrive** e clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="de91c-207">In the list of locations, disable the **Exchange email** and **OneDrive accounts** locations, and then click **Next**.</span></span>
    
8. <span data-ttu-id="de91c-208">No painel **Personalizar os tipos de informações confidenciais que deseja proteger** e clique em **Editar**.</span><span class="sxs-lookup"><span data-stu-id="de91c-208">In the **Customize the types of sensitive info you want to protect** pane, click **Edit**.</span></span>
    
9. <span data-ttu-id="de91c-209">No painel **Escolher os tipos de conteúdo para proteger**, clique em **Adicionar** na caixa suspensa e clique em **Rótulos**.</span><span class="sxs-lookup"><span data-stu-id="de91c-209">In the **Choose the types of content to protect** pane, click **Add** in the drop-down box, and then click **Labels**.</span></span>
    
10. <span data-ttu-id="de91c-210">No painel **Rótulos**, clique em **+ Adicionar**, selecione o **rótulo Altamente Confidencial**, clique em **Adicionar** e clique em **Concluído**.</span><span class="sxs-lookup"><span data-stu-id="de91c-210">In the **Labels** pane, click **+ Add**, select the **Highly Confidential** label, click **Add**, and then click **Done**.</span></span>
    
11. <span data-ttu-id="de91c-211">No painel **Escolher os tipos de conteúdo para proteger**, clique em **Salvar**.</span><span class="sxs-lookup"><span data-stu-id="de91c-211">In the **Choose the types of content to protect** pane, click **Save**.</span></span>
    
12. <span data-ttu-id="de91c-212">No painel **Personalizar os tipos de informações confidenciais que deseja proteger** e clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="de91c-212">In the **Customize the types of sensitive info you want to protect** pane, click **Next**.</span></span>
    
13. <span data-ttu-id="de91c-213">No painel **O que deseja fazer se detectarmos informações confidenciais?**, clique em **Personalizar a dica e o email**.</span><span class="sxs-lookup"><span data-stu-id="de91c-213">In the **What do you want to do if we detect sensitive info?** pane, click **Customize the tip and email**.</span></span>
    
14. <span data-ttu-id="de91c-214">No painel **Personalizar dicas de política e notificações de email**, clique em **Personalizar o texto da dica da política**.</span><span class="sxs-lookup"><span data-stu-id="de91c-214">In the **Customize policy tips and email notifications** pane, click **Customize the policy tip text**.</span></span>
    
15. <span data-ttu-id="de91c-215">Na caixa de texto, digite ou cole o seguinte:</span><span class="sxs-lookup"><span data-stu-id="de91c-215">In the text box, type or paste in the following:</span></span>
    
  - <span data-ttu-id="de91c-p108">Para compartilhar com um usuário de fora da organização, baixe o arquivo e abra-o. Clique em Arquivo, em seguida, Proteger Documento e Criptografar com Senha e especifique uma senha forte. Envie a senha em um email separado ou outros meios de comunicação.</span><span class="sxs-lookup"><span data-stu-id="de91c-p108">To share with a user outside the organization, download the file and then open it. Click File, then Protect Document, and then Encrypt with Password, and then specify a strong password. Send the password in a separate email or other means of communication.</span></span>
    
    <span data-ttu-id="de91c-219">Como alternativa, digite ou cole em sua própria dica de política que instrui os usuários sobre como compartilhar um arquivo fora da organização.</span><span class="sxs-lookup"><span data-stu-id="de91c-219">Alternately, type or paste in your own policy tip that instructs users on how to share a file outside your organization.</span></span>
    
16. <span data-ttu-id="de91c-220">Clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="de91c-220">Click **OK**.</span></span>
    
17. <span data-ttu-id="de91c-221">No painel **O que deseja fazer se detectarmos informações confidenciais?**, clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="de91c-221">In the **What do you want to do if we detect sensitive info?** pane, click **Next**.</span></span>
    
18. <span data-ttu-id="de91c-222">No painel **Deseja ativar a política ou testar primeiro?**, clique em **Sim** para ativá-la imediatamente e clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="de91c-222">In the **Do you want to turn on the policy or test things out first?** pane, click **Yes, turn it on right away**, and then click **Next**.</span></span>
    
19. <span data-ttu-id="de91c-223">No painel **Examine as configurações**, clique em **Criar** e em **Fechar**.</span><span class="sxs-lookup"><span data-stu-id="de91c-223">In the **Review your settings** pane, click **Create**, and then click **Close**.</span></span>
    
<span data-ttu-id="de91c-224">Aqui está a configuração resultante para sites de equipe do SharePoint Online de alta confidencialidade.</span><span class="sxs-lookup"><span data-stu-id="de91c-224">Here is your resulting configuration for high confidentiality SharePoint Online team sites.</span></span>
  
![A política DLP para um site de equipe isolado do SharePoint Online usando o rótulo Altamente Confidencial do Office 365.](media/f705d3d0-23c9-4333-8b70-ad3b91f835ea.png)
  
## <a name="next-step"></a><span data-ttu-id="de91c-226">Próxima etapa</span><span class="sxs-lookup"><span data-stu-id="de91c-226">Next step</span></span>

[<span data-ttu-id="de91c-227">Proteger arquivos do SharePoint Online com a Proteção de Informações do Azure</span><span class="sxs-lookup"><span data-stu-id="de91c-227">Protect SharePoint Online files with Azure Information Protection</span></span>](protect-sharepoint-online-files-with-azure-information-protection.md)
    
## <a name="see-also"></a><span data-ttu-id="de91c-228">Confira também</span><span class="sxs-lookup"><span data-stu-id="de91c-228">See Also</span></span>

[<span data-ttu-id="de91c-229">Proteger sites e arquivos do SharePoint Online</span><span class="sxs-lookup"><span data-stu-id="de91c-229">Secure SharePoint Online sites and files</span></span>](secure-sharepoint-online-sites-and-files.md)
  
[<span data-ttu-id="de91c-230">Proteger os sites do SharePoint Online em um ambiente de desenvolvimento/teste</span><span class="sxs-lookup"><span data-stu-id="de91c-230">Secure SharePoint Online sites in a dev/test environment</span></span>](secure-sharepoint-online-sites-in-a-dev-test-environment.md)
  
[<span data-ttu-id="de91c-231">Diretrizes de segurança da Microsoft para campanhas políticas, instituições sem fins lucrativos e outras organizações Agile</span><span class="sxs-lookup"><span data-stu-id="de91c-231">Microsoft Security Guidance for Political Campaigns, Nonprofits, and Other Agile Organizations</span></span>](microsoft-security-guidance-for-political-campaigns-nonprofits-and-other-agile-o.md)
  
[<span data-ttu-id="de91c-232">Adoção da nuvem e de soluções híbridas</span><span class="sxs-lookup"><span data-stu-id="de91c-232">Cloud adoption and hybrid solutions</span></span>](https://docs.microsoft.com/office365/enterprise/cloud-adoption-and-hybrid-solutions)


