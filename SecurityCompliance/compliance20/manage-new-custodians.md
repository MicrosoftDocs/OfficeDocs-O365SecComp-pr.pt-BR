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
ms.openlocfilehash: 95a1bcbbc279ad4e476fc479e701b0f8a921c83b
ms.sourcegitcommit: baf23be44f1ed5abbf84f140b5ffa64fce605478
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/26/2019
ms.locfileid: "30295674"
---
# <a name="manage-custodians-in-an-advanced-ediscovery-preview-case"></a><span data-ttu-id="253b6-102">Gerenciar os responsáveis em um caso de descoberta eletrônica avançada (visualização)</span><span class="sxs-lookup"><span data-stu-id="253b6-102">Manage custodians in an Advanced eDiscovery (Preview) case</span></span>

<span data-ttu-id="253b6-p101">A guia responsáveis contém uma lista classificável de todos os responsáveis da ocorrência. Após adicionar os responsáveis a um caso, os detalhes sobre cada um serão automaticamente coletados do Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="253b6-p101">The Custodians tab contains a sortable list of all the custodians in the case. After you add custodians to a case, details about each custodian will automatically be collected from Azure Active Directory.</span></span>

## <a name="viewing-custodian-details"></a><span data-ttu-id="253b6-105">Exibindo detalhes do responsáveis</span><span class="sxs-lookup"><span data-stu-id="253b6-105">Viewing custodian details</span></span>

<span data-ttu-id="253b6-p102">A página de menu que contém os detalhes dos responsáveis é exibida após você adicionar um dos responsáveis a um caso e selecioná-los na lista da guia **responsáveis** . A partir daqui, você pode exibir todos os detalhes relacionados a esses responsáveis. A página de submenu contém os seguintes campos:</span><span class="sxs-lookup"><span data-stu-id="253b6-p102">The flyout page that contains custodian details appears after you add a custodian to a case and select them from the list on the **Custodians** tab. From here, you can view all the details related to that custodian. The flyout page contains the following fields:</span></span>

- <span data-ttu-id="253b6-108">Informações de contato</span><span class="sxs-lookup"><span data-stu-id="253b6-108">Contact information</span></span>

  - <span data-ttu-id="253b6-p103">**Nome para exibição**: o nome exibido no catálogo de endereços para os responsáveis. Geralmente, é a combinação do nome do responsáveis, inicial e sobrenome do meio.</span><span class="sxs-lookup"><span data-stu-id="253b6-p103">**Display Name**: The name displayed in the address book for the custodian. This is usually the combination of the custodian’s first name, middle initial and last name.</span></span>
  - <span data-ttu-id="253b6-111">**Mail/SMTP**: o endereço SMTP para os responsáveis, por exemplo, Jeff@contoso.onmicrosoft.com.</span><span class="sxs-lookup"><span data-stu-id="253b6-111">**Mail/SMTP**: The SMTP address for the custodian, for example, jeff@contoso.onmicrosoft.com.</span></span>  
  - <span data-ttu-id="253b6-112">**Título**: o cargo do profissional.</span><span class="sxs-lookup"><span data-stu-id="253b6-112">**Title**: The custodian’s job title.</span></span>
  - <span data-ttu-id="253b6-113">**Departamento**: o nome do departamento no qual os responsáveis funciona.</span><span class="sxs-lookup"><span data-stu-id="253b6-113">**Department**: The name for the department in which the custodian works.</span></span>
  - <span data-ttu-id="253b6-p104">**Gerente**: gerente do responsáveis. O gerente designado receberá qualquer comunicação de escalonamento para este responsáveis.</span><span class="sxs-lookup"><span data-stu-id="253b6-p104">**Manager**: The custodian’s manager. The designated manager will receive any Escalation communications for this custodian.</span></span>
  
- <span data-ttu-id="253b6-116">Informações sobre o local</span><span class="sxs-lookup"><span data-stu-id="253b6-116">Location information</span></span>

  - <span data-ttu-id="253b6-117">**Cidade**: a cidade na qual o responsáveis está localizado.</span><span class="sxs-lookup"><span data-stu-id="253b6-117">**City**: The city in which the custodian is located.</span></span>
  - <span data-ttu-id="253b6-118">**Estado**: o estado ou província no endereço do responsáveis.</span><span class="sxs-lookup"><span data-stu-id="253b6-118">**State**: The state or province in the custodian’s address.</span></span>
  - <span data-ttu-id="253b6-119">**País/região**: o país/região no qual o responsáveis está localizado; por exemplo, "US" ou "ru".</span><span class="sxs-lookup"><span data-stu-id="253b6-119">**Country/Region**: The country/region in which the custodian’s is located; for example, “US” or “UK”.</span></span>
  - <span data-ttu-id="253b6-120">**Office**: o local do escritório no local de trabalho do responsáveis.</span><span class="sxs-lookup"><span data-stu-id="253b6-120">**Office**: The office location in the custodian’s place of business.</span></span>

- <span data-ttu-id="253b6-121">Informações sobre o caso</span><span class="sxs-lookup"><span data-stu-id="253b6-121">Case information</span></span>

  - <span data-ttu-id="253b6-122">**Status de espera**: indica se os responsáveis foram colocados em espera.</span><span class="sxs-lookup"><span data-stu-id="253b6-122">**Hold status**: Indicates if the custodian has been placed on hold.</span></span> 
  - <span data-ttu-id="253b6-p105">**Status de Comunicação**: indica se os responsáveis foram emitidos um aviso de espera. Se o objecttiver sido emitido um aviso, ele será marcado como *publicado*. Se não tiver sido emitido um aviso para os responsáveis, este status será canCelado. \*\*</span><span class="sxs-lookup"><span data-stu-id="253b6-p105">**Communication status**: Indicates if the custodian has been issued a hold notice. If the custodian has been issued a notice, then this will be marked as *Published*. If the custodian has not been issued a notice, then this status will be *Un-Published*.</span></span> 
  - <span data-ttu-id="253b6-p106">**Status**: o status dos responsáveis dentro do caso. Isso estará *ativo* se os responsáveis ainda estiverem em espera para o caso. Se um responsáveis for removido de uma ocorrência, seu status será alterado para *liberado*.</span><span class="sxs-lookup"><span data-stu-id="253b6-p106">**Status**: The status of the custodian within the case. This will be *Active* if the custodian is still on hold for the case. If a custodian is removed from a case, their status will change to *Released*.</span></span> 

- <span data-ttu-id="253b6-129">Status de processamento</span><span class="sxs-lookup"><span data-stu-id="253b6-129">Processing status</span></span>

  - <span data-ttu-id="253b6-130">**Status**de indexação: indica o status do trabalho de indexação profunda.</span><span class="sxs-lookup"><span data-stu-id="253b6-130">**Indexing status**: Indicates the status of the deep indexing job.</span></span>  
  - <span data-ttu-id="253b6-131">**Hora da última atualização**da indexação: indica o dateStamp de quando o trabalho de indexação profunda foi disparado pela última vez.</span><span class="sxs-lookup"><span data-stu-id="253b6-131">**Indexing Last Updated Time**: Indicates the datestamp of when the deep indexing job was last triggered.</span></span>
  - <span data-ttu-id="253b6-132">**Fontes de dados**: mostra a contagem de caixas de correio, sites e equipes que foram selecionadas para os responsáveis.</span><span class="sxs-lookup"><span data-stu-id="253b6-132">**Data sources**: Shows the count of mailboxes, sites, and Teams that have been selected for the custodian.</span></span>

## <a name="updating-a-custodian"></a><span data-ttu-id="253b6-133">Atualizando um responsáveis</span><span class="sxs-lookup"><span data-stu-id="253b6-133">Updating a custodian</span></span>

<span data-ttu-id="253b6-p107">À medida que seu caso avança, você pode descobrir que pode haver fontes de dados adicionais relevantes para um determinado & de seu caso. Em outros cenários, talvez você queira remover determinadas fontes de dados que foram revisadas e consideradas não relevantes.</span><span class="sxs-lookup"><span data-stu-id="253b6-p107">As your case progresses, you may discover that there may be additional data sources relevant to a specific custodian & your case. In other scenarios, you may want to remove certain data sources that have been reviewed and deemed as not relevant.</span></span>

<span data-ttu-id="253b6-136">Para atualizar um Objecte as fontes de dados selecionadas:</span><span class="sxs-lookup"><span data-stu-id="253b6-136">To update a custodian and the selected data sources:</span></span>

1. <span data-ttu-id="253b6-137">Selecione um caso existente na **descoberta eletrônica avançada do > de descoberta eletrônica (visualização)**.</span><span class="sxs-lookup"><span data-stu-id="253b6-137">Select an existing case from the **eDiscovery > Advanced eDiscovery (Preview)**.</span></span>
  
2. <span data-ttu-id="253b6-138">No caso, clique na guia **responsáveis** .</span><span class="sxs-lookup"><span data-stu-id="253b6-138">In the case, click the **Custodians** tab.</span></span>
  
3. <span data-ttu-id="253b6-139">Selecione os responsáveis (s) na lista e clique em **Editar fontes**.</span><span class="sxs-lookup"><span data-stu-id="253b6-139">Select the custodian(s) from the list and click **Edit sources**.</span></span>
  
4. <span data-ttu-id="253b6-140">Atualize as seleções para os locais do Exchange e do OneDrive clicando em **escolher fontes de dados**.</span><span class="sxs-lookup"><span data-stu-id="253b6-140">Update selections for Exchange and OneDrive locations by clicking **Choose data sources**.</span></span>
  
5. <span data-ttu-id="253b6-p108">Adicione ou remova as caixas de correio do Teams, SharePoint ou Exchange mapeadas ao usuário clicando para **selecionar outras fontes de dados**. Para obter mais informações sobre como mapear fontes de dados para um dos responsáveis, confira [Adicionar responsáveis a um caso](add-custodians-to-case.md).</span><span class="sxs-lookup"><span data-stu-id="253b6-p108">Add or remove Teams, SharePoint, or Exchange mailboxes mapped the user by clicking to **Select additional data sources**. For more information about how you to map data sources to a custodian, see [Add custodians to a case](add-custodians-to-case.md).</span></span>
  
6. <span data-ttu-id="253b6-143">Para atualizar o status de retenção de responsáveis, clique em **colocar custodial isenções**e habilite ou desabilite a retenção para os responsáveis.</span><span class="sxs-lookup"><span data-stu-id="253b6-143">To update the custodian hold status, click **Place custodial holds**, and enable or disable the hold for custodians.</span></span>

> [!TIP]
> <span data-ttu-id="253b6-144">Você pode selecionar vários responsáveis para executar ações em massa, como reindexação, liberação ou edição de um conjunto de responsáveis.</span><span class="sxs-lookup"><span data-stu-id="253b6-144">You can select multiple custodians to perform bulk actions, like re-indexing, releasing, or editing a set of custodians.</span></span>

## <a name="resolving-custodian-processing-errors"></a><span data-ttu-id="253b6-145">Resolvendo erros de processamento de responsáveis</span><span class="sxs-lookup"><span data-stu-id="253b6-145">Resolving custodian processing errors</span></span>

<span data-ttu-id="253b6-p109">Na maioria dos fluxos de trabalho jurídicos, após a adição de responsáveis por uma investigação específica, um subconjunto dos dados dos usuários será pesquisado. Devido a grandes tamanhos de arquivo ou possíveis danos, alguns itens dentro das fontes de dados dos responsáveis podem ser parcialmente indexados. Usando o recurso de indexação avançada de descoberta eletrônica avançada (visualização), esses itens parcialmente indexados podem ser corrigidos automaticamente por meio de um novo rastreamento e re-indexação desses itens sob demanda.</span><span class="sxs-lookup"><span data-stu-id="253b6-p109">In most Legal workflows, after custodians are added for a specific investigation, a subset of the users’ data will be searched. Due to large file sizes or possible corruption, some items within the custodians’ data sources may be partially indexed. Using the Advanced eDiscovery (Preview) deep indexing capability, these partially indexed items can be automatically remediated by re-crawling and re-indexing these items on demand.</span></span> 

<span data-ttu-id="253b6-p110">Quando um usuário é adicionado a uma ocorrência, seus dados serão automaticamente "indexados em profundidade", permitindo que os usuários deixem esses itens parcialmente indexados em vez de terem que baixar, corrigir e executar novamente as pesquisas fora do Office 365. Durante o ciclo de vida de um caso, um usuário pode corrigir itens ou adicionar novas fontes de dados para um determinado usuário. Isso pode exigir que o índice de responsáveis seja atualizado.</span><span class="sxs-lookup"><span data-stu-id="253b6-p110">When a custodian is added to a case, their data will automatically be "deep indexed”, allowing users to leave these partially indexed items in place instead of having to download, remediate and re-run searches outside of Office 365. During the lifecycle of a case, a user may remediate items or add new data sources for a given custodian. This may require the Custodian Index to be updated.</span></span> 

<span data-ttu-id="253b6-152">Para acionar um processo de reindexação para lidar com itens parcialmente indexados:</span><span class="sxs-lookup"><span data-stu-id="253b6-152">To trigger a re-indexing process to address partially indexed items:</span></span>

1. <span data-ttu-id="253b6-153">Vá para descoberta eletrônica **_GT_ avançada de descoberta eletrônica (visualização)** e selecione uma ocorrência existente.</span><span class="sxs-lookup"><span data-stu-id="253b6-153">Go to **eDiscovery > Advanced eDiscovery (Preview)** and select an existing case.</span></span>

2. <span data-ttu-id="253b6-154">No caso, clique em para a **guia responsáveis**.</span><span class="sxs-lookup"><span data-stu-id="253b6-154">In the case, click to **Custodians tab**.</span></span> 

3. <span data-ttu-id="253b6-155">Selecione os responsáveis que precisam ser indexados novamente e clique em **Atualizar índice** na página do menu suspenso.</span><span class="sxs-lookup"><span data-stu-id="253b6-155">Select the custodian(s) that needs to be re-indexed, and then click **Update index** on the flyout page.</span></span>

4. <span data-ttu-id="253b6-156">Verifique o status do índice de responsáveis clicando no link na coluna **status do trabalho** de indexação na guia **responsáveis** .</span><span class="sxs-lookup"><span data-stu-id="253b6-156">Check the status of the custodian index by clicking the link in the **Indexing job Status** column on the **Custodians** tab.</span></span>  

5. <span data-ttu-id="253b6-157">O status do processo de reindexação também pode ser acompanhado na guia **trabalhos** .</span><span class="sxs-lookup"><span data-stu-id="253b6-157">The status for the re-indexing process can also be tracked on the **Jobs** tab.</span></span>

<span data-ttu-id="253b6-158">Para obter mais informações sobre a reindexação e a correção de itens parcialmente indexados, consulte [corrigir erros de processamento](processing-data-for-case.md).</span><span class="sxs-lookup"><span data-stu-id="253b6-158">For more information about re-indexing and remediating partially indexed items, see [Fix processing errors](processing-data-for-case.md).</span></span>

## <a name="releasing-a-custodian-from-a-case"></a><span data-ttu-id="253b6-159">Liberar um dos responsáveis por um caso</span><span class="sxs-lookup"><span data-stu-id="253b6-159">Releasing a custodian from a case</span></span>

<span data-ttu-id="253b6-160">Um dos responsáveis é lançado em situações em que um caso é fechado, um não está mais sob obrigação de preservar o conteúdo de um caso ou quando um Objecté considerado não mais relevante para um caso específico.</span><span class="sxs-lookup"><span data-stu-id="253b6-160">A custodian is released in situations where a case is closed, a custodian is no longer under obligation to preserve content for a case, or when a custodian is deemed to no longer be relevant to a particular case.</span></span> 

<span data-ttu-id="253b6-p111">Se você liberar um dos responsáveis após um aviso de isenção ter sido publicado, um aviso de lançamento será enviado para o seu. Além disso, qualquer custodial que tenha sido atribuído aos responsáveis liberados também será removido.</span><span class="sxs-lookup"><span data-stu-id="253b6-p111">If you release a custodian after a hold notice was published, a release notice will be sent to the custodian. In addition, any custodial holds attributed to the released custodians will also be removed.</span></span>

<span data-ttu-id="253b6-163">Se o objecttiver sido colocado em um bloqueio silencioso, onde não foram emitidos notificações de bloqueio legal, qualquer custodial será atribuído aos responsáveis liberados serão removidos.</span><span class="sxs-lookup"><span data-stu-id="253b6-163">If the custodian was placed on a silent hold, where they were not issued any legal hold notifications, then any custodial holds attributed to the released custodians will be removed.</span></span>  

<span data-ttu-id="253b6-164">Para liberar um responsáveis:</span><span class="sxs-lookup"><span data-stu-id="253b6-164">To release a custodian:</span></span> 

1.  <span data-ttu-id="253b6-165">Vá para a guia **responsáveis** .</span><span class="sxs-lookup"><span data-stu-id="253b6-165">Go to the **Custodians** tab.</span></span>

2.  <span data-ttu-id="253b6-166">Selecione os responsáveis na lista e clique em **liberar responsáveis** na página do menu suspenso.</span><span class="sxs-lookup"><span data-stu-id="253b6-166">Select the custodian from the list and click **Release custodians** on the flyout page.</span></span>

    <span data-ttu-id="253b6-167">O status do responsáveis na guia **responsáveis** é definido como **liberado** e o **status de retenção** na página do submenu é alterado para inativo. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="253b6-167">The status of the custodian on the **Custodians** tab is set to **Released** and the **Hold status** on the flyout page is changed to **Inactive**.</span></span> 

> [!TIP]
> <span data-ttu-id="253b6-p112">Os responsáveis podem estar simultaneamente envolvidos em várias questões legais. Quando um dos responsáveis é liberado de uma ocorrência, as isenções e notificações entre outras coisas não serão afetadas.</span><span class="sxs-lookup"><span data-stu-id="253b6-p112">A custodian might be simultaneously be involved in several legal hold matters. When a custodian is released from a case, the holds and notifications across other matters will not be impacted.</span></span>

## <a name="related-information"></a><span data-ttu-id="253b6-170">Informações relacionadas</span><span class="sxs-lookup"><span data-stu-id="253b6-170">Related information</span></span>

 - [<span data-ttu-id="253b6-171">Correção de erro ao processar dados</span><span class="sxs-lookup"><span data-stu-id="253b6-171">Error remediation when processing data</span></span>](error-remediation.md) 
- [<span data-ttu-id="253b6-172">Trabalhar com comunicações</span><span class="sxs-lookup"><span data-stu-id="253b6-172">Work with communications</span></span>](managing-custodian-communications.md)
