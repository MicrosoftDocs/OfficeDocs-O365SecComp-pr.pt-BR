---
title: Definir palavras-chave realçadas e opções avançadas na descoberta eletrônica avançada do Office 365
ms.author: chrfox
author: chrfox
manager: laurawi
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: 03cc4387-2c7d-4058-8a44-0deefb58f011
description: 'Saiba como adicionar palavras-chave definidas pelo usuário à relevância para ajudar a identificar arquivos relevantes durante a marcação na descoberta eletrônica avançada do Office 365 e especificar os parâmetros de custo.  '
ms.openlocfilehash: aec9efac91cc3fb48068fca9b6b7313f829f4fe2
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32257062"
---
# <a name="define-highlighted-keywords-and-advanced-options-in-office-365-advanced-ediscovery"></a><span data-ttu-id="ec350-103">Definir palavras-chave realçadas e opções avançadas na descoberta eletrônica avançada do Office 365</span><span class="sxs-lookup"><span data-stu-id="ec350-103">Define highlighted keywords and advanced options in Office 365 Advanced eDiscovery</span></span>

> [!NOTE]
> <span data-ttu-id="ec350-p101">A Descoberta Eletrônica Avançada exige um Office 365 E3, com um complemento de Conformidade Avançada ou uma assinatura do E5 para sua organização. Se você não tiver esse plano e quiser tentar a Descoberta Eletrônica Avançada, poderá [Inscrever-se para uma avaliação do Office 365 Enterprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span><span class="sxs-lookup"><span data-stu-id="ec350-p101">Advanced eDiscovery requires an Office 365 E3 with the Advanced Compliance add-on or an E5 subscription for your organization. If you don't have that plan and want to try Advanced eDiscovery, you can [sign up for a trial of Office 365 Enterprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span></span> 
  
<span data-ttu-id="ec350-106">Na descoberta eletrônica avançada, é possível adicionar palavras-chave definidas pelo usuário à relevância para ajudá-lo a identificar arquivos relevantes durante a marcação.</span><span class="sxs-lookup"><span data-stu-id="ec350-106">In Advanced eDiscovery, it's possible to add user-defined keywords to Relevance in order to help you identify relevant files while tagging.</span></span> <span data-ttu-id="ec350-107">As palavras-chave serão exibidas na marca cores especificadas em \*\*relevância \> \*\*.</span><span class="sxs-lookup"><span data-stu-id="ec350-107">Keywords will be displayed in the specified colors in **Relevance \> Tag**.</span></span> 
  
<span data-ttu-id="ec350-108">Conforme descrito abaixo, as listas de palavras-chave podem ser adicionadas e as cores atribuídas à lista de palavras-chave e aos problemas relacionados.</span><span class="sxs-lookup"><span data-stu-id="ec350-108">As described below, keyword lists can be added, and colors assigned to the Keywords list and the related issues.</span></span> <span data-ttu-id="ec350-109">Uma dica de ferramenta exibe a descrição da palavra-chave, se houver uma, conforme indicado por um sublinhado duplo.</span><span class="sxs-lookup"><span data-stu-id="ec350-109">A tooltip displays the keyword's description, if one exists, as indicated by a double underline.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="ec350-110">O realce de ocorrências em relevância e exibição de ocorrências de palavras-chave em documentos durante a marcação de relevância não funciona para os conjuntos de caracteres de byte duplo japonês, chinês e coreano.</span><span class="sxs-lookup"><span data-stu-id="ec350-110">Hit highlighting in Relevance and viewing keyword hit results within documents during Relevance tagging does not work for the Japanese, Chinese, and Korean double-byte character sets.</span></span> 
  
## <a name="adding-highlighted-keywords"></a><span data-ttu-id="ec350-111">Adicionando palavras-chave realçadas</span><span class="sxs-lookup"><span data-stu-id="ec350-111">Adding highlighted keywords</span></span>

1. <span data-ttu-id="ec350-112">Na guia **configuração \> de relevância de relevância** , selecione **palavras-chave**realçadas.</span><span class="sxs-lookup"><span data-stu-id="ec350-112">In the **Relevance \> Relevance setup** tab, select **Highlighted keywords**.</span></span>
    
2. <span data-ttu-id="ec350-113">Clique no **+** ícone para adicionar palavras-chave.</span><span class="sxs-lookup"><span data-stu-id="ec350-113">Click the **+** icon to add keywords.</span></span> <span data-ttu-id="ec350-114">A caixa de diálogo **adicionar novas palavras-chave** é exibida.</span><span class="sxs-lookup"><span data-stu-id="ec350-114">The **Add new keywords** dialog is displayed.</span></span> 
    
3. <span data-ttu-id="ec350-115">Em **palavras-chave**, digite a lista palavras-chave, separando palavras-chave com vírgulas.</span><span class="sxs-lookup"><span data-stu-id="ec350-115">In **Keywords**, type the keywords list, separating keywords with commas.</span></span> 
    
4. <span data-ttu-id="ec350-116">Na lista **cor** , selecione a cor para realçar a lista de palavras-chave inserida.</span><span class="sxs-lookup"><span data-stu-id="ec350-116">In the **Color** list, select the color to highlight the entered keywords list.</span></span> 
    
5. <span data-ttu-id="ec350-117">Na lista **selecionar problema** , selecione se deseja aplicar a lista de palavras-chave a "todos os problemas" ou a problemas selecionados.</span><span class="sxs-lookup"><span data-stu-id="ec350-117">In the **Select issue** list, select whether to apply the keywords list to "All issues" or to selected issues.</span></span> 
    
6. <span data-ttu-id="ec350-118">Em **Descrição**, digite a lista de palavras-chave (opcional).</span><span class="sxs-lookup"><span data-stu-id="ec350-118">In **Description**, type the keywords list (optional).</span></span>
    
    ![Adicionar novas palavras-chave](media/1683a71f-0875-48fc-b4ef-01f3b0e8e8e9.png)
  
7. <span data-ttu-id="ec350-120">Clique em **OK** quando terminar.</span><span class="sxs-lookup"><span data-stu-id="ec350-120">Click **OK** when done.</span></span> <span data-ttu-id="ec350-121">A lista criada é adicionada à tabela lista de palavras-chave e pode ser editada ou excluída.</span><span class="sxs-lookup"><span data-stu-id="ec350-121">The created list is added to the keywords list table and can be edited or deleted.</span></span> 
    
    ![Lista de palavras-chave de configuração de relevância](media/a05d5ec0-8bde-470d-97e2-456b169281d6.png)
  
<span data-ttu-id="ec350-123">As palavras-chave definidas pelo usuário serão exibidas, na marca cores especificadas em relevância \> .</span><span class="sxs-lookup"><span data-stu-id="ec350-123">The user-defined keywords will be displayed, in the specified colors in Relevance \> Tag.</span></span> 
  
## <a name="specifying-relevance-setup-advanced-settings"></a><span data-ttu-id="ec350-124">Especificar configurações avançadas da configuração de relevância</span><span class="sxs-lookup"><span data-stu-id="ec350-124">Specifying Relevance setup advanced settings</span></span>

<span data-ttu-id="ec350-125">Essas configurações afetam a faixa e decidem os gráficos de relevância.</span><span class="sxs-lookup"><span data-stu-id="ec350-125">These settings affect the Track and Decide graphs in Relevance.</span></span>
  
1. <span data-ttu-id="ec350-126">Na guia **configuração \> de relevância de relevância** , selecione **Configurações avançadas**.</span><span class="sxs-lookup"><span data-stu-id="ec350-126">In the **Relevance \> Relevance setup** tab, select **Advanced settings**.</span></span>
    
2. <span data-ttu-id="ec350-127">Na caixa de diálogo **parâmetros de custo** , faça as seguintes seleções:</span><span class="sxs-lookup"><span data-stu-id="ec350-127">In the **Cost parameters** dialog, make the following selections:</span></span> 
    
1. <span data-ttu-id="ec350-128">Na lista **análise de custo por hora ($)** , selecione o valor em dólares ou aceite o padrão.</span><span class="sxs-lookup"><span data-stu-id="ec350-128">In the **Cost review per hour ($)** list, select the amount in dollars or accept the default.</span></span> 
    
2. <span data-ttu-id="ec350-129">Na lista **número de arquivos revisados por hora** , selecione o valor ou aceite o padrão.</span><span class="sxs-lookup"><span data-stu-id="ec350-129">In the **Number of files reviewed by hour** list, select the amount or accept the default.</span></span> 
    
    ![Parâmetros de custo de instalação de relevância](media/bab7b5b7-6297-4e7c-b0a6-ba5aa8b21787.png)
  
3. <span data-ttu-id="ec350-131">Clique em **Salvar**.</span><span class="sxs-lookup"><span data-stu-id="ec350-131">Click **Save**.</span></span> <span data-ttu-id="ec350-132">As configurações selecionadas são salvas.</span><span class="sxs-lookup"><span data-stu-id="ec350-132">The selected settings are saved.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="ec350-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="ec350-133">See also</span></span>

[<span data-ttu-id="ec350-134">Descoberta Eletrônica Avançada do Office 365</span><span class="sxs-lookup"><span data-stu-id="ec350-134">Office 365 Advanced eDiscovery</span></span>](office-365-advanced-ediscovery.md)
  
[<span data-ttu-id="ec350-135">Como definir problemas e atribuir usuários</span><span class="sxs-lookup"><span data-stu-id="ec350-135">Defining issues and assigning users</span></span>](define-issues-and-assign-users.md)
  
[<span data-ttu-id="ec350-136">Como configurar carregamentos para adicionar os arquivos importados</span><span class="sxs-lookup"><span data-stu-id="ec350-136">Setting up loads to add imported files</span></span>](set-up-loads-to-add-imported-files.md)

