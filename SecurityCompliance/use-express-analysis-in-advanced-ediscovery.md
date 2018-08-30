---
title: Usar análises expressas na Descoberta Eletrônica Avançada do Office 365
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
ms.assetid: 50580099-3dc0-44a1-a9b6-5ca6d396316b
description: Saiba como executar o modo de análise Express de eDiscovery avançadas do Office 365
ms.openlocfilehash: a71e6775b1116e805e455815dca53a727d887809
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22523919"
---
# <a name="use-express-analysis-in-office-365-advanced-ediscovery"></a>Usar análises expressas na Descoberta Eletrônica Avançada do Office 365

> [!NOTE]
> EDiscovery Avançado requer um Office 365 E3 com o complemento de conformidade avançadas ou uma assinatura E5 para sua organização. Se você não tiver que plano e quiser tentar eDiscovery avançado, você pode [inscrever-se para uma avaliação do Office 365 Enterprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279). 
  
Você pode usar o **Express análise** para analisar rapidamente um caso e exportar os resultados. 
  
Você pode usar a análise express para calcular perto duplicatas e segmentos de email e calcular temas. Você também pode definir determinados parâmetros para temas, semelhança do documento e os arquivos de exportação nas [Configurações avançadas para análise Express](use-express-analysis-in-advanced-ediscovery.md#BK_AdvancedSettings).
  
## <a name="run-express-analysis"></a>Executar a análise de Express

1. Na guia **analysis Express** (1), selecione um contêiner para habilitar o * * Express analysis * * (2) e os botões de **Configurações avançadas** . 
    
    ![Captura de tela da página análise Express](media/60009974-5d1f-4971-8ebe-e5ec74e7fd2a.jpg)
  
2. Em **Analisar parâmetros**:
    
  - Verifique **Calcular perto duplicatas e segmentos de email** se você deseja executar a análise. Ele é selecionado por padrão. 
    
  - Verifique se **Calcular temas** para processar todos os arquivos e atribua temas de. Ele é selecionado por padrão. 
    
3. Em **Exportar destino**:
    
  - Verifique a **baixar para a máquina local** para baixar para seu computador local. 
    
  - Se você marcar **Exportar para blob Azure definidas pelo usuário** , em seguida, você também pode especificar um token de URL e SAS do contêiner. 
    
    > [!NOTE]
    > Depois que um pacote de exportação é armazenado para o usuário definido Azure blob, os dados não mais são gerenciados por eDiscovery avançado. ele é gerenciado pelo Azure blob. Isso significa que se você excluir o caso, os arquivos exportados ainda vai permanecer no Azure blob. 
  
  - **Salvar SAS token para sessão de exportação futuras**: se estiver marcado, o token SAS será criptografado no banco de dados interno para uso futuro da descoberta eletrônica avançado.
    
    > [!NOTE]
    > Atualmente, o token SAS expira após um mês. Se você tentar baixar após mais de um mês em que você precise desfazer última sessão, exporte novamente. 
  
4. Para iniciar a análise express com padrão configurações, escolha **Express análise**e exibirá a página **status da tarefa** 
    
    Na página **status da tarefa** , você pode expandir as guias de **processo**, **Analisar** e **Exportar** para exibir os detalhes sobre a execução express. 
    
    ![Captura de tela de avançadas página status de tarefa de análise do eDiscovery Express](media/bf30ab02-9828-4a6d-a485-0babc2c49ae5.jpg)
  
5. Escolha a página de **Resumo de análise de Express** para listar as informações detalhadas sobre a execução. 
    
    Na parte inferior da página de **Resumo de análise de Express** , escolha a **última sessão de Download** para baixar a análise arquivos PA seu computador local. Primeiro, você terá que baixar a ferramenta de exportação de descoberta eletrônica e cole a chave de exportação para a ferramenta de exportação de descoberta eletrônica. 
    
## <a name="advanced-settings-for-express-analysis"></a>Configurações avançadas para análise Express
<a name="BK_AdvancedSettings"> </a>

Opcionalmente, você pode definir **Configurações avançadas** para alterar os parâmetros de análise Express padrão. 
  
1. Na seção **Analisar** : 
    
  - Na **quase duplicatas e segmentos de email**, insira o valor de **semelhança do documento** ou aceite o padrão de 65%. 
    
  - O **número máximo de temas** Insira ou selecione um valor para o número de temas para criar. O padrão é 200. 
    
    > [!NOTE]
    > Aumento do número de temas afeta o desempenho, bem como a capacidade de um tema para generalizar. Quanto maior o número de temas, mais granular são. Por exemplo, se um conjunto de 50 temas incluir um tema, como "Basquete, rumo, Cortador de Lakers"; 300 temas podem incluir separados temas: "Estimula os", "Cortador de", "Lakers". Se você tivesse sem reconhecimento do tema "Basquete" e usa esse recurso para ECA, vendo o tema "Basquete" poderia ser útil. Mas, se o processamento teve muitos temas, você nunca pode ver a palavra "Basquete" e talvez não saiba que rumo e cortador é boa temas basquete revisar, em vez de itens que vá é inicializado e usado para cabelo. 
  
  - Nos **temas sugeridos** escolha **Modificar** para sugerir palavras de tema para controlar o processamento de temas. EDiscovery avançado será enfocam essas palavras sugeridas e tente criar um ou mais temas relevantes, com base nas configurações de "Número de temas do Max". 
    
    Por exemplo, se a palavra sugerida é "computer", e você especificou "2" como o "número máximo de temas", o eDiscovery avançado tentará gere dois temas que se relacionam com a palavra "computador". Os dois temas poderiam ser "software de computador" e "hardware de computador", por exemplo.
    
    ![Adicionar tema sugerido](media/06e9ffd3-a76c-423b-b450-9e465eb9a02f.png)
  
  - **Modo** Na lista suspensa, selecione uma opção de **temas** : 
    
  - **Criar e aplicar modelo**: calcula temas por modelos a partir de um segmento dos arquivos e distribui arquivos entre eles.
    
  - **Criar modelo**: calcula um modelo de temas de um segmento dos arquivos. O processo de aplicar de divisão de arquivos é feito separadamente mais tarde.
    
  - **Aplicar modelo**: essa opção é mostrada somente se um modelo foi criado anteriormente e ainda não foi aplicado. Isso dividirá os arquivos com base nos temas.
    
2. Na seção **Exportar** : 
    
1. No **lote de exportação selecione**:
    
  - Na lista **Exportar lote** , selecione o nome do lote ou exportar resultados para o lote de exportação 01, (o lote padrão). 
    
  - Para exportar os resultados para novos arquivos adicionados a um caso existente, continue com o lote atual. Para criar uma sessão no lote, selecione o mesmo número de lote e clique em **criar exportar sessão** , você pode usar essa opção para exportar os mesmos parâmetros como o lote anterior, de forma incremental. 
    
  - Para exportar para um novo lote, clique em **Adicionar**![Adicionar ícone](media/c2dd8b3a-5a22-412c-a7fa-143f5b2b5612.png) e insira um novo nome em **nome de lote** (ou aceite o padrão) e uma descrição na **Descrição do lote**. Clique em **Okey**.
    
  - Para editar um nome de lote ou descrição, selecione o nome na **exportação em lote**, clique em **Editar** ![ícone Editar](media/3d613660-7602-4df2-bdb9-14e9ca2f9cf2.png)e, em seguida, modifique os campos.
    
    > [!NOTE]
    > Depois de executar sessões de um lote de exportação, eles não podem ser excluídos. Além disso, apenas alguns parâmetros podem ser editados depois que a primeira sessão é executada. 
  
  - Para criar um lote de exportação duplicados, escolha o **lote de exportação de duplicata**![criar um ícone de lote de exportação duplicados](media/3f6d5f59-e842-4946-a493-473528af0119.jpg) e insira um nome e uma descrição para o lote duplicado no painel. 
    
  - Para excluir um lote de exportação, escolha **Excluir**![excluir um ícone de lote de exportação](media/92a9f8e0-d469-48da-addb-69365e7ffb6f.jpg).
    
  - Para exibir o histórico de um lote, escolha o **histórico de lote**![ícone de histórico de exibição](media/a80cc320-d96c-4d91-8884-75fe2cb147e2.jpg).
    
2. Em definir p **opulation:** selecione **incluir somente os arquivos acima pontuação de interrupção de relevância** e/ou **refinar lote de exportação** , se quiser ajustar as configurações para o lote de exportação. Se você selecionar a opção **incluir somente os arquivos acima pontuação de interrupção de relevância**, o **problema** é habilitada e se a pontuação de relevância do arquivo for superior a pontuação de interrupção para o problema selecionado, o arquivo será exportado. O arquivo será exportado, a menos que ele for excluído pelo ' filtro **para revisão** . Se você selecionar **refinar exportação lote**, em seguida, a **eliminação da duplicação** e **Filter by 'Para revisão' campo** botões de opção estão habilitados. Se você escolher **eliminação da duplicação**, e depois duplicatas arquivos vai ser filtrada-out acordo com a política definida: [caso nível (padrão): a partir de cada conjunto de arquivos duplicados no caso de inteiro, apenas um arquivo será sua duplicação eliminado. Nível dos responsáveis: de cada conjunto de arquivos duplicados do dos responsáveis mesmo, apenas um arquivo será sua duplicação eliminado. Um registro de todos os arquivos duplicados está disponível na saída de exportação. Se você escolher campo **Filter by 'para revisão'** , selecione **Modificar em metadados** para inserir suas configurações de campo **'para revisão'**. Selecione **os arquivos de entrada incluir**para incluir os arquivos de origem no conteúdo do pacote. Você pode desmarcar essa opção para acelerar o processo de exportação. Observe que os arquivos nativos serão exportados em qualquer caso.
    
3. Em **definir metadados**, selecione entre as seguintes opções na lista **Exportar modelo** (uma vez por sessão). 
    
  - **Padrão**: conjunto básico de propriedades, metadados e itens de dados. Use esta opção quando importar dados já foi processados no eDiscovery avançado e exportar dados são carregados com um sistema que já contém os arquivos. Por padrão, exporte modelo colunas são criadas e preenchidas.
    
  - **Todos**: o conjunto completo de metadados padrão, incluindo todos os dados de processamento, bem como as pontuações de analisar e a relevância. Este modelo é necessário quando eDiscovery avançado realiza o processamento e dados de arquivo são carregados no sistema externo pela primeira vez.
    
  - **Problemas**: selecione **Todos os problemas** ou selecione um problema específico que você criou. 
    
Escolha **Okey**para salvar as configurações avançadas, **Restaurar padrões** para usar valores padrão ou em **Cancelar** para cancelar a definição de configurações avançadas. 
  
## <a name="see-also"></a>Confira também
<a name="BK_AdvancedSettings"> </a>

[Descoberta Eletrônica Avançada do Office 365](office-365-advanced-ediscovery.md)

