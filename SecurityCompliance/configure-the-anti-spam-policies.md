---
title: Configurar políticas antispam
ms.author: tracyp
author: MSFTTracyP
manager: laurawi
ms.date: 6/9/2015
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 31279431-828d-48bd-b979-20b6de15fa4a
ms.collection:
- M365-security-compliance
description: A filtragem de spam é automaticamente habilitada em toda a empresa por meio das políticas antispam padrão (filtro de conexão, filtro de spam e spam de saída). Como administrador, você pode exibir e editar, mas não excluir, as políticas antispam padrão de forma que elas sejam ajustadas para atender melhor às necessidades da sua organização. Para maior granularidade, você também pode criar políticas personalizadas e aplicá-las a usuários, grupos ou domínios especificados em sua organização. Por padrão, as políticas personalizadas têm precedência sobre a política padrão, mas é possível alterar a prioridade de suas políticas.
ms.openlocfilehash: 992885a394031e133008f28a455383fc2f3f0616
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32260799"
---
# <a name="configure-the-anti-spam-policies"></a><span data-ttu-id="ca4af-106">Configurar políticas antispam</span><span class="sxs-lookup"><span data-stu-id="ca4af-106">Configure the anti-spam policies</span></span>

<span data-ttu-id="ca4af-107">A filtragem de spam é automaticamente habilitada em toda a empresa por meio das políticas antispam padrão (filtro de conexão, filtro de spam e spam de saída).</span><span class="sxs-lookup"><span data-stu-id="ca4af-107">Spam filtering is automatically enabled company-wide through the default anti-spam policies (connection filter, spam filter, and outbound spam).</span></span> <span data-ttu-id="ca4af-108">Como administrador, você pode exibir e editar, mas não excluir, as políticas antispam padrão de forma que elas sejam ajustadas para atender melhor às necessidades da sua organização.</span><span class="sxs-lookup"><span data-stu-id="ca4af-108">As an administrator, you can view and edit, but not delete, the default anti-spam policies so that they are tailored to best meet the needs of your organization.</span></span> <span data-ttu-id="ca4af-109">Para maior granularidade, você também pode criar políticas personalizadas e aplicá-las a usuários, grupos ou domínios especificados em sua organização.</span><span class="sxs-lookup"><span data-stu-id="ca4af-109">For greater granularity, you can also create custom policies and apply them to specified users, groups, or domains in your organization.</span></span> <span data-ttu-id="ca4af-110">Por padrão, as políticas personalizadas têm precedência sobre a política padrão, mas é possível alterar a prioridade de suas políticas.</span><span class="sxs-lookup"><span data-stu-id="ca4af-110">By default, custom policies take precedence over the default policy, but you can change the priority of your policies.</span></span> 
  
<span data-ttu-id="ca4af-111">Para obter mais informações sobre como configurar suas políticas contra spam, consulte os seguintes tópicos:</span><span class="sxs-lookup"><span data-stu-id="ca4af-111">For more about configuring your anti-spam policies, see the following topics:</span></span>
  
[<span data-ttu-id="ca4af-112">Configurar a política do filtro de conexão</span><span class="sxs-lookup"><span data-stu-id="ca4af-112">Configure the connection filter policy</span></span>](configure-the-connection-filter-policy.md)
  
[<span data-ttu-id="ca4af-113">Configurar suas políticas de filtro de spam</span><span class="sxs-lookup"><span data-stu-id="ca4af-113">Configure your spam filter policies</span></span>](configure-your-spam-filter-policies.md)
  
> [!IMPORTANT]
> <span data-ttu-id="ca4af-114">Para os clientes independentes do EOP: Por padrão, os filtros de conteúdo do EOP enviam as mensagens detectadas como spam para a pasta Lixo Eletrônico de cada destinatário.</span><span class="sxs-lookup"><span data-stu-id="ca4af-114">For EOP standalone customers: By default, the EOP content filters send spam-detected messages to each recipients' Junk Email folder.</span></span> <span data-ttu-id="ca4af-115">No enTanto, para garantir que a ação **mover mensagem para a pasta lixo eletrônico** funcione com caixas de correio locais, você deve configurar duas regras de fluxo de mensagens do Exchange (também conhecidas como regras de transporte) em seus servidores locais para detectar cabeçalhos de spam adicionados por EOP.</span><span class="sxs-lookup"><span data-stu-id="ca4af-115">However, in order to ensure that the **Move message to Junk Email folder** action will work with on-premises mailboxes, you must configure two Exchange mail flow rules (also known as transport rules) on your on-premises servers to detect spam headers added by EOP.</span></span> <span data-ttu-id="ca4af-116">Para obter detalhes, consulte [Garantir que o spam seja direcionado para a pasta Lixo Eletrônico de cada usuário](ensure-that-spam-is-routed-to-each-user-s-junk-email-folder.md).</span><span class="sxs-lookup"><span data-stu-id="ca4af-116">For details, see [Ensure that spam is routed to each user's Junk Email folder](ensure-that-spam-is-routed-to-each-user-s-junk-email-folder.md).</span></span> 
  
[<span data-ttu-id="ca4af-117">Configurar a política de spam de saída</span><span class="sxs-lookup"><span data-stu-id="ca4af-117">Configure the outbound spam policy</span></span>](configure-the-outbound-spam-policy.md)
  

