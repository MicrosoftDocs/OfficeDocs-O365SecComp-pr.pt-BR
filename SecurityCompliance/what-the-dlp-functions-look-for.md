---
title: O que as funções DLP procuram
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: 6/18/2016
ms.audience: Admin
ms.topic: reference
ms.service: o365-administration
localization_priority: Normal
ms.collection: Strat_O365_IP
search.appverid:
- MOE150
- MET150
ms.assetid: 94349ed4-5351-4ee2-bbda-70813c9ed693
description: Os tipos de informações confidenciais procure por um padrão específico e corroborá-lo assegurando formatação apropriada, aplicando somas de verificação e procurando por palavras-chave relevantes ou outras informações. Alguns dessa funcionalidade é realizada pelas funções internas. Este tópico explica o que essas funções procuram, para ajudá-lo a entender como os tipos de informações confidenciais predefinidos funcionam.
ms.openlocfilehash: 510f98e2b4e1d2480550f11026cf445be6ffc931
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/27/2018
ms.locfileid: "23013755"
---
# <a name="what-the-dlp-functions-look-for"></a>O que as funções DLP procuram

A política DLP inclui tipos de informação confidencial, como números de cartão de crédito e de cartão de débito da UE (União Europeia), que estão prontos para uso em suas políticas DLP. Esses tipos de informação confidencial procuram por um padrão específico e o confirmam, garantindo a formatação adequada, impondo as somas de verificação e procurando palavras-chave relevantes ou outras informações. Algumas dessas funcionalidades são realizadas por funções internas. Por exemplo, o tipo de informação confidencial de Número de Cartão de Crédito usa uma função para procurar datas formatadas como uma data de expiração, para ajudar a corroborar que um número é um número de cartão de crédito.
  
Este tópico explica o que essas funções procuram, para ajudar você a entender como funcionam os tipos de informações confidenciais predefinidas. Para saber mais, consulte [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).
  
## <a name="funcusdate"></a>Func_us_date

Essa função procura por uma data no formato comumente usada nos EUA Isso inclui os formatos de "mês/dia/ano", "mês-dia-ano," e "mês dia/ano". Os nomes ou abreviações de meses não diferenciam maiusculas de minúsculas. 
  
Exemplos:
  
- 2 de dezembro de 2016
    
- 2 de dezembro de 2016
    
- dez 2016 02
    
- 12/2/2016
    
- 12/02/16
    
- Dez-2-2016
    
- 2-12-16
    
Nomes de meses aceitos:
  
- Inglês
    
  - Janeiro, fevereiro, março, abril, maio, junho, julho, agosto, setembro, outubro, novembro, dezembro
    
  - Junho, julho ago Dec de novembro de outubro de setembro de maio de fevereiro de janeiro abr de março.
    
## <a name="funceudate"></a>Func_eu_date

Essa função procura uma data no formato comumente usado na UE (e na maioria dos lugares fora dos Estados Unidos). Isso inclui os formatos de "dia/mês/ano", "dia-mês-ano" e "dia mês ano". Os nomes ou as abreviações de meses não diferenciam maiúsculas de minúsculas.
  
Exemplos:
  
- De 2016 2 de dezembro
    
- dez 02 2016
    
- 16 de dezembro de 2
    
- 2/12/2016
    
- 16/12/02
    
- 2-Dec-2016
    
- 2-12-16
    
Nomes de meses aceitos:
  
- Inglês
    
  - Janeiro, fevereiro, março, abril, maio, junho, julho, agosto, setembro, outubro, novembro, dezembro
    
  - Junho, julho ago Dec de novembro de outubro de setembro de maio de fevereiro de janeiro abr de março.
    
- Holandês
    
  - januari, februari, maart, April, mei, juni, juli, augustus, September, ocktober, October, November, December
    
  - Jan CTP de fevereiro maart abr mei junho, julho agosto Set setembro oct okt novembro dec
    
- Francês
    
  - janvier, février, mars, avril, mai, juin juillet, août, septembre, octobre, novembre, décembre
    
  - janv. févr. MARS avril mai juin juil. setembro de août outubro de novembro. déc.
    
- Alemão
    
  - jänuar, februar, märz, abril, mai, juni juli, agosto, setembro, oktober, novembro, dezember
    
  - Jan. / Jän. Fevereiro März Mai abr Juni Juli ago setembro Okt. Dez de novembro.
    
- Italiano
    
  - gennaio, febbraio, marzo, aprile, maggio, giugno, luglio, agosto, settembre, ottobre, novembre, dicembre
    
  - genn. febbr. Mar. abr. magg. giugno luglio ag. definições. ott. novembro. dic.
    
- Português
    
  - janeiro, fevereiro, março, marco, abril, maio, junho, julho, agosto, setembro, outubro, novembro, dezembro
    
  - Jan fev mar abr mai junho, julho atrás dispostos dez novembro
    
- Espanhol
    
  - enero, febrero, marzo, abril, mayo, junio, julio, agosto, septiembre, octubre, noviembre, diciembre
    
  - enero CTP de fevereiro. marzo abr. mayo junho julho. setembro de agosto/conjunto. outubro de novembro. dic.
    
## <a name="funceudate1-deprecated"></a>Func_eu_date1 (preterido)

> [!NOTE]
> Essa função foi preterida porque ele oferece suporte a apenas nomes de mês português, que agora estão incluídos na `Func_eu_date` função acima. 
  
Essa função procura por uma data no formato normalmente usado em português. O formato para essa função é os mesmos `Func_eu_date`, diferentes apenas no idioma usado.
  
Exemplos:
  
- Dez 2 2016
    
- dez 02 2016
    
- Dez 2 16
    
- 2/12/2016
    
- 16/12/02
    
- 2-Dez-2016
    
- 2-12-16
    
Nomes de meses aceitos:
  
- Português
    
  - janeiro, fevereiro, março, marco, abril, maio, junho, julho, agosto, setembro, outubro, novembro, dezembro
    
  - Jan fev mar abr mai junho, julho atrás dispostos dez novembro
    
## <a name="funceudate2-deprecated"></a>Func_eu_date2 (preterido)

> [!NOTE]
> Essa função foi preterida porque ele oferece suporte a apenas nomes de mês holandês, que agora estão incluídos na `Func_eu_date` função acima. 
  
Essa função procura por uma data no formato comumente usada em alemão. O formato para essa função é os mesmos `Func_eu_date`, diferentes apenas no idioma usado.
  
Exemplos:
  
- 2 Mei 2016
    
- 02 mei 2016
    
- 2 Mei 16
    
- 2/12/2016
    
- 16/12/02
    
- 2-Mei-2016
    
- 2-12-16
    
Nomes de meses aceitos:
  
- Holandês
    
  - januari, februari, maart, April, mei, juni, juli, augustus, September, ocktober, October, November, December
    
  - Jan CTP de fevereiro maart abr mei junho, julho agosto Set setembro oct okt novembro dec
    
## <a name="funcexpirationdate"></a>Func_expiration_date

Essa função procura por uma data nos formatos costumam ser utilizados pelos cartões de crédito e débito, que excluir dias em favor meses. Essa função corresponderá datas no formato de "mês/ano", "mês-ano", "ano [nome do mês]" e "ano [abreviação mês]". Os nomes ou abreviações de meses não diferenciam maiusculas de minúsculas.
  
Exemplos
  
- MM/AA -- por exemplo, 01/11 ou 1/11
    
- MM/AAAA -- por exemplo, 01/2011 ou 1/2011
    
- MM-AA -- por exemplo, 01-22 ou 1-11
    
- MM-AAAA -- por exemplo, 01-2000 ou 1-2000
    
Os seguintes formatos dão suporte a AA ou AAAA:
  
- Mês-AAAA – por exemplo, jan-2010 ou janeiro-2010 ou jan-10 ou janeiro-10
    
- Mês AAAA – por exemplo, 'janeiro 2010' ou 'jan 2010' ou 'janeiro 10' ou 'jan 10'
    
- MêsAAAA – por exemplo, 'janeiro2010' ou 'Jan2010' ou 'janeiro10' ou 'Jan10'
    
- Mês aaaa – por exemplo, 'janeiro de 2010' ou ' Jan/2010' ou ' janeiro/10' ou ' Jan/10'
    
Nomes de meses aceitos:
  
- Inglês
    
  - Janeiro, fevereiro, março, abril, maio, junho, julho, agosto, setembro, outubro, novembro, dezembro
    
  - CTP de fevereiro de Jan Mar Abr talvez junho, julho agosto setembro Oct novembro Dec
    
## <a name="funcusaddress"></a>Func_us_address

Essa função procura por um nome ou sigla de estado dos EUA seguida de um CEP válido, como são usados em endereços postais. O CEP deve ser um dos CEPs corretos associados ao nome ou sigla do estado americano. O nome do estado americano e o CEP não podem ser separados por pontos ou letras.
  
Exemplos:
  
- Washington 98052
    
- Washington 98052-9998
    
- WA 98052
    
- WA 98052-9998
    

