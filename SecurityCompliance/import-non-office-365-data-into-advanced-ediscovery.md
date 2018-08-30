---
title: Importar conteúdo não relacionado ao Office 365 para Descoberta Eletrônica Avançada
ms.author: chrfox
author: chrfox
manager: laurawi
ms.date: 5/25/2018
ms.audience: ITPro
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- OEC150
- MET150
ms.assetid: 0ee60763-a30b-495b-8543-971c3384a801
description: Como às etapas para importar o conteúdo que não está armazenado no O365 em um Windows Azure blob para que ele pode ser analisado com AeD
ms.openlocfilehash: ab6c7ac76a159603a34719aa8edb51de3a4fabbb
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22524719"
---
# <a name="import-non-office-365-content-for-advanced-ediscovery-analysis"></a>Importar conteúdo não relacionado ao Office 365 para Descoberta Eletrônica Avançada

Nem todos os documentos que você talvez precise analisar com eDiscovery avançadas do Office 365 residirá no Office 365. Com o conteúdo não-Office 365 importe recurso no eDiscovery avançado, que você pode carregar documentos que não live no Office 365 (exceto os arquivos. PST) em um blob maiusculas armazenamento Azure vinculados e analisá-los com eDiscovery avançado. Esse procedimento mostra como trazer seus documentos do Office 365 para descoberta eletrônica avançada para análise.
  
> [!NOTE]
> EDiscovery Avançado requer um Office 365 E3 com o complemento de conformidade avançadas ou uma assinatura E5 para sua organização. Se você não tiver que plano e quiser tentar eDiscovery avançado, você pode [inscrever-se para uma avaliação do Office 365 Enterprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279). 
  
> [!NOTE]
> Você pode adquirir uma assinatura eDiscovery avançadas do Office 365 de complemento de armazenamento dados para o seu conteúdo do Office 365. Isso é exclusivamente disponível para o conteúdo que deve ser analisada com eDiscovery avançado. Siga as etapas em [comprar ou editar e Add-on do Office 365 for business](https://support.office.com/article/Buy-or-edit-an-add-on-for-Office-365-for-business-4e7b57d6-b93b-457d-aecd-0ea58bff07a6) e comprar o complemento de armazenamento de descoberta eletrônica avançadas do Office 365. 
  
## <a name="before-you-begin"></a>Antes de começar

Usando o recurso de upload Non-Office 365, conforme descrito neste procedimento requer que você tenha:
  
- Um Office 365 E3 com inscrição de E5 ou complemento de conformidade avançadas
    
- Todos os responsáveis cujo conteúdo não - Office 365 será carregado devem ter E3 com licenças de E5 ou complemento de conformidade avançadas
    
- Uma ocorrência de descoberta eletrônica existente
    
- Todos os arquivos para carregar coletadas em pastas onde houver uma pasta por dos responsáveis e nome das pastas se situa este formato *alias@domainname* . O *alias@domainname* deve ser o domínio e alias de usuário Office 365. Você pode coletar todas as pastas de *alias@domainname* em uma pasta raiz. A pasta raiz pode conter apenas as pastas *alias@domainname* , não deve haver nenhum arquivo afastado na pasta raiz 
    
- Uma conta que seja um gerente de descoberta eletrônica ou um administrador de descoberta eletrônica
    
- [Ferramentas de armazenamento do Microsoft Azure](https://aka.ms/downloadazcopy) instalado em um computador que tenha acesso na estrutura de pasta de conteúdo do Office 365. 
    
## <a name="upload-non-office-365-content-into-advanced-ediscovery"></a>Carregar o conteúdo do Office 365 em eDiscovery avançado

1. Como um gerente de descoberta eletrônica ou eDiscovery administrador, abra o **eDiscovery**e, em seguida, abra o caso em que os dados não - Office 365 serão carregados. Se você precisar criar um caso, consulte [gerenciar casos de descoberta eletrônica no Office 365 Security &amp; Centro de conformidade](manage-ediscovery-cases.md)
    
2. Clique em **Alternar para descoberta eletrônica avançada**
    
3. Em **tipo de fonte** , selecione **os dados não-Office 365**.
    
4. Clique em **Adicionar contêiner**. Nomeie o contêiner e adicionar uma descrição.
    
5. Selecione o contêiner recém-adicionado na lista do contêiner e copie a URL que aparece no painel de detalhes do contêiner e, em seguida, feche o painel
    
6. Abra um prompt de comando como administrador e altere o diretório para a pasta onde você tinha AzCopy instalado..
    
7. Construa a linha de comando AzCopy para carregar os arquivos semelhante a esta:
    
    AzCopy /Source: " *o caminho completo para a pasta raiz na máquina local* " /Dest: " *URL contêiner até, mas não incluindo o?* " /DestSAS: " *restante da url de contêiner a? até o final* "/ S. 
    
    Por exemplo, usando estes valores: 
    
  - pasta raiz - C:\Collected dados 
    
  - url de contêiner - https://zoomsabcprodeuss114.blob.core.windows.net/ingestion53d059efe5f74784afb308f66cdebf17?sv=2015-04-05&amp; sr = c&amp;si = NonOfficeData15 %7 C 0&amp;sig = % Bk5INP8CUfv1y4CSJiJl3pJt3Ekvu8GS3P8NkOvoQxA 3D
    
    a sintaxe de linha de comando AzCopy seria:
    
     `AzCopy /Source:"C:\CollectedData" /Dest:"https://zoomsabcprodeuss114.blob.core.windows.net/ingestion53d059efe5f74784afb308f66cdebf17" /DestSAS:"?sv=2015-04-05&amp;sr=c&amp;si=NonOfficeData15%7C0&amp;sig=Bk5INP8CUfv1y4CSJiJl3pJt3Ekvu8GS3P8NkOvoQxA%3D" /S`
    
    Para obter mais informações sobre Azcopy sintaxe consulte, [transferir dados com o AzCopy no Windows](https://docs.microsoft.com/azure/storage/common/storage-use-azcopy) . 
    
    > [!IMPORTANT]
    > Deve haver uma pasta de raiz por usuário e o nome da pasta deve estar no formato *alias@domainname* . 
  
8. Depois que as pastas terminar de carregar, volte para a descoberta eletrônica avançada. O conteúdo nas pastas que você carregou está pronto para ser processado no eDiscovery avançado. Selecione o contêiner e clique no botão de processo. Para obter mais detalhes sobre o eDiscovery avançado processamento ver, [execute o módulo de processo e carregar dados no eDiscovery avançadas do Office 365](run-the-process-module-and-load-data-in-advanced-ediscovery.md)
    
    > [!IMPORTANT]
    > Depois que o contêiner é processado com êxito no eDiscovery avançado, você não mais poderá adicionar novo conteúdo para o armazenamento SAS no Windows Azure. Se você coletar conteúdo adicional e deseja adicioná-lo ao caso para análise de descoberta eletrônica avançado, você deve criar um novo contêiner de **dados de não-Office 365** e repita esse procedimento. 
  
    > [!NOTE]
    > Se o contêiner *não processará com êxito devido a problemas de nomenclatura de pasta* e, em seguida, corrigir os problemas, você ainda precisará criar um novo contêiner e reconecte e carregar novamente usando os procedimentos neste artigo. 
  

