---
title: Pesquisar conteúdo no Office 365
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 4/4/2018
ms.audience: Admin
ms.topic: hub-page
ms.service: O365-seccomp
localization_priority: Normal
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: df2d1e0f-b476-42c9-aade-4a260b24f193
description: Use a ferramenta descoberta eletrônica de pesquisa de conteúdo no centro de conformidade do & de segurança para localizar rapidamente emails em caixas de correio do Exchange, documentos em sites do SharePoint e locais do OneDrive e conversas de mensagens instantâneas no Skype for Business.
ms.openlocfilehash: fc0bea90ce9cbfc27f894985c7d3083756ab108a
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32261349"
---
# <a name="search-for-content-in-office-365"></a>Pesquisar conteúdo no Office 365

Use a ferramenta de pesquisa de conteúdo no centro de conformidade do & de segurança para localizar rapidamente emails em caixas de correio do Exchange, documentos em sites do SharePoint e do OneDrive e conversas de mensagens instantâneas no Skype for Business. Você pode usar a ferramenta de pesquisa de conteúdo para pesquisar emails, documentos e conversas de mensagens instantâneas em ferramentas de colaboração do Office 365, como Microsoft Teams e grupos do Office 365.
  
## <a name="search-for-content"></a>Procurar conteúdo

A primeira etapa é começar a usar a ferramenta de pesquisa de conteúdo para escolher os locais de conteúdo para pesquisar e configurar uma consulta de palavra-chave para procurar itens específicos. Ou você pode simplesmente deixar a consulta em branco e retornar todos os itens nos locais de destino.
  
- [Criar e executar](content-search.md) uma pesquisa de conteúdo 
    
- [Criar consultas de pesquisa e usar condições](keyword-queries-and-search-conditions.md) para restringir a pesquisa 
    
- [Configurar a filtragem de permissões de pesquisa](permissions-filtering-for-content-search.md) para que um gerente de descoberta eletrônica possa Pesquisar apenas o subconjunto de sites ou caixas de correio em sua organização 
    
- [Executar uma pesquisa de lista de ID](csv-file-for-an-id-list-content-search.md) para pesquisar mensagens de email específicas 
    
- [Pesquisar caixas de correio baseadas em nuvem](search-cloud-based-mailboxes-for-on-premises-users.md) para usuários locais no Office 365

- [Exibir estatísticas de palavras-chave](view-keyword-statistics-for-content-search.md) para os resultados de uma pesquisa e depois refinar a consulta, se necessário 
    
- [Pesquisar dados de terceiros](use-content-search-to-search-third-party-data-that-was-imported.md) que sua organização tenha importado para o Office 365 
    
- [Editar em massa](bulk-edit-content-searches.md) os locais de consulta e conteúdo para várias pesquisas 
    
- [Preservar destinatários Cco](https://docs.microsoft.com/exchange/policy-and-compliance/holds/preserve-bcc-recipients-and-group-members) para que você possa procurá-los 

## <a name="perform-actions-on-content-you-find"></a>Executar ações no conteúdo que você encontrar

Após executar uma pesquisa e refiná-la conforme necessário, a próxima etapa é fazer algo com os resultados retornados pela pesquisa. Você pode exportar e baixar os resultados para o seu computador local ou no caso de um ataque de email em sua organização, você pode excluir os resultados de uma pesquisa de caixas de correio do usuário.
  
- [Exportar os resultados de uma pesquisa de conteúdo](export-search-results.md) e baixá-los no computador local 
    
- [Procurar e excluir mensagens de email](search-for-and-delete-messages-in-your-organization.md) , como mensagens que contenham um vírus, um anexo perigoso ou mensagens de phishing 
    
- [Exportar um relatório](export-a-content-search-report.md) sobre os resultados de uma pesquisa de conteúdo, sem exportar os resultados reais 
    
- [Aumentar a velocidade de download](increase-download-speeds-when-exporting-ediscovery-results.md) ao exportar os resultados da pesquisa 
    
## <a name="learn-more-about-content-search"></a>Saiba mais sobre a pesquisa de conteúdo

A pesquisa de conteúdo é fácil de usar, mas também é uma poderosa ferramenta. Por trás das cenas, há muito em andamento. Quanto mais você souber sobre ele e entender seu comportamento e suas limitações, mais bem-sucedida você o usará para as necessidades de pesquisa e investigação da sua organização. Saiba mais:
  
- [Itens parcialmente indexados no Exchange e no SharePoint](partially-indexed-items-in-content-search.md) e como incluí-los ou excluí-los ao exportar e baixar os resultados da pesquisa 
    
- [Investigar itens parcialmente indexados](investigating-partially-indexed-items-in-ediscovery.md) e determinar a exposição da sua organização a eles 
    
- Os [limites da ferramenta de pesquisa de conteúdo](limits-for-content-search.md), como o número máximo de pesquisas que podem ser executadas ao mesmo tempo e o número máximo de locais de conteúdo que podem ser incluídos em uma única pesquisa 
    
- [Resultados de pesquisa estimados e reais](differences-between-estimated-and-actual-ediscovery-search-results.md) e os motivos pelos quais pode haver diferenças entre eles ao exportar e baixar os resultados da pesquisa 
    
- [Desduplicação nos resultados de pesquisa](de-duplication-in-ediscovery-search-results.md) que você pode habilitar ao exportar mensagens de email que são os resultados de uma pesquisa 
    
## <a name="use-scripts-for-advanced-scenarios"></a>Usar scripts para cenários avançados

Às vezes, você precisa executar tarefas de pesquisa de conteúdo mais avançadas, complexas e repetitivas. Nesses casos, é mais fácil e rápido usar os comandos do PowerShell no centro de conformidade do & de segurança. Para ajudar a tornar isso mais fácil, criamos vários scripts do PowerShell do centro de conformidade do & de segurança para ajudá-lo a concluir tarefas relacionadas à pesquisa de conteúdo complexo.
  
- [Pesquisar caixa de correio e pastas de site específicas](use-content-search-for-targeted-collections.md) (chamado de *conjunto direcionado* ) quando você tiver certeza de que os itens que respondem a um caso estão localizados nessa pasta 
    
- [Pesquisar a caixa de correio e o local do onedrive](search-the-mailbox-and-onedrive-for-business-for-a-list-of-users.md) para obter uma lista de usuários 
    
- [Criar, relatar e excluir várias pesquisas](create-report-on-and-delete-multiple-content-searches.md) para identificar e analisar de forma rápida e eficiente os dados de pesquisa 
    
- [Clonar uma pesquisa de conteúdo](clone-a-content-search.md) e comparar rapidamente os resultados das diferentes consultas de pesquisa de palavras-chave executadas nos mesmos locais de conteúdo; ou use o script para economizar tempo não precisa reinserir um grande número de locais de conteúdo ao criar uma nova pesquisa 
    

