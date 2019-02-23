---
title: Usar utilitários da Descoberta Eletrônica Avançada do Office 365
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
ms.assetid: 66ca9993-75f4-4724-aea2-5a0719b660c1
description: 'Saiba mais sobre os utilitários na descoberta eletrônica avançada do Office 365, incluindo log de caso, dados claros, erros de processo, modificar relevância e análise de transparência.  '
ms.openlocfilehash: bd100883804b300e77abcc8a2224cf1a59b53475
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30218201"
---
# <a name="use-office-365-advanced-ediscovery-utilities"></a><span data-ttu-id="ed795-103">Usar utilitários da Descoberta Eletrônica Avançada do Office 365</span><span class="sxs-lookup"><span data-stu-id="ed795-103">Use Office 365 Advanced eDiscovery utilities</span></span>

> [!NOTE]
> <span data-ttu-id="ed795-p101">A Descoberta Eletrônica Avançada exige um Office 365 E3, com um complemento de Conformidade Avançada ou uma assinatura do E5 para sua organização. Se você não tiver esse plano e quiser tentar a Descoberta Eletrônica Avançada, poderá [Inscrever-se para uma avaliação do Office 365 Enterprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span><span class="sxs-lookup"><span data-stu-id="ed795-p101">Advanced eDiscovery requires an Office 365 E3 with the Advanced Compliance add-on or an E5 subscription for your organization. If you don't have that plan and want to try Advanced eDiscovery, you can [sign up for a trial of Office 365 Enterprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span></span> 
  
<span data-ttu-id="ed795-106">Os utilitários que são exibidos e estão disponíveis na descoberta eletrônica avançada dependem de contexto e funções de usuário.</span><span class="sxs-lookup"><span data-stu-id="ed795-106">The utilities that are displayed and available in Advanced eDiscovery depend on context and user roles.</span></span>
  
## <a name="case-log"></a><span data-ttu-id="ed795-107">Log de caso</span><span class="sxs-lookup"><span data-stu-id="ed795-107">Case log</span></span>

<span data-ttu-id="ed795-p102">O log de caso fornece uma lista detalhada das atividades de processamento do aplicativo, que podem ser usadas para controlar, solucionar problemas e para endereçar erros e avisos. O log pode ser gerado e armazenado localmente no host ou servidor ou enviado diretamente para um endereço de email.</span><span class="sxs-lookup"><span data-stu-id="ed795-p102">The Case log provides a detailed list of application processing activities, which can be used for tracking, troubleshooting, and for addressing errors and warnings. The log can be generated and stored locally on the host or server, or sent directly to an email address.</span></span>
  
<span data-ttu-id="ed795-p103">O arquivo de log também pode ser baixado no computador do cliente. A opção de download do cliente pode ser habilitada ou desabilitada de acordo com a configuração e a função do usuário.</span><span class="sxs-lookup"><span data-stu-id="ed795-p103">The log file can also be downloaded to the client's computer. The client download option may be enabled or disabled according to configuration and user role.</span></span>
  
1. <span data-ttu-id="ed795-112">Na barra de menus, clique no ícone **engrenagem** .</span><span class="sxs-lookup"><span data-stu-id="ed795-112">In the menu bar, click the **Cogwheel** icon.</span></span> 
    
2. <span data-ttu-id="ed795-113">Na guia **utilitários de configurações \> e utilitários** , selecione **a configuração \> de log de caso**.</span><span class="sxs-lookup"><span data-stu-id="ed795-113">In the **Settings and utilities \> Utilities** tab, select **Case log \> Setup**.</span></span>
    
3. <span data-ttu-id="ed795-114">Selecione o **nível de log** da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="ed795-114">Select the **Log level** as follows:</span></span> 
    
  - <span data-ttu-id="ed795-p104">**Padrão**: inclui os dados de log básicos. Essa opção geralmente é necessária para monitoramento e deve ser usada, a menos que o contrário seja recomendado.</span><span class="sxs-lookup"><span data-stu-id="ed795-p104">**Standard**: Includes the basic log data. This option is usually necessary for monitoring, and should be used unless recommended otherwise.</span></span>
    
  - <span data-ttu-id="ed795-117">**Mínimo**: usado em casos muito grandes e retorna apenas os dados mais recentes.</span><span class="sxs-lookup"><span data-stu-id="ed795-117">**Minimal**: Used for very large cases, and returns only the latest data.</span></span>
    
4. <span data-ttu-id="ed795-p105">Clique em **executar log de caso**. O log é gerado e o caminho é exibido. As informações de progresso da tarefa para a tarefa atual e a última são exibidas no painel de status da tarefa.</span><span class="sxs-lookup"><span data-stu-id="ed795-p105">Click **Run Case log**. The log is generated and path is displayed. The task progress information for the current and last task is displayed in the Task status pane.</span></span>
    
## <a name="clear-data"></a><span data-ttu-id="ed795-121">Limpar dados</span><span class="sxs-lookup"><span data-stu-id="ed795-121">Clear data</span></span>

<span data-ttu-id="ed795-p106">Se for necessário excluir ou reinicializar os dados da ocorrência, a instância do banco de dados deverá ser inicializada. O utilitário limpar dados exclui todas as entradas especificadas do banco de dados de casos, arquivos de texto, pastas de casos e resultados acumulados. A função só pode ser executada por um administrador.</span><span class="sxs-lookup"><span data-stu-id="ed795-p106">If it is necessary to delete or reinitialize case data, the database instance must be initialized. The Clear data utility deletes all specified entries from the case database, text files, case folder, and accumulated results. The function can only be performed by an administrator.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="ed795-p107">Esta ação não é reversível e desmarcará toda a marcação e análise de relevância executada pelo especialista. Salve um backup de dados, se necessário. Use essa opção com extrema cautela. Excluir arquivos marcados e classificados pode afetar os resultados de relevância.</span><span class="sxs-lookup"><span data-stu-id="ed795-p107">This action is not reversible and will clear all Relevance tagging and analysis performed by the expert. Save a backup of data, if necessary. Use this option with extreme care. Deleting tagged and ranked files can impact the Relevance results.</span></span> 
  
1. <span data-ttu-id="ed795-129">Na barra de menus, clique no ícone **engrenagem** .</span><span class="sxs-lookup"><span data-stu-id="ed795-129">In the menu bar, click the **Cogwheel** icon.</span></span> 
    
2. <span data-ttu-id="ed795-130">Na guia **utilitários de configurações \> e utilitários** , selecione **limpar configuração \> de dados**.</span><span class="sxs-lookup"><span data-stu-id="ed795-130">In the **Settings and utilities \> Utilities** tab, select **Clear data \> Setup**.</span></span>
    
3. <span data-ttu-id="ed795-131">Selecione uma opção para que as informações sejam inicializadas:</span><span class="sxs-lookup"><span data-stu-id="ed795-131">Select an option for the information to initialize:</span></span>
    
  - <span data-ttu-id="ed795-p108">**Relevância**: exclui todo o trabalho realizado de relevância, incluindo a definição de cargas e Associação de arquivos a serem carregados. Ele exclui todos os exemplos e marcação.</span><span class="sxs-lookup"><span data-stu-id="ed795-p108">**Relevance**: Deletes all work done in Relevance, including definition of loads and association of files to loads. It deletes all samples and tagging.</span></span>
    
  - <span data-ttu-id="ed795-134">**Duplicatas e threads de email**: exclui todas as informações de análise de quase duplicatas e threads de email.</span><span class="sxs-lookup"><span data-stu-id="ed795-134">**Near-duplicates and email threads**: Deletes all analysis information of near-duplicates and email threads.</span></span>
    
  - <span data-ttu-id="ed795-135">**Themes**: exclui os dados relacionados a temas.</span><span class="sxs-lookup"><span data-stu-id="ed795-135">**Themes**: Deletes themes-related data.</span></span>
    
  - <span data-ttu-id="ed795-136">**Export History**: Exclui informações de histórico de lotes de exportação.</span><span class="sxs-lookup"><span data-stu-id="ed795-136">**Export history**: Deletes history information of Export batches.</span></span>
    
4. <span data-ttu-id="ed795-p109">Clique em **limpar dados**. Os dados de caso são limpos. As informações de progresso da tarefa para a tarefa atual e a última são exibidas no painel de **status da tarefa** .</span><span class="sxs-lookup"><span data-stu-id="ed795-p109">Click **Clear data**. The case data is cleared. The task progress information for the current and last task is displayed in the **Task status** pane.</span></span> 
    
## <a name="modify-relevance"></a><span data-ttu-id="ed795-140">Modificar relevância</span><span class="sxs-lookup"><span data-stu-id="ed795-140">Modify Relevance</span></span>

<span data-ttu-id="ed795-141">Esta seção descreve como ignorar ou reverter uma amostra de relevância.</span><span class="sxs-lookup"><span data-stu-id="ed795-141">This section describes how to skip or roll back a Relevance sample.</span></span>
  
1. <span data-ttu-id="ed795-142">Na barra de menus, clique no ícone **engrenagem** .</span><span class="sxs-lookup"><span data-stu-id="ed795-142">In the menu bar, click the **Cogwheel** icon.</span></span> 
    
2. <span data-ttu-id="ed795-143">Na guia **utilitários de configurações \> e utilitários** , selecione **Modificar relevância**.</span><span class="sxs-lookup"><span data-stu-id="ed795-143">In the **Settings and utilities \> Utilities** tab, select **Modify relevance**.</span></span>
    
3. <span data-ttu-id="ed795-144">Selecione dentre as opções:</span><span class="sxs-lookup"><span data-stu-id="ed795-144">Select from the options:</span></span> 
    
  - <span data-ttu-id="ed795-p110">**Ignorar amostra atual-para usuário atual**: isso marcará, como **ignorar**, todos os arquivos não marcados no exemplo de caso aberto do usuário que está executando o utilitário. O processamento de relevância não será executado em arquivos marcados como **Skip**.</span><span class="sxs-lookup"><span data-stu-id="ed795-p110">**Skip current sample - for current user**: This will tag, as **Skip**, all untagged files in the open case sample of the user running the utility. Relevance processing will not be performed on files tagged as **Skip**.</span></span>
    
  - <span data-ttu-id="ed795-p111">**Ignorar amostra atual-todos os exemplos abertos**: isso marcará, como **ignorar**, todos os arquivos não marcados em todos os exemplos abertos de todos os usuários. Essa opção não é recomendada se os usuários estiverem atualmente em uma marcação de amostra.</span><span class="sxs-lookup"><span data-stu-id="ed795-p111">**Skip current sample - all open samples**: This will tag, as **Skip**, all untagged files in all open samples for all users. This option is not recommended if users are currently tagging samples.</span></span>
    
  - <span data-ttu-id="ed795-p112">**Reverter último exemplo**: a última amostra de treinamento de relevância será revertida, independentemente de estar antes ou após o processo de "cálculo". A reVersão de um exemplo de atualização não é permitida.</span><span class="sxs-lookup"><span data-stu-id="ed795-p112">**Roll back last sample**: The last completed Relevance training sample will be rolled back, regardless of whether it is before or after the "Calculate" process. Rollback of a catch-up sample is not allowed.</span></span>
    
4. <span data-ttu-id="ed795-151">Clique em **executar** para executar.</span><span class="sxs-lookup"><span data-stu-id="ed795-151">Click **Execute** to run.</span></span> 
    
## <a name="transparency-analysis"></a><span data-ttu-id="ed795-152">Análise de transparência</span><span class="sxs-lookup"><span data-stu-id="ed795-152">Transparency analysis</span></span>

<span data-ttu-id="ed795-p113">O utilitário de análise transparência permite uma visão detalhada dos arquivos e a pontuação de relevância atribuída. O relatório pode ser usado como uma verificação de sanidade ou para comparar a relevância de um arquivo definido por um revisor humano em comparação à relevância atribuída pela descoberta eletrônica avançada.</span><span class="sxs-lookup"><span data-stu-id="ed795-p113">The Transparency analysis utility enables a detailed view of files and their assigned Relevance score. The report can be used as a sanity check or to compare the relevance of a file defined by a human reviewer as compared to the relevance assigned by Advanced eDiscovery.</span></span> 
  
<span data-ttu-id="ed795-p114">Além da Pontuação de relevância, a descoberta eletrônica avançada calcula e atribui pesos de palavras-chave que consideram o contexto da palavra-chave. A mesma palavra em um arquivo pode ser atribuída a diferentes pesos, dependendo do contexto e local. Cada palavra-chave é marcada usando uma escala crescente de intensidade de cor variando de amarelo para laranja escuro e tons de cinza variados. A codificação de cores é usada para indicar visualmente a contribuição positiva ou negativa relativa do Word à pontuação de relevância.</span><span class="sxs-lookup"><span data-stu-id="ed795-p114">In addition to Relevance scores, Advanced eDiscovery calculates and assigns keyword weights that consider the keyword context. The same word in a file can be assigned different weights, depending on context and location. Each keyword is marked using an increasing scale of color intensity ranging from yellow to dark orange and varying shades of gray. Color coding is used to visually indicate the word's relative positive or negative contribution to the Relevance score.</span></span> 
  
<span data-ttu-id="ed795-159">Em um cenário de caso de vários problemas, um relatório de análise de transparência pode ser gerado para cada problema.</span><span class="sxs-lookup"><span data-stu-id="ed795-159">In a multiple-issue case scenario, a Transparency analysis report can be generated for each issue.</span></span>
  
1. <span data-ttu-id="ed795-160">Na barra de menus, clique no ícone **engrenagem** .</span><span class="sxs-lookup"><span data-stu-id="ed795-160">In the menu bar, click the **Cogwheel** icon.</span></span> 
    
2. <span data-ttu-id="ed795-161">Na guia **utilitários de configurações \> e utilitários** , selecione **configuração de \> análise de transparência**.</span><span class="sxs-lookup"><span data-stu-id="ed795-161">In the **Settings and utilities \> Utilities** tab, select **Transparency analysis \> Setup**.</span></span>
    
3. <span data-ttu-id="ed795-162">Em \* \* ID de arquivo \* \*, insira a ID de arquivo do arquivo a ser processado.</span><span class="sxs-lookup"><span data-stu-id="ed795-162">In \*\* File ID \*\*, enter the file ID of the file to process.</span></span>
    
4. <span data-ttu-id="ed795-163">Na lista **problema** , selecione o problema pertinente.</span><span class="sxs-lookup"><span data-stu-id="ed795-163">In the **Issue** list, select the pertinent issue.</span></span> 
    
5. <span data-ttu-id="ed795-p115">Clique em **análise de transparência**. Após a conclusão, o relatório de análise de transparência do arquivo é exibido, mostrando como as cores de palavra-chave marcadas são correlacionadas à pontuação de relevância geral.</span><span class="sxs-lookup"><span data-stu-id="ed795-p115">Click **Transparency analysis**. Upon completion, the Transparency analysis report for the file is displayed, which shows how the marked keyword colors correlate to the overall Relevance score.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="ed795-166">Confira também</span><span class="sxs-lookup"><span data-stu-id="ed795-166">See also</span></span>

[<span data-ttu-id="ed795-167">Descoberta Eletrônica Avançada do Office 365</span><span class="sxs-lookup"><span data-stu-id="ed795-167">Office 365 Advanced eDiscovery</span></span>](office-365-advanced-ediscovery.md)
  
[<span data-ttu-id="ed795-168">Definindo configurações de caso e de locatário</span><span class="sxs-lookup"><span data-stu-id="ed795-168">Defining case and tenant settings</span></span>](define-case-and-tenant-settings-in-advanced-ediscovery.md)

