---
title: Definir a opção Ignorar Texto para análise na Descoberta Eletrônica Avançada do Office 365
ms.author: chrfox
author: chrfox
manager: laurawi
ms.date: 9/14/2017
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: 44055727-56e8-42d7-9dc3-fb942f3901cc
description: 'Saiba como definir a regra para ignorar texto específico ao usar os módulos de análise e de processo na descoberta eletrônica avançada do Office 365.  '
ms.openlocfilehash: 3a4c1d17a9a56d3018509a8dcfd6b49abb951676
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30214241"
---
# <a name="set-ignore-text-option-for-analyze-in-office-365-advanced-ediscovery"></a><span data-ttu-id="4fa60-103">Definir a opção Ignorar Texto para análise na Descoberta Eletrônica Avançada do Office 365</span><span class="sxs-lookup"><span data-stu-id="4fa60-103">Set Ignore Text option for Analyze in Office 365 Advanced eDiscovery</span></span>

> [!NOTE]
> <span data-ttu-id="4fa60-p101">A Descoberta Eletrônica Avançada exige um Office 365 E3, com um complemento de Conformidade Avançada ou uma assinatura do E5 para sua organização. Se você não tiver esse plano e quiser tentar a Descoberta Eletrônica Avançada, poderá [Inscrever-se para uma avaliação do Office 365 Enterprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span><span class="sxs-lookup"><span data-stu-id="4fa60-p101">Advanced eDiscovery requires an Office 365 E3 with the Advanced Compliance add-on or an E5 subscription for your organization. If you don't have that plan and want to try Advanced eDiscovery, you can [sign up for a trial of Office 365 Enterprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span></span> 
  
<span data-ttu-id="4fa60-p102">O recurso Ignorar texto pode ser aplicado a todos os módulos de descoberta eletrônica avançados a seguir ou a qualquer um dos seguintes módulos de descoberta eletrônica avançada: analisar (próximos duplicatas, threads de email, temas) e relevância. O texto ignorado não aparecerá nos arquivos exibidos de relevância e a análise/cálculo descartará o texto ignorado.</span><span class="sxs-lookup"><span data-stu-id="4fa60-p102">The Ignore Text feature can be applied to all or any of the following Advanced eDiscovery modules: Analyze (Near-duplicates, Email Threads, Themes) and Relevance. Ignored text will not appear in files displayed in Relevance, and the analysis/calculations will discard the ignored text.</span></span>
  
<span data-ttu-id="4fa60-p103">Se o recurso Ignorar texto tiver sido definido anteriormente para módulos que já foram executados, a configuração de ignorar texto será agora protegida contra modificações. No enTanto, o recurso Ignorar texto para o módulo de relevância ainda pode ser alterado a qualquer momento.</span><span class="sxs-lookup"><span data-stu-id="4fa60-p103">If the Ignore Text feature was previously defined for modules that have already run, the Ignore Text setting will now be protected from being modified. However, the Ignore Text feature for the Relevance module can still be changed at any time.</span></span>
  
## <a name="how-ignore-text-filters-are-applied"></a><span data-ttu-id="4fa60-110">Como ignorar filtros de texto são aplicados</span><span class="sxs-lookup"><span data-stu-id="4fa60-110">How Ignore Text filters are applied</span></span>

<span data-ttu-id="4fa60-p104">Vários filtros de texto ignorar são aplicados na ordem em que foram inseridos. Para alterar a ordem na qual são aplicadas, elas devem ser excluídas e reinseridas na ordem desejada.</span><span class="sxs-lookup"><span data-stu-id="4fa60-p104">Multiple Ignore Text filters are applied in the order that they were entered. To change the order in which they are applied, they must be deleted and re-entered in the desired order.</span></span>
  
<span data-ttu-id="4fa60-113">Por exemplo, se o conteúdo de texto for: "DAVE BOB Ana Maria, véspera", veja a seguir exemplos de ignorar entradas de texto e resultados:</span><span class="sxs-lookup"><span data-stu-id="4fa60-113">For example, if the text content is: "DAVE BOB ALICE CAROL EVE", the following are samples of Ignore Text entries and the results:</span></span>
  
||||
|:-----|:-----|:-----|
|<span data-ttu-id="4fa60-114">**Ignorar entradas de texto**</span><span class="sxs-lookup"><span data-stu-id="4fa60-114">**Ignore Text entries**</span></span> <br/> |**==\>** <br/> |<span data-ttu-id="4fa60-115">**Resultados**</span><span class="sxs-lookup"><span data-stu-id="4fa60-115">**Results**</span></span> <br/> |
|<span data-ttu-id="4fa60-116">"ALICE", "BOB CAROL"</span><span class="sxs-lookup"><span data-stu-id="4fa60-116">"ALICE", "BOB CAROL"</span></span>  <br/> |==\>  <br/> |<span data-ttu-id="4fa60-117">"VÉSPERA DA DAVE"</span><span class="sxs-lookup"><span data-stu-id="4fa60-117">"DAVE EVE"</span></span>  <br/> |
|<span data-ttu-id="4fa60-118">"ANA", "BOB ALICE CAROL"</span><span class="sxs-lookup"><span data-stu-id="4fa60-118">"ALICE", "BOB ALICE CAROL"</span></span>  <br/> |==\>  <br/> |<span data-ttu-id="4fa60-119">"DAVE BOB CAROL (VÉSPERA)"</span><span class="sxs-lookup"><span data-stu-id="4fa60-119">"DAVE BOB CAROL EVE"</span></span>  <br/> |
   
<span data-ttu-id="4fa60-120">A segunda entrada de texto ignorar não é implementada porque a cadeia de caracteres não é encontrada como tal após a aplicação do primeiro texto para ignorar.</span><span class="sxs-lookup"><span data-stu-id="4fa60-120">The second Ignore Text entry is not implemented because the string is not found as such AFTER the first Ignore Text has been applied.</span></span>
  
## <a name="use-regular-expressions-when-defining-ignore-text"></a><span data-ttu-id="4fa60-121">Usar expressões regulares ao definir o texto de ignorar</span><span class="sxs-lookup"><span data-stu-id="4fa60-121">Use regular expressions when defining Ignore Text</span></span>

<span data-ttu-id="4fa60-p105">As expressões regulares têm suporte para uso ao definir o texto de ignorar. A seguir estão exemplos de sintaxe e uso de expressões regulares:</span><span class="sxs-lookup"><span data-stu-id="4fa60-p105">Regular expressions are supported for use when defining Ignore Text. The following are examples of regular expression syntax and usage:</span></span>
  
- <span data-ttu-id="4fa60-124">Para remover (ignorar) o texto de início até o final de uma linha:</span><span class="sxs-lookup"><span data-stu-id="4fa60-124">To remove (ignore) text from Begin until the end of a line:</span></span>
    
     `Begin(.*)$`
    
    <span data-ttu-id="4fa60-125">onde "Begin" é a ocorrência inicial dessa cadeia de caracteres na linha.</span><span class="sxs-lookup"><span data-stu-id="4fa60-125">where "Begin" is the initial occurrence of this string in the line.</span></span>
    
    <span data-ttu-id="4fa60-126">Por exemplo, para o seguinte texto:</span><span class="sxs-lookup"><span data-stu-id="4fa60-126">For example, for the following text:</span></span>
    
    <span data-ttu-id="4fa60-127">**"Esta é a primeira frase e primeira linha**</span><span class="sxs-lookup"><span data-stu-id="4fa60-127">**"This is first sentence and first line**</span></span>
    
    <span data-ttu-id="4fa60-128">**Esta é segunda frase e segunda linha "**</span><span class="sxs-lookup"><span data-stu-id="4fa60-128">**This is second sentence and second line"**</span></span>
    
    <span data-ttu-id="4fa60-129">a expressão regular primeiro (.\*) $ resultará em:</span><span class="sxs-lookup"><span data-stu-id="4fa60-129">the Regular Expression first(.\*)$ will result in:</span></span>
    
    <span data-ttu-id="4fa60-130">**"Isso é**</span><span class="sxs-lookup"><span data-stu-id="4fa60-130">**"This is**</span></span>
    
    <span data-ttu-id="4fa60-131">**Esta é segunda frase e segunda linha "**</span><span class="sxs-lookup"><span data-stu-id="4fa60-131">**This is second sentence and second line"**</span></span>
    
- <span data-ttu-id="4fa60-132">Para remover avisos de isenção de responsabilidade e instruções legais automaticamente inseridos no final dos threads de email:</span><span class="sxs-lookup"><span data-stu-id="4fa60-132">To remove disclaimers and legal statements automatically inserted at the end of email threads:</span></span>
    
     `Begin(.|\s)*End`
    
    <span data-ttu-id="4fa60-133">onde "Begin" e "End" são cadeias de caracteres exclusivas no início e no final de um parágrafo com quebra de texto.</span><span class="sxs-lookup"><span data-stu-id="4fa60-133">where "Begin" and "End" are unique strings at the beginning and end of a wrapped text paragraph.</span></span> 
    
    <span data-ttu-id="4fa60-134">Por exemplo, a expressão regular a seguir removerá avisos de isenção de responsabilidade e declarações legais que estavam no thread de email entre as cadeias de caracteres de início e término:</span><span class="sxs-lookup"><span data-stu-id="4fa60-134">For example, the following regular expression will remove disclaimers and legal statements that were in the email thread between the Begin and End strings:</span></span>
    
    <span data-ttu-id="4fa60-135">**Esta mensagem contém informações confidenciais (. | \s)\*se a verificação for necessária, solicite uma versão de cópia de disco**</span><span class="sxs-lookup"><span data-stu-id="4fa60-135">**This message contains confidential information (.|\s)\*If verification is required please request a hard-copy version**</span></span>
    
- <span data-ttu-id="4fa60-136">Para remover um aviso de isenção de responsabilidade (incluindo caracteres especiais):</span><span class="sxs-lookup"><span data-stu-id="4fa60-136">To remove a disclaimer (including special characters):</span></span> 
    
    <span data-ttu-id="4fa60-137">Por exemplo, para o texto a seguir (com o aviso de isenção de responsabilidade representado aqui por x):</span><span class="sxs-lookup"><span data-stu-id="4fa60-137">For example, for the following text (with the disclaimer represented here by x's):</span></span> 
    
    <span data-ttu-id="4fa60-138">**/\*\ Esta mensagem contém informações confidenciais. XXXX XXXX**</span><span class="sxs-lookup"><span data-stu-id="4fa60-138">**/\*\ This message contains confidential information. xxxx xxxx**</span></span>
    
    <span data-ttu-id="4fa60-139">**XXXX XXXX XXXX XXXX XXXX XXXX XXXX**</span><span class="sxs-lookup"><span data-stu-id="4fa60-139">**xxxx xxxx xxxx xxxx xxxx xxxx xxxx**</span></span>
    
    <span data-ttu-id="4fa60-140">\**XXXX XXXX se a verificação for necessária, solicite uma versão de cópia impressa. /\*\**</span><span class="sxs-lookup"><span data-stu-id="4fa60-140">\**xxxx xxxx If verification is required, please request a hard-copy version. /\*\**</span></span>
    
    <span data-ttu-id="4fa60-141">a expressão regular para remover o aviso de isenção de responsabilidade acima deve ser:</span><span class="sxs-lookup"><span data-stu-id="4fa60-141">the regular expression to remove the above disclaimer should be:</span></span> 
    
    <span data-ttu-id="4fa60-142">**\/\\*\\Esta mensagem contém informações\.confidenciais (. | \s)\* se a verificação for necessária, solicite uma versão\. de cópia de disco\/\\*\\**</span><span class="sxs-lookup"><span data-stu-id="4fa60-142">**\/\\*\\ This message contains confidential information\.(.|\s)\* If verification is required please request a hard-copy version\. \/\\*\\**</span></span>
    
- <span data-ttu-id="4fa60-143">Regras de expressão regular:</span><span class="sxs-lookup"><span data-stu-id="4fa60-143">Regular expression rules:</span></span>
    
  - <span data-ttu-id="4fa60-144">Todos os caracteres que não fazem parte do alfabeto, exceto os espaços (s), "_" e "-" devem ser precedidos\"por ".</span><span class="sxs-lookup"><span data-stu-id="4fa60-144">Any characters that are not part of the alphabet except for space(s), "_" and "-" must be preceded by "\".</span></span>
    
  - <span data-ttu-id="4fa60-145">O campo normal eExpression pode ter comprimento ilimitado.</span><span class="sxs-lookup"><span data-stu-id="4fa60-145">The regular eExpression field can be unlimited length.</span></span>
    
> [!TIP]
> <span data-ttu-id="4fa60-146">Para obter uma explicação e sintaxe detalhada de expressões regulares, consulte: [linguagem de expressão regular-referência rápida](https://msdn.microsoft.com/en-us/library/az24scfc%28v=vs.110%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="4fa60-146">For an explanation and detailed syntax of regular expressions, see: [Regular Expression Language - Quick Reference](https://msdn.microsoft.com/en-us/library/az24scfc%28v=vs.110%29.aspx).</span></span> 
  
## <a name="define-ignore-text-rule"></a><span data-ttu-id="4fa60-147">Definir a regra de ignorar texto</span><span class="sxs-lookup"><span data-stu-id="4fa60-147">Define Ignore Text rule</span></span>

1. <span data-ttu-id="4fa60-148">Na guia **Gerenciar \> \> opções** de análise, na seção **Ignorar texto** , clique no **+** ícone para adicionar uma regra.</span><span class="sxs-lookup"><span data-stu-id="4fa60-148">In the **Manage \> Analyze \> Analyze options** tab, in the **Ignore Text** section, click the **+** icon to add a rule.</span></span> 
    
2. <span data-ttu-id="4fa60-149">Na caixa de diálogo **Adicionar ignorar texto** , no campo **nome** , digite um nome para a regra de ignorar texto.</span><span class="sxs-lookup"><span data-stu-id="4fa60-149">In the **Add Ignore Text** dialog, in the **Name** field, type a name for the Ignore Text rule.</span></span> 
    
    ![Adicionar texto ignorado](media/98e5129b-2667-4692-86fa-2d0117187a7f.png)
  
3. <span data-ttu-id="4fa60-p106">Na caixa de **texto** , digite o texto a ser ignorado. O campo de texto permite um número ilimitado de caracteres.</span><span class="sxs-lookup"><span data-stu-id="4fa60-p106">In the **Text** box, type the text to be ignored. The text field allows an unlimited number of characters.</span></span> 
    
    > [!TIP]
    > <span data-ttu-id="4fa60-153">Conforme mostrado na janela acima, clique em **lâmpada** para ver as diretrizes de sintaxe comuns da regra de ignorar texto.</span><span class="sxs-lookup"><span data-stu-id="4fa60-153">As shown in the window above, click **light bulb** to see common syntax guidelines for the Ignore Text rule.</span></span> 
  
4. <span data-ttu-id="4fa60-154">Marque a \*\*\*\* caixa de seleção diferencia maiúsculas de minúsculas, se desejado.</span><span class="sxs-lookup"><span data-stu-id="4fa60-154">Select the **Case sensitive** check box, if desired.</span></span> 
    
5. <span data-ttu-id="4fa60-155">Na lista **aplicar a** , selecione os módulos de descoberta eletrônica avançados nos quais a definição será aplicada.</span><span class="sxs-lookup"><span data-stu-id="4fa60-155">In the **Apply to** list, select the Advanced eDiscovery modules in which to apply the definition.</span></span> 
    
6. <span data-ttu-id="4fa60-p107">Se você quiser uma execução de teste em texto de exemplo, digite texto de exemplo na caixa de texto de **entrada** e clique em **testar**. Os resultados são exibidos na caixa de texto de **saída** .</span><span class="sxs-lookup"><span data-stu-id="4fa60-p107">If you want a test run on sample text, type sample text in the **Input** text box and click **Test**. The results are displayed in the **Output** text box.</span></span> 
    
7. <span data-ttu-id="4fa60-p108">Clique em **OK** para salvar a regra de ignorar texto. A regra de ignorar texto definida é exibida.</span><span class="sxs-lookup"><span data-stu-id="4fa60-p108">Click **OK** to save the Ignore Text rule. The defined Ignore Text rule is displayed.</span></span> 
    
    ![Definir nome de texto ignorado](media/3a788ac3-4a1c-46c9-89bd-7ff32d68ce23.png)
  
## <a name="see-also"></a><span data-ttu-id="4fa60-161">Confira também</span><span class="sxs-lookup"><span data-stu-id="4fa60-161">See also</span></span>

[<span data-ttu-id="4fa60-162">Descoberta Eletrônica Avançada do Office 365</span><span class="sxs-lookup"><span data-stu-id="4fa60-162">Office 365 Advanced eDiscovery</span></span>](office-365-advanced-ediscovery.md)
  
[<span data-ttu-id="4fa60-163">Noções básicas sobre a similaridade de documentos</span><span class="sxs-lookup"><span data-stu-id="4fa60-163">Understanding document similarity</span></span>](understand-document-similarity-in-advanced-ediscovery.md)
  
[<span data-ttu-id="4fa60-164">Configuração das opções de análise</span><span class="sxs-lookup"><span data-stu-id="4fa60-164">Setting Analyze options</span></span>](set-analyze-options-in-advanced-ediscovery.md)
  
[<span data-ttu-id="4fa60-165">Configuração analisar configurações avançadas</span><span class="sxs-lookup"><span data-stu-id="4fa60-165">Setting Analyze advanced settings</span></span>](set-analyze-advanced-settings-in-advanced-ediscovery.md)
  
[<span data-ttu-id="4fa60-166">Exibindo resultados de análise</span><span class="sxs-lookup"><span data-stu-id="4fa60-166">Viewing Analyze results</span></span>](view-analyze-results-in-advanced-ediscovery.md)

