---
title: Gerenciar os responsáveis em um caso de descoberta eletrônica avançada (visualização)
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
ms.openlocfilehash: 6a21240f71c64f244ee42c3d3a2ed9d75381edaa
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32241828"
---
# <a name="manage-custodians-in-an-advanced-ediscovery-preview-case"></a><span data-ttu-id="f488e-102">Gerenciar os responsáveis em um caso de descoberta eletrônica avançada (visualização)</span><span class="sxs-lookup"><span data-stu-id="f488e-102">Manage custodians in an Advanced eDiscovery (Preview) case</span></span>

<span data-ttu-id="f488e-103">A guia responsáveis contém uma lista classificável de todos os responsáveis da ocorrência.</span><span class="sxs-lookup"><span data-stu-id="f488e-103">The Custodians tab contains a sortable list of all the custodians in the case.</span></span> <span data-ttu-id="f488e-104">Após adicionar os responsáveis a um caso, os detalhes sobre cada um serão automaticamente coletados do Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="f488e-104">After you add custodians to a case, details about each custodian will automatically be collected from Azure Active Directory.</span></span>

![Gerenciar responsáveis](../media/CustodianDetails.PNG)

## <a name="viewing-custodian-details"></a><span data-ttu-id="f488e-106">Exibindo detalhes do responsáveis</span><span class="sxs-lookup"><span data-stu-id="f488e-106">Viewing custodian details</span></span>

<span data-ttu-id="f488e-107">A página de menu que contém os detalhes dos responsáveis é exibida após você adicionar um dos responsáveis a um caso e selecioná-los na lista da guia **responsáveis** . A partir daqui, você pode exibir todos os detalhes relacionados a esses responsáveis.</span><span class="sxs-lookup"><span data-stu-id="f488e-107">The flyout page that contains custodian details appears after you add a custodian to a case and select them from the list on the **Custodians** tab. From here, you can view all the details related to that custodian.</span></span> <span data-ttu-id="f488e-108">A página de submenu contém os seguintes campos:</span><span class="sxs-lookup"><span data-stu-id="f488e-108">The flyout page contains the following fields:</span></span>

- <span data-ttu-id="f488e-109">Informações de contato</span><span class="sxs-lookup"><span data-stu-id="f488e-109">Contact information</span></span>

  - <span data-ttu-id="f488e-110">**Nome para exibição**: o nome exibido no catálogo de endereços para os responsáveis.</span><span class="sxs-lookup"><span data-stu-id="f488e-110">**Display Name**: The name displayed in the address book for the custodian.</span></span> <span data-ttu-id="f488e-111">Geralmente, é a combinação do nome do responsáveis, inicial e sobrenome do meio.</span><span class="sxs-lookup"><span data-stu-id="f488e-111">This is usually the combination of the custodian’s first name, middle initial and last name.</span></span>
  - <span data-ttu-id="f488e-112">**Mail/SMTP**: o endereço SMTP para os responsáveis, por exemplo, Jeff@contoso.onmicrosoft.com.</span><span class="sxs-lookup"><span data-stu-id="f488e-112">**Mail/SMTP**: The SMTP address for the custodian, for example, jeff@contoso.onmicrosoft.com.</span></span>  
  - <span data-ttu-id="f488e-113">**Título**: o cargo do profissional.</span><span class="sxs-lookup"><span data-stu-id="f488e-113">**Title**: The custodian’s job title.</span></span>
  - <span data-ttu-id="f488e-114">**Departamento**: o nome do departamento no qual os responsáveis funciona.</span><span class="sxs-lookup"><span data-stu-id="f488e-114">**Department**: The name for the department in which the custodian works.</span></span>
  - <span data-ttu-id="f488e-115">**Gerente**: gerente do responsáveis.</span><span class="sxs-lookup"><span data-stu-id="f488e-115">**Manager**: The custodian’s manager.</span></span> <span data-ttu-id="f488e-116">O gerente designado receberá qualquer comunicação de escalonamento para este responsáveis.</span><span class="sxs-lookup"><span data-stu-id="f488e-116">The designated manager will receive any Escalation communications for this custodian.</span></span>
  
- <span data-ttu-id="f488e-117">Informações de local</span><span class="sxs-lookup"><span data-stu-id="f488e-117">Location information</span></span>

  - <span data-ttu-id="f488e-118">**Cidade**: a cidade na qual o responsáveis está localizado.</span><span class="sxs-lookup"><span data-stu-id="f488e-118">**City**: The city in which the custodian is located.</span></span>
  - <span data-ttu-id="f488e-119">**Estado**: o estado ou província no endereço do responsáveis.</span><span class="sxs-lookup"><span data-stu-id="f488e-119">**State**: The state or province in the custodian’s address.</span></span>
  - <span data-ttu-id="f488e-120">**País/região**: o país/região no qual o responsáveis está localizado; por exemplo, "US" ou "ru".</span><span class="sxs-lookup"><span data-stu-id="f488e-120">**Country/Region**: The country/region in which the custodian’s is located; for example, “US” or “UK”.</span></span>
  - <span data-ttu-id="f488e-121">**Office**: o local do escritório no local de trabalho do responsáveis.</span><span class="sxs-lookup"><span data-stu-id="f488e-121">**Office**: The office location in the custodian’s place of business.</span></span>

- <span data-ttu-id="f488e-122">Informações sobre o caso</span><span class="sxs-lookup"><span data-stu-id="f488e-122">Case information</span></span>

  - <span data-ttu-id="f488e-123">**Status de espera**: indica se os responsáveis foram colocados em espera.</span><span class="sxs-lookup"><span data-stu-id="f488e-123">**Hold status**: Indicates if the custodian has been placed on hold.</span></span> 
  - <span data-ttu-id="f488e-124">**Status de Comunicação**: indica se os responsáveis foram emitidos um aviso de espera.</span><span class="sxs-lookup"><span data-stu-id="f488e-124">**Communication status**: Indicates if the custodian has been issued a hold notice.</span></span> <span data-ttu-id="f488e-125">Se o objecttiver sido emitido um aviso, ele será marcado como *publicado*.</span><span class="sxs-lookup"><span data-stu-id="f488e-125">If the custodian has been issued a notice, then this will be marked as *Published*.</span></span> <span data-ttu-id="f488e-126">Se não tiver sido emitido um aviso para os responsáveis, este status será canCelado. \*\*</span><span class="sxs-lookup"><span data-stu-id="f488e-126">If the custodian has not been issued a notice, then this status will be *Un-Published*.</span></span> 
  - <span data-ttu-id="f488e-127">**Status**: o status dos responsáveis dentro do caso.</span><span class="sxs-lookup"><span data-stu-id="f488e-127">**Status**: The status of the custodian within the case.</span></span> <span data-ttu-id="f488e-128">Isso estará *ativo* se os responsáveis ainda estiverem em espera para o caso.</span><span class="sxs-lookup"><span data-stu-id="f488e-128">This will be *Active* if the custodian is still on hold for the case.</span></span> <span data-ttu-id="f488e-129">Se um responsáveis for removido de uma ocorrência, seu status será alterado para *liberado*.</span><span class="sxs-lookup"><span data-stu-id="f488e-129">If a custodian is removed from a case, their status will change to *Released*.</span></span> 

- <span data-ttu-id="f488e-130">Status de processamento</span><span class="sxs-lookup"><span data-stu-id="f488e-130">Processing status</span></span>

  - <span data-ttu-id="f488e-131">**Status**de indexação: indica o status do trabalho de indexação profunda.</span><span class="sxs-lookup"><span data-stu-id="f488e-131">**Indexing status**: Indicates the status of the deep indexing job.</span></span>  
  - <span data-ttu-id="f488e-132">**Hora da última atualização**da indexação: indica o dateStamp de quando o trabalho de indexação profunda foi disparado pela última vez.</span><span class="sxs-lookup"><span data-stu-id="f488e-132">**Indexing Last Updated Time**: Indicates the datestamp of when the deep indexing job was last triggered.</span></span>
  - <span data-ttu-id="f488e-133">**Fontes de dados**: mostra a contagem de caixas de correio, sites e equipes que foram selecionadas para os responsáveis.</span><span class="sxs-lookup"><span data-stu-id="f488e-133">**Data sources**: Shows the count of mailboxes, sites, and Teams that have been selected for the custodian.</span></span>

## <a name="editing-a-custodian"></a><span data-ttu-id="f488e-134">Edição de um responsáveis</span><span class="sxs-lookup"><span data-stu-id="f488e-134">Editing a custodian</span></span>

<span data-ttu-id="f488e-135">À medida que seu caso avança, você pode descobrir que pode haver fontes de dados adicionais relevantes para um determinado & de seu caso.</span><span class="sxs-lookup"><span data-stu-id="f488e-135">As your case progresses, you may discover that there may be additional data sources relevant to a specific custodian & your case.</span></span> <span data-ttu-id="f488e-136">Em outros cenários, talvez você queira remover determinadas fontes de dados que foram revisadas e consideradas não relevantes.</span><span class="sxs-lookup"><span data-stu-id="f488e-136">In other scenarios, you may want to remove certain data sources that have been reviewed and deemed as not relevant.</span></span>

<span data-ttu-id="f488e-137">Para atualizar um Objecte as fontes de dados selecionadas:</span><span class="sxs-lookup"><span data-stu-id="f488e-137">To update a custodian and the selected data sources:</span></span>

1. <span data-ttu-id="f488e-138">Selecione um caso existente na **descoberta eletrônica avançada do > de descoberta eletrônica (visualização)**.</span><span class="sxs-lookup"><span data-stu-id="f488e-138">Select an existing case from the **eDiscovery > Advanced eDiscovery (Preview)**.</span></span>
  
2. <span data-ttu-id="f488e-139">No caso, clique na guia **responsáveis** .</span><span class="sxs-lookup"><span data-stu-id="f488e-139">In the case, click the **Custodians** tab.</span></span>
  
3. <span data-ttu-id="f488e-140">Selecione os responsáveis (s) na lista e clique em **Editar fontes**.</span><span class="sxs-lookup"><span data-stu-id="f488e-140">Select the custodian(s) from the list and click **Edit sources**.</span></span>

    ![Editar fontes de dados](../media/EditCustodianDataSource.PNG)
  
4. <span data-ttu-id="f488e-142">Atualize as seleções para os locais do Exchange e do OneDrive clicando em **escolher fontes de dados**.</span><span class="sxs-lookup"><span data-stu-id="f488e-142">Update selections for Exchange and OneDrive locations by clicking **Choose data sources**.</span></span>
  
5. <span data-ttu-id="f488e-143">Adicione ou remova as caixas de correio do Teams, SharePoint ou Exchange mapeadas ao usuário clicando para **selecionar outras fontes de dados**.</span><span class="sxs-lookup"><span data-stu-id="f488e-143">Add or remove Teams, SharePoint, or Exchange mailboxes mapped the user by clicking to **Select additional data sources**.</span></span> <span data-ttu-id="f488e-144">Para obter mais informações sobre como mapear fontes de dados para um dos responsáveis, confira [Adicionar responsáveis a um caso](add-custodians-to-case.md).</span><span class="sxs-lookup"><span data-stu-id="f488e-144">For more information about how you to map data sources to a custodian, see [Add custodians to a case](add-custodians-to-case.md).</span></span>
  
6. <span data-ttu-id="f488e-145">Para atualizar o status de retenção de responsáveis, clique em **colocar custodial isenções**e habilite ou desabilite a retenção para os responsáveis.</span><span class="sxs-lookup"><span data-stu-id="f488e-145">To update the custodian hold status, click **Place custodial holds**, and enable or disable the hold for custodians.</span></span>

> [!TIP]
> <span data-ttu-id="f488e-146">Você pode selecionar vários responsáveis para executar ações em massa, como reindexação, liberação ou edição de um conjunto de responsáveis.</span><span class="sxs-lookup"><span data-stu-id="f488e-146">You can select multiple custodians to perform bulk actions, like re-indexing, releasing, or editing a set of custodians.</span></span>

## <a name="resolving-custodian-processing-errors"></a><span data-ttu-id="f488e-147">Resolvendo erros de processamento de responsáveis</span><span class="sxs-lookup"><span data-stu-id="f488e-147">Resolving custodian processing errors</span></span>

<span data-ttu-id="f488e-148">Na maioria dos fluxos de trabalho jurídicos, após a adição de responsáveis por uma investigação específica, um subconjunto dos dados dos usuários será pesquisado.</span><span class="sxs-lookup"><span data-stu-id="f488e-148">In most Legal workflows, after custodians are added for a specific investigation, a subset of the users’ data will be searched.</span></span> <span data-ttu-id="f488e-149">Devido a grandes tamanhos de arquivo ou possíveis danos, alguns itens dentro das fontes de dados dos responsáveis podem ser parcialmente indexados.</span><span class="sxs-lookup"><span data-stu-id="f488e-149">Due to large file sizes or possible corruption, some items within the custodians’ data sources may be partially indexed.</span></span> <span data-ttu-id="f488e-150">Usando o recurso de indexação avançada de descoberta eletrônica avançada (visualização), esses itens parcialmente indexados podem ser corrigidos automaticamente por meio de um novo rastreamento e re-indexação desses itens sob demanda.</span><span class="sxs-lookup"><span data-stu-id="f488e-150">Using the Advanced eDiscovery (Preview) deep indexing capability, these partially indexed items can be automatically remediated by re-crawling and re-indexing these items on demand.</span></span> 

<span data-ttu-id="f488e-151">Quando um usuário é adicionado a uma ocorrência, seus dados serão automaticamente "indexados em profundidade", permitindo que os usuários deixem esses itens parcialmente indexados em vez de terem que baixar, corrigir e executar novamente as pesquisas fora do Office 365.</span><span class="sxs-lookup"><span data-stu-id="f488e-151">When a custodian is added to a case, their data will automatically be "deep indexed”, allowing users to leave these partially indexed items in place instead of having to download, remediate and re-run searches outside of Office 365.</span></span> <span data-ttu-id="f488e-152">Durante o ciclo de vida de um caso, um usuário pode corrigir itens ou adicionar novas fontes de dados para um determinado usuário.</span><span class="sxs-lookup"><span data-stu-id="f488e-152">During the lifecycle of a case, a user may remediate items or add new data sources for a given custodian.</span></span> <span data-ttu-id="f488e-153">Isso pode exigir que o índice de responsáveis seja atualizado.</span><span class="sxs-lookup"><span data-stu-id="f488e-153">This may require the Custodian Index to be updated.</span></span> 

<span data-ttu-id="f488e-154">Para acionar um processo de reindexação para lidar com itens parcialmente indexados:</span><span class="sxs-lookup"><span data-stu-id="f488e-154">To trigger a re-indexing process to address partially indexed items:</span></span>

1. <span data-ttu-id="f488e-155">Vá para descoberta eletrônica **_GT_ avançada de descoberta eletrônica (visualização)** e selecione uma ocorrência existente.</span><span class="sxs-lookup"><span data-stu-id="f488e-155">Go to **eDiscovery > Advanced eDiscovery (Preview)** and select an existing case.</span></span>

2. <span data-ttu-id="f488e-156">No caso, clique em para a **guia responsáveis**.</span><span class="sxs-lookup"><span data-stu-id="f488e-156">In the case, click to **Custodians tab**.</span></span> 

3. <span data-ttu-id="f488e-157">Selecione os responsáveis que precisam ser indexados novamente e clique em</span><span class="sxs-lookup"><span data-stu-id="f488e-157">Select the custodian(s) that needs to be re-indexed, and then click</span></span> ![Atualizar índice](../media/UpdateIndex.PNG) <span data-ttu-id="f488e-159">na página do menu de atalho.</span><span class="sxs-lookup"><span data-stu-id="f488e-159">on the flyout page.</span></span>

4. <span data-ttu-id="f488e-160">Verifique o status do índice de responsáveis clicando no link na coluna **status do trabalho** de indexação na guia **responsáveis** .</span><span class="sxs-lookup"><span data-stu-id="f488e-160">Check the status of the custodian index by clicking the link in the **Indexing job Status** column on the **Custodians** tab.</span></span>  

5. <span data-ttu-id="f488e-161">O status do processo de reindexação também pode ser acompanhado na guia **trabalhos** .</span><span class="sxs-lookup"><span data-stu-id="f488e-161">The status for the re-indexing process can also be tracked on the **Jobs** tab.</span></span>

<span data-ttu-id="f488e-162">Para obter mais informações sobre a reindexação e a correção de itens parcialmente indexados, consulte [corrigir erros de processamento](processing-data-for-case.md).</span><span class="sxs-lookup"><span data-stu-id="f488e-162">For more information about re-indexing and remediating partially indexed items, see [Fix processing errors](processing-data-for-case.md).</span></span>

## <a name="releasing-a-custodian-from-a-case"></a><span data-ttu-id="f488e-163">Liberar um dos responsáveis por um caso</span><span class="sxs-lookup"><span data-stu-id="f488e-163">Releasing a custodian from a case</span></span>

<span data-ttu-id="f488e-164">Um dos responsáveis é lançado em situações em que um caso é fechado, um não está mais sob obrigação de preservar o conteúdo de um caso ou quando um Objecté considerado não mais relevante para um caso específico.</span><span class="sxs-lookup"><span data-stu-id="f488e-164">A custodian is released in situations where a case is closed, a custodian is no longer under obligation to preserve content for a case, or when a custodian is deemed to no longer be relevant to a particular case.</span></span> 

<span data-ttu-id="f488e-165">Se você liberar um dos responsáveis após um aviso de isenção ter sido publicado, um aviso de lançamento será enviado para o seu.</span><span class="sxs-lookup"><span data-stu-id="f488e-165">If you release a custodian after a hold notice was published, a release notice will be sent to the custodian.</span></span> <span data-ttu-id="f488e-166">Além disso, qualquer custodial que tenha sido atribuído aos responsáveis liberados também será removido.</span><span class="sxs-lookup"><span data-stu-id="f488e-166">In addition, any custodial holds attributed to the released custodians will also be removed.</span></span>

<span data-ttu-id="f488e-167">Se o objecttiver sido colocado em um bloqueio silencioso, onde não foram emitidos notificações de bloqueio legal, qualquer custodial será atribuído aos responsáveis liberados serão removidos.</span><span class="sxs-lookup"><span data-stu-id="f488e-167">If the custodian was placed on a silent hold, where they were not issued any legal hold notifications, then any custodial holds attributed to the released custodians will be removed.</span></span>  

<span data-ttu-id="f488e-168">Para liberar um responsáveis:</span><span class="sxs-lookup"><span data-stu-id="f488e-168">To release a custodian:</span></span> 

1.  <span data-ttu-id="f488e-169">Vá para a guia **responsáveis** .</span><span class="sxs-lookup"><span data-stu-id="f488e-169">Go to the **Custodians** tab.</span></span>

2.  <span data-ttu-id="f488e-170">Selecione os responsáveis na lista e clique em</span><span class="sxs-lookup"><span data-stu-id="f488e-170">Select the custodian from the list and click</span></span> ![Liberar responsáveis](../media/ReleaseCustodian.PNG) <span data-ttu-id="f488e-172">na página do menu de atalho.</span><span class="sxs-lookup"><span data-stu-id="f488e-172">on the flyout page.</span></span>

    <span data-ttu-id="f488e-173">O status do responsáveis na guia **responsáveis** é definido como **liberado** e o **status de retenção** na página do submenu é alterado para inativo. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="f488e-173">The status of the custodian on the **Custodians** tab is set to **Released** and the **Hold status** on the flyout page is changed to **Inactive**.</span></span> 

> [!TIP]
> <span data-ttu-id="f488e-174">Os responsáveis podem estar simultaneamente envolvidos em várias questões legais.</span><span class="sxs-lookup"><span data-stu-id="f488e-174">A custodian might be simultaneously be involved in several legal hold matters.</span></span> <span data-ttu-id="f488e-175">Quando um dos responsáveis é liberado de uma ocorrência, as isenções e notificações entre outras coisas não serão afetadas.</span><span class="sxs-lookup"><span data-stu-id="f488e-175">When a custodian is released from a case, the holds and notifications across other matters will not be impacted.</span></span>

## <a name="related-information"></a><span data-ttu-id="f488e-176">Informações relacionadas</span><span class="sxs-lookup"><span data-stu-id="f488e-176">Related information</span></span>

 - [<span data-ttu-id="f488e-177">Correção de erros durante o processamento de dados</span><span class="sxs-lookup"><span data-stu-id="f488e-177">Error remediation when processing data</span></span>](error-remediation.md) 
- [<span data-ttu-id="f488e-178">Trabalhar com comunicações</span><span class="sxs-lookup"><span data-stu-id="f488e-178">Work with communications</span></span>](managing-custodian-communications.md)
