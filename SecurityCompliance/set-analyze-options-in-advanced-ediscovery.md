---
title: Definir opções de análise na Descoberta Eletrônica Avançada do Office 365
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
ms.assetid: f6cd6588-f6b6-424a-a9ab-3782b842faee
description: 'Revise as etapas para configurar opções para o processo de análise na descoberta eletrônica avançada do Office 365, incluindo duplicatas, threads de email e temas.  '
ms.openlocfilehash: 12bbe4043803c165a58adac80b72d03afd48adc7
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30218221"
---
# <a name="set-analyze-options-in-office-365-advanced-ediscovery"></a><span data-ttu-id="6f805-103">Definir opções de análise na Descoberta Eletrônica Avançada do Office 365</span><span class="sxs-lookup"><span data-stu-id="6f805-103">Set Analyze options in Office 365 Advanced eDiscovery</span></span>

> [!NOTE]
> <span data-ttu-id="6f805-p101">A Descoberta Eletrônica Avançada exige um Office 365 E3, com um complemento de Conformidade Avançada ou uma assinatura do E5 para sua organização. Se você não tiver esse plano e quiser tentar a Descoberta Eletrônica Avançada, poderá [Inscrever-se para uma avaliação do Office 365 Enterprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span><span class="sxs-lookup"><span data-stu-id="6f805-p101">Advanced eDiscovery requires an Office 365 E3 with the Advanced Compliance add-on or an E5 subscription for your organization. If you don't have that plan and want to try Advanced eDiscovery, you can [sign up for a trial of Office 365 Enterprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span></span> 
  
<span data-ttu-id="6f805-106">Em descoberta eletrônica avançada, defina as opções de análise antes de executar Analyze.</span><span class="sxs-lookup"><span data-stu-id="6f805-106">In Advanced eDiscovery, set the Analyze options prior to running Analyze.</span></span>
  
## <a name="set-analyze-options"></a><span data-ttu-id="6f805-107">Definir opções de análise</span><span class="sxs-lookup"><span data-stu-id="6f805-107">Set Analyze options</span></span>

<span data-ttu-id="6f805-p102">Abra \> **a configuração**de \*\*análise de preparação \> \*\* . A janela a seguir é exibida.</span><span class="sxs-lookup"><span data-stu-id="6f805-p102">Open **Prepare \> Analyze** \> **Setup**. The following window is displayed.</span></span>
  
![Definir Opções de Análise](media/c3ec7a92-8484-4812-b98c-aa3eb740e5b7.png)
  
 <span data-ttu-id="6f805-p103">**Threads quase duplicados e email** Marque esta caixa se você deseja executar a análise. Ela é selecionada por padrão.</span><span class="sxs-lookup"><span data-stu-id="6f805-p103">**Near-duplicates and email threads** Check this box if you want to run the analysis. It is selected by default.</span></span> 
  
 <span data-ttu-id="6f805-113">**Similaridade de documentos** Insira o valor de limite Near-duplicates ou aceite o padrão de 65%.</span><span class="sxs-lookup"><span data-stu-id="6f805-113">**Document similarity**Enter the Near-duplicates threshold value or accept the default of 65%.</span></span> 
  
 <span data-ttu-id="6f805-p104">**Temas** Marque esta caixa para processar todos os arquivos e atribuir temas a eles. Por padrão, essa caixa de seleção não está selecionada. Insira as opções a seguir se você deseja executar o processamento de temas.</span><span class="sxs-lookup"><span data-stu-id="6f805-p104">**Themes**Check this box to process all files and assign themes to them. By default, this check box is not selected. Enter the following options if you want to perform Themes processing.</span></span>
  
- <span data-ttu-id="6f805-p105">**Número máximo de temas** Insira ou selecione um valor para o número de temas a serem criados. O padrão é 200.</span><span class="sxs-lookup"><span data-stu-id="6f805-p105">**Max number of themes**Enter or select a value for the number of themes to create. The default is 200.</span></span> 
    
    > [!NOTE]
    > <span data-ttu-id="6f805-p106">Aumentar o número de temas afeta o desempenho, bem como a capacidade de um tema generalizar. Quanto maior o número de temas, mais granulares eles são. Por exemplo, se um conjunto de 50 temas incluir um tema como "basquete, Spurs, clipes, Lakers"; 300 temas podem incluir temas separados: "Spurs", "Clippings", "Lakers". Se você não teve conhecimento do tema "basquete" e usar esse recurso para ECA, ver o tema "basquete" pode ser útil. Mas, se o processamento tiver muitos temas, talvez você nunca veja a palavra "basquete" e talvez não saiba que Spurs e reCortes são bons temas de basquete para revisar, em vez de itens que entram em inicializações e usados para cabelo.</span><span class="sxs-lookup"><span data-stu-id="6f805-p106">Increasing the number of themes affects performance, as well as the ability of a theme to generalize. The higher the number of themes, the more granular they are. For example, if a set of 50 themes include a theme such as "Basketball, Spurs, Clippers, Lakers"; 300 themes may include separate themes: "Spurs", "Clippers", "Lakers". If you had no awareness of the theme "Basketball" and use this feature for ECA, seeing the theme "Basketball" could be useful. But, if the processing had too many themes, you may never see the word "Basketball" and may not know that Spurs and Clippers are good Basketball themes to review, rather than items that go on boots and used for hair.</span></span> 
  
- <span data-ttu-id="6f805-p107">**Temas sugeridos** Você pode sugerir palavras de tema para controlar o processamento de temas. A descoberta eletrônica avançada se concentrará nessas palavras sugeridas e tentará criar um ou mais temas relevantes, com base nas configurações de "número máximo de temas".</span><span class="sxs-lookup"><span data-stu-id="6f805-p107">**Suggested themes**You can suggest theme words to control Themes processing. Advanced eDiscovery will focus on these suggested words and try to create one or more relevant themes, based on the "Max number of themes" settings.</span></span> 
    
    <span data-ttu-id="6f805-p108">Por exemplo, se a palavra sugerida for "computador" e você tiver especificado "2" como o "número máximo de temas", a descoberta eletrônica avançada tentará gerar dois temas relacionados à palavra "computador". Os dois temas podem ser "software de computador" e "hardware de computador", por exemplo.</span><span class="sxs-lookup"><span data-stu-id="6f805-p108">For example, if the suggested word is "computer", and you specified "2" as the "Max number of Themes", Advanced eDiscovery will try to generate two themes that relate to the word "computer". The two themes might be "computer software" and "computer hardware", for example.</span></span> 
    
    ![Adicionar tema sugerido](media/06e9ffd3-a76c-423b-b450-9e465eb9a02f.png)
  
1. <span data-ttu-id="6f805-129">Para exibir, adicionar ou editar temas sugeridos, clique em **Modificar**.</span><span class="sxs-lookup"><span data-stu-id="6f805-129">To view, add, or edit suggested themes, click **Modify**.</span></span>
    
2. <span data-ttu-id="6f805-p109">No painel **temas sugeridos** , clique no ícone **Adicionar**![ícone](media/c2dd8b3a-5a22-412c-a7fa-143f5b2b5612.png) de adição para adicionar um tema. No painel **Adicionar tema sugerido** , adicione as palavras, separadas por vírgulas.</span><span class="sxs-lookup"><span data-stu-id="6f805-p109">In the **Suggested themes** panel, click the **Add**![add icon](media/c2dd8b3a-5a22-412c-a7fa-143f5b2b5612.png) icon to add a theme. In the **Add suggested theme** panel, add the words, separated by commas.</span></span> 
    
3. <span data-ttu-id="6f805-132">Em **número de temas**, selecione um valor para determinar o número de temas que a descoberta eletrônica avançada tentará gerar para essas palavras (o padrão é 1 tema).</span><span class="sxs-lookup"><span data-stu-id="6f805-132">In **Number of themes**, select a value to determine the number of themes Advanced eDiscovery will try to generate for these words (default is 1 theme).</span></span>
    
4. <span data-ttu-id="6f805-133">Clique em **salvar** e feche a caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="6f805-133">Click **Save** and then close the dialogue.</span></span> 
    
    > [!NOTE]
    > <span data-ttu-id="6f805-p110">O número total de temas inclui temas sugeridos. O total de temas sugeridos não pode exceder o total de temas. Se houver muitos temas sugeridos em relação ao total de temas, apenas alguns temas "romance" serão detectados pelo sistema porque a maioria dos temas será dedicada aos temas sugeridos.</span><span class="sxs-lookup"><span data-stu-id="6f805-p110">The total number of themes includes Suggested Themes. The total Suggested Themes cannot exceed the total themes. If there are many Suggested Themes relative to the total themes, only a few "novel" themes will be detected by the system because most of the themes will be dedicated to Suggested Themes.</span></span> 
  
- <span data-ttu-id="6f805-137">**Modo** Na lista suspensa, selecione uma opção de **temas** :</span><span class="sxs-lookup"><span data-stu-id="6f805-137">**Mode** From the drop-down list, select a **Themes** option:</span></span> 
    
  - <span data-ttu-id="6f805-138">**Criar e aplicar modelo**: calcula temas por modelos de um segmento dos arquivos e, em seguida, distribui arquivos entre eles.</span><span class="sxs-lookup"><span data-stu-id="6f805-138">**Create and apply model**: Calculates themes by models from a segment of the files and then distributes files among them.</span></span>
    
  - <span data-ttu-id="6f805-p111">**Criar modelo**: calcula um modelo de temas de um segmento dos arquivos. O processo de aplicação de divisão de arquivos é feito separadamente em outro momento.</span><span class="sxs-lookup"><span data-stu-id="6f805-p111">**Create model**: Calculates a themes model from a segment of the files. The Apply process of dividing files is done separately at another time.</span></span>
    
  - <span data-ttu-id="6f805-p112">**Aplicar modelo**: essa opção só será mostrada se um modelo foi criado anteriormente e ainda não foi aplicado. Isso irá dividir os arquivos com base nos temas.</span><span class="sxs-lookup"><span data-stu-id="6f805-p112">**Apply model**: This option is only shown if a model was created previously and not yet applied. This will divide the files based on the themes.</span></span>
    
<span data-ttu-id="6f805-143">Você também pode [definir ignorar texto](set-ignore-text-in-advanced-ediscovery.md) e [definir as configurações avançadas de análise](set-analyze-advanced-settings-in-advanced-ediscovery.md) para análise.</span><span class="sxs-lookup"><span data-stu-id="6f805-143">You can also [set ignore text](set-ignore-text-in-advanced-ediscovery.md) and [set Analyze advanced settings](set-analyze-advanced-settings-in-advanced-ediscovery.md) for Analyze.</span></span> 
  
<span data-ttu-id="6f805-p113">Após definir essas opções, clique em **analisar** para executar. [Exibir resultados da análise](view-analyze-results-in-advanced-ediscovery.md) são exibidos.</span><span class="sxs-lookup"><span data-stu-id="6f805-p113">After you've set these options, click **Analyze** to run. [View Analyze results](view-analyze-results-in-advanced-ediscovery.md) are displayed.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="6f805-146">Confira também</span><span class="sxs-lookup"><span data-stu-id="6f805-146">See also</span></span>

[<span data-ttu-id="6f805-147">Descoberta Eletrônica Avançada do Office 365</span><span class="sxs-lookup"><span data-stu-id="6f805-147">Office 365 Advanced eDiscovery</span></span>](office-365-advanced-ediscovery.md)
  
[<span data-ttu-id="6f805-148">Noções básicas sobre a similaridade de documentos</span><span class="sxs-lookup"><span data-stu-id="6f805-148">Understanding document similarity</span></span>](understand-document-similarity-in-advanced-ediscovery.md)
  
[<span data-ttu-id="6f805-149">Definir o texto de ignorar</span><span class="sxs-lookup"><span data-stu-id="6f805-149">Set Ignore text </span></span>](set-ignore-text-in-advanced-ediscovery.md)
  
[<span data-ttu-id="6f805-150">Definir as configurações avançadas de análise</span><span class="sxs-lookup"><span data-stu-id="6f805-150">Set Analyze advanced settings</span></span>](set-analyze-advanced-settings-in-advanced-ediscovery.md)
  
[<span data-ttu-id="6f805-151">Exibir resultados de análise</span><span class="sxs-lookup"><span data-stu-id="6f805-151">View Analyze results</span></span>](view-analyze-results-in-advanced-ediscovery.md)

