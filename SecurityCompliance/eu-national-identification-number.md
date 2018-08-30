---
title: Número de identificação nacional da UE
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: 8/17/2018
ms.audience: Admin
ms.topic: reference
ms.service: o365-administration
localization_priority: Normal
ms.assetid: 2ea971bf-9434-4b61-b825-2bbd28ae6064
description: Este tópico mostra o que uma política de prevenção (DLP) de perda de dados procura por quando detecta o tipo de informações confidenciais de número de identificação nacional da UE. Esse tipo de informações confidenciais define diferentes padrões, palavras-chave e outras evidências para cada país.
ms.openlocfilehash: 29d2126b937ff46039284a74eb2a84f2ebbacb41
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22523996"
---
# <a name="eu-national-identification-number"></a>Número de identificação nacional da UE

Este tópico mostra o que uma política de prevenção (DLP) de perda de dados procura por quando detecta o tipo de informações confidenciais de número de identificação nacional da UE. Esse tipo de informações confidenciais define diferentes padrões, palavras-chave e outras evidências para cada país.
  
## <a name="austria"></a>Áustria

### <a name="format"></a>Formato

Uma combinação de 24 caracteres de letras, dígitos e caracteres especiais
  
### <a name="pattern"></a>Padrão

24 de caracteres:
  
-  22 letras (não diferencia maiusculas de minúsculas), dígitos, barras invertidas, barras ou sinais de adição 
    
- (Não diferencia maiusculas de minúsculas) de duas letras, dígitos, barras invertidas, barras, sinais de adição ou sinais de igual
    
### <a name="checksum"></a>Soma de verificação

Não aplicável
  
### <a name="definition"></a>Definição

Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:
  
- A expressão regular `Regex_austria_eu_national_id_card` encontra conteúdo que corresponde ao padrão. 
    
- Uma palavra-chave da `Keywords_austria_eu_national_id_card` for encontrado. 
    
```
 
<Entity id="419f449f-6d9d-4be1-a154-b531f7a91b41" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_austria_eu_national_id_card" />
          <Match idRef="Keywords_austria_eu_national_id_card" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Palavras-chave

#### <a name="keywordsaustriaeunationalidcard"></a>Keywords_austria_eu_national_id_card

número de identidade austríaco
  
número de identidade nacional
  
número de identidade
  

national id
  
personalausweis republik österreich
  
## <a name="belgium"></a>Bélgica

Para obter detalhes, consulte a seção "Bélgica nacional Number" em [quais tipos de informações confidenciais a procurar](what-the-sensitive-information-types-look-for.md).
  
## <a name="bulgaria"></a>Bulgária

### <a name="format"></a>Formato

Dez dígitos sem espaços e delimitadores
  
### <a name="pattern"></a>Padrão

Dez dígitos sem espaços e delimitadores
  
-  Seis dígitos que correspondem à data de nascimento (aammdd) 
    
- Dois dígitos correspondentes na ordem de nascimento
    
- Um dígito que corresponde ao gênero: um dígito par de masculino e um dígito ímpar para fêmea
    
- Seleção de um dígito
    
### <a name="checksum"></a>Soma de verificação

Sim
  
### <a name="definition"></a>Definição

Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:
  
- A função `Func_bulgaria_national_number` encontra conteúdo que corresponde ao padrão. 
    
- Uma palavra-chave da `Keywords_bulgaria_national_number` for encontrado. 
    
Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:
  
- A função `Func_bulgaria_national_number` encontra conteúdo que corresponde ao padrão. 
    
```
<Entity id="419f449f-6d9d-4be1-a154-b531f7a91b41" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_bulgaria_national_number" />
          <Match idRef="Keywords_bulgaria_national_number" />
        </Pattern>
<Pattern confidenceLevel="75">
          <IdMatch idRef="Func_bulgaria_eu_national_id_card" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Palavras-chave

#### <a name="keywordsbulgarianationalnumber"></a>Keywords_bulgaria_national_number

egn
  
egn #
  
número nacional búlgaro
  
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
  
ЕДИНЕН ГРАЖДАНСКИ НОМЕР
  
edinen grazhdanski nomer
  
ЕГН
  
ЕГН #
  
## <a name="croatia"></a>Croácia

Para obter detalhes, consulte a seção "Croácia identidade Number" em [quais tipos de informações confidenciais a procurar](what-the-sensitive-information-types-look-for.md).
  
## <a name="cyprus"></a>Chipre

### <a name="format"></a>Formato

Dez dígitos sem espaços e delimitadores
  
### <a name="pattern"></a>Padrão

 Dez dígitos 
  
### <a name="checksum"></a>Soma de verificação

Não aplicável
  
### <a name="definition"></a>Definição

Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:
  
- A expressão regular `Regex_cyprus_eu_national_id_card` encontra conteúdo que corresponde ao padrão. 
    
- Uma palavra-chave da `Keywords_cyprus_eu_national_id_card` for encontrado. 
    
```
 
<Entity id="419f449f-6d9d-4be1-a154-b531f7a91b41" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_cyprus_eu_national_id_card" />
          <Match idRef="Keywords_cyprus_eu_national_id_card" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Palavras-chave

#### <a name="keywordscypruseunationalidcard"></a>Keywords_cyprus_eu_national_id_card

número de cartão de identificação
  
número de identificação nacional
  
número de identificação pessoal
  
número de cartão de identificação
  
ΤΑΥΤΟΤΗΤΑΣ
  
## <a name="czech-republic"></a>República Tcheca

Para obter detalhes, consulte a seção "Tcheco nacional identidade Number" em [quais tipos de informações confidenciais a procurar](what-the-sensitive-information-types-look-for.md).
  
## <a name="denmark"></a>Dinamarca

Para obter detalhes, consulte a seção "Dinamarca número de identificação pessoal" nos [quais os tipos de informações confidenciais procurar](what-the-sensitive-information-types-look-for.md).
  
## <a name="estonia"></a>Estônia

### <a name="format"></a>Formato

11 dígitos sem espaços e delimitadores
  
### <a name="pattern"></a>Padrão

11 dígitos:
  
- Um dígito que corresponde ao sexo e century de nascimento (Masculino número ímpar, o número de par feminino; 1-2: 19 century; 3 e 4: 20 century; 5-6: 21 century)
    
- Seis dígitos que correspondem à data de nascimento (aammdd)
    
- Três dígitos que correspondem a um número de série separando pessoas nascidas na mesma data
    
- Seleção de um dígito
    
### <a name="checksum"></a>Soma de verificação

Sim
  
### <a name="definition"></a>Definição

Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:
  
- A função `Func_estonia_eu_national_id_card` encontra conteúdo que corresponde ao padrão. 
    
- Uma palavra-chave da `Keywords_estonia_eu_national_id_card` for encontrado. 
    
Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:
  
- A função `Func_estonia_eu_national_id_card` encontra conteúdo que corresponde ao padrão. 
    
```
 
<Entity id="419f449f-6d9d-4be1-a154-b531f7a91b41" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_estonia_eu_national_id_card" />
          <Match idRef="Keywords_estonia_eu_national_id_card" />
        </Pattern>
<Pattern confidenceLevel="75">
          <IdMatch idRef="Func_estonia_eu_national_id_card" />
</Pattern>
</Entity>
```

### <a name="keywords"></a>Palavras-chave

#### <a name="keywordsestoniaeunationalidcard"></a>Keywords_estonia_eu_national_id_card

código de identificação pessoal
  
número de identificação pessoal
  
número de identificação nacional
  
número nacional
  
número de identificação pessoal
  
personalidnumber #
  
IK
  
isikukood
  
ID-kaart
  
## <a name="finland"></a>Finlândia

Para obter detalhes, consulte a seção "ID nacional da Finlândia" nos [quais os tipos de informações confidenciais procurar](what-the-sensitive-information-types-look-for.md).
  
## <a name="france"></a>França

Para obter detalhes, consulte a seção "França nacional cartão de identificação (CNI)" em [quais tipos de informações confidenciais a procurar](what-the-sensitive-information-types-look-for.md).
  
## <a name="germany"></a>Alemanha

Para obter detalhes, consulte a seção "Número de cartão de identificação da Alemanha" em [quais tipos de informações confidenciais a procurar](what-the-sensitive-information-types-look-for.md).
  
## <a name="greece"></a>Grécia

Para obter detalhes, consulte a seção "Grécia cartão de identificação nacional" nos [quais os tipos de informações confidenciais procurar](what-the-sensitive-information-types-look-for.md).
  
## <a name="hungary"></a>Hungria

### <a name="format"></a>Formato

11 dígitos
  
### <a name="pattern"></a>Padrão

11 dígitos:
  
-  Um dígito que corresponde ao gênero (Masculino-1, 2-fêmea, outros números também são possíveis para cidadãos nascidos antes de 1900 ou cidadãos com ações sociais double) 
    
- Seis dígitos que correspondem à data de nascimento (aammdd)
    
- Três dígitos que correspondem a um número de série
    
- Seleção de um dígito
    
### <a name="checksum"></a>Soma de verificação

Sim
  
### <a name="definition"></a>Definição

Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:
  
- A função `Func_hungary_eu_national_id_card` encontra conteúdo que corresponde ao padrão. 
    
- Uma palavra-chave da `Keywords_hungary_eu_national_id_card` for encontrado. 
    
Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:
  
- A função `Func_hungary_eu_national_id_card` encontra conteúdo que corresponde ao padrão. 
    
```
<Entity id="419f449f-6d9d-4be1-a154-b531f7a91b41" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_hungary_eu_national_id_card" />
          <Match idRef="Keywords_hungary_eu_national_id_card" />
        </Pattern>
<Pattern confidenceLevel="75">
          <IdMatch idRef="Func_hungary_eu_national_id_card" />
</Pattern>
</Entity>
```

### <a name="keywords"></a>Palavras-chave

#### <a name="keywordshungaryeunationalidcard"></a>Keywords_hungary_eu_national_id_card

número de identificação pessoal
  
identification number

  
número de identificação pessoal
  
személyazonosító igazolvány
  
## <a name="ireland"></a>Irlanda

### <a name="format"></a>Formato

Uma combinação de nove caracteres de letras, dígitos e um espaço no padrão especificado
  
### <a name="pattern"></a>Padrão

Uma combinação de nove caracteres de letras, dígitos e um espaço no padrão especificado
  
A partir de 01 de janeiro de 2013 para now:
  
-  Sete dígitos  
    
- Seleção de um dígito
    
- Um espaço ou a letra maiuscula "W" (com distinção entre maiusculas e minúsculas)
    
Antes de 01 de janeiro de 2013:
  
-  Sete dígitos  
    
- Seleção de um dígito
    
- Um espaço ou uma letra maiuscula (diferenciar maiusculas de minúsculas)
    
### <a name="checksum"></a>Soma de verificação

Sim
  
### <a name="definition"></a>Definição

Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:
  
- A função encontra o conteúdo que corresponde ao padrão.
    
- Uma palavra-chave da é encontrada.
    
Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:
  
- A função encontra o conteúdo que corresponde ao padrão.
    
```
 
<Entity id="419f449f-6d9d-4be1-a154-b531f7a91b41" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_ireland_eu_national_id_card" />
          <Match idRef="Keywords_ireland_eu_national_id_card" />
        </Pattern>
<Pattern confidenceLevel="75">
          <IdMatch idRef="Func_ireland_eu_national_id_card" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Palavras-chave

#### <a name="keywordsirelandeunationalidcard"></a>Keywords_ireland_eu_national_id_card

número de serviço pessoal de público
  
PPS nenhum
  
número de seguro social e de receita
  
rsi nenhum
  
número de identificação pessoal
  
identification number

  
número de identificação pessoal
  
uimhir phearsanta seirbhíse poiblí
  
uimh. PSP
  
## <a name="italy"></a>Itália

### <a name="format"></a>Formato

Uma combinação de 16 caracteres de letras e dígitos no padrão especificado
  
### <a name="pattern"></a>Padrão

Uma combinação de 16 caracteres de letras e dígitos:
  
- Três letras que correspondem às três primeiros consoantes no nome da família
    
- Três letras que correspondem à primeira, terceira e quarta consoantes no primeiro nome de usuário
    
- Dois dígitos que correspondem à última dígitos do ano nascimento
    
- Uma letra que corresponde à letra no mês de nascimento — letras são usadas em ordem alfabética, mas apenas as letras de a F, R, L, M, P, R para T são usadas (assim, janeiro é uma e outubro é R)
    
- Dois dígitos que correspondem ao dia do mês de nascimento — para diferenciar entre sexos, 40 é adicionado ao dia de nascimento para feminino
    
- Quatro dígitos que corresponde ao código de área específico para o município onde a pessoa surgiu (códigos de país são usados para países estrangeiros)
    
- Um dígito de paridade
    
### <a name="checksum"></a>Soma de verificação

Sim
  
### <a name="definition"></a>Definição

Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:
  
- A função `Func_italy_eu_national_id_card` encontra conteúdo que corresponde ao padrão. 
    
- Uma palavra-chave da `Keywords_italy_eu_national_id_card` for encontrado. 
    
Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:
  
- A função `Func_italy_eu_national_id_card` encontra conteúdo que corresponde ao padrão. 
    
```
<Entity id="419f449f-6d9d-4be1-a154-b531f7a91b41" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_italy_eu_national_id_card" />
          <Match idRef="Keywords_italy_eu_national_id_card" />
        </Pattern>
<Pattern confidenceLevel="75">
          <IdMatch idRef="Func_italy_eu_national_id_card" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Palavras-chave

#### <a name="keywordsitalyeunationalidcard"></a>Keywords_italy_eu_national_id_card

código pessoal
  
número de código pessoal
  
número de certificados pessoais
  
código fiscal
  
personalcodeno #
  
número de identificação pessoal
  
código de identificação pessoal
  
codice personale
  
numero certificato personale
  
numero personale
  
numero id personale
  
codice personale id
  
codice fiscale
  
## <a name="italy"></a>Itália

### <a name="format"></a>Formato

11 dígitos e um hífen no formato especificado
  
### <a name="pattern"></a>Padrão

11 dígitos e um hífen:
  
-  Seis dígitos que correspondem à data de nascimento (DDMMYY) 
    
- Um hífen
    
- Um dígito que corresponde do century de nascimento ("0" para o décimo nono century, para 20 century "1" e "2" para century 21)
    
- Quatro dígitos, gerados aleatoriamente
    
### <a name="checksum"></a>Soma de verificação

Sim
  
### <a name="definition"></a>Definição

Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:
  
- A função `Func_latvia_eu_national_id_card` encontra conteúdo que corresponde ao padrão. 
    
- Uma palavra-chave da `Keywords_latvia_eu_national_id_card` for encontrado. 
    
Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:
  
- A função `Func_latvia_eu_national_id_card` encontra conteúdo que corresponde ao padrão. 
    
```
<Entity id="419f449f-6d9d-4be1-a154-b531f7a91b41" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_latvia_eu_national_id_card" />
          <Match idRef="Keywords_latvia_eu_national_id_card" />
        </Pattern>
 <Pattern confidenceLevel="75">
          <IdMatch idRef="Func_latvia_eu_national_id_card" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Palavras-chave

#### <a name="keywordslatviaeunationalidcard"></a>Keywords_latvia_eu_national_id_card

código pessoal
  
número de código pessoal
  
número de certificados pessoais
  
personalcodeno #
  
número de identificação pessoal
  
código de identificação pessoal
  
kods personagens
  
## <a name="lithuania"></a>Lituânia

### <a name="format"></a>Formato

11 dígitos sem espaços e delimitadores
  
### <a name="pattern"></a>Padrão

11 dígitos sem espaços e delimitadores:
  
- Um dígito que corresponde ao gênero da pessoa e o century de nascimento
    
-  Seis dígitos que correspondem à data de nascimento (aammdd) 
    
- Três dígitos que correspondem ao número de série da data de nascimento
    
- Seleção de um dígito
    
### <a name="checksum"></a>Soma de verificação

Sim
  
### <a name="definition"></a>Definição

Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:
  
- A função `Func_lithuania_eu_national_id_card` encontra conteúdo que corresponde ao padrão. 
    
- Uma palavra-chave da `Keywords_lithuania_eu_national_id_card` for encontrado. 
    
Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:
  
- A função `Func_lithuania_eu_national_id_card` encontra conteúdo que corresponde ao padrão. 
    
```
 
<Entity id="419f449f-6d9d-4be1-a154-b531f7a91b41" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_lithuania_eu_national_id_card" />
          <Match idRef="Keywords_lithuania_eu_national_id_card" />
        </Pattern> 
<Pattern confidenceLevel="75">
          <IdMatch idRef="Func_lithuania_eu_national_id_card" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Palavras-chave

#### <a name="keywordslithuaniaeunationalidcard"></a>Keywords_lithuania_eu_national_id_card

código numérico pessoal
  
número de identificação exclusivo
  
número de serviços aos cidadãos
  
número de identidade exclusiva
  
uniqueidentityno #
  
código de pessoal.
  
asmeninis skaitmeninis kodas
  
unikalus identifikavimo numeris
  
piliečio paslaugos numeris
  
unikalus identifikavimo kodas
  
asmens kodas.
  
## <a name="luxemburg"></a>Luxemburgo

### <a name="format"></a>Formato

11 dígitos sem espaços e delimitadores
  
### <a name="pattern"></a>Padrão

11 dígitos
  
- Um dígito que corresponde ao gênero da pessoa e o century de nascimento
    
-  Seis dígitos que correspondem à data de nascimento (aammdd) 
    
- Três dígitos que correspondem ao número de série da data de nascimento
    
- Seleção de um dígito
    
### <a name="checksum"></a>Soma de verificação

Não aplicável
  
### <a name="definition"></a>Definição

Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:
  
- A expressão regular `Regex_luxemburg_eu_national_id_card` encontra conteúdo que corresponde ao padrão. 
    
- Uma palavra-chave da `Keywords_luxemburg_eu_national_id_card` for encontrado. 
    
```
<Entity id="419f449f-6d9d-4be1-a154-b531f7a91b41" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_luxemburg_eu_national_id_card" />
          <Match idRef="Keywords_luxemburg_eu_national_id_card" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Palavras-chave

#### <a name="keywordsluxemburgeunationalidcard"></a>Keywords_luxemburg_eu_national_id_card

identificação pessoal
  
número de identificação pessoal
  
personalidno #
  
número de identificação exclusiva
  
personalidnumber #
  
chave de identificação exclusiva
  
código de identificação pessoal
  
uniqueidkey #
  
código individual
  
id individual
  
id de eindeutige-nummer
  
id de eindeutige
  
ID personnelle
  
numéro d'identification pessoal
  
idpersonnelle #
  
persönliche identifikationsnummer
  
eindeutigeid #
  
## <a name="malta"></a>Malta

### <a name="format"></a>Formato

Sete dígitos, seguidos por uma letra
  
### <a name="pattern"></a>Padrão

Sete dígitos seguidos por uma letra:
  
-  Sete dígitos  
    
- Uma letra maiuscula (com distinção entre maiusculas e minúsculas)
    
### <a name="checksum"></a>Soma de verificação

Não aplicável
  
### <a name="definition"></a>Definição

Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:
  
- A expressão regular `Regex_malta_eu_national_id_card` encontra conteúdo que corresponde ao padrão. 
    
- Uma palavra-chave da `Keywords_malta_eu_national_id_card` for encontrado. 
    
Uma política de DLP tem 65% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:
  
- A expressão regular `Regex_malta_eu_national_id_card` encontra conteúdo que corresponde ao padrão. 
    
```
 
<Entity id="419f449f-6d9d-4be1-a154-b531f7a91b41" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_malta_eu_national_id_card" />
          <Match idRef="Keywords_malta_eu_national_id_card" />
        </Pattern>
<Pattern confidenceLevel="65">
          <IdMatch idRef="Regex_malta_eu_national_id_card" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Palavras-chave

#### <a name="keywordsmaltaeunationalidcard"></a>Keywords_malta_eu_national_id_card

código numérico pessoal
  
número de identificação exclusivo
  
número de serviços aos cidadãos
  
número de identidade exclusiva
  
uniqueidentityno #
  
kodiċi numerali personali
  
numru guias ' identifikazzjoni uniku
  
numru servizz de tarefa taċ-ċittadin
  
numru guias ' identità uniku
  
## <a name="netherlands"></a>Países Baixos

### <a name="format"></a>Formato

Nove dígitos sem espaços ou delimitadores
  
### <a name="pattern"></a>Padrão

Nove dígitos
  
### <a name="checksum"></a>Soma de verificação

Sim
  
### <a name="definition"></a>Definição

Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:
  
- A função `Func_netherlands_eu_national_id_card` encontra conteúdo que corresponde ao padrão. 
    
- Uma palavra-chave da é encontrada.
    
Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:
  
- A função `Func_netherlands_eu_national_id_card` encontra conteúdo que corresponde ao padrão. 
    
```
 
<Entity id="419f449f-6d9d-4be1-a154-b531f7a91b41" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_netherlands_eu_national_id_card" />
          <Match idRef="Keywords_netherlands_eu_national_id_card" />
        </Pattern>
<Pattern confidenceLevel="75">
          <IdMatch idRef="Func_netherlands_eu_national_id_card" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Palavras-chave

#### <a name="keywordsnetherlandseunationalidcard"></a>Keywords_netherlands_eu_national_id_card

código numérico pessoal
  
número de identificação exclusivo
  
número de serviços aos cidadãos
  
número de identidade exclusiva
  
uniqueidentityno #
  
bsn
  
bsn #
  
código de numerieke persoonlijke
  
uniek identificatienummer
  
burgerservicenummer
  
uniek identiteitsnummer
  
## <a name="poland"></a>Polônia

Para obter detalhes, consulte a seção "Polônia nacional ID (PESEL)" em [quais tipos de informações confidenciais a procurar](what-the-sensitive-information-types-look-for.md).
  
## <a name="portugal"></a>Portugal

Para obter detalhes, consulte a seção "Número de cartão de cidadãos Portugal" nos [quais os tipos de informações confidenciais procurar](what-the-sensitive-information-types-look-for.md).
  
## <a name="romania"></a>Romênia

### <a name="format"></a>Formato

13 dígitos sem espaços e delimitadores
  
### <a name="pattern"></a>Padrão

13 dígitos
  
### <a name="checksum"></a>Soma de verificação

Sim
  
### <a name="definition"></a>Definição

Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:
  
- A função `Func_romania_eu_national_id_card` encontra conteúdo que corresponde ao padrão. 
    
- Uma palavra-chave da `Keywords_romania_eu_national_id_card` for encontrado. 
    
Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:
  
- A função `Func_romania_eu_national_id_card` encontra conteúdo que corresponde ao padrão. 
    
```
 
<Entity id="419f449f-6d9d-4be1-a154-b531f7a91b41" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_romania_eu_national_id_card" />
          <Match idRef="Keywords_romania_eu_national_id_card" />
        </Pattern>
<Pattern confidenceLevel="75">
          <IdMatch idRef="Func_romania_eu_national_id_card" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Palavras-chave

#### <a name="keywordsromaniaeunationalidcard"></a>Keywords_romania_eu_national_id_card

código numérico pessoal
  
número de identificação exclusivo
  
cnp
  
cnp #
  
fixar
  
PIN #
  
número do seguro
  
insurancenumber #
  
número de identidade exclusiva
  
uniqueidentityno #
  
pessoal de COD numéricos
  
bacalhau identificare pessoal
  
COD UNIX identificare
  
număr UNIX de pessoal
  
număr identitate
  
număr identificare pessoal
  
număridentitate #
  
codnumericpersonal #
  
numărpersonalunic #
  
## <a name="slovakia"></a>Eslováquia

### <a name="format"></a>Formato

Dez dígitos que contém a barra um invertida
  
### <a name="pattern"></a>Padrão

Dez dígitos que contém a barra um invertida:
  
### <a name="checksum"></a>Soma de verificação

Sim
  
### <a name="definition"></a>Definição

Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:
  
- A função `Func_slovakia_eu_national_id_card` encontra conteúdo que corresponde ao padrão. 
    
- Uma palavra-chave da `Keywords_slovakia_eu_national_id_card` for encontrado. 
    
Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:
  
- A função `Func_slovakia_eu_national_id_card` encontra conteúdo que corresponde ao padrão. 
    
```
 
<Entity id="419f449f-6d9d-4be1-a154-b531f7a91b41" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_slovakia_eu_national_id_card" />
          <Match idRef="Keywords_slovakia_eu_national_id_card" />
        </Pattern>
<Pattern confidenceLevel="75">
          <IdMatch idRef="Func_slovakia_eu_national_id_card" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Palavras-chave

#### <a name="keywordsslovakiaeunationalidcard"></a>Keywords_slovakia_eu_national_id_card

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
  
## <a name="slovenia"></a>Eslovênia

### <a name="format"></a>Formato

13 dígitos sem espaços ou delimitadores
  
### <a name="pattern"></a>Padrão

13 dígitos no padrão especificado:
  
-  Sete dígitos que correspondem à data de nascimento (DDMMLLL) onde "LLL" corresponde aos últimos três dígitos do ano nascimento 
    
- Dois dígitos que correspondem à área de nascimento
    
- Três dígitos que correspondem a uma combinação de gênero e número de série para as pessoas nascidas no mesmo dia (000-499 para Masculino) e 500 e 999 para fêmea
    
- Seleção de um dígito
    
### <a name="checksum"></a>Soma de verificação

Sim
  
### <a name="definition"></a>Definição

Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:
  
- A função `Func_slovenia_eu_national_id_card` encontra conteúdo que corresponde ao padrão. 
    
- Uma palavra-chave da `Keywords_slovenia_eu_national_id_card` for encontrado. 
    
Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:
  
- A função `Func_slovenia_eu_national_id_card` encontra conteúdo que corresponde ao padrão. 
    
```
 
<Entity id="419f449f-6d9d-4be1-a154-b531f7a91b41" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_slovenia_eu_national_id_card" />
          <Match idRef="Keywords_slovenia_eu_national_id_card" />
        </Pattern>
<Pattern confidenceLevel="75">
          <IdMatch idRef="Func_slovenia_eu_national_id_card" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Palavras-chave

#### <a name="keywordssloveniaeunationalidcard"></a>Keywords_slovenia_eu_national_id_card

código numérico pessoal
  
número de identificação exclusivo
  
número exclusivo de registro
  
número de identidade exclusiva
  
uniqueidentityno #
  
número exclusivo cidadãos mestre
  
edinstvena identifikacijska številka
  
uniqueidentityno #
  
edinstvena številka glavnega državljana
  
emšo
  
## <a name="spain"></a>Espanha

### <a name="format"></a>Formato

Sete dígitos seguidos por um caractere
  
### <a name="pattern"></a>Padrão

Sete dígitos seguidos por um caractere
  
- Sete dígitos 
    
- Um dígito ou carta (não diferencia maiusculas de minúsculas)
    
### <a name="checksum"></a>Soma de verificação

Não aplicável
  
### <a name="definition"></a>Definição

Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:
  
- A expressão regular `Regex_spain_eu_national_id_card` encontra conteúdo que corresponde ao padrão. 
    
- Uma palavra-chave da `Keywords_spain_eu_national_id_card"` for encontrado. 
    
```
 
<Entity id="419f449f-6d9d-4be1-a154-b531f7a91b41" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_spain_eu_national_id_card" />
          <Match idRef="Keywords_spain_eu_national_id_card" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Palavras-chave

#### <a name="keywordsspaineunationalidcard"></a>Keywords_spain_eu_national_id_card

dni
  
número de identificação nacional
  
número de identidade nacional
  
número do seguro
  
número de identificação pessoal
  
identidade nacional
  
identidade pessoal sem
  
número de identidade exclusiva
  
nationalidno #
  
UniqueID #
  
dni #
  
nationalid #
  
NIE #
  
NIE
  
nienúmero #
  
número de NIE
  
documento nacional de identidad
  
identidad único
  
número nacional identidad
  
número de dni
  
dninúmero #
  
identidadúnico #
  
## <a name="sweden"></a>Suécia

Para obter detalhes, consulte a seção "ID nacional da Suécia" nos [quais os tipos de informações confidenciais procurar](what-the-sensitive-information-types-look-for.md).
  
## <a name="see-also"></a>Confira também

[O que os tipos de informações confidenciais procuram](what-the-sensitive-information-types-look-for.md)

