---
title: Gerenciar investigações legais no Office 365
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 5/18/2018
ms.audience: Admin
ms.topic: hub-page
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 2e5fbe9f-ee4d-4178-8ff8-4356bc1b168e
description: Use os casos de eDiscovery no Office 365 Security &amp; Centro de conformidade para gerenciar a investigação de legais da sua organização. Se você tiver uma assinatura E5, você pode analisar os dados de ocorrências mais usando as capacidades de codificação previsão de indisponibilidade do eDiscovery avançado, aprendizado de máquina e análise de texto.
ms.openlocfilehash: ef8ff9347f7c1d604a01b70f54a1998fde91ace8
ms.sourcegitcommit: edf5db9357c0d34573f8cc406314525ef10d1eb9
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/28/2018
ms.locfileid: "23230023"
---
# <a name="manage-legal-investigations-in-office-365"></a>Gerenciar investigações legais no Office 365

As organizações têm vários motivos para responder a um caso jurídico envolvendo certos executivos ou outros funcionários em sua organização. Isso pode envolver rapidamente encontrar e manter para ainda mais investigação informações específicas em email, documentos, conversas de mensagens instantâneas e outro locais de conteúdo usado pelas pessoas em suas tarefas de trabalho diário. Você pode executar essas e muitas outras atividades semelhantes, usando as ferramentas de casos de descoberta eletrônica no Office 365 Security &amp; Centro de conformidade.
  
[Gerenciar investigações legais com casos de eDiscovery](#manage-legal-investigations-with-ediscovery-cases)
  
[Analisar dados maiusculas usando eDiscovery avançadas do Office 365](#analyze-case-data-using-office-365-advanced-ediscovery)
  
**Deseja saber como a Microsoft gerencia seus investigações de descoberta eletrônica?** Aqui está um [white paper técnico](https://go.microsoft.com/fwlink/?linkid=852161) você pode baixar que explica como podemos usar as mesmas ferramentas de pesquisa e a investigação do Office 365 para gerenciar nosso fluxo de trabalho do eDiscovery interno.
   
## <a name="manage-legal-investigations-with-ediscovery-cases"></a>Gerenciar investigações legais com casos de eDiscovery

descoberta eletrônica casos permitem que você controle quem pode criar, acessar e gerenciar casos do eDiscovery em sua organização. Casos de uso para adicionar membros e controle quais tipos de ações que eles possam executar, colocar uma isenção em locais de conteúdo relevante a um caso jurídico e usar a ferramenta de pesquisa de conteúdo para os locais de pesquisa em espera para o conteúdo que pode ser responsivo ao seu caso. Em seguida, também pode exportar e baixar esses resultados para uma investigação detalhada por revisores externos. Se sua organização do Office 365 tem e E5 assinatura, você pode também preparar os resultados da pesquisa para análise no eDiscovery avançado.
  
- [Gerenciar o fluxo de trabalho de descoberta eletrônica](ediscovery-cases.md) , criando e usando casos de eDiscovery para cada investigação legal sua organização deve se RESPONSABILIZARÃO 
    
- [Atribuir permissões de descoberta eletrônica](assign-ediscovery-permissions.md) para controlar quem pode criar e gerenciar casos do eDiscovery em sua organização 
    
- [Estabeleça os limites de conformidade](set-up-compliance-boundaries.md) para controlar os locais de conteúdo do usuário que os gerentes de descoberta eletrônica podem pesquisar 
    
- [Pesquisar conteúdo](search-for-content.md) na sua organização 
    
- [Prepare o conteúdo maiusculas para eDiscovery avançada](prepare-search-results-for-advanced-ediscovery.md) para que possa executar a análise de uso avançada analítico ferramentas eficientes do eDiscovery, como reconhecimento óptico de caracteres, threading de email e previsão de codificação 
    
### <a name="use-scripts-for-advanced-scenarios"></a>Usar scripts para cenários avançados

Como a seção anterior listados scripts para cenários de pesquisa de conteúdo, criamos também alguns segurança &amp; scripts do PowerShell do Centro de conformidade para ajudá-lo a gerenciar casos do eDiscovery.
  
- [Criar um eDiscovery reter relatório](create-a-report-on-holds-in-ediscovery-cases.md) que contém informações sobre todas as isenções associado casos de descoberta eletrônica em sua organização 
    
- [Adicionar caixas de correio e locais de OneDrive](use-a-script-to-add-users-to-a-hold-in-ediscovery.md) para obter uma lista de usuários de eDiscovery retenção 
  
## <a name="analyze-case-data-using-office-365-advanced-ediscovery"></a>Analisar dados maiusculas usando eDiscovery avançadas do Office 365

Descoberta eletrônica avançada do Office 365 aproveita os recursos de pesquisa e descoberta eletrônica conteúdos descritos nas seções anteriores. Depois de criar um caso de eDiscovery, locais dos responsáveis de local em espera e coletam dados que podem ser responsivos ao caso, você pode analisar melhor os dados usando as capacidades de codificação de previsão de indisponibilidade do avançado, aprendizado de máquina e a análise de texto descoberta eletrônica. Isso pode ajudar sua organização processar rapidamente milhares de mensagens de email, documentos e outros tipos de dados para localizar os itens que são bem prováveis relevantes a um caso específico. E, podemos ter unified eDiscovery avançada e gerenciamento de casos para que você possa gerenciar facilmente o mesmo caso dentro de segurança &amp; Centro de conformidade.
  
> [!NOTE]
> Para analisar dados de um usuário usando o eDiscovery avançado, o usuário (o de responsáveis dos dados) deve ser atribuído uma licença do Office 365 E5. Como alternativa, os usuários com uma licença do Office 365 E1 ou E3 podem ser atribuídos uma licença autônoma de eDiscovery avançado. Os administradores e oficiais de conformidade que estão atribuídos ao casos e usam o eDiscovery avançada para analisar dados não precisam de uma licença E5. 
  
### <a name="get-started"></a>Introdução

A maneira mais rápida para começar a descoberta eletrônica avançada é criar um caso e preparar os resultados da pesquisa em segurança &amp; Centro de conformidade, carga desses resultados no eDiscovery avançado e execute Express análise para analisar que caso dados e clique em seguida exportar o resultados para revisão externa.
  
- [Obtenha uma visão geral](quick-setup-for-advanced-ediscovery.md) do fluxo de trabalho avançada de eDiscovery 
    
- [Configurar usuários e casos](set-up-users-and-cases-in-advanced-ediscovery.md) do eDiscovery avançado criando um caso, atribuindo permissões de descoberta eletrônica e adicionando caso membros, tudo usando a segurança &amp; Centro de conformidade 
    
- [Preparar e carga de dados de pesquisa](prepare-data-for-advanced-ediscovery.md) ao caso no eDiscovery avançado 
    
- [Carregar dados do Office 365](import-non-office-365-data-into-advanced-ediscovery.md) na um caso analisá-lo no eDiscovery avançado 
    
- [Análise de uso Express](use-express-analysis-in-advanced-ediscovery.md) para analisar rapidamente os dados em um caso e exporte facilmente os resultados 
    
### <a name="analyze-data"></a>Analisar dados

Depois que os dados de pesquisa são carregados no caso da eDiscovery avançado, você usará o módulo de analisar para iniciar a análise-lo. A primeira parte do processo de análise consiste em organizar arquivos em grupos de arquivos exclusivos, duplicatas e quase duplicatas (também conhecido como semelhança de documento). Em seguida, você vai organizar os dados novamente em grupos hierarquicamente estruturados de threads de email e temas e, opcionalmente, o conjunto Ignorar texto filtros para excluir certo texto de análise. Em seguida, você executar a análise e exiba os resultados.
  
- [Saiba mais sobre semelhança de documento](understand-document-similarity-in-advanced-ediscovery.md) para prepará-lo para analisar dados no eDiscovery avançado 
    
- [Configurar as opções](set-analyze-options-in-advanced-ediscovery.md) para perto duplicatas, temas e email threading e execute o módulo de analisar 
    
- [Configurar filtros de Ignorar texto](set-ignore-text-in-advanced-ediscovery.md) para excluir o texto e cadeias de caracteres de texto de sendo analisado; Esses filtros também irá ignorar o texto quando você executar a análise de relevância 
    
- [Exiba os resultados](view-analyze-results-in-advanced-ediscovery.md) do processo de análise 
    
- [Configurar configurações avançada](set-analyze-advanced-settings-in-advanced-ediscovery.md) para o processo de análise 
    
### <a name="set-up-relevance-training"></a>Configurar o treinamento de relevância

Previsão de codificação (chamada relevância) no Advanced eDiscovery permite treinar o sistema no qual você está procurando, permitindo que você para tomar decisões (sobre se algo é relevante ou não) em um conjunto pequeno de documentos.
  
- [Saiba mais sobre como configurar o treinamento de relevância](manage-relevance-setup-in-advanced-ediscovery.md) , os arquivos que são relevantes para um caso de marcação e definir o caso de problemas 
    
- [Definir caso de problemas](define-issues-and-assign-users.md) e atribua cada questão a um usuário que será treinar os arquivos 
    
- [Adicionar arquivos importados a carga atual ou nova](set-up-loads-to-add-imported-files.md) que será adicionado ao treinamento a relevância; uma carga é um novo lote de arquivos que são adicionados a um caso e, em seguida, usado para treinamento de relevância 
    
- [Definir realçado palavras-chave](define-highlighted-keywords-and-advanced-options.md) que podem ser adicionados ao treinamento que a relevância; Isso ajuda a identificar melhor os arquivos que são relevantes para um caso 
    
### <a name="run-the-relevance-module"></a>Execute o módulo de relevância

Após configurar o treinamento, você está pronto para executar o módulo de relevância e avaliar a eficácia das definições de treinamento, isso resulta em uma classificação de relevância que ajuda você a decide se você precisar executar treinamento adicional ou se você estiver pronto para iniciar a marcação de arquivos como relevantes ao seu caso.
  
- [Saiba mais sobre o processo de relevância](use-relevance-in-advanced-ediscovery.md) e o processo repetitivo de avaliação, marcação, acompanhamento e treinamento novamente com base no conjunto de amostra de arquivos 
    
- [Saiba mais sobre a avaliação](assessment-in-relevance-in-advanced-ediscovery.md) , onde um especialista familiarizado com o caso analisa um conjunto de arquivos de maiusculas e determina a eficácia do treinamento relevância 
    
- [Arquivos de maiusculas Assess](tagging-and-assessment-in-advanced-ediscovery.md) para calcular a eficácia (chamada *riqueza* ) de configurações de treinamento e, em seguida, os arquivos de marca como relevantes ou não relevantes ao seu caso; Isso ajuda a determinar se o treinamento atual é suficiente ou se você deve ajustar as configurações de treinamento. 
    
- [Executar o treinamento de relevância](tagging-and-relevance-training-in-advanced-ediscovery.md) após a conclusão de avaliação e, em seguida, novamente arquivos como relevantes ou não relevantes para os problemas que você definiu para o caso de marca 
    
- Processo de [acompanhar a análise de relevância](track-relevance-analysis-in-advanced-ediscovery.md) para determinar se o treinamento de relevância atingiu seu destino assessment (conhecido como um *status de treinamento estável* ) ou se é necessário treinamento mais; Você também pode exibir os resultados de relevância para cada questão de maiusculas 
    
- [Tomar decisões com base na análise de relevância](decision-based-on-the-results-in-advanced-ediscovery.md) para determinar que o tamanho do conjunto resultante de caso de arquivos que podem ser exportadas para revisão 
    
- [A qualidade da análise da relevância de teste](test-relevance-analysis-in-advanced-ediscovery.md) para validar as decisões de remoção feitas durante o processo de relevância 
    
### <a name="export-results"></a>Exportar resultados

Analisando dados de maiusculas no eDiscovery avançado a etapa final é exportar os resultados da análise para revisão externa.
  
- [Saiba mais sobre como exportar dados maiusculas](export-case-data-in-advanced-ediscovery.md)
    
- [Exportar dados de maiusculas](export-results-in-advanced-ediscovery.md)
    
- [Exibir o histórico de lote e exportar resultados passado](view-batch-history-and-export-past-results.md)
    
- [Campos de exportação de relatório](export-report-fields-in-advanced-ediscovery.md)
    
### <a name="other-advanced-ediscovery-tools"></a>Outras ferramentas avançadas de eDiscovery

EDiscovery avançado fornece ferramentas adicionais e recursos para além analisando dados maiusculas, análise de relevância e a exportação de dados.
  
- [Executar relatórios de descoberta eletrônica avançada](run-reports-in-advanced-ediscovery.md)
    
- [Definir configurações de maiusculas/minúsculas e locatário](define-case-and-tenant-settings-in-advanced-ediscovery.md)
    
- [Utilitários de descoberta eletrônica avançada](use-advanced-ediscovery-utilities.md)
