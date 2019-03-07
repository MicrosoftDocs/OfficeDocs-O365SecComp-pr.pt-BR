---
title: Visão geral do gerenciador de planos de arquivo
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: 9/25/2018
ms.audience: Admin
ms.topic: conceptual
ms.service: O365-seccomp
localization_priority: Priority
ms.collection: M365-security-compliance
search.appverid:
- MOE150
- MET150
ms.assetid: af398293-c69d-465e-a249-d74561552d30
description: O gerenciador de planos de arquivo fornece recursos avançados de gerenciamento de políticas e rótulos de retenção, e oferece uma maneira integrada de percorrer a atividade de rótulos e de rótulo para conteúdo para todo o seu ciclo de vida de conteúdo, desde a criação à colaboração, à declaração de registros, à retenção e por fim a disposição.
ms.openlocfilehash: d972a7ea6507e51c4efaaef30c98d55a87912417
ms.sourcegitcommit: 6aa82374eef09d2c1921f93bda3eabeeb28aadeb
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/06/2019
ms.locfileid: "30454823"
---
# <a name="overview-of-file-plan-manager"></a><span data-ttu-id="b8200-103">Visão geral do gerenciador de planos de arquivo</span><span class="sxs-lookup"><span data-stu-id="b8200-103">Overview of file plan manager</span></span>

<span data-ttu-id="b8200-104">O gerenciador de planos de arquivo fornece recursos avançados de gerenciamento de políticas e rótulos de retenção, e oferece uma maneira integrada de percorrer a atividade de rótulos e de rótulo para conteúdo para todo o seu ciclo de vida de conteúdo, desde a criação à colaboração, à declaração de registros, à retenção e por fim a disposição.</span><span class="sxs-lookup"><span data-stu-id="b8200-104">File plan manager provides advanced management capabilities for retention labels and policies, and provides an integrated way to traverse label and label-to-content activity for your entire content lifecycle – from creation, through collaboration, record declaration, retention, and finally disposition.</span></span>

![Página de plano de arquivo](media/file-plan-page.png)

## <a name="accessing-file-plan-manager"></a><span data-ttu-id="b8200-106">Acessar o gerenciador de planos de arquivo</span><span class="sxs-lookup"><span data-stu-id="b8200-106">Accessing file plan manager</span></span>

<span data-ttu-id="b8200-107">Há dois requisitos para acessar o gerenciador de planos de arquivo, que são:</span><span class="sxs-lookup"><span data-stu-id="b8200-107">There are two requirements to access file plan manager, they are:</span></span>
- <span data-ttu-id="b8200-108">Uma assinatura do Office 365 Enterprise E5.</span><span class="sxs-lookup"><span data-stu-id="b8200-108">An Office 365 Enterprise E5 subscription.</span></span>
- <span data-ttu-id="b8200-109">O usuário ter recebido uma das seguintes funções do Centro de Conformidade e Segurança:</span><span class="sxs-lookup"><span data-stu-id="b8200-109">The user has been in assigned one of the following roles of the Security &amp; Compliance Center:</span></span> 
    - <span data-ttu-id="b8200-110">Gerenciador de Retenção</span><span class="sxs-lookup"><span data-stu-id="b8200-110">Retention Manager</span></span>
    - <span data-ttu-id="b8200-111">Gerenciador de Retenção somente exibição</span><span class="sxs-lookup"><span data-stu-id="b8200-111">View-only Retention Manager</span></span>

## <a name="navigating-your-file-plan"></a><span data-ttu-id="b8200-112">Navegar pelo plano de arquivo</span><span class="sxs-lookup"><span data-stu-id="b8200-112">Navigating your file plan</span></span>

<span data-ttu-id="b8200-113">O gerente de plano de arquivo torna mais fácil ver todas as configurações dos seus rótulos e políticas de retenção no mesmo modo de exibição.</span><span class="sxs-lookup"><span data-stu-id="b8200-113">File plan manager makes it easier see into and across the settings of all your retention labels and policies from one view.</span></span>

<span data-ttu-id="b8200-114">Observe que os rótulos de retenção criados fora do plano de arquivamento estarão disponíveis no plano de arquivamento e vice-versa.</span><span class="sxs-lookup"><span data-stu-id="b8200-114">Note that retention labels created outside of the file plan will be available in the file plan and vice versa.</span></span>

<span data-ttu-id="b8200-115">Na guia **rótulos de plano de arquivo**, as seguintes informações e recursos adicionais estão disponíveis:</span><span class="sxs-lookup"><span data-stu-id="b8200-115">On the **file plan labels** tab, the following additional information and capabilities are available:</span></span>

### <a name="label-settings-columns"></a><span data-ttu-id="b8200-116">Colunas de configurações de rótulo</span><span class="sxs-lookup"><span data-stu-id="b8200-116">Label settings columns</span></span>
 
- <span data-ttu-id="b8200-p101">**Com base em** identifica o tipo de gatilho que iniciará o período de retenção. Os valores válidos estão:</span><span class="sxs-lookup"><span data-stu-id="b8200-p101">**Based on** identifies the type of trigger that will start the retention period. Valid values are:</span></span> 
    - <span data-ttu-id="b8200-119">Evento</span><span class="sxs-lookup"><span data-stu-id="b8200-119">Event</span></span>
    - <span data-ttu-id="b8200-120">Data de criação</span><span class="sxs-lookup"><span data-stu-id="b8200-120">When created</span></span>
    - <span data-ttu-id="b8200-121">Data da última modificação</span><span class="sxs-lookup"><span data-stu-id="b8200-121">When last modified</span></span>
    - <span data-ttu-id="b8200-122">Data do rótulo</span><span class="sxs-lookup"><span data-stu-id="b8200-122">When labeled</span></span>
- <span data-ttu-id="b8200-p102">**Registro** identifica se o item se tornará um registro declarado quando o rótulo for aplicado. Os valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="b8200-p102">**Record** identifies if the item will become a declared record when the label is applied. Valid values are:</span></span>
    - <span data-ttu-id="b8200-125">Não</span><span class="sxs-lookup"><span data-stu-id="b8200-125">No</span></span>
    - <span data-ttu-id="b8200-126">Sim</span><span class="sxs-lookup"><span data-stu-id="b8200-126">Yes</span></span>
    - <span data-ttu-id="b8200-127">Sim (Regulatório)</span><span class="sxs-lookup"><span data-stu-id="b8200-127">Yes(Regulatory)</span></span>
- <span data-ttu-id="b8200-p103">**Retenção** identifica o tipo de retenção. Os valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="b8200-p103">**Retention** identifies the retention type. Valid values are:</span></span>
    - <span data-ttu-id="b8200-130">Manter</span><span class="sxs-lookup"><span data-stu-id="b8200-130">Keep</span></span>
    - <span data-ttu-id="b8200-131">Manter e excluir</span><span class="sxs-lookup"><span data-stu-id="b8200-131">Keep and delete</span></span>
    - <span data-ttu-id="b8200-132">Excluir</span><span class="sxs-lookup"><span data-stu-id="b8200-132">Delete</span></span>
- <span data-ttu-id="b8200-p104">**Descarte** identifica o que acontecerá com o conteúdo no final do período de retenção. Os valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="b8200-p104">**Disposition** identifies what will happen to the content at the end of the retention period. Valid values are:</span></span> 
    - <span data-ttu-id="b8200-135">null</span><span class="sxs-lookup"><span data-stu-id="b8200-135">null</span></span>
    - <span data-ttu-id="b8200-136">Nenhuma ação</span><span class="sxs-lookup"><span data-stu-id="b8200-136">No action</span></span>
    - <span data-ttu-id="b8200-137">Excluir automaticamente</span><span class="sxs-lookup"><span data-stu-id="b8200-137">Auto-delete</span></span>
    - <span data-ttu-id="b8200-138">Revisão obrigatória (também conhecida como revisão de descarte)</span><span class="sxs-lookup"><span data-stu-id="b8200-138">Review required (aka Disposition review)</span></span>

![Configurações de rótulos no plano de arquivo](media/file-plan-label-columns.png)

### <a name="label-file-plan-descriptors-columns"></a><span data-ttu-id="b8200-140">Etiqueta plano de arquivo descritores colunas</span><span class="sxs-lookup"><span data-stu-id="b8200-140">Label file plan descriptors columns</span></span>

<span data-ttu-id="b8200-p105">Agora você pode incluir mais informações na configuração das suas etiquetas de retenção. Inserir descritores de plano de arquivo em rótulos melhora o gerenciamento e a organização do seu plano de arquivamento.</span><span class="sxs-lookup"><span data-stu-id="b8200-p105">You can now include more information in the configuration of your retention labels. Inserting file plan descriptors into labels will improve the manageability and organization of your file plan.</span></span>

<span data-ttu-id="b8200-p106">Para começar, o gerenciador de planos de arquivo fornece alguns valores prontos de origem para: Função/departamento, Categoria, Tipo de autoridade e Provisão/citação. Você pode adicionar novos valores descritores de planos de arquivo ao criar ou editar um rótulo de retenção.</span><span class="sxs-lookup"><span data-stu-id="b8200-p106">To get you started, file plan manager provides some out-of-box values for: Function/department, Category, Authority type and Provision/citation. You can add new file plan descriptor values when creating or editing a retention label.</span></span>

<span data-ttu-id="b8200-145">Aqui está uma visão geral da etapa de descritores de plano de arquivo ao criar ou editar um rótulo de retenção.</span><span class="sxs-lookup"><span data-stu-id="b8200-145">Here's a view of the file plan descriptors step when creating or editing a retention label.</span></span>

![Descritores de plano de arquivo](media/file-plan-descriptors.png)

<span data-ttu-id="b8200-147">Aqui está um modo de exibição das colunas de descritores de plano de arquivo na guia Rótulos do gerenciador de planos de arquivo.</span><span class="sxs-lookup"><span data-stu-id="b8200-147">Here's a view of the file plan descriptors columns on the labels tab of file plan manager.</span></span>

![file-plan-descriptors-on-labels-tab.png](media/file-plan-descriptors-on-labels-tab.png)

## <a name="export-labels-out-of-your-file-plan"></a><span data-ttu-id="b8200-149">Exportar rótulos do seu plano de arquivo</span><span class="sxs-lookup"><span data-stu-id="b8200-149">Export labels out of your file plan</span></span>

<span data-ttu-id="b8200-150">No gerenciador de planos de arquivo, você pode exportar os detalhes de todos os rótulos de retenção para um arquivo .csv, para ajudá-lo a facilitar as avaliações de conformidade periódicas com os participantes de governança de dados na sua organização.</span><span class="sxs-lookup"><span data-stu-id="b8200-150">From file plan manager, you can export the details of all retention labels into a .csv file to assist you in facilitating periodic compliance reviews with data governance stakeholders in your organization.</span></span>

<span data-ttu-id="b8200-151">Para exportar todos os rótulos de retenção, acesse **gerenciador de planos de arquivo** \> **ações de plano de arquivo** \> **exportar rótulos**.</span><span class="sxs-lookup"><span data-stu-id="b8200-151">To export all retention labels, go to **file plan manager** \> **file plan actions** \> **export labels**.</span></span>

![Opção para exportar o plano de arquivo](media/file-plan-export-labels-option.png)

<span data-ttu-id="b8200-153">Um arquivo \*.csv que contém todos os rótulos de retenção existentes será aberto.</span><span class="sxs-lookup"><span data-stu-id="b8200-153">A \*.csv file containing all existing retention labels will open.</span></span>

![Arquivo CSV mostrando todas as etiquetas de retenção](media/file-plan-csv-file.png)

## <a name="import-labels-into-your-file-plan"></a><span data-ttu-id="b8200-155">Importar rótulos para seu plano de arquivo</span><span class="sxs-lookup"><span data-stu-id="b8200-155">Import labels into your file plan</span></span>

<span data-ttu-id="b8200-156">No gerenciador de planos de arquivo, você pode importar em massa novos rótulos, bem como modificar rótulos de retenção existentes.</span><span class="sxs-lookup"><span data-stu-id="b8200-156">From file plan manager, you can bulk import new labels as well as modify existing retention labels.</span></span>

<span data-ttu-id="b8200-157">Para importar novos rótulos de retenção e fazer atualizações aos rótulos de retenção existentes, acesse **gerenciador de planos de arquivo** \> **ações de plano de arquivo** \> **importar rótulos**.</span><span class="sxs-lookup"><span data-stu-id="b8200-157">To import new retention labels and make updates existing retention labels, go to **file plan manager** \> **file plan actions** \> **import labels**.</span></span>

![Opção para importar plano de arquivo](media/file-plan-import-labels-option.png)

![Opção para baixar um modelo de plano de arquivo em branco](media/file-plan-blank-template-option.png)

<span data-ttu-id="b8200-160">Baixar um modelo em branco (ou começar com base em uma exportação do seu plano de arquivo atual).</span><span class="sxs-lookup"><span data-stu-id="b8200-160">Download a blank template (or start from an export of your current file plan).</span></span>

![Modelo de plano de arquivo em branco aberto no Excel](media/file-plan-blank-template.png)

<span data-ttu-id="b8200-162">Preencha o modelo de discagem (em breve, estarão disponíveis informações de referência sobre os valores válidos para entradas).</span><span class="sxs-lookup"><span data-stu-id="b8200-162">Fill-out the template (coming soon is reference information about valid values for entries).</span></span>

![Modelo de plano de arquivo com as informações preenchidas](media/file-plan-filled-out-template.png)

<span data-ttu-id="b8200-164">Carregue o modelo preenchido, e o gerenciador de plano de arquivo validará as entradas e exibirá as estatísticas de importação.</span><span class="sxs-lookup"><span data-stu-id="b8200-164">Upload the filled-out template, and file plan manager will validate the entries and display import statistics.</span></span>

![Estatísticas de importação de plano de arquivo](media/file-plan-import-statistics.png)

<span data-ttu-id="b8200-166">Quando a instalação for concluída, volte para o gerenciador de planos de arquivo e atribua novos rótulos às políticas novas ou existentes.</span><span class="sxs-lookup"><span data-stu-id="b8200-166">When the import is complete, return to file plan manager to assign new labels to new or existing policies.</span></span>

![Opção para publicar rótulos](media/file-plan-publish-labels-option.png)

