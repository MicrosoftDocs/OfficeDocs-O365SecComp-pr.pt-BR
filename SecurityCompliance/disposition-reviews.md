---
title: Visão geral das revisões de disposição
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: 6/29/2018
ms.audience: Admin
ms.topic: overview
ms.service: o365-administration
localization_priority: Normal
ms.collection: Strat_O365_IP
search.appverid:
- MOE150
- MET150
ms.assetid: d0c6095b-bfee-4906-a2c7-89c2d7f411c1
description: Quando você cria um rótulo que retém o conteúdo no Office 365, você pode optar por acionar uma análise de disposição no final do período de retenção.
ms.openlocfilehash: c0a2933f597c9b314ac4ce2e72de9619fac90082
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/27/2018
ms.locfileid: "23013715"
---
# <a name="overview-of-disposition-reviews"></a><span data-ttu-id="b6515-103">Visão geral das revisões de disposição</span><span class="sxs-lookup"><span data-stu-id="b6515-103">Overview of disposition reviews</span></span>

<span data-ttu-id="b6515-p101">Quando o conteúdo atinge o final do período de retenção, há vários motivos por que talvez você queira revisar o conteúdo para decidir se ele pode ser excluído com segurança ("descartados"). Por exemplo, você pode precisar:</span><span class="sxs-lookup"><span data-stu-id="b6515-p101">When content reaches the end of its retention period, there are several reasons why you might want to review that content to decide whether it can be safely deleted ("disposed"). For example, you might need to:</span></span>
  
- <span data-ttu-id="b6515-106">Suspenda a exclusão ("descarte") de conteúdo relevante em caso de litígio ou auditoria.</span><span class="sxs-lookup"><span data-stu-id="b6515-106">Suspend the deletion ("disposition") of relevant content in the event of litigation or an audit.</span></span>
    
- <span data-ttu-id="b6515-107">Remova o conteúdo da lista disposição para armazenar em um arquivo morto, se esse conteúdo tiver research ou um valor de histórico.</span><span class="sxs-lookup"><span data-stu-id="b6515-107">Remove content from the disposition list to store in an archive, if that content has research or historical value.</span></span>
    
- <span data-ttu-id="b6515-108">Atribua um período de retenção diferente para o conteúdo, se a diretiva original foi uma solução temporária ou provisional.</span><span class="sxs-lookup"><span data-stu-id="b6515-108">Assign a different retention period to the content, if the original policy was a temporary or provisional solution.</span></span>
    
- <span data-ttu-id="b6515-109">Retornar o conteúdo aos clientes ou transferi-la para outra organização.</span><span class="sxs-lookup"><span data-stu-id="b6515-109">Return the content to clients or transfer it to another organization.</span></span>
    
<span data-ttu-id="b6515-p102">Quando você cria um rótulo que retém o conteúdo no Office 365, você pode optar por acionar uma análise de disposição no final do período de retenção. Em uma revisão de disposição:</span><span class="sxs-lookup"><span data-stu-id="b6515-p102">When you create a label that retains content in Office 365, you can choose to trigger a disposition review at the end of the retention period. In a disposition review:</span></span>
  
- <span data-ttu-id="b6515-p103">As pessoas que você escolher recebem uma notificação de e-mail que têm conteúdo para analisar. Esses revisores podem ser usuários individuais, distribuição ou grupos de segurança ou grupos do Office 365. Observe que as notificações são enviadas semanalmente.</span><span class="sxs-lookup"><span data-stu-id="b6515-p103">The people you choose receive an email notification that they have content to review. These reviewers can be individual users, distribution or security groups, or Office 365 groups. Note that notifications are sent on a weekly basis.</span></span>
    
- <span data-ttu-id="b6515-115">Os revisores ir para a página de **disposição** na segurança &amp; Centro de conformidade para analisar o conteúdo.</span><span class="sxs-lookup"><span data-stu-id="b6515-115">The reviewers go to the **Disposition** page in the Security &amp; Compliance Center to review the content.</span></span> 
    
- <span data-ttu-id="b6515-116">Para cada documento, o revisor pode:</span><span class="sxs-lookup"><span data-stu-id="b6515-116">For each document, the reviewer can:</span></span>
    
  - <span data-ttu-id="b6515-117">Aplica um rótulo diferente.</span><span class="sxs-lookup"><span data-stu-id="b6515-117">Apply a different label.</span></span>
    
  - <span data-ttu-id="b6515-118">Estenda seu período de retenção.</span><span class="sxs-lookup"><span data-stu-id="b6515-118">Extend its retention period.</span></span>
    
  - <span data-ttu-id="b6515-119">Excluí-lo permanentemente.</span><span class="sxs-lookup"><span data-stu-id="b6515-119">Permanently delete it.</span></span>
    
- <span data-ttu-id="b6515-120">Revisores podem exibir descartes pendentes ou históricos e exportar essa lista como um arquivo. csv.</span><span class="sxs-lookup"><span data-stu-id="b6515-120">Reviewers can view either pending or historical dispositions, and export that list as a .csv file.</span></span>
    
<span data-ttu-id="b6515-121">Observe que disposição revisões requerem uma assinatura do Office 365 Enterprise E5.</span><span class="sxs-lookup"><span data-stu-id="b6515-121">Note that disposition reviews require an Office 365 Enterprise E5 subscription.</span></span>
  
<span data-ttu-id="b6515-p104">Uma análise de disposição pode incluir o conteúdo em caixas de correio do Exchange, sites do SharePoint, OneDrive contas e grupos do Office 365. Aguardando uma análise de disposição nesses locais de conteúdo é excluído somente depois que um revisor escolhe excluir permanentemente o conteúdo.</span><span class="sxs-lookup"><span data-stu-id="b6515-p104">A disposition review can include content in Exchange mailboxes, SharePoint sites, OneDrive accounts, and Office 365 groups. Content awaiting a disposition review in those locations is deleted only after a reviewer chooses to permanently delete the content.</span></span>
  
![Página de disposição](media/b7436fb2-1f35-4146-8ca2-32c9d10f7e09.png)
  
## <a name="setting-up-the-disposition-review-by-creating-a-label"></a><span data-ttu-id="b6515-125">Configurando a revisão de disposição criando um rótulo</span><span class="sxs-lookup"><span data-stu-id="b6515-125">Setting up the disposition review by creating a label</span></span>

<span data-ttu-id="b6515-p105">Este é o fluxo de trabalho básico para configurar uma análise de disposição. Observe que esse fluxo mostra um rótulo que está sendo publicado e aplicada manualmente por um usuário; Como alternativa, um rótulo que dispara uma análise de disposição pode ser autoaplicado ao conteúdo.</span><span class="sxs-lookup"><span data-stu-id="b6515-p105">This is the basic workflow for setting up a disposition review. Note that this flow shows a label being published and then manually applied by a user; alternatively, a label that triggers a disposition review can be auto-applied to content.</span></span>
  
![Gráfico mostrando o fluxo de como funciona a disposição](media/5fb3f33a-cb53-468c-becc-6dda0ec52778.png)
  
<span data-ttu-id="b6515-p106">Uma análise de disposição é uma opção quando você cria um rótulo no Office 365. Observe que essa opção não está disponível em uma política de retenção, mas somente em um rótulo com as configurações de retenção.</span><span class="sxs-lookup"><span data-stu-id="b6515-p106">A disposition review is an option when you create a label in Office 365. Note that this option is not available in a retention policy but only in a label with retention settings.</span></span>
  
<span data-ttu-id="b6515-131">Para obter mais informações sobre rótulos, consulte [Overview of rótulos](labels.md).</span><span class="sxs-lookup"><span data-stu-id="b6515-131">For more information about labels, see [Overview of labels](labels.md).</span></span>
  
![Configurações de retenção para um rótulo](media/a16dd202-8862-40ac-80ff-6fee974de5da.png)
  
## <a name="disposing-content"></a><span data-ttu-id="b6515-133">Disposição de conteúdo</span><span class="sxs-lookup"><span data-stu-id="b6515-133">Disposing content</span></span>

<span data-ttu-id="b6515-p107">Quando um revisor será notificado por email que o conteúdo está pronto para analisar, eles podem ir para a página de **disposição** na segurança &amp; Centro de conformidade e selecione um ou mais itens. O revisor pode então:</span><span class="sxs-lookup"><span data-stu-id="b6515-p107">When a reviewer is notified by email that content is ready to review, they can go to the **Disposition** page in the Security &amp; Compliance Center and select one or more items. The reviewer can then:</span></span> 
  
- <span data-ttu-id="b6515-136">Aplica um rótulo diferente.</span><span class="sxs-lookup"><span data-stu-id="b6515-136">Apply a different label.</span></span>
    
- <span data-ttu-id="b6515-137">Estenda o período de retenção.</span><span class="sxs-lookup"><span data-stu-id="b6515-137">Extend the retention period.</span></span>
    
- <span data-ttu-id="b6515-138">Exclua permanentemente o item.</span><span class="sxs-lookup"><span data-stu-id="b6515-138">Permanently delete the item.</span></span>
    
<span data-ttu-id="b6515-p108">Um revisor pode usar o link para exibir o documento em seu local original, se o revisor tiver permissões para esse local. Durante uma revisão de disposição, nunca move o conteúdo de seu local original e ele é excluído nunca até que o revisor decide fazê-lo.</span><span class="sxs-lookup"><span data-stu-id="b6515-p108">A reviewer can use the link to view the document in its original location, if the reviewer has permissions for that location. During a disposition review, the content never moves from its original location, and it's never deleted until the reviewer chooses to do so.</span></span>
  
<span data-ttu-id="b6515-p109">Observe que as notificações de email são enviadas automaticamente aos revisores semanalmente. Portanto, quando o conteúdo atinge o final do período de retenção, pode levar até sete dias para revisores receber email de notificação que o conteúdo está aguardando disposição.</span><span class="sxs-lookup"><span data-stu-id="b6515-p109">Note that the email notifications are sent automatically to reviewers on a weekly basis. Therefore, when content reaches the end of its retention period, it may take up to seven days for reviewers to receive the email notification that content is awaiting disposition.</span></span>
  
<span data-ttu-id="b6515-p110">Observe também que todas as ações de disposição sejam auditadas. Para garantir isso, você deve ativar a auditoria de pelo menos um dia antes da primeira ação de disposição - para obter mais informações, consulte [Pesquisar o log de auditoria de segurança do Office 365 &amp; Centro de conformidade](search-the-audit-log-in-security-and-compliance.md).</span><span class="sxs-lookup"><span data-stu-id="b6515-p110">Also note that all disposition actions are audited. To ensure this, you must turn on auditing at least one day prior to the first disposition action - for more information, see [Search the audit log in the Office 365 Security &amp; Compliance Center](search-the-audit-log-in-security-and-compliance.md).</span></span> 
  
![Opções de disposição para um documento](media/771630fd-a9b0-47cf-983b-fe85eb4cdafd.png)
  
## <a name="permissions-for-disposition"></a><span data-ttu-id="b6515-146">Permissões de disposição</span><span class="sxs-lookup"><span data-stu-id="b6515-146">Permissions for disposition</span></span>

<span data-ttu-id="b6515-p111">Para obter acesso à página de **disposição** , revisores devem ser membros da função de **Gerenciamento de disposição** e a função **Logs de auditoria somente para exibição** . Recomendamos a criação de um novo grupo de função chamado revisores de disposição, adicionando essas duas funções a esse grupo de função e, em seguida, adicionar membros ao grupo de funções.</span><span class="sxs-lookup"><span data-stu-id="b6515-p111">To get access to the **Disposition** page, reviewers must be members of the **Disposition Management** role and the **View-Only Audit Logs** role. We recommend creating a new role group called Disposition Reviewers, adding these two roles to that role group, and then adding members to the role group.</span></span> 
  
<span data-ttu-id="b6515-149">Para obter mais informações, consulte [Conceder aos usuários acesso para a segurança do Office 365 &amp; Centro de conformidade](grant-access-to-the-security-and-compliance-center.md)</span><span class="sxs-lookup"><span data-stu-id="b6515-149">For more information, see [Give users access to the Office 365 Security &amp; Compliance Center](grant-access-to-the-security-and-compliance-center.md)</span></span>
  
## <a name="how-long-until-disposed-content-is-permanently-deleted"></a><span data-ttu-id="b6515-150">Quanto tempo até que o conteúdo descartado é permanentemente excluído</span><span class="sxs-lookup"><span data-stu-id="b6515-150">How long until disposed content is permanently deleted</span></span>

<span data-ttu-id="b6515-p112">Aguardando uma análise de disposição de conteúdo é excluído somente depois que um revisor escolhe excluir permanentemente o conteúdo. Quando o revisor escolhe essa opção, o conteúdo no site do SharePoint ou conta de OneDrive se torna qualificado para o processo de limpeza standard descrito nesta seção: [funcionamento de uma política de retenção com conteúdo in-loco](retention-policies.md#how-a-retention-policy-works-with-content-in-place).</span><span class="sxs-lookup"><span data-stu-id="b6515-p112">Content awaiting a disposition review is deleted only after a reviewer chooses to permanently delete the content. When the reviewer chooses this option, the content in the SharePoint site or OneDrive account becomes eligible for the standard cleanup process described in this section: [How a retention policy works with content in place](retention-policies.md#how-a-retention-policy-works-with-content-in-place).</span></span>
  
<span data-ttu-id="b6515-153">Isso significa que:</span><span class="sxs-lookup"><span data-stu-id="b6515-153">This means that:</span></span>
  
- <span data-ttu-id="b6515-p113">Conteúdo em uma biblioteca de documentos será movido para o primeiro estágio Recycle Bin **dentro de 7 dias** de disposição e excluídos permanentemente **93 dias** depois disso. A Lixeira não é indexada pela pesquisa e, portanto, não está disponível a uma isenção de descoberta eletrônica de seu conteúdo.</span><span class="sxs-lookup"><span data-stu-id="b6515-p113">Content in a document library will be moved to the first-stage Recycle Bin **within 7 days** of disposition, and then permanently deleted **93 days** after that. The Recycle Bin is not indexed by search and therefore its contents are not available to an eDiscovery hold.</span></span> 
    
- <span data-ttu-id="b6515-156">Conteúdo na preservação, mantenha biblioteca serão permanentemente excluídos **dentro de 7 dias** de disposição.</span><span class="sxs-lookup"><span data-stu-id="b6515-156">Content in the Preservation Hold library will be permanently deleted **within 7 days** of disposition.</span></span> 
    
## <a name="view-pending-and-completed-dispositions"></a><span data-ttu-id="b6515-157">Modo de exibição pendentes e concluídas de vendas</span><span class="sxs-lookup"><span data-stu-id="b6515-157">View pending and completed dispositions</span></span>

<span data-ttu-id="b6515-158">Na página **disposição** da segurança &amp; Centro de conformidade, você pode exibir descartes pendentes e concluídas:</span><span class="sxs-lookup"><span data-stu-id="b6515-158">On the **Disposition** page of the Security &amp; Compliance Center, you can view both pending and completed dispositions:</span></span> 
  
- <span data-ttu-id="b6515-p114">**Pendente** descartes atingiu o final do seu período de retenção e exigem uma análise de disposição. Após revisar cada item, decida se deseja aplicar um rótulo diferente a ele, estender seu período de retenção ou excluí-lo permanentemente.</span><span class="sxs-lookup"><span data-stu-id="b6515-p114">**Pending** dispositions have reached the end of their retention period and require a disposition review. After reviewing each item, decide if you want to apply a different label to it, extend its retention period, or permanently delete it.</span></span> 
    
- <span data-ttu-id="b6515-p115">**Concluído** descartes foram aprovadas para exclusão durante uma revisão de disposição e agora estão no processo sejam excluídos permanentemente. Itens que tinham um rótulo diferente aplicado ou seu período de retenção estendido como parte de uma análise não aparecerá aqui.</span><span class="sxs-lookup"><span data-stu-id="b6515-p115">**Completed** dispositions were approved for deletion during a disposition review and are now in the process of being permanently deleted. Items that had a different label applied or their retention period extended as part of a review won't appear here.</span></span> 
    
### <a name="filter-the-disposition-views"></a><span data-ttu-id="b6515-163">Filtrar os modos de exibição de disposição</span><span class="sxs-lookup"><span data-stu-id="b6515-163">Filter the disposition views</span></span>

<span data-ttu-id="b6515-p116">Você pode filtrar esses modos de exibição pelo intervalo de rótulo ou hora. Para pendentes descartes, o intervalo de tempo se baseia na data de vencimento. Para descartes históricas, o intervalo de tempo baseia-se na data de exclusão.</span><span class="sxs-lookup"><span data-stu-id="b6515-p116">You can filter these views by label or time range. For pending dispositions, the time range is based on the expiry date. For historical dispositions, the time range is based on the deletion date.</span></span>
  
![Opções de filtro na página de disposição](media/8682a9f5-a77d-45ae-b902-8418a3ebbea1.png)
  
### <a name="export-the-disposition-items"></a><span data-ttu-id="b6515-168">Exportar os itens de disposição</span><span class="sxs-lookup"><span data-stu-id="b6515-168">Export the disposition items</span></span>

<span data-ttu-id="b6515-169">Além disso, você pode exportar os itens em qualquer modo de exibição como um arquivo. csv que pode ser aberta no Excel.</span><span class="sxs-lookup"><span data-stu-id="b6515-169">In addition, you can export the items in either view as a .csv file that you can open in Excel.</span></span>
  
![Dados de disposição exportado no Excel](media/08e3bc09-b132-47b4-a051-a590b697e725.png)
  

