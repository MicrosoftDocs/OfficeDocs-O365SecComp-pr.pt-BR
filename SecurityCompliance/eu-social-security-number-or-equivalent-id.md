---
title: ID do número de Seguridade Social da UE ou equivalente
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: 8/17/2018
ms.audience: Admin
ms.topic: reference
ms.service: o365-administration
localization_priority: Normal
ms.assetid: 1fabd341-e594-4bfe-961c-62aa82893f60
description: Este tópico mostra o que uma política de prevenção (DLP) de perda de dados procura por quando detecta o tipo de informações confidenciais de número de Seguridade Social da UE ou ID equivalente. Esse tipo de informações confidenciais define diferentes padrões, palavras-chave e outras evidências para cada país.
ms.openlocfilehash: 6f1027dcfb648ed937b8180d74d4bc6348dab650
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22523936"
---
# <a name="eu-social-security-number-or-equivalent-id"></a>ID do número de Seguridade Social da UE ou equivalente

Este tópico mostra o que uma política de prevenção (DLP) de perda de dados procura por quando detecta o tipo de informações confidenciais de número de Seguridade Social da UE (SSN) ou ID equivalente. Esse tipo de informações confidenciais define diferentes padrões, palavras-chave e outras evidências para cada país.
  
## <a name="austria"></a>Áustria

### <a name="format"></a>Formato

10 dígitos no formato especificado
  
### <a name="pattern"></a>Padrão

10 dígitos:
  
-  Três dígitos que correspondem a um número de série 
    
- Seleção de um dígito
    
- Seis dígitos que correspondem à data de nascimento (DDMMYY)
    
### <a name="checksum"></a>Soma de verificação

Sim
  
### <a name="definition"></a>Definição

Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:
  
- A função `Func_austria_eu_ssn_or_equivalent` encontra conteúdo que corresponde ao padrão. 
    
- Uma palavra-chave da `Keywords_austria_eu_ssn_or_equivalent` for encontrado. 
    
Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:
  
- A função `Func_austria_eu_ssn_or_equivalent` encontra conteúdo que corresponde ao padrão. 
    
```
 <!-- EU SSN or Equivalent Number -->
<Entity id="d24e32a4-c0bb-4ba8-899d-6303b95742d9" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_austria_eu_ssn_or_equivalent" />
          <Match idRef="Keywords_austria_eu_ssn_or_equivalent" />
        </Pattern>
<Pattern confidenceLevel="75">
            <IdMatch idRef="Func_austria_eu_ssn_or_equivalent" />
          </Pattern>
</Entity>
```

### <a name="keywords"></a>Palavras-chave

#### <a name="keywordsaustriaeussnorequivalent"></a>Keywords_austria_eu_ssn_or_equivalent

seguridade social nenhum
  
social security number

  

social security code
  
número do seguro
  
ssn austríaco
  
SSN #
  
SSN
  
código de seguro
  
código de seguros #
  
socialsecurityno #
  
sozialversicherungsnummer
  
soziale sicherheit kein
  
versicherungsnummer
  
## <a name="belgium"></a>Bélgica

### <a name="format"></a>Formato

11 dígitos sem espaços ou delimitadores
  
### <a name="pattern"></a>Padrão

11 dígitos
  
### <a name="checksum"></a>Soma de verificação

Sim
  
### <a name="definition"></a>Definição

Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:
  
- A função `Func_belgium_eu_ssn_or_equivalent` encontra conteúdo que corresponde ao padrão. 
    
- Uma palavra-chave da `Keywords_belgium_eu_ssn_or_equivalent` for encontrado. 
    
Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:
  
- A função `Func_belgium_eu_ssn_or_equivalent` encontra conteúdo que corresponde ao padrão. 
    
```
 <!-- EU SSN or Equivalent Number -->
<Entity id="d24e32a4-c0bb-4ba8-899d-6303b95742d9" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_belgium_eu_ssn_or_equivalent" />
          <Match idRef="Keywords_belgium_eu_ssn_or_equivalent" />
        </Pattern> 
       <Pattern confidenceLevel="75">
          <IdMatch idRef="Func_belgium_eu_ssn_or_equivalent" />
        </Pattern>      
</Entity>
```

### <a name="keywords"></a>Palavras-chave

#### <a name="keywordsbelgiumeussnorequivalent"></a>Keywords_belgium_eu_ssn_or_equivalent

número nacional belga
  
número nacional
  
social security number

  
nationalnumber #
  
SSN #
  
SSN
  
nationalnumber
  
bnn #
  
bnn
  
número de identificação pessoal
  
personalidnumber #
  
numéro nacional
  
numéro de sécurité

  
d numéro'assuré
  
identifiant nacional
  
identifiantnational #
  
numéronational #
  
## <a name="croatia"></a>Croácia

### <a name="format"></a>Formato

11 dígitos sem espaços e delimitadores
  
### <a name="pattern"></a>Padrão

 11 dígitos: 
  
-  Dez dígitos 
    
- Seleção de um dígito
    
### <a name="checksum"></a>Soma de verificação

Sim
  
### <a name="definition"></a>Definição

Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:
  
- A função `Func_croatia_eu_ssn_or_equivalent` encontra conteúdo que corresponde ao padrão. 
    
- Uma palavra-chave da `Keywords_croatia_eu_ssn_or_equivalent` for encontrado. 
    
Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:
  
- A função `Func_croatia_eu_ssn_or_equivalent` encontra conteúdo que corresponde ao padrão. 
    
```
 <!-- EU SSN or Equivalent Number -->
<Entity id="d24e32a4-c0bb-4ba8-899d-6303b95742d9" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_croatia_eu_ssn_or_equivalent" />
          <Match idRef="Keywords_croatia_eu_ssn_or_equivalent" />
        </Pattern> 
       <Pattern confidenceLevel="75">
          <IdMatch idRef="Func_croatia_eu_ssn_or_equivalent" />
        </Pattern>      
</Entity>
```

### <a name="keywords"></a>Palavras-chave

#### <a name="keywordscroatiaeussnorequivalent"></a>Keywords_croatia_eu_ssn_or_equivalent

número de identificação pessoal
  
número de cidadãos mestre
  
número de identificação nacional
  
social security number

  
nationalnumber #
  
SSN #
  
SSN
  
nationalnumber
  
bnn #
  
bnn
  
número de identificação pessoal
  
personalidnumber #
  
oib
  
osobni identifikacijski broj
  
## <a name="czech-republic"></a>República Tcheca

### <a name="format"></a>Formato

Dez dígitos e uma barra invertida no padrão especificado
  
### <a name="pattern"></a>Padrão

Dez dígitos e uma barra invertida:
  
- Seis dígitos que correspondem à data de nascimento (aammdd): 
    
- Uma barra invertida
    
- Três dígitos que correspondem a um número de série que separa pessoas nascidas na mesma data
    
- Seleção de um dígito
    
### <a name="checksum"></a>Soma de verificação

Sim
  
### <a name="definition"></a>Definição

Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:
  
- A função `Func_czech_republic_eu_ssn_or_equivalent` encontra conteúdo que corresponde ao padrão. 
    
- Uma palavra-chave da `Keywords_czech_republic_eu_ssn_or_equivalent` for encontrado. 
    
Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:
  
- A função `Func_czech_republic_eu_ssn_or_equivalent` encontra conteúdo que corresponde ao padrão. 
    
```
 <!-- EU SSN or Equivalent Number -->
<Entity id="d24e32a4-c0bb-4ba8-899d-6303b95742d9" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_czech_republic_eu_ssn_or_equivalent" />
          <Match idRef="Keywords_czech_republic_eu_ssn_or_equivalent" />
        </Pattern> 
       <Pattern confidenceLevel="75">
          <IdMatch idRef="Func_czech_republic_eu_ssn_or_equivalent" />
        </Pattern>      
</Entity>
```

### <a name="keywords"></a>Palavras-chave

#### <a name="keywordsczechrepubliceussnorequivalent"></a>Keywords_czech_republic_eu_ssn_or_equivalent

número de nascimento
  
número de identificação nacional
  
número de identificação pessoal
  
social security number

  
nationalnumber #
  
SSN #
  
SSN
  
número nacional
  
número de identificação pessoal
  
personalidnumber #
  
rč
  
rodné číslo
  
rodne cislo
  
## <a name="denmark"></a>Dinamarca

### <a name="format"></a>Formato

Dez dígitos e um hífen no padrão especificado
  
### <a name="pattern"></a>Padrão

Dez dígitos e um hífen:
  
- Seis dígitos que correspondem à data de nascimento (DDMMYY) 
    
- Um hífen
    
- Quatro dígitos que correspondem a um número de sequência
    
### <a name="checksum"></a>Soma de verificação

Sim
  
### <a name="definition"></a>Definição

Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:
  
- A função `Func_denmark_eu_ssn_or_equivalent` encontra conteúdo que corresponde ao padrão. 
    
- Uma palavra-chave da `Keywords_denmark_eu_ssn_or_equivalent` for encontrado. 
    
Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:
  
- A função `Func_denmark_eu_ssn_or_equivalent` encontra conteúdo que corresponde ao padrão. 
    
```
 <!-- EU SSN or Equivalent Number -->
<Entity id="d24e32a4-c0bb-4ba8-899d-6303b95742d9" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_denmark_eu_ssn_or_equivalent" />
          <Match idRef="Keywords_denmark_eu_ssn_or_equivalent" />
        </Pattern> 
       <Pattern confidenceLevel="75">
          <IdMatch idRef="Func_denmark_eu_ssn_or_equivalent" />
        </Pattern>      
</Entity>
```

### <a name="keywords"></a>Palavras-chave

#### <a name="keywordsdenmarkeussnorequivalent"></a>Keywords_denmark_eu_ssn_or_equivalent

número de identificação pessoal
  
número de identificação nacional
  
social security number

  
nationalnumber #
  
SSN #
  
SSN
  
número nacional
  
número de identificação pessoal
  
personalidnumber #
  
CPR-nummer
  
personnummer
  
## <a name="finland"></a>Finlândia

### <a name="format"></a>Formato

Uma combinação de caracteres 11 no formato especificado
  
### <a name="pattern"></a>Padrão

Uma combinação de 11 caracteres em um formato específico:
  
-  Seis dígitos 
    
- Uma instância de um dos seguintes:
    
  - Símbolo de mais
    
  - Menos símbolo
    
  - A letra "A" (não diferencia maiusculas de minúsculas)
    
- Três dígitos
    
- Uma letra ou dígito de um
    
### <a name="checksum"></a>Soma de verificação

Sim
  
### <a name="definition"></a>Definição

Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:
  
- A função `Func_finland_eu_ssn_or_equivalent` encontra conteúdo que corresponde ao padrão. 
    
- Uma palavra-chave da `Keywords_finland_eu_ssn_or_equivalent` for encontrado. 
    
Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:
  
- A função `Func_finland_eu_ssn_or_equivalent` encontra conteúdo que corresponde ao padrão. 
    
```
 <!-- EU SSN or Equivalent Number -->
<Entity id="d24e32a4-c0bb-4ba8-899d-6303b95742d9" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_finland_eu_ssn_or_equivalent" />
          <Match idRef="Keywords_finland_eu_ssn_or_equivalent" />
        </Pattern> 
       <Pattern confidenceLevel="75">
          <IdMatch idRef="Func_finland_eu_ssn_or_equivalent" />
        </Pattern>      
</Entity>
```

### <a name="keywords"></a>Palavras-chave

#### <a name="keywordsfinlandeussnorequivalent"></a>Keywords_finland_eu_ssn_or_equivalent

identification number

  
identificação pessoal
  
número de identidade
  
número de identificação nacional finlandês
  
personalidnumber #
  
número de identificação nacional
  
número de identificação
  
id nacional nenhum.
  
número de identificação nacional
  
ID nenhum
  
tunnistenumero
  
henkilötunnus
  
yksilöllinen henkilökohtainen tunnistenumero
  
ainutlaatuinen henkilökohtainen tunnus
  
numero identiteetti
  
suomen kansallinen henkilötunnus
  
henkilötunnusnumero #
  
kansallisen tunnistenumero
  
tunnusnumero
  
kansallinen tunnus numero
  
hetu
  
## <a name="france"></a>França

Para obter detalhes, consulte a seção "França número de Seguridade Social (INSEE)" em [quais tipos de informações confidenciais a procurar](what-the-sensitive-information-types-look-for.md).
  
## <a name="germany"></a>Alemanha

Para obter detalhes, consulte a seção "Número de cartão de identificação da Alemanha" em [quais tipos de informações confidenciais a procurar](what-the-sensitive-information-types-look-for.md).
  
## <a name="greece"></a>Grécia

Para obter detalhes, consulte a seção "Grécia cartão de identificação nacional" nos [quais os tipos de informações confidenciais procurar](what-the-sensitive-information-types-look-for.md).
  
## <a name="hungary"></a>Hungria

### <a name="format"></a>Formato

Nove dígitos sem espaços e delimitadores
  
### <a name="pattern"></a>Padrão

Nove dígitos
  
### <a name="checksum"></a>Soma de verificação

Sim
  
### <a name="definition"></a>Definição

Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:
  
- A função `Func_hungary_eu_ssn_or_equivalent` encontra conteúdo que corresponde ao padrão. 
    
- Uma palavra-chave da `Keywords_hungary_eu_ssn_or_equivalent` for encontrado. 
    
Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:
  
- A função `Func_hungary_eu_ssn_or_equivalent` encontra conteúdo que corresponde ao padrão. 
    
```
 <!-- EU SSN or Equivalent Number -->
<Entity id="d24e32a4-c0bb-4ba8-899d-6303b95742d9" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_hungary_eu_ssn_or_equivalent" />
          <Match idRef="Keywords_hungary_eu_ssn_or_equivalent" />
        </Pattern> 
       <Pattern confidenceLevel="75">
          <IdMatch idRef="Func_hungary_eu_ssn_or_equivalent" />
        </Pattern>      
</Entity>
```

### <a name="keywords"></a>Palavras-chave

#### <a name="keywordshungaryeussnorequivalent"></a>Keywords_hungary_eu_ssn_or_equivalent

número de seguridade social húngaro
  
social security number

  
NúmeroDoINPS #
  
hssn #
  
socialsecuritynno
  
hssn
  
taj
  
taj #
  
SSN
  
SSN #
  
seguridade social nenhum
  
áfa
  
közösségi adószám
  
általános forgalmi adó szám
  
hozzáadottérték adó
  
áfa szám
  
áfa magyar szám
  
## <a name="portugal"></a>Portugal

Para obter detalhes, consulte a seção "Número de cartão de cidadãos Portugal" nos [quais os tipos de informações confidenciais procurar](what-the-sensitive-information-types-look-for.md).
  
## <a name="spain"></a>Espanha

Para obter detalhes, consulte a seção "Espanha número de Seguridade Social (SSN)" em [quais tipos de informações confidenciais a procurar](what-the-sensitive-information-types-look-for.md).
  
## <a name="sweden"></a>Suécia

### <a name="format"></a>Formato

12 dígitos sem espaços e delimitadores
  
### <a name="pattern"></a>Padrão

12 dígitos:
  
-  Oito dígitos que correspondem à data de nascimento (AAAAMMDD) 
    
- Três dígitos que correspondem a um número de série onde: 
    
  - O último dígito no número de série indica gênero pela atribuição de um número ímpar de masculino e um número par de fêmea
    
  - Até 1990, a atribuição do número de série correspondeu a região onde o portador do número surgiu ou (se nascer antes 1947) onde ele/ela tinha sido mora, de acordo com os registros de impostos, em 1 de janeiro de 1947, com um código especial (geralmente 9 como o dígito 7) para immigrants 
    
- Seleção de um dígito
    
### <a name="checksum"></a>Soma de verificação

Sim
  
### <a name="definition"></a>Definição

Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:
  
- A função `Func_sweden_eu_ssn_or_equivalent` encontra conteúdo que corresponde ao padrão. 
    
- Uma palavra-chave da `Keywords_sweden_eu_ssn_or_equivalent` for encontrado. 
    
Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:
  
- A função `Func_sweden_eu_ssn_or_equivalent` encontra conteúdo que corresponde ao padrão. 
    
```
 <!-- EU SSN or Equivalent Number -->
<Entity id="d24e32a4-c0bb-4ba8-899d-6303b95742d9" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_sweden_eu_ssn_or_equivalent" />
          <Match idRef="Keywords_sweden_eu_ssn_or_equivalent" />
        </Pattern> 
       <Pattern confidenceLevel="75">
          <IdMatch idRef="Func_sweden_eu_ssn_or_equivalent" />
        </Pattern>      
</Entity>
```

### <a name="keywords"></a>Palavras-chave

#### <a name="keywordsswedeneussnorequivalent"></a>Keywords_sweden_eu_ssn_or_equivalent

número de identificação pessoal
  
identification number

  
identificação pessoal nenhum
  
identidade nenhum
  
identificação nenhum
  
identificação pessoal nenhum
  
id de personnummer
  
id de personligt-nummer
  
id de unikt-nummer
  
personnummer
  
identifikationsnumret
  
personnummer #
  
identifikationsnumret #
  
## <a name="see-also"></a>Confira também

[O que os tipos de informações confidenciais procuram](what-the-sensitive-information-types-look-for.md)

