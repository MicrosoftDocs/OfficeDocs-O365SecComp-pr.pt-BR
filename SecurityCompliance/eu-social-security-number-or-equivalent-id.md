---
title: Número de seguro social da UE ou ID equivalente
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: 8/17/2018
ms.audience: Admin
ms.topic: reference
ms.service: O365-seccomp
localization_priority: Normal
ms.assetid: 1fabd341-e594-4bfe-961c-62aa82893f60
description: Este tópico mostra o que uma política de prevenção de perda de dados (DLP) procura quando detecta o número de segurança social da UE ou o tipo de informação confidencial de ID equivalente. Esse tipo de informação confidencial define diferentes padrões, palavras-chave e outras evidências para cada país.
ms.openlocfilehash: abcefb6930e9c02d2f32d84b65accfecf1e20d95
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30216521"
---
# <a name="eu-social-security-number-or-equivalent-id"></a>Número de seguro social da UE ou ID equivalente

Este tópico mostra o que uma política de prevenção de perda de dados (DLP) procura quando detecta o número de segurança social da UE (SSN) ou o tipo de informação confidencial de ID equivalente. Esse tipo de informação confidencial define diferentes padrões, palavras-chave e outras evidências para cada país.
  
## <a name="austria"></a>Áustria

### <a name="format"></a>Formato

10 dígitos no formato especificado
  
### <a name="pattern"></a>Padrão

10 dígitos:
  
-  Três dígitos que correspondem a um número de série 
    
- Um dígito de verificação
    
- Seis dígitos que correspondem à data de nascimento (DDMMAA)
    
### <a name="checksum"></a>Soma de verificação

Sim
  
### <a name="definition"></a>Definição

Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:
  
- A função `Func_austria_eu_ssn_or_equivalent` localiza conteúdo que corresponde ao padrão. 
    
- Uma palavra- `Keywords_austria_eu_ssn_or_equivalent` chave de foi encontrada. 
    
Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:
  
- A função `Func_austria_eu_ssn_or_equivalent` localiza conteúdo que corresponde ao padrão. 
    
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

segurança social não
  
social security number

  

social security code
  
número de seguro
  
SSN austríaco
  
es
  
es
  
código de seguro
  
código de seguro #
  
socialsecurityno #
  
sozialversicherungsnummer
  
soziale Sicherheit Kein
  
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
  
- A função `Func_belgium_eu_ssn_or_equivalent` localiza conteúdo que corresponde ao padrão. 
    
- Uma palavra- `Keywords_belgium_eu_ssn_or_equivalent` chave de foi encontrada. 
    
Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:
  
- A função `Func_belgium_eu_ssn_or_equivalent` localiza conteúdo que corresponde ao padrão. 
    
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

número Nacional belga
  
número nacional
  
social security number

  
nationalnumber #
  
es
  
es
  
nationalnumber
  
BNN #
  
BNN
  
número de identificação pessoal
  
personalidnumber #
  
nacional Numéro
  
numéro de sécurité

  
Numéro d'assuré
  
nacional de identificação
  
identifiantnational #
  
numéronational #
  
## <a name="croatia"></a>Croácia

### <a name="format"></a>Formato

11 dígitos sem espaços e delimitadores
  
### <a name="pattern"></a>Padrão

 11 dígitos: 
  
-  Dez dígitos 
    
- Um dígito de verificação
    
### <a name="checksum"></a>Soma de verificação

Sim
  
### <a name="definition"></a>Definição

Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:
  
- A função `Func_croatia_eu_ssn_or_equivalent` localiza conteúdo que corresponde ao padrão. 
    
- Uma palavra- `Keywords_croatia_eu_ssn_or_equivalent` chave de foi encontrada. 
    
Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:
  
- A função `Func_croatia_eu_ssn_or_equivalent` localiza conteúdo que corresponde ao padrão. 
    
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
  
número do cidadão mestre
  
número de identificação nacional
  
social security number

  
nationalnumber #
  
es
  
es
  
nationalnumber
  
BNN #
  
BNN
  
número de identificação pessoal
  
personalidnumber #
  
NIB
  
Osobni identifikacijski broj
  
## <a name="czech-republic"></a>República Tcheca

### <a name="format"></a>Formato

Dez dígitos e uma barra invertida no padrão especificado
  
### <a name="pattern"></a>Padrão

Dez dígitos e uma barra invertida:
  
- Seis dígitos que correspondem à data de nascimento (AAMMDD): 
    
- Uma barra invertida
    
- Três dígitos que correspondem a um número de série que separa as pessoas nasceu na mesma data
    
- Um dígito de verificação
    
### <a name="checksum"></a>Soma de verificação

Sim
  
### <a name="definition"></a>Definição

Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:
  
- A função `Func_czech_republic_eu_ssn_or_equivalent` localiza conteúdo que corresponde ao padrão. 
    
- Uma palavra- `Keywords_czech_republic_eu_ssn_or_equivalent` chave de foi encontrada. 
    
Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:
  
- A função `Func_czech_republic_eu_ssn_or_equivalent` localiza conteúdo que corresponde ao padrão. 
    
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
  
es
  
es
  
número nacional
  
número de identificação pessoal
  
personalidnumber #
  
rč
  
rodné číslo
  
RODNE cislo
  
## <a name="denmark"></a>Dinamarca

### <a name="format"></a>Formato

Dez dígitos e um hífen no padrão especificado
  
### <a name="pattern"></a>Padrão

Dez dígitos e um hífen:
  
- Seis dígitos que correspondem à data de nascimento (DDMMAA) 
    
- Um hífen
    
- Quatro dígitos que correspondem a um número de sequência
    
### <a name="checksum"></a>Soma de verificação

Sim
  
### <a name="definition"></a>Definição

Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:
  
- A função `Func_denmark_eu_ssn_or_equivalent` localiza conteúdo que corresponde ao padrão. 
    
- Uma palavra- `Keywords_denmark_eu_ssn_or_equivalent` chave de foi encontrada. 
    
Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:
  
- A função `Func_denmark_eu_ssn_or_equivalent` localiza conteúdo que corresponde ao padrão. 
    
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
  
es
  
es
  
número nacional
  
número de identificação pessoal
  
personalidnumber #
  
CPR-Nummer
  
personnummer
  
## <a name="finland"></a>Finlândia

### <a name="format"></a>Formato

Uma combinação de 11 caracteres no formato especificado
  
### <a name="pattern"></a>Padrão

Uma combinação de 11 caracteres no formato especificado:
  
-  Seis dígitos 
    
- Uma instância de um dos seguintes:
    
  - Símbolo de adição
    
  - Símbolo de subTração
    
  - A letra "A" (não diferencia maiúsculas de minúsculas)
    
- Três dígitos
    
- Uma letra ou um dígito
    
### <a name="checksum"></a>Soma de verificação

Sim
  
### <a name="definition"></a>Definição

Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:
  
- A função `Func_finland_eu_ssn_or_equivalent` localiza conteúdo que corresponde ao padrão. 
    
- Uma palavra- `Keywords_finland_eu_ssn_or_equivalent` chave de foi encontrada. 
    
Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:
  
- A função `Func_finland_eu_ssn_or_equivalent` localiza conteúdo que corresponde ao padrão. 
    
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

  
ID pessoal
  
número de identidade
  
número de ID nacional da finlandês
  
personalidnumber #
  
número de identificação nacional
  
número de identificação
  
n º de ID nacional
  
número de ID nacional
  
ID não
  
tunnistenumero
  
henkilötunnus
  
yksilöllinen henkilökohtainen tunnistenumero
  
ainutlaatuinen henkilökohtainen Tunnus
  
identiteetti numero
  
Suomen Kansallinen henkilötunnus
  
henkilötunnusnumero #
  
kansallisen tunnistenumero
  
tunnusnumero
  
Kansallinen Tunnus numero
  
Hetu
  
## <a name="france"></a>França

Para obter detalhes, consulte a seção "França Social Security Number (INSEE)" em [o que os tipos de informações confidenciais procuram](what-the-sensitive-information-types-look-for.md).
  
## <a name="germany"></a>Alemanha

Para obter detalhes, consulte a seção "número do cartão de identidade da Alemanha" em [o que os tipos de informações confidenciais buscam](what-the-sensitive-information-types-look-for.md).
  
## <a name="greece"></a>Grécia

Para obter detalhes, consulte a seção "cartão de ID nacional da Grécia" em [que os tipos de informações confidenciais buscam](what-the-sensitive-information-types-look-for.md).
  
## <a name="hungary"></a>Hungria

### <a name="format"></a>Formato

Nove dígitos sem espaços e delimitadores
  
### <a name="pattern"></a>Padrão

Nove dígitos
  
### <a name="checksum"></a>Soma de verificação

Sim
  
### <a name="definition"></a>Definição

Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:
  
- A função `Func_hungary_eu_ssn_or_equivalent` localiza conteúdo que corresponde ao padrão. 
    
- Uma palavra- `Keywords_hungary_eu_ssn_or_equivalent` chave de foi encontrada. 
    
Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:
  
- A função `Func_hungary_eu_ssn_or_equivalent` localiza conteúdo que corresponde ao padrão. 
    
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

número de seguro social de seguridade
  
social security number

  
socialSecurityNumber #
  
hssn #
  
socialsecuritynno
  
hssn
  
Taj
  
Taj #
  
es
  
es
  
segurança social não
  
áfa
  
közösségi adószám
  
általános forgalmi adó szám
  
hozzáadottérték adó
  
áfa szám
  
Magyar áfa szám
  
## <a name="portugal"></a>Portugal

Para obter detalhes, consulte a seção "número de cartão de cidadão da Portugal" em [o que os tipos de informações confidenciais buscam](what-the-sensitive-information-types-look-for.md).
  
## <a name="spain"></a>Espanha

Para obter detalhes, consulte a seção "número de seguridade social da Espanha (SSN)" em [o que os tipos de informações confidenciais procuram](what-the-sensitive-information-types-look-for.md).
  
## <a name="sweden"></a>Suécia

### <a name="format"></a>Formato

12 dígitos sem espaços e delimitadores
  
### <a name="pattern"></a>Padrão

12 dígitos:
  
-  Oito dígitos que correspondem à data de nascimento (AAAAMMDD) 
    
- Três dígitos que correspondem a um número de série em que: 
    
  - O último dígito no número de série indica sexo pela atribuição de um número ímpar para macho e um número par para o fêmea
    
  - Até 1990, a atribuição de número de série correspondente à região onde o portador do número nasceu ou (se nasceu antes de 1947) em que ele/ela estava em vida, de acordo com os registros de impostos, em 1º de janeiro de 1947, com um código especial (geralmente 9 como o sétimo dígito) para immigrants 
    
- Um dígito de verificação
    
### <a name="checksum"></a>Soma de verificação

Sim
  
### <a name="definition"></a>Definição

Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:
  
- A função `Func_sweden_eu_ssn_or_equivalent` localiza conteúdo que corresponde ao padrão. 
    
- Uma palavra- `Keywords_sweden_eu_ssn_or_equivalent` chave de foi encontrada. 
    
Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:
  
- A função `Func_sweden_eu_ssn_or_equivalent` localiza conteúdo que corresponde ao padrão. 
    
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

  
n º de identificação pessoal
  
identidade não
  
identificação não
  
identificação pessoal não
  
ID personnummer
  
ID Personligt-Nummer
  
ID unikt-Nummer
  
personnummer
  
identifikationsnumret
  
personnummer #
  
identifikationsnumret #
  
## <a name="see-also"></a>Confira também

[O que os tipos de informação confidencial procuram](what-the-sensitive-information-types-look-for.md)

