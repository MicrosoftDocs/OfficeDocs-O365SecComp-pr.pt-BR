---
title: Executar o Módulo de processo e carregar dados na Descoberta Eletrônica Avançada do Office 365
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
ms.assetid: c87bb0e5-301c-4d1d-958e-aabeb7990f44
description: 'Saiba como usar a segurança do Office 365 &amp; Centro de conformidade para acessar o eDiscovery avançadas do Office 365 e execute o módulo de processo para uma ocorrência.  '
ms.openlocfilehash: 32052bccc37d20c8707a1efb0592f7c93daf3590
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22524066"
---
# <a name="run-the-process-module-and-load-data-in-office-365-advanced-ediscovery"></a>Executar o Módulo de processo e carregar dados na Descoberta Eletrônica Avançada do Office 365

> [!NOTE]
> EDiscovery Avançado requer um Office 365 E3 com o complemento de conformidade avançadas ou uma assinatura E5 para sua organização. Se você não tiver que plano e quiser tentar eDiscovery avançado, você pode [inscrever-se para uma avaliação do Office 365 Enterprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279). 
  
Esta seção descreve a funcionalidade do módulo de processo de descoberta eletrônica avançado. 
  
Além dos dados de arquivo, metadados, como o tipo de arquivo, extensão, local ou caminho, data de criação e tempo, dos responsáveis, autor e assunto, podem ser carregado no avançada de descoberta eletrônica e salva para cada caso. Por exemplo, alguns metadados é calculado por eDiscovery avançado, quando os arquivos nativos são carregados. 
  
EDiscovery avançado fornece valores de metadados, agrupamentos de quase duplicados ou as pontuações de relevância de sistema. Outros metadados, como anotações de arquivo, podem ser adicionados pelo administrador. 
  
## <a name="running-process"></a>Processo em execução

> [!NOTE]
> Números de lote são atribuídos a um arquivo durante o processo para permitir que o controle dos arquivos. O número de lote também permite que a identificação de lotes de processo para opções de reprocessamento. Filtros adicionais estão disponíveis para filtrar por número de lote e sessões. 
  
Execute as seguintes etapas para executar o processo.
  
1. [Abrir a segurança do Office 365 &amp; Centro de conformidade](go-to-the-securitycompliance-center.md) . 
    
2. Vá para **pesquisa &amp; investigação** \> **eDiscovery** e, em seguida, clique em **Ir para descoberta eletrônica avançada**.
    
3. No eDiscovery avançada, selecione o caso apropriado na página **casos** exibida e clique em **Ir para o caso**.
    
4. Em **Prepare** \> **processo** \> **instalação**, selecione um contêiner da lista de recipientes disponíveis.
    
    ![Clique em processar para adicionar os resultados da pesquisa ao caso](media/50bdc55c-d378-4881-b302-31ef785fa359.png)
  
5. Clique em **… Configurações avançadas** , se você deseja adicionar o contêiner, como arquivos de propagação ou como arquivos previamente marcados. 
    
    Usar arquivos de propagação para acelerar o treinamento para problemas com baixa riqueza (geralmente 2% ou menos). Para arquivos de propagação, é recomendável que você selecione uma variedade de arquivos distintamente relevantes e processar sobre sementes 20 e 50 por problema (muitos arquivos de propagação podem distorcer os resultados de relevância). Arquivos de propagação devem ser revisados pela mesma pessoa que irá treinar o problema.
    
    Use arquivos previamente marcados para automatizar treinamento de relevância. Você deve marcar pelo menos 1.500 arquivos e manter a proporção de relevantes para arquivos não relevantes os mesmos que a coleção adicionada a relevância. Esses arquivos devem ser marcados manualmente, e você deve ter a certeza na qualidade da marcação.
    
    ![Captura de tela de avançadas a página de configurações de processamento de arquivos em lotes](media/3c25cb78-4484-41e5-bd34-3753c7ab6cf2.jpg)
  
  - Na seção de **propagação** : 
    
    Escolha **Marcar como arquivos de propagação** para marcar o contêiner como arquivos de propagação. Você também precisa escolher para atribuí-las por um problema de **problema** drop-down. Escolha **relevantes** ou **não é relevante** no menu suspenso **marca** . 
    
    > [!NOTE]
    > Depois que você definir arquivos como **propagação**, você não pode marcá-las como **previamente marcado**. 
  
  - Na seção **arquivos previamente marcados** : 
    
    Escolha **Marcar como arquivos previamente marcados** para marcar o contêiner como arquivos previamente marcados. Você também precisará atribuí-las por um problema de **problema** drop-down. Escolha **relevantes** ou **não é relevante** no menu suspenso **marca** . 
    
    > [!NOTE]
    > Depois que você definir arquivos como **previamente marcado**, você não pode marcá-las como **propagação**. 
  
  - Na seção **Email marcação** . conjunto que parte de um email processado devem ser marcada como propagação ou previamente marcado. 
    
6. Para começar, clique em **processo**. Quando concluir, os resultados do processo são exibidos.
    
7. (Opcional) Se você precisa atribuir a fontes de dados para dos responsáveis específico, você pode adicionar e editar os nomes dos responsáveis em **responsáveis** \> **Gerenciar** e atribuir responsáveis em **responsáveis** \> **atribuir**. 
    
Se você adicionar ao caso, você pode processar novamente.
  
## <a name="see-also"></a>Confira também

[Descoberta Eletrônica Avançada do Office 365](office-365-advanced-ediscovery.md)
  
[Exibição de resultados de módulo de processo](view-process-module-results-in-advanced-ediscovery.md)

