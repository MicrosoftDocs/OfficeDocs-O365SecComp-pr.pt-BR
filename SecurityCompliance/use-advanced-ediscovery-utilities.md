---
title: Usar utilitários da Descoberta Eletrônica Avançada do Office 365
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
ms.assetid: 66ca9993-75f4-4724-aea2-5a0719b660c1
description: 'Saiba mais sobre os utilitários no eDiscovery avançadas do Office 365, incluindo o log de caso, limpar dados, processar erros, modifique a relevância e a transparência de análise.  '
ms.openlocfilehash: a68c98dd353971fcaa13fdc6b8e12bcf00c2faf0
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22523538"
---
# <a name="use-office-365-advanced-ediscovery-utilities"></a><span data-ttu-id="f73b2-103">Usar utilitários da Descoberta Eletrônica Avançada do Office 365</span><span class="sxs-lookup"><span data-stu-id="f73b2-103">Use Office 365 Advanced eDiscovery utilities</span></span>

> [!NOTE]
> <span data-ttu-id="f73b2-p101">EDiscovery Avançado requer um Office 365 E3 com o complemento de conformidade avançadas ou uma assinatura E5 para sua organização. Se você não tiver que plano e quiser tentar eDiscovery avançado, você pode [inscrever-se para uma avaliação do Office 365 Enterprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span><span class="sxs-lookup"><span data-stu-id="f73b2-p101">Advanced eDiscovery requires an Office 365 E3 with the Advanced Compliance add-on or an E5 subscription for your organization. If you don't have that plan and want to try Advanced eDiscovery, you can [sign up for a trial of Office 365 Enterprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span></span> 
  
<span data-ttu-id="f73b2-106">Os utilitários que são exibidos e estão disponíveis no eDiscovery avançado dependem de funções de usuário e de contexto.</span><span class="sxs-lookup"><span data-stu-id="f73b2-106">The utilities that are displayed and available in Advanced eDiscovery depend on context and user roles.</span></span>
  
## <a name="case-log"></a><span data-ttu-id="f73b2-107">Log de caso</span><span class="sxs-lookup"><span data-stu-id="f73b2-107">Case log</span></span>

<span data-ttu-id="f73b2-p102">O log de caso fornece uma lista detalhada de atividades de processamento de aplicativo, que pode ser usado para acompanhamento, solução de problemas e para lidar com erros e avisos. O log pode ser gerado e armazenado localmente no servidor ou host ou enviado diretamente para um endereço de email.</span><span class="sxs-lookup"><span data-stu-id="f73b2-p102">The Case log provides a detailed list of application processing activities, which can be used for tracking, troubleshooting, and for addressing errors and warnings. The log can be generated and stored locally on the host or server, or sent directly to an email address.</span></span>
  
<span data-ttu-id="f73b2-p103">O arquivo de log também pode ser baixado para o computador do cliente. A opção de download do cliente pode ser habilitada ou desabilitada acordo com a função de configuração e do usuário.</span><span class="sxs-lookup"><span data-stu-id="f73b2-p103">The log file can also be downloaded to the client's computer. The client download option may be enabled or disabled according to configuration and user role.</span></span>
  
1. <span data-ttu-id="f73b2-112">Na barra de menus, clique no ícone de **Cogwheel** .</span><span class="sxs-lookup"><span data-stu-id="f73b2-112">In the menu bar, click the **Cogwheel** icon.</span></span> 
    
2. <span data-ttu-id="f73b2-113">No **configurações e utilitários \> utilitários** guia, selecione **log caso \> instalação**.</span><span class="sxs-lookup"><span data-stu-id="f73b2-113">In the **Settings and utilities \> Utilities** tab, select **Case log \> Setup**.</span></span>
    
3. <span data-ttu-id="f73b2-114">Selecione o **nível de Log** da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="f73b2-114">Select the **Log level** as follows:</span></span> 
    
  - <span data-ttu-id="f73b2-p104">**Padrão**: inclui os dados de log basic. Essa opção é geralmente necessária para monitoramento e deve ser usada a menos que recomendado caso contrário.</span><span class="sxs-lookup"><span data-stu-id="f73b2-p104">**Standard**: Includes the basic log data. This option is usually necessary for monitoring, and should be used unless recommended otherwise.</span></span>
    
  - <span data-ttu-id="f73b2-117">**Mínimo**: usada para casos muito grandes e retorna apenas os dados mais recentes.</span><span class="sxs-lookup"><span data-stu-id="f73b2-117">**Minimal**: Used for very large cases, and returns only the latest data.</span></span>
    
4. <span data-ttu-id="f73b2-p105">Clique em **Executar caso log**. O log é gerado e o caminho é exibido. As informações de andamento da tarefa atual e a última tarefa são exibidas no painel de status da tarefa.</span><span class="sxs-lookup"><span data-stu-id="f73b2-p105">Click **Run Case log**. The log is generated and path is displayed. The task progress information for the current and last task is displayed in the Task status pane.</span></span>
    
## <a name="clear-data"></a><span data-ttu-id="f73b2-121">Limpar dados</span><span class="sxs-lookup"><span data-stu-id="f73b2-121">Clear data</span></span>

<span data-ttu-id="f73b2-p106">Se for necessário excluir ou reinicializar dados casos, a instância do banco de dados deve ser inicializada. O utilitário de dados criptografado exclui especificadas todas as entradas do banco de dados de maiusculas, arquivos de texto, pasta maiusculas e resultados acumulados. A função só pode ser executada por um administrador.</span><span class="sxs-lookup"><span data-stu-id="f73b2-p106">If it is necessary to delete or reinitialize case data, the database instance must be initialized. The Clear data utility deletes all specified entries from the case database, text files, case folder, and accumulated results. The function can only be performed by an administrator.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="f73b2-p107">Essa ação não é reversível e limpará todas as marcas de relevância e análise executada pelo especialista. Salve um backup dos dados, se necessário. Use esta opção com muito cuidado. Excluindo arquivos marcados e classificados pode afetar os resultados de relevância.</span><span class="sxs-lookup"><span data-stu-id="f73b2-p107">This action is not reversible and will clear all Relevance tagging and analysis performed by the expert. Save a backup of data, if necessary. Use this option with extreme care. Deleting tagged and ranked files can impact the Relevance results.</span></span> 
  
1. <span data-ttu-id="f73b2-129">Na barra de menus, clique no ícone de **Cogwheel** .</span><span class="sxs-lookup"><span data-stu-id="f73b2-129">In the menu bar, click the **Cogwheel** icon.</span></span> 
    
2. <span data-ttu-id="f73b2-130">No **configurações e utilitários \> utilitários** guia, selecione **Limpar dados \> instalação**.</span><span class="sxs-lookup"><span data-stu-id="f73b2-130">In the **Settings and utilities \> Utilities** tab, select **Clear data \> Setup**.</span></span>
    
3. <span data-ttu-id="f73b2-131">Selecione uma opção para obter as informações inicializar:</span><span class="sxs-lookup"><span data-stu-id="f73b2-131">Select an option for the information to initialize:</span></span>
    
  - <span data-ttu-id="f73b2-p108">**Relevância**: exclui todo o trabalho feito na relevância, incluindo a definição de cargas e associação de arquivos para cargas. Ele exclui todos os exemplos e marcação.</span><span class="sxs-lookup"><span data-stu-id="f73b2-p108">**Relevance**: Deletes all work done in Relevance, including definition of loads and association of files to loads. It deletes all samples and tagging.</span></span>
    
  - <span data-ttu-id="f73b2-134">**Perto duplicatas e segmentos de email**: exclui todas as informações de análise de perto duplicatas e segmentos de email.</span><span class="sxs-lookup"><span data-stu-id="f73b2-134">**Near-duplicates and email threads**: Deletes all analysis information of near-duplicates and email threads.</span></span>
    
  - <span data-ttu-id="f73b2-135">**Temas**: exclui os dados relacionados à temas.</span><span class="sxs-lookup"><span data-stu-id="f73b2-135">**Themes**: Deletes themes-related data.</span></span>
    
  - <span data-ttu-id="f73b2-136">**Exportar histórico**: exclui informações de histórico de lotes de exportação.</span><span class="sxs-lookup"><span data-stu-id="f73b2-136">**Export history**: Deletes history information of Export batches.</span></span>
    
4. <span data-ttu-id="f73b2-p109">Clique em **Limpar dados**. Os dados casos esteja desmarcados. As informações de andamento da tarefa atual e a última tarefa são exibidas no painel de **status da tarefa** .</span><span class="sxs-lookup"><span data-stu-id="f73b2-p109">Click **Clear data**. The case data is cleared. The task progress information for the current and last task is displayed in the **Task status** pane.</span></span> 
    
## <a name="modify-relevance"></a><span data-ttu-id="f73b2-140">Modificar a relevância</span><span class="sxs-lookup"><span data-stu-id="f73b2-140">Modify Relevance</span></span>

<span data-ttu-id="f73b2-141">Esta seção descreve como ignorar ou reverter uma amostra de relevância.</span><span class="sxs-lookup"><span data-stu-id="f73b2-141">This section describes how to skip or roll back a Relevance sample.</span></span>
  
1. <span data-ttu-id="f73b2-142">Na barra de menus, clique no ícone de **Cogwheel** .</span><span class="sxs-lookup"><span data-stu-id="f73b2-142">In the menu bar, click the **Cogwheel** icon.</span></span> 
    
2. <span data-ttu-id="f73b2-143">No **configurações e utilitários \> utilitários** guia, selecione **Modificar relevância**.</span><span class="sxs-lookup"><span data-stu-id="f73b2-143">In the **Settings and utilities \> Utilities** tab, select **Modify relevance**.</span></span>
    
3. <span data-ttu-id="f73b2-144">Selecione uma das opções:</span><span class="sxs-lookup"><span data-stu-id="f73b2-144">Select from the options:</span></span> 
    
  - <span data-ttu-id="f73b2-p110">**Amostra do atual Ignorar - para o usuário atual**: isso irá marcar, como **Ignorar**, todos os arquivos desmarcados na amostra de maiusculas open do usuário que executa o utilitário. Processamento de relevância não será executado nos arquivos marcados como **Ignorar**.</span><span class="sxs-lookup"><span data-stu-id="f73b2-p110">**Skip current sample - for current user**: This will tag, as **Skip**, all untagged files in the open case sample of the user running the utility. Relevance processing will not be performed on files tagged as **Skip**.</span></span>
    
  - <span data-ttu-id="f73b2-p111">**Sample atual de ignorar - todas as abertas amostras**: isso irá marcar, como **Ignorar**, todos os arquivos desmarcados nas amostras abertos para todos os usuários. Essa opção não é recomendável se os usuários estão atualmente amostras de marcação.</span><span class="sxs-lookup"><span data-stu-id="f73b2-p111">**Skip current sample - all open samples**: This will tag, as **Skip**, all untagged files in all open samples for all users. This option is not recommended if users are currently tagging samples.</span></span>
    
  - <span data-ttu-id="f73b2-p112">**Reverter a última amostra**: O último concluído relevância amostra de treinamento será revertida, independentemente se ele está antes ou após o processo de "Calcular". Não é permitida a reversão de uma amostra os.</span><span class="sxs-lookup"><span data-stu-id="f73b2-p112">**Roll back last sample**: The last completed Relevance training sample will be rolled back, regardless of whether it is before or after the "Calculate" process. Rollback of a catch-up sample is not allowed.</span></span>
    
4. <span data-ttu-id="f73b2-151">Clique em **Executar** para executar.</span><span class="sxs-lookup"><span data-stu-id="f73b2-151">Click **Execute** to run.</span></span> 
    
## <a name="transparency-analysis"></a><span data-ttu-id="f73b2-152">Análise de transparência</span><span class="sxs-lookup"><span data-stu-id="f73b2-152">Transparency analysis</span></span>

<span data-ttu-id="f73b2-p113">O utilitário de análise de transparência permite uma exibição detalhada de arquivos e seus atribuídas pontuação de relevância. O relatório pode ser usado como uma verificação de integridade ou para comparar a relevância de um arquivo definido por um revisor humano em relação à relevância atribuído por eDiscovery avançado.</span><span class="sxs-lookup"><span data-stu-id="f73b2-p113">The Transparency analysis utility enables a detailed view of files and their assigned Relevance score. The report can be used as a sanity check or to compare the relevance of a file defined by a human reviewer as compared to the relevance assigned by Advanced eDiscovery.</span></span> 
  
<span data-ttu-id="f73b2-p114">Além da pontuação de relevância, o eDiscovery avançado calcula e atribui espessuras de palavra-chave que considerar o contexto de palavra-chave. A mesma palavra em um arquivo pode ser atribuída espessuras diferentes, dependendo do contexto e local. Cada palavra-chave é marcado usando uma escala de aumento de intensidade de cor desde amarelo para laranja escura e diversos tons de cinza. Codificação de cores é usada para indicar visualmente a palavra 's relativa positiva ou negativa contribuição para a pontuação de relevância.</span><span class="sxs-lookup"><span data-stu-id="f73b2-p114">In addition to Relevance scores, Advanced eDiscovery calculates and assigns keyword weights that consider the keyword context. The same word in a file can be assigned different weights, depending on context and location. Each keyword is marked using an increasing scale of color intensity ranging from yellow to dark orange and varying shades of gray. Color coding is used to visually indicate the word's relative positive or negative contribution to the Relevance score.</span></span> 
  
<span data-ttu-id="f73b2-159">Em um cenário de problema de vários caso, um relatório de análise de transparência pode ser gerado para cada questão.</span><span class="sxs-lookup"><span data-stu-id="f73b2-159">In a multiple-issue case scenario, a Transparency analysis report can be generated for each issue.</span></span>
  
1. <span data-ttu-id="f73b2-160">Na barra de menus, clique no ícone de **Cogwheel** .</span><span class="sxs-lookup"><span data-stu-id="f73b2-160">In the menu bar, click the **Cogwheel** icon.</span></span> 
    
2. <span data-ttu-id="f73b2-161">No **configurações e utilitários \> utilitários** guia, selecione **analysis transparência \> instalação**.</span><span class="sxs-lookup"><span data-stu-id="f73b2-161">In the **Settings and utilities \> Utilities** tab, select **Transparency analysis \> Setup**.</span></span>
    
3. <span data-ttu-id="f73b2-162">Em * * ID de arquivo * *, insira a ID de arquivo do arquivo para processar.</span><span class="sxs-lookup"><span data-stu-id="f73b2-162">In ** File ID **, enter the file ID of the file to process.</span></span>
    
4. <span data-ttu-id="f73b2-163">Na lista de **problema** , selecione o problema pertinente.</span><span class="sxs-lookup"><span data-stu-id="f73b2-163">In the **Issue** list, select the pertinent issue.</span></span> 
    
5. <span data-ttu-id="f73b2-p115">Clique em **transparência de análise**. Após a conclusão, o relatório de análise de transparência para o arquivo é exibido, que mostra como as cores de palavra-chave marcadas correlacionam para a pontuação de relevância geral.</span><span class="sxs-lookup"><span data-stu-id="f73b2-p115">Click **Transparency analysis**. Upon completion, the Transparency analysis report for the file is displayed, which shows how the marked keyword colors correlate to the overall Relevance score.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f73b2-166">Confira também</span><span class="sxs-lookup"><span data-stu-id="f73b2-166">See also</span></span>

[<span data-ttu-id="f73b2-167">Descoberta Eletrônica Avançada do Office 365</span><span class="sxs-lookup"><span data-stu-id="f73b2-167">Office 365 Advanced eDiscovery</span></span>](office-365-advanced-ediscovery.md)
  
[<span data-ttu-id="f73b2-168">Definindo configurações de maiusculas/minúsculas e locatário</span><span class="sxs-lookup"><span data-stu-id="f73b2-168">Defining case and tenant settings</span></span>](define-case-and-tenant-settings-in-advanced-ediscovery.md)

