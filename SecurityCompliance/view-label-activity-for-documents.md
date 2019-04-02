---
title: Exibir a atividade de rótulos de documentos
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: 5/9/2018
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
ms.collection: M365-security-compliance
localization_priority: Priority
search.appverid:
- MOE150
- MET150
description: Com o Explorador de Atividade de Rótulo no Centro de Conformidade e Segurança do Office 365, você pode rapidamente pesquisar e exibir a atividade de rótulo para todo o conteúdo no SharePoint e no OneDrive for Business nos últimos 30 dias. Esses são dados em tempo real que fornecem uma exibição clara para o que está acontecendo no seu locatário.
ms.openlocfilehash: 55888ff2ef8118389a88955a8f4e047170606524
ms.sourcegitcommit: 799a958fcac643f62dfac6fa04020f2f4758635c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/29/2019
ms.locfileid: "30997107"
---
# <a name="view-label-activity-for-documents"></a><span data-ttu-id="3ab0b-104">Exibir a atividade de rótulos de documentos</span><span class="sxs-lookup"><span data-stu-id="3ab0b-104">View label activity for documents</span></span>

<span data-ttu-id="3ab0b-p102">Depois de criar seus rótulos, você deverá verificar se eles estão sendo aplicados a conteúdo conforme o desejado. Com o Explorador de Atividade de Rótulo no Centro de Conformidade e Segurança do Office 365, você pode rapidamente pesquisar e exibir a atividade de rótulo para todo o conteúdo no SharePoint e no OneDrive for Business nos últimos 30 dias. Esses são dados em tempo real que fornecem uma exibição clara para o que está acontecendo no seu locatário.</span><span class="sxs-lookup"><span data-stu-id="3ab0b-p102">After you create your labels, you'll want to verify that they're being applied to content as you intended. With the Label Activity Explorer in the Office 365 Security &amp; Compliance Center, you can quickly search and view label activity for all content across SharePoint and OneDrive for Business over the past 30 days. This is real-time data that gives you a clear view into what's happening in your tenant.</span></span>
  
<span data-ttu-id="3ab0b-108">Por exemplo, com o Explorador de Atividade do Rótulo, você pode:</span><span class="sxs-lookup"><span data-stu-id="3ab0b-108">For example, with the Label Activity Explorer, you can:</span></span>
  
- <span data-ttu-id="3ab0b-109">Exibir o número de vezes que cada rótulo foi aplicado em cada dia (até 30 dias).</span><span class="sxs-lookup"><span data-stu-id="3ab0b-109">View how many times each label was applied on each day (up to 30 days).</span></span>
    
- <span data-ttu-id="3ab0b-110">Ver quem rotulou exatamente o arquivo em qual data, juntamente com um link para o site onde reside esse arquivo.</span><span class="sxs-lookup"><span data-stu-id="3ab0b-110">See who labeled exactly which file on which date, along with a link to the site where that file resides.</span></span>
    
- <span data-ttu-id="3ab0b-111">Exiba quais arquivos tiveram os rótulos alterados ou removidos, quais são os rótulos antigos e os novos e quem fez a alteração.</span><span class="sxs-lookup"><span data-stu-id="3ab0b-111">View which files had labels changed or removed, what the old and new labels are, and who made the change.</span></span>
    
- <span data-ttu-id="3ab0b-p103">Filtre os dados para ver todas as atividades de rótulo para um rótulo, arquivo ou usuário específico. Você também pode filtrar a atividade de rótulo por local (SharePoint ou OneDrive for Business) e se o rótulo foi aplicado manual ou automaticamente.</span><span class="sxs-lookup"><span data-stu-id="3ab0b-p103">Filter the data to see all the label activity for a specific label, file, or user. You can also filter label activity by location (SharePoint or OneDrive for Business) and whether the label was applied manually or auto-applied.</span></span>
    
- <span data-ttu-id="3ab0b-p104">Exiba a atividade de rótulo para pastas, além de documentos individuais. Em breve haverá a capacidade para mostrar quantos arquivos dentro dessa pasta foram rotulados como resultado da rotulação da pasta.</span><span class="sxs-lookup"><span data-stu-id="3ab0b-p104">View label activity for folders as well as individual documents. Coming soon is the ability to show how many files inside that folder got labeled as a result of the folder getting labeled.</span></span>
    
<span data-ttu-id="3ab0b-116">Você pode encontrar o Explorador de Atividade de Rótulo no &amp;Centro de Conformidade e Segurança > **Governança de dados** > **Explorador de Atividade de Etiqueta**.</span><span class="sxs-lookup"><span data-stu-id="3ab0b-116">You can find the Label Activity Explorer in the Security  Compliance Center  Data governance  Label Activity Explorer.</span></span>
  
<span data-ttu-id="3ab0b-117">Observe que no Gerenciador de Atividade de Rótulo exige uma assinatura do Office 365 Enterprise E5.</span><span class="sxs-lookup"><span data-stu-id="3ab0b-117">Note that the Label Activity Explorer requires an Office 365 Enterprise E5 subscription.</span></span>
  
![Explorador de Atividade de Rótulo](media/671ca0cd-1457-40b4-9917-b663360afd95.png)
  
## <a name="view-label-activities-for-files-or-folders"></a><span data-ttu-id="3ab0b-119">Exibir atividades de rótulo para arquivos ou pastas</span><span class="sxs-lookup"><span data-stu-id="3ab0b-119">View label activities for files or folders</span></span>

<span data-ttu-id="3ab0b-p105">Na parte superior do Gerenciador de Atividade de Rótulo, você pode optar por exibir as atividades para arquivos ou pastas. Observe que as atividades de pasta incluem apenas a pasta propriamente dita, não os arquivos dentro da pasta.</span><span class="sxs-lookup"><span data-stu-id="3ab0b-p105">At the top of the Label Activity Explorer, you can choose whether to view activities for files or folders. Note that folder activity includes only the folder itself, not the files inside the folder.</span></span>
  
<span data-ttu-id="3ab0b-p106">Talvez você queira ver a atividade do rótulo para pastas porque, se rotular uma pasta, todos os arquivos nessa pasta também recebem esse rótulo (exceto os arquivos que tiveram um rótulo explicitamente aplicado a eles). Portanto, rotular pastas pode afetar vários arquivos. Para saber mais, confira [Aplicar um rótulo de retenção padrão a todo o conteúdo em uma biblioteca, pasta ou conjunto de documentos do SharePoint](labels.md#applying-a-default-retention-label-to-all-content-in-a-sharepoint-library-folder-or-document-set).</span><span class="sxs-lookup"><span data-stu-id="3ab0b-p106">You might want to see label activity for folders because if you label a folder, all files inside that folder also get that label (except for files that have had a label applied explicitly to them). Therefore, labeling folders might affect a significant number of files. For more information, see [Applying a default retention label to all content in a SharePoint library, folder, or document set](labels.md#applying-a-default-retention-label-to-all-content-in-a-sharepoint-library-folder-or-document-set).</span></span>
  
![Menu suspenso mostrando as atividades do rótulo para arquivos e pastas](media/11030584-f52d-49eb-86f3-7ead16a3b704.png)
  
### <a name="label-activities"></a><span data-ttu-id="3ab0b-126">Atividades do rótulo</span><span class="sxs-lookup"><span data-stu-id="3ab0b-126">Label activities</span></span>

 <span data-ttu-id="3ab0b-p107">As **Atividades do rótulo** incluem todas as ações do rótulo: **adicionar**, **remover**, ou **alterar** um rótulo. Você pode usar esse modo de exibição para obter uma visão completa de a quantos arquivos cada rótulo é aplicado por dia.</span><span class="sxs-lookup"><span data-stu-id="3ab0b-p107">**Label activities** includes all label actions: **adding**, **removing**, or **changing** a label. You can use this view to get a comprehensive look at how many files each label's been applied to per day.</span></span> 
  
### <a name="label-changes"></a><span data-ttu-id="3ab0b-129">Alterações do rótulo</span><span class="sxs-lookup"><span data-stu-id="3ab0b-129">Label changes</span></span>

 <span data-ttu-id="3ab0b-p108">As **Alterações do rótulo** incluem as ações de possivelmente perigosas de **remover** ou **alterar** um rótulo. Você pode usar esse modo de exibição para ver rapidamente essas ações arriscadas e o usuário as que executou. Na lista atividades abaixo do gráfico, selecione um arquivo e, em seguida, clique em um link para esse arquivo no painel de detalhes à direita.</span><span class="sxs-lookup"><span data-stu-id="3ab0b-p108">**Label changes** includes the potentially risky actions of **removing** or **changing** a label. You can use this view to quickly see such risky actions and the user who performed them. In the activity list below the chart, you can select a file, and then click a link to that file in the details pane on the right.</span></span> 
  
![Painel de detalhes para atividade de rótulos](media/eb580fd4-b5be-4fda-9ba5-c1256777310d.png)
  
## <a name="filter-label-activity"></a><span data-ttu-id="3ab0b-134">Filtrar atividade do rótulo</span><span class="sxs-lookup"><span data-stu-id="3ab0b-134">Filter label activity</span></span>

<span data-ttu-id="3ab0b-p109">Você pode filtrar rapidamente os dados para ver todas as atividades de rótulo para um rótulo, arquivo ou usuário específico. Você também pode filtrar a atividade de rótulo por local (SharePoint ou OneDrive for Business) e se o rótulo foi aplicado manual ou automaticamente.</span><span class="sxs-lookup"><span data-stu-id="3ab0b-p109">You can quickly filter the data to see all the label activity for a specific label, file, or user. You can also filter label activity by location (SharePoint or OneDrive for Business) and whether the label was applied manually or auto-applied.</span></span>
  
![Filtros para atividade do rótulo](media/9de92985-120f-48b4-96a7-ef7ec8a71ff0.png)
  

