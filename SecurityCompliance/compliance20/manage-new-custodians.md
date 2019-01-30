---
title: Gerenciando responsáveis em um caso de eDiscovery avançado (Preview)
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
ms.openlocfilehash: 742f6bc35b67071fba528e6a0ce543ecc6915762
ms.sourcegitcommit: ee28ee2b2bdfd049333c2f495d7f7780d13af4a6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2019
ms.locfileid: "29607375"
---
# <a name="managing-custodians-in-an-advanced-ediscovery-preview-case"></a><span data-ttu-id="aacec-102">Gerenciando responsáveis em um caso de eDiscovery avançado (Preview)</span><span class="sxs-lookup"><span data-stu-id="aacec-102">Managing custodians in an Advanced eDiscovery (Preview) case</span></span>

<span data-ttu-id="aacec-p101">Na guia responsáveis contém uma lista classificada de todos os responsáveis no caso. Depois de adicionar responsáveis a um caso, detalhes sobre cada responsável automaticamente serão coletadas do Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="aacec-p101">The Custodians tab contains a sortable list of all the custodians in the case. After you add custodians to a case, details about each custodian will automatically be collected from Azure Active Directory.</span></span>

## <a name="viewing-custodian-details"></a><span data-ttu-id="aacec-105">Exibir os detalhes dos responsáveis</span><span class="sxs-lookup"><span data-stu-id="aacec-105">Viewing custodian details</span></span>

<span data-ttu-id="aacec-p102">A página de submenu que contém detalhes dos responsáveis é exibida depois de adicionar um funcionário encarregado a um caso e selecione-os da lista na guia **responsáveis** . A partir daqui, você pode exibir todos os detalhes relacionados a dos responsáveis. A página de submenu contém os seguintes campos:</span><span class="sxs-lookup"><span data-stu-id="aacec-p102">The flyout page that contains custodian details appears after you add a custodian to a case and select them from the list on the **Custodians** tab. From here, you can view all the details related to that custodian. The flyout page contains the following fields:</span></span>

- <span data-ttu-id="aacec-108">Informações de contato</span><span class="sxs-lookup"><span data-stu-id="aacec-108">Contact information</span></span>

  - <span data-ttu-id="aacec-p103">**Nome de exibição**: O nome exibido no catálogo de endereços para dos responsáveis. Isso geralmente é a combinação entre nome das dos responsáveis, nome intermediário de inicial e o sobrenome.</span><span class="sxs-lookup"><span data-stu-id="aacec-p103">**Display Name**: The name displayed in the address book for the custodian. This is usually the combination of the custodian’s first name, middle initial and last name.</span></span>
  - <span data-ttu-id="aacec-111">**Mail/SMTP**: endereço SMTP o dos responsáveis, por exemplo, jeff@contoso.onmicrosoft.com.</span><span class="sxs-lookup"><span data-stu-id="aacec-111">**Mail/SMTP**: The SMTP address for the custodian, for example, jeff@contoso.onmicrosoft.com.</span></span>  
  - <span data-ttu-id="aacec-112">**Título**: o cargo de responsáveis.</span><span class="sxs-lookup"><span data-stu-id="aacec-112">**Title**: The custodian’s job title.</span></span>
  - <span data-ttu-id="aacec-113">**Departamento**: O nome para o departamento no qual dos responsáveis funciona.</span><span class="sxs-lookup"><span data-stu-id="aacec-113">**Department**: The name for the department in which the custodian works.</span></span>
  - <span data-ttu-id="aacec-p104">**Gerente**: gerente de responsáveis. O gerente designado receberá qualquer comunicações de escalonamento para dos responsáveis.</span><span class="sxs-lookup"><span data-stu-id="aacec-p104">**Manager**: The custodian’s manager. The designated manager will receive any Escalation communications for this custodian.</span></span>
  
- <span data-ttu-id="aacec-116">Informações sobre o local</span><span class="sxs-lookup"><span data-stu-id="aacec-116">Location information</span></span>

  - <span data-ttu-id="aacec-117">**Cidade**: A cidade na qual dos responsáveis está localizado.</span><span class="sxs-lookup"><span data-stu-id="aacec-117">**City**: The city in which the custodian is located.</span></span>
  - <span data-ttu-id="aacec-118">**Estado**: O estado ou província no endereço de responsáveis.</span><span class="sxs-lookup"><span data-stu-id="aacec-118">**State**: The state or province in the custodian’s address.</span></span>
  - <span data-ttu-id="aacec-119">**País/região**: O país/região no qual dos responsáveis está localizado; Por exemplo, "EUA" ou "UK".</span><span class="sxs-lookup"><span data-stu-id="aacec-119">**Country/Region**: The country/region in which the custodian’s is located; for example, “US” or “UK”.</span></span>
  - <span data-ttu-id="aacec-120">**Office**: O local do escritório no lugar de responsáveis dos negócios.</span><span class="sxs-lookup"><span data-stu-id="aacec-120">**Office**: The office location in the custodian’s place of business.</span></span>

- <span data-ttu-id="aacec-121">Informações do caso</span><span class="sxs-lookup"><span data-stu-id="aacec-121">Case information</span></span>

  - <span data-ttu-id="aacec-122">**Status de isenção**: indica se dos responsáveis foi colocado em espera.</span><span class="sxs-lookup"><span data-stu-id="aacec-122">**Hold status**: Indicates if the custodian has been placed on hold.</span></span> 
  - <span data-ttu-id="aacec-p105">**Status de comunicação**: indica se dos responsáveis tem sido emitido um aviso de isenção. Se dos responsáveis tem sido emitido um aviso, em seguida, isso será marcado como *publicado*. Se dos responsáveis não tem sido emitido um aviso, então esse status será *cancelada*.</span><span class="sxs-lookup"><span data-stu-id="aacec-p105">**Communication status**: Indicates if the custodian has been issued a hold notice. If the custodian has been issued a notice, then this will be marked as *Published*. If the custodian has not been issued a notice, then this status will be *Un-Published*.</span></span> 
  - <span data-ttu-id="aacec-p106">**Status**: O status do dos responsáveis dentro o caso. Isso estará *ativo* se dos responsáveis estiver ainda em espera para o caso. Se um funcionário encarregado for removido de um caso, seu status será alterado para *liberado*.</span><span class="sxs-lookup"><span data-stu-id="aacec-p106">**Status**: The status of the custodian within the case. This will be *Active* if the custodian is still on hold for the case. If a custodian is removed from a case, their status will change to *Released*.</span></span> 

- <span data-ttu-id="aacec-129">Status do processamento</span><span class="sxs-lookup"><span data-stu-id="aacec-129">Processing status</span></span>

  - <span data-ttu-id="aacec-130">**Status da indexação**: indica o status do trabalho de indexação aprofundado.</span><span class="sxs-lookup"><span data-stu-id="aacec-130">**Indexing status**: Indicates the status of the deep indexing job.</span></span>  
  - <span data-ttu-id="aacec-131">**Indexação última vez atualizados**: indica a datestamp de quando o trabalho de indexação minuciosa última foi disparado.</span><span class="sxs-lookup"><span data-stu-id="aacec-131">**Indexing Last Updated Time**: Indicates the datestamp of when the deep indexing job was last triggered.</span></span>
  - <span data-ttu-id="aacec-132">**Fontes de dados**: mostra a contagem de caixas de correio, sites e equipes que foram selecionadas para dos responsáveis.</span><span class="sxs-lookup"><span data-stu-id="aacec-132">**Data sources**: Shows the count of mailboxes, sites, and Teams that have been selected for the custodian.</span></span>

## <a name="updating-a-custodian"></a><span data-ttu-id="aacec-133">Atualizando um funcionário encarregado</span><span class="sxs-lookup"><span data-stu-id="aacec-133">Updating a custodian</span></span>

<span data-ttu-id="aacec-p107">Como suas maiusculas em andamento, você pode descobrir que podem haver fontes de dados adicionais relevantes para uma & dos responsáveis específico seu caso. Em outros cenários, convém remover determinadas fontes de dados que foram revisadas e considerados como não relevantes.</span><span class="sxs-lookup"><span data-stu-id="aacec-p107">As your case progresses, you may discover that there may be additional data sources relevant to a specific custodian & your case. In other scenarios, you may want to remove certain data sources that have been reviewed and deemed as not relevant.</span></span>

<span data-ttu-id="aacec-136">Para atualizar dos responsáveis e as fontes de dados selecionado:</span><span class="sxs-lookup"><span data-stu-id="aacec-136">To update a custodian and the selected data sources:</span></span>

1. <span data-ttu-id="aacec-137">Selecione uma ocorrência existente a **eDiscovery avançado do eDiscovery gt _ (Preview)**.</span><span class="sxs-lookup"><span data-stu-id="aacec-137">Select an existing case from the **eDiscovery > Advanced eDiscovery (Preview)**.</span></span>
  
2. <span data-ttu-id="aacec-138">No caso, clique na guia **responsáveis** .</span><span class="sxs-lookup"><span data-stu-id="aacec-138">In the case, click the **Custodians** tab.</span></span>
  
3. <span data-ttu-id="aacec-139">Selecione o custodian(s) na lista e clique em **Editar fontes**.</span><span class="sxs-lookup"><span data-stu-id="aacec-139">Select the custodian(s) from the list and click **Edit sources**.</span></span>
  
4. <span data-ttu-id="aacec-140">Atualize seleções para locais do Exchange e OneDrive clicando em **fontes de dados de escolha**.</span><span class="sxs-lookup"><span data-stu-id="aacec-140">Update selections for Exchange and OneDrive locations by clicking **Choose data sources**.</span></span>
  
5. <span data-ttu-id="aacec-p108">Adicionar ou remover o Exchange, SharePoint ou equipes caixas de correio mapeado o usuário clicando para **Selecionar as fontes de dados adicionais**. Para obter mais informações sobre como mapear dados fontes para dos responsáveis, consulte [Adicionar responsáveis a um eDiscovery avançado (Preview) caso](add-custodians-to-case.md).</span><span class="sxs-lookup"><span data-stu-id="aacec-p108">Add or remove Teams, SharePoint, or Exchange mailboxes mapped the user by clicking to **Select additional data sources**. For more information about how you to map data sources to a custodian, see [Add custodians to an Advanced eDiscovery (Preview) Case](add-custodians-to-case.md).</span></span>
  
6. <span data-ttu-id="aacec-143">Para atualizar o status de retenção dos responsáveis, clique em **retenções locais custódia**e habilitar ou desabilitar a isenção para os responsáveis.</span><span class="sxs-lookup"><span data-stu-id="aacec-143">To update the custodian hold status, click **Place custodial holds**, and enable or disable the hold for custodians.</span></span>

> [!TIP]
> <span data-ttu-id="aacec-144">Você pode selecionar vários responsáveis para realizar ações em massa, como reindexação, liberando ou editando um conjunto dos responsáveis.</span><span class="sxs-lookup"><span data-stu-id="aacec-144">You can select multiple custodians to perform bulk actions, like re-indexing, releasing, or editing a set of custodians.</span></span>

## <a name="resolving-custodian-processing-errors"></a><span data-ttu-id="aacec-145">Resolvendo erros de processamento dos responsáveis</span><span class="sxs-lookup"><span data-stu-id="aacec-145">Resolving custodian processing errors</span></span>

<span data-ttu-id="aacec-p109">Na maioria dos fluxos de trabalho Legal, depois responsáveis são adicionados para uma investigação específica, um subconjunto de dados dos usuários será pesquisado. Devido aos tamanhos de arquivos grandes ou corrupção possível, alguns itens dentro de fontes de dados dos responsáveis podem ser indexadas parcialmente. Usando o recurso de indexação minuciosa eDiscovery avançado (Preview), esses itens indexados parcialmente podem ser remediadas de automaticamente pelo novamente rastrear e indexar novamente esses itens sob demanda.</span><span class="sxs-lookup"><span data-stu-id="aacec-p109">In most Legal workflows, after custodians are added for a specific investigation, a subset of the users’ data will be searched. Due to large file sizes or possible corruption, some items within the custodians’ data sources may be partially indexed. Using the Advanced eDiscovery (Preview) deep indexing capability, these partially indexed items can be automatically remediated by re-crawling and re-indexing these items on demand.</span></span> 

<span data-ttu-id="aacec-p110">Quando um funcionário encarregado é adicionado a um caso, os dados serão automaticamente "profundidade indexados", permitindo que os usuários deixar estas parcialmente indexados itens locais em vez de informarem baixar, remediar e execute novamente a pesquisas fora do Office 365. Durante o ciclo de vida de um caso, um usuário pode remediar itens ou adicionar novas fontes de dados para dos responsáveis determinado. Isso pode exigir o índice dos responsáveis a ser atualizado.</span><span class="sxs-lookup"><span data-stu-id="aacec-p110">When a custodian is added to a case, their data will automatically be "deep indexed”, allowing users to leave these partially indexed items in place instead of having to download, remediate and re-run searches outside of Office 365. During the lifecycle of a case, a user may remediate items or add new data sources for a given custodian. This may require the Custodian Index to be updated.</span></span> 

<span data-ttu-id="aacec-152">Para disparar um processo de indexação novamente para endereço parcialmente itens indexados:</span><span class="sxs-lookup"><span data-stu-id="aacec-152">To trigger a re-indexing process to address partially indexed items:</span></span>

1. <span data-ttu-id="aacec-153">Vá para **eDiscovery avançado do eDiscovery gt _ (Preview)** e selecione uma ocorrência existente.</span><span class="sxs-lookup"><span data-stu-id="aacec-153">Go to **eDiscovery > Advanced eDiscovery (Preview)** and select an existing case.</span></span>

2. <span data-ttu-id="aacec-154">No caso, clique em à **guia responsáveis**.</span><span class="sxs-lookup"><span data-stu-id="aacec-154">In the case, click to **Custodians tab**.</span></span> 

3. <span data-ttu-id="aacec-155">Selecione o custodian(s) que precisa ser indexado novamente e, em seguida, clique em **Atualizar índice** da página de submenu.</span><span class="sxs-lookup"><span data-stu-id="aacec-155">Select the custodian(s) that needs to be re-indexed, and then click **Update index** on the flyout page.</span></span>

4. <span data-ttu-id="aacec-156">Verificar o status do índice dos responsáveis clicando no link na coluna **Status do trabalho de indexação** na guia **responsáveis** .</span><span class="sxs-lookup"><span data-stu-id="aacec-156">Check the status of the custodian index by clicking the link in the **Indexing job Status** column on the **Custodians** tab.</span></span>  

5. <span data-ttu-id="aacec-157">O status para o processo de indexação novamente também podem ser rastreado na guia **Jobs** .</span><span class="sxs-lookup"><span data-stu-id="aacec-157">The status for the re-indexing process can also be tracked on the **Jobs** tab.</span></span>

<span data-ttu-id="aacec-158">Para obter mais informações sobre os itens indexados parcialmente indexação novamente e remediando, consulte [Corrigindo erros no eDiscovery avançado (Preview) de processamento](processing-data-for-case.md).</span><span class="sxs-lookup"><span data-stu-id="aacec-158">For more information about re-indexing and remediating partially indexed items, see [Fixing processing errors in Advanced eDiscovery (Preview)](processing-data-for-case.md).</span></span>

## <a name="releasing-a-custodian-from-a-case"></a><span data-ttu-id="aacec-159">Liberação de um funcionário encarregado de um caso</span><span class="sxs-lookup"><span data-stu-id="aacec-159">Releasing a custodian from a case</span></span>

<span data-ttu-id="aacec-160">Dos responsáveis for lançado em situações onde um caso for fechado, um funcionário encarregado não está mais sendo obrigação de preservar o conteúdo de um caso ou quando um funcionário encarregado é considerado nenhum mais ser relevantes para uma determinada caso.</span><span class="sxs-lookup"><span data-stu-id="aacec-160">A custodian is released in situations where a case is closed, a custodian is no longer under obligation to preserve content for a case, or when a custodian is deemed to no longer be relevant to a particular case.</span></span> 

<span data-ttu-id="aacec-p111">Se você solta um funcionário encarregado após um aviso de isenção foi publicado, um aviso de versão será enviado para dos responsáveis. Além disso, qualquer isenções custódia atribuídas aos responsáveis lançadas também serão removidas.</span><span class="sxs-lookup"><span data-stu-id="aacec-p111">If you release a custodian after a hold notice was published, a release notice will be sent to the custodian. In addition, any custodial holds attributed to the released custodians will also be removed.</span></span>

<span data-ttu-id="aacec-163">Se dos responsáveis foi colocado em uma espera silenciosa, onde eles não foram emitidos qualquer notificações de retenção legal, qualquer isenções custódia atribuídas aos responsáveis lançadas serão removidas.</span><span class="sxs-lookup"><span data-stu-id="aacec-163">If the custodian was placed on a silent hold, where they were not issued any legal hold notifications, then any custodial holds attributed to the released custodians will be removed.</span></span>  

<span data-ttu-id="aacec-164">Para liberar um funcionário encarregado:</span><span class="sxs-lookup"><span data-stu-id="aacec-164">To release a custodian:</span></span> 

1.  <span data-ttu-id="aacec-165">Vá para a guia **responsáveis** .</span><span class="sxs-lookup"><span data-stu-id="aacec-165">Go to the **Custodians** tab.</span></span>

2.  <span data-ttu-id="aacec-166">Selecione dos responsáveis da lista e clique **responsáveis versão** na página submenu.</span><span class="sxs-lookup"><span data-stu-id="aacec-166">Select the custodian from the list and click **Release custodians** on the flyout page.</span></span>

    <span data-ttu-id="aacec-167">O status do dos responsáveis na guia **responsáveis** é definido para a **Outubrolançada** e o **status de retenção** na página submenu é alterado para **inativo**.</span><span class="sxs-lookup"><span data-stu-id="aacec-167">The status of the custodian on the **Custodians** tab is set to **Released** and the **Hold status** on the flyout page is changed to **Inactive**.</span></span> 

> [!TIP]
> <span data-ttu-id="aacec-p112">Dos responsáveis podem ser simultaneamente estar envolvido nos vários assuntos de retenção legal. Quando um funcionário encarregado é liberado de um caso, as isenções e notificações em outros assuntos não serão afetadas.</span><span class="sxs-lookup"><span data-stu-id="aacec-p112">A custodian might be simultaneously be involved in several legal hold matters. When a custodian is released from a case, the holds and notifications across other matters will not be impacted.</span></span>

## <a name="related-information"></a><span data-ttu-id="aacec-170">Informações relacionadas</span><span class="sxs-lookup"><span data-stu-id="aacec-170">Related information</span></span>

 - <span data-ttu-id="aacec-171">Atributos de usuário no Active Directory</span><span class="sxs-lookup"><span data-stu-id="aacec-171">User Attributes in Active Directory</span></span> 
 - [<span data-ttu-id="aacec-172">Correção de erro durante o processamento de dados</span><span class="sxs-lookup"><span data-stu-id="aacec-172">Error remediation when processing data</span></span>](error-remediation.md) 
 - [<span data-ttu-id="aacec-173">Trabalhando com a comunicação</span><span class="sxs-lookup"><span data-stu-id="aacec-173">Working with communications</span></span>](managing-custodian-communications.md)
