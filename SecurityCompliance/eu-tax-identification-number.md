---
title: Número de identificação de imposto da UE
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: 8/17/2018
ms.audience: Admin
ms.topic: reference
ms.service: o365-administration
localization_priority: Normal
ms.assetid: f04919c8-2356-4de2-bb2a-b9f67f339726
description: Este tópico mostra o que uma política de prevenção (DLP) de perda de dados procura por quando detecta o tipo de informações confidenciais de número de identificação de imposto da UE. Esse tipo de informações confidenciais define diferentes padrões, palavras-chave e outras evidências para cada país.
ms.openlocfilehash: 5192496b393d15fd6d063e09c9bfe1cb3dd7e2dd
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22524029"
---
# <a name="eu-tax-identification-number"></a>Número de identificação de imposto da UE

Este tópico mostra o que uma política de prevenção (DLP) de perda de dados procura por quando detecta o tipo de informações confidenciais de número de identificação da UE imposto (TIN). Esse tipo de informações confidenciais define diferentes padrões, palavras-chave e outras evidências para cada país.
  
## <a name="austria"></a>Áustria

### <a name="format"></a>Formato

Nove dígitos com hífen opcional e barra invertida
  
### <a name="pattern"></a>Padrão

Nove dígitos com hífen opcional e barra invertida:
  
-  Dois dígitos 
    
- Um hífen (opcional)
    
- Três dígitos
    
- Uma barra (opcional)
    
- Quatro dígitos
    
### <a name="checksum"></a>Soma de verificação

Sim
  
### <a name="definition"></a>Definição

Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:
  
- A função `Func_austria_eu_tax_file_number` encontra conteúdo que corresponde ao padrão. 
    
- Uma palavra-chave da `Keywords_austria_eu_tax_file_number` for encontrado. 
    
Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:
  
- A função `Func_austria_eu_tax_file_number` encontra conteúdo que corresponde ao padrão. 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_austria_eu_tax_file_number" />
          <Match idRef="Keywords_austria_eu_tax_file_number" />
        </Pattern>
<Pattern confidenceLevel="75">
          <IdMatch idRef="Func_austria_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Palavras-chave

#### <a name="keywordsaustriaeutaxfilenumber"></a>Keywords_austria_eu_tax_file_number

número de imposto
  
número
  
número de inscrição
  
tax id

  
St.nr.
  
steuernummer
  
## <a name="belgium"></a>Bélgica

### <a name="format"></a>Formato

11 dígitos sem espaços e delimitadores
  
### <a name="pattern"></a>Padrão

11 dígitos:
  
- Dois dígitos
    
- "0" ou "1"
    
- Um dígito
    
- "0" ou "1" ou "2" ou "3" 
    
- Seis dígitos
    
### <a name="checksum"></a>Soma de verificação

Não aplicável
  
### <a name="definition"></a>Definição

Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:
  
- A expressão regular `Regex_belgium_eu_tax_file_number` encontra conteúdo que corresponde ao padrão. 
    
- Uma palavra-chave da `Keywords_belgium_eu_tax_file_number` for encontrado. 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_belgium_eu_tax_file_number" />
          <Match idRef="Keywords_belgium_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Palavras-chave

#### <a name="keywordsbelgiumeutaxfilenumber"></a>Keywords_belgium_eu_tax_file_number

número de imposto
  
número de registro nacional
  
número de inscrição
  
tax id

  
NIF
  
NIF #
  
numéro de registre nacional
  
numéro d'identification fiscale
  
## <a name="bulgaria"></a>Bulgária

### <a name="format"></a>Formato

Dez dígitos sem espaços e delimitadores
  
### <a name="pattern"></a>Padrão

10 dígitos
  
### <a name="checksum"></a>Soma de verificação

Sim
  
### <a name="definition"></a>Definição

Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:
  
- A função `Func_bulgaria_eu_tax_file_number` encontra conteúdo que corresponde ao padrão. 
    
- Uma palavra-chave da `Keywords_bulgaria_eu_tax_file_number` for encontrado. 
    
Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:
  
- A função `Func_bulgaria_eu_tax_file_number` encontra conteúdo que corresponde ao padrão. 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_bulgaria_eu_tax_file_number" />
          <Match idRef="Keywords_bulgaria_eu_tax_file_number" />
        </Pattern>
 <Pattern confidenceLevel="75">
          <IdMatch idRef="Func_bulgaria_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Palavras-chave

#### <a name="keywordsbulgariaeutaxfilenumber"></a>Keywords_bulgaria_eu_tax_file_number

bucn
  
número de civil Uniform
  
bucn #
  
uniformcivilnumber #
  
id de civil Uniform
  
Uniform não civil
  
egn
  
número de civil uniform búlgaro
  
uniformcivilno #
  
egn #
  
УНИФОРМ ГРАЖДАНСКИ НОМЕР
  
Id униформ
  
Id граждански униформ
  
УНИФОРМ ГРАЖДАНСКИ НЕ
  
## <a name="croatia"></a>Croácia

### <a name="format"></a>Formato

11 dígitos sem espaços ou delimitadores
  
### <a name="pattern"></a>Padrão

11 dígitos:
  
- Dez dígitos, escolhidos aleatoriamente
    
- Seleção de um dígito
    
### <a name="checksum"></a>Soma de verificação

Sim
  
### <a name="definition"></a>Definição

Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:
  
- A função `Func_croatia_eu_tax_file_number` encontra conteúdo que corresponde ao padrão. 
    
- Uma palavra-chave da `Keywords_croatia_eu_tax_file_number` for encontrado. 
    
Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:
  
- A função `Func_croatia_eu_tax_file_number` encontra conteúdo que corresponde ao padrão. 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_croatia_eu_tax_file_number" />
          <Match idRef="Keywords_croatia_eu_tax_file_number" />
        </Pattern>
<Pattern confidenceLevel="75">
          <IdMatch idRef="Func_croatia_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Palavras-chave

#### <a name="keywordscroatiaeutaxfilenumber"></a>Keywords_croatia_eu_tax_file_number

número de imposto
  
imposto
  
tax id

  
identificação de objeto
  
identificação de objeto #
  
porezni broj
  
## <a name="cyprus"></a>Chipre

### <a name="format"></a>Formato

Oito dígitos e uma letra no padrão especificado
  
### <a name="pattern"></a>Padrão

Oito dígitos e uma letra:
  
-  "0" 
    
- Sete dígitos 
    
- Uma letra (não diferencia maiusculas de minúsculas)
    
### <a name="checksum"></a>Soma de verificação

Não aplicável
  
### <a name="definition"></a>Definição

Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:
  
- A função `Func_cyprus_eu_tax_file_number` encontra conteúdo que corresponde ao padrão. 
    
- Uma palavra-chave da `Keywords_cyprus_eu_tax_file_number` for encontrado. 
    
Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:
  
- A função `Func_cyprus_eu_tax_file_number` encontra conteúdo que corresponde ao padrão. 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_cyprus_eu_tax_file_number" />
          <Match idRef="Keywords_cyprus_eu_tax_file_number" />
        </Pattern>
Pattern confidenceLevel="75">
          <IdMatch idRef="Func_cyprus_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Palavras-chave

#### <a name="keywordscypruseutaxfilenumber"></a>Keywords_cyprus_eu_tax_file_number

número de imposto
  
imposto
  
tax id

  
código de identificação de imposto
  
velha
  
velha #
  
ΑΡΙΘΜΌΣ ΦΟΡΟΛΟΓΙΚΟΎ ΜΗΤΡΏΟΥ
  
ΦΟΡΟΛΟΓΙΚΉ ΤΑΥΤΌΤΗΤΑ
  
ΚΩΔΙΚΌΣ ΦΟΡΟΛΟΓΙΚΟΎ ΜΗΤΡΏΟΥ
  
## <a name="czech-republic"></a>República Tcheca

### <a name="format"></a>Formato

Nove ou dez dígitos com uma barra invertida a opcional
  
### <a name="pattern"></a>Padrão

Nove ou dez dígitos com um backslashl opcional:
  
- Seis dígitos 
    
- Uma barra invertida (opcional)
    
- Três ou quatro dígitos
    
### <a name="checksum"></a>Soma de verificação

Não aplicável
  
### <a name="definition"></a>Definição

Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:
  
- A expressão regular `Regex_czech_republic_eu_tax_file_number` encontra conteúdo que corresponde ao padrão. 
    
- Uma palavra-chave da `Keywords_czech_republic_eu_tax_file_number` for encontrado. 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_czech_republic_eu_tax_file_number" />
          <Match idRef="Keywords_czech_republic_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Palavras-chave

#### <a name="keywordsczechrepubliceutaxfilenumber"></a>Keywords_czech_republic_eu_tax_file_number

número de imposto
  
imposto
  
tax id

  
número de pessoal
  
daňové číslo
  
osobní číslo
  
## <a name="denmark"></a>Dinamarca

### <a name="format"></a>Formato

Dez dígitos que contém um hífen
  
### <a name="pattern"></a>Padrão

Dez dígitos que contém um hyphenl:
  
-  Seis dígitos que correspondem à data de nascimento (DDMMYY) 
    
- Um hífen
    
- Quatro dígitos que correspondem a um número de sequência em que o primeiro dígito corresponde como o century de nascimento e o último dígito corresponde ao gênero do indivíduo (ímpar para masculino e até mesmo fêmea)
    
### <a name="checksum"></a>Soma de verificação

Sim
  
### <a name="definition"></a>Definição

Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:
  
- A função `Func_denmark_eu_tax_file_number` encontra conteúdo que corresponde ao padrão. 
    
- Uma palavra-chave da `Keywords_denmark_eu_tax_file_number` for encontrado. 
    
Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:
  
- A função `Func_denmark_eu_tax_file_number` encontra conteúdo que corresponde ao padrão. 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_denmark_eu_tax_file_number" />
          <Match idRef="Keywords_denmark_eu_tax_file_number" />
        </Pattern> 
<Pattern confidenceLevel="75">
          <IdMatch idRef="Func_denmark_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Palavras-chave

#### <a name="keywordsdenmarkeutaxfilenumber"></a>Keywords_denmark_eu_tax_file_number

número de imposto
  
imposto
  
tax id

  
número de CPR
  
CPR #
  
skat nummer
  
id de skat
  
## <a name="estonia"></a>Estônia

### <a name="format"></a>Formato

11 dígitos sem espaços ou delimitadores
  
### <a name="pattern"></a>Padrão

11 dígitos:
  
-  Um dígito que corresponde ao gênero e century de nascimento onde um número ímpar indica masculino e o número par fêmea da seguinte maneira: 1, 2 para o décimo nono century; 3, 4 para o century 20; e 5, 6 para o century 21 
    
- Seis dígitos que correspondem à data de nascimento (aammdd)
    
- Três dígitos que correspondem a um número de série separando pessoas nascidas na mesma data
    
- Seleção de um dígito
    
### <a name="checksum"></a>Soma de verificação

Sim
  
### <a name="definition"></a>Definição

Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:
  
- A função `Func_estonia_eu_tax_file_number` encontra conteúdo que corresponde ao padrão. 
    
- Uma palavra-chave da `Keywords_estonia_eu_tax_file_number` for encontrado. 
    
Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:
  
- A função `Func_estonia_eu_tax_file_number` encontra conteúdo que corresponde ao padrão. 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_estonia_eu_tax_file_number" />
          <Match idRef="Keywords_estonia_eu_tax_file_number" />
        </Pattern>
<Pattern confidenceLevel="75">
          <IdMatch idRef="Func_estonia_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Palavras-chave

#### <a name="keywordsestoniaeutaxfilenumber"></a>Keywords_estonia_eu_tax_file_number

número de imposto
  
imposto
  
tax id

  
código pessoal
  
maksunumber
  
id de maksu
  
isikukood
  
## <a name="finland"></a>Finlândia

### <a name="format"></a>Formato

Uma combinação de 11 caracteres de dígitos, letras, e mais e menos de entrada
  
### <a name="pattern"></a>Padrão

Uma combinação de 11 caracteres de dígitos, letras, e mais e menos entrada:
  
- Seis dígitos
    
- Um dos seguintes: um sinal de adição, um sinal de subtração ou a letra "A" (não diferenciar maiusculas de minúsculas) onde o sinal de adição significa nascer entre 1800-1899, o sinal de menos assinar significa nascer entre 1900-1999 e "A" significa Nascida 2000 e depois
    
- Três dígitos
    
- Uma letra ou um número
    
### <a name="checksum"></a>Soma de verificação

Sim
  
### <a name="definition"></a>Definição

Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:
  
- A função `Func_finland_eu_tax_file_number` encontra conteúdo que corresponde ao padrão. 
    
- Uma palavra-chave da `Keywords_finland_eu_tax_file_number` for encontrado. 
    
Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:
  
- A função `Func_finland_eu_tax_file_number` encontra conteúdo que corresponde ao padrão. 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_finland_eu_tax_file_number" />
          <Match idRef="Keywords_finland_eu_tax_file_number" />
        </Pattern>
<Pattern confidenceLevel="75">
          <IdMatch idRef="Func_finland_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Palavras-chave

#### <a name="keywordsfinlandeutaxfilenumber"></a>Keywords_finland_eu_tax_file_number

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
  
## <a name="france"></a>França

### <a name="format"></a>Formato

13 dígitos dos indivíduos e nove dígitos para entidades
  
### <a name="pattern"></a>Padrão

13 dígitos para as pessoas:
  
- Um dígito que deve ser 0, 1, 2 ou 3
    
- 12 dígitos
    
Nove dígitos para entidades
  
### <a name="checksum"></a>Soma de verificação

Não aplicável
  
### <a name="definition"></a>Definição

Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:
  
- A função `Func_france_eu_tax_file_number` encontra conteúdo que corresponde ao padrão. 
    
- Uma palavra-chave da `Keywords_france_eu_tax_file_number` for encontrado. 
    
Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:
  
- A função `Func_france_eu_tax_file_number` encontra conteúdo que corresponde ao padrão. 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_france_eu_tax_file_number" />
          <Match idRef="Keywords_france_eu_tax_file_number" />
        </Pattern>
 <Pattern confidenceLevel="75">
          <IdMatch idRef="Func_france_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Palavras-chave

#### <a name="keywordsfranceeutaxfilenumber"></a>Keywords_france_eu_tax_file_number

número de identificação de imposto
  
número de imposto
  
tax id

  
numéro d'identification fiscale
  
## <a name="germany"></a>Alemanha

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
  
- A função `Func_germany_eu_tax_file_number` encontra conteúdo que corresponde ao padrão. 
    
- Uma palavra-chave da `Keywords_germany_eu_tax_file_number` for encontrado. 
    
Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:
  
- A função `Func_germany_eu_tax_file_number` encontra conteúdo que corresponde ao padrão. 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_germany_eu_tax_file_number" />
          <Match idRef="Keywords_germany_eu_tax_file_number" />
        </Pattern>
<Pattern confidenceLevel="75">
          <IdMatch idRef="Func_germany_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Palavras-chave

#### <a name="keywordsgermanyeutaxfilenumber"></a>Keywords_germany_eu_tax_file_number

número de imposto
  
imposto não.
  
taxno #
  
taxnumber #
  
taxnumber
  
tax id

  
taxid #
  
número de identificação de imposto
  
identificação de imposto não.
  
steuernummer
  
id de steuer
  
steueridentifikationsnummer
  
## <a name="greece"></a>Grécia

### <a name="format"></a>Formato

Nove dígitos sem espaços e delimitadores
  
### <a name="pattern"></a>Padrão

Nove dígitos
  
### <a name="checksum"></a>Soma de verificação

Não aplicável
  
### <a name="definition"></a>Definição

Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:
  
- A expressão regular `Regex_greece_eu_tax_file_number` encontra conteúdo que corresponde ao padrão. 
    
- Uma palavra-chave da `Keywords_greece_eu_tax_file_number` for encontrado. 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_greece_eu_tax_file_number" />
          <Match idRef="Keywords_greece_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Palavras-chave

#### <a name="keywordsgreeceeutaxfilenumber"></a>Keywords_greece_eu_tax_file_number

AFM
  
tin

  
id de imposto não.
  
id de imposto não
  
número de identificação de imposto
  
número de registro de imposto
  
imposto do registro não.
  
AFM #
  
TIN #
  
taxidno #
  
taxregistryno #
  
ΑΡΙΘΜΌΣ ΦΟΡΟΛΟΓΙΚΟΎ ΜΗΤΡΏΟΥ
  
aφμ
  
aφμ αριθμός
  
ΝΟ DE ΜΗΤΡΏΟΥ ΦΟΡΟΛΟΓΙΚΟΎ.
  
ΤΟΝ ΑΡΙΘΜΌ ΦΟΡΟΛΟΓΙΚΟΎ ΜΗΤΡΏΟΥ
  
## <a name="hungary"></a>Hungria

### <a name="format"></a>Formato

Dez dígitos sem espaços ou delimitadores
  
### <a name="pattern"></a>Padrão

Dez dígitos:
  
-  Um dígito que deve estar "8" 
    
- Cinco dígitos que corresponde ao número de dias entre a data 01/01/1867 e a data do nascimento do indivíduo
    
- Três dígitos que corresponde ao número gerado por acaso para diferenciar indivíduos nascidos no mesmo dia
    
- Seleção de um dígito
    
### <a name="checksum"></a>Soma de verificação

Sim
  
### <a name="definition"></a>Definição

Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:
  
- A função `Func_hungary_eu_tax_file_number` encontra conteúdo que corresponde ao padrão. 
    
- Uma palavra-chave da `Keywords_hungary_eu_tax_file_number` for encontrado. 
    
Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:
  
- A função `Func_hungary_eu_tax_file_number` encontra conteúdo que corresponde ao padrão. 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_hungary_eu_tax_file_number" />
          <Match idRef="Keywords_hungary_eu_tax_file_number" />
        </Pattern>
<Pattern confidenceLevel="75">
          <IdMatch idRef="Func_hungary_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Palavras-chave

#### <a name="keywordshungaryeutaxfilenumber"></a>Keywords_hungary_eu_tax_file_number

número de identificação de imposto húngaro
  
tin húngaro
  
número de identificação de imposto
  
número VAT
  
autoridade de fiscal não
  
número de identidade de imposto de id de imposto
  
taxidnumber #
  
TIN #
  
hungatiantin #
  
identificação de imposto não
  
taxidno #
  
adóazonosító szám
  
adószám
  
adóhatóság szám
  
## <a name="ireland"></a>Irlanda

### <a name="format"></a>Formato

Sete dígitos, seguidos por uma letra sem espaços ou delimitadores
  
### <a name="pattern"></a>Padrão

Sete dígitos seguidos por uma letra:
  
-  Sete dígitos  
    
- Uma letra (não diferencia maiusculas de minúsculas)
    
### <a name="checksum"></a>Soma de verificação

Não aplicável
  
### <a name="definition"></a>Definição

Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:
  
- A função `Func_ireland_eu_tax_file_number` encontra conteúdo que corresponde ao padrão. 
    
- Uma palavra-chave da `Keywords_ireland_eu_tax_file_number` for encontrado. 
    
Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:
  
- A função `Func_ireland_eu_tax_file_number` encontra conteúdo que corresponde ao padrão. 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_ireland_eu_tax_file_number" />
          <Match idRef="Keywords_ireland_eu_tax_file_number" />
        </Pattern>
<Pattern confidenceLevel="75">
          <IdMatch idRef="Func_ireland_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Palavras-chave

#### <a name="keywordsirelandeutaxfilenumber"></a>Keywords_ireland_eu_tax_file_number

serviço público nenhum
  
serviço de público pessoal nenhum
  
PPS nenhum
  
pessoal de serviço não
  
PPS pessoal não
  
ppsno #
  
Irlandês pps nenhum
  
publicserviceno #
  
número de serviço pessoal de público
  
uimhir phearsanta seirbhíse poiblí
  
uimh PPS
  
uimhir aitheantais phearsanta
  
## <a name="italy"></a>Itália

### <a name="format"></a>Formato

16 letras e dígitos no padrão especificado
  
### <a name="pattern"></a>Padrão

16 letras e dígitos:
  
-  Três letras que correspondem às três primeiros consoantes no nome da família 
    
- Três letras que correspondem à primeira, terceira e quarta consoantes no primeiro nome de usuário
    
- Dois dígitos que correspondem à última dígitos do ano nascimento
    
- Um dígito que corresponde ao mês de nascimento — letras são usadas em ordem alfabética, mas apenas as letras de a F, R, L, M, P, R para T são usadas (assim, janeiro é uma e outubro é R)
    
- Dois dígitos que correspondem ao dia do mês de nascimento onde 40 é adicionado ao dia de nascimento para mulheres diferenciar dos homens
    
- Quatro dígitos que correspondem a um código de área específico para o município onde a pessoa surgiu — códigos de todo o país são usados para países estrangeiros
    
- Seleção de um dígito
    
### <a name="checksum"></a>Soma de verificação

Sim
  
### <a name="definition"></a>Definição

Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:
  
- A função `Func_italy_eu_tax_file_number` encontra conteúdo que corresponde ao padrão. 
    
- Uma palavra-chave da `Keywords_italy_eu_tax_file_number` for encontrado. 
    
Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:
  
- A função `Func_italy_eu_tax_file_number` encontra conteúdo que corresponde ao padrão. 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_italy_eu_tax_file_number" />
          <Match idRef="Keywords_italy_eu_tax_file_number" />
        </Pattern>
<Pattern confidenceLevel="75">
          <IdMatch idRef="Func_italy_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Palavras-chave

#### <a name="keywordsitalyeutaxfilenumber"></a>Keywords_italy_eu_tax_file_number

número de imposto
  
imposto não.
  
taxno #
  
taxnumber #
  
taxnumber
  
tax id

  
taxid #
  
código fiscal
  
codice fiscale
  
## <a name="latvia"></a>Letônia

### <a name="format"></a>Formato

11 dígitos sem espaços ou delimitadores
  
### <a name="pattern"></a>Padrão

11 dígitos no padrão especificado
  
-  Seis dígitos que correspondem à data de nascimento (DDMMYY) 
    
- Um dígito que corresponde do century de nascimento onde "0" corresponde ao décimo nono century, corresponde "1" como century 20 e "2" corresponde a century 21
    
- Quatro dígitos
    
### <a name="checksum"></a>Soma de verificação

Sim
  
### <a name="definition"></a>Definição

Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:
  
- A função `Func_latvia_eu_tax_file_number` encontra conteúdo que corresponde ao padrão. 
    
- Uma palavra-chave da `Keywords_latvia_eu_tax_file_number` for encontrado. 
    
Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:
  
- A função `Func_latvia_eu_tax_file_number` encontra conteúdo que corresponde ao padrão. 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_latvia_eu_tax_file_number" />
          <Match idRef="Keywords_latvia_eu_tax_file_number" />
        </Pattern>
<Pattern confidenceLevel="75">
          <IdMatch idRef="Func_latvia_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Palavras-chave

#### <a name="keywordslatviaeutaxfilenumber"></a>Keywords_latvia_eu_tax_file_number

número de imposto
  
imposto não.
  
taxno #
  
taxnumber #
  
taxnumber
  
tax id

  
taxid #
  
número de identificação de imposto
  
identificação de imposto não.
  
nodokļa numurs
  
nodokļu identifikācijas numurs
  
nodokļu identifikācija numurs
  
## <a name="lithuania"></a>Lituânia

### <a name="format"></a>Formato

11 dígitos sem espaços ou delimitadores
  
### <a name="pattern"></a>Padrão

11 dígitos
  
### <a name="checksum"></a>Soma de verificação

Não aplicável
  
### <a name="definition"></a>Definição

Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:
  
- A função `Func_lithuania_eu_tax_file_number` encontra conteúdo que corresponde ao padrão. 
    
- Uma palavra-chave da `Keywords_lithuania_eu_tax_file_number` for encontrado. 
    
Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:
  
- A função `Func_lithuania_eu_tax_file_number` encontra conteúdo que corresponde ao padrão. 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_lithuania_eu_tax_file_number" />
          <Match idRef="Keywords_lithuania_eu_tax_file_number" />
        </Pattern>
<Pattern confidenceLevel="75">
          <IdMatch idRef="Func_lithuania_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Palavras-chave

#### <a name="keywordslithuaniaeutaxfilenumber"></a>Keywords_lithuania_eu_tax_file_number

número de imposto
  
imposto não.
  
imposto não #
  
taxnumber #
  
taxnumber
  
tax id

  
taxid #
  
número de identificação de imposto
  
identificação de imposto não.
  
id de mokesčių
  
mokesčių numeris
  
mokesčių identifikavimas numeris
  
## <a name="luxemburg"></a>Luxemburgo

### <a name="format"></a>Formato

13 dígitos sem espaços ou delimitadores
  
### <a name="pattern"></a>Padrão

13 dígitos:
  
-  11 dígitos 
    
- Dois dígitos de verificação
    
### <a name="checksum"></a>Soma de verificação

Sim
  
### <a name="definition"></a>Definição

Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:
  
- A função `Func_luxemburg_eu_tax_file_number` encontra conteúdo que corresponde ao padrão. 
    
- Uma palavra-chave da `Keywords_luxemburg_eu_tax_file_number` for encontrado. 
    
Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:
  
- A função `Func_luxemburg_eu_tax_file_number` encontra conteúdo que corresponde ao padrão. 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_luxemburg_eu_tax_file_number" />
          <Match idRef="Keywords_luxemburg_eu_tax_file_number" />
        </Pattern>
<Pattern confidenceLevel="75">
          <IdMatch idRef="Func_luxemburg_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Palavras-chave

#### <a name="keywordsluxemburgeutaxfilenumber"></a>Keywords_luxemburg_eu_tax_file_number

número de imposto
  
imposto não.
  
taxno #
  
taxnumber #
  
taxnumber
  
tax id

  
taxid #
  
número de identificação de imposto
  
identificação de imposto não.
  
steuernummer
  
id de steuer
  
steueridentifikationsnummer
  
## <a name="malta"></a>Malta

### <a name="format"></a>Formato

Para cidadãos Maltês: 7 dígitos e uma letra no padrão especificado
  
Não-Maltês cidadãos e entidades Maltês: 9 dígitos
  
### <a name="pattern"></a>Padrão

Maltês cidadãos: 7 dígitos e uma letra
  
-  Sete dígitos  
    
- Uma letra (não diferencia maiusculas de minúsculas)
    
Não-Maltês cidadãos e entidades Maltês: 9 dígitos
  
-  Nove dígitos 
    
### <a name="checksum"></a>Soma de verificação

Não aplicável
  
### <a name="definition"></a>Definição

Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:
  
- A função `Func_malta_eu_tax_file_number` encontra conteúdo que corresponde ao padrão. 
    
- Uma palavra-chave da `Keywords_malta_eu_tax_file_number` for encontrado. 
    
Uma política de DLP tem 65% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:
  
- A função `Func_malta_eu_tax_file_number` encontra conteúdo que corresponde ao padrão. 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Func_malta_eu_tax_file_number" />
          <Match idRef="Keywords_malta_eu_tax_file_number" />
        </Pattern>
<Pattern confidenceLevel="65">
          <IdMatch idRef="Regex_malta_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Palavras-chave

#### <a name="keywordsmaltaeutaxfilenumber"></a>Keywords_malta_eu_tax_file_number

número de imposto
  
imposto não.
  
taxno #
  
taxnumber #
  
taxnumber
  
tax id

  
taxid #
  
número de identificação de imposto
  
identificação de imposto não.
  
numru tat-taxxa
  
ID tat-taxxa
  
numru guias ' identifikazzjoni tat-taxxa
  
## <a name="netherlands"></a>Países Baixos

### <a name="format"></a>Formato

Nove dígitos sem espaços ou delimitadores
  
### <a name="pattern"></a>Padrão

Nove dígitos 
  
### <a name="checksum"></a>Soma de verificação

Sim
  
### <a name="definition"></a>Definição

Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:
  
- A função `Func_netherlands_eu_tax_file_number` encontra conteúdo que corresponde ao padrão. 
    
- Uma palavra-chave da `Keywords_netherlands_eu_tax_file_number` for encontrado. 
    
Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:
  
- A função `Func_netherlands_eu_tax_file_number` encontra conteúdo que corresponde ao padrão. 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_netherlands_eu_tax_file_number" />
          <Match idRef="Keywords_netherlands_eu_tax_file_number" />
        </Pattern>
<Pattern confidenceLevel="75">
          <IdMatch idRef="Func_netherlands_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Palavras-chave

#### <a name="keywordsnetherlandseutaxfilenumber"></a>Keywords_netherlands_eu_tax_file_number

número de identificação de imposto países baixos
  
identificação de imposto países baixos
  
número de identificação do Antilhas imposto
  
identificação de imposto do Antilhas
  
número de identificação de imposto
  
id de imposto holandês
  
número de identificação de imposto holandês
  
tax id

  
n º fiscal
  
número de imposto
  
imposto não #
  
imposto #
  
tin

  
TIN #
  
tin países baixos
  
tin do Antilhas
  
Holanda belasting identificatienummer
  
identificatienummer van belasting
  
identificatienummer belasting
  
Holanda belasting identificatie
  
Holanda belasting id nummer
  
Holanda belastingnummer
  
btw nummer
  
nederlandse belasting identificatie
  
## <a name="poland"></a>Polônia

### <a name="format"></a>Formato

Onze dígitos sem espaços ou delimitadores
  
### <a name="pattern"></a>Padrão

Onze dígitos
  
### <a name="checksum"></a>Soma de verificação

Sim
  
### <a name="definition"></a>Definição

Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:
  
- A função `Func_poland_eu_tax_file_number` encontra conteúdo que corresponde ao padrão. 
    
- Uma palavra-chave da `Keywords_poland_eu_tax_file_number` for encontrado. 
    
Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:
  
- A função `Func_poland_eu_tax_file_number` encontra conteúdo que corresponde ao padrão. 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_poland_eu_tax_file_number" />
          <Match idRef="Keywords_poland_eu_tax_file_number" />
        </Pattern>
<Pattern confidenceLevel="75">
          <IdMatch idRef="Func_poland_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Palavras-chave

#### <a name="keywordspolandeutaxfilenumber"></a>Keywords_poland_eu_tax_file_number

número de imposto
  
imposto não.
  
taxno #
  
taxnumber #
  
taxnumber
  
NIP
  
NIP #
  
tax id

  
n º fiscal
  
id de NIP
  
id de NIP #
  
número de identificação de imposto
  
identificação de imposto não.
  
número VAT
  
IVA não.
  
vatno #
  
id de VAT
  
id de VAT #
  
número identyfikacji podatkowej
  
Polski número identyfikacji podatkowej
  
numeridentyfikacjipodatkowej #
  
## <a name="portugal"></a>Portugal

### <a name="format"></a>Formato

Nove dígitos sem espaços ou delimitadores
  
### <a name="pattern"></a>Padrão

Nove dígitos
  
### <a name="checksum"></a>Soma de verificação

Sim
  
### <a name="definition"></a>Definição

Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:
  
- A função `Func_portugal_eu_tax_file_number` encontra conteúdo que corresponde ao padrão. 
    
- Uma palavra-chave da `Keywords_portugal_eu_tax_file_number` for encontrado. 
    
Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:
  
- A função `Func_portugal_eu_tax_file_number` encontra conteúdo que corresponde ao padrão. 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_portugal_eu_tax_file_number" />
          <Match idRef="Keywords_portugal_eu_tax_file_number" />
        </Pattern>
<Pattern confidenceLevel="75">
          <IdMatch idRef="Func_portugal_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Palavras-chave

#### <a name="keywordsportugaleutaxfilenumber"></a>Keywords_portugal_eu_tax_file_number

número de imposto
  
imposto não.
  
taxno #
  
taxnumber #
  
taxnumber
  
NIF
  
NIF #
  
numero fiscal
  
número de identificação fiscal
  
## <a name="romania"></a>Romênia

### <a name="format"></a>Formato

13 dígitos sem espaços ou delimitadores
  
### <a name="pattern"></a>Padrão

13 dígitos
  
### <a name="checksum"></a>Soma de verificação

Não aplicável
  
### <a name="definition"></a>Definição

Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:
  
- A expressão regular `Regex_romania_eu_tax_file_number` encontra conteúdo que corresponde ao padrão. 
    
- Uma palavra-chave da `Keywords_romania_eu_tax_file_number` for encontrado. 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_romania_eu_tax_file_number" />
          <Match idRef="Keywords_romania_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Palavras-chave

#### <a name="keywordsromaniaeutaxfilenumber"></a>Keywords_romania_eu_tax_file_number

tax id

  
número de identificação de imposto
  
arquivo do imposto não
  


tax file number
  
imposto não
  
número de imposto
  
taxid #
  
taxno #
  
ID-ul taxei
  
numărul de identificare fiscală
  
## <a name="slovakia"></a>Eslováquia

### <a name="format"></a>Formato

10 dígitos sem espaços ou delimitadores
  
### <a name="pattern"></a>Padrão

10 dígitos
  
### <a name="checksum"></a>Soma de verificação

Não aplicável
  
### <a name="definition"></a>Definição

Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:
  
- A expressão regular `Regex_slovakia_eu_tax_file_number` encontra conteúdo que corresponde ao padrão. 
    
- Uma palavra-chave da `Keywords_slovakia_eu_tax_file_number` for encontrado. 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_slovakia_eu_tax_file_number" />
          <Match idRef="Keywords_slovakia_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Palavras-chave

#### <a name="keywordsslovakiaeutaxfilenumber"></a>Keywords_slovakia_eu_tax_file_number

tax id

  
número de identificação de imposto
  
id de estanho
  
não estanho
  
id de estanho eslovaco
  
tin

  
arquivo do imposto não
  


tax file number
  
imposto não
  
número de imposto
  
taxid #
  
taxno #
  
daňové identifikačné číslo
  
daňové číslo
  
daňové číslo súboru
  
## <a name="slovenia"></a>Eslovênia

### <a name="format"></a>Formato

Oito dígitos sem espaços ou delimitadores
  
### <a name="pattern"></a>Padrão

Oito dígitos
  
### <a name="checksum"></a>Soma de verificação

Sim
  
### <a name="definition"></a>Definição

Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:
  
- A função `Func_slovenia_eu_tax_file_number` encontra conteúdo que corresponde ao padrão. 
    
- Uma palavra-chave da `Keywords_slovenia_eu_tax_file_number` for encontrado. 
    
Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:
  
- A função `Func_slovenia_eu_tax_file_number` encontra conteúdo que corresponde ao padrão. 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_nation_eu_tax_file_number" />
          <Match idRef="Keywords_nation_eu_tax_file_number" />
        </Pattern>
<Pattern confidenceLevel="75">
          <IdMatch idRef="Func_slovenia_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Palavras-chave

#### <a name="keywordssloveniaeutaxfilenumber"></a>Keywords_slovenia_eu_tax_file_number

tax id

  
número de identificação de imposto
  
id de estanho
  
não estanho
  
id de estanho esloveno
  
tin

  
arquivo do imposto não
  


tax file number
  
imposto não
  
número de imposto
  
taxid #
  
taxno #
  
identifikacijska številka davka
  
davčna številka
  
Številka davčne datoteke
  
## <a name="spain"></a>Espanha

### <a name="format"></a>Formato

Sete ou oito dígitos e uma ou duas letras no padrão especificado
  
### <a name="pattern"></a>Padrão

Espanholas Natural as pessoas com um cartão de identificação nacional da Espanha:
  
-  Oito dígitos 
    
- Uma letra maiuscula (diferencia maiusculas de minúsculas) 
    
Não residente Spaniards sem um cartão de identificação nacional da Espanha
  
- Uma letra maiuscula "L" (diferencia maiusculas de minúsculas)
    
- Sete dígitos 
    
- Uma letra maiuscula (diferencia maiusculas de minúsculas) 
    
Spaniards residente sob a idade dos 14 anos sem um Espanha nacional identidade cartão:
  
- Uma letra maiuscula "K" (diferencia maiusculas de minúsculas)
    
-  Sete dígitos  
    
- Uma letra maiuscula (diferencia maiusculas de minúsculas)
    
Estrangeiros com número de identificação de um Foreigner
  
- Letras maiusculas uma letra ou seja "X", "Y" ou "Z" (diferencia maiusculas de minúsculas) 
    
- Sete dígitos 
    
- Uma letra maiuscula (diferencia maiusculas de minúsculas) 
    
Estrangeiros sem número de identificação de um Foreigner
  
- Uma letra maiuscula que é "M" (diferencia maiusculas de minúsculas) 
    
- Sete dígitos 
    
- Uma letra maiuscula (diferencia maiusculas de minúsculas) 
    
### <a name="checksum"></a>Soma de verificação

Sim
  
### <a name="definition"></a>Definição

Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:
  
- A função `Func_spain_eu_tax_file_number` encontra conteúdo que corresponde ao padrão. 
    
- Uma palavra-chave da `Keywords_spain_eu_tax_file_number` for encontrado. 
    
Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:
  
- A função `Func_spain_eu_tax_file_number` encontra conteúdo que corresponde ao padrão. 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_spain_eu_tax_file_number" />
          <Match idRef="Keywords_spain_eu_tax_file_number" />
        </Pattern>
<Pattern confidenceLevel="75">
          <IdMatch idRef="Func_spain_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Palavras-chave

#### <a name="keywordsspaineutaxfilenumber"></a>Keywords_spain_eu_tax_file_number

tax id

  
número de identificação de imposto
  
id de CIF
  
CIF nenhum
  
id do espanhol cif
  
CIF
  
arquivo do imposto não
  
número de cif espanhol
  


tax file number
  
Espanhol cif nenhum
  
imposto não
  
número de imposto
  
taxid #
  
taxno #
  
cifid #
  
spanishcifid #
  
spanishcifno #
  
número de contribuyente
  
número de impuesto corporativo
  
número de identificación fiscal
  
número de CIF
  
cifnúmero #
  
## <a name="sweden"></a>Suécia

### <a name="format"></a>Formato

Dez dígitos e um símbolo no padrão especificado
  
### <a name="pattern"></a>Padrão

Dez dígitos e um símbolo:
  
-  Seis dígitos que correspondem à data de nascimento (aammdd) 
    
- Um sinal de adição, sinal de subtração ou barra invertida
    
- Três dígitos que tornam a identificação do número exclusivo where: 
    
  - Para números emitidos antes de 1990, o sétimo e oitavo dígito identificar a região de nascimento ou foreign-born pessoas
    
  - O dígito na posição mais à nono indica gênero por qualquer um dos ímpares para Masculino ou até mesmo fêmea
    
- Seleção de um dígito
    
### <a name="checksum"></a>Soma de verificação

Sim
  
### <a name="definition"></a>Definição

Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:
  
- A função `Func_sweden_eu_tax_file_number` encontra conteúdo que corresponde ao padrão. 
    
- Uma palavra-chave da `Keywords_sweden_eu_tax_file_number` for encontrado. 
    
Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:
  
- A função `Func_sweden_eu_tax_file_number` encontra conteúdo que corresponde ao padrão. 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_sweden_eu_tax_file_number" />
          <Match idRef="Keywords_sweden_eu_tax_file_number" />
        </Pattern>
<Pattern confidenceLevel="75">
          <IdMatch idRef="Func_sweden_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Palavras-chave

#### <a name="keywordsswedeneutaxfilenumber"></a>Keywords_sweden_eu_tax_file_number

tax id

  
id de imposto não.
  
número de identificação de imposto
  
tax identification

  
identificação de imposto #
  
imposto não.
  
imposto #
  
taxid #
  
arquivo impostos
  
imposto não o arquivo.
  
número de identificação pessoal
  
skatt id nummer
  
skatt identifikation
  
personnummer
  
## <a name="uk"></a>REINO UNIDO

### <a name="format"></a>Formato

Referência de contribuinte exclusivo (UTR): 10 dígitos sem espaços e delimitadores
  
Número de seguro de Nacional (NINO): Para obter detalhes, consulte a seção "número de Insurance nacional da Reino Unido (NINO)" em [quais tipos de informações confidenciais a procurar](what-the-sensitive-information-types-look-for.md).
  
### <a name="pattern"></a>Padrão

Referência de contribuinte exclusivo (UTR): 10 dígitos
  
Número de seguro de Nacional (NINO): Para obter detalhes, consulte a seção "número de Insurance nacional da Reino Unido (NINO)" em [quais tipos de informações confidenciais a procurar](what-the-sensitive-information-types-look-for.md).
  
### <a name="checksum"></a>Soma de verificação

Sim
  
### <a name="definition"></a>Definição

Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:
  
- A função `Func_uk_eu_tax_file_number` encontra conteúdo que corresponde ao padrão. 
    
- Uma palavra-chave da `Keywords_uk_eu_tax_file_number` for encontrado. 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Func_uk_eu_tax_file_number" />
          <Match idRef="Keywords_uk_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Palavras-chave

#### <a name="keywordsukeutaxfilenumber"></a>Keywords_uk_eu_tax_file_number

tax id

  
id de imposto não.
  
número de identificação de imposto
  
tax identification

  
identificação de imposto #
  
imposto não.
  
imposto #
  
taxid #
  
arquivo impostos
  
imposto não o arquivo.
  
## <a name="see-also"></a>Confira também

[O que os tipos de informações confidenciais procuram](what-the-sensitive-information-types-look-for.md)

