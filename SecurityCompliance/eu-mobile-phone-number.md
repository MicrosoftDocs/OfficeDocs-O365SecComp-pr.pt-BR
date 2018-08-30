---
title: Número de telefone celular da UE
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: 8/16/2018
ms.audience: Admin
ms.topic: reference
ms.service: o365-administration
localization_priority: Normal
ms.assetid: 555e7675-2ae8-42d1-9b8e-2c8f8cd21337
description: Prevenção de perda de dados (DLP) no Office 365 Security &amp; Centro de conformidade inclui muitos tipos de informações confidenciais que estão prontos para uso em suas políticas de DLP. Este tópico descreve o tipo de informações confidenciais da UE número de telefone celular.
ms.openlocfilehash: d0818759dae8ed86cc9aef6f7fad48cbd2acf24f
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22523960"
---
# <a name="eu-mobile-phone-number"></a>Número de telefone celular da UE

Prevenção de perda de dados (DLP) no Office 365 Security &amp; Centro de conformidade inclui muitos tipos de informações confidenciais que estão prontos para uso em suas políticas de DLP. Este tópico descreve o tipo de informações confidenciais da UE número de telefone celular. 
  
## <a name="austria"></a>Áustria

### <a name="format"></a>Formato

Dígitos sem comprimentos standard
  
### <a name="pattern"></a>Padrão

-  Dígitos 
    
### <a name="definition"></a>Definição

Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:
  
- A expressão regular `Regex_austria_eu_mobile_number` encontra conteúdo que corresponde ao padrão. 
    
- A expressão regular `Regex_austria_eu_formatted_mobile_number` encontra conteúdo que corresponde ao padrão. 
    
- Uma palavra-chave da `Keywords_austria_eu_mobile_number` for encontrado. 
    
```
 
<Entity id="a56a0418-136a-41ea-a337-4d0388b28e69" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_austria_eu_mobile_number"/>
          <Match idRef="Keywords_austria_eu_mobile_number" />
        </Pattern>
<Pattern confidenceLevel="75">
<IdMatch idRef="Regex_austria_eu_formatted_mobile_number" />
          </Pattern>
</Entity>
```

## <a name="belgium"></a>Bélgica

### <a name="pattern"></a>Padrão

-  Dígitos 
    
### <a name="definition"></a>Definição

Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:
  
- A expressão regular `Regex_belgium_eu_mobile_number` encontra conteúdo que corresponde ao padrão. 
    
- A expressão regular `Regex_belgium_eu_formatted_mobile_number` encontra conteúdo que corresponde ao padrão. 
    
- Uma palavra-chave da `Keywords_belgium_eu_mobile_number` for encontrado. 
    
```
 
<Entity id="a56a0418-136a-41ea-a337-4d0388b28e69" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_belgium_eu_mobile_number"/>
          <Match idRef="Keywords_belgium_eu_mobile_number" />
        </Pattern>
<Pattern confidenceLevel="75">
<IdMatch idRef="Regex_belgium_eu_formatted_mobile_number" />
          </Pattern>
</Entity>
```

## <a name="bulgaria"></a>Bulgária

### <a name="pattern"></a>Padrão

-  Dígitos 
    
### <a name="definition"></a>Definição

Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:
  
- A expressão regular `Regex_bulgaria_eu_mobile_number` encontra conteúdo que corresponde ao padrão. 
    
- A expressão regular `Regex_bulgaria_eu_formatted_mobile_number` encontra conteúdo que corresponde ao padrão. 
    
- Uma palavra-chave da `Keywords_bulgaria_eu_mobile_number` for encontrado. 
    
```
 
<Entity id="a56a0418-136a-41ea-a337-4d0388b28e69" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_bulgaria_eu_mobile_number"/>
          <Match idRef="Keywords_bulgaria_eu_mobile_number" />
        </Pattern>
<Pattern confidenceLevel="75">
<IdMatch idRef="Regex_bulgaria_eu_formatted_mobile_number" />
          </Pattern>
</Entity>
```

## <a name="croatia"></a>Croácia

### <a name="pattern"></a>Padrão

-  Dígitos 
    
### <a name="definition"></a>Definição

Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:
  
- A expressão regular `Regex_croatia_eu_mobile_number` encontra conteúdo que corresponde ao padrão. 
    
- A expressão regular `Regex_croatia_eu_formatted_mobile_number` encontra conteúdo que corresponde ao padrão. 
    
- Uma palavra-chave da `Keywords_croatia_eu_mobile_number` for encontrado. 
    
```
<Entity id="a56a0418-136a-41ea-a337-4d0388b28e69" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_croatia_eu_mobile_number"/>
          <Match idRef="Keywords_croatia_eu_mobile_number" />
        </Pattern>
<Pattern confidenceLevel="75">
<IdMatch idRef="Regex_croatia_eu_formatted_mobile_number" />
          </Pattern>
</Entity>
```

## <a name="cyprus"></a>Chipre

### <a name="pattern"></a>Padrão

-  Dígitos 
    
### <a name="checksum"></a>Soma de verificação

Não aplicável
  
### <a name="definition"></a>Definição

Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:
  
- A expressão regular `Regex_cyprus_eu_mobile_number` encontra conteúdo que corresponde ao padrão. 
    
- A expressão regular `Regex_cyprus_eu_formatted_mobile_number` encontra conteúdo que corresponde ao padrão. 
    
- Uma palavra-chave da `Keywords_cyprus_eu_mobile_number` for encontrado. 
    
```
 
<Entity id="a56a0418-136a-41ea-a337-4d0388b28e69" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_cyprus_eu_mobile_number"/>
          <Match idRef="Keywords_cyprus_eu_mobile_number" />
        </Pattern>
<Pattern confidenceLevel="75">
<IdMatch idRef="Regex_cyprus_eu_formatted_mobile_number" />
          </Pattern>
</Entity>
```

## <a name="czech-republic"></a>República Tcheca

### <a name="pattern"></a>Padrão

-  Dígitos 
    
### <a name="checksum"></a>Soma de verificação

Não aplicável
  
### <a name="definition"></a>Definição

Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:
  
- A expressão regular `Regex_czech_republic_eu_mobile_number` encontra conteúdo que corresponde ao padrão. 
    
- A expressão regular `Regex_czech_republic_eu_formatted_mobile_number` encontra conteúdo que corresponde ao padrão. 
    
- Uma palavra-chave da `Keywords_czech_republic_eu_mobile_number` for encontrado. 
    
```
 
<Entity id="a56a0418-136a-41ea-a337-4d0388b28e69" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_czech_republic_eu_mobile_number"/>
          <Match idRef="Keywords_czech_republic_eu_mobile_number" />
        </Pattern>
<Pattern confidenceLevel="75">
<IdMatch idRef="Regex_czech_republic_eu_formatted_mobile_number" />
          </Pattern>
</Entity>
```

## <a name="denmark"></a>Dinamarca

### <a name="pattern"></a>Padrão

-  Dígitos 
    
### <a name="checksum"></a>Soma de verificação

Não aplicável
  
### <a name="definition"></a>Definição

Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:
  
- A expressão regular `Regex_denmark_eu_mobile_number` encontra conteúdo que corresponde ao padrão. 
    
- A expressão regular `Regex_denmark_eu_formatted_mobile_number` encontra conteúdo que corresponde ao padrão. 
    
- Uma palavra-chave da `Keywords_denmark_eu_mobile_number` for encontrado. 
    
```
 
<Entity id="a56a0418-136a-41ea-a337-4d0388b28e69" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_denmark_eu_mobile_number"/>
          <Match idRef="Keywords_denmark_eu_mobile_number" />
        </Pattern>
<Pattern confidenceLevel="75">
<IdMatch idRef="Regex_denmark_eu_formatted_mobile_number" />
          </Pattern>
</Entity>
```

## <a name="estonia"></a>Estônia

### <a name="pattern"></a>Padrão

-  Dígitos 
    
### <a name="checksum"></a>Soma de verificação

Não aplicável
  
### <a name="definition"></a>Definição

Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:
  
- A expressão regular `Regex_estonia_eu_mobile_number` encontra conteúdo que corresponde ao padrão. 
    
- A expressão regular `Regex_estonia_eu_formatted_mobile_number` encontra conteúdo que corresponde ao padrão. 
    
- Uma palavra-chave da `Keywords_estonia_eu_mobile_number` for encontrado. 
    
```
<Entity id="a56a0418-136a-41ea-a337-4d0388b28e69" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_estonia_eu_mobile_number"/>
          <Match idRef="Keywords_estonia_eu_mobile_number" />
        </Pattern>
<Pattern confidenceLevel="75">
<IdMatch idRef="Regex_estonia_eu_formatted_mobile_number" />
          </Pattern>
</Entity>
```

## <a name="finland"></a>Finlândia

### <a name="pattern"></a>Padrão

-  Dígitos 
    
### <a name="checksum"></a>Soma de verificação

Não aplicável
  
### <a name="definition"></a>Definição

Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:
  
- A expressão regular `Regex_finland_eu_mobile_number` encontra conteúdo que corresponde ao padrão. 
    
- A expressão regular `Regex_finland_eu_formatted_mobile_number` encontra conteúdo que corresponde ao padrão. 
    
- Uma palavra-chave da `Keywords_finland_eu_mobile_number` for encontrado. 
    
```
 
<Entity id="a56a0418-136a-41ea-a337-4d0388b28e69" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_finland_eu_mobile_number"/>
          <Match idRef="Keywords_finland_eu_mobile_number" />
        </Pattern>
<Pattern confidenceLevel="75">
<IdMatch idRef="Regex_finland_eu_formatted_mobile_number" />
          </Pattern>
</Entity>
```

## <a name="france"></a>França

### <a name="pattern"></a>Padrão

-  Dígitos 
    
### <a name="checksum"></a>Soma de verificação

Não aplicável
  
### <a name="definition"></a>Definição

Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:
  
- A expressão regular `Regex_france_eu_mobile_number` encontra conteúdo que corresponde ao padrão. 
    
- A expressão regular `Regex_france_eu_formatted_mobile_number` encontra conteúdo que corresponde ao padrão. 
    
- Uma palavra-chave da `Keywords_france_eu_mobile_number` for encontrado. 
    
```
 
<Entity id="a56a0418-136a-41ea-a337-4d0388b28e69" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_france_eu_mobile_number"/>
          <Match idRef="Keywords_france_eu_mobile_number" />
        </Pattern>
<Pattern confidenceLevel="75">
<IdMatch idRef="Regex_france_eu_formatted_mobile_number" />
          </Pattern>
</Entity>
```

## <a name="germany"></a>Alemanha

### <a name="pattern"></a>Padrão

-  Dígitos 
    
### <a name="checksum"></a>Soma de verificação

Não aplicável
  
### <a name="definition"></a>Definição

Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:
  
- A expressão regular `Regex_germany_eu_mobile_number` encontra conteúdo que corresponde ao padrão. 
    
- A expressão regular `Regex_germany_eu_formatted_mobile_number` encontra conteúdo que corresponde ao padrão. 
    
- Uma palavra-chave da `Keywords_germany_eu_mobile_number` for encontrado. 
    
```
 
<Entity id="a56a0418-136a-41ea-a337-4d0388b28e69" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_germany_eu_mobile_number"/>
          <Match idRef="Keywords_germany_eu_mobile_number" />
        </Pattern>
<Pattern confidenceLevel="75">
<IdMatch idRef="Regex_germany_eu_formatted_mobile_number" />
          </Pattern>
</Entity>
```

## <a name="greece"></a>Grécia

### <a name="pattern"></a>Padrão

-  Dígitos 
    
### <a name="checksum"></a>Soma de verificação

Não aplicável
  
### <a name="definition"></a>Definição

Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:
  
- A expressão regular `Regex_greece_eu_mobile_number` encontra conteúdo que corresponde ao padrão. 
    
- A expressão regular `Regex_greece_eu_formatted_mobile_number` encontra conteúdo que corresponde ao padrão. 
    
- Uma palavra-chave da `Keywords_greece_eu_mobile_number` for encontrado. 
    
```
 
<Entity id="a56a0418-136a-41ea-a337-4d0388b28e69" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_greece_eu_mobile_number"/>
          <Match idRef="Keywords_greece_eu_mobile_number" />
        </Pattern>
<Pattern confidenceLevel="75">
<IdMatch idRef="Regex_greece_eu_formatted_mobile_number" />
          </Pattern>
</Entity>
```

## <a name="hungary"></a>Hungria

### <a name="pattern"></a>Padrão

-  Dígitos 
    
### <a name="checksum"></a>Soma de verificação

Não aplicável
  
### <a name="definition"></a>Definição

Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:
  
- A expressão regular `Regex_hungary_eu_mobile_number` encontra conteúdo que corresponde ao padrão. 
    
- A expressão regular `Regex_hungary_eu_formatted_mobile_number` encontra conteúdo que corresponde ao padrão. 
    
- Uma palavra-chave da `Keywords_hungary_eu_mobile_number` for encontrado. 
    
```
<Entity id="a56a0418-136a-41ea-a337-4d0388b28e69" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_hungary_eu_mobile_number"/>
          <Match idRef="Keywords_hungary_eu_mobile_number" />
        </Pattern>
<Pattern confidenceLevel="75">
<IdMatch idRef="Regex_hungary_eu_formatted_mobile_number" />
          </Pattern>
</Entity>
```

## <a name="ireland"></a>Irlanda

### <a name="pattern"></a>Padrão

-  Dígitos 
    
### <a name="checksum"></a>Soma de verificação

Não aplicável
  
### <a name="definition"></a>Definição

Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:
  
- A expressão regular `Regex_ireland_eu_mobile_number` encontra conteúdo que corresponde ao padrão. 
    
- A expressão regular `Regex_ireland_eu_formatted_mobile_number` encontra conteúdo que corresponde ao padrão. 
    
- Uma palavra-chave da `Keywords_ireland_eu_mobile_number` for encontrado. 
    
```
 
<Entity id="a56a0418-136a-41ea-a337-4d0388b28e69" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_ireland_eu_mobile_number"/>
          <Match idRef="Keywords_ireland_eu_mobile_number" />
        </Pattern>
<!-- Strictly formatted patterns without mandatory corroborative evidence -->
<Pattern confidenceLevel="75">
<IdMatch idRef="Regex_ireland_eu_formatted_mobile_number" />
          </Pattern>
</Entity>
```

## <a name="italy"></a>Itália

### <a name="pattern"></a>Padrão

-  Dígitos 
    
### <a name="checksum"></a>Soma de verificação

Não aplicável
  
### <a name="definition"></a>Definição

Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:
  
- A expressão regular `Regex_italy_eu_mobile_number` encontra conteúdo que corresponde ao padrão. 
    
- A expressão regular `Regex_italy_eu_formatted_mobile_number` encontra conteúdo que corresponde ao padrão. 
    
- Uma palavra-chave da `Keywords_italy_eu_mobile_number` for encontrado. 
    
```
 
<Entity id="a56a0418-136a-41ea-a337-4d0388b28e69" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_italy_eu_mobile_number"/>
          <Match idRef="Keywords_italy_eu_mobile_number" />
        </Pattern>
<!-- Strictly formatted patterns without mandatory corroborative evidence -->
<Pattern confidenceLevel="75">
<IdMatch idRef="Regex_italy_eu_formatted_mobile_number" />
          </Pattern>
</Entity>
```

## <a name="latvia"></a>Letônia

### <a name="pattern"></a>Padrão

-  Dígitos 
    
### <a name="checksum"></a>Soma de verificação

Não aplicável
  
### <a name="definition"></a>Definição

Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:
  
- A expressão regular `Regex_latvia_eu_mobile_number` encontra conteúdo que corresponde ao padrão. 
    
- A expressão regular `Regex_latvia_eu_formatted_mobile_number` encontra conteúdo que corresponde ao padrão. 
    
- Uma palavra-chave da `Keywords_latvia_eu_mobile_number` for encontrado. 
    
```
 
<Entity id="a56a0418-136a-41ea-a337-4d0388b28e69" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_latvia_eu_mobile_number"/>
          <Match idRef="Keywords_latvia_eu_mobile_number" />
        </Pattern>
<Pattern confidenceLevel="75">
<IdMatch idRef="Regex_latvia_eu_formatted_mobile_number" />
          </Pattern>
</Entity>
```

## <a name="lithuania"></a>Lituânia

### <a name="pattern"></a>Padrão

-  Dígitos 
    
### <a name="checksum"></a>Soma de verificação

Não aplicável
  
### <a name="definition"></a>Definição

Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:
  
- A expressão regular `Regex_lithuania_eu_mobile_number` encontra conteúdo que corresponde ao padrão. 
    
- A expressão regular `Regex_lithuania_eu_formatted_mobile_number` encontra conteúdo que corresponde ao padrão. 
    
- Uma palavra-chave da `Keywords_lithuania_eu_mobile_number` for encontrado. 
    
```
 
<Entity id="a56a0418-136a-41ea-a337-4d0388b28e69" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_lithuania_eu_mobile_number"/>
          <Match idRef="Keywords_lithuania_eu_mobile_number" />
        </Pattern>
<Pattern confidenceLevel="75">
<IdMatch idRef="Regex_lithuania_eu_formatted_mobile_number" />
          </Pattern>
</Entity>
```

## <a name="luxemburg"></a>Luxemburgo

### <a name="pattern"></a>Padrão

-  Dígitos 
    
### <a name="checksum"></a>Soma de verificação

Não aplicável
  
### <a name="definition"></a>Definição

Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:
  
- A expressão regular `Regex_luxumburg_eu_mobile_number` encontra conteúdo que corresponde ao padrão. 
    
- A expressão regular `Regex_luxumburg_eu_formatted_mobile_number` encontra conteúdo que corresponde ao padrão. 
    
- Uma palavra-chave da `Keywords_luxumburg_eu_mobile_number` for encontrado. 
    
```
 
<Entity id="a56a0418-136a-41ea-a337-4d0388b28e69" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_luxumburg_eu_mobile_number"/>
          <Match idRef="Keywords_luxumburg_eu_mobile_number" />
        </Pattern>
<Pattern confidenceLevel="75">
<IdMatch idRef="Regex_luxumburg_eu_formatted_mobile_number" />
          </Pattern>
</Entity>
```

## <a name="malta"></a>Malta

### <a name="pattern"></a>Padrão

-  Dígitos 
    
### <a name="checksum"></a>Soma de verificação

Não aplicável
  
### <a name="definition"></a>Definição

Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:
  
- A expressão regular `Regex_malta_eu_mobile_number` encontra conteúdo que corresponde ao padrão. 
    
- A expressão regular `Regex_malta_eu_formatted_mobile_number` encontra conteúdo que corresponde ao padrão. 
    
- Uma palavra-chave da `Keywords_malta_eu_mobile_number` for encontrado. 
    
```
 
<Entity id="a56a0418-136a-41ea-a337-4d0388b28e69" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_malta_eu_mobile_number"/>
          <Match idRef="Keywords_malta_eu_mobile_number" />
        </Pattern>
<!-- Strictly formatted patterns without mandatory corroborative evidence -->
<Pattern confidenceLevel="75">
<IdMatch idRef="Regex_malta_eu_formatted_mobile_number" />
          </Pattern>
</Entity>
```

## <a name="netherlands"></a>Países Baixos

### <a name="pattern"></a>Padrão

-  Dígitos 
    
### <a name="checksum"></a>Soma de verificação

Não aplicável
  
### <a name="definition"></a>Definição

Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:
  
- A expressão regular `Regex_netherlands_eu_mobile_number` encontra conteúdo que corresponde ao padrão. 
    
- A expressão regular `Regex_netherlands_eu_formatted_mobile_number` encontra conteúdo que corresponde ao padrão. 
    
- Uma palavra-chave da `Keywords_netherlands_eu_mobile_number` for encontrado. 
    
```
<Entity id="a56a0418-136a-41ea-a337-4d0388b28e69" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_netherlands_eu_mobile_number"/>
          <Match idRef="Keywords_netherlands_eu_mobile_number" />
        </Pattern>
<!-- Strictly formatted patterns without mandatory corroborative evidence -->
<Pattern confidenceLevel="75">
<IdMatch idRef="Regex_netherlands_eu_formatted_mobile_number" />
          </Pattern>
</Entity>
```

## <a name="poland"></a>Polônia

### <a name="pattern"></a>Padrão

-  Dígitos 
    
### <a name="checksum"></a>Soma de verificação

Não aplicável
  
### <a name="definition"></a>Definição

Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:
  
- A expressão regular `Regex_poland_eu_mobile_number` encontra conteúdo que corresponde ao padrão. 
    
- A expressão regular `Regex_poland_eu_formatted_mobile_number` encontra conteúdo que corresponde ao padrão. 
    
- Uma palavra-chave da `Keywords_poland_eu_mobile_number` for encontrado. 
    
```
 
<Entity id="a56a0418-136a-41ea-a337-4d0388b28e69" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_poland_eu_mobile_number"/>
          <Match idRef="Keywords_poland_eu_mobile_number" />
        </Pattern>
<!-- Strictly formatted patterns without mandatory corroborative evidence -->
<Pattern confidenceLevel="75">
<IdMatch idRef="Regex_poland_eu_formatted_mobile_number" />
          </Pattern>
</Entity>
```

## <a name="portugal"></a>Portugal

### <a name="pattern"></a>Padrão

-  Dígitos 
    
### <a name="checksum"></a>Soma de verificação

Não aplicável
  
### <a name="definition"></a>Definição

Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:
  
- A expressão regular `Regex_portugal_eu_mobile_number` encontra conteúdo que corresponde ao padrão. 
    
- A expressão regular `Regex_portugal_eu_formatted_mobile_number` encontra conteúdo que corresponde ao padrão. 
    
- Uma palavra-chave da `Keywords_portugal_eu_mobile_number` for encontrado. 
    
```
 
<Entity id="a56a0418-136a-41ea-a337-4d0388b28e69" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_portugal_eu_mobile_number"/>
          <Match idRef="Keywords_portugal_eu_mobile_number" />
        </Pattern>
<Pattern confidenceLevel="75">
<IdMatch idRef="Regex_portugal_eu_formatted_mobile_number" />
          </Pattern>
</Entity>
```

## <a name="romania"></a>Romênia

### <a name="pattern"></a>Padrão

-  Dígitos 
    
### <a name="checksum"></a>Soma de verificação

Não aplicável
  
### <a name="definition"></a>Definição

Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:
  
- A expressão regular `Regex_romania_eu_mobile_number` encontra conteúdo que corresponde ao padrão. 
    
- A expressão regular `Regex_romania_eu_formatted_mobile_number` encontra conteúdo que corresponde ao padrão. 
    
- Uma palavra-chave da `Keywords_romania_eu_mobile_number` for encontrado. 
    
```
 
<Entity id="a56a0418-136a-41ea-a337-4d0388b28e69" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_romania_eu_mobile_number"/>
          <Match idRef="Keywords_romania_eu_mobile_number" />
        </Pattern>
<Pattern confidenceLevel="75">
<IdMatch idRef="Regex_romania_eu_formatted_mobile_number" />
          </Pattern>
</Entity>
```

## <a name="slovakia"></a>Eslováquia

### <a name="pattern"></a>Padrão

-  Dígitos 
    
### <a name="checksum"></a>Soma de verificação

Não aplicável
  
### <a name="definition"></a>Definição

Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:
  
- A expressão regular `Regex_slovakia_eu_mobile_number` encontra conteúdo que corresponde ao padrão. 
    
- A expressão regular `Regex_slovakia_eu_formatted_mobile_number` encontra conteúdo que corresponde ao padrão. 
    
- Uma palavra-chave da `Keywords_slovakia_eu_mobile_number` for encontrado. 
    
```
 
<Entity id="a56a0418-136a-41ea-a337-4d0388b28e69" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_slovakia_eu_mobile_number"/>
          <Match idRef="Keywords_slovakia_eu_mobile_number" />
        </Pattern>
<Pattern confidenceLevel="75">
<IdMatch idRef="Regex_slovakia_eu_formatted_mobile_number" />
          </Pattern>
</Entity>
```

## <a name="slovenia"></a>Eslovênia

### <a name="pattern"></a>Padrão

-  Dígitos 
    
### <a name="checksum"></a>Soma de verificação

Não aplicável
  
### <a name="definition"></a>Definição

Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:
  
- A expressão regular `Regex_slovenia_eu_mobile_number` encontra conteúdo que corresponde ao padrão. 
    
- A expressão regular `Regex_slovenia_eu_formatted_mobile_number` encontra conteúdo que corresponde ao padrão. 
    
- Uma palavra-chave da `Keywords_slovenia_eu_mobile_number` for encontrado. 
    
```
<Entity id="a56a0418-136a-41ea-a337-4d0388b28e69" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_slovenia_eu_mobile_number"/>
          <Match idRef="Keywords_slovenia_eu_mobile_number" />
        </Pattern>
<Pattern confidenceLevel="75">
<IdMatch idRef="Regex_slovenia_eu_formatted_mobile_number" />
          </Pattern>
</Entity>
```

## <a name="spain"></a>Espanha

### <a name="pattern"></a>Padrão

-  Dígitos 
    
### <a name="checksum"></a>Soma de verificação

Não aplicável
  
### <a name="definition"></a>Definição

Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:
  
- A expressão regular `Regex_spain_eu_mobile_number` encontra conteúdo que corresponde ao padrão. 
    
- A expressão regular `Regex_spain_eu_formatted_mobile_number` encontra conteúdo que corresponde ao padrão. 
    
- Uma palavra-chave da `Keywords_spain_eu_mobile_number` for encontrado. 
    
```
 
<Entity id="a56a0418-136a-41ea-a337-4d0388b28e69" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_spain_eu_mobile_number"/>
          <Match idRef="Keywords_spain_eu_mobile_number" />
        </Pattern>
<Pattern confidenceLevel="75">
<IdMatch idRef="Regex_spain_eu_formatted_mobile_number" />
          </Pattern>
</Entity>
```

## <a name="sweden"></a>Suécia

### <a name="pattern"></a>Padrão

-  Dígitos 
    
### <a name="checksum"></a>Soma de verificação

Não aplicável
  
### <a name="definition"></a>Definição

Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:
  
- A expressão regular `Regex_sweden_eu_mobile_number` encontra conteúdo que corresponde ao padrão. 
    
- A expressão regular `Regex_sweden_eu_formatted_mobile_number` encontra conteúdo que corresponde ao padrão. 
    
- Uma palavra-chave da `Keywords_sweden_eu_mobile_number` for encontrado. 
    
```
 
<Entity id="a56a0418-136a-41ea-a337-4d0388b28e69" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_sweden_eu_mobile_number"/>
          <Match idRef="Keywords_sweden_eu_mobile_number" />
        </Pattern>
<Pattern confidenceLevel="75">
<IdMatch idRef="Regex_sweden_eu_formatted_mobile_number" />
          </Pattern>
</Entity>
```

## <a name="uk"></a>REINO UNIDO

### <a name="pattern"></a>Padrão

-  Dígitos 
    
### <a name="checksum"></a>Soma de verificação

Não aplicável
  
### <a name="definition"></a>Definição

Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:
  
- A expressão regular `Regex_uk_eu_mobile_number` encontra conteúdo que corresponde ao padrão. 
    
- A expressão regular `Regex_uk_eu_formatted_mobile_number` encontra conteúdo que corresponde ao padrão. 
    
- Uma palavra-chave da `Keywords_uk_eu_mobile_number` for encontrado. 
    
```
 
<Entity id="a56a0418-136a-41ea-a337-4d0388b28e69" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_uk_eu_mobile_number"/>
          <Match idRef="Keywords_uk_eu_mobile_number" />
        </Pattern>
<Pattern confidenceLevel="75">
<IdMatch idRef="Regex_uk_eu_formatted_mobile_number" />
          </Pattern>
</Entity>
```

## <a name="see-also"></a>Confira também

[O que os tipos de informações confidenciais procuram](what-the-sensitive-information-types-look-for.md)

