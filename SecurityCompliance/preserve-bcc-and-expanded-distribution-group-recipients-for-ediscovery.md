---
title: Preservar destinatários Cco e de grupos de distribuição expandidos para descoberta eletrônica
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 6/19/2017
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
ms.assetid: eb8ddf15-0080-457e-9d83-e73e193da334
description: Políticas de retenção do Office 365, litígio e bloqueio in-loco permitem que você preserve conteúdo de caixa de correio para atender aos requisitos de descoberta eletrônica e de conformidade a normas.
ms.openlocfilehash: 1149834181bca527bd06cea846f455e36fad283c
ms.sourcegitcommit: 7956955cd919f6e00b64e4506605a743c5872549
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/26/2018
ms.locfileid: "25038154"
---
# <a name="preserve-bcc-and-expanded-distribution-group-recipients-for-ediscovery"></a>Preservar destinatários Cco e de grupos de distribuição expandidos para descoberta eletrônica
  
Bloqueio in-loco, retenção de litígio e [políticas de retenção do Office 365](http://go.microsoft.com/fwlink/?LinkID=827811) (criados no Office 365 Security &amp; Centro de conformidade) permitem que você preserve conteúdo de caixa de correio para atender aos requisitos normativos de conformidade e eDiscovery. Informações sobre destinatários endereçada diretamente em para e Cc campos de uma mensagem é incluída em todas as mensagens por padrão, mas sua organização pode exigir a capacidade de pesquisar e reproduza detalhes sobre todos os destinatários de uma mensagem. Isso inclui: 
  
- **Destinatários endereçados utilizando o campo Cco de uma mensagem** Destinatários Cco são armazenados na mensagem na caixa de correio do remetente, mas não são incluídos em cabeçalhos da mensagem entregue aos destinatários. 
    
- **Destinatários do grupo de distribuição expandido** Destinatários que a mensagem porque eles são membros de um grupo de distribuição para o qual a mensagem foi tratada, tanto em para, Cc ou Cco campos. 
    
Exchange Online e Exchange Server 2013 (atualização cumulativa 7 e versões posteriores) mantêm informações sobre Cco e os destinatários do grupo de distribuição expandido. Você pode procurar essas informações usando uma pesquisa de descoberta eletrônica In-loco no Centro de administração do Exchange (EAC) ou uma pesquisa de conteúdo na segurança &amp; Centro de conformidade. 
  
## <a name="how-bcc-recipients-and-expanded-distribution-group-recipients-are-preserved"></a>Como destinatários Cco e os destinatários do grupo de distribuição expandido são preservados
<a name="sectionSection0"> </a>

Conforme mencionado anteriormente, as informações sobre destinatários Bcc'ed serão armazenadas com a mensagem na caixa de correio do remetente. Essa informação é indexada e disponíveis para pesquisas de descoberta eletrônica e retenções. 
  
Informações sobre os destinatários do grupo de distribuição expandido são armazenadas com a mensagem após colocar uma caixa de correio em bloqueio In-loco ou retenção de litígio. No Office 365, essas informações também são armazenadas quando uma política de retenção do Office 365 é aplicada a uma caixa de correio. A associação ao grupo de distribuição é determinada no momento em que a mensagem é enviada. A lista de destinatários expandida armazenada com a mensagem não é afetada pelas alterações à associação do grupo, depois que a mensagem é enviada. 
  
|**Informações sobre...**|**É armazenado no …**|**São armazenadas por padrão?**|**É acessível aos …**|
|:-----|:-----|:-----|:-----|
|Para e Cc destinatários  <br/> |Propriedades de mensagem no remetente e caixas de correio dos destinatários.  <br/> |Sim  <br/> |Oficiais de conformidade de remetente e destinatários  <br/> |
|Destinatários Cco  <br/> |Propriedade de mensagem na caixa de correio do remetente.  <br/> |Sim  <br/> |Oficiais de conformidade e de remetente  <br/> |
|Destinatários do grupo de distribuição expandido  <br/> |Propriedades da mensagem na caixa de correio do remetente.  <br/> |Não. Informações do grupo de distribuição expandido destinatário são armazenadas após uma caixa de correio for colocada em retenção In-loco ou retenção de litígio ou atribuídas a uma política de retenção do Office 365.  <br/> |Oficiais de conformidade  <br/> |
   
## <a name="searching-for-messages-sent-to-bcc-and-expanded-distribution-group-recipients"></a>Procurando por mensagens enviadas para Cco e os destinatários do grupo de distribuição expandido
<a name="sectionSection1"> </a>

Ao procurar por mensagens enviadas para um destinatário, os resultados da pesquisa de descoberta eletrônica agora incluem mensagens enviadas a um grupo de distribuição que o destinatário é um membro de. A tabela a seguir mostra os cenários em que as mensagens enviadas para Cco e os destinatários do grupo de distribuição expandido são retornadas em pesquisas de descoberta eletrônica.
  
Cenário 1: John é um membro do grupo de distribuição de vendas dos EUA. Esta tabela mostra os resultados da pesquisa de descoberta eletrônica quando Bob envia uma mensagem para John direta ou indiretamente por meio de um grupo de distribuição.
  
|**Quando você pesquisa de caixa de correio de Bob para mensagens enviadas …**|**E a mensagem é enviada com …**|**Os resultados incluem mensagem?**|
|:-----|:-----|:-----|
|Como: John  <br/> |John logon em  <br/> |Sim  <br/> |
|Como: John  <br/> |US-Sales logon em  <br/> |Sim  <br/> |
|Como: vendas dos EUA  <br/> |US-Sales logon em  <br/> |Sim  <br/> |
|Cc:John  <br/> |John em CC  <br/> |Sim  <br/> |
|Cc:John  <br/> |US-vendas em CC  <br/> |Sim  <br/> |
|Cc:US-vendas  <br/> |US-vendas em CC  <br/> |Sim  <br/> |
   
Cenário 2: Bob envia um email para John (para / Cc) e a tomada (diretamente, Cco ou indiretamente por meio de um grupo de distribuição). A tabela a seguir mostra os resultados da pesquisa de descoberta eletrônica.
  
|**Quando você pesquisa …**|**Para mensagens enviadas …**|**Os resultados incluem mensagem?**|**Observações**|
|:-----|:-----|:-----|:-----|
|Caixa de correio de Bob  <br/> |Para / Cc:John  <br/> |Sim  <br/> |Apresenta uma indicação de que o conector foi Bcc'ed.  <br/> |
|Caixa de correio de Bob  <br/> |BCC:Jack  <br/> |Sim  <br/> |Apresenta uma indicação de que o conector foi Bcc'ed.  <br/> |
|Caixa de correio de Bob  <br/> |BCC:Jack (por meio do grupo de distribuição)  <br/> |Sim  <br/> |Lista de membros do grupo de distribuição Bcc'ed expandidos quando a mensagem foi enviada, é visível em logs, a exportação e a visualização da pesquisa de descoberta eletrônica.  <br/> |
|Caixa de correio de John  <br/> |Para / Cc:John  <br/> |Sim  <br/> |Nenhuma indicação de destinatários Cco.  <br/> |
|Caixa de correio de John  <br/> |BCC:Jack (diretamente ou por meio da distribuição de grupo)  <br/> |Não  <br/> |Informações de Cco não são armazenadas na mensagem entregue aos destinatários. Você deve pesquisar a caixa de correio do remetente.  <br/> |
|Caixa de correio de tomada.  <br/> |Para / Cc:John (diretamente ou por meio da distribuição de grupo)  <br/> |Sim  <br/> |Para / Cc informações são incluídas na mensagem entregue a todos os destinatários.  <br/> |
|Caixa de correio de tomada.  <br/> |BCC:Jack (diretamente ou por meio da distribuição de grupo)  <br/> |Não  <br/> |Informações de Cco não são armazenadas na mensagem entregue aos destinatários. Você deve pesquisar a caixa de correio do remetente.  <br/> |
   
## <a name="frequently-asked-questions"></a>Perguntas frequentes
<a name="sectionSection2"> </a>

 **P. quando e onde são armazenadas as informações de destinatário Cco?**
  
Informações do destinatário Cco r. são preservadas por padrão na mensagem original na caixa de correio do remetente. Se o destinatário Cco for um grupo de distribuição, a associação de grupo de distribuição somente é expandida se a caixa de correio do remetente está em retenção ou atribuída a uma política de retenção do Office 365.
  
 **P. quando e onde está a lista de distribuição expandido destinatários do grupo armazenados?**
  
R. a associação ao grupo de é expandida no momento em que a mensagem é enviada. A lista de membros do grupo de distribuição expandido é armazenada na mensagem original na caixa de correio do remetente. Caixa de correio do remetente deve estar em bloqueio In-loco, retenção de litígio, ou atribuído a uma política de retenção do Office 365.
  
 **P. pode para / destinatários Cc consulte quais destinatários foram Bcc'ed?**
  
R. n º de Essas informações não estão incluídas nos cabeçalhos de mensagem e não são visíveis para / Cc os destinatários. O remetente pode ver o campo Cco armazenado na mensagem original armazenada em suas caixas de correio. Oficiais de conformidade podem ver essa informação ao pesquisar a caixa de correio do remetente.
  
 **P. como garantir os destinatários do grupo de distribuição expandido sempre são preservados?**
  
R. para assegurar membros do grupo de distribuição expandido sempre são preservados com uma mensagem, e [colocar todas as caixas de correio em espera](http://technet.microsoft.com/library/4c141604-3210-44cc-b98e-f3e0f15613b8.aspx) ou criar uma política de retenção do Office 365 de toda a organização. 
  
 **P. quais tipos de grupos são suportados?**
  
R. há suporte para grupos de distribuição, grupos dinâmicos de distribuição e grupos de segurança habilitados para email. 
  
 **P. existe um limite no número de distribuição destinatários do grupo que são expandidos e armazenados na mensagem?**
  
A. backup para 10.000 membros de uma distribuição grupo é preservado.
  
 **P. são aninhadas grupos de distribuição suportados?**
  
R. Sim, 25 níveis de grupos de distribuição aninhados são expandidos.
  
 **P. Where são a informação destinatário de grupo de distribuição expandido visível e Cco?**
  
R. destinatários do grupo de distribuição expandido e Cco informações são visíveis para oficiais de conformidade ao executar uma pesquisa de descoberta eletrônica. Cco e os destinatários do grupo de distribuição expandido são incluídos nos resultados de pesquisa copiados para uma caixa de correio de descoberta ou exportado para um arquivo PST e no log de descoberta eletrônica incluído nos resultados da pesquisa. Informações do destinatário Cco também estão disponíveis na visualização da pesquisa.
  
 **P. o que acontece se um membro de um grupo de distribuição é oculto da lista de endereços global (GAL) da organização?**
  
R. não há nenhum impacto. Se os destinatários estiverem ocultos da GAL, eles ainda estiver incluídos na lista de destinatários para o grupo de distribuição expandido.
  

