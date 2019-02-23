---
title: Visão geral das revisões de disposição
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: 6/29/2018
ms.audience: Admin
ms.topic: overview
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: Strat_O365_IP
search.appverid:
- MOE150
- MET150
ms.assetid: d0c6095b-bfee-4906-a2c7-89c2d7f411c1
description: Ao criar um rótulo que mantém o conteúdo no Office 365, você pode optar por acionar uma análise de disposição no final do período de retenção.
ms.openlocfilehash: 0948d61131595d4111f656c385c58258c5cce99c
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30215001"
---
# <a name="overview-of-disposition-reviews"></a><span data-ttu-id="09571-103">Visão geral das revisões de disposição</span><span class="sxs-lookup"><span data-stu-id="09571-103">Overview of disposition reviews</span></span>

<span data-ttu-id="09571-p101">Quando o conteúdo atinge o final do período de retenção, há vários motivos para que você possa querer revisar o conteúdo para decidir se ele pode ser excluído com segurança ("descartado"). Por exemplo, você pode precisar:</span><span class="sxs-lookup"><span data-stu-id="09571-p101">When content reaches the end of its retention period, there are several reasons why you might want to review that content to decide whether it can be safely deleted ("disposed"). For example, you might need to:</span></span>
  
- <span data-ttu-id="09571-106">Suspender a exclusão ("disposição") de conteúdo relevante no caso de litígio ou auditoria.</span><span class="sxs-lookup"><span data-stu-id="09571-106">Suspend the deletion ("disposition") of relevant content in the event of litigation or an audit.</span></span>
    
- <span data-ttu-id="09571-107">Remova o conteúdo da lista de descarte para armazenar em um arquivo morto, se esse conteúdo tiver um valor de pesquisa ou histórico.</span><span class="sxs-lookup"><span data-stu-id="09571-107">Remove content from the disposition list to store in an archive, if that content has research or historical value.</span></span>
    
- <span data-ttu-id="09571-108">Atribua um período de retenção diferente ao conteúdo, se a política original era uma solução temporária ou provisionada.</span><span class="sxs-lookup"><span data-stu-id="09571-108">Assign a different retention period to the content, if the original policy was a temporary or provisional solution.</span></span>
    
- <span data-ttu-id="09571-109">Retornar o conteúdo aos clientes ou transferi-lo para outra organização.</span><span class="sxs-lookup"><span data-stu-id="09571-109">Return the content to clients or transfer it to another organization.</span></span>
    
<span data-ttu-id="09571-p102">Ao criar um rótulo que mantém o conteúdo no Office 365, você pode optar por acionar uma análise de disposição no final do período de retenção. Em uma revisão de disposição:</span><span class="sxs-lookup"><span data-stu-id="09571-p102">When you create a label that retains content in Office 365, you can choose to trigger a disposition review at the end of the retention period. In a disposition review:</span></span>
  
- <span data-ttu-id="09571-p103">As pessoas escolhidas recebem uma notificação por email de que o conteúdo deve ser revisado. Esses revisores podem ser usuários individuais, grupos de distribuição ou segurança ou grupos do Office 365. Observe que as notificações são enviadas semanalmente.</span><span class="sxs-lookup"><span data-stu-id="09571-p103">The people you choose receive an email notification that they have content to review. These reviewers can be individual users, distribution or security groups, or Office 365 groups. Note that notifications are sent on a weekly basis.</span></span>
    
- <span data-ttu-id="09571-115">Os revisores vão para a página de **disposição** no centro &amp; de conformidade de segurança para analisar o conteúdo.</span><span class="sxs-lookup"><span data-stu-id="09571-115">The reviewers go to the **Disposition** page in the Security &amp; Compliance Center to review the content.</span></span> 
    
- <span data-ttu-id="09571-116">Para cada documento, o revisor pode:</span><span class="sxs-lookup"><span data-stu-id="09571-116">For each document, the reviewer can:</span></span>
    
  - <span data-ttu-id="09571-117">Aplicar um rótulo diferente.</span><span class="sxs-lookup"><span data-stu-id="09571-117">Apply a different label.</span></span>
    
  - <span data-ttu-id="09571-118">Estenda seu período de retenção.</span><span class="sxs-lookup"><span data-stu-id="09571-118">Extend its retention period.</span></span>
    
  - <span data-ttu-id="09571-119">Excluí-la permanentemente.</span><span class="sxs-lookup"><span data-stu-id="09571-119">Permanently delete it.</span></span>
    
- <span data-ttu-id="09571-120">Os revisores podem exibir as desposições de histórico ou pendentes e exportar essa lista como um arquivo. csv.</span><span class="sxs-lookup"><span data-stu-id="09571-120">Reviewers can view either pending or historical dispositions, and export that list as a .csv file.</span></span>
    
<span data-ttu-id="09571-121">Observe que as revisões de disposição exigem uma assinatura do Office 365 Enterprise e5.</span><span class="sxs-lookup"><span data-stu-id="09571-121">Note that disposition reviews require an Office 365 Enterprise E5 subscription.</span></span>
  
<span data-ttu-id="09571-p104">Uma análise de disposição pode incluir conteúdo em caixas de correio do Exchange, sites do SharePoint, contas do OneDrive e grupos do Office 365. O conteúdo que está aguardando uma revisão de disposição nesses locais é excluído somente depois que um revisor escolhe excluir permanentemente o conteúdo.</span><span class="sxs-lookup"><span data-stu-id="09571-p104">A disposition review can include content in Exchange mailboxes, SharePoint sites, OneDrive accounts, and Office 365 groups. Content awaiting a disposition review in those locations is deleted only after a reviewer chooses to permanently delete the content.</span></span>
  
![Página de disposição](media/b7436fb2-1f35-4146-8ca2-32c9d10f7e09.png)
  
## <a name="setting-up-the-disposition-review-by-creating-a-label"></a><span data-ttu-id="09571-125">ConFigurando a revisão de disposição criando um rótulo</span><span class="sxs-lookup"><span data-stu-id="09571-125">Setting up the disposition review by creating a label</span></span>

<span data-ttu-id="09571-p105">Este é o fluxo de trabalho básico para configurar uma revisão de disposição. Observe que esse fluxo mostra um rótulo que está sendo publicado e, em seguida, aplicado manualmente por um usuário; Como alternativa, um rótulo que dispara uma revisão de disposição pode ser aplicado automaticamente ao conteúdo.</span><span class="sxs-lookup"><span data-stu-id="09571-p105">This is the basic workflow for setting up a disposition review. Note that this flow shows a label being published and then manually applied by a user; alternatively, a label that triggers a disposition review can be auto-applied to content.</span></span>
  
![Gráfico mostrando o fluxo de como o descarte funciona](media/5fb3f33a-cb53-468c-becc-6dda0ec52778.png)
  
<span data-ttu-id="09571-p106">Uma revisão de disposição é uma opção quando você cria um rótulo no Office 365. Observe que essa opção não está disponível em uma política de retenção, mas somente em um rótulo com configurações de retenção.</span><span class="sxs-lookup"><span data-stu-id="09571-p106">A disposition review is an option when you create a label in Office 365. Note that this option is not available in a retention policy but only in a label with retention settings.</span></span>
  
<span data-ttu-id="09571-131">Para saber mais sobre rótulos, confira [Visão geral dos rótulos](labels.md).</span><span class="sxs-lookup"><span data-stu-id="09571-131">For more information about labels, see [Overview of labels](labels.md).</span></span>
  
![Configurações de retenção para um rótulo](media/a16dd202-8862-40ac-80ff-6fee974de5da.png)
  
## <a name="disposing-content"></a><span data-ttu-id="09571-133">DesCartando conteúdo</span><span class="sxs-lookup"><span data-stu-id="09571-133">Disposing content</span></span>

<span data-ttu-id="09571-p107">Quando um revisor é notificado por email que o conteúdo está pronto para revisão, eles podem ir até a página de **disposição** no &amp; centro de conformidade de segurança e selecionar um ou mais itens. O revisor pode então:</span><span class="sxs-lookup"><span data-stu-id="09571-p107">When a reviewer is notified by email that content is ready to review, they can go to the **Disposition** page in the Security &amp; Compliance Center and select one or more items. The reviewer can then:</span></span> 
  
- <span data-ttu-id="09571-136">Aplicar um rótulo diferente.</span><span class="sxs-lookup"><span data-stu-id="09571-136">Apply a different label.</span></span>
    
- <span data-ttu-id="09571-137">Estenda o período de retenção.</span><span class="sxs-lookup"><span data-stu-id="09571-137">Extend the retention period.</span></span>
    
- <span data-ttu-id="09571-138">Excluir permanentemente o item.</span><span class="sxs-lookup"><span data-stu-id="09571-138">Permanently delete the item.</span></span>
    
<span data-ttu-id="09571-p108">Um revisor pode usar o link para exibir o documento em seu local original, se o revisor tiver permissões para esse local. Durante uma revisão de disposição, o conteúdo nunca se move do local original e nunca é excluído até que o revisor opte por fazê-lo.</span><span class="sxs-lookup"><span data-stu-id="09571-p108">A reviewer can use the link to view the document in its original location, if the reviewer has permissions for that location. During a disposition review, the content never moves from its original location, and it's never deleted until the reviewer chooses to do so.</span></span>
  
<span data-ttu-id="09571-p109">Observe que as notificações por email são enviadas automaticamente aos revisores de forma semanal. Portanto, quando o conteúdo atinge o final do período de retenção, pode levar até sete dias para que os revisores recebam a notificação por email de que o conteúdo está aguardando disposição.</span><span class="sxs-lookup"><span data-stu-id="09571-p109">Note that the email notifications are sent automatically to reviewers on a weekly basis. Therefore, when content reaches the end of its retention period, it may take up to seven days for reviewers to receive the email notification that content is awaiting disposition.</span></span>
  
<span data-ttu-id="09571-p110">Observe também que todas as ações de disposição são auditadas. Para garantir isso, você deve ativar a auditoria pelo menos um dia antes da primeira ação de disposição: para saber mais, confira [Pesquisar o log de auditoria no centro de conformidade &amp; de segurança do Office 365](search-the-audit-log-in-security-and-compliance.md).</span><span class="sxs-lookup"><span data-stu-id="09571-p110">Also note that all disposition actions are audited. To ensure this, you must turn on auditing at least one day prior to the first disposition action - for more information, see [Search the audit log in the Office 365 Security &amp; Compliance Center](search-the-audit-log-in-security-and-compliance.md).</span></span> 
  
![Opções de disposição para um documento](media/771630fd-a9b0-47cf-983b-fe85eb4cdafd.png)
  
## <a name="permissions-for-disposition"></a><span data-ttu-id="09571-146">Permissões para descarte</span><span class="sxs-lookup"><span data-stu-id="09571-146">Permissions for disposition</span></span>

<span data-ttu-id="09571-p111">Para obter acesso à página de **disposição** , os revisores devem ser membros da função de **Gerenciamento de descarte** e da função de logs de **auditoria somente para exibição** . Recomendamos a criação de um novo grupo de função chamado revisores de disposição, adição dessas duas funções a esse grupo de função e adição de membros ao grupo de funções.</span><span class="sxs-lookup"><span data-stu-id="09571-p111">To get access to the **Disposition** page, reviewers must be members of the **Disposition Management** role and the **View-Only Audit Logs** role. We recommend creating a new role group called Disposition Reviewers, adding these two roles to that role group, and then adding members to the role group.</span></span> 
  
<span data-ttu-id="09571-149">Para obter mais informações, consulte [conceder aos usuários acesso ao centro de &amp; conformidade de segurança do Office 365](grant-access-to-the-security-and-compliance-center.md)</span><span class="sxs-lookup"><span data-stu-id="09571-149">For more information, see [Give users access to the Office 365 Security &amp; Compliance Center](grant-access-to-the-security-and-compliance-center.md)</span></span>
  
## <a name="how-long-until-disposed-content-is-permanently-deleted"></a><span data-ttu-id="09571-150">Quanto tempo até o conteúdo Descartado é excluído permanentemente</span><span class="sxs-lookup"><span data-stu-id="09571-150">How long until disposed content is permanently deleted</span></span>

<span data-ttu-id="09571-p112">O conteúdo que está aguardando uma análise de disposição é excluído somente depois que um revisor escolhe excluir permanentemente o conteúdo. Quando o revisor escolhe essa opção, o conteúdo do site do SharePoint ou da conta do OneDrive fica qualificado para o processo de limpeza padrão descrito nesta seção: [como funciona uma política de retenção com conteúdo in-loco](retention-policies.md#how-a-retention-policy-works-with-content-in-place).</span><span class="sxs-lookup"><span data-stu-id="09571-p112">Content awaiting a disposition review is deleted only after a reviewer chooses to permanently delete the content. When the reviewer chooses this option, the content in the SharePoint site or OneDrive account becomes eligible for the standard cleanup process described in this section: [How a retention policy works with content in place](retention-policies.md#how-a-retention-policy-works-with-content-in-place).</span></span>
  
<span data-ttu-id="09571-153">Isso significa que:</span><span class="sxs-lookup"><span data-stu-id="09571-153">This means that:</span></span>
  
- <span data-ttu-id="09571-p113">O conteúdo de uma biblioteca de documentos será movido para a lixeira de primeiro estágio **dentro de sete dias** de disposição e, em seguida, excluído permanentemente **93 dias** após isso. A lixeira não é indexada pela pesquisa e, portanto, seu conteúdo não está disponível para um bloqueio de descoberta eletrônica.</span><span class="sxs-lookup"><span data-stu-id="09571-p113">Content in a document library will be moved to the first-stage Recycle Bin **within 7 days** of disposition, and then permanently deleted **93 days** after that. The Recycle Bin is not indexed by search and therefore its contents are not available to an eDiscovery hold.</span></span> 
    
- <span data-ttu-id="09571-156">O conteúdo da biblioteca de retenção de preservação será excluído permanentemente **dentro de 7 dias** após o descarte.</span><span class="sxs-lookup"><span data-stu-id="09571-156">Content in the Preservation Hold library will be permanently deleted **within 7 days** of disposition.</span></span> 
    
## <a name="view-pending-and-completed-dispositions"></a><span data-ttu-id="09571-157">Exibir as desposições pendentes e concluídas</span><span class="sxs-lookup"><span data-stu-id="09571-157">View pending and completed dispositions</span></span>

<span data-ttu-id="09571-158">Na página **disposição** do centro de conformidade &amp; de segurança, você pode exibir as desposições pendentes e concluídas:</span><span class="sxs-lookup"><span data-stu-id="09571-158">On the **Disposition** page of the Security &amp; Compliance Center, you can view both pending and completed dispositions:</span></span> 
  
- <span data-ttu-id="09571-p114">\*\*\*\* As disposições pendentes atingiram o final do período de retenção e exigem uma análise de disposição. Após a revisão de cada item, decida se deseja aplicar um rótulo diferente a ele, estenda o período de retenção ou exclua-o permanentemente.</span><span class="sxs-lookup"><span data-stu-id="09571-p114">**Pending** dispositions have reached the end of their retention period and require a disposition review. After reviewing each item, decide if you want to apply a different label to it, extend its retention period, or permanently delete it.</span></span> 
    
- <span data-ttu-id="09571-p115">\*\*\*\* As desposições concluídas foram aprovadas para exclusão durante uma revisão de disposição e agora estão em processo de exclusão permanente. Os itens que tinham um rótulo diferente aplicado ou seu período de retenção estendido como parte de uma revisão não aparecerão aqui.</span><span class="sxs-lookup"><span data-stu-id="09571-p115">**Completed** dispositions were approved for deletion during a disposition review and are now in the process of being permanently deleted. Items that had a different label applied or their retention period extended as part of a review won't appear here.</span></span> 
    
### <a name="filter-the-disposition-views"></a><span data-ttu-id="09571-163">Filtrar as exibições de disposição</span><span class="sxs-lookup"><span data-stu-id="09571-163">Filter the disposition views</span></span>

<span data-ttu-id="09571-p116">Você pode filtrar esses modos de exibição por rótulo ou intervalo de tempo. Para desposições pendentes, o intervalo de tempo é baseado na data de expiração. Para desposições históricas, o intervalo de tempo é baseado na data de exclusão.</span><span class="sxs-lookup"><span data-stu-id="09571-p116">You can filter these views by label or time range. For pending dispositions, the time range is based on the expiry date. For historical dispositions, the time range is based on the deletion date.</span></span>
  
![Opções de filtro na página de disposição](media/8682a9f5-a77d-45ae-b902-8418a3ebbea1.png)
  
### <a name="export-the-disposition-items"></a><span data-ttu-id="09571-168">Exportar os itens de disposição</span><span class="sxs-lookup"><span data-stu-id="09571-168">Export the disposition items</span></span>

<span data-ttu-id="09571-169">Além disso, você pode exportar os itens em um modo de exibição como um arquivo. csv que pode ser aberto no Excel.</span><span class="sxs-lookup"><span data-stu-id="09571-169">In addition, you can export the items in either view as a .csv file that you can open in Excel.</span></span>
  
![Dados de disposição exPortados no Excel](media/08e3bc09-b132-47b4-a051-a590b697e725.png)
  

