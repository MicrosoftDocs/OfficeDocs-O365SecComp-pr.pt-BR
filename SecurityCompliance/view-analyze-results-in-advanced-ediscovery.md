---
title: Exibir resultados de análise na Descoberta Eletrônica Avançada do Office 365
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
ms.assetid: 5974f3c2-89fe-4c5f-ac7b-57f214437f7e
description: 'Compreenda where exibir os resultados do processo de análise no eDiscovery avançadas do Office 365, incluindo definições das opções de tipo de exibição de tarefa.  '
ms.openlocfilehash: 8f1de53e5548c8721f8fbfdb83374edb18379114
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22524441"
---
# <a name="view-analyze-results-in-office-365-advanced-ediscovery"></a><span data-ttu-id="1285a-103">Exibir resultados de análise na Descoberta Eletrônica Avançada do Office 365</span><span class="sxs-lookup"><span data-stu-id="1285a-103">View Analyze results in Office 365 Advanced eDiscovery</span></span>

> [!NOTE]
> <span data-ttu-id="1285a-p101">EDiscovery Avançado requer um Office 365 E3 com o complemento de conformidade avançadas ou uma assinatura E5 para sua organização. Se você não tiver que plano e quiser tentar eDiscovery avançado, você pode [inscrever-se para uma avaliação do Office 365 Enterprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span><span class="sxs-lookup"><span data-stu-id="1285a-p101">Advanced eDiscovery requires an Office 365 E3 with the Advanced Compliance add-on or an E5 subscription for your organization. If you don't have that plan and want to try Advanced eDiscovery, you can [sign up for a trial of Office 365 Enterprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span></span> 
  
<span data-ttu-id="1285a-106">No eDiscovery avançado, andamento e os resultados para o processo de analisar podem ser exibidos em uma variedade de exibe conforme descrito abaixo.</span><span class="sxs-lookup"><span data-stu-id="1285a-106">In Advanced eDiscovery, progress and results for the Analyze process can be viewed in a variety of displays as described below.</span></span>
  
## <a name="view-analyze-task-status"></a><span data-ttu-id="1285a-107">Exibir o status da tarefa de analisar</span><span class="sxs-lookup"><span data-stu-id="1285a-107">View Analyze task status</span></span>

<span data-ttu-id="1285a-108">No **Prepare \> analisar \> resultados \> status da tarefa**, o status é exibido durante e após a execução do processo de análise.</span><span class="sxs-lookup"><span data-stu-id="1285a-108">In **Prepare \> Analyze \> Results \> Task status**, the status is displayed during and after Analyze process execution.</span></span> 
  
![Status de tarefa de análise](media/d0372978-ce08-4f4e-a1fc-aa918ae44364.png)
  
<span data-ttu-id="1285a-110">As tarefas exibidas podem variar dependendo das opções selecionadas.</span><span class="sxs-lookup"><span data-stu-id="1285a-110">The tasks displayed may vary depending on the options selected.</span></span> 
  
- <span data-ttu-id="1285a-111">**Término/ET: instalação**: prepara para o tempo de execução, por exemplo, define os parâmetros de execução e maiusculas.</span><span class="sxs-lookup"><span data-stu-id="1285a-111">**ND/ET: setup**: Prepares for the run, for example, sets run and case parameters.</span></span>
    
- <span data-ttu-id="1285a-112">**Término/ET: cálculo de término**: análise de quase duplicados de processos de arquivos.</span><span class="sxs-lookup"><span data-stu-id="1285a-112">**ND/ET: ND calculation**: Processes Near-duplicate analysis of files.</span></span>
    
- <span data-ttu-id="1285a-113">**Término/ET: cálculo ET**: análise realiza Thread de Email no conjunto de email inteira.</span><span class="sxs-lookup"><span data-stu-id="1285a-113">**ND/ET: ET calculation**: Performs Email Thread analysis on the entire email set.</span></span>
    
- <span data-ttu-id="1285a-114">**Término/ET: dinamização e semelhanças**: executa pivot e processamento de semelhança do arquivo.</span><span class="sxs-lookup"><span data-stu-id="1285a-114">**ND/ET: pivots and similarities**: Performs pivot and file similarity processing.</span></span>
    
- <span data-ttu-id="1285a-115">**Término/ET: atualização de metadados**: Finaliza os novos dados coletados nos arquivos do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="1285a-115">**ND/ET: metadata update**: Finalizes the new data collected on the files in the database.</span></span>
    
- <span data-ttu-id="1285a-p102">**Temas: cálculo de temas**: executa a análise de temas. (Exibida somente se tiver selecionado).</span><span class="sxs-lookup"><span data-stu-id="1285a-p102">**Themes: themes calculation**: Runs themes analysis. (Displayed only if selected.)</span></span>
    
- <span data-ttu-id="1285a-p103">**Status da tarefa**: esta linha é exibida após a conclusão da tarefa. Enquanto estiver executando tarefas, a duração da execução é exibida.</span><span class="sxs-lookup"><span data-stu-id="1285a-p103">**Task status**: This line is displayed after task completion. While tasks are running, run duration is displayed.</span></span>
    
> [!NOTE]
> <span data-ttu-id="1285a-p104">Os resultados de analisar de perto duplicatas e segmentos de Email (término e ED) aplica-se ao número de documentos a serem processados. Ele não inclui arquivos duplicados exatos.</span><span class="sxs-lookup"><span data-stu-id="1285a-p104">The Analyze results of Near-duplicates and Email Threads (ND and ED) applies to the number of documents to be processed. It does not include Exact duplicate files.</span></span> 
  
## <a name="view-near-duplicates-and-email-threads-status"></a><span data-ttu-id="1285a-122">Exibir o status de perto duplicatas e segmentos de Email</span><span class="sxs-lookup"><span data-stu-id="1285a-122">View Near-duplicates and Email Threads status</span></span>

<span data-ttu-id="1285a-123">Os resultados da população de **destino** exibem o número de documentos, emails, anexos e erros da população de destino.</span><span class="sxs-lookup"><span data-stu-id="1285a-123">The **Target** population results display the number of documents, emails, attachments, and errors in the target population.</span></span> 
  
<span data-ttu-id="1285a-124">Os resultados de **documentos** exibem o número de dinamização, perto duplicatas exclusivas e extraia os arquivos duplicados.</span><span class="sxs-lookup"><span data-stu-id="1285a-124">The **Documents** results display the number of pivots, unique near-duplicates, and exact duplicate files.</span></span> 
  
<span data-ttu-id="1285a-p105">Os resultados de **Emails** exibem o número de inclusive, inclusive menos, cópias inclusive exclusivas e o restante das mensagens de email. Os diferentes tipos de resultados de email são:</span><span class="sxs-lookup"><span data-stu-id="1285a-p105">The **Emails** results display the number of inclusive, inclusive minus, unique inclusive copies, and the rest of the email messages. The different types of email results are:</span></span> 
  
- <span data-ttu-id="1285a-p106">**Inclusiva**: um email inclusive é o nó terminação em um segmento de email e contém todos os o histórico anterior desse thread. Como resultado, o revisor com segurança pode se concentrar na inclusive email, sem a necessidade de ler as mensagens anteriores no segmento.</span><span class="sxs-lookup"><span data-stu-id="1285a-p106">**Inclusive**: An inclusive email is the terminating node in an email thread and contains all the previous history of that thread. As a result, the reviewer can safely focus on the inclusive email, without the need to read the previous messages in the thread.</span></span> 
    
- <span data-ttu-id="1285a-p107">**Inclusiva menos**: um email inclusive é designado como inclusive subtração, se houver um ou mais anexos diferentes associados com os pais da mensagem inclusive. Neste contexto, o termo que pai é usado para mensagens localizadas para cima no segmento de email ou conversas são incluídos nesse email inclusive específico. Um revisor pode usar inclusive menos indicação como um sinal que embora talvez não seja necessário analisar o conteúdo dos pais inclusive email, ele pode ser útil revisar os anexos associados com os pais inclusive caminho.</span><span class="sxs-lookup"><span data-stu-id="1285a-p107">**Inclusive minus**: An inclusive email is designated as inclusive minus if there are one or more different attachments associated with the parents of the inclusive message. In this context, the term Parent is used for messages located upwards on the email thread or conversations included in that specific inclusive email. A reviewer can use the inclusive minus indication as a signal that although it might not be necessary to review the content of the inclusive email parents, it may be useful to review the attachments associated with the inclusive path parents.</span></span> 
    
- <span data-ttu-id="1285a-p108">**Inclusive cópia**: um email inclusive é designado como cópia inclusive se ela for a cópia de outra mensagem marcado como inclusive ou inclusive menos. Em outras palavras, essa mensagem tem o mesmo assunto e corpo como outra mensagem inclusive e, como tal, co reside nos mesmos nós. Como mensagens de cópia inclusive contêm o mesmo conteúdo, eles geralmente podem ser ignorados no processo de revisão.</span><span class="sxs-lookup"><span data-stu-id="1285a-p108">**Inclusive copy**: An inclusive email is designated as inclusive copy if it's the copy of another message marked as inclusive or inclusive minus. In other words, this message has the same subject and body as another inclusive message and, as such, co-resides in the same node. Because inclusive copy messages contain the same content, they can usually be skipped in the review process.</span></span> 
    
- <span data-ttu-id="1285a-p109">**O restante**: isso indica que o email que não contêm qualquer conteúdo exclusivo e, portanto, não se enquadram qualquer uma das três categorias anteriores. Essas mensagens de email não precisam ser revisados. Se uma mensagem contiver um anexo que não está em um email inclusive mais tarde, o anexo, em seguida, talvez seja necessário ser analisado. Isso é indicado pela existência de uma inclusive menos email dentro do segmento.</span><span class="sxs-lookup"><span data-stu-id="1285a-p109">**The rest**: This indicates email that doesn't contain any unique content, and therefore doesn't fall into any of the previous three categories. These email messages don't need to be reviewed. If a message contains an attachment that isn't on a later inclusive email, then the attachment might need to be reviewed. This is indicated by the existence of an inclusive minus email within the thread.</span></span>
    
<span data-ttu-id="1285a-139">Os resultados de **anexos** exibem o número de anexos, de acordo com tal tipo como exclusivo e duplicatas.</span><span class="sxs-lookup"><span data-stu-id="1285a-139">The **Attachments** results display the number of attachments, according to such type as unique and duplicates.</span></span> 
  
![Quase duplicatas e threads de email](media/54491303-0ee3-4739-b42e-d1ee486842fd.png)
  
## <a name="see-also"></a><span data-ttu-id="1285a-141">Confira também</span><span class="sxs-lookup"><span data-stu-id="1285a-141">See also</span></span>

[<span data-ttu-id="1285a-142">Descoberta Eletrônica Avançada do Office 365</span><span class="sxs-lookup"><span data-stu-id="1285a-142">Office 365 Advanced eDiscovery</span></span>](office-365-advanced-ediscovery.md)
  
[<span data-ttu-id="1285a-143">Noções básicas sobre semelhança de documento</span><span class="sxs-lookup"><span data-stu-id="1285a-143">Understanding document similarity</span></span>](understand-document-similarity-in-advanced-ediscovery.md)
  
[<span data-ttu-id="1285a-144">Definindo opções de analisar</span><span class="sxs-lookup"><span data-stu-id="1285a-144">Setting Analyze options</span></span>](set-analyze-options-in-advanced-ediscovery.md)
  
[<span data-ttu-id="1285a-145">Configuração Ignorar texto</span><span class="sxs-lookup"><span data-stu-id="1285a-145">Setting ignore text</span></span>](set-ignore-text-in-advanced-ediscovery.md)
  
[<span data-ttu-id="1285a-146">Analisar configuração configurações avançada</span><span class="sxs-lookup"><span data-stu-id="1285a-146">Setting Analyze advanced settings</span></span>](view-analyze-results-in-advanced-ediscovery.md)

