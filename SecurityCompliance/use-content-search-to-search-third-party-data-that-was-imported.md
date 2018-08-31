---
title: Use a pesquisa de conteúdo para pesquisar dados de terceiros que foi importados para o Office 365
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 10/27/2017
ms.audience: Admin
ms.topic: reference
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: ec2677ff-c4d7-4363-a9e7-22c80e015688
description: Use a ferramenta de descoberta eletrônica de pesquisa de conteúdo para procurar itens que tenham sido importados para caixas de correio no Office 365 de uma fonte de dados de terceiros. Você pode criar uma consulta para procurar todos os itens importados ou criar uma consulta para pesquisar por tipos de dados específicos de terceiros. Este artigo lista os valores que você pode usar em uma consulta de palavra-chave para pesquisar os tipos de dados de terceiros que podem ser importados para o Office 365.
ms.openlocfilehash: 90d9dc52dcd9dba9bc273dfcf1c5f22e3913d6ba
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22524303"
---
# <a name="use-content-search-to-search-third-party-data-that-was-imported-to-office-365"></a>Use a pesquisa de conteúdo para pesquisar dados de terceiros que foi importados para o Office 365

Você pode usar a [ferramenta de pesquisa de conteúdo de descoberta eletrônica](content-search.md) no Office 365 Security &amp; Centro de conformidade para procurar itens que tenham sido importados para caixas de correio no Office 365 de uma fonte de dados de terceiros. Você pode criar uma consulta para pesquisar importados todos os itens de dados de terceiros ou você pode criar uma consulta para pesquisar somente itens de dados específicos de terceiros. Além disso, você também pode criar uma política de preservação baseado em consulta ou uma descoberta eletrônica baseado em consulta espera preservar dados de terceiros no Office 365. 
  
Para obter mais informações sobre a importação de dados de terceiros e uma lista dos tipos de dados de terceiros que podem ser importados para o Office 365, consulte [arquivamento dados de terceiros no Office 365](archiving-third-party-data.md). 
  
## <a name="creating-a-query-to-search-all-third-party-data"></a>Criando uma consulta para pesquisar todos os dados de terceiros

Para pesquisar (ou colocada em espera) qualquer tipo de dados de terceiros que você importou para o Office 365, é possível que você pode usar o `kind:externaldata` par de mensagens do valor da propriedade na caixa de palavra-chave para uma pesquisa de conteúdo ou ao criar uma isenção baseado em consulta. Por exemplo, para procurar itens que tenham sido importados de qualquer fonte de dados de terceiros e contêm a palavra "contoso" na propriedade assunto do item importado, você usaria a seguinte consulta: 
  
```
kind:externaldata AND subject:contoso
```

O exemplo anterior de consulta de palavra-chave inclui a propriedade subject. Para obter uma lista das outras propriedades para itens de dados de terceiros que podem incluído em uma consulta de palavra-chave, consulte a seção "Mais informações" em [arquivamento de dados de terceiros no Office 365](archiving-third-party-data.md#more-information).
  
Ao criar consultas para pesquisar e manter os dados de terceiros, você também pode usar condições para restringir os resultados da pesquisa. Para obter mais informações sobre como criar consultas de pesquisa de conteúdo, consulte [consultas de palavra-chave e condições de pesquisa para pesquisa de conteúdo](keyword-queries-and-search-conditions.md).
  
## <a name="creating-a-query-to-search-specific-types-of-third-party-data"></a>Criando uma consulta para pesquisar tipos específicos de dados de terceiros

Em vez de pesquisar todos os tipos de dados de terceiros, você pode criar consultas de pesquisa somente para um tipo de dados de terceiros de especificar usando o seguinte par de valor de propriedade de mensagem na caixa de palavra-chave para uma pesquisa de conteúdo:
  
```
itemclass:ipm.externaldata.<third-party data type>* 
```

Por exemplo, para pesquisar somente dados de Facebook que contenham a palavra "contoso" na propriedade Subject, você usaria a seguinte consulta:
  
```
itemclass:ipm.externaldata.Facebook* AND subject:contoso
```

A tabela a seguir lista os tipos de dados de terceiros que você pode pesquisar e o valor a ser usado para o `itemclass:` propriedade especificamente pesquisar por esse tipo de dados de terceiros message. Observe que a sintaxe de consulta não diferenciam maiusculas de minúsculas. 
  
|**Tipo de dados de terceiros**|**O valor para `itemclass:` propriedade**|
|:-----|:-----|
|OBJETIVO  <br/> | `ipm.externaldata.AIM*` <br/> |
|American Idol  <br/> | `ipm.externaldata.AmericanIdol*` <br/> |
|AOL with Pivot Client  <br/> | `ipm.externaldata.Pivot.IM` <br/> |
|Apple Juice  <br/> | `ipm.externaldata.AppleJuice*` <br/> |
|Ares  <br/> | `ipm.externaldata.Ares*` <br/> |
|Axs Encrypted  <br/> | `ipm.externaldata.AxsEncrypted*` <br/> |
|Axs Exchange  <br/> | `ipm.externaldata.AxsExchange*` <br/> |
|Axs Local Archive  <br/> | `ipm.externaldata.AxsLocalArchive*` <br/> |
|Espaço reservado do AXs  <br/> | `ipm.externaldata.AxsPlaceHolder*` <br/> |
|Axs Signed  <br/> | `ipm.externaldata.AxsSigned*` <br/> |
|Bazaarvoice  <br/> | `ipm.externaldata.Bazaarvoice*` <br/> |
|Bearshare  <br/> | `ipm.externaldata.Bearshare*` <br/> |
|BitTorrent  <br/> | `ipm.externaldata.BitTorrent*` <br/> |
|BlackBerry  <br/> | `ipm.externaldata.Blackberry*` <br/> |
|Logs de chamada do blackBerry  <br/> | `ipm.externaldata.BlackBerryCall*` <br/> |
|BlackBerry Messenger  <br/> | `ipm.externaldata.BlackBerryMessenger*` <br/> |
|BlackBerry PIN  <br/> | `ipm.externaldata.BlackBerryPIN*` <br/> |
|BlackBerry SMS  <br/> | `ipm.externaldata.BlackBerrySMS*` <br/> |
|Bloomberg  <br/> | `ipm.externaldata.Bloomberg*` <br/> |
|Bloomberg Mail
  <br/> | `ipm.externaldata.BloombergMail*` <br/> |
|Mensagens Bloomberg  <br/> | `ipm.externaldata.BloombergMessaging*` <br/> |
|Box
  <br/> | `ipm.externaldata.Box*` <br/> |
|Cisco IM &amp; servidor de presença  <br/> | `ipm.externaldata.Jabber.IM` <br/> |
|Cisco Jabber  <br/> | `ipm.externaldata.Jabber*` <br/> |
|CipherCloud for Salesforce Chatter  <br/> | `ipm.externaldata.Chatter.Post` <br/>  `ipm.externaldata.Chatter.Comment` <br/> |
|Conexão Direta  <br/> | `ipm.externaldata.DirectConnect*` <br/> |
|Facebook  <br/> | `ipm.externaldata.Facebook*` <br/> |
|FastTrack  <br/> | `ipm.externaldata.FastTrack*` <br/> |
|FXConnect  <br/> | `ipm.externaldata.FXConnect.chat` <br/> |
|Flickr
  <br/> | `ipm.externaldata.Flickr*` <br/> |
|Gnutella  <br/> | `ipm.externaldata.Gnutella*` <br/> |
|Google+
  <br/> | `ipm.externaldata.GooglePlus*` <br/> |
|Google Talk  <br/> | `ipm.externaldata.GoogleTalk*` <br/> |
|GoToMyPC  <br/> | `ipm.externaldata.GoToMyPC*` <br/> |
|HipChat  <br/> | `ipm.externaldata.HipChat*` <br/> |
|Hopster  <br/> | `ipm.externaldata.Hopster*` <br/> |
|HubConnex  <br/> | `ipm.externaldata.HubConnex*` <br/> |
|Conexões da IBM  <br/> | `ipm.externaldata.Connections*` <br/> |
|IBM SameTime  <br/> | `ipm.externaldata.Sametime*` <br/> |
|Bate-papo do ICE  <br/> | `ipm.externaldata.ICEChat.Chat` <br/> |
|Indii Messenger
  <br/> | `ipm.externaldata.Indii*` <br/> |
|Instagram
  <br/> | `ipm.externaldata.Instagram*` <br/> |
|Instant Bloomberg
  <br/> | `ipm.externaldata.InstantBloomberg*` <br/> |
|InvestEdge  <br/> | `ipm.externaldata.InvestEdge*` <br/> |
|IRC  <br/> | `ipm.externaldata.IRC*` <br/> |
|Jive
  <br/> | `ipm.externaldata.Jive*` <br/> |
|JiveApiRetention  <br/> | `ipm.externaldata.JiveApiRetention*` <br/> |
|JXTA  <br/> | `ipm.externaldata.JXTA*` <br/> |
|LinkedIn  <br/> | `ipm.externaldata.LinkedIn*` <br/> |
|MFTP  <br/> | `ipm.externaldata.MFTP*` <br/> |
|Comunicação unificada da Microsoft  <br/> | `ipm.externaldata.MicrosoftUC*` <br/> |
|Alinhar mente  <br/> | `ipm.externaldata.MindAlign*` <br/> |
|Mobile Guard  <br/> | `ipm.externaldata.MobileGuard*` <br/> |
|MSN  <br/> | `ipm.externaldata.MSN*` <br/> |
|Meu espaço  <br/> | `ipm.externaldata.MySpace*` <br/> |
|NEONetwork  <br/> | `ipm.externaldata.NEONetwork*` <br/> |
|OpenNap  <br/> | `ipm.externaldata.OpenNap*` <br/> |
|Pinterest  <br/> | `ipm.externaldata.Pinterest*` <br/> |
|Tabela dinâmica  <br/> | `ipm.externaldata.Pivot*` <br/> |
|QQ  <br/> | `ipm.externaldata.QQ*` <br/> |
|Microsoft SharePoint  <br/> | `ipm.externaldata.SharePoint*` <br/> |
|Salesforce Chatter  <br/> | `ipm.externaldata.Chatter*` <br/> |
|Skype for Business  <br/> | `ipm.externaldata.Skype*` <br/> |
|Slack Enterprise Grid  <br/> | `ipm.externaldata.Slack.IM` <br/> |
|SoftEther  <br/> | `ipm.externaldata.SoftEther*` <br/> |
|
Squawker
  <br/> | `ipm.externaldata.Squawker*` <br/> |
|Symphony
  <br/> | `ipm.externaldata.Symphony*` <br/> |
|Thomson Reuters  <br/> | `ipm.externaldata.Reuters*` <br/> |
| Thomson Reuters Eikon Messenger
  <br/> | `ipm.externaldata.ReutersEikon*` <br/> |
|Tor  <br/> | `ipm.externaldata.Tor*` <br/> |
|TTT  <br/> | `ipm.externaldata.TTT*` <br/> |
|Twitter  <br/> | `ipm.externaldata.Twitter*` <br/> |
|UBS Chat
  <br/> | `ipm.externaldata.UBS*` <br/> |
|Vimeo  <br/> | `ipm.externaldata.Vimeo*` <br/> |
|WinMX  <br/> | `ipm.externaldata.WinMX*` <br/> |
|Winny  <br/> | `ipm.externaldata.Winny*` <br/> |
|Yahoo!  <br/> | `ipm.externaldata.Yahoo!*` <br/> |
|Yammer  <br/> | `ipm.externaldata.Yammer*` <br/> |
|YellowJacket  <br/> | `ipm.externaldata.YellowJacket*` <br/> |
|YouTube  <br/> | `ipm.externaldata.YouTube*` <br/> |
