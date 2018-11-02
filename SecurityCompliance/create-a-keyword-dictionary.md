---
title: Criar um dicionário de palavras-chave
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: 6/29/2018
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Priority
ms.collection: Strat_O365_IP
search.appverid:
- MOE150
- MET150
ms.assetid: c8a95d1b-c3b6-4613-98ab-0331d1872cf3
description: Identificar informações confidenciais, às vezes, exige procurar palavras-chave, especialmente quando identificar o conteúdo genérico (como comunicações relacionadas à saúde) ou idioma inapropriado ou explícito. Embora você possa criar listas de palavra-chave nos tipos de informação confidencial, essas listas são limitadas no tamanho e exigem modificar XML para criá-los ou editá-los. Dicionários de palavras-chave fornecem um gerenciamento mais simples de palavras-chave em uma escala muito maior, com suporte até 100.000 termos por dicionário.
ms.openlocfilehash: 1cf41df5475af7ac5018cd34ea26e66ad5d668ee
ms.sourcegitcommit: ceb70ea863d8b97afea077a04fc7ec612b870695
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25857229"
---
# <a name="create-a-keyword-dictionary"></a>Criar um dicionário de palavras-chave

A Prevenção de perda de dados (DLP) no Office 365 pode identificar, monitorar e proteger suas informações confidenciais. Identificar informações confidenciais, às vezes, exige procurar palavras-chave, especialmente quando identificar o conteúdo genérico (como comunicações relacionadas à saúde) ou idioma inapropriado ou explícito. Embora você possa criar listas de palavra-chave nos tipos de informação confidencial, essas listas são limitadas no tamanho e exigem modificar XML para criá-los ou editá-los. Dicionários de palavras-chave fornecem um gerenciamento mais simples de palavras-chave em uma escala muito maior, com suporte até 100.000 termos por dicionário.
  
## <a name="basic-steps-to-creating-a-keyword-dictionary"></a>Etapas básicas para criar um dicionário de palavra-chave

As palavras-chave para o seu dicionário podem vir de uma variedade de fontes, mais comumente de um arquivo (como uma lista .csv ou .txt), de uma lista que você insere diretamente no cmdlet ou de um dicionário existente. Quando você cria um dicionário de palavras-chave, siga as mesmas etapas principais:
  
1. **Conectar-se ao PowerShell do Centro de Segurança e Conformidade** – confira [este tópico](https://docs.microsoft.com/pt-BR/powershell/exchange/office-365-scc/connect-to-scc-powershell/connect-to-scc-powershell).
    
2. **Defina ou carregue suas palavras-chave na sua fonte pretendido** - o cmdlet para criar um dicionário de palavras-chave aceita uma lista de palavras-chave separadas por vírgula, de modo que esta etapa podem variar dependendo da origem de suas palavras-chave. 
    
3. **Codifique suas palavras-chave** - uma vez carregadas, são convertidas em uma matriz bytes antes de serem importadas. 
    
4. **Crie seu dicionário** - escolha um nome e uma descrição e crie seu dicionário. 
    
## <a name="create-a-keyword-dictionary-from-a-file"></a>Criar um dicionário de palavras-chave de um arquivo

Muitas vezes, quando você precisa criar um dicionário grande é para usar palavras-chave de um arquivo ou uma lista exportados de outra fonte. Nesse caso, você criará um dicionário de palavras-chave que contém uma lista de termos inadequados a verificar em emails externos. Será preciso [conectar-se ao PowerShell do Centro de Segurança e Conformidade do Office 365](https://docs.microsoft.com/pt-BR/powershell/exchange/office-365-scc/connect-to-scc-powershell/connect-to-scc-powershell).
  
1. Copie as palavras-chave para um arquivo de texto e verifique se cada palavra-chave está em uma linha separada.
    
2. Salve o arquivo de texto com codificação Unicode. No Bloco de Notas \> **Salvar como** \> **Codificação** \> **Unicode**.
    
3. Leia o arquivo em uma variável executando este cmdlet:
    
  ```
  $fileData = Get-Content <filename> -Encoding Byte -ReadCount 0
  ```

4. Crie o dicionário executando este cmdlet:
    
  ```
  New-DlpKeywordDictionary -Name <name> -Description <description> -FileData $fileData
  ```

## <a name="modifying-an-existing-keyword-dictionary"></a>Como modificar um dicionário de palavra-chave existente

Talvez seja necessário modificar palavras-chave em um dos seus dicionários de palavras-chave ou modificar um dos dicionários internos. Neste exemplo, modificaremos alguns termos no PowerShell, salvaremos os termos localmente onde você pode modificá-los em um editor e atualizar os termos anteriores no local. Primeiro, recupere o objeto dicionário:
  
```
$dict = Get-DlpKeywordDictionary -Name "Diseases"
```

A impressão de `$dict` mostrará as diversas variáveis. As próprias palavras-chave estão armazenadas em um objeto de back-end, mas `$dict.KeywordDictionary` contém uma cadeia de caracteres de representação delas, que você usará para modificar o dicionário. Para modificar o dicionário, será necessário colocar a cadeia de caracteres de termos de volta em uma matriz usando o método `.split(',')`. Em seguida, você limpará espaços indesejados entre palavras-chave com o método `.trim()`, deixando apenas as palavras-chave com as quais trabalhar. 
  
```
$terms = $dict.KeywordDictionary.split(',').trim()
```

Agora, você removerá alguns termos do dicionário. Como o dicionário de exemplo tem apenas alguns as palavras-chave, você poderá ignorar facilmente para exportar o dicionário e editá-lo no Bloco de Notas, mas os dicionários geralmente contêm uma grande quantidade de texto, então você vai aprender primeiro assim para editá-los facilmente no PowerShell.
  
Na última etapa, você salvou as palavras-chave em uma matriz. Há várias maneiras de [remover itens de uma matriz](https://go.microsoft.com/fwlink/p/?linkid=852620), mas como uma abordagem simples, você criará uma matriz de termos que deseja remover do dicionário e, em seguida, copia apenas os termos de dicionário para que ele não esteja na lista de termos para remover.
  
Execute o comando `$terms` para mostrar a lista atual de termos. A saída do comando tem esta aparência: 
  
```
aarskog's syndrome
abandonment
abasia
abderhalden-kaufmann-lignac
abdominalgia
abduction contracture
abetalipoproteinemia
abiotrophy
ablatio
ablation
ablepharia
abocclusion
abolition
aborter
abortion
abortus
aboulomania
abrami's disease
```

Execute este comando para especificar os termos que você deseja remover:
  
```
$termsToRemove = @('abandonment', 'ablatio')
```

Execute este comando para remover os termos realmente da lista:
  
```
$updatedTerms = $terms | Where-Object{ $_ -notin $termsToRemove }
```

Execute o comando `$updatedTerms` para mostrar a lista atualizada de termos. A saída do comando tem esta aparência (os termos especificados foram removidos): 
  
```
aarskog's syndrome
abasia
abderhalden-kaufmann-lignac
abdominalgia
abduction contracture
abetalipo proteinemia
abiotrophy
ablation
ablepharia
abocclusion
abolition
aborter
abortion
abortus
aboulomania
abrami's disease
```

Agora, salve o dicionário localmente e adicione mais alguns termos. Você pode adicionar os termos direto aqui no PowerShell, mas você ainda precisará exportar o arquivo localmente para garantir que ele está salvo com codificação Unicode e contém o BOM.
  
Salve o dicionário localmente executando o seguinte:
  
```
Set-Content $updatedTerms -Path "C:\myPath\terms.txt"
```

Agora basta abrir o arquivo, adicionar os termos adicionais e salvar a codificação Unicode (UTF-16). Agora você carregará os termos atualizados e atualizará o dicionário no local.
  
```
PS> Set-DlpKeywordDictionary -Identity "Diseases" -FileData (Get-Content -Path "C:myPath\terms.txt" -Encoding Byte -ReadCount 0)
```

Agora, o dicionário foi atualizado no local. Observe que o campo `Identity` leva o nome do dicionário. Se você também quiser alterar o nome do dicionário usando o cmdlet `set-`, basta adicionar o parâmetro `-Name` para o que está acima com o novo nome do dicionário. 
  
## <a name="using-keyword-dictionaries-in-custom-sensitive-information-types-and-dlp-policies"></a>Usar dicionários de palavras-chave em tipos de informação confidencial personalizados e as políticas DLP

Os dicionários de palavras-chave podem ser usados como parte dos requisitos de correspondência de um tipo de informação confidencial personalizado ou como um tipo de informação confidencial por si. Ambos precisam [criar um tipo de informação confidencial personalizado no PowerShell do Centro de Conformidade e Segurança do Office 365](create-a-custom-sensitive-information-type-in-scc-powershell.md). Siga as instruções do artigo vinculado para criar um tipo de informação confidencial. Depois do XML, você precisará do identificador GUID para o dicionário usá-lo.
  
```
<Entity id="9e5382d0-1b6a-42fd-820e-44e0d3b15b6e" patternsProximity="300" recommendedConfidence="75">
    <Pattern confidenceLevel="75">
        <IdMatch idRef=". . ."/>
    </Pattern>
</Entity>
```

Para obter a identidade do seu dicionário, execute este comando e copie o valor da propriedade **Identity**: 
  
```
Get-DlpKeywordDictionary -Name "Diseases"
```

A saída do comando será parecida com o seguinte:
  
```
RunspaceId        : 138e55e7-ea1e-4f7a-b824-79f2c4252255
Identity          : 8d2d44b0-91f4-41f2-94e0-21c1c5b5fc9f
Name              : Diseases
Description       : Names of diseases and injuries from ICD-10-CM lexicon
KeywordDictionary : aarskog's syndrome, abandonment, abasia, abderhalden-kaufmann-lignac, abdominalgia, abduction contracture, abetalipo
                    proteinemia, abiotrophy, ablatio, ablation, ablepharia, abocclusion, abolition, aborter, abortion, abortus, aboulomania,
                    abrami's disease, abramo
IsValid           : True
ObjectState       : Unchanged
```

Cole a identidade no XML do seu tipo de informação confidencial personalizado e carregue-a. Agora seu dicionário aparecerá na sua lista de tipos de informação confidencial e você poderá usá-lo direto em sua política, especificando o número de palavras-chave necessário para corresponder.
  
```
<Entity id="d333c6c2-5f4c-4131-9433-db3ef72a89e8" patternsProximity="300" recommendedConfidence="85">
      <Pattern confidenceLevel="85">
        <IdMatch idRef="8d2d44b0-91f4-41f2-94e0-21c1c5b5fc9f" />
      </Pattern>
    </Entity>
    <LocalizedStrings>
      <Resource idRef="d333c6c2-5f4c-4131-9433-db3ef72a89e8">
        <Name default="true" langcode="en-us">Diseases</Name>
        <Description default="true" langcode="en-us">Detects various diseases</Description>
      </Resource>
    </LocalizedStrings>
```


