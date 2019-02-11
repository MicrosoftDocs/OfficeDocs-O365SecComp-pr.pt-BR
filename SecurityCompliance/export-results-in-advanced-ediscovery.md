---
title: Exportar resultados na Descoberta Eletrônica Avançada do Office 365
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
ms.assetid: a9951a07-10b3-48cb-b37a-0ffaa24931ad
description: 'Saiba como definir opções para exportar os resultados do eDiscovery avançadas do Office 365, incluindo o procedimento para especificar os parâmetros de um lote de exportação. '
ms.openlocfilehash: 49dab9820735af3bf5c322fc531c78a6baab2f8e
ms.sourcegitcommit: 7e2a0185cadea7f3a6afc5ddc445eac2e1ce22eb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/11/2019
ms.locfileid: "29559044"
---
# <a name="export-results-in-office-365-advanced-ediscovery"></a>Exportar resultados na Descoberta Eletrônica Avançada do Office 365

> [!NOTE]
> A Descoberta Eletrônica Avançada exige um Office 365 E3, com um complemento de Conformidade Avançada ou uma assinatura do E5 para sua organização. Se você não tiver esse plano e quiser tentar a Descoberta Eletrônica Avançada, poderá [Inscrever-se para uma avaliação do Office 365 Enterprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279). 
  
Este tópico descreve as opções de configuração de exportação de eDiscovery avançado.
  
 **Neste tópico:**
  
- [Definição de lotes de exportação e sessões](export-results-in-advanced-ediscovery.md#BK_Define)
    
- [Exportações incrementais e adicionais](export-results-in-advanced-ediscovery.md#BK_IncrementalReports)
    
- [Configurar os parâmetros de exportação em lote](export-results-in-advanced-ediscovery.md#BK_SetUpExport)
    
- [Exporte os arquivos de saída de relatório](export-results-in-advanced-ediscovery.md#BK_ExportOutputFIles)
    
## <a name="defining-export-batches-and-sessions"></a>Definição de lotes de exportação e sessões
<a name="BK_Define"> </a>

Um lote de exportação permite que o processo de exportação usando um conjunto de parâmetros definidos. EDiscovery avançado permite que você defina lotes para personalizar cada exportação.
  
Parâmetros são definidos por lote de exportação. Um lote denominado "Exportar lote 01" é criado por padrão para o primeiro lote de um caso. Você também pode editar o nome de lote e a descrição.
  
Uma sessão de exportação é uma execução de exportação de eDiscovery avançada dentro de um lote de exportação.
  
## <a name="incremental-and-additional-exports"></a>Exportações incrementais e adicionais
<a name="BK_IncrementalReports"> </a>

Você pode executar várias sessões de exportação dentro de um lote de exportação, para garantir resultados consistentes com base nos parâmetros e o mesmo modelo de exportação. Para cada sessão dentro de um lote, você pode exportar analytics para recentemente processados dados maiusculas e processar cada "incrementalmente".
  
Para exportar usando um conjunto de parâmetros diferentes, você precisa primeiro criar um novo lote. A primeira sessão no novo lote produzirá resultados para arquivos processados no caso de até o momento, se ou não esses arquivos foram importados e processados por um ou vários importações. Cada lote recalcula dinamização, semelhança, inclusives, etc. Sessões usam os parâmetros definidos para o lote e não recalcular dinamização, semelhança, inclusives, etc. para cada execução da sessão.
  
Por exemplo, suponha que um caso foi importado e seus dados analisados. Para recuperar perto duplicatas e Email Threading resultados para os dados incrementais, clique em **criar exportar sessão** no mesmo lote que era usado para exportar dados. 
  
## <a name="set-up-batch-export-parameters"></a>Configurar os parâmetros de exportação em lote
<a name="BK_SetUpExport"> </a>

A ferramenta de exportação de descoberta eletrônica é usada para exportar os resultados da pesquisa de descoberta eletrônica avançada ao computador local. Para aumentar a taxa de transferência de transferência de dados e a velocidade o processo de exportação, você pode configurar uma configuração de registro do Windows no computador que você usa para exportar os resultados da pesquisa. Se você quiser aumentar a velocidade de download, configure a configuração do registro antes de configurar os parâmetros de exportação. Para obter mais informações, consulte [aumentar a velocidade de download ao exportar os resultados da pesquisa de descoberta eletrônica do Office 365](increase-download-speeds-when-exporting-ediscovery-results.md).
  
1. No eDiscovery avançada, selecione um caso e clique em **Exportar** \> **instalação**.
    
    - Na lista **Exportar lote** , selecione o nome do lote ou exportar resultados para o lote de exportação 01, (o lote padrão). 
    
    - Para exportar os resultados para novos arquivos adicionados a um caso existente, continue com o lote atual. Para criar uma sessão no lote, selecione o mesmo número de lote e clique em **criar exportar sessão** , você pode usar essa opção para exportar os mesmos parâmetros como o lote anterior, de forma incremental. 
    
    - Para exportar para um novo lote, clique em **Adicionar** ![Adicionar ícone](media/c2dd8b3a-5a22-412c-a7fa-143f5b2b5612.png)e insira um novo nome em **nome de lote** (ou aceite o padrão) e uma descrição na **Descrição do lote**. Clique em **Okey**.
    
    - Para editar um nome de lote ou descrição, selecione o nome na **exportação em lote**, clique em **Editar** ![ícone Editar](media/3d613660-7602-4df2-bdb9-14e9ca2f9cf2.png)e, em seguida, modifique os campos.
    
      > [!NOTE]
      > Depois de executar sessões de um lote de exportação, eles não podem ser excluídos. Além disso, apenas alguns parâmetros podem ser editados depois que a primeira sessão é executada. 
  
    - Para criar um lote de exportação duplicados, escolha o **lote de exportação de duplicata** ![criar um ícone de lote de exportação duplicados](media/3f6d5f59-e842-4946-a493-473528af0119.jpg) e insira um nome e uma descrição para o lote duplicado no painel. 
    
    - Para excluir um lote de exportação, escolha **Excluir** ![excluir um ícone de lote de exportação](media/92a9f8e0-d469-48da-addb-69365e7ffb6f.jpg).
    
    - Para exibir o histórico de um lote, escolha o **histórico de lote** ![ícone de histórico de exibição](media/a80cc320-d96c-4d91-8884-75fe2cb147e2.jpg).
    
2. Em **população**, selecione **incluir somente os arquivos acima pontuação de interrupção de relevância** e/ou **refinar lote de exportação** , se você quiser ajustar as configurações para o lote de exportação. 
    
3. Se você selecionar a opção **incluir somente os arquivos acima pontuação de interrupção de relevância**, o **problema** é habilitado. Se a pontuação de relevância do arquivo for superior a pontuação de interrupção para o problema selecionado, o arquivo será exportado, a menos que ele é excluído pelo filtro 'para revisão'. 
  
    Se você selecionar **refinar exportação lote**, a **eliminação da duplicação** e filtrar por 'Para revisão' botões de opção de campo são ativados. Se você escolher **eliminação da duplicação**, e os arquivos duplicados serão filtrados de acordo com a política definida [caso nível (padrão): a partir de cada conjunto de arquivos duplicados no caso de inteiro, apenas um arquivo será sua duplicação eliminado. Nível dos responsáveis: de cada conjunto de arquivos duplicados do dos responsáveis mesmo, apenas um arquivo será sua duplicação eliminado.] A saída de exportação contém um registro de todos os arquivos duplicados. Se você escolher campo **Filter by 'para revisão'** , selecione **Modificar em metadados** para inserir suas configurações de campo **'para revisão'** . Selecione **os arquivos de entrada incluir** para incluir os arquivos de origem no conteúdo do pacote. Você pode desmarcar essa configuração para acelerar o processo de exportação. Observe que os arquivos nativos serão exportados em qualquer caso. 
    
4. Em **metadados**, selecione entre as seguintes opções na lista **Exportar modelo** (uma vez por sessão). 
    
    - **Padrão**: conjunto básico de propriedades, metadados e itens de dados. Use esta opção quando importar dados já foi processados no eDiscovery avançado e exportar dados são carregados com um sistema que já contém os arquivos. Por padrão, exporte modelo colunas são criadas e preenchidas.
    
    - **Todos**: o conjunto completo de metadados padrão, incluindo todos os dados de processamento, bem como as pontuações de analisar e a relevância. Este modelo é necessário quando eDiscovery avançado realiza o processamento e dados de arquivo são carregados no sistema externo pela primeira vez.
    
    - **Problemas**: selecione **Todos os problemas** ou selecione um problema específico que você criou. 
    
5. Em **destino**:
    
    - **Baixe a máquina local**
    
    - **Exportar para definidas pelo usuário blob Azure**: se essa opção estiver marcada, você pode especificar um token de URL e SAS do contêiner.
    
      > [!NOTE]
      > Assim que um pacote de exportação é armazenado para o usuário definido Azure blob, os dados não mais são gerenciados por eDiscovery avançado; ele é gerenciado pelo Azure blob. Isso significa que se você excluir o caso, os arquivos exportados ainda vai permanecer no Azure blob. 
  
    - **Salvar SAS token para sessão de exportação futuras**: se estiver marcado, o token SAS será criptografado no banco de dados interno para uso futuro da descoberta eletrônica avançado.
    
      > [!NOTE]
      > Atualmente, o token SAS expira após um mês. Se você tentar baixar após mais de um mês em que você precise desfazer última sessão, exporte novamente. 
  
6. Clique em **Modificar** para definir as configurações de campo 'para revisão'. 
    
    ![Configurar para configurações de campo de revisão de um lote de exportação](media/39451aba-f6fe-4a01-8ed0-0be6a6ce889a.png)
  
   - Em **para revisar configurações do campo**, na lista suspensa **Selecionar cenário** , selecione o cenário e o escopo da revisão. As configurações são exibidas com base em sua seleção.
    
      - **Examinar todos os** (padrão): todos os emails, anexos e documentos são marcados por padrão. 
    
      - **Examinar todo o conteúdo em um conjunto exclusivo**: Inclusives e cópias inclusive exclusivas, anexos exclusivos no email definir nível, representante de cada conjunto de cópias exatas.
    
      - **Revisar o conteúdo exclusivo em um conjunto - nenhuma cópia inclusive**: Inclusives, anexos exclusivos no email definir nível de representante de cada conjunto de cópias exatas.
    
      - **Analisar os arquivos de família conteúdos e relacionados de exclusivos todos**: Inclusives, anexos exclusivos no email definir o nível, o representante de cada conjunto de cópias exatas, expanda para incluir arquivos família.
    
      - **Sinalizador** (permite que você defina as opções na caixa de diálogo): O padrão é manter as seleções atuais e habilitar todas as opções de diálogo permitir que a sua seleção. Se você selecionar essa opção, você pode personalizar as configurações de emails, documentos, anexos e diversos.
    
    - Em **Emails**, selecione os emails que você deseja exportar.
    
      - **Todos os emails**: (padrão) todos os emails estão selecionados.
    
      - **Inclusives**: um email inclusive você encontra um email último de um segmento e contém todos os outros emails do segmento.
    
      - **Inclusives e exclusivas cópias inclusive**: Inclusive cópias e inclusives com o mesmo assunto, corpo e anexos; cópias inclusive exclusivas são exclusivas cópias desses emails.
    
    - Em **documentos**, selecione os documentos que você deseja exportar. 
    
      - **Todos os documentos**: (padrão) todos os documentos são selecionados.
    
      - **Dinamização**: um arquivo escolhido como representante do conjunto de perto duplicatas, que é geralmente usado como a linha de base ao revisar o conjunto.
    
      - **Representante de cada conjunto de cópias exatas**: arquivos de quase duplicados exclusivos (incluindo o pivô).
    
    - Em **anexos**, selecione os anexos que você deseja exportar. 
    
      - **Todos os anexos**: (padrão) todos os anexos estão selecionados.
    
      - **Anexo exclusivo em nível de maiusculas**: arquivos de anexo exclusivo dentro do gabinete especificado.
    
      - **Anexo exclusivo em email definir nível**: arquivos de anexo exclusivo dentro do caso de email especificado.
    
   - Em**Micellaneous**, você pode escolher para **tratar anexos como documentos**, **trate emails como documentos**ou **Expandir para incluir arquivos família**. Quando você escolhe **Expand para incluir arquivos família**, para cada arquivo que foi sinalizado para revisão, todos os arquivos da mesma família também serão sinalizados.
    
7. Escolha **Salvar** para salvar as configurações. 
    
8. Depois de especificar os parâmetros de exportação, para iniciar o lote de exportação, clique em **criar exportar a sessão**.
    
    Durante a exportação, o status é exibido em **status da tarefa**. Os resultados são exibidos no **Resumo de exportação**.
    
9. Na janela de **Download de arquivos** , clique em **Copiar para a área de transferência** para copiar a chave de exportação. 
    
    ![Baixar arquivos](media/99cf2c13-4954-479f-9741-80d7458c1a15.png)
  
10. Clique em **Fechar**. 
    
    A ferramenta de exportação de descoberta eletrônica é iniciada.
    
    ![Ferramenta de exportação de Descoberta Eletrônica](media/705756ca-ee97-4d24-b70f-8b23513f6d11.gif)
  
11. Em que a **ferramenta de exportação de descoberta eletrônica**:
    
    -  Em **Colar a assinatura de acesso compartilhado que será usada para conectar a fonte**, cole a chave de exportação que youcopied na área de transferência na etapa 7.
    
    - Clique em **Procurar** para selecionar o local de destino para armazenar os arquivos de exportação baixado na máquina local. 
    
    - Clique em **Iniciar**. Os arquivos de exportação são baixados para a máquina local. Se você escolher **Exportar para blob Azure definidas pelo usuário** na etapa 4, a sessão é exportada para um destino de URL de armazenamento de Blob de sua escolha.
    
Para obter uma descrição completa dos campos no relatório de exportação, consulte [exportar campos do relatório](export-report-fields-in-advanced-ediscovery.md).
  
## <a name="export-report-output-files"></a>Exporte os arquivos de saída de relatório
<a name="BK_ExportOutputFIles"> </a>

A tabela a seguir lista os arquivos de saída que são gerados quando você executa um lote de exportação.
  
|**Nome do arquivo**|**Tipo de arquivo**|**Descrição**|
|:-----|:-----|:-----|
|Resumo de exportação  <br/> |CSV  <br/> |Um arquivo de log gerado pela ferramenta de exportação de descoberta eletrônica.  <br/> |
|Rastreamento  <br/> |txt  <br/> |Um arquivo de log gerado pela ferramenta de exportação de descoberta eletrônica.  <br/> |
|Arquivos de texto extraídos  <br/> |Pasta de arquivo  <br/> |Pasta que contém os arquivos de texto extraídos dos arquivos exportados.  <br/> |
|Entrada ou arquivos nativos  <br/> |Pasta de arquivo  <br/> |Pasta que contém os arquivos nativos e entrados dos arquivos exportados.  <br/> |
|Lista de exportação  <br/> |xlsx  <br/> |Metadados de arquivos exportados no formato xlsx. Campos nos arquivos estão de acordo com seleciona de usuário do modelo a ser exportado. Se necessário, vários arquivos são criados, cada um contém linhas de 100 a 150 mil. Se um determinado valor conterá mais caracteres do que uma célula do Excel pode conter (atualmente o limite é 32.767 caracteres), e em seguida, excluirá o valor para o tamanho máximo permitido. Se um valor é cortado, cor de plano de fundo da célula é vermelho para indicar isso ao usuário." Os participantes de email"é um exemplo de um campo que pode exceder o limite de comprimento, se o email foi enviado para uma distribuição grandes. Para obter detalhes sobre os campos de saída, consulte [exportar campos do relatório](export-report-fields-in-advanced-ediscovery.md) .<br/> |
|Carregar arquivo  <br/> |CSV  <br/> |Metadados de arquivos exportados no formato csv para carregamento em outro aplicativo. Campos nos arquivos estão de acordo com seleciona de usuário do modelo a ser exportado.  <br/> |
|Indicador de sucesso  <br/> |txt  <br/> |Só é criado durante a exportação para um 3rd Azure blob de terceiros. Se a exportação tiver êxito completamente, o arquivo será criado. Em caso de falha, ou parcial sucesso o arquivo não será criado. Arquivo será criado na pasta raiz, permitindo que automatizado de acompanhamento no status de lotes/sessões de exportação diferentes. Este é um arquivo vazio. Seu nome é: TenantId_CaseId_ExternalCaseId_CaseName_ExportBatchId_SessionId_DateTime.txt.  <br/> |
   
## <a name="see-also"></a>Confira também

[Descoberta Eletrônica Avançada do Office 365](office-365-advanced-ediscovery.md)
  
[Exibir o histórico de lote e exportando resultados passado](view-batch-history-and-export-past-results.md)
  
[Configuração rápida da Descoberta Eletrônica Avançada do Office 365](quick-setup-for-advanced-ediscovery.md)

[Campos de exportação de relatório](export-report-fields-in-advanced-ediscovery.md)
  
[Aumentar a velocidade de download ao exportar os resultados da pesquisa de descoberta eletrônica do Office 365](increase-download-speeds-when-exporting-ediscovery-results.md)

