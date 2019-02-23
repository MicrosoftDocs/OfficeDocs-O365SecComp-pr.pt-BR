---
title: O que as funções DLP procuram
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: 6/18/2016
ms.audience: Admin
ms.topic: reference
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: Strat_O365_IP
search.appverid:
- MOE150
- MET150
ms.assetid: 94349ed4-5351-4ee2-bbda-70813c9ed693
description: Os tipos de informações confidenciais procuram um padrão específico e o corroboratem, garantindo a formatação adequada, aplicando as somas de verificação e procurando palavras-chave relevantes ou outras informações. Algumas dessas funcionalidades são executadas por funções internas. Este tópico explica o que essas funções procuram para ajudá-lo a entender como funcionam os tipos de informações confidenciais predefinidos.
ms.openlocfilehash: 55c740e892e92902b368b2dcf7b0999cbc60f3ed
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30219351"
---
# <a name="what-the-dlp-functions-look-for"></a>O que as funções DLP procuram

A política DLP inclui tipos de informação confidencial, como números de cartão de crédito e de cartão de débito da UE (União Europeia), que estão prontos para uso em suas políticas DLP. Esses tipos de informação confidencial procuram por um padrão específico e o confirmam, garantindo a formatação adequada, impondo as somas de verificação e procurando palavras-chave relevantes ou outras informações. Algumas dessas funcionalidades são realizadas por funções internas. Por exemplo, o tipo de informação confidencial de Número de Cartão de Crédito usa uma função para procurar datas formatadas como uma data de expiração, para ajudar a corroborar que um número é um número de cartão de crédito.
  
Este tópico explica o que essas funções procuram, para ajudar você a entender como funcionam os tipos de informações confidenciais predefinidas. Para saber mais, consulte [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).
  
## <a name="funcusdate"></a>Func_us_date

Essa função procura uma data no formato comumente usado nos EUA. Isso inclui os formatos "mês/dia/ano", "mês-dia-ano" e "ano dia do mês". Os nomes ou abreviações de meses não diferenciam maiúsculas de minúsculas. 
  
Exemplos:
  
- 2 de dezembro de 2016
    
- 2 de dezembro de 2016
    
- Dec 02 2016
    
- 12/2/2016
    
- 12/02/16
    
- Dec-2-2016
    
- 12-2-16
    
Nomes de meses aceitos:
  
- Inglês
    
  - Janeiro, fevereiro, março, abril, maio, junho de julho, agosto, setembro, outubro, novembro de dezembro
    
  - Jan. Fev. mar. abr. Maio de 1º de julho de agosto de setembro. Dec.
    
## <a name="funceudate"></a>Func_eu_date

Essa função procura uma data no formato comumente usado na UE (e na maioria dos lugares fora dos Estados Unidos). Isso inclui os formatos de "dia/mês/ano", "dia-mês-ano" e "dia mês ano". Os nomes ou as abreviações de meses não diferenciam maiúsculas de minúsculas.
  
Exemplos:
  
- 2 Dec 2016
    
- 02 de dezembro de 2016
    
- 2 de dezembro de 16
    
- 2/12/2016
    
- 02/12/16
    
- 2-dez-2016
    
- 2-12-16
    
Nomes de meses aceitos:
  
- Inglês
    
  - Janeiro, fevereiro, março, abril, maio, junho de julho, agosto, setembro, outubro, novembro de dezembro
    
  - Jan. Fev. mar. abr. Maio de 1º de julho de agosto de setembro. Dec.
    
- Holandês
    
  - januari, februari, maart, April, mei, juni, juli, augustus, September, ocktober, October, November, December
    
  - Jan fevereiro de maart de abril de Mei jun jul setembro de agosto de dezembro de Okt de Nov
    
- Francês
    
  - Janvier, Février, Mars, Avril, Mai, Juin Juillet, Août, Septembre, outubro, Novembre, décembre
    
  - Janv. févr. Mars Avril Mai Juin Juil. Août set. Oct. nov. déc.
    
- Alemão
    
  - jänuar, februar, März, abril, Mai, Juni Juli, agosto, setembro, Oktober, novembro de Dezember
    
  - Jan./Jän. Fev. März abr. Mai Juni Juli ago. set. Okt. Nov. dez.
    
- Italiano
    
  - gennaio, febbraio, Marzo, Aprile, Maggio, giugno, Luglio, agosto, Settembre, ottobre, Novembre, Dicembre
    
  - Genn. febbr. mar. abr. Magg. giugno Luglio AG. definida. Ott. Nov. DIC.
    
- Português
    
  - janeiro, fevereiro, março, marco, abril, maio, junho, julho, agosto, setembro, outubro, novembro, dezembro
    
  - Jan fev mar abr mai jun jul atrás Set out nov dez
    
- Espanhol
    
  - Enero, Febrero, Marzo, abril, Mayo, junio, Julio, agosto, Septiembre, Octubre, Noviembre, Diciembre
    
  - Enero Fev. Marzo abr. Mayo Jun. Jul. agosto set./set. Oct. nov. DIC.
    
## <a name="funceudate1-deprecated"></a>Func_eu_date1 (preterido)

> [!NOTE]
> Essa função foi preterida porque dá suporte apenas a `Func_eu_date` nomes de meses em Português, que agora estão incluídos na função acima. 
  
Essa função procura uma data no formato comumente usado em Português. O formato dessa função é o mesmo que `Func_eu_date`, diferente somente no idioma usado.
  
Exemplos:
  
- 2 dez 2016
    
- 02 dez 2016
    
- 2 dez 16
    
- 2/12/2016
    
- 02/12/16
    
- 2-dez-2016
    
- 2-12-16
    
Nomes de meses aceitos:
  
- Português
    
  - janeiro, fevereiro, março, marco, abril, maio, junho, julho, agosto, setembro, outubro, novembro, dezembro
    
  - Jan fev mar abr mai jun jul atrás Set out nov dez
    
## <a name="funceudate2-deprecated"></a>Func_eu_date2 (preterido)

> [!NOTE]
> Essa função foi preterida porque dá suporte apenas a `Func_eu_date` nomes de meses em Holandês, que agora estão incluídos na função acima. 
  
Essa função procura uma data no formato comumente usado em Holandês. O formato dessa função é o mesmo que `Func_eu_date`, diferente somente no idioma usado.
  
Exemplos:
  
- 2 Mei 2016
    
- 02 Mei 2016
    
- 2 Mei 16
    
- 2/12/2016
    
- 02/12/16
    
- 2-Mei-2016
    
- 2-12-16
    
Nomes de meses aceitos:
  
- Holandês
    
  - januari, februari, maart, April, mei, juni, juli, augustus, September, ocktober, October, November, December
    
  - Jan fevereiro de maart de abril de Mei jun jul setembro de agosto de dezembro de Okt de Nov
    
## <a name="funcexpirationdate"></a>Func_expiration_date

Essa função procura uma data nos formatos comumente usados por cartões de crédito e débito, que excluem dias em favor de meses. Essa função coincidirá datas no formato de "mês/ano", "Mês-Year", "[month Name] Year" e "[month abreviation] Year". Os nomes ou abreviações de meses não diferenciam maiúsculas de minúsculas.
  
Exemplos
  
- MM/AA -- por exemplo, 01/11 ou 1/11
    
- MM/AAAA -- por exemplo, 01/2011 ou 1/2011
    
- MM-AA -- por exemplo, 01-22 ou 1-11
    
- MM-AAAA -- por exemplo, 01-2000 ou 1-2000
    
Os seguintes formatos dão suporte a AA ou AAAA:
  
- Mês-AAAA – por exemplo, jan-2010 ou janeiro-2010 ou jan-10 ou janeiro-10
    
- Mês AAAA – por exemplo, 'janeiro 2010' ou 'jan 2010' ou 'janeiro 10' ou 'jan 10'
    
- MêsAAAA – por exemplo, 'janeiro2010' ou 'Jan2010' ou 'janeiro10' ou 'Jan10'
    
- Month/aaaa--por exemplo, ' Janeiro/2010 ' ou ' Jan/2010 ' ou ' janeiro/10 ' ou ' Jan/10 '
    
Nomes de meses aceitos:
  
- Inglês
    
  - Janeiro, fevereiro, março, abril, maio, junho de julho, agosto, setembro, outubro, novembro de dezembro
    
  - Jan fev mar de junho de julho de agosto de agosto de abril de dezembro
    
## <a name="funcusaddress"></a>Func_us_address

Essa função procura por um nome ou sigla de estado dos EUA seguida de um CEP válido, como são usados em endereços postais. O CEP deve ser um dos CEPs corretos associados ao nome ou sigla do estado americano. O nome do estado americano e o CEP não podem ser separados por pontos ou letras.
  
Exemplos:
  
- Washington 98052
    
- Washington 98052-9998
    
- WA 98052
    
- WA 98052-9998
    

