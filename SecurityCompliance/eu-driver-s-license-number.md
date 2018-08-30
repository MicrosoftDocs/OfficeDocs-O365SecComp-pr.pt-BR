---
title: Número de carteira de motorista da UE
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: 8/17/2018
ms.audience: Admin
ms.topic: reference
ms.service: o365-administration
localization_priority: Normal
ms.assetid: c3923cd3-ec84-435f-bf41-cadc37996a4b
description: Este tópico mostra o que uma política de prevenção (DLP) de perda de dados procura por quando ele detectar o tipo de informação confidencial número de carteira de motorista da UE. Esse tipo de informações confidenciais define diferentes padrões, palavras-chave e outras evidências para cada país.
ms.openlocfilehash: 065684249f9766d567c63e6b8170d36f56692e45
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22524018"
---
# <a name="eu-drivers-license-number"></a>Número de carteira de motorista da UE

Este tópico mostra o que uma política de prevenção (DLP) de perda de dados procura por quando ele detectar o tipo de informação confidencial número de carteira de motorista da UE. Esse tipo de informações confidenciais define diferentes padrões, palavras-chave e outras evidências para cada país.
  
## <a name="austria"></a>Áustria

### <a name="format"></a>Formato

Oito dígitos sem espaços e delimitadores
  
### <a name="pattern"></a>Padrão

Oito dígitos
  
### <a name="checksum"></a>Soma de verificação

Não
  
### <a name="definition"></a>Definição

Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:
  
- A expressão regular `Regex_austria_eu_driver's_license_number` encontra conteúdo que corresponde ao padrão. 
    
- Uma palavra-chave da `Keywords_austria_eu_driver's_license_number` for encontrado. 
    
```
<!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_austria_eu_driver's_license_number" />
          <Match idRef="Keywords_austria_eu_driver's_license_number" />
        </Pattern>
    </Entity>

```

### <a name="keywords"></a>Palavras-chave

| |
|**Keywords_austria_eu_driver's_license_number**|
|:-----|
|DL #  <br/> licença de driver  <br/> número de carteira de motorista  <br/> licença de driver  <br/> lic drivers.  <br/> carteira de motorista  <br/> licença de motorista  <br/> de motorista carteira  <br/> número de carteira de motorista  <br/> número de licença de motorista  <br/>  número de carteira de dirigir  <br/> dlno #  <br/> fuhrerschein  <br/> fuhrerschein republik osterreich  <br/> |
   
## <a name="belgium"></a>Bélgica

### <a name="format"></a>Formato

10 dígitos sem espaços e delimitadores
  
### <a name="pattern"></a>Padrão

10 dígitos
  
### <a name="checksum"></a>Soma de verificação

Não
  
### <a name="definition"></a>Definição

Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:
  
- A expressão regular `Regex_belgium_eu_driver's_license_number` encontra conteúdo que corresponde ao padrão. 
    
- Uma palavra-chave da `Keywords_belgium_eu_driver's_license_number` for encontrado. 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_belgium_eu_driver's_license_number" />
          <Match idRef="Keywords_belgium_eu_driver's_license_number" />
        </Pattern>
</Entity>

```

### <a name="keywords"></a>Palavras-chave

| |
|**Keywords__belgium_eu_driver's_license_number**|
|:-----|
|DL #  <br/> licença de driver  <br/> número de carteira de motorista  <br/> licença de driver  <br/> lic drivers.  <br/> carteira de motorista  <br/> drivers licence  <br/> de motorista carteira  <br/> número de carteira de motorista  <br/> número de licença de motorista  <br/> dlno #  <br/> rijbewijs  <br/> rijbewijsnummer  <br/> führerscheinnummer  <br/> fuhrerscheinnummer  <br/> fuehrerscheinnummer  <br/> führerschein-nr  <br/> fuehrerschein-Nr  <br/> fuehrerschein-nr  <br/> |
   
## <a name="bulgaria"></a>Bulgária

### <a name="format"></a>Formato

Nove dígitos sem espaços e delimitadores
  
### <a name="pattern"></a>Padrão

Nove dígitos
  
### <a name="checksum"></a>Soma de verificação

Não
  
### <a name="definition"></a>Definição

Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:
  
- A expressão regular `Regex_bulgaria_eu_driver's_license_number` encontra conteúdo que corresponde ao padrão. 
    
- Uma palavra-chave da `Keywords_bulgaria_eu_driver's_license_number` for encontrado. 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
             <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_bulgaria_eu_driver's_license_number" />
          <Match idRef="Keywords_bulgaria_eu_driver's_license_number" />
        </Pattern> 
</Entity>    

```

### <a name="keywords"></a>Palavras-chave

| |
|**Keywords_bulgaria_eu_driver's_license_number**|
|:-----|
|DL #  <br/> licença de driver  <br/> número de carteira de motorista  <br/> licença de driver  <br/> lic drivers.  <br/> carteira de motorista  <br/> drivers licence  <br/> de motorista carteira  <br/> número de carteira de motorista  <br/> número de licença de motorista  <br/> número de carteira de dirigir  <br/> dlno #  <br/> СВИДЕТЕЛСТВО ЗА УПРАВЛЕНИЕ НА МПС  <br/> СВИДЕТЕЛСТВО ЗА УПРАВЛЕНИЕ НА МОТОРНО ПРЕВОЗНО СРЕДСТВО  <br/> СУМПС  <br/> ШОФЬОРСКА КНИЖКА  <br/> |
   
## <a name="croatia"></a>Croácia

### <a name="format"></a>Formato

Oito dígitos sem espaços e delimitadores
  
### <a name="pattern"></a>Padrão

Oito dígitos
  
### <a name="checksum"></a>Soma de verificação

Não
  
### <a name="definition"></a>Definição

Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:
  
- A expressão regular `Regex_croatia_eu_driver's_license_number` encontra conteúdo que corresponde ao padrão. 
    
- Uma palavra-chave da `Keywords_croatia_eu_driver's_license_number` for encontrado. 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_croatia_eu_driver's_license_number" />
          <Match idRef="Keywords_croatia_eu_driver's_license_number" />
        </Pattern>
</Entity>

```

### <a name="keywords"></a>Palavras-chave

| |
|**Keywords_croatia_eu_driver's_license_number**|
|:-----|
|DL #  <br/> licença de driver  <br/> número de carteira de motorista  <br/> licença de driver  <br/> lic drivers.  <br/> carteira de motorista  <br/> drivers licence  <br/> de motorista carteira  <br/> número de carteira de motorista  <br/> número de licença de motorista  <br/> número de carteira de dirigir  <br/> dlno #  <br/> vozačka dozvola  <br/> |
   
## <a name="cyprus"></a>Chipre

### <a name="format"></a>Formato

12 dígitos sem espaços e delimitadores
  
### <a name="pattern"></a>Padrão

12 dígitos
  
### <a name="checksum"></a>Soma de verificação

Não
  
### <a name="definition"></a>Definição

Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:
  
- A expressão regular `Regex_cyprus_eu_driver's_license_number` encontra conteúdo que corresponde ao padrão. 
    
- Uma palavra-chave da `Keywords_cyprus_eu_driver's_license_number` for encontrado. 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_cyprus_eu_driver's_license_number" />
          <Match idRef="Keywords_cyprus_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Palavras-chave

| |
|**Keywords_cyprus_eu_driver's_license_number**|
|:-----|
|DL #  <br/> licença de driver  <br/> número de carteira de motorista  <br/> licença de driver  <br/> lic drivers.  <br/> carteira de motorista  <br/> drivers licence  <br/> número de carteira de motorista  <br/> número de licença de motorista  <br/> número de carteira de dirigir  <br/> dlno #  <br/> ΆΔΕΙΑ ΟΔΉΓΗΣΗΣ  <br/> |
   
## <a name="czech-republic"></a>República Tcheca

### <a name="format"></a>Formato

Duas letras seguidas de seis dígitos
  
### <a name="pattern"></a>Padrão

Oito letras e dígitos:
  
- Duas letras (não diferencia maiusculas de minúsculas)
    
- Um espaço (opcional)
    
- Seis dígitos
    
### <a name="checksum"></a>Soma de verificação

Não
  
### <a name="definition"></a>Definição

Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:
  
- A expressão regular `Regex_czech_republic_eu_driver's_license_number` encontra conteúdo que corresponde ao padrão. 
    
- Uma palavra-chave da `Keywords_czech_republic_eu_driver's_license_number` for encontrado. 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_czech_republic_eu_driver's_license_number" />
          <Match idRef="Keywords_czech_republic_eu_driver's_license_number" />
        </Pattern>
</Entity>

```

### <a name="keywords"></a>Palavras-chave

| |
|**Keywords_czech_republic_eu_driver's_license_number**|
|:-----|
|DL #  <br/> licença de driver  <br/> número de carteira de motorista  <br/> licença de driver  <br/> lic drivers.  <br/> carteira de motorista  <br/> drivers licence  <br/> de motorista carteira  <br/> número de carteira de motorista  <br/> número de carteira de motorista  <br/> número de licença de motorista  <br/> número de carteira de dirigir  <br/> dlno #  <br/> Řidičský prúkaz  <br/> |
   
## <a name="denmark"></a>Dinamarca

### <a name="format"></a>Formato

Oito dígitos sem espaços e delimitadores
  
### <a name="pattern"></a>Padrão

Oito dígitos
  
### <a name="checksum"></a>Soma de verificação

Sim
  
### <a name="definition"></a>Definição

Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:
  
- A expressão regular `Regex_denmark_eu_driver's_license_number` encontra conteúdo que corresponde ao padrão. 
    
- Uma palavra-chave da `Keywords_denmark_eu_driver's_license_number` for encontrado. 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_denmark_eu_driver's_license_number" />
          <Match idRef="Keywords_denmark_eu_driver's_license_number" />
        </Pattern>
</Entity>

```

### <a name="keywords"></a>Palavras-chave

| |
|**Keywords_denmark_eu_driver's_license_number**|
|:-----|
|DL #  <br/> licença de driver  <br/> número de carteira de motorista  <br/> licença de driver  <br/> lic drivers.  <br/> carteira de motorista  <br/> drivers licence  <br/> de motorista carteira  <br/> número de carteira de motorista  <br/> número de licença de motorista  <br/> número de carteira de dirigir  <br/> dlno #  <br/> kørekort  <br/> kørekortnummer  <br/> |
   
## <a name="estonia"></a>Estônia

### <a name="format"></a>Formato

Duas letras seguidas de seis dígitos
  
### <a name="pattern"></a>Padrão

Duas letras e seis dígitos:
  
-  As letras "ET" (não diferencia maiusculas de minúsculas) 
    
- Seis dígitos
    
### <a name="checksum"></a>Soma de verificação

Não
  
### <a name="definition"></a>Definição

Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:
  
- A expressão regular `Regex_estonia_eu_driver's_license_number` encontra conteúdo que corresponde ao padrão. 
    
- Uma palavra-chave da `Keywords_estonia_eu_driver's_license_number` for encontrado. 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_estonia_eu_driver's_license_number" />
          <Match idRef="Keywords_estonia_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Palavras-chave

| |
|**Keywords_estonia_eu_driver's_license_number**|
|:-----|
|DL #  <br/> licença de driver  <br/> número de carteira de motorista  <br/> número de carteira de motorista  <br/> licença de driver  <br/> lic drivers.  <br/> carteira de motorista  <br/> drivers licence  <br/> de motorista carteira  <br/> número de carteira de motorista  <br/> número de carteira de dirigir  <br/> dlno #  <br/> 
permis de conduire  <br/> |
   
## <a name="finland"></a>Finlândia

### <a name="format"></a>Formato

10 dígitos que contêm um hífen
  
### <a name="pattern"></a>Padrão

10 dígitos que contém um hífen:
  
-  Seis dígitos 
    
- Um hífen
    
-  Quatro dígitos 
    
### <a name="checksum"></a>Soma de verificação

Não
  
### <a name="definition"></a>Definição

Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:
  
- A expressão regular `Regex_finland_eu_driver's_license_number` encontra conteúdo que corresponde ao padrão. 
    
- Uma palavra-chave da `Keywords_finland_eu_driver's_license_number` for encontrado. 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_finland_eu_driver's_license_number" />
          <Match idRef="Keywords_finland_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Palavras-chave

| |
|**Keywords_finland_eu_driver's_license_number**|
|:-----|
|DL #  <br/> licença de driver  <br/> número de carteira de motorista  <br/> licença de driver  <br/> lic drivers.  <br/> carteira de motorista  <br/> drivers licence  <br/> de motorista carteira  <br/> número de carteira de motorista  <br/> número de licença de motorista  <br/> número de carteira de dirigir  <br/> dlno #  <br/> ajokortti  <br/> |
   
## <a name="france"></a>França

Para obter detalhes, consulte a seção "Número de carteira de motorista da França" nos [quais os tipos de informações confidenciais procurar](what-the-sensitive-information-types-look-for.md).
  
## <a name="germany"></a>Alemanha

Para obter detalhes, consulte a seção "Número de carteira de motorista da Alemanha" em [quais tipos de informações confidenciais a procurar](what-the-sensitive-information-types-look-for.md).
  
## <a name="greece"></a>Grécia

### <a name="format"></a>Formato

Nove dígitos sem espaços e delimitadores
  
### <a name="pattern"></a>Padrão

 Nove dígitos 
  
### <a name="checksum"></a>Soma de verificação

Não
  
### <a name="definition"></a>Definição

Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:
  
- A expressão regular `Regex_greece_eu_driver's_license_number` encontra conteúdo que corresponde ao padrão. 
    
- Uma palavra-chave da `Keywords_greece_eu_driver's_license_number` for encontrado. 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_greece_eu_driver's_license_number" />
          <Match idRef="Keywords_greece_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Palavras-chave

| |
|**Keywords_greece_eu_driver's_license_number**|
|:-----|
|dlL #  <br/> licença de driver  <br/> número de carteira de motorista  <br/> licença de driver  <br/> lic drivers.  <br/> carteira de motorista  <br/> drivers licence  <br/> de motorista carteira  <br/> número de carteira de motorista  <br/> número de licença de motorista  <br/> número de carteira de dirigir  <br/> dlno #  <br/> ΔΕΙΑ ΟΔΉΓΗΣΗΣ  <br/> Adeia odigisis  <br/> |
   
## <a name="hungary"></a>Hungria

### <a name="format"></a>Formato

Duas letras seguidas de seis dígitos
  
### <a name="pattern"></a>Padrão

Duas letras e seis dígitos:
  
-  Duas letras (não diferencia maiusculas de minúsculas) 
    
- Seis dígitos
    
### <a name="checksum"></a>Soma de verificação

Não
  
### <a name="definition"></a>Definição

Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:
  
- A expressão regular `Regex_hungary_eu_driver's_license_number` encontra conteúdo que corresponde ao padrão. 
    
- Uma palavra-chave da `Keywords_hungary_eu_driver's_license_number` for encontrado. 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_hungary_eu_driver's_license_number" />
          <Match idRef="Keywords_hungary_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Palavras-chave

| |
|**Keywords_hungary_eu_driver's_license_number**|
|:-----|
|DL #  <br/> licença de driver  <br/> número de carteira de motorista  <br/> licença de driver  <br/> lic drivers.  <br/> carteira de motorista  <br/> drivers licence  <br/> de motorista carteira  <br/> número de carteira de motorista  <br/> número de licença de motorista  <br/> número de carteira de dirigir  <br/> dlno #  <br/> vezetoi engedely  <br/> |
   
## <a name="ireland"></a>Irlanda

### <a name="format"></a>Formato

Seis dígitos seguidos por quatro letras
  
### <a name="pattern"></a>Padrão

Seis dígitos e quatro letras:
  
- Seis dígitos
    
- Quatro letras (não diferencia maiusculas de minúsculas)
    
### <a name="checksum"></a>Soma de verificação

Não
  
### <a name="definition"></a>Definição

Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:
  
- A expressão regular `Regex_ireland_eu_driver's_license_number` encontra conteúdo que corresponde ao padrão. 
    
- Uma palavra-chave da `Keywords_ireland_eu_driver's_license_number` for encontrado. 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_ireland_eu_driver's_license_number" />
          <Match idRef="Keywords_ireland_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Palavras-chave

| |
|**Keywords_ireland_eu_driver's_license_number**|
|:-----|
|DL #  <br/> licença de driver  <br/> número de carteira de motorista  <br/> licença de driver  <br/> lic drivers.  <br/> carteira de motorista  <br/> drivers licence  <br/> de motorista carteira  <br/> número de carteira de motorista  <br/> número de licença de motorista  <br/> número de carteira de dirigir  <br/> dlno #  <br/> ceadúnas tiomána  <br/> |
   
## <a name="italy"></a>Itália

Para obter detalhes, consulte a seção "Número de carteira de motorista da Itália" nos [quais os tipos de informações confidenciais procurar](what-the-sensitive-information-types-look-for.md).
  
## <a name="latvia"></a>Letônia

### <a name="format"></a>Formato

Três letras seguidas de seis dígitos
  
### <a name="pattern"></a>Padrão

Três letras e seis dígitos:
  
-  Três letras (não diferencia maiusculas de minúsculas) 
    
- Seis dígitos
    
### <a name="checksum"></a>Soma de verificação

Não
  
### <a name="definition"></a>Definição

Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:
  
- A expressão regular `Regex_latvia_eu_driver's_license_number` encontra conteúdo que corresponde ao padrão. 
    
- Uma palavra-chave da `Keywords_latvia_eu_driver's_license_number` for encontrado. 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_latvia_eu_driver's_license_number" />
          <Match idRef="Keywords_latvia_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Palavras-chave

| |
|**Keywords_latvia_eu_driver's_license_number**|
|:-----|
|DL #  <br/> licença de driver  <br/> número de carteira de motorista  <br/> licença de driver  <br/> lic drivers.  <br/> carteira de motorista  <br/> drivers licence  <br/> de motorista carteira  <br/> número de carteira de motorista  <br/> número de licença de motorista  <br/> número de carteira de dirigir  <br/> dlno #  <br/> autovadītāja apliecība  <br/> |
   
## <a name="lithuania"></a>Lituânia

### <a name="format"></a>Formato

Oito dígitos sem espaços e delimitadores
  
### <a name="pattern"></a>Padrão

 Oito dígitos 
  
### <a name="checksum"></a>Soma de verificação

Não
  
### <a name="definition"></a>Definição

Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:
  
- A expressão regular `Regex_lithuania_eu_driver's_license_number` encontra conteúdo que corresponde ao padrão. 
    
- Uma palavra-chave da `Keywords_lithuania_eu_driver's_license_number` for encontrado. 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_lithuania_eu_driver's_license_number" />
          <Match idRef="Keywords_lithuania_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Palavras-chave

| |
|**Keywords_lithuania_eu_driver's_license_number**|
|:-----|
|DL #  <br/> licença de driver  <br/> número de carteira de motorista  <br/> licença de driver  <br/> lic drivers.  <br/> carteira de motorista  <br/> drivers licence  <br/> de motorista carteira  <br/> número de carteira de motorista  <br/> número de licença de motorista  <br/> número de carteira de dirigir  <br/> dlno #  <br/> vairuotojo pažymėjimas  <br/> |
   
## <a name="luxemburg"></a>Luxemburgo

### <a name="format"></a>Formato

Seis dígitos sem espaços e delimitadores
  
### <a name="pattern"></a>Padrão

 Seis dígitos 
  
### <a name="checksum"></a>Soma de verificação

Não
  
### <a name="definition"></a>Definição

Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:
  
- A expressão regular `Regex_luxemburg_eu_driver's_license_number` encontra conteúdo que corresponde ao padrão. 
    
- Uma palavra-chave da `Keywords_luxemburg_eu_driver's_license_number` for encontrado. 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_luxemburg_eu_driver's_license_number" />
          <Match idRef="Keywords_luxemburg_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Palavras-chave

| |
|**Keywords_luxemburg_eu_driver's_license_number**|
|:-----|
|DL #  <br/> licença de driver  <br/> número de carteira de motorista  <br/> licença de driver  <br/> lic drivers.  <br/> carteira de motorista  <br/> drivers licence  <br/> de motorista carteira  <br/> número de carteira de motorista  <br/> número de licença de motorista  <br/> número de carteira de dirigir  <br/> dlno #  <br/> fahrerlaubnis  <br/> |
   
## <a name="malta"></a>Malta

### <a name="format"></a>Formato

Combinação de dois caracteres e seis dígitos no padrão especificado
  
### <a name="pattern"></a>Padrão

Combinação de dois caracteres e seis dígitos:
  
- Dois caracteres (dígitos ou letras, não diferencia maiusculas de minúsculas)
    
- Um espaço (opcional)
    
- Três dígitos
    
- Um espaço (opcional)
    
- Três dígitos
    
### <a name="checksum"></a>Soma de verificação

Não
  
### <a name="definition"></a>Definição

Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:
  
- A expressão regular `Regex_malta_eu_driver's_license_number` encontra conteúdo que corresponde ao padrão. 
    
- Uma palavra-chave da `Keywords_malta_eu_driver's_license_number` for encontrado. 
    
```
<!-- EU Driver's License Number -->
 <Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_malta_eu_driver's_license_number" />
          <Match idRef="Keywords_malta_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Palavras-chave

| |
|**Keywords_malta_eu_driver's_license_number**|
|:-----|
|DL #  <br/> licença de driver  <br/> número de carteira de motorista  <br/> licença de driver  <br/> lic drivers.  <br/> carteira de motorista  <br/> drivers licence  <br/> de motorista carteira  <br/> número de carteira de motorista  <br/> número de licença de motorista  <br/> número de carteira de dirigir  <br/> dlno #  <br/> tarefa liċenzja-sewqan  <br/> |
   
## <a name="netherlands"></a>Países Baixos

### <a name="format"></a>Formato

10 dígitos sem espaços e delimitadores
  
### <a name="pattern"></a>Padrão

10 dígitos
  
### <a name="checksum"></a>Soma de verificação

Não
  
### <a name="definition"></a>Definição

Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:
  
- A expressão regular `Regex_netherlands_eu_driver's_license_number` encontra conteúdo que corresponde ao padrão. 
    
- Uma palavra-chave da `Keywords_netherlands_eu_driver's_license_number` for encontrado. 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_netherlands_eu_driver's_license_number" />
          <Match idRef="Keywords_netherlands_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Palavras-chave

| |
|**Keywords_netherlands_eu_driver's_license_number**|
|:-----|
|DL #  <br/> licença de driver  <br/> número de carteira de motorista  <br/> licença de driver  <br/> lic drivers.  <br/> carteira de motorista  <br/> drivers licence  <br/> de motorista carteira  <br/> número de carteira de motorista  <br/> número de licença de motorista  <br/> número de carteira de dirigir  <br/> dlno #  <br/> 
permis de conduire  <br/> rijbewijs  <br/> rijbewijsnummer  <br/> |
   
## <a name="poland"></a>Polônia

### <a name="format"></a>Formato

14 dígitos contendo 2 barras
  
### <a name="pattern"></a>Padrão

14 dígitos e 2 barras:
  
-  Cinco dígitos 
    
- Uma barra
    
- Dois dígitos
    
- Uma barra
    
- Sete dígitos
    
### <a name="checksum"></a>Soma de verificação

Não
  
### <a name="definition"></a>Definição

Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:
  
- A expressão regular `Regex_poland_eu_driver's_license_number` encontra conteúdo que corresponde ao padrão. 
    
- Uma palavra-chave da `Keywords_poland_eu_driver's_license_number` for encontrado. 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_poland_eu_driver's_license_number" />
          <Match idRef="Keywords_poland_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Palavras-chave

| |
|**Keywords_poland_eu_driver's_license_number**|
|:-----|
|DL #  <br/> licença de driver  <br/> número de carteira de motorista  <br/> licença de driver  <br/> lic drivers.  <br/> carteira de motorista  <br/> drivers licence  <br/> de motorista carteira  <br/> número de carteira de motorista  <br/> número de licença de motorista  <br/> número de carteira de dirigir  <br/> dlno #  <br/> prawo jazdy  <br/> |
   
## <a name="portugal"></a>Portugal

### <a name="format"></a>Formato

Duas letras seguidas por um sete números no padrão especificado
  
### <a name="pattern"></a>Padrão

Duas letras seguidas por sete números com caracteres especiais:
  
-  Duas letras (não diferencia maiusculas de minúsculas) 
    
- Um hífen
    
- Seis dígitos
    
- Um espaço
    
- Um dígito
    
### <a name="checksum"></a>Soma de verificação

Não
  
### <a name="definition"></a>Definição

Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:
  
- A expressão regular `Regex_portugal_eu_driver's_license_number` encontra conteúdo que corresponde ao padrão. 
    
- Uma palavra-chave da `Keywords_portugal_eu_driver's_license_number` for encontrado. 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_portugal_eu_driver's_license_number" />
          <Match idRef="Keywords_portugal_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Palavras-chave

| |
|**Keywords_portugal_eu_driver's_license_number**|
|:-----|
|DL #  <br/> licença de driver  <br/> número de carteira de motorista  <br/> licença de driver  <br/> lic drivers.  <br/> carteira de motorista  <br/> drivers licence  <br/> de motorista carteira  <br/> número de carteira de motorista  <br/> número de licença de motorista  <br/> número de carteira de dirigir  <br/> dlno #  <br/> carteira de motorista  <br/> |
   
## <a name="romania"></a>Romênia

### <a name="format"></a>Formato

Um caractere seguido oito dígitos
  
### <a name="pattern"></a>Padrão

Um caractere seguido oito dígitos:
  
-  Uma letra (não diferencia maiusculas de minúsculas) ou dígito 
    
- Oito dígitos
    
### <a name="checksum"></a>Soma de verificação

Não
  
### <a name="definition"></a>Definição

Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:
  
- A expressão regular `Regex_romania_eu_driver's_license_number` encontra conteúdo que corresponde ao padrão. 
    
- Uma palavra-chave da `Keywords_romania_eu_driver's_license_number` for encontrado. 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_romania_eu_driver's_license_number" />
          <Match idRef="Keywords_romania_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Palavras-chave

| |
|**Keywords_romania_eu_driver's_license_number**|
|:-----|
|DL #  <br/> licença de driver  <br/> número de carteira de motorista  <br/> licença de driver  <br/> lic drivers.  <br/> carteira de motorista  <br/> drivers licence  <br/> de motorista carteira  <br/> número de carteira de motorista  <br/> número de licença de motorista  <br/> número de carteira de dirigir  <br/> dlno #  <br/> permis de conducere  <br/> |
   
## <a name="slovakia"></a>Eslováquia

### <a name="format"></a>Formato

Um caractere seguido por sete dígitos
  
### <a name="pattern"></a>Padrão

Um caractere seguido por sete dígitos
  
- Uma letra (não diferencia maiusculas de minúsculas) ou dígito
    
-  Sete dígitos 
    
### <a name="checksum"></a>Soma de verificação

Não
  
### <a name="definition"></a>Definição

Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:
  
- A expressão regular `Regex_slovakia_eu_driver's_license_number` encontra conteúdo que corresponde ao padrão. 
    
- Uma palavra-chave da `Keywords_slovakia_eu_driver's_license_number` for encontrado. 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_slovaknia_eu_driver's_license_number" />
          <Match idRef="Keywords_slovakia_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Palavras-chave

| |
|**Keywords_slovakia_eu_driver's_license_number**|
|:-----|
|DL #  <br/> licença de driver  <br/> número de carteira de motorista  <br/> licença de driver  <br/> lic drivers.  <br/> carteira de motorista  <br/> drivers licence  <br/> de motorista carteira  <br/> número de carteira de motorista  <br/> número de licença de motorista  <br/> número de carteira de dirigir  <br/> dlno #  <br/> vodičský preukaz  <br/> |
   
## <a name="slovenia"></a>Eslovênia

### <a name="format"></a>Formato

Nove dígitos sem espaços e delimitadores
  
### <a name="pattern"></a>Padrão

Nove dígitos
  
### <a name="checksum"></a>Soma de verificação

Não
  
### <a name="definition"></a>Definição

Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:
  
- A expressão regular `Regex_slovenia_eu_driver's_license_number` encontra conteúdo que corresponde ao padrão. 
    
- Uma palavra-chave da `Keywords_slovenia_eu_driver's_license_number` for encontrado. 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_slovenia_eu_driver's_license_number" />
          <Match idRef="Keywords_slovenia_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Palavras-chave

| |
|**Keywords_slovenia_eu_driver's_license_number**|
|:-----|
|DL #  <br/> licença de driver  <br/> número de carteira de motorista  <br/> licença de driver  <br/> lic drivers.  <br/> carteira de motorista  <br/> drivers licence  <br/> de motorista carteira  <br/> número de carteira de motorista  <br/> número de licença de motorista  <br/> número de carteira de dirigir  <br/> dlno #  <br/> vozniško dovoljenje  <br/> |
   
## <a name="spain"></a>Espanha

### <a name="format"></a>Formato

Oito dígitos seguidos por um caractere
  
### <a name="pattern"></a>Padrão

Oito dígitos seguidos por um caractere:
  
-  Oito dígitos 
    
- Um dígito ou carta (não diferencia maiusculas de minúsculas)
    
### <a name="checksum"></a>Soma de verificação

Sim
  
### <a name="definition"></a>Definição

Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:
  
- A função `Func_spain_eu_driver's_license_number` encontra conteúdo que corresponde ao padrão. 
    
- Uma palavra-chave da `Keywords_spain_eu_driver's_license_number` for encontrado. 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Func_spain_eu_driver's_license_number" />
          <Match idRef="Keywords_spain_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Palavras-chave

| |
|**Keywords_spain_eu_driver's_license_number**|
|:-----|
|dlno #  <br/> DL #  <br/> lic drivers.  <br/> licença de driver  <br/> licença de driver  <br/> drivers licence  <br/> 
drivers license  <br/> licença de motorista  <br/> de motorista carteira  <br/> driving licence
  <br/> orientando licença  <br/> número de carteira de licença  <br/> número de carteira de motorista  <br/> número de licenciar drivers  <br/> número de carteira de drivers  <br/> número de licença de motorista  <br/> número de carteira de motorista  <br/> número de licença driving  <br/> número de carteira de dirigir  <br/> orientando permitir  <br/> número de permitir que controla  <br/> permiso de conducción  <br/> permiso conducción  <br/> número licencia conducir  <br/> número de carnet de conducir  <br/> número carnet conducir  <br/> licencia conducir  <br/> número de permiso de conducir  <br/> número de permiso conducir  <br/> número permiso conducir  <br/> permiso conducir  <br/> licencia de manejo  <br/> el carnet de conducir  <br/> carnet conducir  <br/> |
   
## <a name="sweden"></a>Suécia

### <a name="format"></a>Formato

Dez dígitos que contém um hífen
  
### <a name="pattern"></a>Padrão

Dez dígitos que contém um hífen:
  
-  Seis dígitos 
    
- Um hífen
    
- Quatro dígitos
    
### <a name="checksum"></a>Soma de verificação

Não
  
### <a name="definition"></a>Definição

Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:
  
- A expressão regular `Regex_sweden_eu_driver's_license_number` encontra conteúdo que corresponde ao padrão. 
    
- Uma palavra-chave da `Keywords_sweden_eu_driver's_license_number` for encontrado. 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_sweden_eu_driver's_license_number" />
          <Match idRef="Keywords_sweden_eu_driver's_license_number" />
        </Pattern>
</Entity> 
```

### <a name="keywords"></a>Palavras-chave

| |
|**Keywords_sweden_eu_driver's_license_number**|
|:-----|
|DL #  <br/> licença de driver  <br/> número de carteira de motorista  <br/> licença de driver  <br/> lic drivers.  <br/> carteira de motorista  <br/> drivers licence  <br/> de motorista carteira  <br/> número de carteira de motorista  <br/> número de licença de motorista  <br/> número de carteira de dirigir  <br/> dlno #  <br/> körkort  <br/> |
   
## <a name="uk"></a>REINO UNIDO

Para obter detalhes, consulte a seção "Número de carteira de motorista do Reino Unido" nos [quais os tipos de informações confidenciais procurar](what-the-sensitive-information-types-look-for.md).
  
## <a name="see-also"></a>Confira também

[O que os tipos de informações confidenciais procuram](what-the-sensitive-information-types-look-for.md)

