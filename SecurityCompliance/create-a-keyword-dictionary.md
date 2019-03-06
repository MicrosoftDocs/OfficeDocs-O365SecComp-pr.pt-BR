---
title: Criar um dicionário de palavras-chave
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: 6/29/2018
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Priority
ms.collection: M365-security-compliance
search.appverid:
- MOE150
- MET150
description: Identificar informações confidenciais, às vezes, exige procurar palavras-chave, especialmente quando identificar o conteúdo genérico (como comunicações relacionadas à saúde) ou idioma inapropriado ou explícito. Embora você possa criar listas de palavra-chave nos tipos de informação confidencial, essas listas são limitadas no tamanho e exigem modificar XML para criá-los ou editá-los. Dicionários de palavras-chave fornecem um gerenciamento mais simples de palavras-chave em uma escala muito maior, com suporte até 100.000 termos por dicionário.
ms.openlocfilehash: bd13b4d522b22773fe56f93e1975f1d4decfbfe5
ms.sourcegitcommit: ed822a776d3419853453583e882f3c61ca26d4b2
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/05/2019
ms.locfileid: "30410726"
---
# <a name="create-a-keyword-dictionary"></a><span data-ttu-id="7bc94-105">Criar um dicionário de palavras-chave</span><span class="sxs-lookup"><span data-stu-id="7bc94-105">Create a keyword dictionary</span></span>

<span data-ttu-id="7bc94-p102">A Prevenção de perda de dados (DLP) no Office 365 pode identificar, monitorar e proteger suas informações confidenciais. Identificar informações confidenciais, às vezes, exige procurar palavras-chave, especialmente quando identificar o conteúdo genérico (como comunicações relacionadas à saúde) ou idioma inapropriado ou explícito. Embora você possa criar listas de palavra-chave nos tipos de informação confidencial, essas listas são limitadas no tamanho e exigem modificar XML para criá-los ou editá-los. Dicionários de palavras-chave fornecem um gerenciamento mais simples de palavras-chave em uma escala muito maior, com suporte até 100.000 termos por dicionário.</span><span class="sxs-lookup"><span data-stu-id="7bc94-p102">Data loss prevention (DLP) in Office 365 can identify, monitor, and protect your sensitive information. Identifying sensitive information sometimes requires looking for keywords, particularly when identifying generic content (such as healthcare-related communication) or inappropriate or explicit language. While you can create keyword lists in sensitive information types, keyword lists are limited in size and require modifying XML to create or edit them. Keyword dictionaries provide simpler management of keywords and at a much larger scale, supporting up to 100,000 terms per dictionary.</span></span>
  
## <a name="basic-steps-to-creating-a-keyword-dictionary"></a><span data-ttu-id="7bc94-110">Etapas básicas para criar um dicionário de palavra-chave</span><span class="sxs-lookup"><span data-stu-id="7bc94-110">Basic steps to creating a keyword dictionary</span></span>

<span data-ttu-id="7bc94-p103">As palavras-chave para o seu dicionário podem vir de uma variedade de fontes, mais comumente de um arquivo (como uma lista .csv ou .txt), de uma lista que você insere diretamente no cmdlet ou de um dicionário existente. Quando você cria um dicionário de palavras-chave, siga as mesmas etapas principais:</span><span class="sxs-lookup"><span data-stu-id="7bc94-p103">The keywords for your dictionary could come from a variety of sources, most commonly from a file (such as a .csv or .txt list), from a list you enter directly in the cmdlet, or from an existing dictionary. When you create a keyword dictionary, you follow the same core steps:</span></span>
  
1. <span data-ttu-id="7bc94-113">**Conectar-se ao PowerShell do Centro de Segurança e Conformidade** – confira [este tópico](https://docs.microsoft.com/pt-BR/powershell/exchange/office-365-scc/connect-to-scc-powershell/connect-to-scc-powershell).</span><span class="sxs-lookup"><span data-stu-id="7bc94-113">**Connect to Security &amp; Compliance Center PowerShell** - see [this topic](https://docs.microsoft.com/pt-BR/powershell/exchange/office-365-scc/connect-to-scc-powershell/connect-to-scc-powershell).</span></span>
    
2. <span data-ttu-id="7bc94-114">**Defina ou carregue suas palavras-chave na sua fonte pretendido** - o cmdlet para criar um dicionário de palavras-chave aceita uma lista de palavras-chave separadas por vírgula, de modo que esta etapa podem variar dependendo da origem de suas palavras-chave.</span><span class="sxs-lookup"><span data-stu-id="7bc94-114">**Define or load your keywords from your intended source** - the cmdlet to create a keyword dictionary accepts a comma-separated list of keywords, so this step will vary slightly depending on where your keywords come from.</span></span> 
    
3. <span data-ttu-id="7bc94-115">**Codifique suas palavras-chave** - uma vez carregadas, são convertidas em uma matriz bytes antes de serem importadas.</span><span class="sxs-lookup"><span data-stu-id="7bc94-115">**Encode your keywords** - once loaded, they're converted to a byte array before they're imported.</span></span> 
    
4. <span data-ttu-id="7bc94-116">**Crie seu dicionário** - escolha um nome e uma descrição e crie seu dicionário.</span><span class="sxs-lookup"><span data-stu-id="7bc94-116">**Create your dictionary** - choose a name and description and create your dictionary.</span></span> 
    
## <a name="create-a-keyword-dictionary-from-a-file"></a><span data-ttu-id="7bc94-117">Criar um dicionário de palavras-chave de um arquivo</span><span class="sxs-lookup"><span data-stu-id="7bc94-117">Create a keyword dictionary from a file</span></span>

<span data-ttu-id="7bc94-p104">Muitas vezes, quando você precisa criar um dicionário grande é para usar palavras-chave de um arquivo ou uma lista exportados de outra fonte. Nesse caso, você criará um dicionário de palavras-chave que contém uma lista de termos inadequados a verificar em emails externos. Será preciso [conectar-se ao PowerShell do Centro de Segurança e Conformidade do Office 365](https://docs.microsoft.com/pt-BR/powershell/exchange/office-365-scc/connect-to-scc-powershell/connect-to-scc-powershell).</span><span class="sxs-lookup"><span data-stu-id="7bc94-p104">Often when you need to create a large dictionary, it's to use keywords from a file or a list exported from some other source. In this case, you'll create a keyword dictionary containing a list of inappropriate language to screen in external email. You need to first [Connect to Office 365 Security &amp; Compliance Center PowerShell](https://docs.microsoft.com/pt-BR/powershell/exchange/office-365-scc/connect-to-scc-powershell/connect-to-scc-powershell).</span></span>
  
1. <span data-ttu-id="7bc94-121">Copie as palavras-chave para um arquivo de texto e verifique se cada palavra-chave está em uma linha separada.</span><span class="sxs-lookup"><span data-stu-id="7bc94-121">Copy the keywords into a text file and make sure that each keyword is on a separate line.</span></span>
    
2. <span data-ttu-id="7bc94-p105">Salve o arquivo de texto com codificação Unicode. No Bloco de Notas \> **Salvar como** \> **Codificação** \> **Unicode**.</span><span class="sxs-lookup"><span data-stu-id="7bc94-p105">Save the text file with Unicode encoding. In Notepad \> **Save As** \> **Encoding** \> **Unicode**.</span></span>
    
3. <span data-ttu-id="7bc94-124">Leia o arquivo em uma variável executando este cmdlet:</span><span class="sxs-lookup"><span data-stu-id="7bc94-124">Read the file into a variable by running this cmdlet:</span></span>
    
  ```
  $fileData = Get-Content <filename> -Encoding Byte -ReadCount 0
  ```

4. <span data-ttu-id="7bc94-125">Crie o dicionário executando este cmdlet:</span><span class="sxs-lookup"><span data-stu-id="7bc94-125">Create the dictionary by running this cmdlet:</span></span>
    
  ```
  New-DlpKeywordDictionary -Name <name> -Description <description> -FileData $fileData
  ```

## <a name="modifying-an-existing-keyword-dictionary"></a><span data-ttu-id="7bc94-126">Como modificar um dicionário de palavra-chave existente</span><span class="sxs-lookup"><span data-stu-id="7bc94-126">Modifying an existing keyword dictionary</span></span>

<span data-ttu-id="7bc94-p106">Talvez seja necessário modificar palavras-chave em um dos seus dicionários de palavras-chave ou modificar um dos dicionários internos. Neste exemplo, modificaremos alguns termos no PowerShell, salvaremos os termos localmente onde você pode modificá-los em um editor e atualizar os termos anteriores no local. Primeiro, recupere o objeto dicionário:</span><span class="sxs-lookup"><span data-stu-id="7bc94-p106">You might need to modify keywords in one of your keyword dictionaries, or modify one of the built-in dictionaries. In this example, we'll modify some terms in PowerShell, save the terms locally where you can modify them in an editor, and then update the previous terms in place. First, retrieve the dictionary object:</span></span>
  
```
$dict = Get-DlpKeywordDictionary -Name "Diseases"
```

<span data-ttu-id="7bc94-p107">A impressão de `$dict` mostrará as diversas variáveis. As próprias palavras-chave estão armazenadas em um objeto de back-end, mas `$dict.KeywordDictionary` contém uma cadeia de caracteres de representação delas, que você usará para modificar o dicionário. Para modificar o dicionário, será necessário colocar a cadeia de caracteres de termos de volta em uma matriz usando o método `.split(',')`. Em seguida, você limpará espaços indesejados entre palavras-chave com o método `.trim()`, deixando apenas as palavras-chave com as quais trabalhar.</span><span class="sxs-lookup"><span data-stu-id="7bc94-p107">Printing  `$dict` will show the various variables. The keywords themselves are stored in an object on the backend, but  `$dict.KeywordDictionary` contains a string representation of them, which you'll use to modify the dictionary. Before you modify the dictionary, you need to turn the string of terms back into an array using the  `.split(',')` method. Then you'll clean up the unwanted spaces between the keywords with the  `.trim()` method, leaving just the keywords to work with.</span></span> 
  
```
$terms = $dict.KeywordDictionary.split(',').trim()
```

<span data-ttu-id="7bc94-p108">Agora, você removerá alguns termos do dicionário. Como o dicionário de exemplo tem apenas alguns as palavras-chave, você poderá ignorar facilmente para exportar o dicionário e editá-lo no Bloco de Notas, mas os dicionários geralmente contêm uma grande quantidade de texto, então você vai aprender primeiro assim para editá-los facilmente no PowerShell.</span><span class="sxs-lookup"><span data-stu-id="7bc94-p108">Now you'll remove some terms from the dictionary. Because the example dictionary has only a few keywords, you could just as easily skip to exporting the dictionary and editing it in Notepad, but dictionaries generally contain a large amount of text, so you'll first learn this way to edit them easily in PowerShell.</span></span>
  
<span data-ttu-id="7bc94-p109">Na última etapa, você salvou as palavras-chave em uma matriz. Há várias maneiras de [remover itens de uma matriz](https://go.microsoft.com/fwlink/p/?linkid=852620), mas como uma abordagem simples, você criará uma matriz de termos que deseja remover do dicionário e, em seguida, copia apenas os termos de dicionário para que ele não esteja na lista de termos para remover.</span><span class="sxs-lookup"><span data-stu-id="7bc94-p109">In the last step, you saved the keywords to an array. There are several ways to [remove items from an array](https://go.microsoft.com/fwlink/p/?linkid=852620), but as a straightforward approach, you'll create an array of the terms you want to remove from the dictionary, and then copy only the dictionary terms to it that aren't in the list of terms to remove.</span></span>
  
<span data-ttu-id="7bc94-p110">Execute o comando `$terms` para mostrar a lista atual de termos. A saída do comando tem esta aparência:</span><span class="sxs-lookup"><span data-stu-id="7bc94-p110">Run the command  `$terms` to show the current list of terms. The output of the command looks like this:</span></span> 
  
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

<span data-ttu-id="7bc94-140">Execute este comando para especificar os termos que você deseja remover:</span><span class="sxs-lookup"><span data-stu-id="7bc94-140">Run this command to specify the terms that you want to remove:</span></span>
  
```
$termsToRemove = @('abandonment', 'ablatio')
```

<span data-ttu-id="7bc94-141">Execute este comando para remover os termos realmente da lista:</span><span class="sxs-lookup"><span data-stu-id="7bc94-141">Run this command to actually remove the terms from the list:</span></span>
  
```
$updatedTerms = $terms | Where-Object{ $_ -notin $termsToRemove }
```

<span data-ttu-id="7bc94-p111">Execute o comando `$updatedTerms` para mostrar a lista atualizada de termos. A saída do comando tem esta aparência (os termos especificados foram removidos):</span><span class="sxs-lookup"><span data-stu-id="7bc94-p111">Run the command  `$updatedTerms` to show the updated list of terms. The output of the command looks like this (the specified terms have been removed):</span></span> 
  
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

<span data-ttu-id="7bc94-p112">Agora, salve o dicionário localmente e adicione mais alguns termos. Você pode adicionar os termos direto aqui no PowerShell, mas você ainda precisará exportar o arquivo localmente para garantir que ele está salvo com codificação Unicode e contém o BOM.</span><span class="sxs-lookup"><span data-stu-id="7bc94-p112">Now save the dictionary locally and add a few more terms. You could add the terms right here in PowerShell, but you'll still need to export the file locally to ensure it's saved with Unicode encoding and contains the BOM.</span></span>
  
<span data-ttu-id="7bc94-146">Salve o dicionário localmente executando o seguinte:</span><span class="sxs-lookup"><span data-stu-id="7bc94-146">Save the dictionary locally by running the following:</span></span>
  
```
Set-Content $updatedTerms -Path "C:\myPath\terms.txt"
```

<span data-ttu-id="7bc94-p113">Agora basta abrir o arquivo, adicionar os termos adicionais e salvar a codificação Unicode (UTF-16). Agora você carregará os termos atualizados e atualizará o dicionário no local.</span><span class="sxs-lookup"><span data-stu-id="7bc94-p113">Now simply open the file, add your additional terms, and save with Unicode encoding (UTF-16). Now you'll upload the updated terms and update the dictionary in place.</span></span>
  
```
PS> Set-DlpKeywordDictionary -Identity "Diseases" -FileData (Get-Content -Path "C:myPath\terms.txt" -Encoding Byte -ReadCount 0)
```

<span data-ttu-id="7bc94-p114">Agora, o dicionário foi atualizado no local. Observe que o campo `Identity` leva o nome do dicionário. Se você também quiser alterar o nome do dicionário usando o cmdlet `set-`, basta adicionar o parâmetro `-Name` para o que está acima com o novo nome do dicionário.</span><span class="sxs-lookup"><span data-stu-id="7bc94-p114">Now the dictionary has been updated in place. Note that the  `Identity` field takes the name of the dictionary. If you wanted to also change the name of your dictionary using the  `set-` cmdlet, you would just need to add the  `-Name` parameter to what's above with your new dictionary name.</span></span> 
  
## <a name="using-keyword-dictionaries-in-custom-sensitive-information-types-and-dlp-policies"></a><span data-ttu-id="7bc94-152">Usar dicionários de palavras-chave em tipos de informação confidencial personalizados e as políticas DLP</span><span class="sxs-lookup"><span data-stu-id="7bc94-152">Using keyword dictionaries in custom sensitive information types and DLP policies</span></span>

<span data-ttu-id="7bc94-p115">Os dicionários de palavras-chave podem ser usados como parte dos requisitos de correspondência de um tipo de informação confidencial personalizado ou como um tipo de informação confidencial por si. Ambos precisam [criar um tipo de informação confidencial personalizado no PowerShell do Centro de Conformidade e Segurança do Office 365](create-a-custom-sensitive-information-type-in-scc-powershell.md). Siga as instruções do artigo vinculado para criar um tipo de informação confidencial. Depois do XML, você precisará do identificador GUID para o dicionário usá-lo.</span><span class="sxs-lookup"><span data-stu-id="7bc94-p115">Keyword dictionaries can be used as part of the match requirements for a custom sensitive information type, or as a sensitive information type themselves. Both require [Create a custom sensitive information type in Office 365 Security & Compliance Center PowerShell](create-a-custom-sensitive-information-type-in-scc-powershell.md). Follow the instructions in the linked article to create a sensitive information type. Once you have the XML, you'll need the GUID identifier for the dictionary to use it.</span></span>
  
```
<Entity id="9e5382d0-1b6a-42fd-820e-44e0d3b15b6e" patternsProximity="300" recommendedConfidence="75">
    <Pattern confidenceLevel="75">
        <IdMatch idRef=". . ."/>
    </Pattern>
</Entity>
```

<span data-ttu-id="7bc94-157">Para obter a identidade do seu dicionário, execute este comando e copie o valor da propriedade **Identity**:</span><span class="sxs-lookup"><span data-stu-id="7bc94-157">To get the identity of your dictionary, run this command and copy the **Identity** property value:</span></span> 
  
```
Get-DlpKeywordDictionary -Name "Diseases"
```

<span data-ttu-id="7bc94-158">A saída do comando será parecida com o seguinte:</span><span class="sxs-lookup"><span data-stu-id="7bc94-158">The output of the command looks like this:</span></span>
  
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

<span data-ttu-id="7bc94-p116">Cole a identidade no XML do seu tipo de informação confidencial personalizado e carregue-a. Agora seu dicionário aparecerá na sua lista de tipos de informação confidencial e você poderá usá-lo direto em sua política, especificando o número de palavras-chave necessário para corresponder.</span><span class="sxs-lookup"><span data-stu-id="7bc94-p116">Paste the identity into your custom sensitive information type's XML and upload it. Now your dictionary will appear in your list of sensitive information types and you can use it right in your policy, specifying how many keywords are required to match.</span></span>
  
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


