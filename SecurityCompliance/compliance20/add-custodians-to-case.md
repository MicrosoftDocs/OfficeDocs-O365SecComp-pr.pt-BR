---
title: Adicionar os responsáveis a uma descoberta eletrônica avançada (visualização)
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: M365-security-compliance
search.appverid:
- MOE150
- MET150
ms.assetid: ''
description: ''
ms.openlocfilehash: fe208f4a9f7927d8481d5c6ec8b901baafb98626
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32243535"
---
# <a name="add-custodians-to-an-advanced-ediscovery-preview-case"></a><span data-ttu-id="e1ee9-102">Adicionar os responsáveis a uma descoberta eletrônica avançada (visualização)</span><span class="sxs-lookup"><span data-stu-id="e1ee9-102">Add custodians to an Advanced eDiscovery (Preview) case</span></span>

<span data-ttu-id="e1ee9-103">Usando a descoberta eletrônica avançada (versão prévia), você pode aproveitar a ferramenta de gerenciamento de responsáveis interno para coordenar seus fluxos de trabalho em torno do gerenciamento de responsáveis e identificando fontes de dados relevantes e de custodial em um caso.</span><span class="sxs-lookup"><span data-stu-id="e1ee9-103">Using Advanced eDiscovery (Preview), you can leverage the built-in custodian management tool to coordinate your workflows around managing custodians and identifying relevant, custodial data sources within a case.</span></span> <span data-ttu-id="e1ee9-104">Quando você adiciona um profissional, o sistema pode identificar automaticamente e colocar suspensões em sua caixa de correio principal do Exchange e no site do OneDrive for Business.</span><span class="sxs-lookup"><span data-stu-id="e1ee9-104">When you add a custodian, the system can automatically identify, and place holds on their primary Exchange mailbox and OneDrive for Business site.</span></span> <span data-ttu-id="e1ee9-105">Ao conduzir sua descoberta, você também pode descobrir e mapear caixas de correio ou sites adicionais que um acessado no passado ou nas equipes de que um responsáveis é membro de hoje.</span><span class="sxs-lookup"><span data-stu-id="e1ee9-105">As you conduct your discovery, you might also uncover and map additional mailboxes or sites that a custodian accessed in the past or Teams that a custodian is a member of today.</span></span>

<span data-ttu-id="e1ee9-106">Use o fluxo de trabalho a seguir para adicionar e gerenciar os responsáveis em casos de descoberta eletrônica avançada (visualização) no centro de conformidade do & de segurança.</span><span class="sxs-lookup"><span data-stu-id="e1ee9-106">Use the following workflow to add and manage custodians in Advanced eDiscovery (Preview) cases within the Security & Compliance Center.</span></span> 

![Guia gerenciamento de responsáveis](../media/CustodianMgtPage.png)


## <a name="step-1-identify-potential-custodians"></a><span data-ttu-id="e1ee9-108">Etapa 1: identificar possíveis responsáveis</span><span class="sxs-lookup"><span data-stu-id="e1ee9-108">Step 1: Identify potential custodians</span></span>

<span data-ttu-id="e1ee9-109">A primeira etapa é identificar os responsáveis apropriados para sua questão.</span><span class="sxs-lookup"><span data-stu-id="e1ee9-109">The first step is to identify the appropriate custodians for your matter.</span></span> <span data-ttu-id="e1ee9-110">Para adicionar os responsáveis a um caso, você deve ser membro do grupo de função gerenciadores de descoberta eletrônica ou administradores de descoberta eletrônica.</span><span class="sxs-lookup"><span data-stu-id="e1ee9-110">To add custodians to a case, you must be a member of the eDiscovery Managers or eDiscovery Admins role group.</span></span>   

![Identificar possíveis responsáveis](../media/AddCustodianStep1.png)

<span data-ttu-id="e1ee9-112">Para adicionar os responsáveis a uma descoberta eletrônica avançada existente (visualização):</span><span class="sxs-lookup"><span data-stu-id="e1ee9-112">To add custodians to an existing Advanced eDiscovery (Preview) case:</span></span>

1. <span data-ttu-id="e1ee9-113">Na página **descoberta eletrônica avançada (visualização)** , vá para o seu caso.</span><span class="sxs-lookup"><span data-stu-id="e1ee9-113">From the **Advanced eDiscovery (Preview)** page, go to your case.</span></span>
 
2. <span data-ttu-id="e1ee9-114">Depois de selecionar uma ocorrência, vá para a guia **responsáveis** e clique em **+ Adicionar**um.</span><span class="sxs-lookup"><span data-stu-id="e1ee9-114">After you have selected a case, go to the **Custodians** tab and click **+ Add Custodian**.</span></span> 
 
3. <span data-ttu-id="e1ee9-115">Escolha os responsáveis que você deseja adicionar à ocorrência.</span><span class="sxs-lookup"><span data-stu-id="e1ee9-115">Choose the custodians that you want to add to the case.</span></span> <span data-ttu-id="e1ee9-116">Você pode começar digitando para pesquisar e selecionar os usuários do Azure Active Directory da sua organização.</span><span class="sxs-lookup"><span data-stu-id="e1ee9-116">You can start by typing to search and select the users from your organization's Azure Active Directory.</span></span>
 
4. <span data-ttu-id="e1ee9-117">Depois de finalizar a lista de responsáveis, clique em **Avançar** para começar a identificar as fontes de dados potenciais.</span><span class="sxs-lookup"><span data-stu-id="e1ee9-117">After you have finalized the list of custodians, click **Next** to begin identifying potential data sources.</span></span> 
  
## <a name="optional-step-2-select-custodian-data-sources"></a><span data-ttu-id="e1ee9-118">Opcion Etapa 2: selecionar fontes de dados de responsáveis</span><span class="sxs-lookup"><span data-stu-id="e1ee9-118">(Optional) Step 2: Select custodian data sources</span></span>

<span data-ttu-id="e1ee9-119">Depois de adicionar os responsáveis a um caso, você pode aproveitar o Office 365 para ajudá-lo a identificar e preservar as fontes de dados dos responsáveis principais.</span><span class="sxs-lookup"><span data-stu-id="e1ee9-119">After you have added custodians to a case, you can leverage Office 365 to help you identify and preserve the primary custodian data sources.</span></span> <span data-ttu-id="e1ee9-120">A próxima etapa deste fluxo de trabalho é selecionar as fontes de dados de propriedade dos responsáveis especificados na etapa 1.</span><span class="sxs-lookup"><span data-stu-id="e1ee9-120">The next step in this workflow is to select the data sources owned by the custodians specified in Step 1.</span></span> 

![Selecionar fontes de dados do custodial](../media/AddCustodianStep2.png)

<span data-ttu-id="e1ee9-122">Para identificar as fontes de dados de responsáveis:</span><span class="sxs-lookup"><span data-stu-id="e1ee9-122">To identify custodian data sources:</span></span> 

1. <span data-ttu-id="e1ee9-123">Para cada pessoa, selecione **Exchange** se quiser que o sistema identifique automaticamente e adicione a caixa de correio principal do Exchange do responsáveis.</span><span class="sxs-lookup"><span data-stu-id="e1ee9-123">For each custodian, select **Exchange** if you would like the system to automatically identify and add the custodian's primary Exchange mailbox.</span></span> 
 
2. <span data-ttu-id="e1ee9-124">Para cada pessoa, selecione **onedrive** se quiser que o sistema identifique e adicione automaticamente a URL do onedrive principal do responsáveis.</span><span class="sxs-lookup"><span data-stu-id="e1ee9-124">For each custodian, select **OneDrive** if you would like the system to automatically identify and add the custodian's primary OneDrive URL.</span></span> 

    <span data-ttu-id="e1ee9-125">Após fazer suas seleções, o sistema tentará automaticamente identificar as fontes de dados e adicioná-las ao seu caso.</span><span class="sxs-lookup"><span data-stu-id="e1ee9-125">After you've made your selections, they system will automatically try to identify the data sources and add them to your case.</span></span>
 
4. <span data-ttu-id="e1ee9-126">Clique em **Avançar** para começar a mapear fontes de dados adicionais para seus responsáveis.</span><span class="sxs-lookup"><span data-stu-id="e1ee9-126">Click **Next** to begin mapping additional data sources to your custodian.</span></span>

## <a name="optional-step-3-map-additional-data-sources"></a><span data-ttu-id="e1ee9-127">Opcion Etapa 3: mapear fontes de dados adicionais</span><span class="sxs-lookup"><span data-stu-id="e1ee9-127">(Optional) Step 3: Map additional data sources</span></span>

<span data-ttu-id="e1ee9-128">Dependendo do seu caso, você também pode querer adicionar caixas de correio que um determinado participante possa ter usado no passado, grupos nos quais um responsáveis é um membro no momento ou sites aos quais os responsáveis tinham acesso no passado.</span><span class="sxs-lookup"><span data-stu-id="e1ee9-128">Depending on your case, you may also want to add mailboxes that a given custodian may have used in the past, groups where a custodian is currently a member, or sites that a custodian had access to in the past.</span></span> <span data-ttu-id="e1ee9-129">Além de fontes de dados principais responsáveis, você pode adicionar outras fontes de dados do Office 365 a um ou aproveitar o Office 365 para ajudá-lo também a identificar fontes de dados potencialmente relevantes.</span><span class="sxs-lookup"><span data-stu-id="e1ee9-129">In addition to primary custodian data sources, you can add additional Office 365 data sources to a custodian or leverage Office 365 to help you identify potentially relevant data sources as well.</span></span> 

![Mapear fontes de dados adicionais](../media/AddCustodianStep3.PNG)

<span data-ttu-id="e1ee9-131">Para mapear caixas de correio, sites ou equipes para um determinado local:</span><span class="sxs-lookup"><span data-stu-id="e1ee9-131">To map mailboxes, sites, or teams to a specific custodian:</span></span>
1. <span data-ttu-id="e1ee9-132">Selecione **Adicionar** para atribuir locais de conteúdo, como caixas de correio, sites e equipes, a um determinado local.</span><span class="sxs-lookup"><span data-stu-id="e1ee9-132">Select **Add** to assign content locations, like mailboxes, sites, and Teams, to a specific custodian.</span></span> 

2. <span data-ttu-id="e1ee9-133">No submenu, especifique o seguinte: ![mapear fontes de dados](../media/AddCustodianStep4.PNG)</span><span class="sxs-lookup"><span data-stu-id="e1ee9-133">In the flyout, specify the following: ![Map Data Sources](../media/AddCustodianStep4.PNG)</span></span>
  -  <span data-ttu-id="e1ee9-134">**Caixas de correio do Exchange** -clique em **escolher usuários, grupos ou equipes** e, em seguida, clique em **escolher usuários, grupos ou equipes** novamente.</span><span class="sxs-lookup"><span data-stu-id="e1ee9-134">**Exchange Mailboxes** - Click **Choose users, groups, or Teams** and then click **Choose users, groups, or teams** again.</span></span> <span data-ttu-id="e1ee9-135">Para especificar as caixas de correio a serem atribuídas aos responsáveis selecionados, use a caixa de pesquisa para localizar caixas de correio de usuário e grupos de distribuição.</span><span class="sxs-lookup"><span data-stu-id="e1ee9-135">To specify mailboxes to assign to the selected custodian, use the search box to find user mailboxes and distribution groups.</span></span> <span data-ttu-id="e1ee9-136">Você também pode atribuir a caixa de correio associada a um grupo do Office 365 ou a uma equipe da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="e1ee9-136">You can also assign the associated mailbox for an Office 365 Group or a Microsoft Team.</span></span> <span data-ttu-id="e1ee9-137">Marque a caixa de seleção usuário, grupo, equipe, clique em **escolher**e em **concluído**.</span><span class="sxs-lookup"><span data-stu-id="e1ee9-137">Select the user, group, team check box, click **Choose**, and then click **Done**.</span></span>

        > [!NOTE]
        > <span data-ttu-id="e1ee9-138">Ao clicar em escolher usuários, grupos ou equipes para especificar caixas de correio, o seletor de caixa de correio exibido estará vazio.</span><span class="sxs-lookup"><span data-stu-id="e1ee9-138">When you click Choose users, groups, or teams to specify mailboxes, the mailbox picker that's displayed is empty.</span></span> <span data-ttu-id="e1ee9-139">Isso foi desenvolvido para melhorar o desempenho.</span><span class="sxs-lookup"><span data-stu-id="e1ee9-139">This is by design to enhance performance.</span></span> <span data-ttu-id="e1ee9-140">Para adicionar pessoas a esta lista, digite um nome (no mínimo 3 caracteres) na caixa de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="e1ee9-140">To add people to this list, type a name (a minimum of 3 characters) in the search box.</span></span>
     
     - <span data-ttu-id="e1ee9-141">**Sites do SharePoint** -clique em **escolher sites** e, em seguida, clique em **escolher sites** novamente para especificar sites adicionais do SharePoint e do onedrive for Business que você gostaria de atribuir aos responsáveis selecionados.</span><span class="sxs-lookup"><span data-stu-id="e1ee9-141">**SharePoint Sites** - Click **Choose sites** and then click **Choose sites** again to specify additional SharePoint and OneDrive for Business sites that you would like to assign to the selected custodian.</span></span> <span data-ttu-id="e1ee9-142">Você também pode adicionar a URL do site do SharePoint para um grupo do Office 365 ou uma equipe da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="e1ee9-142">You can also add the URL for the SharePoint site for an Office 365 Group or a Microsoft Team.</span></span> <span data-ttu-id="e1ee9-143">Digite a URL de cada site que você deseja atribuir.</span><span class="sxs-lookup"><span data-stu-id="e1ee9-143">Type the URL for each site that you want to assign.</span></span> <span data-ttu-id="e1ee9-144">Clique em **escolher**e em **concluído**.</span><span class="sxs-lookup"><span data-stu-id="e1ee9-144">Click **Choose**, and then click **Done**.</span></span>
     - <span data-ttu-id="e1ee9-145">**Microsoft Teams** – clique em **escolher equipes** e, em seguida, clique em **escolher Teams** novamente para exibir uma lista de grupos do Microsoft Team nos quais o responsáveis é membro de hoje.</span><span class="sxs-lookup"><span data-stu-id="e1ee9-145">**Microsoft Teams** – Click **Choose Teams** and then click **Choose Teams** again to view a list of Microsoft Team groups that the custodian is a member of today.</span></span> <span data-ttu-id="e1ee9-146">Selecione as equipes que você gostaria de adicionar a seus responsáveis.</span><span class="sxs-lookup"><span data-stu-id="e1ee9-146">Select the Teams that you would like to add to your custodian.</span></span> <span data-ttu-id="e1ee9-147">Depois de selecionado, o sistema identificará automaticamente o & selecione o site do SharePoint associado e a caixa de correio de grupo associados a essa equipe da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="e1ee9-147">Once selected, the system will automatically identify & select the associated SharePoint site and Group Mailbox associated to that Microsoft Team.</span></span> <span data-ttu-id="e1ee9-148">Clique em **escolher**e em **concluído**.</span><span class="sxs-lookup"><span data-stu-id="e1ee9-148">Click **Choose**, and then click **Done**.</span></span>
        
      > [!NOTE]
      > <span data-ttu-id="e1ee9-149">Para adicionar outras Teams da Microsoft, você precisará adicionar separadamente a caixa de correio e o site do SharePoint, conforme mostrado acima.</span><span class="sxs-lookup"><span data-stu-id="e1ee9-149">To add additional Microsoft Teams, you will need to separately add the mailbox and SharePoint site as shown above.</span></span>

<span data-ttu-id="e1ee9-150">Após concluir o mapeamento de suas fontes, você poderá exibir as caixas de correio de total, sites e equipes para os responsáveis que você acabou de adicionar.</span><span class="sxs-lookup"><span data-stu-id="e1ee9-150">After you have finished mapping your sources, you can view the total mailboxes, sites, and Teams for the custodians that you have just added.</span></span> <span data-ttu-id="e1ee9-151">Depois de finalizar as fontes de dados relevantes para um determinado, esse mapeamento será mantido e estendido para os fluxos de trabalho de coleta de descoberta eletrônica, processamento e revisão.</span><span class="sxs-lookup"><span data-stu-id="e1ee9-151">When you've finalized the data sources relevant for a specific custodian, this mapping will be maintained and extended to the eDiscovery collection, processing, and review workflows.</span></span> 

## <a name="optional-step-4-place-custodians-on-hold"></a><span data-ttu-id="e1ee9-152">Opcion Etapa 4: colocar os responsáveis em espera</span><span class="sxs-lookup"><span data-stu-id="e1ee9-152">(Optional) Step 4: Place custodians on hold</span></span>

![Colocar suspensões](../media/AddCustodianStep5.PNG)

<span data-ttu-id="e1ee9-154">Depois de finalizar os responsáveis e as fontes de dados que você deseja adicionar ao seu caso, você pode, opcionalmente, colocar alguns ou todos os seus responsáveis em espera.</span><span class="sxs-lookup"><span data-stu-id="e1ee9-154">After you have finalized the custodians and data sources that you would like to add to your case, you can optionally place some or all of your custodians on hold.</span></span> <span data-ttu-id="e1ee9-155">Quando você coloca um bloqueador, o conteúdo mapeado para esse usuário é mantido até que você libere os responsáveis do caso ou até que a retenção seja excluída.</span><span class="sxs-lookup"><span data-stu-id="e1ee9-155">When you place a custodian on hold, the content mapped to that user is held until you release the custodian from the case or until you delete the hold.</span></span> <span data-ttu-id="e1ee9-156">Em alguns casos, talvez você queira adicionar os responsáveis por um caso sem colocá-los em espera.</span><span class="sxs-lookup"><span data-stu-id="e1ee9-156">In some cases, you may want to add custodians to a case without placing them on hold.</span></span> 

<span data-ttu-id="e1ee9-157">Para colocar os responsáveis e as fontes de dados selecionados em retenção:</span><span class="sxs-lookup"><span data-stu-id="e1ee9-157">To place the selected custodians and data sources on hold:</span></span>

1. <span data-ttu-id="e1ee9-158">Verifique as seleções dos seus responsáveis e marque a caixa de seleção para colocar cada um em espera.</span><span class="sxs-lookup"><span data-stu-id="e1ee9-158">Verify your custodian selections and select the checkbox to place each custodian on hold.</span></span> <span data-ttu-id="e1ee9-159">Depois que um Objectfor colocado em espera, uma política de retenção de responsáveis contendo todas as fontes de custodial será criada automaticamente.</span><span class="sxs-lookup"><span data-stu-id="e1ee9-159">After a custodian is placed on hold, a custodian hold policy containing all custodial sources will be automatically created.</span></span> <span data-ttu-id="e1ee9-160">Se a opção não for selecionada, os responsáveis e as fontes de dados selecionadas serão adicionados ao caso, mas o conteúdo não será preservado.</span><span class="sxs-lookup"><span data-stu-id="e1ee9-160">If the option is not checked, the custodian and selected data sources will be added to the case but the content will not be preserved.</span></span>

2. <span data-ttu-id="e1ee9-161">Vá até a guia **isenções** e selecione a **política de retenção de responsáveis**.</span><span class="sxs-lookup"><span data-stu-id="e1ee9-161">Go to the **Holds** tab and select the **Custodian Hold Policy**.</span></span> 

3. <span data-ttu-id="e1ee9-162">Clique em **Editar** para exibir todas as fontes de dados do responsáveis.</span><span class="sxs-lookup"><span data-stu-id="e1ee9-162">Click **Edit** to view all the selected custodian data sources.</span></span>

   
