---
title: Procurar conteúdo no Office 365
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 4/4/2018
ms.audience: Admin
ms.topic: hub-page
ms.service: o365-administration
localization_priority: Normal
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: df2d1e0f-b476-42c9-aade-4a260b24f193
description: Use a ferramenta de descoberta eletrônica de pesquisa de conteúdo no Office 365 Security &amp; Centro de conformidade para localizar rapidamente email nas caixas de correio do Exchange, documentos em sites do SharePoint e locais de OneDrive e conversas em Skype para negócios de mensagens instantâneas.
ms.openlocfilehash: d7ccdd8e501e38b67cc00ec457622080d6c58001
ms.sourcegitcommit: 7956955cd919f6e00b64e4506605a743c5872549
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/26/2018
ms.locfileid: "25038224"
---
# <a name="search-for-content-in-office-365"></a>Procurar conteúdo no Office 365

Use a ferramenta de pesquisa de conteúdo na segurança &amp; Centro de conformidade para localizar rapidamente email nas caixas de correio do Exchange, documentos em sites do SharePoint e locais de OneDrive e conversas em Skype para negócios de mensagens instantâneas. Você pode usar a ferramenta de pesquisa de conteúdo para pesquisar por email, documentos e nas ferramentas de colaboração do Office 365, como Microsoft Teams e grupos do Office 365 as conversas de mensagens instantâneas.
  
## <a name="search-for-content"></a>Procurar conteúdo

A primeira etapa é iniciar usando a ferramenta de pesquisa de conteúdo para escolher locais de conteúdo para pesquisar e configurar uma consulta de palavra-chave para procurar itens específicos. Ou então, basta deixar a consulta em branco e retornar todos os itens em locais de destino.
  
- [Criar e executar](content-search.md) uma pesquisa de conteúdo 
    
- [Consultas de pesquisa e usar as condições de compilação](keyword-queries-and-search-conditions.md) para restringir a pesquisa 
    
- [Configurar permissões de pesquisa de filtragem](permissions-filtering-for-content-search.md) para que um gerente de descoberta eletrônica somente pode pesquisar o subconjunto de caixas de correio ou sites em sua organização 
    
- [Executar uma pesquisa de ID de lista](csv-file-for-an-id-list-content-search.md) para pesquisar mensagens de email específicos 
    
- [Caixas de correio baseadas em nuvem do pesquisa](search-cloud-based-mailboxes-for-on-premises-users.md) para usuários locais no Office 365

- [Exibir estatísticas de palavra-chave](view-keyword-statistics-for-content-search.md) para os resultados de uma pesquisa e, em seguida, refinar a consulta, se necessário 
    
- [Pesquisa de dados de terceiros](use-content-search-to-search-third-party-data-that-was-imported.md) que sua organização tem importadas para o Office 365 
    
- [Editar em massa](bulk-edit-content-searches.md) a consulta e locais de conteúdo para várias pesquisas 
    
## <a name="perform-actions-on-content-you-find"></a>Executar ações no conteúdo que você acha

Depois de executar uma pesquisa e refiná-lo conforme necessário, a próxima etapa é fazer algo com os resultados retornados pela pesquisa. Você pode exportar e baixe os resultados ao computador local ou no caso de um ataque de email em sua organização, você pode excluir os resultados de uma pesquisa de caixas de correio do usuário.
  
- [Exportar os resultados de uma pesquisa de conteúdo](export-search-results.md) e fazer o download deles para seu computador local 
    
- [Procurar e excluir mensagens de email](search-for-and-delete-messages-in-your-organization.md) , como mensagens que o conteúdo de um vírus, anexo perigoso ou mensagens de phishing 
    
- [Exportar um relatório](export-a-content-search-report.md) sobre os resultados de uma pesquisa de conteúdo, sem exportar os resultados reais 
    
- [Aumentar a velocidade de download](increase-download-speeds-when-exporting-ediscovery-results.md) quando você exporta os resultados da pesquisa 
    
## <a name="learn-more-about-content-search"></a>Saiba mais sobre a pesquisa de conteúdo

Pesquisa de conteúdo é fácil de usar, mas também é uma ferramenta poderosa. Dos bastidores, há muito em andamento. Quanto mais você souber sobre ele e entender seu comportamento e suas limitações, mais bem-sucedida você usará para necessidades de pesquisa e a investigação da sua organização. Saiba mais sobre:
  
- [Parcialmente indexados itens no Exchange e SharePoint](partially-indexed-items-in-content-search.md) e como incluir ou exclui-los ao exportar e baixe os resultados de pesquisa 
    
- [Investigar itens indexados parcialmente](investigating-partially-indexed-items-in-ediscovery.md) e determinar a exposição da sua organização para acessá-los 
    
- [Limites da ferramenta de pesquisa de conteúdo](limits-for-content-search.md), como o número máximo de pesquisas que podem ser executados ao mesmo tempo e o número máximo de locais de conteúdo, que você pode incluir em uma única pesquisa 
    
- [Resultados de pesquisa real e estimada](differences-between-estimated-and-actual-ediscovery-search-results.md) e os motivos por que pode haver diferenças entre elas quando você exporta e baixe os resultados da pesquisa 
    
- [Eliminação da duplicação nos resultados da pesquisa](de-duplication-in-ediscovery-search-results.md) que você pode habilitar ao exportar mensagens de email que são os resultados de uma pesquisa 
    
## <a name="use-scripts-for-advanced-scenarios"></a>Usar scripts para cenários avançados

Em alguns casos, você precisa executar tarefas de pesquisa de conteúdo mais avançado, complexo e repetitivas. Nesses casos, é mais fácil e rápido para usar os comandos do PowerShell a segurança &amp; Centro de conformidade. Para ajudar a facilitar isso, criamos um número de segurança &amp; scripts do PowerShell do Centro de conformidade para ajudá-lo a concluir tarefas relacionados à pesquisa de conteúdo complexas.
  
- [Caixa de correio específica de pesquisa e pastas de site](use-content-search-for-targeted-collections.md) (chamado um *destinadas a coleção* ) quando estiver confiante de que os itens responsivos a um caso estão localizados nessa pasta 
    
- [Pesquisar a caixa de correio e a localização do OneDrive](search-the-mailbox-and-onedrive-for-business-for-a-list-of-users.md) para obter uma lista de usuários 
    
- [Criar, relatar e excluir várias pesquisas](create-report-on-and-delete-multiple-content-searches.md) para identificar e analisar dados de pesquisa rápida e eficiente 
    
- [Como clonar uma pesquisa de conteúdo](clone-a-content-search.md) e comparar rapidamente os resultados de consultas de pesquisa de palavra-chave diferentes executados na mesmos locais conteúdos; ou use o script para economizar tempo sem a necessidade de reinserir um grande número de locais de conteúdo quando você cria uma nova pesquisa 
    

