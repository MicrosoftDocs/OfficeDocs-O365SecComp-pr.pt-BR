---
title: Número de passaporte da UE
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: 8/16/2018
ms.audience: Admin
ms.topic: reference
ms.service: o365-administration
localization_priority: Normal
ms.assetid: 8c00df57-9fb3-459c-ba87-40480c87bd55
description: Este tópico mostra o que uma política de prevenção (DLP) de perda de dados procura por quando detecta o tipo de informações confidenciais de número de passaporte da UE. Esse tipo de informações confidenciais define diferentes padrões, palavras-chave e outras evidências para cada país.
ms.openlocfilehash: 71acc39b885c057e1771ec13b2f3c25017ac1bb6
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22524139"
---
# <a name="eu-passport-number"></a>Número de passaporte da UE

Este tópico mostra o que uma política de prevenção (DLP) de perda de dados procura por quando detecta o tipo de informações confidenciais de número de passaporte da UE. Esse tipo de informações confidenciais define diferentes padrões, palavras-chave e outras evidências para cada país.
  
## <a name="austria"></a>Áustria

### <a name="format"></a>Formato

Uma letra seguida por um espaço opcional e sete dígitos
  
### <a name="pattern"></a>Padrão

Uma combinação de uma letra, um espaço e sete dígitos:
  
- Uma letra (não diferencia maiúscula de minúscula)
    
- Um espaço (opcional)
    
- Sete dígitos
    
### <a name="checksum"></a>Soma de verificação

Não aplicável
  
### <a name="definition"></a>Definição

Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:
  
- A expressão regular `Regex_austria_eu_passport_number` encontra conteúdo que corresponde ao padrão. 
    
- Uma palavra-chave da `Keywords_austria_eu_passport_number` for encontrado. 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_austria_eu_passport_number" />
          <Match idRef="Keywords_austria_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Palavras-chave

| |
|**Keywords_austria_eu_passport_number**|
|:-----|
|número de passaporte  <br/> número de passaporte austríaco  <br/> Passport nenhum  <br/> reisepass  <br/> österreichisch reisepass  <br/> |
   
## <a name="belgium"></a>Bélgica

### <a name="format"></a>Formato

Duas letras seguidas de seis dígitos sem espaços ou delimitadores
  
### <a name="pattern"></a>Padrão

Duas letras e seguido de seis dígitos
  
### <a name="checksum"></a>Soma de verificação

Não aplicável
  
### <a name="definition"></a>Definição

Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:
  
- A expressão regular `Regex_belgium_eu_passport_number` encontra conteúdo que corresponde ao padrão. 
    
- Uma palavra-chave da `Keywords_belgium_eu_passport_number` for encontrado. 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_belgium__eu_passport_number" />
          <Match idRef="Keywords_belgium_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Palavras-chave

| |
|**Keywords_belgium_eu_passport_number**|
|:-----|
|número de passaporte  <br/> número de passaporte belga  <br/> Passport nenhum  <br/> paspoort  <br/> paspoortnummer  <br/> reisepass kein  <br/> reisepass  <br/> |
   
## <a name="bulgaria"></a>Bulgária

### <a name="format"></a>Formato

Nove dígitos sem espaços e delimitadores
  
### <a name="pattern"></a>Padrão

 Nove dígitos 
  
### <a name="checksum"></a>Soma de verificação

Não
  
### <a name="definition"></a>Definição

Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:
  
- A expressão regular `Regex_bulgaria_eu_passport_number` encontra conteúdo que corresponde ao padrão. 
    
- Uma palavra-chave da `Keywords_bulgaria_eu_passport_number` for encontrado. 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_bulgaria_eu_passport_number" />
          <Match idRef="Keywords_bulgaria_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Palavras-chave

| |
|**Keywords_bulgaria_eu_passport_number**|
|:-----|
|número de passaporte  <br/> número de passaporte búlgaro  <br/> Passport nenhum  <br/> НОМЕР НА ПАСПОРТА  <br/> |
   
## <a name="croatia"></a>Croácia

### <a name="format"></a>Formato

Nove dígitos sem espaços e delimitadores
  
### <a name="pattern"></a>Padrão

 Nove dígitos 
  
### <a name="checksum"></a>Soma de verificação

Não
  
### <a name="definition"></a>Definição

Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:
  
- A expressão regular `Regex_croatia_eu_passport_number` encontra conteúdo que corresponde ao padrão. 
    
- Uma palavra-chave da `Keywords_croatia_eu_passport_number` for encontrado. 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_croatia_eu_passport_number" />
          <Match idRef="Keywords_croatia_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Palavras-chave

| |
|**Keywords_croatia_eu_passport_number**|
|:-----|
|número de passaporte  <br/> número de passaporte croata  <br/> Passport nenhum  <br/> broj putovnice  <br/> |
   
## <a name="cyprus"></a>Chipre

### <a name="format"></a>Formato

Uma letra seguida de 6 a 8 dígitos sem espaços ou delimitadores
  
### <a name="pattern"></a>Padrão

Uma letra seguida de seis a oito dígitos
  
### <a name="checksum"></a>Soma de verificação

Não
  
### <a name="definition"></a>Definição

Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:
  
- A expressão regular `Regex_cyprus_eu_passport_number` encontra conteúdo que corresponde ao padrão. 
    
- Uma palavra-chave da `Keywords_cyprus_eu_passport_number` for encontrado. 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_cyprus_eu_passport_number" />
          <Match idRef="Keywords_cyprus_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Palavras-chave

| |
|**Keywords_cyprus_eu_passport_number**|
|:-----|
|número de passaporte  <br/> número de passaporte Chipre  <br/> Passport nenhum  <br/> ΑΡΙΘΜΌ ΔΙΑΒΑΤΗΡΊΟΥ  <br/> |
   
## <a name="czech-republic"></a>República Tcheca

### <a name="format"></a>Formato

Oito dígitos sem espaços ou delimitadores
  
### <a name="pattern"></a>Padrão

Oito dígitos sem espaços ou delimitadores
  
### <a name="checksum"></a>Soma de verificação

Não
  
### <a name="definition"></a>Definição

Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:
  
- A expressão regular `Regex_czech_republic_eu_passport_number` encontra conteúdo que corresponde ao padrão. 
    
- Uma palavra-chave da `Keywords_czech_republic_eu_passport_number` for encontrado. 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_czech_republic_eu_passport_number" />
          <Match idRef="Keywords_czech_republic_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Palavras-chave

| |
|**Keywords_czech_republic_eu_passport_number**|
|:-----|
|número de passaporte  <br/> número de passaporte tcheco  <br/> Passport nenhum  <br/> cestovní pas  <br/> PAS  <br/> |
   
## <a name="denmark"></a>Dinamarca

### <a name="format"></a>Formato

Nove dígitos sem espaços e delimitadores
  
### <a name="pattern"></a>Padrão

 Nove dígitos 
  
### <a name="checksum"></a>Soma de verificação

Não
  
### <a name="definition"></a>Definição

Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:
  
- A expressão regular `Regex_denmark_eu_passport_number` encontra conteúdo que corresponde ao padrão. 
    
- Uma palavra-chave da `Keywords_denmark_eu_passport_number` for encontrado. 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_denmark_eu_passport_number" />
          <Match idRef="Keywords_denmark_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Palavras-chave

| |
|**Keywords_denmark_eu_passport_number**|
|:-----|
|número de passaporte  <br/> número de passaporte dinamarquês  <br/> Passport nenhum  <br/> PAS  <br/> pasnummer  <br/> |
   
## <a name="estonia"></a>Estônia

### <a name="format"></a>Formato

Uma letra seguida por sete dígitos sem espaços ou delimitadores
  
### <a name="pattern"></a>Padrão

Uma letra seguida por sete dígitos
  
### <a name="checksum"></a>Soma de verificação

Não
  
### <a name="definition"></a>Definição

Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:
  
- A expressão regular `Regex_estonia_eu_passport_number` encontra conteúdo que corresponde ao padrão. 
    
- Uma palavra-chave da `Keywords_estonia_eu_passport_number` for encontrado. 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_estonia_eu_passport_number" />
          <Match idRef="Keywords_estonia_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Palavras-chave

| |
|**Keywords_estonia_eu_passport_number**|
|:-----|
|número de passaporte  <br/> número de passaporte estoniano  <br/> Passport nenhum  <br/> eesti kodaniku secreta  <br/> |
   
## <a name="finland"></a>Finlândia

Para obter detalhes, consulte a seção "Número de passaporte da Finlândia" nos [quais os tipos de informações confidenciais procurar](what-the-sensitive-information-types-look-for.md).
  
## <a name="france"></a>França

Para obter detalhes, consulte a seção "Número de passaporte da França" nos [quais os tipos de informações confidenciais procurar](what-the-sensitive-information-types-look-for.md).
  
## <a name="germany"></a>Alemanha

Para obter detalhes, consulte a seção "Número de passaporte da Alemanha" em [quais tipos de informações confidenciais a procurar](what-the-sensitive-information-types-look-for.md).
  
## <a name="greece"></a>Grécia

### <a name="format"></a>Formato

Duas letras seguidas por sete dígitos sem espaços ou delimitadores
  
### <a name="pattern"></a>Padrão

Duas letras seguidas por sete dígitos
  
### <a name="checksum"></a>Soma de verificação

Não
  
### <a name="definition"></a>Definição

Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:
  
- A expressão regular `Regex_greece_eu_passport_number` encontra conteúdo que corresponde ao padrão. 
    
- Uma palavra-chave da `Keywords_greece_eu_passport_number` for encontrado. 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_greece_eu_passport_number" />
          <Match idRef="Keywords_greece_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Palavras-chave

| |
|**Keywords_greece_eu_passport_number**|
|:-----|
|número de passaporte  <br/> número de passaporte grego  <br/> Passport nenhum  <br/> ΔΙΑΒΑΤΗΡΙΟ  <br/> |
   
## <a name="hungary"></a>Hungria

### <a name="format"></a>Formato

Duas letras seguidas por seis ou sete dígitos sem espaços ou delimitadores
  
### <a name="pattern"></a>Padrão

Duas letras seguidas por seis ou sete dígitos
  
### <a name="checksum"></a>Soma de verificação

Não
  
### <a name="definition"></a>Definição

Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:
  
- A expressão regular `Regex_hungary_eu_passport_number` encontra conteúdo que corresponde ao padrão. 
    
- Uma palavra-chave da `Keywords_hungary_eu_passport_number` for encontrado. 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_hungary_eu_passport_number" />
          <Match idRef="Keywords_hungary_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Palavras-chave

| |
|**Keywords_hungary_eu_passport_number**|
|:-----|
|número de passaporte  <br/> número de passaporte húngaro  <br/> Passport nenhum  <br/> útlevél száma  <br/> |
   
## <a name="ireland"></a>Irlanda

### <a name="format"></a>Formato

Duas letras ou dígitos seguidos por sete dígitos sem espaços ou delimitadores
  
### <a name="pattern"></a>Padrão

Duas letras ou dígitos seguidos por sete dígitos:
  
- Dois dígitos ou letras (não diferenciam maiúsculas de minúsculas)
    
- Sete dígitos
    
### <a name="checksum"></a>Soma de verificação

Não
  
### <a name="definition"></a>Definição

Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:
  
- A expressão regular `Regex_ireland_eu_passport_number` encontra conteúdo que corresponde ao padrão. 
    
- Uma palavra-chave da `Keywords_ireland_eu_passport_number` for encontrado. 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_ireland_eu_passport_number" />
          <Match idRef="Keywords_ireland_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Palavras-chave

| |
|**Keywords_ireland_eu_passport_number**|
|:-----|
|número de passaporte  <br/> número de passaporte irlandês  <br/> Passport nenhum  <br/> PAS  <br/> passport  <br/> passeport  <br/> numero passeport  <br/> |
   
## <a name="italy"></a>Itália

### <a name="format"></a>Formato

Duas letras ou dígitos seguidos por sete dígitos sem espaços ou delimitadores
  
### <a name="pattern"></a>Padrão

Duas letras ou dígitos seguidos por sete dígitos:
  
- Dois dígitos ou letras (não diferenciam maiúsculas de minúsculas)
    
- Sete dígitos
    
### <a name="checksum"></a>Soma de verificação

Não aplicável
  
### <a name="definition"></a>Definição

Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:
  
- A expressão regular `Regex_italy_eu_passport_number` encontra conteúdo que corresponde ao padrão. 
    
- Uma palavra-chave da `Keywords_italy_eu_passport_number` for encontrado. 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_italy_eu_passport_number" />
          <Match idRef="Keywords_italy_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Palavras-chave

| |
|**Keywords_italy_eu_passport_number**|
|:-----|
|número de passaporte italiano  <br/> repubblica italiana passaporto  <br/> passaporto  <br/> passaporto italiana  <br/> número de passaporte  <br/> italiana passaporto numero  <br/> numero passaporto  <br/> numéro passeport italien  <br/> numéro passeport  <br/> |
   
## <a name="latvia"></a>Letônia

### <a name="format"></a>Formato

Duas letras ou dígitos seguidos por sete dígitos sem espaços ou delimitadores
  
### <a name="pattern"></a>Padrão

Duas letras ou dígitos seguidos por sete dígitos:
  
- Dois dígitos ou letras (não diferenciam maiúsculas de minúsculas)
    
- Sete dígitos
    
### <a name="checksum"></a>Soma de verificação

Não
  
### <a name="definition"></a>Definição

Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:
  
- A expressão regular `Regex_latvia_eu_passport_number` encontra conteúdo que corresponde ao padrão. 
    
- Uma palavra-chave da `Keywords_latvia_eu_passport_number` for encontrado. 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_latvia_eu_passport_number" />
          <Match idRef="Keywords_latvia_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Palavras-chave

| |
|**Keywords_latvia_eu_passport_number**|
|:-----|
|número de passaporte  <br/> número de passaporte letão  <br/> Passport nenhum  <br/> pase numurs  <br/> |
   
## <a name="lithuania"></a>Lituânia

### <a name="format"></a>Formato

Oito dígitos ou letras sem espaços ou delimitadores
  
### <a name="pattern"></a>Padrão

Oito dígitos ou letras (não maiusculas de minúsculas)
  
### <a name="checksum"></a>Soma de verificação

Não aplicável
  
### <a name="definition"></a>Definição

Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:
  
- A expressão regular `Regex_lithuania_eu_passport_number` encontra conteúdo que corresponde ao padrão. 
    
- Uma palavra-chave da `Keywords_lithuania_eu_passport_number` for encontrado. 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_lithuania_eu_passport_number" />
          <Match idRef="Keywords_lithuania_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Palavras-chave

| |
|**Keywords_lithuania_eu_passport_number**|
|:-----|
|número de passaporte  <br/> número de passaporte lithunian  <br/> Passport nenhum  <br/> Paso numeris  <br/> |
   
## <a name="luxemburg"></a>Luxemburgo

### <a name="format"></a>Formato

Oito dígitos ou letras sem espaços ou delimitadores
  
### <a name="pattern"></a>Padrão

Oito dígitos ou letras (não maiusculas de minúsculas)
  
### <a name="checksum"></a>Soma de verificação

Não
  
### <a name="definition"></a>Definição

Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:
  
- A expressão regular `Regex_nation_eu_passport_number` encontra conteúdo que corresponde ao padrão. 
    
- Uma palavra-chave da `Keywords_nation_eu_passport_number` for encontrado. 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_nation_eu_passport_number" />
          <Match idRef="Keywords_nation_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Palavras-chave

| |
|**Keywords_nation_eu_passport_number**|
|:-----|
|número de passaporte  <br/> número de passaporte letão  <br/> Passport nenhum  <br/> passnummer  <br/> |
   
## <a name="malta"></a>Malta

### <a name="format"></a>Formato

Sete dígitos sem espaços ou delimitadores
  
### <a name="pattern"></a>Padrão

 Sete dígitos 
  
### <a name="checksum"></a>Soma de verificação

Não
  
### <a name="definition"></a>Definição

Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:
  
- A expressão regular `Regex_malta_eu_passport_number` encontra conteúdo que corresponde ao padrão. 
    
- Uma palavra-chave da `Keywords_malta_eu_passport_number` for encontrado. 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_malta_eu_passport_number" />
          <Match idRef="Keywords_malta_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Palavras-chave

| |
|**Keywords_malta_eu_passport_number**|
|:-----|
|número de passaporte  <br/> número de passaporte Maltês  <br/> Passport nenhum  <br/> horizontal-passaport numru  <br/> |
   
## <a name="netherlands"></a>Países Baixos

### <a name="format"></a>Formato

Nove letras ou dígitos sem espaços ou delimitadores
  
### <a name="pattern"></a>Padrão

Nove letras ou dígitos
  
### <a name="checksum"></a>Soma de verificação

Não aplicável
  
### <a name="definition"></a>Definição

Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:
  
- A expressão regular `Regex_netherlands_eu_passport_number` encontra conteúdo que corresponde ao padrão. 
    
- Uma palavra-chave da `Keywords_netherlands_eu_passport_number` for encontrado. 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_netherlands_eu_passport_number" />
          <Match idRef="Keywords_netherlands_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Palavras-chave

| |
|**Keywords_netherlands_eu_passport_number**|
|:-----|
|número de passaporte holandês  <br/> número de passaporte  <br/> número de passaporte países baixos  <br/> nederlanden paspoort nummer  <br/> paspoort  <br/> nederlanden paspoortnummer  <br/> paspoortnummer  <br/> |
   
## <a name="poland"></a>Polônia

Para obter detalhes, consulte a seção "Número de passaporte da Polônia" nos [quais os tipos de informações confidenciais procurar](what-the-sensitive-information-types-look-for.md).
  
## <a name="portugal"></a>Portugal

### <a name="format"></a>Formato

Uma letra seguida de seis dígitos sem espaços ou delimitadores
  
### <a name="pattern"></a>Padrão

Uma letra seguida de seis dígitos:
  
- Uma letra (não diferencia maiúscula de minúscula)
    
- Seis dígitos
    
### <a name="checksum"></a>Soma de verificação

Não
  
### <a name="definition"></a>Definição

Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:
  
- A expressão regular `Regex_portugal_eu_passport_number` encontra conteúdo que corresponde ao padrão. 
    
- Uma palavra-chave da `Keywords_portugal_eu_passport_number` for encontrado. 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_portugal_eu_passport_number" />
          <Match idRef="Keywords_portugal_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Palavras-chave

| |
|**Keywords_portugal_eu_passport_number**|
|:-----|
|número de passaporte  <br/> número de passaporte português  <br/> Passport nenhum  <br/> número passaporte  <br/> |
   
## <a name="romania"></a>Romênia

### <a name="format"></a>Formato

Oito ou nove dígitos sem espaços e delimitadores
  
### <a name="pattern"></a>Padrão

Oito ou nove dígitos
  
### <a name="checksum"></a>Soma de verificação

Não
  
### <a name="definition"></a>Definição

Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:
  
- A expressão regular `Regex_romania_eu_passport_number` encontra conteúdo que corresponde ao padrão. 
    
- Uma palavra-chave da `Keywords_romania_eu_passport_number` for encontrado. 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_romania_eu_passport_number" />
          <Match idRef="Keywords_romania_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Palavras-chave

| |
|**Keywords_romania_eu_passport_number**|
|:-----|
|número de passaporte  <br/> número de passaporte romeno  <br/> Passport nenhum  <br/> numărul pașaportului  <br/> |
   
## <a name="slovakia"></a>Eslováquia

### <a name="format"></a>Formato

Um dígito ou letra seguido por sete dígitos sem espaços ou delimitadores
  
### <a name="pattern"></a>Padrão

Um dígito ou carta (não maiusculas de minúsculas) seguido por sete dígitos
  
### <a name="checksum"></a>Soma de verificação

Não
  
### <a name="definition"></a>Definição

Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:
  
- A expressão regular `Regex_slovakia_eu_passport_number` encontra conteúdo que corresponde ao padrão. 
    
- Uma palavra-chave da `Keywords_slovakia_eu_passport_number` for encontrado. 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_slovakia_eu_passport_number" />
          <Match idRef="Keywords_slovakia_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Palavras-chave

| |
|**Keywords_slovakia_eu_passport_number**|
|:-----|
|número de passaporte  <br/> número de passaporte eslovaco  <br/> Passport nenhum  <br/> Číslo pasu  <br/> |
   
## <a name="slovenia"></a>Eslovênia

### <a name="format"></a>Formato

Duas letras seguidas por sete dígitos sem espaços ou delimitadores
  
### <a name="pattern"></a>Padrão

Duas letras seguidas por sete dígitos:
  
- A letra "P"
    
- Uma letra maiuscula
    
- Sete dígitos
    
### <a name="checksum"></a>Soma de verificação

Não
  
### <a name="definition"></a>Definição

Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:
  
- A expressão regular `Regex_slovenia_eu_passport_number` encontra conteúdo que corresponde ao padrão. 
    
- Uma palavra-chave da `Keywords_slovenia_eu_passport_number` for encontrado. 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_slovenia_eu_passport_number" />
          <Match idRef="Keywords_slovenia_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Palavras-chave

| |
|**Keywords_slovenia_eu_passport_number**|
|:-----|
|número de passaporte  <br/> número de passaporte esloveno  <br/> Passport nenhum  <br/> Lista de potnega številka  <br/> |
   
## <a name="spain"></a>Espanha

### <a name="format"></a>Formato

Uma combinação de oito ou nove caracteres de letras e números sem espaços ou delimitadores
  
### <a name="pattern"></a>Padrão

Uma combinação de oito ou nove caracteres de letras e números:
  
-  Dois dígitos ou letras 
    
- Um dígito ou carta (opcional)
    
- Seis dígitos
    
### <a name="checksum"></a>Soma de verificação

Não aplicável
  
### <a name="definition"></a>Definição

Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:
  
- A expressão regular `Regex_spain_eu_passport_number` encontra conteúdo que corresponde ao padrão. 
    
- Uma palavra-chave da `Keywords_spain_eu_passport_number` for encontrado. 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_spain_eu_passport_number" />
          <Match idRef="Keywords_spain_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Palavras-chave

| |
|**Keywords_spain_eu_passport_number**|
|:-----|
|passport  <br/> passaporte da Espanha  <br/> Catálogo do Passport  <br/> número de passaporte  <br/> Passport nenhum  <br/> libreta pasaporte  <br/> número pasaporte  <br/> españa pasaporte  <br/> pasaporte  <br/> |
   
## <a name="sweden"></a>Suécia

Para obter detalhes, consulte a seção "Número de passaporte da Suécia" nos [quais os tipos de informações confidenciais procurar](what-the-sensitive-information-types-look-for.md).
  
## <a name="uk"></a>REINO UNIDO

Para obter detalhes, consulte a seção "Número de passaporte US / Reino Unido" nos [quais os tipos de informações confidenciais procurar](what-the-sensitive-information-types-look-for.md).
  
## <a name="see-also"></a>Confira também

[O que os tipos de informações confidenciais procuram](what-the-sensitive-information-types-look-for.md)

