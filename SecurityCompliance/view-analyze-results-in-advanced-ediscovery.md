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
# <a name="view-analyze-results-in-office-365-advanced-ediscovery"></a>Exibir resultados de análise na Descoberta Eletrônica Avançada do Office 365

> [!NOTE]
> EDiscovery Avançado requer um Office 365 E3 com o complemento de conformidade avançadas ou uma assinatura E5 para sua organização. Se você não tiver que plano e quiser tentar eDiscovery avançado, você pode [inscrever-se para uma avaliação do Office 365 Enterprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279). 
  
No eDiscovery avançado, andamento e os resultados para o processo de analisar podem ser exibidos em uma variedade de exibe conforme descrito abaixo.
  
## <a name="view-analyze-task-status"></a>Exibir o status da tarefa de analisar

No **Prepare \> analisar \> resultados \> status da tarefa**, o status é exibido durante e após a execução do processo de análise. 
  
![Status de tarefa de análise](media/d0372978-ce08-4f4e-a1fc-aa918ae44364.png)
  
As tarefas exibidas podem variar dependendo das opções selecionadas. 
  
- **Término/ET: instalação**: prepara para o tempo de execução, por exemplo, define os parâmetros de execução e maiusculas.
    
- **Término/ET: cálculo de término**: análise de quase duplicados de processos de arquivos.
    
- **Término/ET: cálculo ET**: análise realiza Thread de Email no conjunto de email inteira.
    
- **Término/ET: dinamização e semelhanças**: executa pivot e processamento de semelhança do arquivo.
    
- **Término/ET: atualização de metadados**: Finaliza os novos dados coletados nos arquivos do banco de dados.
    
- **Temas: cálculo de temas**: executa a análise de temas. (Exibida somente se tiver selecionado).
    
- **Status da tarefa**: esta linha é exibida após a conclusão da tarefa. Enquanto estiver executando tarefas, a duração da execução é exibida.
    
> [!NOTE]
> Os resultados de analisar de perto duplicatas e segmentos de Email (término e ED) aplica-se ao número de documentos a serem processados. Ele não inclui arquivos duplicados exatos. 
  
## <a name="view-near-duplicates-and-email-threads-status"></a>Exibir o status de perto duplicatas e segmentos de Email

Os resultados da população de **destino** exibem o número de documentos, emails, anexos e erros da população de destino. 
  
Os resultados de **documentos** exibem o número de dinamização, perto duplicatas exclusivas e extraia os arquivos duplicados. 
  
Os resultados de **Emails** exibem o número de inclusive, inclusive menos, cópias inclusive exclusivas e o restante das mensagens de email. Os diferentes tipos de resultados de email são: 
  
- **Inclusiva**: um email inclusive é o nó terminação em um segmento de email e contém todos os o histórico anterior desse thread. Como resultado, o revisor com segurança pode se concentrar na inclusive email, sem a necessidade de ler as mensagens anteriores no segmento. 
    
- **Inclusiva menos**: um email inclusive é designado como inclusive subtração, se houver um ou mais anexos diferentes associados com os pais da mensagem inclusive. Neste contexto, o termo que pai é usado para mensagens localizadas para cima no segmento de email ou conversas são incluídos nesse email inclusive específico. Um revisor pode usar inclusive menos indicação como um sinal que embora talvez não seja necessário analisar o conteúdo dos pais inclusive email, ele pode ser útil revisar os anexos associados com os pais inclusive caminho. 
    
- **Inclusive cópia**: um email inclusive é designado como cópia inclusive se ela for a cópia de outra mensagem marcado como inclusive ou inclusive menos. Em outras palavras, essa mensagem tem o mesmo assunto e corpo como outra mensagem inclusive e, como tal, co reside nos mesmos nós. Como mensagens de cópia inclusive contêm o mesmo conteúdo, eles geralmente podem ser ignorados no processo de revisão. 
    
- **O restante**: isso indica que o email que não contêm qualquer conteúdo exclusivo e, portanto, não se enquadram qualquer uma das três categorias anteriores. Essas mensagens de email não precisam ser revisados. Se uma mensagem contiver um anexo que não está em um email inclusive mais tarde, o anexo, em seguida, talvez seja necessário ser analisado. Isso é indicado pela existência de uma inclusive menos email dentro do segmento.
    
Os resultados de **anexos** exibem o número de anexos, de acordo com tal tipo como exclusivo e duplicatas. 
  
![Quase duplicatas e threads de email](media/54491303-0ee3-4739-b42e-d1ee486842fd.png)
  
## <a name="see-also"></a>Confira também

[Descoberta Eletrônica Avançada do Office 365](office-365-advanced-ediscovery.md)
  
[Noções básicas sobre semelhança de documento](understand-document-similarity-in-advanced-ediscovery.md)
  
[Definindo opções de analisar](set-analyze-options-in-advanced-ediscovery.md)
  
[Configuração Ignorar texto](set-ignore-text-in-advanced-ediscovery.md)
  
[Analisar configuração configurações avançada](view-analyze-results-in-advanced-ediscovery.md)

