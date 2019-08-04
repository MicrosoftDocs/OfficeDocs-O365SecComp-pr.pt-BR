---
title: Gerente de conformidade da Microsoft e o RGPD
ms.author: robmazz
author: robmazz
manager: laurawi
audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: None
ROBOTS: NOINDEX, NOFOLLOW
ms.collection: M365-security-compliance
search.appverid:
- MOE150
- MET150
description: O Gerenciador de conformidade da Microsoft é uma ferramenta de avaliação de riscos gratuita baseada em fluxo de trabalho no portal de confiança do serviço Microsoft. O Gerenciador de conformidade permite que você rastreie, atribua e verifique as atividades de conformidade normativa relacionadas aos serviços em nuvem da Microsoft.
ms.openlocfilehash: af0efa2711215946930c091fc7c38cc1b9f575fd
ms.sourcegitcommit: f0d23e57b00f07cef5b1b2d366eaeeeacda37e3e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2019
ms.locfileid: "35786646"
---
# <a name="microsoft-compliance-manager-and-the-gdpr"></a><span data-ttu-id="dea77-104">Gerente de conformidade da Microsoft e o RGPD</span><span class="sxs-lookup"><span data-stu-id="dea77-104">Microsoft Compliance Manager and the GDPR</span></span>

<span data-ttu-id="dea77-105">A regulamentação geral de proteção de dados (RGPD), aprovada pela União Européia, pode impactar a estratégia de conformidade e exigir ações específicas para gerenciar as informações do usuário e do cliente usadas no Gerenciador de conformidade.</span><span class="sxs-lookup"><span data-stu-id="dea77-105">The General Data Protection Regulation (GDPR) enacted by the European Union can impact your compliance strategy and mandate specific actions to manage user and customer information used in Compliance Manager.</span></span>

## <a name="user-privacy-settings"></a><span data-ttu-id="dea77-106">Configurações de privacidade do usuário</span><span class="sxs-lookup"><span data-stu-id="dea77-106">User Privacy settings</span></span>

<span data-ttu-id="dea77-107">Determinadas regulamentações exigem que uma organização seja capaz de excluir dados de histórico do usuário.</span><span class="sxs-lookup"><span data-stu-id="dea77-107">Certain regulations require that an organization must be able to delete user history data.</span></span> <span data-ttu-id="dea77-108">O Gerenciador de conformidade fornece funções de **configurações de privacidade do usuário** que permitem aos administradores:</span><span class="sxs-lookup"><span data-stu-id="dea77-108">Compliance Manager provides **User Privacy Settings** functions that allow administrators to:</span></span>
  
- [<span data-ttu-id="dea77-109">Procurar um usuário</span><span class="sxs-lookup"><span data-stu-id="dea77-109">Search for a user</span></span>](#search-for-a-user)
- [<span data-ttu-id="dea77-110">Exportar um relatório do histórico de dados da conta</span><span class="sxs-lookup"><span data-stu-id="dea77-110">Export a report of account data history</span></span>](#export-a-report-of-account-data-history)
- [<span data-ttu-id="dea77-111">Excluir o histórico de dados do usuário</span><span class="sxs-lookup"><span data-stu-id="dea77-111">Delete user data history</span></span>](#delete-user-data-history)
  
## <a name="search-for-a-user"></a><span data-ttu-id="dea77-112">Procurar um usuário</span><span class="sxs-lookup"><span data-stu-id="dea77-112">Search for a user</span></span>

<span data-ttu-id="dea77-113">Para procurar uma conta de usuário:</span><span class="sxs-lookup"><span data-stu-id="dea77-113">To search for a user account:</span></span>
  
1. <span data-ttu-id="dea77-114">Insira o alias de email do usuário (as informações à esquerda do símbolo @) e escolha o nome do domínio na lista de sufixos de domínio à direita.</span><span class="sxs-lookup"><span data-stu-id="dea77-114">Enter the user email alias (the information to the left of the @ symbol) and choose the domain name from the  domain suffix list on the right.</span></span> <span data-ttu-id="dea77-115">Para organizações com vários domínios registrados, verifique novamente o sufixo de nome de domínio para garantir que ele está correto.</span><span class="sxs-lookup"><span data-stu-id="dea77-115">For organizations with multiple registered domains, double check the domain name suffix to ensure that it is correct.</span></span>

2. <span data-ttu-id="dea77-116">Quando o nome de usuário for inserido corretamente, selecione **Pesquisar**.</span><span class="sxs-lookup"><span data-stu-id="dea77-116">When you have the username correctly entered, select **Search**.</span></span>

3. <span data-ttu-id="dea77-117">Para contas de usuário não retornadas, o ' usuário não encontrado ' é exibido na página.</span><span class="sxs-lookup"><span data-stu-id="dea77-117">For user accounts not returned, 'User not found' is displayed on the page.</span></span> <span data-ttu-id="dea77-118">Verifique as informações do endereço de email do usuário e faça as correções necessárias.</span><span class="sxs-lookup"><span data-stu-id="dea77-118">Check the user's email address information and make corrections as necessary.</span></span> <span data-ttu-id="dea77-119">Para repetir, selecione **Pesquisar**.</span><span class="sxs-lookup"><span data-stu-id="dea77-119">To retry, select **Search**.</span></span>

4. <span data-ttu-id="dea77-120">Para contas de usuário retornadas, o texto do botão muda de **pesquisa** para **limpo**.</span><span class="sxs-lookup"><span data-stu-id="dea77-120">For user accounts returned, the text of the button changes from **Search** to **Clear**.</span></span> <span data-ttu-id="dea77-121">Isso indica que a conta de usuário retornada é o contexto operacional para as funções adicionais e que essas funções se aplicam a essa conta de usuário.</span><span class="sxs-lookup"><span data-stu-id="dea77-121">This indicates that the returned user account is the operating context for the additional functions and that these functions apply to this user account.</span></span>

5. <span data-ttu-id="dea77-122">Para limpar os resultados da pesquisa e pesquisar um usuário diferente, selecione **limpar**.</span><span class="sxs-lookup"><span data-stu-id="dea77-122">To clear search results and search for a different user, select **Clear**.</span></span>

## <a name="export-a-report-of-account-data-history"></a><span data-ttu-id="dea77-123">Exportar um relatório do histórico de dados da conta</span><span class="sxs-lookup"><span data-stu-id="dea77-123">Export a report of account data history</span></span>

<span data-ttu-id="dea77-124">Para cada conta de usuário identificada, você pode gerar um relatório de dependências vinculadas a essa conta.</span><span class="sxs-lookup"><span data-stu-id="dea77-124">For each user account identified, you can generate a report of dependencies linked to this account.</span></span> <span data-ttu-id="dea77-125">Essas informações permitem que você reatribua itens de ação abertas ou assegure o acesso a evidências previamente carregadas.</span><span class="sxs-lookup"><span data-stu-id="dea77-125">This information allows you to reassign open Action Items or ensure access to previously uploaded evidence.</span></span>
  
 <span data-ttu-id="dea77-126">Para gerar e exportar um relatório:</span><span class="sxs-lookup"><span data-stu-id="dea77-126">To generate and export a report:</span></span>
  
1. <span data-ttu-id="dea77-127">Selecione **Exportar** para gerar e baixar um relatório dos itens de ação de controle do Gerenciador de conformidade atribuídos atualmente à conta de usuário retornada e a lista de documentos carregados por esse usuário.</span><span class="sxs-lookup"><span data-stu-id="dea77-127">Select **Export** to generate and download a report of the Compliance Manager control Action Items currently assigned to the returned user account, and the list of documents uploaded by that user.</span></span> <span data-ttu-id="dea77-128">Se não houver ações atribuídas ou documentos carregados, uma mensagem de erro diz "não há dados para este usuário".</span><span class="sxs-lookup"><span data-stu-id="dea77-128">If there are no assigned actions or uploaded documents, an error message states "No data for this user".</span></span>

2. <span data-ttu-id="dea77-129">O relatório é baixado no plano de fundo da janela ativa do navegador — se você não vir um pop-up de download que deseja verificar o histórico de download do seu navegador.</span><span class="sxs-lookup"><span data-stu-id="dea77-129">The report downloads in the background of the active browser window — if you don't see a download popup that you want to check your browser download history.</span></span>

3. <span data-ttu-id="dea77-130">Abra o documento para verificar os dados do relatório.</span><span class="sxs-lookup"><span data-stu-id="dea77-130">Open the document to review the report data.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="dea77-131">Os dados do relatório não são uma lista histórica que mantém e exibe as alterações de estado no histórico de atribuição de itens de ação.</span><span class="sxs-lookup"><span data-stu-id="dea77-131">The report data is not a historical list that retains and displays state changes to Action Item assignment history.</span></span> <span data-ttu-id="dea77-132">O relatório gerado é um instantâneo dos itens de ação de controle atribuídos no momento em que o relatório é executado (carimbo de data e hora gravados no relatório).</span><span class="sxs-lookup"><span data-stu-id="dea77-132">The generated report is a snapshot of the control Action Items assigned at the time that the report is run (date and time stamp written into the report).</span></span> <span data-ttu-id="dea77-133">Por exemplo, qualquer reatribuição subsequente de itens de ação resultará em diferentes dados de relatório de instantâneo se o relatório for gerado novamente para o mesmo usuário.</span><span class="sxs-lookup"><span data-stu-id="dea77-133">For example, any subsequent reassignment of Action Items result in different snapshot report data if the report is generated again for the same user.</span></span>
  
## <a name="delete-user-data-history"></a><span data-ttu-id="dea77-134">Excluir o histórico de dados do usuário</span><span class="sxs-lookup"><span data-stu-id="dea77-134">Delete user data history</span></span>

<span data-ttu-id="dea77-135">Define todos os itens de ação de controle atribuídos ao usuário retornado como ' não atribuído '.</span><span class="sxs-lookup"><span data-stu-id="dea77-135">Sets all control Action Items assigned to the returned user to 'unassigned'.</span></span> <span data-ttu-id="dea77-136">Define o valor **carregado por** para qualquer documento carregado pelo usuário retornado para "removido pelo usuário".</span><span class="sxs-lookup"><span data-stu-id="dea77-136">Sets the **uploaded by** value for any documents uploaded by the returned user to 'user removed'.</span></span>
  
<span data-ttu-id="dea77-137">Para excluir o item de ação da conta de usuário e o histórico de upload de documentos:</span><span class="sxs-lookup"><span data-stu-id="dea77-137">To delete the user account Action Item and document upload history:</span></span>
  
1. <span data-ttu-id="dea77-138">Selecione **excluir**.</span><span class="sxs-lookup"><span data-stu-id="dea77-138">Select **Delete**.</span></span>

    <span data-ttu-id="dea77-139">Uma caixa de diálogo de confirmação é exibida, "*isso remove todas as atribuições de item de ação de controle e o histórico de carregamento do documento para o usuário selecionado. Esta ação é permanente. Tem certeza de que deseja continuar?*"</span><span class="sxs-lookup"><span data-stu-id="dea77-139">A confirmation dialog is displayed, "*This removes all control Action Item assignments and the document upload history for the selected user. This action is permanent. Are you sure you want to continue?*"</span></span>

2. <span data-ttu-id="dea77-140">Para continuar, selecione **OK**; caso contrário, selecione **Cancelar**.</span><span class="sxs-lookup"><span data-stu-id="dea77-140">To continue select **OK**, otherwise select **Cancel**.</span></span>
