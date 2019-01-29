---
title: Adicionar responsáveis a um caso de eDiscovery avançado (Preview)
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
ms.collection: ''
search.appverid:
- MOE150
- MET150
ms.assetid: ''
description: ''
ms.openlocfilehash: d9a7dc6b1c2eeffdcd49be64d1d09d4a2bda782b
ms.sourcegitcommit: ee28ee2b2bdfd049333c2f495d7f7780d13af4a6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2019
ms.locfileid: "29607349"
---
# <a name="add-custodians-to-an-advanced-ediscovery-preview-case"></a><span data-ttu-id="312f7-102">Adicionar responsáveis a um eDiscovery avançado (Preview) caso</span><span class="sxs-lookup"><span data-stu-id="312f7-102">Add custodians to an Advanced eDiscovery (Preview) Case</span></span>

<span data-ttu-id="312f7-p101">Usando o eDiscovery avançado (Preview), você pode aproveitar a ferramenta de gerenciamento dos responsáveis internas para coordenar os fluxos de trabalho em torno Gerenciando responsáveis e identificar as fontes de dados relevantes, custódia dentro de um caso. Quando você adiciona um funcionário encarregado, o sistema pode identificar automaticamente e retenções locais em sua caixa de correio principal do Exchange e OneDrive para o site de negócios. Conforme você conduzir sua descoberta, você pode descobrir e mapear caixas de correio adicionais ou sites que um funcionário encarregado acessado no passado ou equipes que um funcionário encarregado é um membro de hoje.</span><span class="sxs-lookup"><span data-stu-id="312f7-p101">Using Advanced eDiscovery (Preview), you can leverage the built-in custodian management tool to coordinate your workflows around managing custodians and identifying relevant, custodial data sources within a case. When you add a custodian, the system can automatically identify, and place holds on their primary Exchange mailbox and OneDrive for Business site. As you conduct your discovery, you might also uncover and map additional mailboxes or sites that a custodian accessed in the past or Teams that a custodian is a member of today.</span></span>

<span data-ttu-id="312f7-106">Use o seguinte fluxo de trabalho para adicione e gerencie responsáveis em casos de eDiscovery avançado (Preview) dentro do Centro de conformidade do & de segurança.</span><span class="sxs-lookup"><span data-stu-id="312f7-106">Use the following workflow to add and manage custodians in Advanced eDiscovery (Preview) cases within the Security & Compliance Center.</span></span> 

## <a name="step-1-identify-potential-custodians"></a><span data-ttu-id="312f7-107">Etapa 1: Identificar potenciais responsáveis</span><span class="sxs-lookup"><span data-stu-id="312f7-107">Step 1: Identify potential custodians</span></span>

<span data-ttu-id="312f7-p102">A primeira etapa é identificar os responsáveis apropriados para sua questão. Para adicionar responsáveis a um caso, você deve ser um membro do gerentes de descoberta eletrônica ou um grupo de função de administradores de descoberta eletrônica.</span><span class="sxs-lookup"><span data-stu-id="312f7-p102">The first step is to identify the appropriate custodians for your matter. To add custodians to a case, you must be a member of the eDiscovery Managers or eDiscovery Admins role group.</span></span>   

<span data-ttu-id="312f7-110">Para adicionar responsáveis a um caso de eDiscovery avançado (Preview) existente:</span><span class="sxs-lookup"><span data-stu-id="312f7-110">To add custodians to an existing Advanced eDiscovery (Preview) case:</span></span>

1. <span data-ttu-id="312f7-111">Na página **eDiscovery avançado (Preview)** , vá para o seu caso.</span><span class="sxs-lookup"><span data-stu-id="312f7-111">From the **Advanced eDiscovery (Preview)** page, go to your case.</span></span>
 
2. <span data-ttu-id="312f7-112">Depois de ter selecionado um caso, vá para a guia **responsáveis** e clique em **+ dos responsáveis a adicionar**.</span><span class="sxs-lookup"><span data-stu-id="312f7-112">After you have selected a case, go to the **Custodians** tab and click **+ Add Custodian**.</span></span> 
 
3. <span data-ttu-id="312f7-p103">Escolha os responsáveis que você deseja adicionar ao caso. Você pode iniciar digitando para pesquisar e selecione os usuários Azure Active Directory da sua organização.</span><span class="sxs-lookup"><span data-stu-id="312f7-p103">Choose the custodians that you want to add to the case. You can start by typing to search and select the users from your organization's Azure Active Directory.</span></span>
 
4. <span data-ttu-id="312f7-115">Depois de finalizar a lista dos responsáveis, clique em **Avançar** para começar a identificar possíveis fontes de dados.</span><span class="sxs-lookup"><span data-stu-id="312f7-115">After you have finalized the list of custodians, click **Next** to begin identifying potential data sources.</span></span> 
   
## <a name="optional-step-2-select-custodian-data-sources"></a><span data-ttu-id="312f7-116">(Opcional) Etapa 2: Selecionar fontes de dados dos responsáveis</span><span class="sxs-lookup"><span data-stu-id="312f7-116">(Optional) Step 2: Select custodian data sources</span></span>

<span data-ttu-id="312f7-p104">Após ter adicionado responsáveis a um caso, você pode aproveitar o Office 365 para ajudá-lo a identificar e preservar as fontes de dados dos responsáveis principal. A próxima etapa neste fluxo de trabalho é selecionar as fontes de dados pertencentes as responsáveis especificados na etapa 1.</span><span class="sxs-lookup"><span data-stu-id="312f7-p104">After you have added custodians to a case, you can leverage Office 365 to help you identify and preserve the primary custodian data sources. The next step in this workflow is to select the data sources owned by the custodians specified in Step 1.</span></span> 

<span data-ttu-id="312f7-119">Para identificar as fontes de dados dos responsáveis:</span><span class="sxs-lookup"><span data-stu-id="312f7-119">To identify custodian data sources:</span></span> 

1. <span data-ttu-id="312f7-120">Para cada responsável, selecione **Exchange** se você quiser a identificar automaticamente e adicionar principal Exchange da caixa de correio do dos responsáveis do sistema.</span><span class="sxs-lookup"><span data-stu-id="312f7-120">For each custodian, select **Exchange** if you would like the system to automatically identify and add the custodian's primary Exchange mailbox.</span></span> 
 
2. <span data-ttu-id="312f7-121">Para cada responsável, selecione **OneDrive** se você quiser a identificar automaticamente e Adicionar URL principal do dos responsáveis do OneDrive do sistema.</span><span class="sxs-lookup"><span data-stu-id="312f7-121">For each custodian, select **OneDrive** if you would like the system to automatically identify and add the custodian's primary OneDrive URL.</span></span> 

    <span data-ttu-id="312f7-122">Depois de fazer suas seleções, eles sistema tentará automaticamente identificar as fontes de dados e adicioná-los ao seu caso.</span><span class="sxs-lookup"><span data-stu-id="312f7-122">After you've made your selections, they system will automatically try to identify the data sources and add them to your case.</span></span>
 
4. <span data-ttu-id="312f7-123">Clique em **Avançar** para iniciar o mapeamento de fontes de dados adicionais para seu dos responsáveis.</span><span class="sxs-lookup"><span data-stu-id="312f7-123">Click **Next** to begin mapping additional data sources to your custodian.</span></span>

## <a name="optional-step-3-map-additional-data-sources"></a><span data-ttu-id="312f7-124">(Opcional) Etapa 3: Mapear fontes de dados adicionais</span><span class="sxs-lookup"><span data-stu-id="312f7-124">(Optional) Step 3: Map additional data sources</span></span>

<span data-ttu-id="312f7-p105">Dependendo do seu caso, você talvez queira adicionar caixas de correio que dos responsáveis determinado podem ter usado no passado, grupos em que um funcionário encarregado é membro atualmente ou sites que um funcionário encarregado tinha acesso a no passado. Além das fontes de dados dos responsáveis principal, pode adicionar fontes de dados adicionais do Office 365 a dos responsáveis ou aproveitar o Office 365 para ajudá-lo a identificar fontes de dados relevantes potencialmente também.</span><span class="sxs-lookup"><span data-stu-id="312f7-p105">Depending on your case, you may also want to add mailboxes that a given custodian may have used in the past, groups where a custodian is currently a member, or sites that a custodian had access to in the past. In addition to primary custodian data sources, you can add additional Office 365 data sources to a custodian or leverage Office 365 to help you identify potentially relevant data sources as well.</span></span> 

<span data-ttu-id="312f7-127">Para mapear as equipes, sites ou caixas de correio para dos responsáveis específico:</span><span class="sxs-lookup"><span data-stu-id="312f7-127">To map mailboxes, sites, or teams to a specific custodian:</span></span>
1. <span data-ttu-id="312f7-128">Selecione a **atualização** para atribuir os locais de conteúdo, como caixas de correio, sites e equipes, a dos responsáveis específico.</span><span class="sxs-lookup"><span data-stu-id="312f7-128">Select **Update** to assign content locations, like mailboxes, sites, and Teams, to a specific custodian.</span></span> 

2. <span data-ttu-id="312f7-129">No submenu, especifique o seguinte:</span><span class="sxs-lookup"><span data-stu-id="312f7-129">In the flyout, specify the following:</span></span>
   
  -  <span data-ttu-id="312f7-p106">**Caixas de correio do Exchange** - clique em **Escolher usuários, grupos ou equipes** e, em seguida, clique em **Escolher usuários, grupos ou equipes** novamente. Para especificar as caixas de correio para atribuir ao dos responsáveis selecionado, use a caixa Pesquisar para localizar caixas de correio de usuário e grupos de distribuição. Você também pode atribuir a caixa de correio associada para um Team Microsoft ou de um grupo do Office 365. Selecione o usuário, grupo, caixa de seleção de equipe, clique em **Escolher**e, em seguida, clique em **concluído**.</span><span class="sxs-lookup"><span data-stu-id="312f7-p106">**Exchange Mailboxes** - Click **Choose users, groups, or Teams** and then click **Choose users, groups, or teams** again. To specify mailboxes to assign to the selected custodian, use the search box to find user mailboxes and distribution groups. You can also assign the associated mailbox for an Office 365 Group or a Microsoft Team. Select the user, group, team check box, click **Choose**, and then click **Done**.</span></span>

      > [!NOTE]
      > <span data-ttu-id="312f7-p107">Quando você clica em usuários, grupos ou equipes escolher para especificar as caixas de correio, o seletor de caixa de correio que é exibido está vazio. Isso ocorre por design para aprimorar o desempenho. Para adicionar pessoas a essa lista, digite um nome (um mínimo de 3 caracteres) na caixa Pesquisar.</span><span class="sxs-lookup"><span data-stu-id="312f7-p107">When you click Choose users, groups, or teams to specify mailboxes, the mailbox picker that's displayed is empty. This is by design to enhance performance. To add people to this list, type a name (a minimum of 3 characters) in the search box.</span></span>
     
   - <span data-ttu-id="312f7-p108">**Sites do SharePoint** - clique em **sites de escolha** e clique em **Escolher sites** novamente para especificar o SharePoint e OneDrive adicionais para sites corporativos que você gostaria de atribuir para dos responsáveis selecionado. Você também pode adicionar a URL do site do SharePoint para um Team Microsoft ou de um grupo do Office 365. Digite a URL para cada site que você deseja atribuir. Clique em **Escolher**e, em seguida, clique em **concluído**.</span><span class="sxs-lookup"><span data-stu-id="312f7-p108">**SharePoint Sites** - Click **Choose sites** and then click **Choose sites** again to specify additional SharePoint and OneDrive for Business sites that you would like to assign to the selected custodian. You can also add the URL for the SharePoint site for an Office 365 Group or a Microsoft Team. Type the URL for each site that you want to assign. Click **Choose**, and then click **Done**.</span></span>
   - <span data-ttu-id="312f7-p109">**As equipes da Microsoft** – clique em **Escolher equipes** e clique em **Escolher equipes** novamente para exibir uma lista de grupos de Microsoft Team que dos responsáveis é um membro de hoje. Selecione as equipes que você gostaria de adicionar à sua dos responsáveis. Uma vez selecionado, o sistema automaticamente identificará selecionar & que o site do SharePoint associado e a caixa de correio de grupo associado a esse Team Microsoft. Clique em **Escolher**e, em seguida, clique em **concluído**.</span><span class="sxs-lookup"><span data-stu-id="312f7-p109">**Microsoft Teams** – Click **Choose Teams** and then click **Choose Teams** again to view a list of Microsoft Team groups that the custodian is a member of today. Select the Teams that you would like to add to your custodian. Once selected, the system will automatically identify & select the associated SharePoint site and Group Mailbox associated to that Microsoft Team. Click **Choose**, and then click **Done**.</span></span>
        
      > [!NOTE]
      > <span data-ttu-id="312f7-145">Para adicionar Teams adicionais da Microsoft, você precisará adicionar separadamente a caixa de correio e o site do SharePoint, como mostrado acima.</span><span class="sxs-lookup"><span data-stu-id="312f7-145">To add additional Microsoft Teams, you will need to separately add the mailbox and SharePoint site as shown above.</span></span>

<span data-ttu-id="312f7-p110">Depois de concluir o mapeamento de suas fontes, você poderá exibir as caixas de correio total, sites e equipes para os responsáveis que você acabou de adicionar. Quando tiver finalizado as fontes de dados relevantes para dos responsáveis específico, esse mapeamento será mantido e estendido até o conjunto de descoberta eletrônica, processamento e fluxos de trabalho de revisão.</span><span class="sxs-lookup"><span data-stu-id="312f7-p110">After you have finished mapping your sources, you can view the total mailboxes, sites, and Teams for the custodians that you have just added. When you've finalized the data sources relevant for a specific custodian, this mapping will be maintained and extended to the eDiscovery collection, processing, and review workflows.</span></span> 

## <a name="optional-step-4-place-custodians-on-hold"></a><span data-ttu-id="312f7-148">(Opcional) Etapa 4: Local responsáveis em espera</span><span class="sxs-lookup"><span data-stu-id="312f7-148">(Optional) Step 4: Place custodians on hold</span></span>

 <span data-ttu-id="312f7-p111">Depois de finalizar os responsáveis e as fontes de dados que você gostaria de adicionar ao seu caso, opcionalmente, você pode colocar alguns ou todos os seus responsáveis em espera. Quando você realiza um funcionário encarregado em espera, o conteúdo mapeado para o usuário será retido até que você libere dos responsáveis do gabinete ou até que você exclua isenção. Em alguns casos, convém adicionar responsáveis a um caso sem colocá-los em espera.</span><span class="sxs-lookup"><span data-stu-id="312f7-p111">After you have finalized the custodians and data sources that you would like to add to your case, you can optionally place some or all of your custodians on hold. When you place a custodian on hold, the content mapped to that user is held until you release the custodian from the case or until you delete the hold. In some cases, you may want to add custodians to a case without placing them on hold.</span></span> 

<span data-ttu-id="312f7-152">Para colocar as origens selecionadas responsáveis e dados em espera:</span><span class="sxs-lookup"><span data-stu-id="312f7-152">To place the selected custodians and data sources on hold:</span></span>

1. <span data-ttu-id="312f7-p112">Verifique suas seleções dos responsáveis e selecione o checkox para colocar cada responsável em espera. Depois que um funcionário encarregado é colocado em espera, uma política de retenção dos responsáveis contendo custódia todas as fontes será criada automaticamente. Se a opção não estiver marcada, as fontes de dados dos responsáveis & selecionada serão adicionadas ao caso, mas o conteúdo não será preservado.</span><span class="sxs-lookup"><span data-stu-id="312f7-p112">Verify your custodian selections and select the checkox to place each custodian on hold.Once a custodian is placed on hold, a custodian hold policy containing all custodial sources will automatically be created. If the option is not checked, the custodian & selected data sources will be added to the case but the content will not be preserved.</span></span>

2. <span data-ttu-id="312f7-155">Vá para a guia **contém** e selecione a **Política de retenção dos responsáveis**.</span><span class="sxs-lookup"><span data-stu-id="312f7-155">Go to the **Holds** tab and select the **Custodian Hold Policy**.</span></span> 

3. <span data-ttu-id="312f7-156">Clique em **Editar** para exibir todas as fontes de dados dos responsáveis selecionado.</span><span class="sxs-lookup"><span data-stu-id="312f7-156">Click **Edit** to view all the selected custodian data sources.</span></span>
