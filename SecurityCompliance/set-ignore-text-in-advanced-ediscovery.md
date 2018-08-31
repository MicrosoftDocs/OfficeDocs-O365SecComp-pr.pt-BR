---
title: Definir a opção Ignorar Texto para análise na Descoberta Eletrônica Avançada do Office 365
ms.author: chrfox
author: chrfox
manager: laurawi
ms.date: 9/14/2017
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: 44055727-56e8-42d7-9dc3-fb942f3901cc
description: 'Aprenda a definir a regra para ignorar o texto específico ao usar os módulos de analisar e processar no eDiscovery avançadas do Office 365.  '
ms.openlocfilehash: eb7e7052979087b7dba98aac3b0c9ab75ec0d02a
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22524098"
---
# <a name="set-ignore-text-option-for-analyze-in-office-365-advanced-ediscovery"></a><span data-ttu-id="1946e-103">Definir a opção Ignorar Texto para análise na Descoberta Eletrônica Avançada do Office 365</span><span class="sxs-lookup"><span data-stu-id="1946e-103">Set Ignore Text option for Analyze in Office 365 Advanced eDiscovery</span></span>

> [!NOTE]
> <span data-ttu-id="1946e-p101">EDiscovery Avançado requer um Office 365 E3 com o complemento de conformidade avançadas ou uma assinatura E5 para sua organização. Se você não tiver que plano e quiser tentar eDiscovery avançado, você pode [inscrever-se para uma avaliação do Office 365 Enterprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span><span class="sxs-lookup"><span data-stu-id="1946e-p101">Advanced eDiscovery requires an Office 365 E3 with the Advanced Compliance add-on or an E5 subscription for your organization. If you don't have that plan and want to try Advanced eDiscovery, you can [sign up for a trial of Office 365 Enterprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span></span> 
  
<span data-ttu-id="1946e-p102">O recurso Ignorar texto pode ser aplicado a todos ou qualquer um dos seguintes módulos avançados eDiscovery: analisar (temas de Threads de Email, perto de duplicatas) e a relevância. Texto ignorado não aparecerá na arquivos exibidos em relevância e os cálculos de análise/descartará o texto ignorado.</span><span class="sxs-lookup"><span data-stu-id="1946e-p102">The Ignore Text feature can be applied to all or any of the following Advanced eDiscovery modules: Analyze (Near-duplicates, Email Threads, Themes) and Relevance. Ignored text will not appear in files displayed in Relevance, and the analysis/calculations will discard the ignored text.</span></span>
  
<span data-ttu-id="1946e-p103">Se o recurso Ignorar texto foi definido anteriormente para módulos que já foi executado, a configuração Ignorar texto agora estará protegida contra modificação. No entanto, o recurso de ignorar o texto para o módulo de relevância ainda pode ser alterado a qualquer momento.</span><span class="sxs-lookup"><span data-stu-id="1946e-p103">If the Ignore Text feature was previously defined for modules that have already run, the Ignore Text setting will now be protected from being modified. However, the Ignore Text feature for the Relevance module can still be changed at any time.</span></span>
  
## <a name="how-ignore-text-filters-are-applied"></a><span data-ttu-id="1946e-110">Como Ignorar texto filtros são aplicados</span><span class="sxs-lookup"><span data-stu-id="1946e-110">How Ignore Text filters are applied</span></span>

<span data-ttu-id="1946e-p104">Vários filtros Ignorar texto são aplicados na ordem em que foram inseridos. Para alterar a ordem na qual elas serão aplicadas, eles devem ser excluídos e entrado novamente na ordem desejada.</span><span class="sxs-lookup"><span data-stu-id="1946e-p104">Multiple Ignore Text filters are applied in the order that they were entered. To change the order in which they are applied, they must be deleted and re-entered in the desired order.</span></span>
  
<span data-ttu-id="1946e-113">Por exemplo, se o conteúdo de texto é: "DAVE BOB ALICE CAROL noite", a seguir estão exemplos de entradas de ignorar o texto e os resultados:</span><span class="sxs-lookup"><span data-stu-id="1946e-113">For example, if the text content is: "DAVE BOB ALICE CAROL EVE", the following are samples of Ignore Text entries and the results:</span></span>
  
||||
|:-----|:-----|:-----|
|<span data-ttu-id="1946e-114">**Ignorar as entradas de texto**</span><span class="sxs-lookup"><span data-stu-id="1946e-114">**Ignore Text entries**</span></span> <br/> |**==\>** <br/> |<span data-ttu-id="1946e-115">**Resultados**</span><span class="sxs-lookup"><span data-stu-id="1946e-115">**Results**</span></span> <br/> |
|<span data-ttu-id="1946e-116">"ALICE", "BOB CAROL"</span><span class="sxs-lookup"><span data-stu-id="1946e-116">"ALICE", "BOB CAROL"</span></span>  <br/> |==\>  <br/> |<span data-ttu-id="1946e-117">"DAVE NOITE"</span><span class="sxs-lookup"><span data-stu-id="1946e-117">"DAVE EVE"</span></span>  <br/> |
|<span data-ttu-id="1946e-118">"ALICE", "BOB ALICE CAROL"</span><span class="sxs-lookup"><span data-stu-id="1946e-118">"ALICE", "BOB ALICE CAROL"</span></span>  <br/> |==\>  <br/> |<span data-ttu-id="1946e-119">"DAVE BOB CAROL NOITE"</span><span class="sxs-lookup"><span data-stu-id="1946e-119">"DAVE BOB CAROL EVE"</span></span>  <br/> |
   
<span data-ttu-id="1946e-120">A segunda entrada de texto ignorar não está implementada porque a cadeia de caracteres não for encontrada como tal, após o primeiro texto ignorar tiver sido aplicado.</span><span class="sxs-lookup"><span data-stu-id="1946e-120">The second Ignore Text entry is not implemented because the string is not found as such AFTER the first Ignore Text has been applied.</span></span>
  
## <a name="use-regular-expressions-when-defining-ignore-text"></a><span data-ttu-id="1946e-121">Usar expressões regulares ao definir Ignorar texto</span><span class="sxs-lookup"><span data-stu-id="1946e-121">Use regular expressions when defining Ignore Text</span></span>

<span data-ttu-id="1946e-p105">Expressões regulares são compatíveis para uso ao definir Ignorar texto. A seguir está exemplos de uso e a sintaxe de expressão regular:</span><span class="sxs-lookup"><span data-stu-id="1946e-p105">Regular expressions are supported for use when defining Ignore Text. The following are examples of regular expression syntax and usage:</span></span>
  
- <span data-ttu-id="1946e-124">Para remover (ignorar) o texto de Begin até o final de uma linha:</span><span class="sxs-lookup"><span data-stu-id="1946e-124">To remove (ignore) text from Begin until the end of a line:</span></span>
    
     `Begin(.*)$`
    
    <span data-ttu-id="1946e-125">onde "Begin" é a ocorrência inicial dessa cadeia de caracteres na linha.</span><span class="sxs-lookup"><span data-stu-id="1946e-125">where "Begin" is the initial occurrence of this string in the line.</span></span>
    
    <span data-ttu-id="1946e-126">Por exemplo, para o seguinte texto:</span><span class="sxs-lookup"><span data-stu-id="1946e-126">For example, for the following text:</span></span>
    
    <span data-ttu-id="1946e-127">**"Este é primeira frase e a primeira linha**</span><span class="sxs-lookup"><span data-stu-id="1946e-127">**"This is first sentence and first line**</span></span>
    
    <span data-ttu-id="1946e-128">**Esta é a segunda frase e a segunda linha"**</span><span class="sxs-lookup"><span data-stu-id="1946e-128">**This is second sentence and second line"**</span></span>
    
    <span data-ttu-id="1946e-129">a expressão Regular first(.\*) $ resultará em:</span><span class="sxs-lookup"><span data-stu-id="1946e-129">the Regular Expression first(.\*)$ will result in:</span></span>
    
    <span data-ttu-id="1946e-130">**"Este é**</span><span class="sxs-lookup"><span data-stu-id="1946e-130">**"This is**</span></span>
    
    <span data-ttu-id="1946e-131">**Esta é a segunda frase e a segunda linha"**</span><span class="sxs-lookup"><span data-stu-id="1946e-131">**This is second sentence and second line"**</span></span>
    
- <span data-ttu-id="1946e-132">Para remover os avisos de isenção e declarações jurídicas automaticamente inseridas no fim de threads de email:</span><span class="sxs-lookup"><span data-stu-id="1946e-132">To remove disclaimers and legal statements automatically inserted at the end of email threads:</span></span>
    
     `Begin(.|\s)*End`
    
    <span data-ttu-id="1946e-133">onde "Begin" e "End" são cadeias de caracteres exclusivas no início e no final de um parágrafo do texto quebrado automaticamente.</span><span class="sxs-lookup"><span data-stu-id="1946e-133">where "Begin" and "End" are unique strings at the beginning and end of a wrapped text paragraph.</span></span> 
    
    <span data-ttu-id="1946e-134">Por exemplo, a seguinte expressão regular e serão removidos avisos de isenção legais instruções que estavam no segmento de email entre as cadeias de caracteres Begin e End:</span><span class="sxs-lookup"><span data-stu-id="1946e-134">For example, the following regular expression will remove disclaimers and legal statements that were in the email thread between the Begin and End strings:</span></span>
    
    <span data-ttu-id="1946e-135">**Esta mensagem contém informações confidenciais (. | \s)\*se é necessária uma verificação solicite uma versão impresso**</span><span class="sxs-lookup"><span data-stu-id="1946e-135">**This message contains confidential information (.|\s)\*If verification is required please request a hard-copy version**</span></span>
    
- <span data-ttu-id="1946e-136">Para remover um aviso de isenção (incluindo caracteres especiais):</span><span class="sxs-lookup"><span data-stu-id="1946e-136">To remove a disclaimer (including special characters):</span></span> 
    
    <span data-ttu-id="1946e-137">Por exemplo, para o seguinte texto (com a isenção de responsabilidade representado aqui por xx):</span><span class="sxs-lookup"><span data-stu-id="1946e-137">For example, for the following text (with the disclaimer represented here by x's):</span></span> 
    
    <span data-ttu-id="1946e-138">**/\*\ Esta mensagem contém informações confidenciais. xxxx xxxx**</span><span class="sxs-lookup"><span data-stu-id="1946e-138">**/\*\ This message contains confidential information. xxxx xxxx**</span></span>
    
    <span data-ttu-id="1946e-139">**xxxx xxxx xxxx xxxx xxxx xxxx xxxx**</span><span class="sxs-lookup"><span data-stu-id="1946e-139">**xxxx xxxx xxxx xxxx xxxx xxxx xxxx**</span></span>
    
    <span data-ttu-id="1946e-140">\**xxxx xxxx se verificação for necessária, solicite uma versão impresso. /\*\**</span><span class="sxs-lookup"><span data-stu-id="1946e-140">\**xxxx xxxx If verification is required, please request a hard-copy version. /\*\**</span></span>
    
    <span data-ttu-id="1946e-141">a expressão regular para remover a isenção de responsabilidade acima deve ser:</span><span class="sxs-lookup"><span data-stu-id="1946e-141">the regular expression to remove the above disclaimer should be:</span></span> 
    
    <span data-ttu-id="1946e-142">**\/\\*\\Esta mensagem contém informações confidenciais\.(. | \s)\* se é necessária uma verificação solicite uma versão impresso\.\/\\*\\**</span><span class="sxs-lookup"><span data-stu-id="1946e-142">**\/\\*\\ This message contains confidential information\.(.|\s)\* If verification is required please request a hard-copy version\. \/\\*\\**</span></span>
    
- <span data-ttu-id="1946e-143">Regras de expressão regular:</span><span class="sxs-lookup"><span data-stu-id="1946e-143">Regular expression rules:</span></span>
    
  - <span data-ttu-id="1946e-144">Quaisquer caracteres que não fazem parte do alfabeto, com exceção de espaço (s), "_" e "-" deve ser precedido por "\".</span><span class="sxs-lookup"><span data-stu-id="1946e-144">Any characters that are not part of the alphabet except for space(s), "_" and "-" must be preceded by "\".</span></span>
    
  - <span data-ttu-id="1946e-145">O campo eExpression regular pode ser comprimento ilimitado.</span><span class="sxs-lookup"><span data-stu-id="1946e-145">The regular eExpression field can be unlimited length.</span></span>
    
> [!TIP]
> <span data-ttu-id="1946e-146">Para obter uma explicação e detalhadas sobre sintaxe das expressões regulares, consulte: [Linguagem de expressão Regular - referência rápida](https://msdn.microsoft.com/en-us/library/az24scfc%28v=vs.110%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="1946e-146">For an explanation and detailed syntax of regular expressions, see: [Regular Expression Language - Quick Reference](https://msdn.microsoft.com/en-us/library/az24scfc%28v=vs.110%29.aspx).</span></span> 
  
## <a name="define-ignore-text-rule"></a><span data-ttu-id="1946e-147">Definir texto Ignorar regra</span><span class="sxs-lookup"><span data-stu-id="1946e-147">Define Ignore Text rule</span></span>

1. <span data-ttu-id="1946e-148">No **Gerenciar \> analisar \> analisar opções** guia, na seção **Ignorar texto** , clique no **+** ícone para adicionar uma regra.</span><span class="sxs-lookup"><span data-stu-id="1946e-148">In the **Manage \> Analyze \> Analyze options** tab, in the **Ignore Text** section, click the **+** icon to add a rule.</span></span> 
    
2. <span data-ttu-id="1946e-149">Na caixa de diálogo **Adicionar texto ignorar** , no campo **nome** , digite um nome para a regra Ignorar texto.</span><span class="sxs-lookup"><span data-stu-id="1946e-149">In the **Add Ignore Text** dialog, in the **Name** field, type a name for the Ignore Text rule.</span></span> 
    
    ![Adicionar texto ignorado](media/98e5129b-2667-4692-86fa-2d0117187a7f.png)
  
3. <span data-ttu-id="1946e-p106">Na caixa de **texto** , digite o texto a ser ignorado. O campo texto permite que um número ilimitado de caracteres.</span><span class="sxs-lookup"><span data-stu-id="1946e-p106">In the **Text** box, type the text to be ignored. The text field allows an unlimited number of characters.</span></span> 
    
    > [!TIP]
    > <span data-ttu-id="1946e-153">Conforme mostrado na janela acima, clique em **lâmpada** para ver as diretrizes de sintaxe comuns para a regra Ignorar texto.</span><span class="sxs-lookup"><span data-stu-id="1946e-153">As shown in the window above, click **light bulb** to see common syntax guidelines for the Ignore Text rule.</span></span> 
  
4. <span data-ttu-id="1946e-154">Marque a caixa de seleção **Diferenciar maiusculas de minúsculas** , se desejado.</span><span class="sxs-lookup"><span data-stu-id="1946e-154">Select the **Case sensitive** check box, if desired.</span></span> 
    
5. <span data-ttu-id="1946e-155">Na lista **Aplicar a** , selecione os módulos de descoberta eletrônica avançada na qual aplicar a definição.</span><span class="sxs-lookup"><span data-stu-id="1946e-155">In the **Apply to** list, select the Advanced eDiscovery modules in which to apply the definition.</span></span> 
    
6. <span data-ttu-id="1946e-p107">Se você quiser um execução de teste em texto de exemplo, digite o texto de exemplo na caixa de texto de **entrada** e clique em **Testar**. Os resultados são exibidos na caixa de texto de **saída** .</span><span class="sxs-lookup"><span data-stu-id="1946e-p107">If you want a test run on sample text, type sample text in the **Input** text box and click **Test**. The results are displayed in the **Output** text box.</span></span> 
    
7. <span data-ttu-id="1946e-p108">Clique em **Okey** para salvar a regra Ignorar texto. A regra de Ignorar texto definida é exibida.</span><span class="sxs-lookup"><span data-stu-id="1946e-p108">Click **OK** to save the Ignore Text rule. The defined Ignore Text rule is displayed.</span></span> 
    
    ![Definir nome de texto ignorado](media/3a788ac3-4a1c-46c9-89bd-7ff32d68ce23.png)
  
## <a name="see-also"></a><span data-ttu-id="1946e-161">Confira também</span><span class="sxs-lookup"><span data-stu-id="1946e-161">See also</span></span>

[<span data-ttu-id="1946e-162">Descoberta Eletrônica Avançada do Office 365</span><span class="sxs-lookup"><span data-stu-id="1946e-162">Office 365 Advanced eDiscovery</span></span>](office-365-advanced-ediscovery.md)
  
[<span data-ttu-id="1946e-163">Noções básicas sobre semelhança de documento</span><span class="sxs-lookup"><span data-stu-id="1946e-163">Understanding document similarity</span></span>](understand-document-similarity-in-advanced-ediscovery.md)
  
[<span data-ttu-id="1946e-164">Definindo opções de analisar</span><span class="sxs-lookup"><span data-stu-id="1946e-164">Setting Analyze options</span></span>](set-analyze-options-in-advanced-ediscovery.md)
  
[<span data-ttu-id="1946e-165">Analisar configuração configurações avançada</span><span class="sxs-lookup"><span data-stu-id="1946e-165">Setting Analyze advanced settings</span></span>](set-analyze-advanced-settings-in-advanced-ediscovery.md)
  
[<span data-ttu-id="1946e-166">Exibindo os resultados da análise</span><span class="sxs-lookup"><span data-stu-id="1946e-166">Viewing Analyze results</span></span>](view-analyze-results-in-advanced-ediscovery.md)

