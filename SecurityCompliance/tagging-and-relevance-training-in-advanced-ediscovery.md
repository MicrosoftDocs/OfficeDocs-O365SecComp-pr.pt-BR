---
title: Treinamento de marcação e relevância na Descoberta Eletrônica Avançada do Office 365
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
ms.assetid: 8576cc86-d51b-4285-b54b-67184714cc62
description: 'Conheça as etapas a marca e, em seguida, trabalhar com um exemplo de treinamento de 40 arquivos durante o estágio de treinamento de relevância de eDiscovery avançadas do Office 365.  '
ms.openlocfilehash: 90272452c8c1317957e542eba07bc43722f9c0e9
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22524090"
---
# <a name="tagging-and-relevance-training-in-office-365-advanced-ediscovery"></a>Treinamento de marcação e relevância na Descoberta Eletrônica Avançada do Office 365

> [!NOTE]
> EDiscovery Avançado requer um Office 365 E3 com o complemento de conformidade avançadas ou uma assinatura E5 para sua organização. Se você não tiver que plano e quiser tentar eDiscovery avançado, você pode [inscrever-se para uma avaliação do Office 365 Enterprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279). 
  
Este tópico descreve o procedimento para trabalhar com o módulo de treinamento de relevância de descoberta eletrônica avançado. 
  
Após Assessment for concluída no eDiscovery avançado, e você inserir o estágio de treinamento de relevância, uma amostra de treinamento de 40 arquivos é transformada para a guia marca para marcação. 
  
## <a name="performing-relevance-training"></a>Executando o treinamento de relevância

1. No **relevância \> marca** guia, o painel de marcação é exibido por padrão no painel à esquerda e a amostra de arquivos são exibidos, um por vez para marcação. 
    
    ![Painel Marca de Relevância](media/0cf19ab4-b427-4a7f-8749-0f4ed9afaf58.png)
  
    Na guia **marca** , o nome para exibição do arquivo é mostrado. Isso poderia ser o caminho, assunto do email, cargo ou nome definido pelo usuário. A ID, o caminho do arquivo ou o caminho de texto pode ser copiado clicando no caminho do arquivo. 
    
    Na guia **marca** Mostrar estatísticas de marcação, o número de amostra do arquivo (na parte superior do painel à esquerda), o número do arquivo exibido atualmente sem o total de arquivos na amostra de (parte inferior do painel direito) e o número total atual dos arquivos marcados na amostra de (parte inferior do t ele painel esquerdo), que muda à medida que você marcar os arquivos. Isso se aplica para qualquer marcação de relevância feito na avaliação, treinamento, ajuste ou teste. 
    
    Ícones indicando a existência de comentários, marcas e família arquivos são exibidos no modo de exibição de arquivo em uma barra acima do arquivo.
    
2. Determine a relevância do arquivo para o problema de maiusculas e marca o arquivo usando os botões de ícone de opção de marcação ou atalhos de teclado, conforme mostrado na tabela a seguir:
    
| |
|**Opção de marcação**|**Descrição**|**Atalho do teclado**|**Para várias questões - em massa atalho de teclado de marca**|
|:-----|:-----|:-----|:-----|
|S  <br/> |Relevantes  <br/> |A  <br/> |SHIFT + Z  <br/> |
|NR  <br/> |Não é relevante  <br/> |X  <br/> |SHIFT + X  <br/> |
|Ignorar  <br/> |Ignorar  <br/> |C  <br/> |Shift + A  <br/> |
   
  - Quando há várias questões para um arquivo, após a marcação de um problema, move a seleção para a próxima edição (se houver). 
    
  - Palavras-chave que foram definidas pelo administrador ou do gerente de casos, quando o realce de palavras-chave (instalação de relevância \> realçado palavras-chave), será exibida (em cores especificadas) para ajudar a identificar arquivos relevantes durante a marcação. Se uma palavra-chave contém um sublinhado duplo, ele pode ser clicado para exibir uma dica de ferramenta com descrição da palavra-chave. 
    
    Opcionalmente, na guia **marca** , clique em **configurações de marca** para definir as seguintes opções: 
    
    ![Configurações de marca de relevância](media/533e89fa-7eb4-409e-ab07-f5aab9296dd8.png)
  
  - **Marca em massa**: Use esta opção para atribuir várias questões para um arquivo, selecionando **todos** para definir a marca para o arquivo selecionado para todos os problemas (substituições já marcados problemas) ou selecionando **o restante** para aplicar a marca para os problemas não marcados restantes. A opção selecionada permanece em vigor para todos os casos desse usuário até ser alterado pelo usuário (configuração é por usuário para casos de todas as do usuário). 
    
  - **Marca automático**: marque essa caixa de seleção para definir a outros problemas de um arquivo como não é relevante após uma única marcação relevantes.
    
  - **Avanço automático**: marque essa caixa de seleção para mover a seleção de arquivo exibido para o próximo arquivo quando a última ou somente o problema não marcado de marcação. 
    
    Arquivos ignorados não serão considerados para fins de pontuação de relevância e treinamento de relevância.
    
3. Comentários de texto livre, associados a um arquivo, podem ser exibidos e editados por meio da opção de **comentário** na lista suspensa painel esquerdo. (opcional) 
    
4. Diretrizes para marcação podem ser exibidas, selecionando a opção de **diretrizes de marcação** na lista suspensa painel esquerdo. 
    
5. Depois de concluir a todos os arquivos na lista de marcação e estiver pronto para calcular os resultados, clique em **Calcular**. A guia **faixa** é exibida. 
    
## <a name="working-with-the-sample-files-list"></a>Trabalhando com a lista de arquivos de amostra

A lista de arquivos de amostra permite exibir uma lista dos arquivos em um exemplo de treinamento e executar várias ação em um ou mais arquivos. Na **relevância** \> guia **marca** , no painel esquerdo de **arquivos de exemplo** exibe uma lista dos arquivos de amostra para processamento com avaliação, treinamento, ajuste e inconsistências de processos. 
  
1. No **relevância \> marca** guia, selecione os arquivos de exemplo na lista suspensa painel esquerdo. Os arquivos de exemplo estão listados no painel à esquerda. 
    
    ![Lista de arquivos de exemplo de Marca de Relevância](media/fd058bdd-645a-4af1-a1eb-bff08581cb18.png)
  
2. Selecione um número específico de amostra ou arquivo inserindo ou selecionando o seu número nas caixas de **amostra** ou o **arquivo** . 
    
  -   - Um número de sequência de arquivo está listado na coluna à esquerda da lista de arquivo exibido na guia **marca** . Clicando no cabeçalho, a ordem exibida original dos arquivos retorna à sua ordem original. 
    
  - Clicar em uma linha do arquivo exibe seu conteúdo no painel direito.
    
  - Navegar entre arquivos na amostra de atual usando as opções de barra de menu inferiores. Além disso, os atalhos de teclado de navegação estão disponíveis:
    
    Para navegar até o primeiro arquivo na amostra: Shift + Ctrl +\<
    
    Para navegar até o arquivo anterior na amostra: Shift +\<
    
    Para navegar até o próximo arquivo na amostra: Shift +\>
    
    Para navegar até o último arquivo na amostra: Shift + Ctrl +\>
    
## <a name="see-also"></a>Confira também

[Descoberta Eletrônica Avançada do Office 365](office-365-advanced-ediscovery.md)
  
[Noções básicas sobre avaliação na relevância](assessment-in-relevance-in-advanced-ediscovery.md)
  
[Avaliação e marcação](tagging-and-assessment-in-advanced-ediscovery.md)
  
[Análise de relevância de acompanhamento](track-relevance-analysis-in-advanced-ediscovery.md)
  
[Decidindo com base nos resultados](decision-based-on-the-results-in-advanced-ediscovery.md)
  
[Análise de relevância de teste](test-relevance-analysis-in-advanced-ediscovery.md)

