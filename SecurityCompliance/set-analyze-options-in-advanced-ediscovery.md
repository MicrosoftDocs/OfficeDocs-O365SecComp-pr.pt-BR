---
title: Definir opções de análise na Descoberta Eletrônica Avançada do Office 365
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
ms.assetid: f6cd6588-f6b6-424a-a9ab-3782b842faee
description: 'Revise as etapas para configurar as opções para o processo de analisar no eDiscovery avançadas do Office 365, incluindo perto duplicatas, threads de email e temas.  '
ms.openlocfilehash: a0ebbadb180321a3094cb1056ed8e0e6500ee66a
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22524046"
---
# <a name="set-analyze-options-in-office-365-advanced-ediscovery"></a><span data-ttu-id="c783d-103">Definir opções de análise na Descoberta Eletrônica Avançada do Office 365</span><span class="sxs-lookup"><span data-stu-id="c783d-103">Set Analyze options in Office 365 Advanced eDiscovery</span></span>

> [!NOTE]
> <span data-ttu-id="c783d-p101">EDiscovery Avançado requer um Office 365 E3 com o complemento de conformidade avançadas ou uma assinatura E5 para sua organização. Se você não tiver que plano e quiser tentar eDiscovery avançado, você pode [inscrever-se para uma avaliação do Office 365 Enterprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span><span class="sxs-lookup"><span data-stu-id="c783d-p101">Advanced eDiscovery requires an Office 365 E3 with the Advanced Compliance add-on or an E5 subscription for your organization. If you don't have that plan and want to try Advanced eDiscovery, you can [sign up for a trial of Office 365 Enterprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span></span> 
  
<span data-ttu-id="c783d-106">No eDiscovery avançado, defina as opções de analisar antes de executar Analyze.</span><span class="sxs-lookup"><span data-stu-id="c783d-106">In Advanced eDiscovery, set the Analyze options prior to running Analyze.</span></span>
  
## <a name="set-analyze-options"></a><span data-ttu-id="c783d-107">Definir opções de analisar</span><span class="sxs-lookup"><span data-stu-id="c783d-107">Set Analyze options</span></span>

<span data-ttu-id="c783d-p102">Open **Preparar \> analisar** \> **instalação**. A seguinte janela é exibida.</span><span class="sxs-lookup"><span data-stu-id="c783d-p102">Open **Prepare \> Analyze** \> **Setup**. The following window is displayed.</span></span>
  
![Definir Opções de Análise](media/c3ec7a92-8484-4812-b98c-aa3eb740e5b7.png)
  
 <span data-ttu-id="c783d-p103">**Perto duplicatas e segmentos de email** Esta caixa de seleção se você deseja executar a análise. Ele é selecionado por padrão.</span><span class="sxs-lookup"><span data-stu-id="c783d-p103">**Near-duplicates and email threads** Check this box if you want to run the analysis. It is selected by default.</span></span> 
  
 <span data-ttu-id="c783d-113">**Semelhança de documento** Insira o valor de limite de repetições de Near ou aceite o padrão de 65%.</span><span class="sxs-lookup"><span data-stu-id="c783d-113">**Document similarity**Enter the Near-duplicates threshold value or accept the default of 65%.</span></span> 
  
 <span data-ttu-id="c783d-p104">**Temas** Marque esta caixa para processar todos os arquivos e atribua temas de. Por padrão, essa caixa de seleção não está selecionada. Insira as seguintes opções se você deseja realizar o processamento de temas.</span><span class="sxs-lookup"><span data-stu-id="c783d-p104">**Themes**Check this box to process all files and assign themes to them. By default, this check box is not selected. Enter the following options if you want to perform Themes processing.</span></span>
  
- <span data-ttu-id="c783d-p105">**Número máximo de temas** Insira ou selecione um valor para o número de temas para criar. O padrão é 200.</span><span class="sxs-lookup"><span data-stu-id="c783d-p105">**Max number of themes**Enter or select a value for the number of themes to create. The default is 200.</span></span> 
    
    > [!NOTE]
    > <span data-ttu-id="c783d-p106">Aumento do número de temas afeta o desempenho, bem como a capacidade de um tema para generalizar. Quanto maior o número de temas, mais granular são. Por exemplo, se um conjunto de 50 temas incluir um tema, como "Basquete, rumo, Cortador de Lakers"; 300 temas podem incluir separados temas: "Estimula os", "Cortador de", "Lakers". Se você tivesse sem reconhecimento do tema "Basquete" e usa esse recurso para ECA, vendo o tema "Basquete" poderia ser útil. Mas, se o processamento teve muitos temas, você nunca pode ver a palavra "Basquete" e talvez não saiba que rumo e cortador é boa temas basquete revisar, em vez de itens que vá é inicializado e usado para cabelo.</span><span class="sxs-lookup"><span data-stu-id="c783d-p106">Increasing the number of themes affects performance, as well as the ability of a theme to generalize. The higher the number of themes, the more granular they are. For example, if a set of 50 themes include a theme such as "Basketball, Spurs, Clippers, Lakers"; 300 themes may include separate themes: "Spurs", "Clippers", "Lakers". If you had no awareness of the theme "Basketball" and use this feature for ECA, seeing the theme "Basketball" could be useful. But, if the processing had too many themes, you may never see the word "Basketball" and may not know that Spurs and Clippers are good Basketball themes to review, rather than items that go on boots and used for hair.</span></span> 
  
- <span data-ttu-id="c783d-p107">**Temas sugeridos** Você pode sugerir palavras de tema para controlar o processamento de temas. EDiscovery avançado será enfocam essas palavras sugeridas e tente criar um ou mais temas relevantes, com base nas configurações de "Número de temas do Max".</span><span class="sxs-lookup"><span data-stu-id="c783d-p107">**Suggested themes**You can suggest theme words to control Themes processing. Advanced eDiscovery will focus on these suggested words and try to create one or more relevant themes, based on the "Max number of themes" settings.</span></span> 
    
    <span data-ttu-id="c783d-p108">Por exemplo, se a palavra sugerida é "computer", e você especificou "2" como o "número máximo de temas", o eDiscovery avançado tentará gere dois temas que se relacionam com a palavra "computador". Os dois temas poderiam ser "software de computador" e "hardware de computador", por exemplo.</span><span class="sxs-lookup"><span data-stu-id="c783d-p108">For example, if the suggested word is "computer", and you specified "2" as the "Max number of Themes", Advanced eDiscovery will try to generate two themes that relate to the word "computer". The two themes might be "computer software" and "computer hardware", for example.</span></span> 
    
    ![Adicionar tema sugerido](media/06e9ffd3-a76c-423b-b450-9e465eb9a02f.png)
  
1. <span data-ttu-id="c783d-129">Para exibir, adicionar ou editar temas sugeridos, clique em **Modificar**.</span><span class="sxs-lookup"><span data-stu-id="c783d-129">To view, add, or edit suggested themes, click **Modify**.</span></span>
    
2. <span data-ttu-id="c783d-p109">No painel **sugeridos temas** , clique em **Adicionar**![Adicionar ícone](media/c2dd8b3a-5a22-412c-a7fa-143f5b2b5612.png) ícone para adicionar um tema. No painel do **tema sugerido de adicionar** , adicione as palavras, separadas por vírgulas.</span><span class="sxs-lookup"><span data-stu-id="c783d-p109">In the **Suggested themes** panel, click the **Add**![add icon](media/c2dd8b3a-5a22-412c-a7fa-143f5b2b5612.png) icon to add a theme. In the **Add suggested theme** panel, add the words, separated by commas.</span></span> 
    
3. <span data-ttu-id="c783d-132">Em **número de temas**, selecione um valor para determinar o número de temas eDiscovery avançado tentará gerar por estas palavras (o padrão é 1 tema).</span><span class="sxs-lookup"><span data-stu-id="c783d-132">In **Number of themes**, select a value to determine the number of themes Advanced eDiscovery will try to generate for these words (default is 1 theme).</span></span>
    
4. <span data-ttu-id="c783d-133">Clique em **Salvar** e feche a caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="c783d-133">Click **Save** and then close the dialogue.</span></span> 
    
    > [!NOTE]
    > <span data-ttu-id="c783d-p110">O número total de temas inclui sugerido temas. Os temas de sugerido total não pode exceder os temas total. Se houver vários temas sugerido em relação aos temas total, somente os temas "livro" poucos serão detectados pelo sistema porque a maioria dos temas vai ser dedicada ao temas sugerido.</span><span class="sxs-lookup"><span data-stu-id="c783d-p110">The total number of themes includes Suggested Themes. The total Suggested Themes cannot exceed the total themes. If there are many Suggested Themes relative to the total themes, only a few "novel" themes will be detected by the system because most of the themes will be dedicated to Suggested Themes.</span></span> 
  
- <span data-ttu-id="c783d-137">**Modo** Na lista suspensa, selecione uma opção de **temas** :</span><span class="sxs-lookup"><span data-stu-id="c783d-137">**Mode** From the drop-down list, select a **Themes** option:</span></span> 
    
  - <span data-ttu-id="c783d-138">**Criar e aplicar modelo**: calcula temas por modelos a partir de um segmento dos arquivos e distribui arquivos entre eles.</span><span class="sxs-lookup"><span data-stu-id="c783d-138">**Create and apply model**: Calculates themes by models from a segment of the files and then distributes files among them.</span></span>
    
  - <span data-ttu-id="c783d-p111">**Criar modelo**: calcula um modelo de temas de um segmento dos arquivos. O processo de aplicar de divisão de arquivos é feito separadamente mais tarde.</span><span class="sxs-lookup"><span data-stu-id="c783d-p111">**Create model**: Calculates a themes model from a segment of the files. The Apply process of dividing files is done separately at another time.</span></span>
    
  - <span data-ttu-id="c783d-p112">**Aplicar modelo**: essa opção é mostrada somente se um modelo foi criado anteriormente e ainda não foi aplicado. Isso dividirá os arquivos com base nos temas.</span><span class="sxs-lookup"><span data-stu-id="c783d-p112">**Apply model**: This option is only shown if a model was created previously and not yet applied. This will divide the files based on the themes.</span></span>
    
<span data-ttu-id="c783d-143">Você também pode [Definir Ignorar texto](set-ignore-text-in-advanced-ediscovery.md) e [definir configurações avançada de analisar](set-analyze-advanced-settings-in-advanced-ediscovery.md) para analisar.</span><span class="sxs-lookup"><span data-stu-id="c783d-143">You can also [set ignore text](set-ignore-text-in-advanced-ediscovery.md) and [set Analyze advanced settings](set-analyze-advanced-settings-in-advanced-ediscovery.md) for Analyze.</span></span> 
  
<span data-ttu-id="c783d-p113">Depois de configurar essas opções, clique em **Analisar** para ser executado. [Analisar o modo de exibição de resultados](view-analyze-results-in-advanced-ediscovery.md) são exibidos.</span><span class="sxs-lookup"><span data-stu-id="c783d-p113">After you've set these options, click **Analyze** to run. [View Analyze results](view-analyze-results-in-advanced-ediscovery.md) are displayed.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="c783d-146">Confira também</span><span class="sxs-lookup"><span data-stu-id="c783d-146">See also</span></span>

[<span data-ttu-id="c783d-147">Descoberta Eletrônica Avançada do Office 365</span><span class="sxs-lookup"><span data-stu-id="c783d-147">Office 365 Advanced eDiscovery</span></span>](office-365-advanced-ediscovery.md)
  
[<span data-ttu-id="c783d-148">Noções básicas sobre semelhança de documento</span><span class="sxs-lookup"><span data-stu-id="c783d-148">Understanding document similarity</span></span>](understand-document-similarity-in-advanced-ediscovery.md)
  
[<span data-ttu-id="c783d-149">Definir Ignorar texto</span><span class="sxs-lookup"><span data-stu-id="c783d-149">Set Ignore text </span></span>](set-ignore-text-in-advanced-ediscovery.md)
  
[<span data-ttu-id="c783d-150">Definir as configurações avançadas de análise</span><span class="sxs-lookup"><span data-stu-id="c783d-150">Set Analyze advanced settings</span></span>](set-analyze-advanced-settings-in-advanced-ediscovery.md)
  
[<span data-ttu-id="c783d-151">Exibir resultados de análise</span><span class="sxs-lookup"><span data-stu-id="c783d-151">View Analyze results</span></span>](view-analyze-results-in-advanced-ediscovery.md)

