---
title: Desduplicação nos resultados da pesquisa de descoberta eletrônica
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 12/21/2016
ms.audience: Admin
ms.topic: overview
ms.service: o365-administration
localization_priority: Normal
ms.collection: Strat_O365_IP
search.appverid: MOE150
ms.assetid: 5af334b6-a15d-4f73-97f8-1423457d9f6b
description: Você tem a opção para eliminar a duplicação de resultados de pesquisa de descoberta eletrônica que são exportados para que apenas uma cópia de uma mensagem de email será exportada, mesmo que várias instâncias da mesma mensagem podem ter sido encontradas em caixas de correio diferentes.
ms.openlocfilehash: 5e54f0e5841fdbd29d1ab8b6b9509ff06e827920
ms.sourcegitcommit: 7956955cd919f6e00b64e4506605a743c5872549
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/26/2018
ms.locfileid: "25038004"
---
# <a name="de-duplication-in-ediscovery-search-results"></a>Desduplicação nos resultados da pesquisa de descoberta eletrônica

Este artigo descreve como a eliminação da duplicação dos resultados da pesquisa de descoberta eletrônica funciona e explica as limitações do algoritmo desduplicação.
  
Ao usar ferramentas de descoberta eletrônica do Office 365 para exportar os resultados de uma pesquisa de descoberta eletrônica, você tem a opção de eliminação da duplicação os resultados são exportados. O que isso significa? Quando você habilita a eliminação da duplicação (por padrão, a eliminação da duplicação não estiver habilitada), apenas uma cópia de uma mensagem de email será exportada, mesmo que várias instâncias da mesma mensagem podem ter sido encontradas nas caixas de correio que foram pesquisadas. Eliminação da duplicação ajuda você a economizar tempo, reduzindo o número de itens que você deve revisar e analisar depois que os resultados da pesquisa serão exportados. Mas, é importante compreender como funciona a eliminação da duplicação e lembre-se de que há limitações para o algoritmo que podem causar um item exclusivo a ser marcado como uma duplicata durante o processo de exportação.
  
## <a name="how-duplicate-messages-are-identified"></a>Como mensagens duplicadas são identificadas

Ferramentas do Office 365 eDiscovery usam uma combinação das propriedades de email a seguir para determinar se uma mensagem é uma duplicata:
  
- **InternetMessageId** - essa propriedade especifica o identificador de mensagem de Internet de uma mensagem de email, que é um identificador globalmente exclusivo que se refere a uma versão específica de uma mensagem específica. Este ID é gerada pelo sistema de email de host que envia a mensagem ou o programa de cliente de email do remetente. Se uma pessoa envia uma mensagem para mais de um destinatário, a ID da mensagem de Internet será o mesmo para cada instância da mensagem. Revisões subsequentes na mensagem original receberá um identificador de mensagem diferente. 
    
- **ConversationTopic** - sua propriedade especifica o assunto do segmento de conversação de uma mensagem. O valor da propriedade **ConversationTopic** é a cadeia de caracteres que descreve o tópico geral da conversa. Uma conservação consiste em uma mensagem inicial e todas as mensagens enviadas em resposta à mensagem inicial. Mensagens dentro da mesma conversa têm o mesmo valor da propriedade **ConversationTopic** . O valor dessa propriedade normalmente é a linha de assunto da mensagem inicial que gerado a conversa. 
    
- **BodyTagInfo** - esta é uma propriedade interna de repositório do Exchange. O valor dessa propriedade é calculado, verificando vários atributos no corpo da mensagem. Essa propriedade é usada para identificar as diferenças no corpo das mensagens. 
    
Durante o processo de exportação de descoberta eletrônica, essas três propriedades são comparadas para todas as mensagens que correspondam aos critérios de pesquisa. Se essas propriedades são idênticas para mensagens de duas (ou mais), essas mensagens sejam determinadas como duplicatas e o resultado é que apenas uma cópia da mensagem será exportada se desduplicação estiver habilitada. A mensagem que será exportada é conhecida como o item de origem"". Informações sobre mensagens duplicadas são incluídas nos relatórios **Results.csv** e **manifest** incluídos com os resultados da pesquisa exportado. No arquivo **Results.csv** , uma mensagem duplicada é identificada por ter um valor na coluna **duplicados ao Item** . O valor nessa coluna corresponde ao valor na coluna **Identidade do Item** para a mensagem que foi exportada. 
  
Os gráficos a seguir mostram como duplicadas mensagens são exibidas nos relatórios **Results.csv** e **manifest** que são exportados com os resultados da pesquisa. Esses relatórios não incluem as propriedades de email descritas anteriormente, que são usadas no algoritmo de eliminação da duplicação. Em vez disso, os relatórios incluem a propriedade de **Identidade do Item** que é atribuída aos itens do armazenamento do Exchange. 
  
 ### <a name="resultscsv-report-viewed-in-excel"></a>Relatório Results.csv (exibido no Excel)
  
![Exibindo informações sobre itens duplicados no relatório Results.csv](media/e3d64004-3b91-4cba-b6f3-934b46cbdcdb.png)
  
 ### <a name="manifestxml-report-viewed-in-excel"></a>Relatório de manifest (exibido no Excel)
  
![Exibindo informações sobre itens duplicados no relatório manifest](media/69aa4786-9883-46ff-bcae-b35e0daf4a6d.png)
  
Além disso, outras propriedades de mensagens duplicadas são incluídas nos relatórios de exportação. Isso inclui a caixa de correio que a mensagem duplicada está localizada, se a mensagem foi enviada a um grupo de distribuição e se a mensagem foi seria Cc ou Cco distr para outro usuário.
  
## <a name="limitations-of-the-de-duplication-algorithm"></a>Limitações do algoritmo desduplicação

Há algumas limitações conhecidas do algoritmo eliminação da duplicação que podem causar itens exclusivos obter marcado como duplicatas. É importante entender estas limitações para decidir se deseja ou não usar o recurso desduplicação opcional.
  
Há uma situação em que o recurso de eliminação da duplicação pode identificar por engano uma mensagem como uma duplicata e não exportá-lo (mas ainda citação-lo como uma duplicata nos relatórios de exportação). Essas são mensagens que um usuário edita, mas não envia. Por exemplo, digamos que um usuário seleciona uma mensagem no Outlook, copia o conteúdo da mensagem e, em seguida, cola-o em uma nova mensagem. Em seguida, o usuário altera uma das cópias, removendo ou adicionando um anexo ou alterando a linha de assunto ou corpo em si. Se essas duas mensagens correspondem à consulta de uma pesquisa de descoberta eletrônica, apenas um das mensagens será exportado se desduplicação será habilitada quando os resultados da pesquisa serão exportados. Portanto, mesmo que a mensagem original ou a mensagem copiada foi alterada, nenhuma das mensagens revisadas foram enviadas e, portanto, os valores das propriedades **InternetMessageId**, **ConversationTopic** e **BodyTagInfo** não foram atualizados. Mas conforme explicado anteriormente, ambas as mensagens serão listadas nos relatórios de exportação 
  
Observe que exclusivos de mensagens também podem ser marcados como duplicatas quando o recurso de proteção de página de cópia-na-gravação estiver habilitado, como no caso de uma caixa de correio sendo em litígio ou bloqueio In-loco. O recurso de cópia-na-gravação copia a mensagem original (e o salva na pasta versões da pasta de itens recuperáveis do usuário) antes que a revisão do item original seja salvo. Nesse caso, a cópia revisada e a mensagem original (na pasta itens recuperáveis) podem ser considerados como mensagens duplicadas e, portanto, apenas uma delas seria ser exportada.
  
> [!IMPORTANT]
> Se as limitações do algoritmo desduplicação podem afetar a qualidade dos resultados da pesquisa, você não deve habilitar a eliminação da duplicação ao exportar itens. Se as situações descritas nesta seção são improvável de ser um fator os resultados da pesquisa, e você deseja reduzir o número de itens mais prováveis de ser duplicatas, você deve considerar habilitando a eliminação da duplicação. 
  
## <a name="more-information"></a>Mais informações

- As informações neste artigo se aplicam ao exportar os resultados de pesquisa usando uma das seguintes ferramentas de descoberta eletrônica:
    
  - Pesquisa de conteúdo no Office 365 Security &amp; Centro de conformidade
    
  - Descoberta Eletrônica In-loco no Exchange Online
    
  - A Central de Descoberta Eletrônica no SharePoint Online
    
- Para obter mais informações sobre como exportar os resultados da pesquisa, consulte:
    
  - [Exportar resultados da pesquisa da segurança do Office 365 &amp; Centro de conformidade](export-search-results.md)
    
  - [Exportar um relatório de pesquisa de conteúdo da segurança do Office 365 &amp; Centro de conformidade](export-a-content-search-report.md)
    
  - [Exportar In-loco resultados de pesquisa de descoberta eletrônica para um arquivo PST](https://go.microsoft.com/fwlink/p/?linkid=832671)
    
  - [Exportar conteúdo e criar relatórios no Centro de Descoberta eletrônica](https://support.office.com/article/7b2ea190-5f9b-4876-86e5-4440354c381a)
