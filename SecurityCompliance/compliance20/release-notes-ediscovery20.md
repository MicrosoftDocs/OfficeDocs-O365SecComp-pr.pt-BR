---
title: Notas de versão para descoberta eletrônica avançada (versão prévia)
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
description: Este artigo contém as notas de versão da descoberta eletrônica avançada (versão prévia).
ms.openlocfilehash: 32a02c16fd30e740fcc6e1c99b46775b97590a28
ms.sourcegitcommit: 15202bba32313534da2478b0cd215f32a10c9ef4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/19/2019
ms.locfileid: "30684350"
---
# <a name="release-notes-for-advanced-ediscovery-preview"></a><span data-ttu-id="70006-103">Notas de versão para descoberta eletrônica avançada (versão prévia)</span><span class="sxs-lookup"><span data-stu-id="70006-103">Release notes for Advanced eDiscovery (Preview)</span></span>

<span data-ttu-id="70006-104">O programa de visualização pública para descoberta eletrônica avançada é a maneira de obter acesso antecipado à funcionalidade e às atualizações futuras.</span><span class="sxs-lookup"><span data-stu-id="70006-104">The Public Preview program for Advanced eDiscovery is the way to get early access to the upcoming functionality and updates.</span></span> <span data-ttu-id="70006-105">Para obter acesso antecipado aos recursos mais recentes, basta criar e usar um caso de descoberta eletrônica avançada (visualização) no centro de conformidade do & de segurança do Office 365.</span><span class="sxs-lookup"><span data-stu-id="70006-105">To get early access to the newest features, just create and use an Advanced eDiscovery (Preview) case in the Office 365 Security & Compliance Center.</span></span> <span data-ttu-id="70006-106">ConFira [criar um novo caso](create-new-ediscovery-case.md).</span><span class="sxs-lookup"><span data-stu-id="70006-106">See [Create a new case](create-new-ediscovery-case.md).</span></span>

## <a name="known-issues"></a><span data-ttu-id="70006-107">Problemas conhecidos</span><span class="sxs-lookup"><span data-stu-id="70006-107">Known issues</span></span>

<span data-ttu-id="70006-108">**Microsoft Forms**</span><span class="sxs-lookup"><span data-stu-id="70006-108">**Microsoft Forms**</span></span>

- <span data-ttu-id="70006-109">Os dados correspondentes a um formulário criado antes de 31 de janeiro de 2019 não poderão ser pesquisados ao usar a ferramenta de pesquisa na descoberta eletrônica avançada (visualização) para pesquisar caixas de correio.</span><span class="sxs-lookup"><span data-stu-id="70006-109">The data corresponding to a form created before January 31, 2019 will not be searchable when using the Search tool in Advanced eDiscovery (Preview) to search custodian mailboxes.</span></span> <span data-ttu-id="70006-110">Formulários criados após essa data estarão disponíveis para pesquisa.</span><span class="sxs-lookup"><span data-stu-id="70006-110">Forms created after this date will be available to search.</span></span>

- <span data-ttu-id="70006-111">Um formulário criado por um usuário ainda pode receber respostas, mesmo depois que o usuário que criou o formulário é excluído.</span><span class="sxs-lookup"><span data-stu-id="70006-111">A form created by a user can still receive responses even after the user who created the Form is deleted.</span></span> <span data-ttu-id="70006-112">No enTanto, os dados correspondentes para essas respostas (que ocorreram depois da exclusão da caixa de correio) não poderão ser pesquisados ao usar a ferramenta de pesquisa na descoberta eletrônica avançada (visualização) para pesquisar caixas de correio de responsáveis.</span><span class="sxs-lookup"><span data-stu-id="70006-112">However, the corresponding data for those responses (that occurred after the custodian mailbox was deleted) will not be searchable when using the Search tool in Advanced eDiscovery (Preview) to search custodian mailboxes.</span></span>
 
<span data-ttu-id="70006-113">**Microsoft Sway**</span><span class="sxs-lookup"><span data-stu-id="70006-113">**Microsoft Sway**</span></span>

- <span data-ttu-id="70006-114">Se um usuário editar um Sway imediatamente antes da exclusão da conta de usuário para o proprietário desse Sway, essas alterações poderão não ser pesquisadas ao usar a ferramenta de pesquisa na descoberta eletrônica avançada (visualização) para pesquisar caixas de correio de responsáveis.</span><span class="sxs-lookup"><span data-stu-id="70006-114">If a user edits a sway just prior to the deletion of the user account for the owner of that sway, then those changes may not be be searchable when using the Search tool in Advanced eDiscovery (Preview) to search custodian mailboxes.</span></span> <span data-ttu-id="70006-115">O Sway bloqueia alterações em um Sway assim que recebe um sinal de que a conta foi excluída.</span><span class="sxs-lookup"><span data-stu-id="70006-115">Sway blocks changes to to a sway as soon as it receives a signal that the account was deleted.</span></span> <span data-ttu-id="70006-116">No enTanto, há uma pequena chance de que um Sway possa ser editado antes que esse sinal seja recebido.</span><span class="sxs-lookup"><span data-stu-id="70006-116">However, there's a small chance that a sway can be edited before this signal is received.</span></span>

## <a name="issues-fixed-in-this-release"></a><span data-ttu-id="70006-117">Problemas corrigidos nesta versão</span><span class="sxs-lookup"><span data-stu-id="70006-117">Issues fixed in this release</span></span>

- <span data-ttu-id="70006-118">DCR: manipulação de exceção para itens não indexados e itens órfãos</span><span class="sxs-lookup"><span data-stu-id="70006-118">DCR: Exception handling for unindexed items and orphaned items</span></span>
- <span data-ttu-id="70006-119">DCR: notificações de bloqueio</span><span class="sxs-lookup"><span data-stu-id="70006-119">DCR: Hold notifications</span></span>
- <span data-ttu-id="70006-120">DCR: responsáveis pela descoberta eletrônica</span><span class="sxs-lookup"><span data-stu-id="70006-120">DCR: Custodians in eDiscovery</span></span>

## <a name="whats-new"></a><span data-ttu-id="70006-121">Novidades</span><span class="sxs-lookup"><span data-stu-id="70006-121">What’s new</span></span>

- <span data-ttu-id="70006-122">**Navegação reprojetada no centro de conformidade do & de segurança** – a descoberta eletrônica avançada (visualização) tem uma nova aparência.</span><span class="sxs-lookup"><span data-stu-id="70006-122">**Redesigned navigation in the Security & Compliance Center** – Advanced eDiscovery (Preview) has a new look and feel.</span></span> <span data-ttu-id="70006-123">Use a descoberta eletrônica avançada (versão prévia) para gerenciar mais de seu fluxo de trabalho de caso.</span><span class="sxs-lookup"><span data-stu-id="70006-123">Use Advanced eDiscovery (Preview) to manage more of your case workflow.</span></span>

- <span data-ttu-id="70006-124">**Gerenciamento de casos** – há suporte adicional para novos tipos de caso.</span><span class="sxs-lookup"><span data-stu-id="70006-124">**Case management** – There’s additional support for new case types.</span></span> <span data-ttu-id="70006-125">Você também pode selecionar e salvar seus casos recentes e favoritos.</span><span class="sxs-lookup"><span data-stu-id="70006-125">You can also select and save your recent and favorite cases.</span></span> <span data-ttu-id="70006-126">Controlar e monitorar a atividade em e entre casos usando novos painéis.</span><span class="sxs-lookup"><span data-stu-id="70006-126">Track and monitor activity within and across cases using new dashboards.</span></span>

- <span data-ttu-id="70006-127">**Gerenciamento de responsáveis** – adicione e remova usuários como responsáveis por dados em um caso.</span><span class="sxs-lookup"><span data-stu-id="70006-127">**Custodian management** – Add and remove users as data custodians within a case.</span></span>

- <span data-ttu-id="70006-128">**Integração com o Exchange, o onedrive e** o Teams – adicione automaticamente a caixa de correio de um usuário, a conta do onedrive for Business e os sites do Microsoft Teams a uma ocorrência.</span><span class="sxs-lookup"><span data-stu-id="70006-128">**Exchange, OneDrive, and Teams Integration** – Automatically add a user’s current mailbox, OneDrive for Business account, and Microsoft Teams sites to a case.</span></span> 

- <span data-ttu-id="70006-129">**Comunicações de responsáveis** – envie e gerencie notificações de retenção legal em nome da sua organização.</span><span class="sxs-lookup"><span data-stu-id="70006-129">**Custodian communications** – Send and manage legal hold notifications on behalf of your organization.</span></span>

- <span data-ttu-id="70006-130">**Portal de responsáveis** – novo portal para que os responsáveis acessem seus avisos de isenção ativos.</span><span class="sxs-lookup"><span data-stu-id="70006-130">**Custodian portal** – New portal for custodians to access their active hold notices.</span></span>

- <span data-ttu-id="70006-131">**IndexAção profunda** – Rastreie novamente os itens parcialmente indexados sob demanda.</span><span class="sxs-lookup"><span data-stu-id="70006-131">**Deep indexing** – Re-crawl partially indexed items on demand.</span></span>

- <span data-ttu-id="70006-132">**Correção de erro** : corrigir ou baixar erros de processamento; Isso inclui suporte de correção para tipos de arquivo grandes, arquivos protegidos por senha e muito mais.</span><span class="sxs-lookup"><span data-stu-id="70006-132">**Error remediation** – Remediate or download processing errors; this include remediation support for large file types, password protected files, and more.</span></span> 

- <span data-ttu-id="70006-133">**Melhorias na pesquisa** – crie uma pesquisa identificando os responsáveis e/ou locais.</span><span class="sxs-lookup"><span data-stu-id="70006-133">**Improvements to search** – Create a search by identifying custodians and/or locations.</span></span>

- <span data-ttu-id="70006-134">**Conjuntos de trabalho** – gerencie, rastreie e faça auditoria de conjuntos estáticos de documentos.</span><span class="sxs-lookup"><span data-stu-id="70006-134">**Working sets** – Manage, track, and audit static sets of documents.</span></span>

- <span data-ttu-id="70006-135">**Revisão** – use um modo de exibição nativo, de texto e quase nativo para revisar os documentos adicionados ao seu conjunto de trabalho.</span><span class="sxs-lookup"><span data-stu-id="70006-135">**Review** – Use a native, text, and near-native view to review documents added to your working set.</span></span>

- <span data-ttu-id="70006-136">**Redigir, marcar e anotar** – redigir texto, aplicar marcas e fazer anotações à medida que você revisar documentos.</span><span class="sxs-lookup"><span data-stu-id="70006-136">**Redact, tag, and annotate** – Redact text, apply tags, and make annotations as you review documents.</span></span>
  
- <span data-ttu-id="70006-137">**Análise com capacidade para análise**– Aproveite a análise de descoberta eletrônica para localizar, Pesquisar e examinar os resultados em um conjunto de trabalho.</span><span class="sxs-lookup"><span data-stu-id="70006-137">**Analytics-powered review**– Leverage eDiscovery analytics to find, search, and cull results within a working set.</span></span>

- <span data-ttu-id="70006-138">**Jobs** – rastreie o status de processos de execução longa.</span><span class="sxs-lookup"><span data-stu-id="70006-138">**Jobs** – Track status of long-running processes.</span></span>

- <span data-ttu-id="70006-139">**Novas atividades de auditoria** – rastrear e exibir novas atividades de auditoria para descoberta eletrônica avançada.</span><span class="sxs-lookup"><span data-stu-id="70006-139">**New audit activities** – Track and view new audit activity for Advanced eDiscovery.</span></span>
