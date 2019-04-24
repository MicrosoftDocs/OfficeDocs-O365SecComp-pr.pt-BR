---
title: Usar a pesquisa de conteúdo para pesquisar dados de terceiros que foram importados para o Office 365
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 10/27/2017
ms.audience: Admin
ms.topic: conceptual
ms.service: O365-seccomp
ms.collection: M365-security-compliance
localization_priority: Normal
search.appverid: MOE150
ms.assetid: ec2677ff-c4d7-4363-a9e7-22c80e015688
description: Use a ferramenta de descoberta eletrônica de pesquisa de conteúdo para pesquisar itens que foram importados para caixas de correio no Office 365 de uma fonte de dados de terceiros. Você pode criar uma consulta para pesquisar todos os itens importados ou criar uma consulta para Pesquisar tipos de dados específicos de terceiros. Este artigo lista os valores que podem ser usados em uma consulta de palavra-chave para pesquisar os tipos de dados de terceiros que podem ser importados para o Office 365.
ms.openlocfilehash: 361ead435d397464452c5b58ecf251a7322ced05
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32263773"
---
# <a name="use-content-search-to-search-third-party-data-that-was-imported-to-office-365"></a>Usar a pesquisa de conteúdo para pesquisar dados de terceiros que foram importados para o Office 365

Você pode usar a [ferramenta de descoberta eletrônica de pesquisa de conteúdo](content-search.md) no centro de conformidade do _AMP_ de segurança para pesquisar itens que foram importados para caixas de correio no Office 365 de uma fonte de dados de terceiros. Você pode criar uma consulta para pesquisar todos os itens importados de dados de terceiros ou pode criar uma consulta para pesquisar apenas itens de dados de terceiros específicos. Além disso, você também pode criar uma política de preservação baseada em consulta ou uma descoberta eletrônica baseada em consulta para preservar dados de terceiros no Office 365. 
  
Para obter mais informações sobre a importação de dados de terceiros e uma lista dos tipos de dados de terceiros que podem ser importados para o Office 365, consulte arquivamento de dados de terceiros [no office 365](archiving-third-party-data.md). 
  
## <a name="creating-a-query-to-search-all-third-party-data"></a>Criar uma consulta para pesquisar todos os dados de terceiros

Para pesquisar (ou colocar em espera) qualquer tipo de dados de terceiros que você importou para o Office 365, é possível usar o `kind:externaldata` par propriedade-valor da mensagem na caixa palavra-chave para uma pesquisa de conteúdo ou ao criar uma retenção baseada em consulta. Por exemplo, para pesquisar itens que foram importados de qualquer fonte de dados de terceiros e que contenham a palavra "contoso" na propriedade Subject do item importado, você usaria a seguinte consulta: 
  
```
kind:externaldata AND subject:contoso
```

O exemplo de consulta de palavra-chave anterior inclui a propriedade Subject. Para obter uma lista de outras propriedades dos itens de dados de terceiros que podem ser incluídos em uma consulta de palavra-chave, consulte a seção "mais informações" em arquivamento de [dados de terceiros no Office 365](archiving-third-party-data.md#more-information).
  
Ao criar consultas para pesquisar e manter dados de terceiros, você também pode usar condições para restringir os resultados da pesquisa. Para obter mais informações sobre a criação de consultas de pesquisa de conteúdo, consulte [keyword queries and Search Conditions for Content Search](keyword-queries-and-search-conditions.md).
  
## <a name="creating-a-query-to-search-specific-types-of-third-party-data"></a>Criar uma consulta para Pesquisar tipos específicos de dados de terceiros

Em vez de Pesquisar todos os tipos de dados de terceiros, você pode criar consultas que só pesquisem um tipo especificado de dados de terceiros usando o par de valor de propriedade de mensagem a seguir na caixa de palavra-chave de uma pesquisa de conteúdo:
  
```
itemclass:ipm.externaldata.<third-party data type>* 
```

Por exemplo, para pesquisar apenas dados do Facebook que contenham a palavra "contoso" na propriedade Subject, você deve usar a seguinte consulta:
  
```
itemclass:ipm.externaldata.Facebook* AND subject:contoso
```

A tabela a seguir lista os tipos de dados de terceiros que podem ser pesquisados e o valor a ser usado `itemclass:` para a propriedade Message para pesquisar especificamente o tipo de dados de terceiros. Observe que a sintaxe de consulta não diferencia maiúsculas de minúsculas. 
  
|**Tipo de dados de terceiros**|**Valor da `itemclass:` Propriedade**|
|:-----|:-----|
|META  <br/> | `ipm.externaldata.AIM*` <br/> |
|American Idol  <br/> | `ipm.externaldata.AmericanIdol*` <br/> |
|AOL with Pivot Client  <br/> | `ipm.externaldata.Pivot.IM` <br/> |
|Apple Juice  <br/> | `ipm.externaldata.AppleJuice*` <br/> |
|Ares  <br/> | `ipm.externaldata.Ares*` <br/> |
|Axs Encrypted  <br/> | `ipm.externaldata.AxsEncrypted*` <br/> |
|Axs Exchange  <br/> | `ipm.externaldata.AxsExchange*` <br/> |
|Axs Local Archive  <br/> | `ipm.externaldata.AxsLocalArchive*` <br/> |
|Espaço reservado do AXS  <br/> | `ipm.externaldata.AxsPlaceHolder*` <br/> |
|Axs Signed  <br/> | `ipm.externaldata.AxsSigned*` <br/> |
|Bazaarvoice  <br/> | `ipm.externaldata.Bazaarvoice*` <br/> |
|BearShare  <br/> | `ipm.externaldata.Bearshare*` <br/> |
|BitTorrent  <br/> | `ipm.externaldata.BitTorrent*` <br/> |
|Rim  <br/> | `ipm.externaldata.Blackberry*` <br/> |
|Logs de chamadas do BlackBerry  <br/> | `ipm.externaldata.BlackBerryCall*` <br/> |
|BlackBerry Messenger  <br/> | `ipm.externaldata.BlackBerryMessenger*` <br/> |
|PIN do BlackBerry  <br/> | `ipm.externaldata.BlackBerryPIN*` <br/> |
|SMS BlackBerry  <br/> | `ipm.externaldata.BlackBerrySMS*` <br/> |
|Bloomberg  <br/> | `ipm.externaldata.Bloomberg*` <br/> |
|Bloomberg Mail  <br/> | `ipm.externaldata.BloombergMail*` <br/> |
|Mensagens do Bloomberg  <br/> | `ipm.externaldata.BloombergMessaging*` <br/> |
|Caixa  <br/> | `ipm.externaldata.Box*` <br/> |
|Servidor de &amp; presença de im da Cisco  <br/> | `ipm.externaldata.Jabber.IM` <br/> |
|Cisco Jabber  <br/> | `ipm.externaldata.Jabber*` <br/> |
|CipherCloud for Salesforce Chatter  <br/> | `ipm.externaldata.Chatter.Post` <br/>  `ipm.externaldata.Chatter.Comment` <br/> |
|Conexão Direta  <br/> | `ipm.externaldata.DirectConnect*` <br/> |
|Facebook  <br/> | `ipm.externaldata.Facebook*` <br/> |
|FastTrack  <br/> | `ipm.externaldata.FastTrack*` <br/> |
|FXConnect  <br/> | `ipm.externaldata.FXConnect.chat` <br/> |
|Flickr  <br/> | `ipm.externaldata.Flickr*` <br/> |
|Gnutella  <br/> | `ipm.externaldata.Gnutella*` <br/> |
|Google +  <br/> | `ipm.externaldata.GooglePlus*` <br/> |
|Google Talk  <br/> | `ipm.externaldata.GoogleTalk*` <br/> |
|GoToMyPC  <br/> | `ipm.externaldata.GoToMyPC*` <br/> |
|HipChat  <br/> | `ipm.externaldata.HipChat*` <br/> |
|Hopster  <br/> | `ipm.externaldata.Hopster*` <br/> |
|HubConnex  <br/> | `ipm.externaldata.HubConnex*` <br/> |
|Conexões IBM  <br/> | `ipm.externaldata.Connections*` <br/> |
|IBM SameTime  <br/> | `ipm.externaldata.Sametime*` <br/> |
|Chat de gelo  <br/> | `ipm.externaldata.ICEChat.Chat` <br/> |
|Indii Messenger  <br/> | `ipm.externaldata.Indii*` <br/> |
|Instagram  <br/> | `ipm.externaldata.Instagram*` <br/> |
|Instant Bloomberg  <br/> | `ipm.externaldata.InstantBloomberg*` <br/> |
|InvestEdge  <br/> | `ipm.externaldata.InvestEdge*` <br/> |
|IRC  <br/> | `ipm.externaldata.IRC*` <br/> |
|Jive  <br/> | `ipm.externaldata.Jive*` <br/> |
|JiveApiRetention  <br/> | `ipm.externaldata.JiveApiRetention*` <br/> |
|JXTA  <br/> | `ipm.externaldata.JXTA*` <br/> |
|LinkedIn  <br/> | `ipm.externaldata.LinkedIn*` <br/> |
|MFTP  <br/> | `ipm.externaldata.MFTP*` <br/> |
|UC da Microsoft  <br/> | `ipm.externaldata.MicrosoftUC*` <br/> |
|Alinhamento de mentalidade  <br/> | `ipm.externaldata.MindAlign*` <br/> |
|Mobile Guard  <br/> | `ipm.externaldata.MobileGuard*` <br/> |
|MSN  <br/> | `ipm.externaldata.MSN*` <br/> |
|MySpace  <br/> | `ipm.externaldata.MySpace*` <br/> |
|NEONetwork  <br/> | `ipm.externaldata.NEONetwork*` <br/> |
|OpenNap  <br/> | `ipm.externaldata.OpenNap*` <br/> |
|Pinterest  <br/> | `ipm.externaldata.Pinterest*` <br/> |
|Navegação dinâmica  <br/> | `ipm.externaldata.Pivot*` <br/> |
|QQ  <br/> | `ipm.externaldata.QQ*` <br/> |
|Microsoft SharePoint  <br/> | `ipm.externaldata.SharePoint*` <br/> |
|Salesforce Chatter  <br/> | `ipm.externaldata.Chatter*` <br/> |
|Skype for Business  <br/> | `ipm.externaldata.Skype*` <br/> |
|Slack Enterprise Grid  <br/> | `ipm.externaldata.Slack.IM` <br/> |
|SoftEther  <br/> | `ipm.externaldata.SoftEther*` <br/> |
|Squawker  <br/> | `ipm.externaldata.Squawker*` <br/> |
|Symphony  <br/> | `ipm.externaldata.Symphony*` <br/> |
|Thomson Reuters  <br/> | `ipm.externaldata.Reuters*` <br/> |
| Thomson Reuters Eikon Messenger  <br/> | `ipm.externaldata.ReutersEikon*` <br/> |
|Tor  <br/> | `ipm.externaldata.Tor*` <br/> |
|TTT  <br/> | `ipm.externaldata.TTT*` <br/> |
|Twitter  <br/> | `ipm.externaldata.Twitter*` <br/> |
|UBS Chat  <br/> | `ipm.externaldata.UBS*` <br/> |
|Vimeo  <br/> | `ipm.externaldata.Vimeo*` <br/> |
|WinMX  <br/> | `ipm.externaldata.WinMX*` <br/> |
|Winny  <br/> | `ipm.externaldata.Winny*` <br/> |
|Toolbar  <br/> | `ipm.externaldata.Yahoo!*` <br/> |
|Yammer  <br/> | `ipm.externaldata.Yammer*` <br/> |
|YellowJacket  <br/> | `ipm.externaldata.YellowJacket*` <br/> |
|YouTube  <br/> | `ipm.externaldata.YouTube*` <br/> |
