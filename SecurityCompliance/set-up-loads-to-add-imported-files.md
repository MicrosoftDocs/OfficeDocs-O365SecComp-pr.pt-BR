---
title: Configurar carregamentos para adicionar arquivos importados na Descoberta Eletrônica Avançada do Office 365
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
ms.assetid: 0e0a9d04-294f-4f54-8bf1-b32d81345126
description: 'Revise as etapas para adicionar arquivos importados ao última carga definidos ou lote, de arquivos antes da execução de treinamento de relevância no eDiscovery avançadas do Office 365.  '
ms.openlocfilehash: 2c986578b969b671351930fd6939a90e3a821dc2
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22524578"
---
# <a name="set-up-loads-to-add-imported-files-in-office-365-advanced-ediscovery"></a>Configurar carregamentos para adicionar arquivos importados na Descoberta Eletrônica Avançada do Office 365

> [!NOTE]
> EDiscovery Avançado requer um Office 365 E3 com o complemento de conformidade avançadas ou uma assinatura E5 para sua organização. Se você não tiver que plano e quiser tentar eDiscovery avançado, você pode [inscrever-se para uma avaliação do Office 365 Enterprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279). 
  
EDiscovery avançado, uma carga é um novo lote de arquivos adicionados a um caso. Por padrão, uma carga é definida e todos os arquivos importados são adicionados a ela. Antes de executar o treinamento de relevância, os arquivos importados devem ser adicionados à carga. 
  
Considere os seguintes cenários:
  
- Novos arquivos são conhecidos como se parecer com os arquivos anteriores carregados no banco de dados caso ou a carga anterior de arquivos era um conjunto aleatório usando o conjunto de arquivos. Neste exemplo, adicione os arquivos importados para o carregamento de arquivo atual.
    
- Novos arquivos são diferentes daqueles anteriores (por exemplo, a partir de uma fonte diferente), ou você não tiver nenhum conhecimento prévio que elas são semelhantes ou diferentes para as cargas anteriores. Neste cenário, adicione os arquivos importados para um novo arquivo de carga. EDiscovery avançado reconhece isso como um cenário de cargas sem interrupção, chama um processo que os, bloqueia o treinamento de relevância e cálculos de lote até que o ajuste for concluída, e a nova carga é integrada e treinada. 
    
## <a name="adding-imported-files-to-the-current-load"></a>Adicionando arquivos importados para a carga atual

Todos os arquivos importados devem ser adicionados a uma carga a serem processados no eDiscovery avançado. Arquivos importados são adicionados à última carga definida. Se você importar arquivos adicionais posteriormente, eles também devem ser adicionados à carga.
  
1. No **relevância \> instalação relevância** guia, selecione **cargas**.
    
    ![Guia Cargas de Configuração de Relevância](media/278aac7f-655f-462f-852a-6baa5d818768.png)
  
2. **Arquivos de inclusão**: selecionar uma opção para arquivos a serem incluídos. Por padrão, a adição de arquivos para a carga atual baseado na população "Todos os arquivos".
    
    > [!TIP]
    > Carrege todos os arquivos culled disponíveis na relevância. Se você pretende carregar apenas um subconjunto dos arquivos disponíveis, primeiro consulte com suporte, como carregar subconjuntos pode prejudicar o treinamento de relevância. 
  
3. Em **gerenciamento de cargas**, selecione uma carga.
    
4. Clique em **Adicionar arquivos**. Os arquivos são adicionados à carga e uma mensagem de confirmação é exibida. 
    
5. Clique em **OK**.
    
Os arquivos agora podem ser processados no eDiscovery avançado relevância para os arquivos de treinamento.
  
## <a name="editing-a-load-name-within-a-case"></a>Um nome de carga dentro de um caso de edição

Se a alteração do nome de carga, é recomendável usar um nome que é relevante ao caso.
  
1. No **relevância \> instalação relevância** guia, selecione **cargas**.
    
2. Na lista de **cargas de gerenciamento** , selecione uma carga e clique no ícone **Editar** . A janela de carga de editar é exibida. 
    
3. Insira as alterações e clique em **Okey**.
    
## <a name="adding-imported-files-to-a-new-load"></a>Adicionando arquivos importados para uma nova carga

Depois de iniciar o treinamento de relevância ou executando o cálculo de lote, convém importar e processar um conjunto adicional de arquivos. 
  
Durante o ajuste, você pode criar, marcar e analisar o conjunto de ajuste. EDiscovery avançado compara sua avaliação dos arquivos relevantes e não-relevantes na carga da nova no carregamentos anteriores. Com base nos resultados, você é solicitado a tomar decisões de recuperar o atraso, se necessário e avançado eDiscovery fornece recomendações com base nas informações de relevância acumuladas. 
  
Aplicação de cargas e funcionalidade os varia da seguinte maneira: 
  
- Quando você importa um novo arquivo de carga após o cálculo de lote, o eDiscovery avançado determina até que ponto os arquivos se encaixam em uma das seguintes categorias:
    
  - Semelhante (homogêneo): um round novo e personalizado de treinamento de relevância não é necessária e o conhecimento acumulado pela carga anterior pode ser aplicado "no estado em que se encontra" à carga nova. 
    
  - DISTINCT (heterogêneo): um round novo e personalizado de treinamento de relevância é necessária e o conhecimento acumulado pela carga anterior não pode ser aplicado. 
    
    Esses termos referem-se ao nível de semelhança de arquivos entre cargas e não no carrega. 
    
- Ao importar um novo arquivo de carga durante o treinamento de relevância (antes de cálculo de lote), ajuste permite continuar treinamento relevância fazendo o conjunto de arquivos Unido. Descoberta eletrônica avançada não estimar se a carga nova é semelhante ao ou distinta da carga anterior. Ele simplesmente coleta informações sobre a nova carga e habilita a relevância de treinamento continuar na nova e anterior define dos arquivos. 
    
- Quando houver várias questões em treinamento de relevância, bem como problemas após o cálculo de lote, o processo de recuperar o atraso é executado uma vez por todos os problemas e os resultados são calculados e exibidos para cada questão.
    
> [!NOTE]
> O tamanho da amostra recuperar o atraso pode variar. Ele depende do tamanho da carga nova em relação às cargas anteriores e o número de amostras concluídas antes de adicionar a nova carga. O exemplo de ajuste geralmente é um conjunto de arquivos de 200 para 2.000 para a nova carga. 
  
> [!TIP]
> Recuperar o atraso interrompe quaisquer outras tarefas e requer revisão e marcação de arquivo individuais. Portanto, você pode reduzir sobrecarga quando você adiciona novos arquivos em grandes lotes. 
  
## <a name="adding-a-new-file-load-using-catch-up-and-rolling-loads"></a>Adicionar uma nova carga de arquivo usando os e sem interrupção carrega

1. No **relevância \> instalação relevância** guia, selecione **cargas**.
    
2. Em **gerenciamento de cargas**, clique o **+** ícone para adicionar uma carga. Uma mensagem de confirmação é exibida. 
    
3. Clique em **Sim** para continuar. A caixa de diálogo **Adicionar novo carregar** é exibida. 
    
    > [!NOTE]
    > Você só pode adicionar uma nova carga se ações foram realizadas à carga anterior. 
  
4. Na caixa de diálogo **Adicionar novo de carga** , digite as informações de **carregar o nome** e a **Descrição** e clique em **Okey**. EDiscovery avançado adiciona uma nova carga.
    
5. Para importar o novo arquivo de carga, clique em **Adicionar arquivos**. Todos os novos arquivos são adicionados a essa carga. Depois de descoberta eletrônica avançada importa os arquivos, ela reconhece o cenário de cargas sem interrupção e indica ajuste como a próxima etapa.
    
6. Clique em **recuperar o atraso** na parte inferior da caixa de diálogo para executar o cenário. 
    
    Um único conjunto de recuperar o atraso, normalmente contendo os arquivos de 200 para 2.000 da carga de novo, é criado para todos os problemas permitir a marcação de arquivo simultâneo.
    
    São fornecidos detalhes sobre se cargas são similares ou distintos, se o eDiscovery avançado mescladas ou divididas o carrega automaticamente e informações relacionadas ao processamento na próxima etapa.
    
    Você pode marcar os arquivos e executar uma operação de calcular. A marcação habilita a relevância determinar se as cargas são similares ou distintos e permite que você continuar trabalhando com o novo conjunto de arquivos.
    
7. Depois que o conjunto de recuperar o atraso é analisado, exibir **relevância \> Track** para os resultados do ajuste. 
    
1. Se a nova carga de arquivo foi adicionada durante o treinamento de relevância (isto é, o problema ainda não tiver passaram pelo cálculo de lote), **treinamento continuar** é a próxima etapa, independentemente dos resultados do ajuste. 
    
    As cargas de novas e anteriores são processadas como uma carga e treinamento de relevância continua no conjunto Unido. Você agora estiverem terminadas com este procedimento e pode continuar treinamento de relevância. 
    
2. Se a carga nova foi adicionada após o cálculo de lote, vá para as etapas a seguir.
    
8. Para cargas novas adicionadas após o cálculo de lote, eDiscovery avançado determina se a nova carga é semelhante ao ou distintos de carregamentos anteriores, da seguinte maneira:
    
1. Se cargas encontradas para ser semelhante: nenhum treinamento relevância adicional é necessário. O painel mostra a próxima etapa recomendada é executar * * cálculo de lote * * novamente para calcular as pontuações de relevância para o novo carregamento. Cargas foram encontradas seja semelhante, de modo a análise de classificador anterior pode ser executada em novos arquivos. 
    
2. Se cargas encontradas distinto: treinamento mais relevância é necessário e a próxima etapa é a decisão de ajuste. Selecione uma decisão de ajuste da seguinte maneira:
    
    Se você selecionar **Mesclar cargas**, eDiscovery avançado mescla cargas anteriores e novas para o conjunto de treinamento. Embora a primeira carga passou pelo cálculo em lotes, mais treinamento será necessária. Continue treinamento cargas novas e anteriores juntos. Cálculo de lote, em seguida, será executado novamente e as pontuações de cálculo de lote anteriores devem ser ignoradas. Escolha esta seleção quando as pontuações de relevância de cargas existentes podem ser recalculadas, por exemplo, quando a revisão dos carregamentos de arquivo existente não foi iniciada.
    
    Se você selecionar a **divisão carrega**, continue treinamento relevância somente sobre a carga de nova. Neste exemplo, pontuações de cálculo de lote anteriores permanecerá como está. Escolha esta opção quando não da pontuações de relevância existentes para cargas existentes seja recalculadas, por exemplo, se a revisão de cargas existentes já tenha sido iniciada. As pontuações de relevância são gerenciadas separadamente a partir deste ponto em diante e não podem ser mescladas.
    
3. Clique em **continuar treinamento**.
    
## <a name="see-also"></a>Confira também

[Descoberta Eletrônica Avançada do Office 365](office-365-advanced-ediscovery.md)
  
[Definindo os problemas e como atribuir usuários](define-issues-and-assign-users.md)
  
[Definindo realçado palavras-chave e avançadas opções](define-highlighted-keywords-and-advanced-options.md)

