---
title: Notas de versão do Gerenciador de conformidade da Microsoft
ms.author: robmazz
author: robmazz
manager: laurawi
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: M365-security-compliance
search.appverid:
- MOE150
- MET150
description: O Gerenciador de conformidade da Microsoft é uma ferramenta de avaliação de riscos gratuita baseada em fluxo de trabalho no portal de confiança do serviço Microsoft. O Gerenciador de conformidade permite que você rastreie, atribua e verifique as atividades de conformidade normativa relacionadas aos serviços em nuvem da Microsoft.
ms.openlocfilehash: 5e18445e3f9ad2848f18174788ec6dd40bc4a178
ms.sourcegitcommit: 696c1ed6b270be3f9da7395b49a7d8fec98e6db0
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/29/2019
ms.locfileid: "33472986"
---
# <a name="release-notes-for-compliance-manager-preview"></a><span data-ttu-id="8f200-104">Notas de versão do Gerenciador de conformidade (visualização)</span><span class="sxs-lookup"><span data-stu-id="8f200-104">Release Notes for Compliance Manager (Preview)</span></span>

<span data-ttu-id="8f200-105">A visualização pública do Gerenciador de conformidade fornece acesso antecipado às futuras funcionalidades e atualizações.</span><span class="sxs-lookup"><span data-stu-id="8f200-105">The public preview of Compliance Manager provides you with early access to upcoming functionality and updates.</span></span>

<span data-ttu-id="8f200-106">Você pode usar a ferramenta atualizada do [Gerenciador de conformidade](https://servicetrust.microsoft.com/ComplianceManager) no portal de [confiança do serviço](https://servicetrust.microsoft.com) para rastrear, atribuir e verificar as atividades de conformidade regulatória relacionadas aos serviços de nuvem da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="8f200-106">You can use the updated [Compliance Manager](https://servicetrust.microsoft.com/ComplianceManager) tool on the [Service Trust Portal](https://servicetrust.microsoft.com) to track, assign, and verify regulatory compliance activities related to Microsoft cloud services.</span></span>

## <a name="whats-new-in-compliance-manager-preview"></a><span data-ttu-id="8f200-107">O que há de novo no Gerenciador de conformidade (versão prévia)</span><span class="sxs-lookup"><span data-stu-id="8f200-107">What’s new in Compliance Manager (Preview)</span></span>

- <span data-ttu-id="8f200-108">**Integração com a pontuação segura da Microsoft:** O Gerenciador de conformidade oferece suporte à integração com a [Pontuação segura da Microsoft](microsoft-secure-score.md) , mapeaNdo as ações gerenciadas pelo cliente para mais de 50 de Pontuação segura.</span><span class="sxs-lookup"><span data-stu-id="8f200-108">**Integration with Microsoft Secure Score:** Compliance Manager supports integration with [Microsoft Secure Score](microsoft-secure-score.md) by mapping customer-managed Actions to more than 50 Secure Score actions.</span></span> <span data-ttu-id="8f200-109">Quando você completa uma ação mapeada na pontuação segura, a ação correspondente do Gerenciador de conformidade é atualizada automaticamente.</span><span class="sxs-lookup"><span data-stu-id="8f200-109">When you complete a mapped action in Secure Score, the corresponding Compliance Manager Action is automatically updated.</span></span>

- <span data-ttu-id="8f200-110">**Importe avaliações personalizadas:** Além das avaliações internas, o Gerenciador de conformidade agora oferece suporte à importação de modelos personalizados, permitindo que você crie avaliações personalizadas para qualquer produto ou serviço e qualquer padrão ou regulamentação.</span><span class="sxs-lookup"><span data-stu-id="8f200-110">**Import custom Assessments:** In addition to built-in Assessments, Compliance Manager now supports importing custom Templates, enabling you to create custom Assessments for any product or service and any standard or regulation.</span></span>

- <span data-ttu-id="8f200-111">**Itens de ações:** Os itens de ação agora são itens individuais e muitos incluem coleção de telemetria da API do Microsoft Secure Score Graph.</span><span class="sxs-lookup"><span data-stu-id="8f200-111">**Actions Items:** Action Items are now individual items and many include telemetry collection from the Microsoft Secure Score Graph API.</span></span> <span data-ttu-id="8f200-112">Sempre que possível, as recomendações de ações técnicas agora têm links para a página de configuração aplicável no serviço do Office 365.</span><span class="sxs-lookup"><span data-stu-id="8f200-112">Where possible, technical action recommendations now have links to the applicable configuration page in the Office 365 service.</span></span>

- <span data-ttu-id="8f200-113">**Gerenciamento de locatário:** Nova interface para gerenciar novos elementos de dados no Gerenciador de conformidade (visualização):</span><span class="sxs-lookup"><span data-stu-id="8f200-113">**Tenant Management:** New interface for managing new data elements in Compliance Manager (Preview):</span></span>
    - <span data-ttu-id="8f200-114">**Dimensões:** Exibir, adicionar e personalizar metadados para modelos, avaliações e itens de ação que permitem que você crie pivôs personalizados para filtros.</span><span class="sxs-lookup"><span data-stu-id="8f200-114">**Dimensions:** View, add and customize metadata for Templates, Assessments, and Action Items that allow you to create custom pivots for filters.</span></span>
    - <span data-ttu-id="8f200-115">**Proprietários:** Especifique um proprietário para cada item de ação.</span><span class="sxs-lookup"><span data-stu-id="8f200-115">**Owners:** Specify an owner for each Action Item.</span></span>
    - <span data-ttu-id="8f200-116">**Ações do cliente:** Gerencie a lista completa de itens de ações incluídas no Gerenciador de conformidade (visualização) e habilite/desabilite o monitoramento de Pontuação segura para itens de ação que estão integrados à pontuação segura.</span><span class="sxs-lookup"><span data-stu-id="8f200-116">**Customer Actions:** Manage the complete list of Actions Items included in Compliance Manager (Preview) and enable/disable Secure Score monitoring for Action Items that are integrated with Secure Score.</span></span>

- <span data-ttu-id="8f200-117">**Pontuação de conformidade atualizada**: a metodologia mudou para suportar a sincronização com a pontuação segura da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="8f200-117">**Updated Compliance Score**: The methodology has changed to support syncing with Microsoft Secure Score.</span></span> <span data-ttu-id="8f200-118">O sistema de Pontuação remove os créditos de controle gerenciados pela Microsoft e se concentra apenas na conclusão dos controles gerenciados pelo cliente.</span><span class="sxs-lookup"><span data-stu-id="8f200-118">The scoring system removes the Microsoft-managed control credits and focuses solely on the completion of customer-managed controls.</span></span>

## <a name="known-issues-in-compliance-manager-preview"></a><span data-ttu-id="8f200-119">Problemas conhecidos no gerente de conformidade (visualização)</span><span class="sxs-lookup"><span data-stu-id="8f200-119">Known issues in Compliance Manager (Preview)</span></span>

<span data-ttu-id="8f200-120">As seções a seguir abordam problemas conhecidos a serem resolvidos em futuras versões do Gerenciador de conformidade.</span><span class="sxs-lookup"><span data-stu-id="8f200-120">The following sections cover known issues to be resolved in upcoming releases of Compliance Manager.</span></span>

### <a name="compliance-score"></a><span data-ttu-id="8f200-121">Pontuação de conformidade</span><span class="sxs-lookup"><span data-stu-id="8f200-121">Compliance Score</span></span>

- <span data-ttu-id="8f200-122">Quando os itens de ação são marcados como **não no escopo**, a pontuação atribuída ao item de ação não é excluída do cálculo da Pontuação de conformidade.</span><span class="sxs-lookup"><span data-stu-id="8f200-122">When Action Items are marked as **Not in Scope**, the score assigned to the Action Item is not excluded from the Compliance Score calculation.</span></span> <span data-ttu-id="8f200-123">Itens de ação marcados como **não no escopo** não devem aumentar a pontuação de conformidade.</span><span class="sxs-lookup"><span data-stu-id="8f200-123">Action Items marked **Not in Scope** should not increase your Compliance Score.</span></span>

### <a name="microsoft-managed-controls"></a><span data-ttu-id="8f200-124">Controles gerenciados pela Microsoft</span><span class="sxs-lookup"><span data-stu-id="8f200-124">Microsoft-managed Controls</span></span>

- <span data-ttu-id="8f200-125">A data de teste dos controles gerenciados pela Microsoft não aparecerá na interface do usuário, mesmo quando estiver incluída na avaliação.</span><span class="sxs-lookup"><span data-stu-id="8f200-125">The test date for Microsoft-managed controls is not appearing in the UI, even when included in the Assessment.</span></span> <span data-ttu-id="8f200-126">Para ver as informações de data de teste, você deve exportar a avaliação.</span><span class="sxs-lookup"><span data-stu-id="8f200-126">To see test date information, you must export the Assessment.</span></span>

### <a name="customization"></a><span data-ttu-id="8f200-127">Personalização</span><span class="sxs-lookup"><span data-stu-id="8f200-127">Customization</span></span>

- <span data-ttu-id="8f200-128">Adicionar controles personalizados permite adicionar um novo controle a uma família de controles existente, mas não permite que você adicione uma nova família de controle.</span><span class="sxs-lookup"><span data-stu-id="8f200-128">Adding custom Controls enables adding a new control to an existing control family, but it does not allow you to add a new Control Family.</span></span>
- <span data-ttu-id="8f200-129">Esta versão não dá suporte à vinculação de itens de ação ou à adição de itens de ações ou controles a uma avaliação.</span><span class="sxs-lookup"><span data-stu-id="8f200-129">This release does not support linking Action Items or adding Actions Items or Controls to an Assessment.</span></span>
- <span data-ttu-id="8f200-130">Se você criar uma ação personalizada, não será possível editá-la ou excluí-la.</span><span class="sxs-lookup"><span data-stu-id="8f200-130">If you create a custom Action, you cannot edit or delete it.</span></span>

### <a name="control-families-not-shown-in-assessments"></a><span data-ttu-id="8f200-131">Famílias de controle não exibidas em avaliações</span><span class="sxs-lookup"><span data-stu-id="8f200-131">Control Families Not Shown in Assessments</span></span>

- <span data-ttu-id="8f200-132">Quando você importa um modelo, todas as avaliações baseadas nesse modelo refletirão todas as famílias de controle que fazem parte do modelo.</span><span class="sxs-lookup"><span data-stu-id="8f200-132">When you import a Template, all Assessments based on that Template will reflect all Control Families that are part of the Template.</span></span> <span data-ttu-id="8f200-133">Mas se você adicionar novas famílias de controle ao modelo, qualquer avaliação existente não refletirá as alterações.</span><span class="sxs-lookup"><span data-stu-id="8f200-133">But if you add new Control Families to the Template, any existing Assessments will not reflect the changes.</span></span> <span data-ttu-id="8f200-134">Somente as novas avaliações criadas a partir do modelo atualizado refletirão as alterações.</span><span class="sxs-lookup"><span data-stu-id="8f200-134">Only new Assessments created off the updated Template will reflect the changes.</span></span>

### <a name="filters"></a><span data-ttu-id="8f200-135">Filtros</span><span class="sxs-lookup"><span data-stu-id="8f200-135">Filters</span></span>

- <span data-ttu-id="8f200-136">A filtragem em itens de ação ou controles não produz resultados corretos de forma consistente.</span><span class="sxs-lookup"><span data-stu-id="8f200-136">Filtering on Action Items or Controls does not consistently produce correct results.</span></span>

### <a name="templates"></a><span data-ttu-id="8f200-137">Modelos</span><span class="sxs-lookup"><span data-stu-id="8f200-137">Templates</span></span>

- <span data-ttu-id="8f200-138">Os modelos arquivados são editáveis e não devem ser editáveis.</span><span class="sxs-lookup"><span data-stu-id="8f200-138">Archived templates are editable and they should not be editable.</span></span>
- <span data-ttu-id="8f200-139">Os modelos bloqueados permitem a criação da avaliação, quando não deveriam.</span><span class="sxs-lookup"><span data-stu-id="8f200-139">Locked templates allow for Assessment creation when they should not.</span></span> <span data-ttu-id="8f200-140">Bloquear um modelo é destinado a impedir que ele seja usado para criar avaliações.</span><span class="sxs-lookup"><span data-stu-id="8f200-140">Locking a Template is meant to prevent it from being used to create Assessments.</span></span>

### <a name="export"></a><span data-ttu-id="8f200-141">Exportar</span><span class="sxs-lookup"><span data-stu-id="8f200-141">Export</span></span>

- <span data-ttu-id="8f200-142">O modelo exportar para JSON falha quando o status do modelo é \*\*\*\* definido como importado ou com **aprovação pendente**.</span><span class="sxs-lookup"><span data-stu-id="8f200-142">Template export to JSON fails when the template status is set to **Imported** or **Pending Approval**.</span></span>

### <a name="supported-browsers"></a><span data-ttu-id="8f200-143">Navegadores com suporte</span><span class="sxs-lookup"><span data-stu-id="8f200-143">Supported browsers</span></span>

- <span data-ttu-id="8f200-144">As versões mais recentes do Microsoft Edge, do Chrome e do Safari são suportadas.</span><span class="sxs-lookup"><span data-stu-id="8f200-144">The latest versions of Microsoft Edge, Chrome, and Safari are supported.</span></span>
- <span data-ttu-id="8f200-145">Pode haver casos em que os dados atualizados não aparecem até que seu navegador seja atualizado.</span><span class="sxs-lookup"><span data-stu-id="8f200-145">There may be instances where updated data does not appear until your browser is refreshed.</span></span>
- <span data-ttu-id="8f200-146">A versão de visualização do Microsoft Edge não é suportada, mas não tem problemas conhecidos.</span><span class="sxs-lookup"><span data-stu-id="8f200-146">The preview version of Microsoft Edge is not supported but has no known issues.</span></span>
- <span data-ttu-id="8f200-147">Não há suporte para o Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="8f200-147">Internet Explorer is not supported.</span></span>

### <a name="session-timeout"></a><span data-ttu-id="8f200-148">Tempo limite da sessão</span><span class="sxs-lookup"><span data-stu-id="8f200-148">Session timeout</span></span>

- <span data-ttu-id="8f200-149">Quando uma sessão expira, um erro "algo deu errado" pode ser exibido.</span><span class="sxs-lookup"><span data-stu-id="8f200-149">When a session times out, a “Something went wrong” error may appear.</span></span> <span data-ttu-id="8f200-150">Para resolver, vá para o [Gerenciador de conformidade](https://servicetrust.microsoft.com/ComplianceManager) e faça login novamente.</span><span class="sxs-lookup"><span data-stu-id="8f200-150">To resolve, go to [Compliance Manager](https://servicetrust.microsoft.com/ComplianceManager) and log in again.</span></span>