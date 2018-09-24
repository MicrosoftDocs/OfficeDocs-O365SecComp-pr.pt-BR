---
title: O que os tipos de informações confidenciais procuram
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: 6/29/2018
ms.audience: Admin
ms.topic: reference
f1_keywords:
- ms.o365.cc.UnifiedDLPRuleContainsSensitiveInformation
ms.service: o365-administration
localization_priority: Normal
ms.collection: Strat_O365_IP
ms.assetid: fd505979-76be-4d9f-b459-abef3fc9e86b
description: Prevenção de perda de dados (DLP) no Office 365 Security &amp; Centro de conformidade inclui 80 tipos de informações confidenciais que estão prontos para uso em suas políticas de DLP. Este tópico lista todos esses tipos de informações confidenciais e mostra o que uma política de DLP procura por quando detecta cada tipo.
ms.openlocfilehash: 2e59b322730ca7fa828a685ed3a80c48ebdbbfd8
ms.sourcegitcommit: 17c7e18d7d00135b1af40cbea117c9a817a41117
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/24/2018
ms.locfileid: "24972353"
---
# <a name="what-the-sensitive-information-types-look-for"></a>O que os tipos de informações confidenciais procuram

Prevenção de perda de dados (DLP) no Office 365 Security &amp; Centro de conformidade inclui muitos tipos de informações confidenciais que estão prontos para uso em suas políticas de DLP. Este tópico lista todos esses tipos de informações confidenciais e mostra o que uma política de DLP procura por quando detecta cada tipo. Um tipo de informação confidencial é definido por um padrão que pode ser identificado por uma função ou uma expressão regular. Além disso, a evidência corroborativa como palavras-chave e somas de verificação pode ser usada para identificar um tipo de informações confidenciais. Proximidade e nível de confiança também são usados no processo de avaliação.
  
## <a name="aba-routing-number"></a>Número de roteamento ABA

### <a name="format"></a>Formato

9 dígitos que podem estar em um padrão formatado ou não formatado

### <a name="pattern"></a>Padrão

Formatado:
- Quatro dígitos, começando com 0, 1, 2, 3, 6, 7 ou 8
- Um hífen
- Quatro dígitos
- Um hífen
- Um dígito

Não formatada: 9 dígitos consecutivos começando com 0, 1, 2, 3, 6, 7 ou 8 

### <a name="checksum"></a>Soma de verificação

Não

### <a name="definition"></a>Definição

Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:
- A função Func_aba_routing localiza conteúdo que corresponde ao padrão.
- Uma palavra-chave de Keyword_ABA_Routing for encontrada.

```
<!-- ABA Routing Number -->
<Entity id="cb353f78-2b72-4c3c-8827-92ebe4f69fdf" patternsProximity="300" recommendedConfidence="75">
      <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_aba_routing" />
        <Match idRef="Keyword_ABA_Routing" />
      </Pattern>
 </Entity>
```


### <a name="keywords"></a>Palavras-chave

#### <a name="keywordabarouting"></a>Keyword_ABA_Routing

- aba
- 
aba #
- 
aba routing #
- 
aba routing number
- 
aba#
- 
abarouting#
- 
aba number
- 
abaroutingnumber
- 
american bank association routing #
- 
american bank association routing number
- 
americanbankassociationrouting#
- 
americanbankassociationroutingnumber
- 
bank routing number
- 
bankrouting#
- 
bankroutingnumber
- 
routing transit number
- 
RTN
 
   
## <a name="argentina-national-identity-dni-number"></a>Número de Identidade Nacional (DNI) da Argentina

### <a name="format"></a>Formato

Oito dígitos separados por pontos

### <a name="pattern"></a>Padrão

Oito dígitos:
- Dois dígitos
- Um ponto 
- Três dígitos
- Um ponto 
- Três dígitos

### <a name="checksum"></a>Soma de verificação

Não

### <a name="definition"></a>Definição

Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:
- A expressão regular Regex_argentina_national_id encontra o conteúdo que corresponde ao padrão.
- Uma palavra-chave de Keyword_argentina_national_id é encontrada.

```
<!-- Argentina National Identity (DNI) Number -->
<Entity id="eefbb00e-8282-433c-8620-8f1da3bffdb2" recommendedConfidence="75" patternsProximity="300">
   <Pattern confidenceLevel="75">
      <IdMatch idRef="Regex_argentina_national_id"/>
      <Match idRef="Keyword_argentina_national_id"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a>Palavras-chave

#### <a name="keywordargentinanationalid"></a>Keyword_argentina_national_id

- Número de Identidade Nacional da Argentina
 
- Identidade 
- Cartão de identificação nacional de identidade 
- DNI
 
- Registro NIC nacional de pessoas 
- Documento Nacional de Identidad
 
- Registro Nacional de las Personas
 
- Identidad
 
- Identificación
 
   
## <a name="australia-bank-account-number"></a>Número de conta de banco da Austrália

### <a name="format"></a>Formato

6 a 10 dígitos com ou sem um número BSB

### <a name="pattern"></a>Padrão

Número de conta é 6-10 dígitos. Número de filial do estado de banco da Austrália:
- Três dígitos 
- Um hífen 
- Três dígitos

### <a name="checksum"></a>Soma de verificação

Não

### <a name="definition"></a>Definição

Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:
- A expressão regular Regex_australia_bank_account_number localiza o conteúdo que corresponde ao padrão.
- Uma palavra-chave de Keyword_australia_bank_account_number for encontrada.
- A expressão regular Regex_australia_bank_account_number_bsb localiza o conteúdo que corresponde ao padrão.

Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:
- A expressão regular Regex_australia_bank_account_number localiza o conteúdo que corresponde ao padrão.
- Uma palavra-chave de Keyword_australia_bank_account_number for encontrada.

```
<!-- Australia Bank Account Number -->
<Entity id="74a54de9-2a30-4aa0-a8aa-3d9327fc07c7" patternsProximity="300" recommendedConfidence="75">
  <Pattern confidenceLevel="85">
        <IdMatch idRef="Regex_australia_bank_account_number" />
        <Match idRef="Keyword_australia_bank_account_number" />
        <Match idRef="Regex_australia_bank_account_number_bsb" />
  </Pattern>
  <Pattern confidenceLevel="75">
        <IdMatch idRef="Regex_australia_bank_account_number" />
        <Match idRef="Keyword_australia_bank_account_number" />
  </Pattern>
 </Entity>
```

### <a name="keywords"></a>Palavras-chave

#### <a name="keywordaustraliabankaccountnumber"></a>Keyword_australia_bank_account_number

- swift bank code
- 
correspondent bank
- 
base currency
- 
usa account
- 
holder address
- 
bank address
- 
information account
- 
fund transfers
- 
bank charges
- 
bank details
- 
banking information
- 
full names
- 

iaea

   
## <a name="australia-drivers-license-number"></a>Número de carteira de motorista da Austrália

### <a name="format"></a>Formato

Nove letras e dígitos

### <a name="pattern"></a>Padrão

Nove letras e dígitos: 

- Dois dígitos ou letras (não diferenciam maiúsculas de minúsculas) 
- Dois dígitos 
- Cinco dígitos ou letras (não diferenciam maiúsculas de minúsculas)

OU

- 1 a 2 letras opcionais (não diferenciam maiúsculas de minúsculas) 
- 4 a 9 dígitos

OU

- Nove dígitos ou letras (não diferenciam maiúsculas de minúsculas)

### <a name="checksum"></a>Soma de verificação

Não

### <a name="definition"></a>Definição

Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:
- A expressão regular Regex_australia_drivers_license_number localiza o conteúdo que corresponde ao padrão.
- Uma palavra-chave de Keyword_australia_drivers_license_number for encontrada.
- Nenhuma palavra-chave de Keyword_australia_drivers_license_number_exclusions for encontrada.

```
<!-- Australia Drivers License Number -->
<Entity id="1cbbc8f5-9216-4392-9eb5-5ac2298d1356" patternsProximity="300" recommendedConfidence="75">
   <Pattern confidenceLevel="75">
        <IdMatch idRef="Regex_australia_drivers_license_number" />
        <Match idRef="Keyword_australia_drivers_license_number" />
        <Any minMatches="0" maxMatches="0">
          <Match idRef="Keyword_australia_drivers_license_number_exclusions" />
        </Any>
  </Pattern>
</Entity>
```

### <a name="keywords"></a>Palavras-chave

#### <a name="keywordaustraliadriverslicensenumber"></a>Keyword_australia_drivers_license_number

- international driving permits
- 
australian automobile association
- 
sydney nsw
- 
international driving permit
- DriverLicence
- DriverLicences
- Driver Lic
- Driver Licence

- Driver Licences

- DriversLic
- DriversLicence
- DriversLicences
- Drivers Lic
- Drivers Lics
- Drivers de licença
- Licenças de drivers
- Driver'Lic
- Driver'Lics
- Driver'Licence
- Driver'Licences
- Driver' Lic
- Driver' Lics
- Driver' licença
- Driver' licenças
- Driver'sLic
- Driver'sLics
- Driver'sLicence
- Driver'sLicences
- Lic do driver
- Lics do driver
- Driver's Licence

- Driver's Licences

- DriverLic #
- DriverLics #
- DriverLicence #
- DriverLicences #
- Driver Lic#
- 
Driver Lics#

- Licença do driver #
- Driver licenças #
- DriversLic #
- DriversLics #
- DriversLicence #
- DriversLicences #
- Drivers Lic #
- Drivers Lics #
- Drivers licença #
- Drivers licenças #
- Driver'Lic#

- Driver'Lics#

- Driver'Licence#

- Driver'Licences#

- Driver' Lic#

- Driver' Lics#

- Driver' licença #
- Driver' licenças #
- Driver'sLic #
- Driver'sLics #
- Driver'sLicence #
- Driver'sLicences #
- Driver's Lic#

- Driver's Lics#

- Licença # de motorista
- Licenças # de motorista 

#### <a name="keywordaustraliadriverslicensenumberexclusions"></a>Keyword_australia_drivers_license_number_exclusions

- aaa
- DriverLicense
- DriverLicenses
- Driver de licença
- Licenças de driver
- CarteiraDeMotorista
- DriversLicenses
- Carteira de motorista
- Licenças de drivers
- Driver'License
- Driver'Licenses
- Driver' licença
- Driver' licenças
- Driver'sLicense
- Driver'sLicenses
- De motorista carteira
- Licenças de motorista
- DriverLicense #
- DriverLicenses #
- Licença do driver #
- Driver licenças #
- CarteiraDeMotorista #
- DriversLicenses #
- Drivers licença #
- Drivers licenças #
- Driver'License#

- Driver'Licenses#

- Driver' License#

- Driver' Licenses#

- Driver'sLicense #
- Driver'sLicenses #
- Driver's License#

- 

Driver's Licenses#
   
## <a name="australia-medical-account-number"></a>Número de conta médica da Austrália

### <a name="format"></a>Formato

10 a 11 dígitos

### <a name="pattern"></a>Padrão

10 a 11 dígitos:
- Primeiro dígito está no intervalo de 2 a 6
- O nono dígito é um dígito de verificação
- O décimo dígito é o dígito do problema
- O décimo primeiro dígito (opcional) é o número individual

### <a name="checksum"></a>Soma de verificação

Sim

### <a name="definition"></a>Definição

Uma política de DLP tem 95% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:
- A função Func_australian_medical_account_number localiza conteúdo que corresponde ao padrão.
- Uma palavra-chave de Keyword_Australia_Medical_Account_Number for encontrada.
- A soma de verificação passa.

Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:
- A função Func_australian_medical_account_number localiza conteúdo que corresponde ao padrão.
- A soma de verificação passa.

```
  <!-- Australia Medical Account Number -->
<Entity id="104a99a0-3d3b-4542-a40d-ab0b9e1efe63" recommendedConfidence="85" patternsProximity="300">
    <Pattern confidenceLevel="95">
     <IdMatch idRef="Func_australian_medical_account_number"/>
     <Any minMatches="1">
     <Match idRef="Keyword_Australia_Medical_Account_Number"/>
     </Any>
  </Pattern>
<Pattern confidenceLevel="85">
     <IdMatch idRef="Func_australian_medical_account_number"/>
     <Any minMatches="0" maxMatches="0">
  <Match idRef="Keyword_Australia_Medical_Account_Number"/>
     </Any>
  </Pattern>
</Entity>
```

### <a name="keywords"></a>Palavras-chave

#### <a name="keywordaustraliamedicalaccountnumber"></a>Keyword_Australia_Medical_Account_Number

- bank account details
- 
medicare payments
- 
mortgage account
- 
bank payments
- 
information branch
- 
credit card loan
- 
department of human services
- serviço local
- 

medicare

   
## <a name="australia-passport-number"></a>Número de passaporte da Austrália

### <a name="format"></a>Formato

Uma letra seguida por sete dígitos

### <a name="pattern"></a>Padrão

Uma letra (não diferencia maiúsculas de minúsculas) seguida de sete dígitos

### <a name="checksum"></a>Soma de verificação

Não

### <a name="definition"></a>Definição

Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:
- A expressão regular Regex_australia_passport_number localiza o conteúdo que corresponde ao padrão.
- Uma palavra-chave de Keyword_passport ou Keyword_australia_passport_number é encontrada.

```
<!-- Australia Passport Number -->
<Entity id="29869db6-602d-4853-ab93-3484f905df50" patternsProximity="300" recommendedConfidence="75">
  <Pattern confidenceLevel="75">
        <IdMatch idRef="Regex_australia_passport_number" />
        <Any minMatches="1">
          <Match idRef="Keyword_passport" />
          <Match idRef="Keyword_australia_passport_number" />
        </Any>
   </Pattern>
</Entity>   
```

### <a name="keywords"></a>Palavras-chave

#### <a name="keywordpassport"></a>Keyword_passport

- Passport Number
- 
Passport No
- Passport #

- Passport#

- PassportID
- Passportno

- passportnumber

- パスポート
- パスポート番号

- パスポートのNum

- 
パスポート ＃
 
- Numéro de passeport
- 
Passeport n °
- Passeport Non

- Passeport #

- Passeport#

- PasseportNon
- Passeportn °


#### <a name="keywordaustraliapassportnumber"></a>Keyword_australia_passport_number

- passport
- 
passport details
- 
immigration and citizenship
- 
commonwealth of australia
- 
department of immigration
- 
residential address
- 
department of immigration and citizenship
- visa

- 
national identity card
- número de passaporte
- 
travel document
- 

issuing authority
   
## <a name="australia-tax-file-number"></a>Número de imposto de renda da Austrália

### <a name="format"></a>Formato

8 a 9 dígitos

### <a name="pattern"></a>Padrão

8 a 9 dígitos normalmente apresentados com espaços, da seguinte maneira:
- Três dígitos 
- Um espaço opcional 
- Três dígitos 
- Um espaço opcional 
- 2 a 3 dígitos em que o último dígito é um dígito de verificação

### <a name="checksum"></a>Soma de verificação

Sim

### <a name="definition"></a>Definição

Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:
- A função Func_australian_tax_file_number localiza conteúdo que corresponde ao padrão.
- Nenhuma palavra-chave de Keyword_Australia_Tax_File_Number ou Keyword_number_exclusions for encontrada.
- A soma de verificação passa.

```
    <!-- Australia Tax File Number -->
<Entity id="e29bc95f-ff70-4a37-aa01-04d17360a4c5" patternsProximity="300" recommendedConfidence="85">
    
  <Pattern confidenceLevel="85">
        <IdMatch idRef="Func_australian_tax_file_number" />
        <Any minMatches="0" maxMatches="0">
          <Match idRef="Keyword_Australia_Tax_File_Number" />
          <Match idRef="Keyword_number_exclusions" />
        </Any>
  </Pattern>
</Entity>
```

### <a name="keywords"></a>Palavras-chave

#### <a name="keywordaustraliataxfilenumber"></a>Keyword_Australia_Tax_File_Number

- australian business number
- 
marginal tax rate
- 
medicare levy
- 
portfolio number
- 
service veterans
- 
withholding tax
- 
individual tax return
- 

tax file number

#### <a name="keywordnumberexclusions"></a>Keyword_number_exclusions

- 00000000
- 11111111
- 22222222
- 33333333
- 44444444
- 55555555
- 66666666
- 77777777
- 88888888
- 99999999
- 000000000
- 111111111
- 222222222
- 333333333
- 444444444
- 555555555
- 666666666
- 777777777
- 888888888
- 999999999
- 0000000000
- 1111111111
- 2222222222
- 3333333333
- 4444444444
- 5555555555
- 6666666666
- 7777777777
- 8888888888
- 9999999999
   
## <a name="belgium-national-number"></a>Número Nacional da Bélgica

### <a name="format"></a>Formato

11 dígitos mais delimitadores

### <a name="pattern"></a>Padrão

11 dígitos mais delimitadores.
- Seis dígitos e dois pontos no formato AA.MM.DD da data de nascimento  
- Um hífen 
- Três dígitos sequenciais (ímpares para homens, pares para mulheres)  
- Um ponto  
- Dois dígitos que são um dígito de verificação

### <a name="checksum"></a>Soma de verificação

Sim

### <a name="definition"></a>Definição

Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:
- A função Func_belgium_national_number encontra o conteúdo que corresponde ao padrão.
- Uma palavra-chave de Keyword_belgium_national_number é encontrada.
- A soma de verificação passa.

```
<!-- Belgium National Number -->
  <Entity id="fb969c9e-0fd1-4b18-8091-a2123c5e6a54" recommendedConfidence="75" patternsProximity="300">
   <Pattern confidenceLevel="75">
     <IdMatch idRef="Func_belgium_national_number"/>
     <Match idRef="Keyword_belgium_national_number"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a>Palavras-chave

#### <a name="keywordbelgiumnationalnumber"></a>Keyword_belgium_national_number

- Identity
- Registro
- Identificação  
- ID 
- Identiteitskaart
- Registratie nummer 
 
- Identificatie nummer
 
- Identiteit
- Registratie
- Identificatie

 
- Carte d’identité
 
- numéro d'immatriculation
- numéro d'identification
- 
identité
 
- inscription
 
- Identifikation
- Identifizierung
- Identifikationsnummer
- Personalausweis
- Registrierung
- Registrationsnummer

   
## <a name="brazil-cpf-number"></a>Número de CPF do Brasil

### <a name="format"></a>Formato

11 dígitos que incluem um dígito de verificação e podem ser formatados ou não formatados

### <a name="pattern"></a>Padrão

Formatado:
- Três dígitos 
- Um ponto  
- Três dígitos 
- Um ponto  
- Três dígitos 
- Um hífen 
- Dois dígitos que são dígitos de verificação

Não Formatado:
- 11 dígitos em que os dois últimos dígitos são dígitos de verificação

### <a name="checksum"></a>Soma de verificação

Sim

### <a name="definition"></a>Definição

Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:
- A função Func_brazil_cpf encontra o conteúdo que corresponde ao padrão.
- Uma palavra-chave de Keyword_brazil_cpf é encontrada.
- A soma de verificação passa.

Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:
- A função Func_brazil_cpf encontra o conteúdo que corresponde ao padrão.
- A soma de verificação passa.

```
<!-- Brazil CPF Number -->
<Entity id="78e09124-f2c3-4656-b32a-c1a132cd2711" recommendedConfidence="85" patternsProximity="300">
  <Pattern confidenceLevel="85">
     <IdMatch idRef="Func_brazil_cpf"/>
     <Match idRef="Keyword_brazil_cpf"/>
  </Pattern>
  <Pattern confidenceLevel="75">
     <IdMatch idRef="Func_brazil_cpf"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a>Palavras-chave

#### <a name="keywordbrazilcpf"></a>Keyword_brazil_cpf

- CPF
- Identificação 
- Registro
- Receita
- Cadastro de Pessoas Físicas
 
- Imposto
 
- Identificação
 
- Inscrição
 
- Receita

 
   
## <a name="brazil-legal-entity-number-cnpj"></a>Número de Pessoa Jurídica (CNPJ) do Brasil

### <a name="format"></a>Formato

14 dígitos que incluem um número de registro, o número da ramificação e dígitos de verificação, além de delimitadores de seleção

### <a name="pattern"></a>Padrão
14 dígitos mais delimitadores:
- Dois dígitos 
- Um ponto  
- Três dígitos 
- Um ponto  
- Três dígitos (esses primeiros oito dígitos são o número de registro)  
- Uma barra 
- Número da ramificação de quatro dígitos  
- Um hífen 
- Dois dígitos que são dígitos de verificação

### <a name="checksum"></a>Soma de verificação

Sim

### <a name="definition"></a>Definição

Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:
- A função Func_brazil_cnpj encontra o conteúdo que corresponde ao padrão.
- Uma palavra-chave de Keyword_brazil_cnpj é encontrada.
- A soma de verificação passa.

Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:
- A função Func_brazil_cnpj encontra o conteúdo que corresponde ao padrão.
- A soma de verificação passa.

```
<!-- Brazil Legal Entity Number (CNPJ) -->
<Entity id="9b58b5cd-5e90-4df6-b34f-1ebcc88ceae4" recommendedConfidence="85" patternsProximity="300">
   <Pattern confidenceLevel="85">
     <IdMatch idRef="Func_brazil_cnpj"/>
     <Match idRef="Keyword_brazil_cnpj"/>
  </Pattern>
  <Pattern confidenceLevel="75">
     <IdMatch idRef="Func_brazil_cnpj"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a>Palavras-chave

#### <a name="keywordbrazilcnpj"></a>Keyword_brazil_cnpj

- CNPJ
 
- CNPJ/MF 
- CNPJ-MF
 
- Registro Nacional de Pessoas Jurídicas
 
- Registro de Contribuintes
 
- Pessoa jurídica
 
- Pessoas jurídicas
 
- Status do Registro
 
- Comercial
 
- Empresa
- CNPJ
 
- Cadastro Nacional da Pessoa Jurídica
 
- Cadastro Geral de Contribuintes
 
- CGC
 
- Pessoa jurídica
 
- Pessoas jurídicas
 
- Situação cadastral
 
- Inscrição
 
- Empresa
 
   
## <a name="brazil-national-id-card-rg"></a>	Cartão de Identidade Nacional (RG) do Brasil

### <a name="format"></a>Formato

Registro Geral (formato antigo): nove dígitos

Registro de Identidade (RIC) (novo formato): 11 dígitos

### <a name="pattern"></a>Padrão

Registro Geral (formato antigo):
- Dois dígitos 
- Um ponto  
- Três dígitos 
- Um ponto  
- Três dígitos 
- Um hífen 
- Um dígito que é um dígito de verificação

Registro de Identidade (RIC) (formato novo):
- 10 dígitos  
- Um hífen 
- Um dígito que é um dígito de verificação

### <a name="checksum"></a>Soma de verificação

Sim

### <a name="definition"></a>Definição

Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:
- A função Func_brazil_rg encontra o conteúdo que corresponde ao padrão.
- Uma palavra-chave de Keyword_brazil_rg é encontrada.
- A soma de verificação passa.

Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:
- A função Func_brazil_rg encontra o conteúdo que corresponde ao padrão.
- A soma de verificação passa.

```
<!-- Brazil National ID Card (RG) -->
<Entity id="486de900-db70-41b3-a886-abdf25af119c" recommendedConfidence="85" patternsProximity="300">
  <Pattern confidenceLevel="85">
     <IdMatch idRef="Func_brazil_rg"/>
     <Match idRef="Keyword_brazil_rg"/>
  </Pattern>
  <Pattern confidenceLevel="75">
     <IdMatch idRef="Func_brazil_rg"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a>Palavras-chave

#### <a name="keywordbrazilrg"></a>Keyword_brazil_rg

Cédula de identidade cartão de identificação id nacional número de rregistro registro de Iidentidade registro geral RG (essa palavra-chave diferencia maiusculas de minúsculas) RIC (essa palavra-chave diferencia maiusculas de minúsculas) 
   
## <a name="canada-bank-account-number"></a>Número de conta bancária do Canadá

### <a name="format"></a>Formato

Sete ou doze dígitos

### <a name="pattern"></a>Padrão

Um número de conta bancária do Canadá tem sete ou doze dígitos.

Um número de trânsito de conta bancária do Canadá tem:
- Cinco dígitos 
- Um hífen 
- Três dígitos ou
- Um zero "0" 
- Oito dígitos

### <a name="checksum"></a>Soma de verificação

Não

### <a name="definition"></a>Definição

Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:
- A expressão regular Regex_canada_bank_account_number localiza o conteúdo que corresponde ao padrão.
- Uma palavra-chave de Keyword_canada_bank_account_number for encontrada.
- A expressão regular Regex_canada_bank_account_transit_number localiza o conteúdo que corresponde ao padrão.

Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:
- A expressão regular Regex_canada_bank_account_number localiza o conteúdo que corresponde ao padrão.
- Uma palavra-chave de Keyword_canada_bank_account_number for encontrada.

```
<!-- Canada Bank Account Number -->
<Entity id="552e814c-cb50-4d94-bbaa-bb1d1ffb34de" patternsProximity="300" recommendedConfidence="75">
  <Pattern confidenceLevel="85">
        <IdMatch idRef="Regex_canada_bank_account_number" />
        <Match idRef="Keyword_canada_bank_account_number" />
        <Match idRef="Regex_canada_bank_account_transit_number" />
   </Pattern>
   <Pattern confidenceLevel="75">
        <IdMatch idRef="Regex_canada_bank_account_number" />
        <Match idRef="Keyword_canada_bank_account_number" />
   </Pattern>
</Entity>
```

### <a name="keywords"></a>Palavras-chave

#### <a name="keywordcanadabankaccountnumber"></a>Keyword_canada_bank_account_number

- canada savings bonds
- 
canada revenue agency
- 
canadian financial institution
- 
direct deposit form
- 
canadian citizen
- 
legal representative
- 
notary public
- 
commissioner for oaths
- 
child care benefit
- 
universal child care
- 
canada child tax benefit
- 
income tax benefit
- 
harmonized sales tax
- social insurance number
- 
income tax refund
- 
child tax benefit
- 
territorial payments
- 
institution number
- 
deposit request
- 
banking information
- 

direct deposit
   
## <a name="canada-drivers-license-number"></a>Número de carteira de motorista do Canadá

### <a name="format"></a>Formato

Varia por província

### <a name="pattern"></a>Padrão

Vários padrões que abrangem Alberta, Columbia Britânica, Manitoba, New Brunswick, Newfoundland/Labrador, Nova Escócia, Ontário, Ilha do Príncipe Eduardo, Quebec e Saskatchewan

### <a name="checksum"></a>Soma de verificação

Não

### <a name="definition"></a>Definição

Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:
- A função Func_[province_name]_drivers_license_number localiza conteúdo que corresponde ao padrão.
- Uma palavra-chave de Keyword_[province_name]_drivers_license_name for encontrada.
- Uma palavra-chave de Keyword_canada_drivers_license for encontrada.

```
<!-- Canada Driver's License Number -->
    <Entity id="37186abb-8e48-4800-ad3c-e3d1610b3db0" patternsProximity="300" recommendedConfidence="75">
      <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_alberta_drivers_license_number" />
        <Match idRef="Keyword_alberta_drivers_license_name" />
        <Match idRef="Keyword_canada_drivers_license" />
      </Pattern>
      <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_british_columbia_drivers_license_number" />
        <Match idRef="Keyword_british_columbia_drivers_license_name" />
        <Match idRef="Keyword_canada_drivers_license" />
      </Pattern>
      <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_manitoba_drivers_license_number" />
        <Match idRef="Keyword_manitoba_drivers_license_name" />
        <Match idRef="Keyword_canada_drivers_license" />
      </Pattern>
      <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_new_brunswick_drivers_license_number" />
        <Match idRef="Keyword_new_brunswick_drivers_license_name" />
        <Match idRef="Keyword_canada_drivers_license" />
      </Pattern>
      <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_newfoundland_labrador_drivers_license_number" />
        <Match idRef="Keyword_newfoundland_labrador_drivers_license_name" />
        <Match idRef="Keyword_canada_drivers_license" />
      </Pattern>
      <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_nova_scotia_drivers_license_number" />
        <Match idRef="Keyword_nova_scotia_drivers_license_name" />
        <Match idRef="Keyword_canada_drivers_license" />
      </Pattern>
      <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_ontario_drivers_license_number" />
        <Match idRef="Keyword_ontario_drivers_license_name" />
        <Match idRef="Keyword_canada_drivers_license" />
      </Pattern>
      <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_prince_edward_island_drivers_license_number" />
        <Match idRef="Keyword_prince_edward_island_drivers_license_name" />
        <Match idRef="Keyword_canada_drivers_license" />
      </Pattern>
      <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_quebec_drivers_license_number" />
        <Match idRef="Keyword_quebec_drivers_license_name" />
        <Match idRef="Keyword_canada_drivers_license" />
      </Pattern>
      <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_saskatchewan_drivers_license_number" />
        <Match idRef="Keyword_saskatchewan_drivers_license_name" />
        <Match idRef="Keyword_canada_drivers_license" />
      </Pattern>
    </Entity>
```

### <a name="keywords"></a>Palavras-chave

#### <a name="keywordprovincenamedriverslicensename"></a>Keyword_[province_name]_drivers_license_name

- A abreviação da província, por exemplo AB
- 
O nome da província, por exemplo, Alberta

#### <a name="keywordcanadadriverslicense"></a>Keyword_canada_drivers_license

- DL
- DLS
- CDL
- CDLS
- DriverLic
- DriverLics
- DriverLicense
- DriverLicenses
- DriverLicence
- DriverLicences
- Driver Lic
- Driver Lics
- Driver de licença
- Licenças de driver
- Driver Licence

- Driver Licences

- DriversLic
- DriversLics
- DriversLicence
- DriversLicences
- CarteiraDeMotorista
- DriversLicenses
- Drivers Lic
- Drivers Lics
- Carteira de motorista
- Licenças de drivers
- Drivers de licença
- Licenças de drivers
- Driver'Lic
- Driver'Lics
- Driver'License
- Driver'Licenses
- Driver'Licence
- Driver'Licences
- Driver' Lic
- Driver' Lics
- Driver' licença
- Driver' licenças
- Driver' licença
- Driver' licenças
- Driver'sLic
- Driver'sLics
- Driver'sLicense
- Driver'sLicenses
- Driver'sLicence
- Driver'sLicences
- Lic do driver
- Lics do driver
- De motorista carteira
- Licenças de motorista
- Driver's Licence

- Driver's Licences

- Permis de Conduire
- id
- IDs
- 
idcard number
- 
idcard numbers
- 
idcard #
- 
idcard #s
- cartão de idcard
- cartões de idcard
- idcard
- identification number

- identification numbers

- identification #

- 
identification #s
- cartão de identificação
- cartões de identificação
- 
identification
 
- DL#
- 
DLS#
 
- CDL#
 
- CDLS#
 
- DriverLic # 
- DriverLics # 
- DriverLicense # 
- DriverLicenses # 
- DriverLicence # 
- DriverLicences # 
- Driver Lic#
- 
Driver Lics#
 
- Licença do driver # 
- Driver licenças # 
- Licença do driver # 
- Driver licenças # 
- DriversLic # 
- DriversLics # 
- CarteiraDeMotorista # 
- DriversLicenses # 
- DriversLicence # 
- DriversLicences # 
- Drivers Lic # 
- Drivers Lics # 
- Drivers licença # 
- Drivers licenças # 
- Drivers licença # 
- Drivers licenças # 
- Driver'Lic#
 
- Driver'Lics#
 
- Driver'License#
 
- Driver'Licenses#
 
- Driver'Licence#
 
- Driver'Licences#
 
- Driver' Lic#
 
- Driver' Lics#
 
- Driver' License#
 
- Driver' Licenses#
 
- Driver' licença # 
- Driver' licenças # 
- Driver'sLic # 
- Driver'sLics # 
- Driver'sLicense # 
- Driver'sLicenses # 
- Driver'sLicence # 
- Driver'sLicences # 
- Driver's Lic#
 
- Driver's Lics#
 
- Driver's License#
 
- Driver's Licenses#
 
- Licença # de motorista 
- Licenças # de motorista 
- Permis de Conduire # 
- ID # 
- IDs # 
- idcard card#
 
- idcard cards#
 
- idcard #
 
- identification card#
 
- identification cards#
 
- identification #
 
   
## <a name="canada-health-service-number"></a>Número de serviço de saúde do Canadá

### <a name="format"></a>Formato

10 dígitos

### <a name="pattern"></a>Padrão

10 dígitos

### <a name="checksum"></a>Soma de verificação

Não

### <a name="definition"></a>Definição

Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:
- A expressão regular Regex_canada_health_service_number localiza o conteúdo que corresponde ao padrão.
- Uma palavra-chave de Keyword_canada_health_service_number for encontrada.

```
<!-- Canada Health Service Number -->
<Entity id="59c0bf39-7fab-482c-af25-00faa4384c94" patternsProximity="300" recommendedConfidence="75">
  <Pattern confidenceLevel="75">
        <IdMatch idRef="Regex_canada_health_service_number" />
        <Any minMatches="1">
          <Match idRef="Keyword_canada_health_service_number" />
        </Any>
  </Pattern>
</Entity>
```

### <a name="keywords"></a>Palavras-chave

#### <a name="keywordcanadahealthservicenumber"></a>Keyword_canada_health_service_number

- personal health number
- 
patient information
- Serviços de integridade
- 
speciality services
- 
automobile accident
- 
patient hospital
- 
psychiatrist
- 
workers compensation
- 
disability
      
## <a name="canada-passport-number"></a>Número de passaporte do Canadá

### <a name="format"></a>Formato

Duas letras maiúsculas, seguidas de seis dígitos

### <a name="pattern"></a>Padrão

Duas letras maiúsculas, seguidas de seis dígitos

### <a name="checksum"></a>Soma de verificação

Não

### <a name="definition"></a>Definição

Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:
- A expressão regular Regex_canada_passport_number localiza o conteúdo que corresponde ao padrão.
- Uma palavra-chave de Keyword_canada_passport_number ou Keyword_passport é encontrada.

``` 
<!-- Canada Passport Number -->
<Entity id="14d0db8b-498a-43ed-9fca-f6097ae687eb" patternsProximity="300" recommendedConfidence="75">
  <Pattern confidenceLevel="75">
        <IdMatch idRef="Regex_canada_passport_number" />
        <Any minMatches="1">
          <Match idRef="Keyword_canada_passport_number" />
          <Match idRef="Keyword_passport" />
        </Any>
  </Pattern>
</Entity>
```

### <a name="keywords"></a>Palavras-chave

#### <a name="keywordcanadapassportnumber"></a>Keyword_canada_passport_number

- canadian citizenship
- 
canadian passport
- 
passport application
- 
passport photos
- 
certified translator
- 
canadian citizens
- 
processing times
- 

renewal application

#### <a name="keywordpassport"></a>Keyword_passport

- Passport Number
- 
Passport No
- Passport #

- Passport#

- PassportID
- Passportno

- passportnumber

- パスポート
- パスポート番号

- パスポートのNum

- パスポート＃

- Numéro de passeport
- 
Passeport n °
- Passeport Non

- Passeport #

- Passeport#

- PasseportNon
- 

Passeportn °
   
## <a name="canada-personal-health-identification-number-phin"></a>Número de identificação pessoal de saúde do Canadá (PHIN)

### <a name="format"></a>Formato

Nove dígitos

### <a name="pattern"></a>Padrão

Nove dígitos

### <a name="checksum"></a>Soma de verificação

Não

### <a name="definition"></a>Definição

Uma política de DLP é 75% confiante de que detectou esse tipo de informações confidenciais if, dentro de uma proximidade de 300 caracteres: A expressão regular Regex_canada_phin encontra o conteúdo que corresponde ao padrão. Pelo menos duas palavras-chave da Keyword_canada_phin ou Keyword_canada_provinces são encontradas..

```
<!-- Canada PHIN -->
<Entity id="722e12ac-c89a-4ec8-a1b7-fea3469f89db" patternsProximity="300" recommendedConfidence="75">
  <Pattern confidenceLevel="75">
        <IdMatch idRef="Regex_canada_phin" />
        <Any minMatches="2">
          <Match idRef="Keyword_canada_phin" />
          <Match idRef="Keyword_canada_provinces" />
        </Any>
  </Pattern>
</Entity>
```

### <a name="keywords"></a>Palavras-chave

#### <a name="keywordcanadaphin"></a>Keyword_canada_phin

- social insurance number
- 
health information act
- 
income tax information
- 
manitoba health
- 
health registration
- 
prescription purchases
- 
benefit eligibility
- 
personal health
- 
power of attorney
- 
registration number
- personal health number
- 
practitioner referral
- 
wellness professional
- 
patient referral
- 

health and wellness

#### <a name="keywordcanadaprovinces"></a>Keyword_canada_provinces

- Nunavut
- 
Quebec
- 
Northwest Territories
- 
Ontario
- 
British Columbia
- 
Alberta
- 
Saskatchewan
- 
Manitoba
- 
Yukon
- 
Newfoundland and Labrador
- 
New Brunswick
- 
Nova Scotia
- 
Prince Edward Island
- Canadá
   
## <a name="canada-social-insurance-number"></a>Número de seguro social do Canadá

### <a name="format"></a>Formato

Nove dígitos com espaços ou hífens opcionais

### <a name="pattern"></a>Padrão

Formatado:
- Três dígitos 
- Um hífen ou espaço 
- Três dígitos 
- Um hífen ou espaço 
- Três dígitos

Formatada: Dígitos de nove

### <a name="checksum"></a>Soma de verificação

Sim

### <a name="definition"></a>Definição

Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:
- A função Func_canadian_sin localiza conteúdo que corresponde ao padrão.
- Pelo menos duas de qualquer combinação do seguinte:
    - Uma palavra-chave de Keyword_sin for encontrada.
    - Uma palavra-chave de Keyword_sin_collaborative for encontrada.
    - A função Func_eu_date encontra uma data no formato de data à direita.
- A soma de verificação passa.

Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:
- A função Func_unformatted_canadian_sin localiza conteúdo que corresponde ao padrão.
- Uma palavra-chave de Keyword_sin for encontrada.
- A soma de verificação passa.

```
<!-- Canada Social Insurance Number -->
<Entity id="a2f29c85-ecb8-4514-a610-364790c0773e" patternsProximity="300" recommendedConfidence="75">
  <Pattern confidenceLevel="85">
        <IdMatch idRef="Func_canadian_sin" />
        <Any minMatches="2">
          <Match idRef="Keyword_sin" />
          <Match idRef="Keyword_sin_collaborative" />
          <Match idRef="Func_eu_date" />
        </Any>
  </Pattern>
  <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_unformatted_canadian_sin" />
        <Match idRef="Keyword_sin" />
  </Pattern>
</Entity>
```

### <a name="keywords"></a>Palavras-chave

#### <a name="keywordsin"></a>Keyword_sin

- sin 
- social insurance
 
- numero d'assurance sociale
 
- sins
 
- SSN 
- números de identificação fiscal 
- seguridade social 
- numero d'assurance social
 
- número de identificação nacional 
- 
national id 
- sin#
 
- soc ins
 
- social ins
 

#### <a name="keywordsincollaborative"></a>Keyword_sin_collaborative

- de motorista carteira 
- carteira de motorista 
- licença de motorista 
- drivers licence 
- DOB
 
- Data de Nascimento 
- Aniversário  
- Date of Birth
 
   
## <a name="chile-identity-card-number"></a>	Número do Cartão de Identidade do Chile

### <a name="format"></a>Formato

os dígitos plus delimitadores 7 e 8 um dígito de verificação ou uma letra

### <a name="pattern"></a>Padrão

7 a 8 dígitos mais delimitadores:
- 1 a 2 dígitos 
- Um ponto  
- Três dígitos 
- Um ponto  
- Três dígitos 
- Um traço 
- Um dígito ou letra (não diferencia maiúscula de minúscula) que é um dígito de verificação

### <a name="checksum"></a>Soma de verificação

Sim

### <a name="definition"></a>Definição

Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:
- A função Func_chile_id_card encontra o conteúdo que corresponde ao padrão.
- Uma palavra-chave de Keyword_chile_id_card é encontrada.
- A soma de verificação passa.

Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:
- A função Func_chile_id_card encontra o conteúdo que corresponde ao padrão.
- A soma de verificação passa.

```
<!-- Chile Identity Card Number -->
<Entity id="4e979794-49a0-407e-a0b9-2c536937b925" recommendedConfidence="85" patternsProximity="300">
  <Pattern confidenceLevel="85">
     <IdMatch idRef="Func_chile_id_card"/>
     <Match idRef="Keyword_chile_id_card"/>
  </Pattern>
  <Pattern confidenceLevel="75">
     <IdMatch idRef="Func_chile_id_card"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a>Palavras-chave

#### <a name="keywordchileidcard"></a>Keyword_chile_id_card

- Número de Identificação Nacional
 
- Cartão de identidade 
- ID 
- Identificação  
- Rol Único Nacional
 
- EXECUTAR 
- Rol Único Tributario
 
- RUT
 
- Cédula de Identidad
 
- Número De Identificación Nacional
 
- Tarjeta de identificación
 
- Identificación
 
   
## <a name="china-resident-identity-card-prc-number"></a>	Número do Cartão de Identidade de Residentes (PRC) da China

### <a name="format"></a>Formato

18 dígitos

### <a name="pattern"></a>Padrão

18 dígitos:
- Seis dígitos que são um código de endereço  
- Oito dígitos no formato AAAAMMDD que são a data de nascimento  
- Três dígitos que são um código de pedido  
- Um dígito que é um dígito de verificação

### <a name="checksum"></a>Soma de verificação

Sim

### <a name="definition"></a>Definição

Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:
- A função Func_china_resident_id encontra o conteúdo que corresponde ao padrão.
- Uma palavra-chave de Keyword_china_resident_id é encontrada.
- A soma de verificação passa.

Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:
- A função Func_china_resident_id encontra o conteúdo que corresponde ao padrão.
- A soma de verificação passa.

```
<!-- China Resident Identity Card (PRC) Number -->
<Entity id="c92daa86-2d16-4871-901f-816b3f554fc1" recommendedConfidence="85" patternsProximity="300">
  <Pattern confidenceLevel="85">
     <IdMatch idRef="Func_china_resident_id"/>
     <Match idRef="Keyword_china_resident_id"/>
  </Pattern>
  <Pattern confidenceLevel="75">
     <IdMatch idRef="Func_china_resident_id"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a>Palavras-chave

### <a name="keywordchinaresidentid"></a>Keyword_china_resident_id

- Cartão de Identidade da Polônia
 
- PRC
 
- Cartão de Identificação Nacional
 
- 身份证  
- 居民 身份证  
- 居民身份证
 
- 鉴定

 
- 身分證  
- 居民 身份證
- 鑑定  
   
## <a name="credit-card-number"></a>Credit Card Number

### <a name="format"></a>Formato

16 dígitos que podem ser formatados ou não formatado (dddddddddddddddd) e deve passar o teste de Luhn.

### <a name="pattern"></a>Padrão

Padrão muito complexo e robusto que detecta cartões de todas as principais marcas em todo o mundo, incluindo Visa, MasterCard, Discover Card, JCB, American Express, vales-presentes e cartões diner.

### <a name="checksum"></a>Soma de verificação

Sim, a soma de verificação Luhn

### <a name="definition"></a>Definição

Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:
- A função Func_credit_card localiza conteúdo que corresponde ao padrão.
- Uma das seguintes opções for verdadeira:
    - Uma palavra-chave de Keyword_cc_verification for encontrada.
    - Uma palavra-chave de Keyword_cc_name for encontrada.
    - A função Func_expiration_date encontra uma data no formato de data à direita.
- A soma de verificação passa.

Uma política de DLP tem 65% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:
- A função Func_credit_card localiza conteúdo que corresponde ao padrão.
- A soma de verificação passa.

```
<!-- Credit Card Number -->
<Entity id="50842eb7-edc8-4019-85dd-5a5c1f2bb085" patternsProximity="300" recommendedConfidence="85">
  <Pattern confidenceLevel="85">
        <IdMatch idRef="Func_credit_card" />
        <Any minMatches="1">
          <Match idRef="Keyword_cc_verification" />
          <Match idRef="Keyword_cc_name" />
          <Match idRef="Func_expiration_date" />
        </Any>
  </Pattern>
  <Pattern confidenceLevel="65">
        <IdMatch idRef="Func_credit_card" />
  </Pattern>
</Entity>
```

### <a name="keywords"></a>Palavras-chave

#### <a name="keywordccverification"></a>Keyword_cc_verification

- card verification
- card identification number
- cvn

- cid

- CVC2
- cvv2
- pin block

- security code

- security number

- security no

- issue number

- issue no

- cryptogramme

- numéro de sécurité

- numero de securite

- kreditkartenprüfnummer

- kreditkartenprufnummer

- prüfziffer

- prufziffer

- sicherheits Kode
- sicherheitscode

- sicherheitsnummer

- verfalldatum

- codice di verifica

- cod. sicurezza

- COD sicurezza
- 
n autorizzazione
- código

- codigo

- cod. seg

- COD seg
- código de segurança

- codigo de seguranca

- codigo de segurança

- código de seguranca

- cód. segurança

- Cod. segurança cod. segurança
- cód. seguranca

- segurança Cód
- bacalhau segurança cod segurança
- segurança Cód
- número de verificação

- numero de verificacao

- ablauf

- gültig bis

- gültigkeitsdatum

- gultig bis

- gultigkeitsdatum

- scadenza

- data scad

- fecha de expiracion

- fecha de venc

- vencimiento

- válido hasta

- valido hasta

- vto

- data de expiração

- data de expiracao

- data em que expira

- validade

- valor

- vencimento

- Venc 

#### <a name="keywordccname"></a>Keyword_cc_name

- amex
- 
american express
- americanexpress

- Visa
- mastercard

- master card

- 
mc
 
- mastercards
- 
master cards
- Clube do cliente
- diners club

- dinersclub

- discover card

- discovercard

- discover cards

- JCB
- japanese card bureau

- carte blanche

- carteblanche

- credit card

- Cc #
- n º cc:
- 
expiration date
- exp date

- 
expiry date
- 
date d’expiration
- 
date d'exp
- 
date expiration
- bank card

- 
bankcard
- card number

- card num

- cardnumber

- cardnumbers

- card numbers

- creditcard

- credit cards

- creditcards

- ccn

- card holder

- cardholder

- card holders

- cardholders

- check card

- checkcard

- check cards

- checkcards

- debit card

- debitcard

- debit cards

- debitcards

- atm card

- atmcard

- atm cards

- atmcards

- 
enroute
- 
en route
- card type

- carte bancaire

- carte de crédit

- carte de credit

- numéro de carte

- numero de carte

- nº de la carte

- nº de carte

- kreditkarte

- karte

- karteninhaber

- karteninhabers
- kreditkarteninhaber

- kreditkarteninstitut

- kreditkartentyp

- eigentümername

- 
kartennr
 
- kartennummer
- 
kreditkartennummer
- kreditkarten-nummer
- carta di credito

- carta credito

- carta
- carta n
- nr. carta

- carta nr
- numero carta

- numero della carta

- numero di carta

- tarjeta credito

- tarjeta de credito

- 
tarjeta crédito
- 
tarjeta de crédito
- tarjeta de atm

- tarjeta atm

- tarjeta debito

- tarjeta de debito

- 
tarjeta débito
- 
tarjeta de débito
- nº de tarjeta

- no. de tarjeta

- Nenhum tarjeta de
- numero de tarjeta

- número de tarjeta

- tarjeta no

- tarjetahabiente

- cartão de crédito

- cartão de credito

- cartao de crédito

- cartao de credito

- cartão de débito

- cartao de débito

- cartão de debito

- cartao de debito

- débito automático
- debito automatico

- 
número do cartão
- 
numero do cartão
 
- número do cartao
- 
numero do cartao
- número de cartão

- numero de cartão

- número de cartao

- numero de cartao

- n º cartão
- nº do cartao

- nº. do cartão

- Nenhum cartão execute
- Nenhum cartao execute
- no. do cartão

- 
no. do cartao
 
   
## <a name="croatia-identity-card-number"></a>	Número do Cartão de Identidade da Croácia

### <a name="format"></a>Formato

Nove dígitos

### <a name="pattern"></a>Padrão

Nove dígitos consecutivos

### <a name="checksum"></a>Soma de verificação

Não

### <a name="definition"></a>Definição

Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:
- A função Func_croatia_id_card encontra o conteúdo que corresponde ao padrão.
- Uma palavra-chave de Keyword_croatia_id_card é encontrada.

```
<!--Croatia Identity Card Number-->
<Entity id="ff12f884-c20a-4189-b185-34c8e7258d47" recommendedConfidence="75" patternsProximity="300">
  <Pattern confidenceLevel="75">
     <IdMatch idRef="Func_croatia_id_card"/>
     <Match idRef="Keyword_croatia_id_card"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a>Palavras-chave

#### <a name="keywordcroatiaidcard"></a>Keyword_croatia_id_card

- Cartão de identidade croata
- Osobna iskaznica

   
## <a name="croatia-personal-identification-oib-number"></a>	Número de Identificação Pessoal (OIB) da Croácia

### <a name="format"></a>Formato

10 dígitos

### <a name="pattern"></a>Padrão

10 dígitos:
- Seis dígitos no formato DDMMAA que são a data de nascimento 
- Quatro dígitos em que o último é um dígito de verificação

### <a name="checksum"></a>Soma de verificação

Sim

### <a name="definition"></a>Definição

Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:
- A função Func_croatia_oib_number encontra o conteúdo que corresponde ao padrão.
- Uma palavra-chave de Keyword_croatia_oib_number é encontrada.
- A soma de verificação passa.

Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:
- A função Func_croatia_oib_number encontra o conteúdo que corresponde ao padrão.
- A soma de verificação passa.

```
<!-- Croatia Personal Identification (OIB) Number -->
<Entity id="31983b6d-db95-4eb2-a630-b44bd091968d" recommendedConfidence="85" patternsProximity="300">
  <Pattern confidenceLevel="85">
     <IdMatch idRef="Func_croatia_oib_number"/>
     <Match idRef="Keyword_croatia_oib_number"/>
  </Pattern>
  <Pattern confidenceLevel="75">
     <IdMatch idRef="Func_croatia_oib_number"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a>Palavras-chave

#### <a name="keywordcroatiaoibnumber"></a>Keyword_croatia_oib_number

- Número de Identificação Pessoal
- Osobni identifikacijski broj
 
- OIB
 

   
## <a name="czech-national-identity-card-number"></a>	Número do Cartão de Identidade Nacional Tcheco

### <a name="format"></a>Formato

10 dígitos que contém uma barra

### <a name="pattern"></a>Padrão

10 dígitos:
- Seis dígitos que são a data de nascimento 
- Uma barra 
- Quatro dígitos em que o último é um dígito de verificação

### <a name="checksum"></a>Soma de verificação

Sim

### <a name="definition"></a>Definição

Uma política DLP é de 85% confiante de que detectou esse tipo de informações confidenciais if, dentro de uma proximidade de 300 caracteres: A função Func_czech_id_card encontra o conteúdo que corresponde ao padrão. Uma palavra-chave de Keyword_czech_id_card é encontrada. A soma de verificação passa.

```
<!-- Czech National Identity Card Number -->
<Entity id="60c0725a-4eb6-455b-9dda-05d8a7396497" recommendedConfidence="85" patternsProximity="300">
  <Pattern confidenceLevel="85">
     <IdMatch idRef="Func_czech_id_card"/>
     <Match idRef="Keyword_czech_id_card"/>
  </Pattern>
</Entity>
```


### <a name="keywords"></a>Palavras-chave

- Keyword_czech_id_card
- Número do cartão de identidade nacional tcheco
- Občanský průka
   
## <a name="denmark-personal-identification-number"></a>	Número de Identificação Pessoal da Dinamarca

### <a name="format"></a>Formato

10 dígitos que contêm um hífen

### <a name="pattern"></a>Padrão

10 dígitos:
- Seis dígitos no formato DDMMAA que são a data de nascimento 
- Um hífen 
- Quatro dígitos em que o último é um dígito de verificação

### <a name="checksum"></a>Soma de verificação

Sim

### <a name="definition"></a>Definição

Uma política de DLP é 75% confiante de que detectou esse tipo de informações confidenciais if, dentro de uma proximidade de 300 caracteres: A expressão regular Regex_denmark_id encontra o conteúdo que corresponde ao padrão. Uma palavra-chave de Keyword_denmark_id é encontrada. A soma de verificação passa.

```
<!-- Denmark Personal Identification Number -->
<Entity id="6c4f2fef-56e1-4c00-8093-88d7a01cf460" recommendedConfidence="75" patternsProximity="300">
  <Pattern confidenceLevel="75">
     <IdMatch idRef="Regex_denmark_id"/>
     <Match idRef="Keyword_denmark_id"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a>Palavras-chave

#### <a name="keyworddenmarkid"></a>Keyword_denmark_id

- Número de Identificação Pessoal
- CPR
- Det Centrale Personregister
- Personnummer
   
## <a name="drug-enforcement-agency-dea-number"></a>Número da Drug Enforcement Agency (DEA)

### <a name="format"></a>Formato

Duas letras seguidas por sete dígitos

### <a name="pattern"></a>Padrão

O padrão deve incluir todos os seguintes itens:
- Uma letra (não diferencia maiúscula de minúscula) deste conjunto de letras possíveis: abcdefghjklmnprstux, que é um código de inscrito 
- Uma letra (não diferencia maiúscula de minúscula), que é a primeira letra do sobrenome do inscrito 
- Sete dígitos, dos quais o último é o dígito de verificação

### <a name="checksum"></a>Soma de verificação

Sim

### <a name="definition"></a>Definição

Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:
- A função Func_dea_number localiza conteúdo que corresponde ao padrão.
- A soma de verificação passa.

```
<!-- DEA Number -->
<Entity id="9a5445ad-406e-43eb-8bd7-cac17ab6d0e4" recommendedConfidence="85" patternsProximity="300">
  <Pattern confidenceLevel="85">
     <IdMatch idRef="Func_dea_number"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a>Palavras-chave

Nenhum

   
## <a name="eu-debit-card-number"></a>Número de cartão de débito da UE

### <a name="format"></a>Formato

16 dígitos

### <a name="pattern"></a>Padrão

Padrão muito complexo e robusto

### <a name="checksum"></a>Soma de verificação

Sim

### <a name="definition"></a>Definição

Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:
- A função Func_eu_debit_card localiza conteúdo que corresponde ao padrão.
- Pelo menos uma das seguintes opções for verdadeira:
    - Uma palavra-chave de Keyword_eu_debit_card for encontrada.
    - Uma palavra-chave de Keyword_card_terms_dict for encontrada.
    - Uma palavra-chave de Keyword_card_security_terms_dict for encontrada.
    - Uma palavra-chave de Keyword_card_expiration_terms_dict for encontrada.
    - A função Func_expiration_date encontra uma data no formato de data à direita.
- A soma de verificação passa.

```
    <!-- EU Debit Card Number -->
    <Entity id="0e9b3178-9678-47dd-a509-37222ca96b42" patternsProximity="300" recommendedConfidence="85">
      <Pattern confidenceLevel="85">
        <IdMatch idRef="Func_eu_debit_card" />
        <Any minMatches="1">
          <Match idRef="Keyword_eu_debit_card" />
          <Match idRef="Keyword_card_terms_dict" />
          <Match idRef="Keyword_card_security_terms_dict" />
          <Match idRef="Keyword_card_expiration_terms_dict" />
          <Match idRef="Func_expiration_date" />
        </Any>
      </Pattern>
    </Entity>
```

### <a name="keywords"></a>Palavras-chave

#### <a name="keywordeudebitcard"></a>Keyword_eu_debit_card

- número de conta 
- card number
 
- card no.
 
- security number
 
- Cc # 

#### <a name="keywordcardtermsdict"></a>Keyword_card_terms_dict

- acct nbr
 
- acct num
 
- acct no
 
- american express
 
- americanexpress
 
- americano espresso
 
- amex 
- atm card
 
- atm cards
 
- atm kaart
 
- atmcard
 
- atmcards
 
- atmkaart
 
- atmkaarten
 
- bancontact
 
- bank card
 
- bankkaart
 
- card holder
 
- card holders
 
- card num
 
- card number
 
- card numbers
 
- card type
 
- cardano numerico
 
- cardholder
 
- cardholders
 
- cardnumber
 
- cardnumbers
 
- carta bianca
 
- carta credito
 
- carta di credito
 
- cartao de credito
 
- cartao de crédito
 
- cartao de debito
 
- cartao de débito
 
- carte bancaire
 
- carte blanche
 
- carte bleue
 
- carte de credit
 
- carte de crédit
 
- carte di credito
 
- carteblanche
 
- cartão de credito
 
- cartão de crédito
 
- cartão de debito
 
- cartão de débito
 
- cb
 
- ccn
 
- check card
 
- check cards
 
- checkcard

- checkcards
 
- chequekaart
 
- cirrus
 
- cirrus-edc-maestro
 
- controlekaart
 
- controlekaarten
 
- credit card
 
- credit cards
 
- creditcard
 
- creditcards
 
- debetkaart
 
- debetkaarten
 
- debit card
 
- debit cards
 
- debitcard
 
- debitcards
 
- debito automatico
 
- diners club
 
- dinersclub
 
- descobrir 
- discover card
 
- discover cards
 
- discovercard
 
- discovercards
 
- débito automático
- 
edc
 
- eigentümername
 
- european debit card
 
- hoofdkaart
 
- hoofdkaarten
 
- in viaggio
 
- japanese card bureau
 
- japanse kaartdienst
 
- jcb
 
- kaart
 
- kaart num
 
- kaartaantal
 
- kaartaantallen
 
- kaarthouder
 
- kaarthouders
 
- karte
  
- karteninhaber
 
- karteninhabers
- 
kartennr
 
- kartennummer 
- kreditkarte
 
- kreditkarten-nummer 
- kreditkarteninhaber
 
- kreditkarteninstitut
 
- kreditkartennummer
 
- kreditkartentyp
 
- maestro
 
- master card
 
- master cards
 
- mastercard
 
- mastercards 
- MC 
- mister cash
 
- carta n 
- carta 
- Nenhum tarjeta de 
- Nenhum cartao execute 
- Nenhum cartão execute 
- no. de tarjeta
 
- no. do cartao
 
- no. do cartão
 
- carta nr 
- nr. carta
 
- numeri di scheda
 
- numero carta
 
- numero de cartao
 
- numero de carte
 
- numero de cartão
 
- numero de tarjeta

- numero della carta
 
- numero di carta
 
- numero di scheda
 
- numero do cartao
 
- numero do cartão
 
- numéro de carte
 
- nº carta
 
- nº de carte
 
- nº de la carte
 
- nº de tarjeta
 
- nº do cartao
 
- n º cartão 
- nº. do cartão
 
- número de cartao
 
- número de cartão
 
- número de tarjeta
 
- número do cartao 
- scheda dell'assegno
 
- scheda dell'atmosfera
 
- scheda dell'atmosfera
 
- scheda della banca
 
- scheda di controllo
 
- scheda di debito
 
- scheda matrice
 
- schede dell'atmosfera
 
- schede di controllo
 
- schede di debito
 
- schede matrici
 
- scoprono la scheda
 
- scoprono le schede
 
- solo
 
- supporti di scheda
 
- supporto di scheda
 
- opção 
- tarjeta atm
 
- tarjeta credito
 
- tarjeta de atm
 
- tarjeta de credito
 
- tarjeta de debito
 
- tarjeta debito
 
- tarjeta no

- tarjetahabiente
 
- tipo della scheda
 
- ufficio giapponese della 
- scheda
 
- v pay
 
- Salário-v 
- visa
 
- visa plus
 
- visa electron
 
- visto
 
- visum
 
- vpay
   

#### <a name="keywordcardsecuritytermsdict"></a>Keyword_card_security_terms_dict

- card identification number
- card verification 
- cardi la verifica
 
- cid
 
- COD seg 
- segurança de COD 
- segurança de COD 
- COD sicurezza 
- cod. seg
 
- cod. seguranca
 
- cod. segurança
 
- cod. sicurezza
 
- codice di sicurezza
 
- codice di verifica
 
- codigo
 
- codigo de seguranca
 
- codigo de segurança
 
- crittogramma
 
- cryptogram
 
- cryptogramme
 
- CV2 
- cvc
 
- CVC2 
- cvn
 
- cvv
 
- cvv2 
- segurança Cód 
- segurança Cód 
- cód. seguranca
 
- cód. segurança
 
- código
 
- código de seguranca
 
- código de segurança
 
- de kaart controle
 
- geeft nr uit
 
- issue no
 
- issue number
 
- kaartidentificatienummer
 
- kreditkartenprufnummer
 
- kreditkartenprüfnummer
 
- kwestieaantal
 
- no. dell'edizione
 
- no. di sicurezza
 
- numero de securite
 
- numero de verificacao
 
- numero dell'edizione
 
- numero di identificazione della 
- scheda
 
- numero di sicurezza
 
- numero van veiligheid
 
- numéro de sécurité
 
- nº autorizzazione
 
- número de verificação
 
- perno il blocco
 
- pin block
 
- prufziffer
 
- prüfziffer
 
- security code
 
- security no
 
- security number
 
- sicherheits kode
 
- sicherheitscode
 
- sicherheitsnummer
 
- speldblok
 
- veiligheid nr
 
- veiligheidsaantal
 
- veiligheidscode
 
- veiligheidsnummer
 
- verfalldatum
 

#### <a name="keywordcardexpirationtermsdict"></a>Keyword_card_expiration_terms_dict

- ablauf
 
- data de expiracao
 
- data de expiração
 
- data del exp
 
- data di exp
 
- data di scadenza
 
- data em que expira
 
- data scad
 
- data scadenza
 
- date de validité
 
- datum afloop
 
- datum van exp
 
- de afloop
 
- espira
 
- espira
 
- exp date
 
- exp datum
 
- expiração 
- expire
 
- expires
 
- expiry
 
- fecha de expiracion
 
- fecha de venc
 
- gultig bis
 
- gultigkeitsdatum
 
- gültig bis
 
- gültigkeitsdatum
 
- la scadenza
 
- scadenza
 
- valable
 
- validade
 
- valido hasta
 
- valor
 
- venc
 
- vencimento
 
- vencimiento
 
- verloopt
 
- vervaldag
 
- vervaldatum
 
- vto
 
- válido hasta
 
   
## <a name="eu-drivers-license-number"></a>Número de carteira de motorista da UE

Para saber mais, consulte o [tipo de informação confidencial do número de carteira de motorista da UE](eu-driver-s-license-number.md).
  
## <a name="eu-national-identification-number"></a>Número de identificação nacional da UE

Para saber mais, consulte o [tipo de informação confidencial do número de identificação nacional da UE](eu-national-identification-number.md).
  
## <a name="eu-passport-number"></a>Número de passaporte da UE

Para saber mais, consulte o [tipo de informação confidencial do número de passaporte da UE](eu-passport-number.md).
  
## <a name="eu-social-security-number-or-equivalent-id"></a>ID do número de Seguridade Social da UE ou equivalente

Para saber mais, consulte o [número de Seguridade Social da UE ou tipo de informação confidencial ID equivalente](eu-social-security-number-or-equivalent-id.md).
  
## <a name="eu-tax-identification-number"></a>Número de identificação de imposto da UE

Para saber mais, consulte o [tipo de informação confidencial do número de identificação de imposto da UE](eu-tax-identification-number.md).
  
## <a name="finland-national-id"></a>ID nacional da Finlândia

### <a name="format"></a>Formato

Seis dígitos mais um caractere indicando um século mais três dígitos mais um dígito de verificação

### <a name="pattern"></a>Padrão

O padrão deve incluir todos os seguintes itens:
- Seis dígitos no formato DDMMAA que é uma data de nascimento 
- Marcador do século (qualquer '-', '+' ou 'a') 
- Número de identificação pessoal de três dígitos 
- Um dígito ou letra (não diferencia maiúscula de minúscula), que é um dígito de verificação

### <a name="checksum"></a>Soma de verificação

Sim

### <a name="definition"></a>Definição

Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:
- A função Func_finnish_national_id localiza conteúdo que corresponde ao padrão.
- Uma palavra-chave de Keyword_finnish_national_id for encontrada.
- A soma de verificação passa.

```
<!-- Finnish National ID-->
<Entity id="338FD995-4CB5-4F87-AD35-79BD1DD926C1" patternsProximity="300" recommendedConfidence="85">
  <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_finnish_national_id" />
          <Match idRef="Keyword_finnish_national_id" />
  </Pattern>
</Entity>
```

### <a name="keywords"></a>Palavras-chave

- Keyword_finnish_national_id
- 

Sosiaaliturvatunnus
- SOTU Henkilötunnus HETU
- Personbeteckning
- Personnummer
   
## <a name="finland-passport-number"></a>Número de Passaporte da Finlândia

Formatar a combinação de nove letras e dígitos combinação de padrão de nove letras e dígitos: política de DLP de uma soma de verificação não definição do duas letras (não maiusculas de minúsculas) sete dígitos é 75% confiante de que detectou esse tipo de informações confidenciais se, contido em um proximidade de 300 caracteres: A expressão regular Regex_finland_passport_number encontra o conteúdo que corresponde ao padrão. Uma palavra-chave de Keyword_finland_passport_number é encontrada. <!-- Finland Passport Number --> 
 <Entity id="d1685ac3-1d3a-40f8-8198-32ef5669c7a5" recommendedConfidence="75" patternsProximity="300"> <Pattern confidenceLevel="75"> <IdMatch idRef="Regex_finland_passport_number"/> <Match idRef="Keyword_finland_passport_number"/> </Pattern> 
 </Entity> Palavras-chave Keyword_finland_passport_number Passport Passi
   
## <a name="france-drivers-license-number"></a>Número de carteira de motorista da França

### <a name="format"></a>Formato

12 dígitos

### <a name="pattern"></a>Padrão

12 dígitos com a validação para descontar padrões similares, como números de telefone em francês

### <a name="checksum"></a>Soma de verificação

Não

### <a name="definition"></a>Definição

Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:
- A função Func_french_drivers_license localiza conteúdo que corresponde ao padrão.
- Pelo menos uma das seguintes opções for verdadeira:
- Uma palavra-chave de Keyword_french_drivers_license for encontrada.
- A função Func_eu_date encontra uma data no formato de data à direita.

```
<!-- France Driver's License Number -->
<Entity id="18e55a36-a01b-4b0f-943d-dc10282a1824" patternsProximity="300" recommendedConfidence="75">
  <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_french_drivers_license" />
        <Any minMatches="1">
          <Match idRef="Keyword_french_drivers_license" />
          <Match idRef="Func_eu_date" />
        </Any>
  </Pattern>
</Entity>
```

### <a name="keywords"></a>Palavras-chave

#### <a name="keywordfrenchdriverslicense"></a>Keyword_french_drivers_license

- drivers licence
- 
drivers license
- driving licence

- orientando licença
- 
permis de conduire
- 
licence number
- 
license number
- 
licence numbers
- 

license numbers

## <a name="france-national-id-card-cni"></a>Cartão de identificação nacional da França (CNI)

### <a name="format"></a>Formato

12 dígitos

### <a name="pattern"></a>Padrão

12 dígitos

### <a name="checksum"></a>Soma de verificação

Não

### <a name="definition"></a>Definição

Uma política de DLP tem 65% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:
- A expressão regular Regex_france_cni localiza o conteúdo que corresponde ao padrão.

```
<!-- France CNI -->
<Entity id="f741ac74-1bc0-4665-b69b-f0c7f927c0c4" patternsProximity="300" recommendedConfidence="65">
  <Pattern confidenceLevel="65">
        <IdMatch idRef="Regex_france_cni" />
  </Pattern>
</Entity>
```

### <a name="keywords"></a>Palavras-chave

Nenhum
   
## <a name="france-passport-number"></a>Número de passaporte da França

### <a name="format"></a>Formato

Nove letras e dígitos

### <a name="pattern"></a>Padrão

Nove letras e dígitos:
- Dois dígitos 
- Duas letras (não diferenciam maiúsculas de minúsculas) 
- Cinco dígitos

### <a name="checksum"></a>Soma de verificação

Não

### <a name="definition"></a>Definição

Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:
- A função Func_fr_passport localiza conteúdo que corresponde ao padrão.
- Uma palavra-chave de Keyword_passport for encontrada.

```
<!-- France Passport Number -->
<Entity id="3008b884-8c8c-4cd8-a289-99f34fc7ff5d" patternsProximity="300" recommendedConfidence="75">
  <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_fr_passport" />
        <Match idRef="Keyword_passport" />
  </Pattern>
</Entity>
```

### <a name="keywords"></a>Palavras-chave

#### <a name="keywordpassport"></a>Keyword_passport

- Passport Number
- 
Passport No
- Passport #

- Passport#

- PassportID
- Passportno

- passportnumber

- パスポート
- パスポート番号

- パスポートのNum

- 
パスポート ＃
 
- Numéro de passeport
- 
Passeport n °
- Passeport Non

- Passeport #

- Passeport#

- PasseportNon
- 

Passeportn °

      
## <a name="france-social-security-number-insee"></a>Número de seguridade social da França (INSEE)

### <a name="format"></a>Formato

15 dígitos

### <a name="pattern"></a>Padrão

Deve corresponder a um dos dois padrões:
- 13 dígitos seguidos por um espaço seguido por dois dígitos<br/>
ou
- 15 dígitos consecutivos

### <a name="checksum"></a>Soma de verificação

Sim

### <a name="definition"></a>Definição

Uma política de DLP tem 95% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:
- A função Func_french_insee ou Func_fr_insee encontra o conteúdo que corresponde ao padrão.
- Uma palavra-chave de Keyword_fr_insee for encontrada.
- A soma de verificação passa.

Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:
- A função Func_french_insee ou Func_fr_insee encontra o conteúdo que corresponde ao padrão.
- Nenhuma palavra-chave de Keyword_fr_insee for encontrada.
- A soma de verificação passa.

```
<!-- France INSEE -->
<Entity id="71f62b97-efe0-4aa1-aa49-e14de253619d" patternsProximity="300" recommendedConfidence="85">
  <Pattern confidenceLevel="95">
        <IdMatch idRef="Func_french_insee" />
        <Match idRef="Func_fr_insee" />
        <Any minMatches="1">
          <Match idRef="Keyword_fr_insee" />
        </Any>
  </Pattern>
  <Pattern confidenceLevel="85">
        <IdMatch idRef="Func_french_insee" />
        <Match idRef="Func_fr_insee" />
        <Any minMatches="0" maxMatches="0">
          <Match idRef="Keyword_fr_insee" />
        </Any>
  </Pattern>
</Entity>
```

### <a name="keywords"></a>Palavras-chave

#### <a name="keywordfrinsee"></a>Keyword_fr_insee

- insee
- 
securité sociale
- 
securite sociale
- 
national id
- 
national identification
- 
numéro d'identité
- Nenhum d'identité
- 
no. d'identité
- 
numero d'identite
- Nenhum d'identite
- 
no. d'identite
- social security number

- 
social security code
- social insurance number
- 
le numéro d'identification nationale
- 
d'identité nationale
- 
numéro de sécurité sociale
- 
le code de la sécurité sociale
- 
numéro d'assurance sociale
- 
numéro de sécu
- 
code sécu
 
   
## <a name="german-drivers-license-number"></a>Número de carteira de motorista da Alemanha

### <a name="format"></a>Formato

Combinação de 11 dígitos e letras

### <a name="pattern"></a>Padrão

11 dígitos e letras (não diferenciam maiúsculas de minúsculas):
- Um dígito ou letra 
- Dois dígitos 
- Seis dígitos ou letras 
- Um dígito 
- Um dígito ou letra

### <a name="checksum"></a>Soma de verificação

Sim

### <a name="definition"></a>Definição

Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:
- A função Func_german_drivers_license localiza conteúdo que corresponde ao padrão.
- Pelo menos uma das seguintes opções for verdadeira:
    - Uma palavra-chave de Keyword_german_drivers_license_number for encontrada.
    - Uma palavra-chave de Keyword_german_drivers_license_collaborative for encontrada.
    - Uma palavra-chave de Keyword_german_drivers_license for encontrada.
- A soma de verificação passa.

```
<!-- German Driver's License Number -->
<Entity id="91da9335-1edb-45b7-a95f-5fe41a16c63c" patternsProximity="300" recommendedConfidence="75">
  <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_german_drivers_license" />
        <Any minMatches="1">
          <Match idRef="Keyword_german_drivers_license_number" />
          <Match idRef="Keyword_german_drivers_license_collaborative" />
          <Match idRef="Keyword_german_drivers_license" />
        </Any>
  </Pattern>
</Entity>
```

### <a name="keywords"></a>Palavras-chave

#### <a name="keywordgermandriverslicensenumber"></a>Keyword_german_drivers_license_number

- Führerschein
- 
Fuhrerschein
- Fuehrerschein
- 
Führerscheinnummer
- 
Fuhrerscheinnummer
- 
Fuehrerscheinnummer
- 
Führerschein-
 
- Fuhrerschein-
 
- Fuehrerschein-
 
- FührerscheinnummerNr
- FuhrerscheinnummerNr
- FuehrerscheinnummerNr
- FührerscheinnummerKlasse
- FuhrerscheinnummerKlasse
- FuehrerscheinnummerKlasse
- Führerschein- Nr

- Fuhrerschein- Nr

- Fuehrerschein- Nr
 
- Führerschein- Klasse
 
- Fuhrerschein- Klasse
 
- Fuehrerschein- Klasse
- FührerscheinnummerNr 
- FuhrerscheinnummerNr 
- FuehrerscheinnummerNr 
- FührerscheinnummerKlasse 
- FuhrerscheinnummerKlasse 
- FuehrerscheinnummerKlasse 
- Führerschein- Nr
 
- Fuhrerschein- Nr
 
- Fuehrerschein- Nr
 
- Führerschein- Klasse
 
- Fuhrerschein- Klasse
 
- Fuehrerschein- Klasse 
- DL 
- DLS
- 
Driv Lic
 
- Driv Licen
 
- Driv License
- 
Driv Licenses
 
- Driv Licence
 
- Driv Licences
 
- Driv Lic
 
- Driver Licen
 
- Driver de licença 
- Licenças de driver 
- Driver Licence
 
- Driver Licences
 
- Drivers Lic 
- Drivers Licen 
- Carteira de motorista 
- Licenças de drivers 
- Drivers de licença 
- Licenças de drivers 
- Lic do driver 
- Driver's Licen
 
- De motorista carteira 
- Licenças de motorista 
- Driver's Licence
 
- Driver's Licences
 
- Driving Lic
 
- Driving Licen
 
- Driving License
 
- Driving Licenses
 
- Driving Licence

 
- Driving Licences

#### <a name="keywordgermandriverslicensecollaborative"></a>Keyword_german_drivers_license_collaborative

- 
Nr-Führerschein
 
- Nr-Fuhrerschein
 
- Nr-Fuehrerschein
 
- No-Führerschein
 
- No-Fuhrerschein
 
- No-Fuehrerschein
 
- N-Führerschein
 
- N-Fuhrerschein
 
- N-Fuehrerschein
- 
Nr-Führerschein
 
- Nr-Fuhrerschein
 
- Nr-Fuehrerschein
 
- No-Führerschein
 
- No-Fuhrerschein
 
- No-Fuehrerschein
 
- N-Führerschein
 
- N-Fuhrerschein
 
- N-Fuehrerschein 

#### <a name="keywordgermandriverslicense"></a>Keyword_german_drivers_license

- ausstellungsdatum
- 
ausstellungsort
- 
ausstellende behöde
- 
ausstellende behorde
- 

ausstellende behoerde
   
## <a name="german-passport-number"></a>Número de passaporte da Alemanha

### <a name="format"></a>Formato

10 dígitos ou letras

### <a name="pattern"></a>Padrão

O padrão deve incluir todos os seguintes itens:
- Primeiro caractere é um dígito ou uma letra desse conjunto (C, F, G, H, J, K) 
- Três dígitos 
- Cinco dígitos ou letras a partir desse conjunto (C, -H, J N, P, R, T, V-Z) 
- Um dígito

### <a name="checksum"></a>Soma de verificação

Sim

### <a name="definition"></a>Definição

Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:
- A função Func_german_passport localiza conteúdo que corresponde ao padrão.
- Uma palavra-chave de qualquer uma das cinco listas de palavras-chave for encontrada.
- A soma de verificação passa.

Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:
- A função Func_german_passport_data localiza conteúdo que corresponde ao padrão.
- Uma palavra-chave de qualquer uma das cinco listas de palavras-chave for encontrada.
- A soma de verificação passa.

```
<!-- German Passport Number -->
<Entity id="2e3da144-d42b-47ed-b123-fbf78604e52c" patternsProximity="300" recommendedConfidence="75">
  <Pattern confidenceLevel="85">
        <IdMatch idRef="Func_german_passport" />
        <Any minMatches="1">
          <Match idRef="Keyword_german_passport" />
          <Match idRef="Keyword_german_passport_collaborative" />
          <Match idRef="Keyword_german_passport_number" />
          <Match idRef="Keyword_german_passport1" />
          <Match idRef="Keyword_german_passport2" />
        </Any>
  </Pattern>
  <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_german_passport_data" />
        <Any minMatches="1">
          <Match idRef="Keyword_german_passport" />
          <Match idRef="Keyword_german_passport_collaborative" />
          <Match idRef="Keyword_german_passport_number" />
          <Match idRef="Keyword_german_passport1" />
          <Match idRef="Keyword_german_passport2" />
        </Any>
  </Pattern>
</Entity>
```

### <a name="keywords"></a>Palavras-chave

#### <a name="keywordgermanpassport"></a>Keyword_german_passport

- reisepass
- 
reisepasse
- 
reisepassnummer
- passport
- 

passports

#### <a name="keywordgermanpassportcollaborative"></a>Keyword_german_passport_collaborative

- geburtsdatum
- ausstellungsdatum
- 
ausstellungsort

#### <a name="keywordgermanpassportnumber"></a>Keyword_german_passport_number

Não-Reisepass Nr-Reisepass

#### <a name="keywordgermanpassport1"></a>Keyword_german_passport1

Reisepass-Nr


#### <a name="keywordgermanpassport2"></a>Keyword_german_passport2

bnationalit.t
   
## <a name="germany-identity-card-number"></a>Número da carteira de identidade alemã

### <a name="format"></a>Formato

Desde 1 de novembro de 2010: nove letras e dígitos

De 1987 1 de abril até 31 dígitos 2010:10 de outubro

### <a name="pattern"></a>Padrão

Desde 1º de novembro de 2010:
- Uma letra (não diferencia maiúscula de minúscula) 
- Oito dígitos

De 1 de abril de 1987 até 31 de outubro de 2010:
- 10 dígitos

### <a name="checksum"></a>Soma de verificação

Não

### <a name="definition"></a>Definição

Uma política de DLP tem 65% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:
- A expressão regular Regex_germany_id_card encontra o conteúdo que corresponde ao padrão.
- Uma palavra-chave de Keyword_germany_id_card é encontrada.

```
<!-- Germany Identity Card Number -->
<Entity id="e577372f-c42e-47a0-9d85-bebed1c237d4" recommendedConfidence="65" patternsProximity="300">
  <Pattern confidenceLevel="65">
     <IdMatch idRef="Regex_germany_id_card"/>
     <Match idRef="Keyword_germany_id_card"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a>Palavras-chave

#### <a name="keywordgermanyidcard"></a>Keyword_germany_id_card

- Cartão de Identidade
- ID
- Identificação 
- Personalausweis
- Identifizierungsnummer
- Ausweis
- Identifikation
   
## <a name="greece-national-id-card"></a>Cartão de Identificação Nacional da Grécia

### <a name="format"></a>Formato

Combinação de 7 a 8 letras e números mais um traço

### <a name="pattern"></a>Padrão

Sete letras e números (formato antigo):
- Uma letra (qualquer letra do alfabeto grego)  
- Um traço 
- Seis dígitos

Oito letras e números (novo formato):
- Duas letras cujos caracteres maiúsculos ocorre em alfabetos latino e grego (ABEZHIKMNOPTYX)  
- Um traço 
- Seis dígitos

### <a name="checksum"></a>Soma de verificação

Não

### <a name="definition"></a>Definição

Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:
- A expressão regular Regex_greece_id_card encontra o conteúdo que corresponde ao padrão.
- Uma palavra-chave de Keyword_greece_id_card é encontrada.

```
<!-- Greece National ID Card -->
<Entity id="82568215-1da1-46d3-874a-d2294d81b5ac" recommendedConfidence="85" patternsProximity="300">
  <Pattern confidenceLevel="85">
     <IdMatch idRef="Regex_greece_id_card"/>
     <Match idRef="Keyword_greece_id_card"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a>Palavras-chave

#### <a name="keywordgreeceidcard"></a>Keyword_greece_id_card

- Cartão de identidade grego
- Tautotita
- Δελτίο αστυνομικής ταυτότητας
- Ταυτότητα
   
## <a name="hong-kong-identity-card-hkid-number"></a>Número do Cartão de Identidade de Hong Kong (HKID)

### <a name="format"></a>Formato

Combinação de 8 a 9 letras e números mais parênteses opcionais ao redor do caractere final

### <a name="pattern"></a>Padrão

Combinação de 8 a 9 letras:
- 1 a 2 letras (não diferenciam maiúsculas de minúsculas) 
- Seis dígitos 
- O caractere final (qualquer dígito ou a letra A), que é o dígito de verificação e é opcionalmente colocado entre parênteses.

### <a name="checksum"></a>Soma de verificação

Sim

### <a name="definition"></a>Definição

Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:
- A função Func_hong_kong_id_card encontra o conteúdo que corresponde ao padrão.
- Uma palavra-chave de Keyword_hong_kong_id_card é encontrada.
- A soma de verificação passa.

Uma política de DLP tem 65% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:
- A função Func_hong_kong_id_card encontra o conteúdo que corresponde ao padrão.
- A soma de verificação passa.

```
<!-- Hong Kong Identity Card (HKID) number -->
<Entity id="e63c28a7-ad29-4c17-a41a-3d2a0b70fd9c" recommendedConfidence="75" patternsProximity="300">
  <Pattern confidenceLevel="75">
     <IdMatch idRef="Func_hong_kong_id_card"/>
     <Match idRef="Keyword_hong_kong_id_card"/>
  </Pattern>
  <Pattern confidenceLevel="65">
     <IdMatch idRef="Func_hong_kong_id_card"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a>Palavras-chave

#### <a name="keywordhongkongidcard"></a>Keyword_hong_kong_id_card

- Número do Cartão de Identidade de Hong Kong
- HKID
- Cartão de identificação
- 香港身份證
 
- 香港永久性居民身份證
 
   
## <a name="india-permanent-account-number-pan"></a>Número da Conta Permanente da Índia (PAN)

### <a name="format"></a>Formato

10 letras ou dígitos

### <a name="pattern"></a>Padrão

10 letras ou dígitos.
- Cinco letras (não diferenciam maiúsculas de minúsculas) 
- Quatro dígitos 
- Uma letra que é um dígito de verificação alfabético

### <a name="checksum"></a>Soma de verificação

Sim

### <a name="definition"></a>Definição

Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:
- A expressão regular Regex_india_permanent_account_number encontra o conteúdo que corresponde ao padrão.
- Uma palavra-chave de Keyword_india_permanent_account_number é encontrada.
- A soma de verificação passa.

```
<!-- India Permanent Account Number -->
<Entity id="2602bfee-9bb0-47a5-a7a6-2bf3053e2804" recommendedConfidence="85" patternsProximity="300">
  <Pattern confidenceLevel="85">
     <IdMatch idRef="Regex_india_permanent_account_number"/>
     <Match idRef="Keyword_india_permanent_account_number"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a>Palavras-chave

#### <a name="keywordindiapermanentaccountnumber"></a>Keyword_india_permanent_account_number

- Número da Conta Permanente
 
- PAN
 
   
## <a name="india-unique-identification-aadhaar-number"></a>Número de Identificação Exclusivo da Índia (Aadhaar)

### <a name="format"></a>Formato

12 dígitos contendo espaços opcionais ou traços

### <a name="pattern"></a>Padrão

12 dígitos:
- Quatro dígitos 
- Um espaço ou um traço opcional  
- Quatro dígitos 
- Um espaço ou um traço opcional  
- O dígito final que é o dígito de verificação

### <a name="checksum"></a>Soma de verificação

Sim

### <a name="definition"></a>Definição

Uma política DLP é de 85% confiante de que detectou esse tipo de informações confidenciais if, dentro de uma proximidade de 300 caracteres: A função Func_india_aadhaar encontra o conteúdo que corresponde ao padrão. Uma palavra-chave de Keyword_india_aadhar é encontrada. A soma de verificação passa. Uma política de DLP é 75% confiante de que detectou esse tipo de informações confidenciais if, dentro de uma proximidade de 300 caracteres: A função Func_india_aadhaar encontra o conteúdo que corresponde ao padrão. A soma de verificação passa. <!-- India Unique Identification (Aadhaar) number -->
<Entity id="1ca46b29-76f5-4f46-9383-cfa15e91048f" recommendedConfidence="85" patternsProximity="300"> <Pattern confidenceLevel="85"> <IdMatch idRef="Func_india_aadhaar"/> <Match idRef="Keyword_india_aadhar"/> </Pattern> <Pattern confidenceLevel="75"> <IdMatch idRef="Func_india_aadhaar"/> </Pattern>
</Entity>

### <a name="keywords"></a>Palavras-chave
   
#### <a name="keywordindiaaadhar"></a>Keyword_india_aadhar
- Aadhar
- Aadhaar
- UID
- आधार
   
## <a name="indonesia-identity-card-ktp-number"></a>Número do Cartão de Identidade da Indonésia (KTP)

### <a name="format"></a>Formato

16 dígitos contendo pontos opcionais

### <a name="pattern"></a>Padrão

16 dígitos:
- Código de província de dois dígitos  
- Um ponto (opcional)  
- Código de dois dígitos da regência ou da cidade  
- Código de dois dígitos do subdistrito  
- Um ponto (opcional)  
- Seis dígitos no formato DDMMAA que são a data de nascimento 
- Um ponto (opcional)  
- Quatro dígitos

### <a name="checksum"></a>Soma de verificação

Não

### <a name="definition"></a>Definição

Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:
- A expressão regular Regex_indonesia_id_card encontra o conteúdo que corresponde ao padrão.
- Uma palavra-chave de Keyword_indonesia_id_card é encontrada.

Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:
- A expressão regular Regex_indonesia_id_card encontra o conteúdo que corresponde ao padrão.

```
<!-- Indonesia Identity Card (KTP) Number -->
<Entity id="da68fdb0-f383-4981-8c86-82689d3b7d55" recommendedConfidence="85" patternsProximity="300">
  <Pattern confidenceLevel="85">
     <IdMatch idRef="Regex_indonesia_id_card"/>
     <Match idRef="Keyword_indonesia_id_card"/>
  </Pattern>
  <Pattern confidenceLevel="75">
     <IdMatch idRef="Regex_indonesia_id_card"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a>Palavras-chave
   
#### <a name="keywordindonesiaidcard"></a>Keyword_indonesia_id_card

- KTP
- Kartu Tanda Penduduk
 
- Nomor Induk Kependudukan
 
   
## <a name="international-banking-account-number-iban"></a>Número da Conta Bancária Internacional (IBAN)

### <a name="format"></a>Formato

Verificar o código de país (duas letras) mais dígitos (dois dígitos) plus /bbO número (até 30 caracteres)

### <a name="pattern"></a>Padrão

O padrão deve incluir todos os seguintes itens:

- Código de país com duas letras
- Dois dígitos de verificação (seguidos por um espaço opcional) 
- grupos de 1 a 7 de quatro letras ou dígitos (pode ser separada por espaços)
- 1 a 3 letras ou dígitos

O formato para cada país é ligeiramente diferente. O tipo de informações confidenciais IBAN aborda essas 60 países:

AD, ae, al, at, az, ba, ser, bg, bbH, ESC, cr, cy, cz, de, dk, execute, ee, es, fi, fo, fr, gb, ge, gi, gl, GA, RH, hu, isto é, il, há, ele, kw, kz, lb, li, lt, lu, lv, mc, md, me, mk, mr, mt, mu , nl, não pl, pt, LIN, rs, sa, se, si, sk, sm, tn, tr, vg

### <a name="checksum"></a>Soma de verificação

Sim

### <a name="definition"></a>Definição

Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:
- A função Func_iban localiza conteúdo que corresponde ao padrão.
- A soma de verificação passa.

```
<Entity id="e7dc4711-11b7-4cb0-b88b-2c394a771f0e" patternsProximity="300" recommendedConfidence="85">
  <Pattern confidenceLevel="85">
        <IdMatch idRef="Func_iban" />
  </Pattern>
</Entity>
```

### <a name="keywords"></a>Palavras-chave

Nenhum

   
## <a name="ip-address"></a>Endereço IP

### <a name="format"></a>Formato

#### <a name="ipv4"></a>IPv4:
Padrão complexo que é responsável por versões formatadas (pontos) e não formatadas (sem pontos) dos endereços IPv4

#### <a name="ipv6"></a>IPv6:
Padrão complexo que é responsável por números IPv6 formatados (que incluem dois pontos)

### <a name="pattern"></a>Padrão

### <a name="checksum"></a>Soma de verificação

Não

### <a name="definition"></a>Definição

Para IPv6, uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:
- A expressão regular Regex_ipv6_address localiza o conteúdo que corresponde ao padrão.
- Nenhuma palavra-chave de Keyword_ipaddress for encontrada.

Para IPv4, uma política de DLP tem 95% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:
- A expressão regular Regex_ipv4_address localiza o conteúdo que corresponde ao padrão.
- Uma palavra-chave de Keyword_ipaddress for encontrada.

Para IPv6, uma política de DLP tem 95% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:
- A expressão regular Regex_ipv6_address localiza o conteúdo que corresponde ao padrão.
- Nenhuma palavra-chave de Keyword_ipaddress for encontrada.

```
    <!-- IP Address -->
    <Entity id="1daa4ad5-e2dd-4ca4-a788-54722c09efb2" patternsProximity="300" recommendedConfidence="85">
      <Pattern confidenceLevel="85">
        <IdMatch idRef="Regex_ipv6_address" />
        <Any minMatches="0" maxMatches="0">
          <Match idRef="Keyword_ipaddress" />
        </Any>
      </Pattern>
      <Pattern confidenceLevel="95">
        <IdMatch idRef="Regex_ipv4_address" />
        <Any minMatches="1">
          <Match idRef="Keyword_ipaddress" />
        </Any>
      </Pattern>
      <Pattern confidenceLevel="95">
        <IdMatch idRef="Regex_ipv6_address" />
        <Any minMatches="1">
          <Match idRef="Keyword_ipaddress" />
        </Any>
      </Pattern>
    </Entity>
```

### <a name="keywords"></a>Palavras-chave

#### <a name="keywordipaddress"></a>Keyword_ipaddress

- IP (esta palavra-chave diferencia maiúsculas de minúsculas)
- ip address
 
- endereços ip
- internet protocol
- 
IP כתובת ה
 
   
## <a name="international-classification-of-diseases-icd-10-cm"></a>Classificação internacional de doenças (ICD-10-CM)

### <a name="format"></a>Formato

Dicionário

### <a name="pattern"></a>Padrão

Palavra-chave

### <a name="checksum"></a>Soma de verificação

Não

### <a name="definition"></a>Definição

Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:
- Uma palavra-chave de Dictionary_icd_10_cm é encontrada.

```
      <!-- ICD-10 CM -->
      <Entity id="3356946c-6bb7-449b-b253-6ffa419c0ce7" patternsProximity="300" recommendedConfidence="85">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Dictionary_icd_10_cm" />
        </Pattern>
      </Entity>
```

Palavras-chave

Qualquer termo do dicionário Dictionary_icd_10_cm palavra-chave, que é baseada na [classificação de internacional de doenças, décimo revisão, a modificação de início de estudos clínicos (ICD-10-CM)](https://go.microsoft.com/fwlink/?linkid=852604). Esse tipo de procura apenas o termo, e não os códigos de seguros.

   
## <a name="international-classification-of-diseases-icd-9-cm"></a>Classificação internacional de doenças (ICD-9-CM)

### <a name="format"></a>Formato

Dicionário

### <a name="pattern"></a>Padrão

Palavra-chave

### <a name="checksum"></a>Soma de verificação

Não

### <a name="definition"></a>Definição

Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:
- Uma palavra-chave de Dictionary_icd_9_cm é encontrada.

```
      <Entity id="fa3f9c74-ee07-4c52-b5f2-085d6b2c0ec4" patternsProximity="300" recommendedConfidence="85">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Dictionary_icd_9_cm" />
        </Pattern>
      </Entity>
```

### <a name="keywords"></a>Palavras-chave

Qualquer termo do dicionário Dictionary_icd_9_cm palavra-chave, que é baseada na [classificação de internacional de doenças, nono revisão, a modificação de início de estudos clínicos (ICD-9-CM)](https://go.microsoft.com/fwlink/?linkid=852605). Esse tipo de procura apenas o termo, e não os códigos de seguros.
   
## <a name="ireland-personal-public-service-pps-number"></a>Número de Serviço Público Pessoal (PPS) da Irlanda

### <a name="format"></a>Formato

Formato antigo (até 31 de dezembro de 2012):
- Sete dígitos seguidos de 1 a 2 letras  

Novo formato (1 de janeiro de 2013 e depois):
- Sete dígitos seguidos de duas letras

### <a name="pattern"></a>Padrão

Formato antigo (até 31 de dezembro de 2012):
- Sete dígitos  
- 1 a 2 letras (não diferenciam maiúsculas de minúsculas) 

Novo formato (1 de janeiro de 2013 e depois):
- Sete dígitos  
- Uma letra (não diferencia maiúsculas de minúsculas) que é um dígito de verificação alfabético  
- A letra "A" ou "H" (não diferencia maiúsculas de minúsculas)

### <a name="checksum"></a>Soma de verificação

Sim

### <a name="definition"></a>Definição

Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:
- A função Func_ireland_pps encontra o conteúdo que corresponde ao padrão.
- Uma das seguintes opções for verdadeira:
    - Uma palavra-chave de Keyword_ireland_pps é encontrada.
    - A função Func_eu_date encontra uma data no formato de data à direita.
- A soma de verificação passa.

Uma política de DLP tem 65% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:
- A função Func_ireland_pps encontra o conteúdo que corresponde ao padrão.
- A soma de verificação passa.

```
<!-- Ireland Personal Public Service (PPS) Number -->
<Entity id="1cdb674d-c19a-4fcf-9f4b-7f56cc87345a" recommendedConfidence="85" patternsProximity="300">
  <Pattern confidenceLevel="85">
     <IdMatch idRef="Func_ireland_pps"/>
     <Any minMatches="1">
  <Match idRef="Keyword_ireland_pps"/>
  <Match idRef="Func_eu_date"/>
     </Any>
  </Pattern>
  <Pattern confidenceLevel="65">
     <IdMatch idRef="Func_ireland_pps"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a>Palavras-chave

#### <a name="keywordirelandpps"></a>Keyword_ireland_pps

- Número do Serviço Público Pessoal 
 
- Número PPS
 
- Núm PPS
 
- Nº PPS
 
- # PPS
 
- #PPS
 
- NPPS
 
- Cartão dos Serviços Públicos
 
- Uimhir Phearsanta Seirbhíse Poiblí
 
- Uimh. PSP
 
- PSP
 
   
## <a name="israel-bank-account-number"></a>Número de conta bancária de Israel

### <a name="format"></a>Formato

13 dígitos

### <a name="pattern"></a>Padrão

Formatado:
- Dois dígitos 
- Um traço 
- Três dígitos 
- Um traço 
- Oito dígitos

Não Formatado:
- 13 dígitos consecutivos

### <a name="checksum"></a>Soma de verificação

Não

### <a name="definition"></a>Definição

Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:
- A expressão regular Regex_israel_bank_account_number localiza o conteúdo que corresponde ao padrão.
- Uma palavra-chave de Keyword_israel_bank_account_number for encontrada.

```
<!-- Israel Bank Account Number -->
<Entity id="7d08b2ff-a0b9-437f-957c-aeddbf9b2b25" patternsProximity="300" recommendedConfidence="75">
    <Pattern confidenceLevel="75">
        <IdMatch idRef="Regex_israel_bank_account_number" />
        <Any minMatches="1">
          <Match idRef="Keyword_israel_bank_account_number" />
        </Any>
    </Pattern>
</Entity>
```

### <a name="keywords"></a>Palavras-chave

#### <a name="keywordisraelbankaccountnumber"></a>Keyword_israel_bank_account_number

- Bank Account Number
 
- Bank Account
 
- Account Number
 
- מספר חשבון בנק
 
   
## <a name="israel-national-id"></a>ID nacional de Israel

### <a name="format"></a>Formato

Nove dígitos

### <a name="pattern"></a>Padrão

Nove dígitos consecutivos

### <a name="checksum"></a>Soma de verificação

Sim

### <a name="definition"></a>Definição

Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:
- A função Func_israeli_national_id_number localiza conteúdo que corresponde ao padrão.
- Uma palavra-chave de Keyword_Israel_National_ID for encontrada.
- A soma de verificação passa.

```
<!-- Israel National ID Number -->
<Entity id="e05881f5-1db1-418c-89aa-a3ac5c5277ee" patternsProximity="300" recommendedConfidence="75">
    <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_israeli_national_id_number" />
        <Any minMatches="1">
          <Match idRef="Keyword_Israel_National_ID" />
        </Any>
    </Pattern>
</Entity>
```

### <a name="keywords"></a>Palavras-chave

#### <a name="keywordisraelnationalid"></a>Keyword_Israel_National_ID

- מספר זהות
 
- Número de identificação nacional
   
## <a name="italy-drivers-license-number"></a>Número de carteira de motorista da Itália

### <a name="format"></a>Formato

Uma combinação de 10 letras e dígitos

### <a name="pattern"></a>Padrão

- Uma combinação de 10 letras e dígitos:
- Uma letra (não diferencia maiúscula de minúscula) 
- A letra "A" ou "V" (não diferencia maiúscula de minúscula) 
- Sete letras (não diferenciam maiúsculas de minúsculas), dígitos ou o caractere de sublinhado 
- Uma letra (não diferencia maiúscula de minúscula)

### <a name="checksum"></a>Soma de verificação

Não

### <a name="definition"></a>Definição

Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:
- A expressão regular Regex_italy_drivers_license_number localiza o conteúdo que corresponde ao padrão.
- Uma palavra-chave de Keyword_italy_drivers_license_number for encontrada.

```
<!-- Italy Driver's license Number -->
<Entity id="97d6244f-9157-41bd-8e0c-9d669a5c4d71" patternsProximity="300" recommendedConfidence="75">
    <Pattern confidenceLevel="75">
        <IdMatch idRef="Regex_italy_drivers_license_number" />
        <Any minMatches="1">
          <Match idRef="Keyword_italy_drivers_license_number" />
        </Any>
    </Pattern>
</Entity>
```

### <a name="keywords"></a>Palavras-chave

#### <a name="keyworditalydriverslicensenumber"></a>Keyword_italy_drivers_license_number

- numero di patente di guida
 
- patente di guida
 
   
## <a name="japan-bank-account-number"></a>Número de conta bancária do Japão

### <a name="format"></a>Formato

Sete ou oito dígitos

### <a name="pattern"></a>Padrão

Número da Conta Bancária:
- Sete ou oito dígitos
- Código da agência de conta bancária:
- Quatro dígitos 
- Um espaço ou um traço (opcional) 
- Três dígitos

Soma de verificação

Não

### <a name="definition"></a>Definição

Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:
- A função Func_jp_bank_account localiza conteúdo que corresponde ao padrão.
- Uma palavra-chave de Keyword_jp_bank_account for encontrada.
- Uma das seguintes opções for verdadeira:
- A função Func_jp_bank_account_branch_code localiza conteúdo que corresponde ao padrão.
- Uma palavra-chave de Keyword_jp_bank_branch_code for encontrada.

Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:
- A função Func_jp_bank_account localiza conteúdo que corresponde ao padrão.
- Uma palavra-chave de Keyword_jp_bank_account for encontrada.

```
<!-- Japan Bank Account Number -->
<Entity id="d354f95b-96ee-4b80-80bc-4377312b55bc" patternsProximity="300" recommendedConfidence="75">
  <Version minEngineVersion="15.01.0131.000">
    <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_jp_bank_account" />
          <Match idRef="Keyword_jp_bank_account" />
          <Any minMatches="1">
            <Match idRef="Func_jp_bank_account_branch_code" />
            <Match idRef="Keyword_jp_bank_branch_code" />
          </Any>
      </Pattern>
  </Version>    
     <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_jp_bank_account" />
        <Match idRef="Keyword_jp_bank_account" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a>Palavras-chave

#### <a name="keywordjpbankaccount"></a>Keyword_jp_bank_account

- Checking Account Number
 
- Checking Account
 
- Checking Account #
 
- Checking Acct Number
 
- Checking Acct #
 
- Checking Acct No.
 
- Checking Account No.
 
- Bank Account Number
 
- Bank Account
 
- Bank Account #
 
- Bank Acct Number
 
- Bank Acct #
 
- Bank Acct No.
 
- Bank Account No.
 
- Savings Account Number
 
- Conta de economia 
- Savings Account #
 
- Savings Acct Number
 
- Savings Acct #
 
- Savings Acct No.
 
- Savings Account No.
 
- Debit Account Number
 
- Debit Account
 
- Debit Account #
 
- Debit Acct Number
 
- Debit Acct #
 
- Debit Acct No.
 
- Debit Account No.
 
- 口座番号を当座預金口座の確認
 
- ＃アカウントの確認、勘定番号の確認
 
- ＃勘定の確認
 
- 勘定番号の確認
 
- 口座番号の確認
 
- 銀行口座番号 
- 銀行口座 
- 銀行口座＃
 
- 銀行の勘定番号
 
- 銀行のacct＃
 
- 銀行の勘定いいえ
 
- 銀行口座番号
- 
普通預金口座番号
 
- 預金口座
 
- 貯蓄口座＃
 
- 貯蓄勘定の数
 
- 貯蓄勘定＃
 
- 貯蓄勘定番号
 
- 普通預金口座番号
 
- 引き落とし口座番号
 
- 口座番号 
- 口座番号＃
 
- デビットのacct番号
 
- デビット勘定＃
 
- デビットACCTの番号
 
- デビット口座番号
 

#### <a name="keywordjpbankbranchcode"></a>Keyword_jp_bank_branch_code

Otemachi

## <a name="japan-drivers-license-number"></a>Número de carteira de motorista do Japão

### <a name="format"></a>Formato

12 dígitos

### <a name="pattern"></a>Padrão

12 dígitos consecutivos

### <a name="checksum"></a>Soma de verificação

Não

### <a name="definition"></a>Definição

Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:
- A função Func_jp_drivers_license_number localiza conteúdo que corresponde ao padrão.
- Uma palavra-chave de Keyword_jp_drivers_license_number for encontrada.

```
<!-- Japan Driver's License Number -->
<Entity id="c6011143-d087-451c-8313-7f6d4aed2270" patternsProximity="300" recommendedConfidence="75">
    <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_jp_drivers_license_number" />
        <Match idRef ="Keyword_jp_drivers_license_number" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a>Palavras-chave

#### <a name="keywordjpdriverslicensenumber"></a>Keyword_jp_drivers_license_number

- dl#
 
- DL # 
- DLs # 
- DLS # 
- licença de driver 
- licenças de driver 
- carteira de motorista 
- de motorista carteira 
- licenças de drivers 
- licenças de motorista 
- driving licence
 
- lic # 
- LIC # 
- lics#
 
- id de estado 
- state identification
 
- state identification number
 
- 低所得国＃
 
- 免許証
 
- 状態ID
- 
状態の識別
 
- 状態の識別番号
 
- 運転免許
 
- 運転免許証
 
- 運転免許証番号
 
   
## <a name="japan-passport-number"></a>Número de passaporte do Japão

### <a name="format"></a>Formato

Duas letras seguidas por sete dígitos

### <a name="pattern"></a>Padrão

Duas letras (não diferencia maiúsculas de minúsculas) seguidas de sete dígitos

### <a name="checksum"></a>Soma de verificação

Não

### <a name="definition"></a>Definição

Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:
- A função Func_jp_passport localiza conteúdo que corresponde ao padrão.
- Uma palavra-chave de Keyword_jp_passport for encontrada.

```
<!-- Japan Passport Number -->
<Entity id="75177310-1a09-4613-bf6d-833aae3743f8" patternsProximity="300" recommendedConfidence="75">
    <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_jp_passport" />
        <Match idRef="Keyword_jp_passport" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a>Palavras-chave

#### <a name="keywordjppassport"></a>Keyword_jp_passport

- パスポート
 
- パスポート番号
 
- パスポートのNum
 
- パスポート ＃
 
   
## <a name="japan-resident-registration-number"></a>Número de registro de residente do Japão

### <a name="format"></a>Formato

11 dígitos

### <a name="pattern"></a>Padrão

11 dígitos consecutivos

### <a name="checksum"></a>Soma de verificação

Não

### <a name="definition"></a>Definição

Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:
- A função Func_jp_resident_registration_number localiza conteúdo que corresponde ao padrão.
- Uma palavra-chave de Keyword_jp_resident_registration_number for encontrada.

```
<!-- Japan Resident Registration Number -->
<Entity id="01c1209b-6389-4faf-a5f8-3f7e13899652" patternsProximity="300" recommendedConfidence="75">
    <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_jp_resident_registration_number" />
        <Match idRef ="Keyword_jp_resident_registration_number" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a>Palavras-chave

#### <a name="keywordjpresidentregistrationnumber"></a>Keyword_jp_resident_registration_number

- Resident Registration Number
- Resident Register Number
 
- Residents Basic Registry Number
 
- Resident Registration No.
 
- Resident Register No.
 
- Residents Basic Registry No.
 
- Basic Resident Register No.
 
- 住民登録番号、登録番号をレジデント
 
- 住民基本登録番号、登録番号
 
- 住民基本レジストリ番号を常駐
 
- 登録番号を常駐住民基本台帳登録番号
 

   
## <a name="japan-social-insurance-number-sin"></a>Número de seguro social do Japão (SIN)

### <a name="format"></a>Formato

7 a 12 dígitos

### <a name="pattern"></a>Padrão

7 a 12 dígitos:
- Quatro dígitos 
- Um hífen (opcional) 
- Seis dígitos ou
- 7 a 12 dígitos consecutivos

### <a name="checksum"></a>Soma de verificação

Não

### <a name="definition"></a>Definição

Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:
- A função Func_jp_sin localiza conteúdo que corresponde ao padrão.
- Uma palavra-chave de Keyword_jp_sin for encontrada.

Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:
- A função Func_jp_sin_pre_1997 localiza conteúdo que corresponde ao padrão.
- Uma palavra-chave de Keyword_jp_sin for encontrada.

```
<!-- Japan Social Insurance Number -->
<Entity id="c840e719-0896-45bb-84fd-1ed5c95e45ff" patternsProximity="300" recommendedConfidence="75">
    <Pattern confidenceLevel="85">
        <IdMatch idRef="Func_jp_sin" />
        <Match idRef="Keyword_jp_sin" />
    </Pattern>
    <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_jp_sin_pre_1997" />
        <Match idRef="Keyword_jp_sin" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a>Palavras-chave

#### <a name="keywordjpsin"></a>Keyword_jp_sin

- Social Insurance No.
 
- Social Insurance Num
 
- Social Insurance Number
 
- 社会保険のテンキー
 
- 社会保険番号
 
   
## <a name="malaysia-id-card-number"></a>Número do Cartão de Identificação da Malásia

### <a name="format"></a>Formato

12 dígitos contendo hifens opcionais

### <a name="pattern"></a>Padrão

12 dígitos:
- Seis dígitos no formato AAMMDD que são a data de nascimento 
- Um traço (opcional) 
- Código do local de nascimento de duas letras  
- Um traço (opcional) 
- Três dígitos aleatórios  
- Código de sexo de um dígito

### <a name="checksum"></a>Soma de verificação

Não

### <a name="definition"></a>Definição

Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:
- A expressão regular Regex_malaysia_id_card_number encontra o conteúdo que corresponde ao padrão.
- Uma palavra-chave de Keyword_malaysia_id_card_number é encontrada.

```
<!-- Malaysia ID Card Number -->
</Entity>
      <Entity id="7f0e921c-9677-435b-aba2-bb8f1013c749" patternsProximity="300" recommendedConfidence="85">
        <Pattern confidenceLevel="85">
            <IdMatch idRef="Regex_malaysia_id_card_number" />
            <Match idRef="Keyword_malaysia_id_card_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Palavras-chave
   
#### <a name="keywordmalaysiaidcardnumber"></a>Keyword_malaysia_id_card_number

- MyKad 
- Cartão de Identidade 
- Cartão de identificação 
- Cartão de identificação 
- Cartão do Aplicativo Digital
 
- Kad Akuan Diri
 
- Kad Aplikasi Digital
 
   
## <a name="netherlands-citizens-service-bsn-number"></a>Número do Serviço do Cidadão (BSN) da Holland

### <a name="format"></a>Formato

8 a 9 dígitos contendo espaços opcionais

### <a name="pattern"></a>Padrão

8 a 9 dígitos.
- Três dígitos 
- Um espaço (opcional) 
- Três dígitos 
- Um espaço (opcional) 
- 2 a 3 dígitos

### <a name="checksum"></a>Soma de verificação

Sim

### <a name="definition"></a>Definição

Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:
- A função Func_netherlands_bsn encontra o conteúdo que corresponde ao padrão.
- Uma palavra-chave de Keyword_netherlands_bsn é encontrada.
- A função Func_eu_date2 encontra uma data no formato de data à direita.
- A soma de verificação passa.

```
<!-- Netherlands Citizen's Service (BSN) Number -->
<Entity id="c5f54253-ef7e-44f6-a578-440ed67e946d" patternsProximity="300" recommendedConfidence="85">
  <Pattern confidenceLevel="85">
       <IdMatch idRef="Func_netherlands_bsn" /> 
       <Match idRef="Keyword_netherlands_bsn" /> 
       <Match idRef="Func_eu_date2" /> 
  </Pattern>
</Entity>
```

### <a name="keywords"></a>Palavras-chave

#### <a name="keywordnetherlandsbsn"></a>Keyword_netherlands_bsn

- Número do serviço do cidadão
 
- BSN

 
- Burgerservicenummer
 
- Sofinummer
 
- Persoonsgebonden nummer
 
- Persoonsnummer
    

   
## <a name="new-zealand-ministry-of-health-number"></a>Número do Ministério da Saúde da Nova Zelândia

### <a name="format"></a>Formato

Três letras, um espaço (opcional) e quatro dígitos

### <a name="pattern"></a>Padrão

Três letras (não diferenciar maiusculas de minúsculas) um quatro dígitos (opcional) espaço

### <a name="checksum"></a>Soma de verificação

Sim

### <a name="definition"></a>Definição

Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:
- A função Func_new_zealand_ministry_of_health_number localiza conteúdo que corresponde ao padrão.
- Uma palavra-chave de Keyword_nz_terms for encontrada.
- A soma de verificação passa.

```
<!-- New Zealand Health Number -->
<Entity id="2b71c1c8-d14e-4430-82dc-fd1ed6bf05c7" patternsProximity="300" recommendedConfidence="85">
    <Pattern confidenceLevel="85">
        <IdMatch idRef="Func_new_zealand_ministry_of_health_number" />
        <Any minMatches="1">
          <Match idRef="Keyword_nz_terms" />
        </Any>
    </Pattern>
</Entity>
```

Palavras-chave

Keyword_nz_terms

- NHI
 
- Nova Zelândia 
- Integridade 
- tratamento
 
   
## <a name="norway-identification-number"></a>Número de Identificação da Noruega

### <a name="format"></a>Formato

11 dígitos

### <a name="pattern"></a>Padrão

11 dígitos:
- Seis dígitos no formato DDMMAA que são a data de nascimento 
- Número individual de três dígitos  
- Dois dígitos de verificação

### <a name="checksum"></a>Soma de verificação

Sim

### <a name="definition"></a>Definição

Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:
- A função Func_norway_id_number encontra o conteúdo que corresponde ao padrão.
- Uma palavra-chave de Keyword_norway_id_number é encontrada.
- A soma de verificação passa.
- Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:
- A função Func_norway_id_numbe encontra o conteúdo que corresponde ao padrão.
- A soma de verificação passa.

```
<!-- Norway Identification Number -->
<Entity id="d4c8a798-e9f2-4bd3-9652-500d24080fc3" recommendedConfidence="85" patternsProximity="300">
  <Pattern confidenceLevel="85">
     <IdMatch idRef="Func_norway_id_number"/>
     <Match idRef="Keyword_norway_id_number"/>
  </Pattern>
  <Pattern confidenceLevel="75">
     <IdMatch idRef="Func_norway_id_number"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a>Palavras-chave

#### <a name="keywordnorwayidnumber"></a>Keyword_norway_id_number

- Número de identificação pessoal
- Número de Identificação Norueguês
- Número de Identificação
- Identificação 
- Personnummer
- Fødselsnummer

   
## <a name="philippines-unified-multi-purpose-id-number"></a>Número de Identificação Multiuso Unificada das Filipinas

### <a name="format"></a>Formato

12 dígitos separados por hifens

### <a name="pattern"></a>Padrão

12 dígitos:
- Quatro dígitos 
- Um hífen 
- Sete dígitos  
- Um hífen 
- Um dígito

### <a name="checksum"></a>Soma de verificação

Não

### <a name="definition"></a>Definição

Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:
- A expressão regular Regex_philippines_unified_id encontra o conteúdo que corresponde ao padrão.
- Uma palavra-chave de Keyword_philippines_id é encontrada.

```
<!-- Philippines Unified Multi-Purpose ID number -->
<Entity id="019b39dd-8c25-4765-91a3-d9c6baf3c3b3" recommendedConfidence="75" patternsProximity="300">
  <Pattern confidenceLevel="75">
     <IdMatch idRef="Regex_philippines_unified_id"/>
     <Match idRef="Keyword_philippines_id"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a>Palavras-chave
   
#### <a name="keywordphilippinesid"></a>Keyword_philippines_id

- Identificação Multiuso Unificada
 
- IMU
 
- Cartão de Identidade 
- Pinag-isang Multi-Layunin ID
   
## <a name="poland-identity-card"></a>Cartão de Identificação da Polônia

### <a name="format"></a>Formato

Três letras e seis dígitos

### <a name="pattern"></a>Padrão

Três letras (não diferenciam maiúsculas de minúsculas) seguidas de seis dígitos

### <a name="checksum"></a>Soma de verificação

Sim

### <a name="definition"></a>Definição

Uma política de DLP é 75% confiante de que detectou esse tipo de informações confidenciais if, dentro de uma proximidade de 300 caracteres: A função Func_polish_national_id encontra o conteúdo que corresponde ao padrão. Uma palavra-chave de Keyword_polish_national_id_passport_number é encontrada. A soma de verificação passa.

```
<!-- Poland Identity Card-->
<Entity id="25E64989-ED5D-40CA-A939-6C14183BB7BF" patternsProximity="300" recommendedConfidence="85">
      <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_polish_national_id" />
          <Match idRef="Keyword_polish_national_id_passport_number" />
      </Pattern>
</Entity>
```

### <a name="keywords"></a>Palavras-chave

#### <a name="keywordpolishnationalidpassportnumber"></a>Keyword_polish_national_id_passport_number

- Nazwa i nr dowodu tożsamości
 
- Dowód Tożsamości
 
- dow. os.
 

   
## <a name="poland-national-id-pesel"></a>ID nacional da Polônia (PESEL)

### <a name="format"></a>Formato

11 dígitos

### <a name="pattern"></a>Padrão

11 dígitos consecutivos

### <a name="checksum"></a>Soma de verificação

Sim

### <a name="definition"></a>Definição

Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:
- A função Func_pesel_identification_number localiza conteúdo que corresponde ao padrão.
- Uma palavra-chave de Keyword_pesel_identification_number for encontrada.
- A soma de verificação passa.

```
<!-- Poland National ID (PESEL) -->      
<Entity id="E3AAF206-4297-412F-9E06-BA8487E22456" patternsProximity="300" recommendedConfidence="85">
      <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_pesel_identification_number" />
          <Match idRef="Keyword_pesel_identification_number" />
      </Pattern>
</Entity>
```

### <a name="keywords"></a>Palavras-chave

#### <a name="keywordpeselidentificationnumber"></a>Keyword_pesel_identification_number

- Nr PESEL
- PESEL   

   
## <a name="poland-passport"></a>Passaporte da Polônia

### <a name="format"></a>Formato

Duas letras e sete dígitos

### <a name="pattern"></a>Padrão

Duas letras (não diferencia maiúsculas de minúsculas) seguidas de sete dígitos

### <a name="checksum"></a>Soma de verificação

Sim

### <a name="definition"></a>Definição

Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:
- A função Func_polish_passport_number localiza conteúdo que corresponde ao padrão.
- Uma palavra-chave de Keyword_polish_national_id_passport_number for encontrada.
- A soma de verificação passa.

```
<!-- Poland Passport Number -->
<Entity id="03937FB5-D2B6-4487-B61F-0F8BFF7C3517" patternsProximity="300" recommendedConfidence="85">
      <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_polish_passport_number" />
          <Match idRef="Keyword_polish_national_id_passport_number" />
      </Pattern>
</Entity>
</Version>
```

### <a name="keywords"></a>Palavras-chave

#### <a name="keywordpolishnationalidpassportnumber"></a>Keyword_polish_national_id_passport_number

- Nazwa i nr dowodu tożsamości
 
- Dowód Tożsamości
 
- dow. os.
 

   
## <a name="portugal-citizen-card-number"></a>Número do Cartão de Cidadão de Portugal

### <a name="format"></a>Formato

Oito dígitos

### <a name="pattern"></a>Padrão

Oito dígitos

### <a name="checksum"></a>Soma de verificação

Não

### <a name="definition"></a>Definição

Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:
- A expressão regular Regex_portugal_citizen_card encontra o conteúdo que corresponde ao padrão.
- Uma palavra-chave de Keyword_portugal_citizen_card é encontrada.

```
<!-- Portugal Citizen Card Number -->
<Entity id="91a7ece2-add4-4986-9a15-c84544d81ecd" recommendedConfidence="85" patternsProximity="300">
  <Pattern confidenceLevel="85">
     <IdMatch idRef="Regex_portugal_citizen_card"/>
     <Match idRef="Keyword_portugal_citizen_card"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a>Palavras-chave

#### <a name="keywordportugalcitizencard"></a>Keyword_portugal_citizen_card

- Cartão de Cidadão
- Cartão de Identidade Nacional
- CC
- Cartão de Cidadão
- Bilhete de Identidade
   
## <a name="saudi-arabia-national-id"></a>ID nacional da Arábia Saudita

### <a name="format"></a>Formato

10 dígitos

### <a name="pattern"></a>Padrão

10 dígitos consecutivos

### <a name="checksum"></a>Soma de verificação

Não

### <a name="definition"></a>Definição

Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:
- A expressão regular Regex_saudi_arabia_national_id localiza o conteúdo que corresponde ao padrão.
- Uma palavra-chave de Keyword_saudi_arabia_national_id for encontrada.

```
<!-- Saudi Arabia National ID -->
<Entity id="8c5a0ba8-404a-41a3-8871-746aa21ee6c0" patternsProximity="300" recommendedConfidence="75">
    <Pattern confidenceLevel="75">
        <IdMatch idRef="Regex_saudi_arabia_national_id" />
        <Any minMatches="1">
          <Match idRef="Keyword_saudi_arabia_national_id" />
        </Any>
    </Pattern>
</Entity>
```

### <a name="keywords"></a>Palavras-chave

#### <a name="keywordsaudiarabianationalid"></a>Keyword_saudi_arabia_national_id

- Identification Card
 
- I card number
 
- número de identificação 
- الوطنية الهوية بطاقة رقم
 

   
## <a name="singapore-national-registration-identity-card-nric-number"></a>Número do Cartão de Identidade do Registro Nacional (NRIC) de Cingapura

### <a name="format"></a>Formato

Nove letras e dígitos

### <a name="pattern"></a>Padrão

- Nove letras e dígitos:
- A letra "F", "G", "S" ou "T" (não diferenciam maiúsculas de minúsculas)  
- Sete dígitos  
- Um dígito de verificação alfabético

### <a name="checksum"></a>Soma de verificação

Sim

### <a name="definition"></a>Definição

Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:
- A expressão regular Regex_singapore_nric encontra o conteúdo que corresponde ao padrão.
- Uma palavra-chave de Keyword_singapore_nric é encontrada.
- A soma de verificação passa.

Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:
- A expressão regular Regex_singapore_nric encontra o conteúdo que corresponde ao padrão.
- A soma de verificação passa.

```
<!-- Singapore National Registration Identity Card (NRIC) Number -->
<Entity id="cead390a-dd83-4856-9751-fb6dc98c34da" recommendedConfidence="75" patternsProximity="300">
  <Pattern confidenceLevel="85">
     <IdMatch idRef="Regex_singapore_nric"/>
     <Match idRef="Keyword_singapore_nric"/>
  </Pattern>
  <Pattern confidenceLevel="75">
     <IdMatch idRef="Regex_singapore_nric"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a>Palavras-chave
   
#### <a name="keywordsingaporenric"></a>Keyword_singapore_nric

- Número do Cartão de Identidade do Registro Nacional
 
- Número do Cartão de Identidade
 
- NRIC
 
- IC
 
- Número de Identificação Estrangeira
 
- FIN
 
- 身份证  
- 身份證
 
   
## <a name="south-africa-identification-number"></a>Número de Identificação da África do Sul

### <a name="format"></a>Formato

13 dígitos que podem conter espaços

### <a name="pattern"></a>Padrão

13 dígitos:
- Seis dígitos no formato AAMMDD que são a data de nascimento 
- Quatro dígitos 
- Indicador de cidadania de um dígito  
- O dígito "8" ou "9"  
- Um dígito que é um dígito de soma de verificação

### <a name="checksum"></a>Soma de verificação

Sim

### <a name="definition"></a>Definição

Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:
- A função Func_south_africa_identification_number encontra o conteúdo que corresponde ao padrão.
- Uma palavra-chave de Keyword_south_africa_identification_number é encontrada.
- A soma de verificação passa.

```
<!-- South Africa Identification Number -->
<Entity id="e2adf7cb-8ea6-4048-a2ed-d89eb65f2780" recommendedConfidence="85" patternsProximity="300">
  <Pattern confidenceLevel="85">
     <IdMatch idRef="Func_south_africa_identification_number"/>
     <Match idRef="Keyword_south_africa_identification_number"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a>Palavras-chave
   
#### <a name="keywordsouthafricaidentificationnumber"></a>Keyword_south_africa_identification_number

- Cartão de identidade
- ID
- Identificação  
   
## <a name="south-korea-resident-registration-number"></a>Número do Registro de Residentes da Coreia do Sul

### <a name="format"></a>Formato

13 dígitos que contém um hifen

### <a name="pattern"></a>Padrão

13 dígitos:
- Seis dígitos no formato AAMMDD que são a data de nascimento 
- Um hífen 
- Um dígito determinado pelo século e pelo sexo  
- Código da região de nascimento de quatro dígitos  
- Um dígito usado para diferenciar as pessoas para as quais os números anteriores são idênticos  
- Um dígito de verificação.

### <a name="checksum"></a>Soma de verificação

Sim

### <a name="definition"></a>Definição

Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:
- A função Func_south_korea_resident_number encontra o conteúdo que corresponde ao padrão.
- Uma palavra-chave de Keyword_south_korea_resident_number é encontrada.
- A soma de verificação passa.

Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:
- A função Func_south_korea_resident_number encontra o conteúdo que corresponde ao padrão.
- A soma de verificação passa.

```
<!-- South Korea Resident Registration Number -->
<Entity id="5b802e18-ba80-44c4-bc83-bf2ad36ae36a" recommendedConfidence="85" patternsProximity="300">
  <Pattern confidenceLevel="85">
     <IdMatch idRef="Func_south_korea_resident_number"/>
     <Match idRef="Keyword_south_korea_resident_number"/>
  </Pattern>
  <Pattern confidenceLevel="75">
     <IdMatch idRef="Func_south_korea_resident_number"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a>Palavras-chave
   
#### <a name="keywordsouthkorearesidentnumber"></a>Keyword_south_korea_resident_number

- Cartão de identidade nacional
 
- Número de Registro do Cidadão
 
- Jumin deungnok beonho
 
- RRN
 
- 주민등록번호
   
## <a name="spain-social-security-number-ssn"></a>Número de seguridade social da Espanha (SSN)

### <a name="format"></a>Formato

11 a 12 dígitos

### <a name="pattern"></a>Padrão

12 de 11 dígitos:
- Dois dígitos 
- Uma barra (opcional) 
- 7 a 8 dígitos 
- Uma barra (opcional) 
- Dois dígitos

### <a name="checksum"></a>Soma de verificação

Sim

### <a name="definition"></a>Definição

Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:
- A função Func_spanish_social_security_number localiza conteúdo que corresponde ao padrão.
- A soma de verificação passa.

```
<!-- Spain SSN -->
<Entity id="5df987c0-8eae-4bce-ace7-b316347f3070" patternsProximity="300" recommendedConfidence="85">
    <Pattern confidenceLevel="85">
        <IdMatch idRef="Func_spanish_social_security_number" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a>Palavras-chave

Nenhum
   
## <a name="sweden-national-id"></a>ID nacional da Suécia

### <a name="format"></a>Formato

10 ou 12 dígitos e um delimitador opcional

### <a name="pattern"></a>Padrão

10 ou 12 dígitos e um delimitador opcional:
- 2 a 4 dígitos (opcionais) 
- Seis dígitos no formato de data AAMMDD 
- Um delimitador de "-" ou "+" (opcional), mais
- Quatro dígitos

### <a name="checksum"></a>Soma de verificação

Sim

### <a name="definition"></a>Definição

Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:
- A função Func_swedish_national_identifier localiza conteúdo que corresponde ao padrão.
- A soma de verificação passa.

```
<!-- Sweden National ID -->
<Entity id="f69aaf40-79be-4fac-8f05-fd1910d272c8" patternsProximity="300" recommendedConfidence="85">
    <Pattern confidenceLevel="85">
        <IdMatch idRef="Func_swedish_national_identifier" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a>Palavras-chave

Não
   
## <a name="sweden-passport-number"></a>Número de passaporte da Suécia

### <a name="format"></a>Formato

Oito dígitos

### <a name="pattern"></a>Padrão

Oito dígitos consecutivos

### <a name="checksum"></a>Soma de verificação

Não

### <a name="definition"></a>Definição

Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:
- A expressão regular Regex_sweden_passport_number localiza o conteúdo que corresponde ao padrão.
- Uma das seguintes opções for verdadeira:
    - Uma palavra-chave de Keyword_passport for encontrada.
    - Uma palavra-chave de Keyword_sweden_passport for encontrada.

```
<!-- Sweden Passport Number -->
<Entity id="ba4e7456-55a9-4d89-9140-c33673553526" patternsProximity="300" recommendedConfidence="75">
    <Pattern confidenceLevel="75">
        <IdMatch idRef="Regex_sweden_passport_number" />
        <Any minMatches="1">
          <Match idRef="Keyword_passport" />
          <Match idRef="Keyword_sweden_passport" />
        </Any>
    </Pattern>
</Entity>
```

### <a name="keywords"></a>Palavras-chave
   
#### <a name="keywordswedenpassport"></a>Keyword_sweden_passport

- visa requirements
 
- Alien Registration Card
 
- Schengen visas
 
- Schengen visa
 
- Visa Processing
 
- Visa Type
 
- Single Entry
 
- Multiple Entry
 
- G3 Processing Fees

 

#### <a name="keywordpassport"></a>Keyword_passport

- Passport Number 
- 
Passport No 
- Passport #
 
- Passport#
 
- PassportID 
- Passportno
 
- passportnumber
 
- パスポート 
- パスポート番号
 
- パスポートのNum
 
- パスポート＃
 
- Numéro de passeport 
- 
Passeport n ° 
- Passeport Non
 
- Passeport #
 
- Passeport#
 
- PasseportNon 
- Passeportn °
 
   
## <a name="swift-code"></a>Código SWIFT

### <a name="format"></a>Formato

Quatro letras seguidas por 5 a 31 letras ou dígitos

### <a name="pattern"></a>Padrão

Quatro letras seguidas por 5 a 31 letras ou dígitos:
- Código bancário de quatro letras (não diferencia maiúsculas de minúsculas) 
- Um espaço opcional 
- 4 a 28 letras ou dígitos (o número de conta bancária básica (BBAN)) 
- Um espaço opcional 
- 1 a 3 letras ou dígitos (restante do BBAN)

### <a name="checksum"></a>Soma de verificação

Não

### <a name="definition"></a>Definição

Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:
- A expressão regular Regex_swift localiza o conteúdo que corresponde ao padrão.
- Uma palavra-chave de Keyword_swift for encontrada.

```
<Entity id="cb2ab58c-9cb8-4c81-baf8-a4e106791df4" patternsProximity="300" recommendedConfidence="75">
<Pattern confidenceLevel="75">
        <IdMatch idRef="Regex_swift" />
        <Match idRef="Keyword_swift" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a>Palavras-chave
   
#### <a name="keywordswift"></a>Keyword_swift

- international organization for standardization 9362
 
- iso 9362
 
- iso9362 
- SWIFT\# 
- swiftcode
 
- swiftnumber
 
- swiftroutingnumber
 
- swift code
 
- swift number #
 
- swift routing number
 
- bic number
 
- bic code
 
- BIC\# 
- BIC\# 
- bank identifier code
 
- 標準化9362 
- 迅速＃
 
- SWIFTコード
 
- SWIFT番号
 
- 迅速なルーティング番号
 
- BIC番号
 
- BICコード
 
- 銀行識別コードのための国際組織
 
- Organisation internationale de normalisation 9362
 
- rapide\# 
- code SWIFT
 
- le numéro de swift
 
- swift numéro d'acheminement
 
- le numéro BIC
 
- \#BIC 
- code identificateur de banque
 
   
## <a name="taiwan-national-id"></a>ID nacional de Taiwan

### <a name="format"></a>Formato

Uma letra (em inglês) seguida de nove dígitos

### <a name="pattern"></a>Padrão

Uma letra (em inglês) seguida de nove dígitos:
- Uma letra (em inglês, não diferencia maiúscula de minúscula) 
- O dígito "1" ou "2" 
- Oito dígitos

### <a name="checksum"></a>Soma de verificação

Sim

### <a name="definition"></a>Definição

Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:
- A função Func_taiwanese_national_id localiza conteúdo que corresponde ao padrão.
- Uma palavra-chave de Keyword_taiwanese_national_id for encontrada.
- A soma de verificação passa.

```
<!-- Taiwanese National ID -->
<Entity id="4C7BFC34-8DD1-421D-8FB7-6C6182C2AF03" patternsProximity="300" recommendedConfidence="85">
      <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_taiwanese_national_id" />
          <Match idRef="Keyword_taiwanese_national_id" />
      </Pattern>
</Entity>
```

### <a name="keywords"></a>Palavras-chave

#### <a name="keywordtaiwanesenationalid"></a>Keyword_taiwanese_national_id

- 身份證字號
 
- 身份證
 
- 身份證號碼
 
- 身份證號
 
- 身分證字號
 
- 身分證  
- 身分證號碼
 
- 身份證號
 
- 身分證統一編號
 
- 國民身分證統一編號
 
- 簽名
 
- 蓋章
 
- 簽名或蓋章

 
- 簽章   
   
## <a name="taiwan-passport-number"></a>	Número de passaporte de Taiwan

### <a name="format"></a>Formato

- Número de passaporte biométrica: nove dígitos
- Número de passaporte Non-biométrica: nove dígitos

### <a name="pattern"></a>Padrão
Número de passaporte biométrica:
- O dígito "3"  
- Oito dígitos

Número de passaporte Non-biométrica:
- Nove dígitos

### <a name="checksum"></a>Soma de verificação

Não

### <a name="definition"></a>Definição

Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:
- A expressão regular Regex_taiwan_passport encontra o conteúdo que corresponde ao padrão.
- Uma palavra-chave de Keyword_taiwan_passport é encontrada.

```
<!-- Taiwan Passport Number -->
<Entity id="e7251cb4-4c2c-41df-963e-924eb3dae04a" recommendedConfidence="75" patternsProximity="300">
  <Pattern confidenceLevel="75">
     <IdMatch idRef="Regex_taiwan_passport"/>
     <Match idRef="Keyword_taiwan_passport"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a>Palavras-chave

#### <a name="keywordtaiwanpassport"></a>Keyword_taiwan_passport

- Número de passaporte ROC
 
- Número de passaporte 
- Passport nenhum 
- Núm de Passaporte
 
- Passport #
 
- 护照
 
- 中華民國護照
 
- Zhōnghuá Mínguó hùzhào
   
## <a name="taiwan-resident-certificate-arctarc-number"></a>Número do Certificado de residente de Taiwan (ARC/TARC)

### <a name="format"></a>Formato

10 letras e dígitos

### <a name="pattern"></a>Padrão

10 letras e dígitos:
- Duas letras (não diferenciam maiúsculas de minúsculas) 
- Oito dígitos

### <a name="checksum"></a>Soma de verificação

Não

### <a name="definition"></a>Definição

Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:
- A expressão regular Regex_taiwan_resident_certificate encontra o conteúdo que corresponde ao padrão.
- Uma palavra-chave de Keyword_taiwan_resident_certificate é encontrada.

```
<!-- Taiwan Resident Certificate (ARC/TARC) -->
<Entity id="48269fec-05ea-46ea-b326-f5623a58c6e9" recommendedConfidence="75" patternsProximity="300">
  <Pattern confidenceLevel="75">
     <IdMatch idRef="Regex_taiwan_resident_certificate"/>
     <Match idRef="Keyword_taiwan_resident_certificate"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a>Palavras-chave

#### <a name="keywordtaiwanresidentcertificate"></a>Keyword_taiwan_resident_certificate

- Certificado de Residente
 
- Cert residente 
- Cert. de Residente
 
- Cartão de identificação 
- Certificado de Residente Alien
 
- ARC
 
- Certificado de Residente da Área de Taiwan
 
- TARC
 
- 居留證
 
- 外僑居留證
 
- 台灣地區居留證
 
   
## <a name="uk-drivers-license-number"></a>Número de carteira de motorista do Reino Unido

### <a name="format"></a>Formato

Combinação de 18 letras e dígitos no formato especificado

### <a name="pattern"></a>Padrão

18 letras e dígitos:
- Cinco letras (não diferenciam maiúsculas de minúsculas) ou o dígito "9" em vez de uma letra 
- Um dígito 
- Cinco dígitos no formato de data DDMMA para data de nascimento 
- Duas letras (não diferenciam maiúsculas de minúsculas) ou o dígito "9" em vez de uma letra 
- Cinco dígitos

### <a name="checksum"></a>Soma de verificação

Sim

### <a name="definition"></a>Definição

Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:
- A função Func_uk_drivers_license localiza conteúdo que corresponde ao padrão.
- Uma palavra-chave de Keyword_uk_drivers_license for encontrada.
- A soma de verificação passa.

```
<!-- U.K. Driver's License Number -->
<Entity id="f93de4be-d94c-40df-a8be-461738047551" patternsProximity="300" recommendedConfidence="75">
    <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_uk_drivers_license" />
        <Match idRef="Keyword_uk_drivers_license" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a>Palavras-chave

#### <a name="keywordukdriverslicense"></a>Keyword_uk_drivers_license

- DVLA
 
- light vans
 
- quadbikes
 
- motor cars
 
- 125cc 
- sidecar
 
- tricycles
 
- motorcycles
 
- photocard licence
 
- learner drivers
 
- licence holder
 
- licence holders
 
- driving licences
 
- driving licence
 
- dual control car
 
   
## <a name="uk-electoral-roll-number"></a>Número de Título de Eleitor do Reino Unido

### <a name="format"></a>Formato

Duas letras seguidas por 1 a 4 dígitos

### <a name="pattern"></a>Padrão

Duas letras (não diferencia maiúsculas de minúsculas) seguidas de 1 a 4 anos

### <a name="checksum"></a>Soma de verificação

Não

### <a name="definition"></a>Definição

Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:
- A expressão regular Regex_uk_electoral localiza o conteúdo que corresponde ao padrão.
- Uma palavra-chave de Keyword_uk_electoral for encontrada.

```
<!-- U.K. Electoral Number -->
<Entity id="a3eea206-dc0c-4f06-9e22-aa1be3059963" patternsProximity="300" recommendedConfidence="75">
    <Pattern confidenceLevel="75">
        <IdMatch idRef="Regex_uk_electoral" />
        <Any minMatches="1">
          <Match idRef="Keyword_uk_electoral" />
        </Any>
    </Pattern>
</Entity>
```

### <a name="keywords"></a>Palavras-chave

#### <a name="keywordukelectoral"></a>Keyword_uk_electoral

- council nomination
 
- nomination form
 
- electoral register

 
- electoral roll

   
## <a name="uk-national-health-service-number"></a>Número do serviço de saúde nacional do Reino Unido

### <a name="format"></a>Formato

10 a 17 dígitos separados por espaços

### <a name="pattern"></a>Padrão

10 a 17 dígitos:
- 3 ou 10 dígitos 
- Um espaço 
- Três dígitos 
- Um espaço 
- Quatro dígitos

### <a name="checksum"></a>Soma de verificação

Sim

### <a name="definition"></a>Definição

Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:
- A função Func_uk_nhs_number localiza conteúdo que corresponde ao padrão.
- Uma das seguintes opções for verdadeira:
    - Uma palavra-chave de Keyword_uk_nhs_number for encontrada.
    - Uma palavra-chave de Keyword_uk_nhs_number1 for encontrada.
    - Uma palavra-chave de Keyword_uk_nhs_number_dob for encontrada.
- A soma de verificação passa.

```
<!-- U.K. NHS Number -->
<Entity id="3192014e-2a16-44e9-aa69-4b20375c9a78" patternsProximity="300" recommendedConfidence="85">
    <Pattern confidenceLevel="85">
        <IdMatch idRef="Func_uk_nhs_number" />
        <Any minMatches="1">
          <Match idRef="Keyword_uk_nhs_number" />
          <Match idRef="Keyword_uk_nhs_number1" />
          <Match idRef="Keyword_uk_nhs_number_dob" />
        </Any>
    </Pattern>
</Entity>
```

### <a name="keywords"></a>Palavras-chave
   
#### <a name="keyworduknhsnumber"></a>Keyword_uk_nhs_number

- national health service
 
- nhs
 
- health services authority

 
- health authority

#### <a name="keyworduknhsnumber1"></a>Keyword_uk_nhs_number1

- patient id
 
- patient identification
 
- patient no

 
- patient number

#### <a name="keyworduknhsnumberdob"></a>Keyword_uk_nhs_number_dob

- GP 
- DOB
 
- D.O.B 
- Date of Birth
 
- Birth Date
 
   
## <a name="uk-national-insurance-number-nino"></a>Número de seguro nacional do Reino Unido (NINO)

### <a name="format"></a>Formato

7 caracteres ou 9 caracteres separados por espaços nem traços

### <a name="pattern"></a>Padrão

Dois padrões possíveis:

- Duas letras (NINOs válidos usam apenas determinados caracteres nesse prefixo, que valida a este padrão; não diferencia maiusculas de minúsculas)
- Seis dígitos
- Qualquer um dos '', 'B', 'C, ou tinha ' (como o prefixo, apenas determinados caracteres são permitidos no sufixo; não diferenciam maiusculas de minúsculas)

OU

- Duas letras
- Um espaço ou um traço
- Dois dígitos
- Um espaço ou um traço
- Dois dígitos
- Um espaço ou um traço
- Dois dígitos
- Um espaço ou um traço
- Qualquer um dos 'A', 'B', 'C, ou tinha '

### <a name="checksum"></a>Soma de verificação

Não

### <a name="definition"></a>Definição

Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:
- A função Func_uk_nino localiza conteúdo que corresponde ao padrão.
- Uma palavra-chave de Keyword_uk_nino for encontrada.

Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:
- A função Func_uk_nino localiza conteúdo que corresponde ao padrão.
- Nenhuma palavra-chave de Keyword_uk_nino for encontrada.

```
<!-- U.K. NINO -->
<Entity id="16c07343-c26f-49d2-a987-3daf717e94cc" patternsProximity="300" recommendedConfidence="75">
    <Pattern confidenceLevel="85">
        <IdMatch idRef="Func_uk_nino" />
        <Any minMatches="1">
          <Match idRef="Keyword_uk_nino" />
        </Any>
    </Pattern>    
     <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_uk_nino" />
        <Any minMatches="0" maxMatches="0">
          <Match idRef="Keyword_uk_nino" />
        </Any>
    </Pattern>
</Entity>
```

### <a name="keywords"></a>Palavras-chave

#### <a name="keyworduknino"></a>Keyword_uk_nino

- national insurance number
 
- national insurance contributions
 
- protection act
 
- insurance
 
- social security number
 
- insurance application
 
- medical application
 
- social insurance
 
- medical attention
 
- seguridade social 
- great britain
 
- insurance
    
   
## <a name="us--uk-passport-number"></a>Número de passaporte dos EUA/Reino Unido

### <a name="format"></a>Formato

Nove dígitos

### <a name="pattern"></a>Padrão

Nove dígitos consecutivos

### <a name="checksum"></a>Soma de verificação

Não

### <a name="definition"></a>Definição

Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:
- A função Func_usa_uk_passport localiza conteúdo que corresponde ao padrão.
- Uma palavra-chave de Keyword_passport for encontrada.

```
<Entity id="178ec42a-18b4-47cc-85c7-d62c92fd67f8" patternsProximity="300" recommendedConfidence="75">
    <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_usa_uk_passport" />
        <Match idRef="Keyword_passport" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a>Palavras-chave

#### <a name="keywordpassport"></a>Keyword_passport

- Passport Number 
- 
Passport No 
- Passport #
 
- Passport#
 
- PassportID 
- Passportno
 
- passportnumber
 
- パスポート 
- パスポート番号
 
- パスポートのNum
 
- パスポート＃
 
- Numéro de passeport 
- 
Passeport n ° 
- Passeport Non
 
- Passeport #
 
- Passeport#
 
- PasseportNon 
- Passeportn °
 
   
## <a name="us-bank-account-number"></a>Número de conta bancária dos EUA

### <a name="format"></a>Formato

8 a 17 dígitos

### <a name="pattern"></a>Padrão

8 a 17 dígitos consecutivos

### <a name="checksum"></a>Soma de verificação

Não

### <a name="definition"></a>Definição

Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:
- A expressão regular Regex_usa_bank_account_number localiza o conteúdo que corresponde ao padrão.
- Uma palavra-chave de Keyword_usa_Bank_Account for encontrada.

```
<!-- U.S. Bank Account Number -->
<Entity id="a2ce32a8-f935-4bb6-8e96-2a5157672e2c" patternsProximity="300" recommendedConfidence="75">
    <Pattern confidenceLevel="75">
        <IdMatch idRef="Regex_usa_bank_account_number" />
        <Match idRef="Keyword_usa_Bank_Account" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a>Palavras-chave

#### <a name="keywordusabankaccount"></a>Keyword_usa_Bank_Account

- Checking Account Number
 
- Checking Account
 
- Checking Account #
 
- Checking Acct Number
 
- Checking Acct #
 
- Checking Acct No.
 
- Checking Account No.
 
- Bank Account Number
 
- Bank Account #
 
- Bank Acct Number
 
- Bank Acct #
 
- Bank Acct No.
 
- Bank Account No.
 
- Savings Account Number
 
- Savings Account.
 
- Savings Account #
 
- Savings Acct Number
 
- Savings Acct #
 
- Savings Acct No.
 
- Savings Account No.
 
- Debit Account Number
 
- Debit Account
 
- Debit Account #
 
- Debit Acct Number
 
- Debit Acct #
 
- Debit Acct No.
 
- Debit Account No.
 
   
## <a name="us-drivers-license-number"></a>Número de carteira de motorista dos EUA

### <a name="format"></a>Formato

Depende do estado

### <a name="pattern"></a>Padrão

Depende do estado – por exemplo, Nova York:
- Nove dígitos formatado como ddd ddd ddd corresponderá.
- Nove dígitos como ddddddddd não corresponderá.

### <a name="checksum"></a>Soma de verificação

Não

### <a name="definition"></a>Definição

Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:
- A função Func_new_york_drivers_license_number localiza conteúdo que corresponde ao padrão.
- Uma palavra-chave de Keyword_[state_name]_drivers_license_name for encontrada.
- Uma palavra-chave de Keyword_us_drivers_license é encontrada.

Uma política de DLP tem 65% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:
- A função Func_new_york_drivers_license_number localiza conteúdo que corresponde ao padrão.
- Uma palavra-chave de Keyword_[state_name]_drivers_license_name for encontrada.
- Uma palavra-chave de Keyword_us_drivers_license_abbreviations for encontrada.
- Nenhuma palavra-chave de Keyword_us_drivers_license for encontrada.

```
    <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_new_york_drivers_license_number" />
        <Match idRef="Keyword_new_york_drivers_license_name" />
        <Match idRef="Keyword_us_drivers_license" />
    </Pattern>
    <Pattern confidenceLevel="65">
        <IdMatch idRef="Func_new_york_drivers_license_number" />
        <Match idRef="Keyword_new_york_drivers_license_name" />
        <Match idRef="Keyword_us_drivers_license_abbreviations" />
        <Any minMatches="0" maxMatches="0">
          <Match idRef="Keyword_us_drivers_license" />
        </Any>
    </Pattern>
```

### <a name="keywords"></a>Palavras-chave

#### <a name="keywordusdriverslicenseabbreviations"></a>Keyword_us_drivers_license_abbreviations

- DL 
- DLS 
- CDL 
- CDLS 
- ID 
- IDs 
- DL# 
- 
DLS#
 
- CDL#
 
- CDLS#
 
- ID#
- 
IDs#
 
- número de identificação 
- ID numbers
 
- LIC 
- LIC#
 

#### <a name="keywordusdriverslicense"></a>Keyword_us_drivers_license

- DriverLic 
- DriverLics 
- DriverLicense 
- DriverLicenses 
- Driver Lic 
- Driver Lics 
- Driver de licença 
- Licenças de driver 
- DriversLic 
- DriversLics 
- CarteiraDeMotorista 
- DriversLicenses 
- Drivers Lic 
- Drivers Lics 
- Carteira de motorista 
- Licenças de drivers 
- Driver'Lic 
- Driver'Lics 
- Driver'License 
- Driver'Licenses 
- Driver' Lic 
- Driver' Lics 
- Driver' licença 
- Driver' licenças
- Driver'sLic 
- Driver'sLics 
- Driver'sLicense 
- Driver'sLicenses 
- Lic do driver 
- Lics do driver 
- De motorista carteira 
- Licenças de motorista 
- identification number
 
- identification numbers
 
- identification #
 
- cartão de identificação 
- cartões de ID 
- cartão de identificação 
- cartões de identificação 
- DriverLic # 
- DriverLics # 
- DriverLicense # 
- DriverLicenses # 
- Driver Lic# 
- 
Driver Lics#
 
- Licença do driver # 
- Driver licenças # 
- DriversLic # 
- DriversLics # 
- CarteiraDeMotorista # 
- DriversLicenses # 
- Drivers Lic # 
- Drivers Lics # 
- Drivers licença # 
- Drivers licenças # 
- Driver'Lic#
 
- Driver'Lics#
 
- Driver'License#
 
- Driver'Licenses#
 
- Driver' Lic#
 
- Driver' Lics#
 
- Driver' License#
 
- Driver' Licenses#
 
- Driver'sLic # 
- Driver'sLics # 
- Driver'sLicense # 
- Driver'sLicenses # 
- Driver's Lic#
 
- Driver's Lics#
 
- Driver's License#
 
- Driver's Licenses#
 
- cartão de identificação # 
- id cards#
 
- identification card#
 
- identification cards#
 


#### <a name="keywordstatenamedriverslicensename"></a>Keyword_[state_name]_drivers_license_name

- Abreviação do estado (por exemplo, "NY")
 
- Nome do estado (por exemplo, "Nova York")
    
   
## <a name="us-individual-taxpayer-identification-number-itin"></a>Número de identificação de contribuinte individual (ITIN) dos EUA

### <a name="format"></a>Formato

Nove dígitos que começam com "9" e contêm um "7" ou "8" como o quarto dígito, opcionalmente formatado com espaços ou traços

### <a name="pattern"></a>Padrão

Formatado:
- O dígito "9" 
- Dois dígitos 
- Um espaço ou um traço 
- Um "7" ou "8" 
- Um dígito 
- Um espaço ou um traço 
- Quatro dígitos

Não Formatado:
- O dígito "9" 
- Dois dígitos 
- Um "7" ou "8" 
- Cinco dígitos

### <a name="checksum"></a>Soma de verificação

Não

### <a name="definition"></a>Definição

Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:
- A função Func_formatted_itin localiza conteúdo que corresponde ao padrão.
- Pelo menos uma das seguintes opções for verdadeira:
    - Uma palavra-chave de Keyword_itin for encontrada.
    - A função Func_us_address encontrar um endereço no formato de data à direita.
    - A função Func_us_date encontra uma data no formato de data à direita.
    - Uma palavra-chave de Keyword_itin_collaborative for encontrada.

Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:
- A função Func_unformatted_itin localiza conteúdo que corresponde ao padrão.
- Pelo menos uma das seguintes opções for verdadeira:
    - Uma palavra-chave de Keyword_itin_collaborative for encontrada.
    - A função Func_us_address encontrar um endereço no formato de data à direita.
    - A função Func_us_date encontra uma data no formato de data à direita.

```
<!-- U.S. Individual Taxpayer Identification Number (ITIN) -->
<Entity id="e55e2a32-f92d-4985-a35d-a0b269eb687b" patternsProximity="300" recommendedConfidence="75">
    <Pattern confidenceLevel="85">
        <IdMatch idRef="Func_formatted_itin" />
        <Any minMatches="1">
          <Match idRef="Keyword_itin" />
          <Match idRef="Func_us_address" />
          <Match idRef="Func_us_date" />
          <Match idRef="Keyword_itin_collaborative" />
        </Any>
    </Pattern>
    <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_unformatted_itin" />
        <Match idRef="Keyword_itin" />
        <Any minMatches="1">
          <Match idRef="Keyword_itin_collaborative" />
          <Match idRef="Func_us_address" />
          <Match idRef="Func_us_date" />
        </Any>
    </Pattern>
</Entity>
```

### <a name="keywords"></a>Palavras-chave

#### <a name="keyworditin"></a>Keyword_itin

- taxpayer
 
- tax id
 
- tax identification
 
- itin
 
- SSN 
- tin
 
- seguridade social 
- tax payer
 
- itins
 
- taxid

 
- individual taxpayer
 

#### <a name="keyworditincollaborative"></a>Keyword_itin_collaborative

- License 
- DL 
- DOB
 
- Data de Nascimento 
- Aniversário  
- Date of Birth
 
   
## <a name="us-social-security-number-ssn"></a>Número de seguridade social dos EUA (SSN)

### <a name="format"></a>Formato

9 dígitos que podem estar em um padrão formatado ou não formatado

> [!NOTE]
> Se emitido antes de meados de 2011, um SSN possui formatação forte onde determinadas partes do número devem se enquadra determinados intervalos seja válido (mas não há nenhum soma de verificação).

### <a name="pattern"></a>Padrão

Quatro funções procurado números de identificação fiscal nas quatro diferentes padrões:
- Func_ssn encontra os números de identificação fiscal com pré-2011 forte formatação formatados com travessões ou espaços (ddd-dd-dddd OR ddd dd dddd)
- Func_unformatted_ssn encontra os números de identificação fiscal com pré-2011 forte formatação que estão não formatado como nove dígitos consecutivos (ddddddddd)
- Func_randomized_formatted_ssn encontrar números de identificação fiscal post-2011 formatados com travessões ou espaços (ddd-dd-dddd OR ddd dd dddd)
- Func_randomized_unformatted_ssn encontrar números de identificação fiscal post-2011 que estão não formatados como nove dígitos consecutivos (ddddddddd)

### <a name="checksum"></a>Soma de verificação

Não


### <a name="definition"></a>Definição

Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:
- A função Func_ssn localiza conteúdo que corresponde ao padrão.
- Uma palavra-chave de Keyword_ssn for encontrada.

Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:
- A função Func_unformatted_ssn encontra o conteúdo que corresponde ao padrão.
- Uma palavra-chave de Keyword_ssn for encontrada.

Uma política de DLP tem 65% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:
- A função Func_randomized_formatted_ssn localiza conteúdo que corresponde ao padrão.
- Uma palavra-chave de Keyword_ssn for encontrada.
- A função Func_ssn não localiza conteúdo que corresponde ao padrão.

Uma política de DLP tem 55% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:
- A função Func_randomized_unformatted_ssn localiza conteúdo que corresponde ao padrão.
- Uma palavra-chave de Keyword_ssn for encontrada.
- A função Func_unformatted_ssn não localiza conteúdo que corresponde ao padrão.

```
<!-- U.S. Social Security Number (SSN) -->
    <Entity id="a44669fe-0d48-453d-a9b1-2cc83f2cba77" patternsProximity="300" recommendedConfidence="75">
      <Pattern confidenceLevel="85">
        <IdMatch idRef="Func_ssn" />
        <Match idRef="Keyword_ssn" />
      </Pattern>
      <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_unformatted_ssn" />
        <Match idRef="Keyword_ssn" />
      </Pattern>
      <Pattern confidenceLevel="65">
        <IdMatch idRef="Func_randomized_formatted_ssn" />
        <Match idRef="Keyword_ssn" />
        <Any minMatches="0" maxMatches="0">
          <Match idRef="Func_ssn" />
        </Any>
      </Pattern>
      <Pattern confidenceLevel="55">
        <IdMatch idRef="Func_randomized_unformatted_ssn" />
        <Match idRef="Keyword_ssn" />
        <Any minMatches="0" maxMatches="0">
          <Match idRef="Func_unformatted_ssn" />
        </Any>
      </Pattern>
    </Entity>
```

### <a name="keywords"></a>Palavras-chave

#### <a name="keywordssn"></a>Keyword_ssn

- Social Security
 
- Social Security#
 
- Soc Sec
 
- SSN 
- SSNS
 
- SSN#
 
- SS#
 
- SSID
 
   

