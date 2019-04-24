---
title: Criar um dicionário de palavras-chave
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
ms.date: 04/11/2019
localization_priority: Normal
ms.collection:
- M365-security-compliance
search.appverid:
- MOE150
- MET150
description: Identificar informações confidenciais, às vezes, exige procurar palavras-chave, especialmente quando identificar o conteúdo genérico (como comunicações relacionadas à saúde) ou idioma inapropriado ou explícito. Embora você possa criar listas de palavra-chave nos tipos de informação confidencial, essas listas são limitadas no tamanho e exigem modificar XML para criá-los ou editá-los. Dicionários de palavras-chave fornecem um gerenciamento mais simples de palavras-chave em uma escala muito maior, com suporte até 100.000 termos por dicionário.
ms.openlocfilehash: 142f471d80c7278cabd4c437f0ae0ee9af3ff219
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32258159"
---
# <a name="create-a-keyword-dictionary"></a><span data-ttu-id="997b4-105">Criar um dicionário de palavras-chave</span><span class="sxs-lookup"><span data-stu-id="997b4-105">Create a keyword dictionary</span></span>

<span data-ttu-id="997b4-106">A prevenção de perda de dados (DLP) no Office 365 pode identificar, monitorar e proteger suas informações confidenciais.</span><span class="sxs-lookup"><span data-stu-id="997b4-106">Data loss prevention (DLP) in Office 365 can identify, monitor, and protect your sensitive information.</span></span> <span data-ttu-id="997b4-107">A identificação de informações confidenciais às vezes requer a procura de palavras-chave, particularmente ao identificar conteúdo genérico (como comunicação relacionada à assistência médica) ou linguagem inadequada ou explícita.</span><span class="sxs-lookup"><span data-stu-id="997b4-107">Identifying sensitive information sometimes requires looking for keywords, particularly when identifying generic content (such as healthcare-related communication), or inappropriate or explicit language.</span></span> <span data-ttu-id="997b4-108">Embora você possa criar listas de palavras-chave em tipos de informações confidenciais, as listas de palavras-chave têm tamanho limitado e exigem a modificação de XML para criá-las ou editá-las.</span><span class="sxs-lookup"><span data-stu-id="997b4-108">Although you can create keyword lists in sensitive information types, keyword lists are limited in size and require modifying XML to create or edit them.</span></span> <span data-ttu-id="997b4-109">Os dicionários de palavras-chave oferecem gerenciamento mais simples de palavras-chave e em escala muito maior, com suporte para até 100.000 termos por dicionário.</span><span class="sxs-lookup"><span data-stu-id="997b4-109">Keyword dictionaries provide simpler management of keywords and at a much larger scale, supporting up to 100,000 terms per dictionary.</span></span>
  
## <a name="basic-steps-to-creating-a-keyword-dictionary"></a><span data-ttu-id="997b4-110">Etapas básicas para criar um dicionário de palavra-chave</span><span class="sxs-lookup"><span data-stu-id="997b4-110">Basic steps to creating a keyword dictionary</span></span>

<span data-ttu-id="997b4-p103">As palavras-chave para o seu dicionário podem vir de uma variedade de fontes, mais comumente de um arquivo (como uma lista .csv ou .txt), importada no serviço ou pelo cmdlet do PowerShell de uma lista que você insere diretamente no cmdlet do PowerShell ou de um dicionário existente. Quando você cria um dicionário de palavras-chave, siga as mesmas etapas principais:</span><span class="sxs-lookup"><span data-stu-id="997b4-p103">The keywords for your dictionary could come from a variety of sources, most commonly from a file (such as a .csv or .txt list) imported in the service or by PowerShell cmdlet, from a list you enter directly in the PowerShell cmdlet, or from an existing dictionary. When you create a keyword dictionary, you follow the same core steps:</span></span>
  
1. <span data-ttu-id="997b4-113">Use o **centro de conformidade** do &[https://protection.office.com](https://protection.office.com)de segurança () ou conecte-se ao **PowerShell do centro de conformidade de &amp; segurança do Office 365**.</span><span class="sxs-lookup"><span data-stu-id="997b4-113">Use the **Security & Compliance Center** ([https://protection.office.com](https://protection.office.com)) or connect to  **Office 365 Security &amp; Compliance Center PowerShell**.</span></span>
    
2. <span data-ttu-id="997b4-114">**Defina ou carregue suas palavras-chave da fonte pretendida**.</span><span class="sxs-lookup"><span data-stu-id="997b4-114">**Define or load your keywords from your intended source**.</span></span> <span data-ttu-id="997b4-115">O assistente e o cmdlet aceitam uma lista separada por vírgulas de palavras-chave para criar um dicionário de palavras-chave personalizado, portanto, essa etapa variará um pouco dependendo de onde vêm suas palavras-chave.</span><span class="sxs-lookup"><span data-stu-id="997b4-115">The wizard and the cmdlet both accept a comma-separated list of keywords to create a custom keyword dictionary, so this step will vary slightly depending on where your keywords come from.</span></span> <span data-ttu-id="997b4-116">Uma vez carregadas, elas são codificadas e convertidas em uma matriz bytes antes de serem importadas.</span><span class="sxs-lookup"><span data-stu-id="997b4-116">Once loaded, they're encoded and converted to a byte array before they're imported.</span></span>
    
3. <span data-ttu-id="997b4-117">**Crie seu dicionário**.</span><span class="sxs-lookup"><span data-stu-id="997b4-117">**Create your dictionary**.</span></span> <span data-ttu-id="997b4-118">Escolha um nome e uma descrição e crie seu dicionário.</span><span class="sxs-lookup"><span data-stu-id="997b4-118">Choose a name and description and create your dictionary.</span></span>

## <a name="create-a-keyword-dictionary-using-the-security--compliance-center"></a><span data-ttu-id="997b4-119">Criar um dicionário de palavras-chave usando o centro de conformidade do & de segurança</span><span class="sxs-lookup"><span data-stu-id="997b4-119">Create a keyword dictionary using the Security & Compliance Center</span></span>

<span data-ttu-id="997b4-120">Use as etapas a seguir para criar e importar palavras-chave para um dicionário personalizado:</span><span class="sxs-lookup"><span data-stu-id="997b4-120">Use the following steps to create and import keywords for a custom dictionary:</span></span>

1. <span data-ttu-id="997b4-121">Conecte-se ao centro de conformidade do[https://protection.office.com](https://protection.office.com)_AMP_ de segurança ().</span><span class="sxs-lookup"><span data-stu-id="997b4-121">Connect to the Security & Compliance Center ([https://protection.office.com](https://protection.office.com)).</span></span>

2. <span data-ttu-id="997b4-122">Navegue até **Classificações > Tipos de informações confidenciais**.</span><span class="sxs-lookup"><span data-stu-id="997b4-122">Navigate to **Classifications > Sensitive info types**.</span></span>

3. <span data-ttu-id="997b4-123">Selecione **Criar** e insira **Nome** e **Descrição** para o tipo de informações confidenciais, em seguida, selecione **Avançar**</span><span class="sxs-lookup"><span data-stu-id="997b4-123">Select **Create** and enter a **Name** and **Description** for your sensitive info type, then select **Next**</span></span>

4. <span data-ttu-id="997b4-124">Selecione **Adicionar um elemento**e selecione **Dicionário (Palavras-chave grandes)** na lista suspensa **Detectar conteúdo que tenha**.</span><span class="sxs-lookup"><span data-stu-id="997b4-124">Select **Add an element**, then select **Dictionary (Large keywords)** in the **Detect content containing** drop-down list.</span></span>

5. <span data-ttu-id="997b4-125">Selecione **Adicionar um dicionário**</span><span class="sxs-lookup"><span data-stu-id="997b4-125">Select **Add a dictionary**</span></span>

6. <span data-ttu-id="997b4-126">Sob o controle da pesquisa, selecione **Você pode criar novos dicionários de palavras-chave**.</span><span class="sxs-lookup"><span data-stu-id="997b4-126">Under the Search control, select **You can create new keyword dictionaries here**.</span></span>

7. <span data-ttu-id="997b4-127">Insira um **Nome** para o dicionário personalizado.</span><span class="sxs-lookup"><span data-stu-id="997b4-127">Enter a **Name** for your custom dictionary.</span></span>

8. <span data-ttu-id="997b4-128">Selecione **Importação**e selecione **a partir do texto** ou **a partir do csv** dependendo do tipo de arquivo de palavra-chave.</span><span class="sxs-lookup"><span data-stu-id="997b4-128">Select **Import**, and select either **From text** or **From csv** depending on your keyword file type.</span></span>

9. <span data-ttu-id="997b4-129">Na caixa de diálogo arquivo, selecione o arquivo de palavra-chave no compartilhamento de arquivos do computador ou rede local e selecione **Abrir**.</span><span class="sxs-lookup"><span data-stu-id="997b4-129">In the file dialog, select the keyword file from your local PC or network file share, then select **Open**.</span></span>

10. <span data-ttu-id="997b4-130">Selecione **Salvar**, em seguida selecione o dicionário personalizado da lista **Dicionários de palavras-chave**.</span><span class="sxs-lookup"><span data-stu-id="997b4-130">Select **Save**, then select your custom dictionary from the **Keyword dictionaries** list.</span></span>

11. <span data-ttu-id="997b4-131">Selecione **Próximo**, e em seguida**Avançar**.</span><span class="sxs-lookup"><span data-stu-id="997b4-131">Select **Add**, then select **Next**.</span></span>

12. <span data-ttu-id="997b4-132">Revise e finalize as seleções de tipo de informações confidenciais e selecione **Terminar**.</span><span class="sxs-lookup"><span data-stu-id="997b4-132">Review and finalize your sensitive info type selections, then select **Finish**.</span></span>
    
## <a name="create-a-keyword-dictionary-from-a-file-using-powershell"></a><span data-ttu-id="997b4-133">Criar um dicionário de palavras-chave de um arquivo usando o Power Shell</span><span class="sxs-lookup"><span data-stu-id="997b4-133">Create a keyword dictionary from a file using PowerShell</span></span>

<span data-ttu-id="997b4-134">Geralmente, quando você precisa criar um dicionário grande, é usar palavras-chave de um arquivo ou uma lista exportada de outra fonte.</span><span class="sxs-lookup"><span data-stu-id="997b4-134">Often when you need to create a large dictionary, it's to use keywords from a file or a list exported from some other source.</span></span> <span data-ttu-id="997b4-135">Nesse caso, você criará um dicionário de palavras-chave contendo uma lista de idiomas inadequados para a tela em emails externos.</span><span class="sxs-lookup"><span data-stu-id="997b4-135">In this case, you'll create a keyword dictionary containing a list of inappropriate language to screen in external email.</span></span> <span data-ttu-id="997b4-136">Primeiro você deve [se conectar ao PowerShell do &amp; centro de conformidade de segurança do Office 365](https://docs.microsoft.com/powershell/exchange/office-365-scc/connect-to-scc-powershell/connect-to-scc-powershell).</span><span class="sxs-lookup"><span data-stu-id="997b4-136">You must first [connect to Office 365 Security &amp; Compliance Center PowerShell](https://docs.microsoft.com/powershell/exchange/office-365-scc/connect-to-scc-powershell/connect-to-scc-powershell).</span></span>
  
1. <span data-ttu-id="997b4-137">Copie as palavras-chave para um arquivo de texto e verifique se cada palavra-chave está em uma linha separada.</span><span class="sxs-lookup"><span data-stu-id="997b4-137">Copy the keywords into a text file and make sure that each keyword is on a separate line.</span></span>
    
2. <span data-ttu-id="997b4-p107">Salve o arquivo de texto com codificação Unicode. No Bloco de Notas \> **Salvar como** \> **Codificação** \> **Unicode**.</span><span class="sxs-lookup"><span data-stu-id="997b4-p107">Save the text file with Unicode encoding. In Notepad \> **Save As** \> **Encoding** \> **Unicode**.</span></span>
    
3. <span data-ttu-id="997b4-140">Leia o arquivo em uma variável executando este cmdlet:</span><span class="sxs-lookup"><span data-stu-id="997b4-140">Read the file into a variable by running this cmdlet:</span></span>
    
    ```
    $fileData = Get-Content <filename> -Encoding Byte -ReadCount 0
    ```

4. <span data-ttu-id="997b4-141">Crie o dicionário executando este cmdlet:</span><span class="sxs-lookup"><span data-stu-id="997b4-141">Create the dictionary by running this cmdlet:</span></span>
    
    ```
    New-DlpKeywordDictionary -Name <name> -Description <description> -FileData $fileData
    ```

## <a name="modifying-an-existing-keyword-dictionary"></a><span data-ttu-id="997b4-142">Como modificar um dicionário de palavra-chave existente</span><span class="sxs-lookup"><span data-stu-id="997b4-142">Modifying an existing keyword dictionary</span></span>

<span data-ttu-id="997b4-143">Talvez seja necessário modificar palavras-chave em um de seus dicionários de palavras-chave ou modificar um dos dicionários internos.</span><span class="sxs-lookup"><span data-stu-id="997b4-143">You might need to modify keywords in one of your keyword dictionaries, or modify one of the built-in dictionaries.</span></span> <span data-ttu-id="997b4-144">Atualmente, você pode atualizar somente um dicionário personalizado de palavras-chave usando o PowerShell.</span><span class="sxs-lookup"><span data-stu-id="997b4-144">Currently, your can only update a custom keyword dictionary using PowerShell.</span></span> 

<span data-ttu-id="997b4-145">Por exemplo, modificaremos alguns termos no PowerShell, salvaremos os termos localmente, onde você poderá modificá-los em um editor e, em seguida, atualizar os termos anteriores no local.</span><span class="sxs-lookup"><span data-stu-id="997b4-145">For example, we'll modify some terms in PowerShell, save the terms locally where you can modify them in an editor, and then update the previous terms in place.</span></span> 

<span data-ttu-id="997b4-146">Primeiro, recupere o objeto dicionário:</span><span class="sxs-lookup"><span data-stu-id="997b4-146">First, retrieve the dictionary object:</span></span>
  
```
$dict = Get-DlpKeywordDictionary -Name "Diseases"
```

<span data-ttu-id="997b4-147">A `$dict` impressão mostrará várias variáveis.</span><span class="sxs-lookup"><span data-stu-id="997b4-147">Printing  `$dict` will show the various variables.</span></span> <span data-ttu-id="997b4-148">As palavras-chave são armazenadas em um objeto no back-end, mas `$dict.KeywordDictionary` contêm uma representação de cadeia de caracteres delas, que você usará para modificar o dicionário.</span><span class="sxs-lookup"><span data-stu-id="997b4-148">The keywords themselves are stored in an object on the backend, but  `$dict.KeywordDictionary` contains a string representation of them, which you'll use to modify the dictionary.</span></span> 

<span data-ttu-id="997b4-149">Antes de modificar o dicionário, você precisa transformar a sequência de termos de volta em uma matriz usando o `.split(',')` método.</span><span class="sxs-lookup"><span data-stu-id="997b4-149">Before you modify the dictionary, you need to turn the string of terms back into an array using the  `.split(',')` method.</span></span> <span data-ttu-id="997b4-150">Em seguida, você limpará os espaços indesejados entre as palavras- `.trim()` chave com o método, deixando apenas as palavras-chave com as quais trabalhar.</span><span class="sxs-lookup"><span data-stu-id="997b4-150">Then you'll clean up the unwanted spaces between the keywords with the  `.trim()` method, leaving just the keywords to work with.</span></span> 
  
```
$terms = $dict.KeywordDictionary.split(',').trim()
```

<span data-ttu-id="997b4-p111">Agora, você removerá alguns termos do dicionário. Como o dicionário de exemplo tem apenas alguns as palavras-chave, você poderá ignorar facilmente para exportar o dicionário e editá-lo no Bloco de Notas, mas os dicionários geralmente contêm uma grande quantidade de texto, então você vai aprender primeiro assim para editá-los facilmente no PowerShell.</span><span class="sxs-lookup"><span data-stu-id="997b4-p111">Now you'll remove some terms from the dictionary. Because the example dictionary has only a few keywords, you could just as easily skip to exporting the dictionary and editing it in Notepad, but dictionaries generally contain a large amount of text, so you'll first learn this way to edit them easily in PowerShell.</span></span>
  
<span data-ttu-id="997b4-p112">Na última etapa, você salvou as palavras-chave em uma matriz. Há várias maneiras de [remover itens de uma matriz](https://docs.microsoft.com/previous-versions/windows/it-pro/windows-powershell-1.0/ee692802(v=technet.10)), mas como uma abordagem simples, você criará uma matriz de termos que deseja remover do dicionário e, em seguida, copia apenas os termos de dicionário para que ele não esteja na lista de termos para remover.</span><span class="sxs-lookup"><span data-stu-id="997b4-p112">In the last step, you saved the keywords to an array. There are several ways to [remove items from an array](https://docs.microsoft.com/previous-versions/windows/it-pro/windows-powershell-1.0/ee692802(v=technet.10)), but as a straightforward approach, you'll create an array of the terms you want to remove from the dictionary, and then copy only the dictionary terms to it that aren't in the list of terms to remove.</span></span>
  
<span data-ttu-id="997b4-p113">Execute o comando `$terms` para mostrar a lista atual de termos. A saída do comando tem esta aparência:</span><span class="sxs-lookup"><span data-stu-id="997b4-p113">Run the command  `$terms` to show the current list of terms. The output of the command looks like this:</span></span> 
  
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

<span data-ttu-id="997b4-157">Execute este comando para especificar os termos que você deseja remover:</span><span class="sxs-lookup"><span data-stu-id="997b4-157">Run this command to specify the terms that you want to remove:</span></span>
  
```
$termsToRemove = @('abandonment', 'ablatio')
```

<span data-ttu-id="997b4-158">Execute este comando para remover os termos realmente da lista:</span><span class="sxs-lookup"><span data-stu-id="997b4-158">Run this command to actually remove the terms from the list:</span></span>
  
```
$updatedTerms = $terms | Where-Object{ $_ -notin $termsToRemove }
```

<span data-ttu-id="997b4-p114">Execute o comando `$updatedTerms` para mostrar a lista atualizada de termos. A saída do comando tem esta aparência (os termos especificados foram removidos):</span><span class="sxs-lookup"><span data-stu-id="997b4-p114">Run the command  `$updatedTerms` to show the updated list of terms. The output of the command looks like this (the specified terms have been removed):</span></span> 
  
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

<span data-ttu-id="997b4-p115">Agora, salve o dicionário localmente e adicione mais alguns termos. Você pode adicionar os termos direto aqui no PowerShell, mas você ainda precisará exportar o arquivo localmente para garantir que ele está salvo com codificação Unicode e contém o BOM.</span><span class="sxs-lookup"><span data-stu-id="997b4-p115">Now save the dictionary locally and add a few more terms. You could add the terms right here in PowerShell, but you'll still need to export the file locally to ensure it's saved with Unicode encoding and contains the BOM.</span></span>
  
<span data-ttu-id="997b4-163">Salve o dicionário localmente executando o seguinte:</span><span class="sxs-lookup"><span data-stu-id="997b4-163">Save the dictionary locally by running the following:</span></span>
  
```
Set-Content $updatedTerms -Path "C:\myPath\terms.txt"
```

<span data-ttu-id="997b4-p116">Agora basta abrir o arquivo, adicionar os termos adicionais e salvar a codificação Unicode (UTF-16). Agora você carregará os termos atualizados e atualizará o dicionário no local.</span><span class="sxs-lookup"><span data-stu-id="997b4-p116">Now simply open the file, add your additional terms, and save with Unicode encoding (UTF-16). Now you'll upload the updated terms and update the dictionary in place.</span></span>
  
```
PS> Set-DlpKeywordDictionary -Identity "Diseases" -FileData (Get-Content -Path "C:myPath\terms.txt" -Encoding Byte -ReadCount 0)
```

<span data-ttu-id="997b4-p117">Agora, o dicionário foi atualizado no local. Observe que o campo `Identity` leva o nome do dicionário. Se você também quiser alterar o nome do dicionário usando o cmdlet `set-`, basta adicionar o parâmetro `-Name` para o que está acima com o novo nome do dicionário.</span><span class="sxs-lookup"><span data-stu-id="997b4-p117">Now the dictionary has been updated in place. Note that the  `Identity` field takes the name of the dictionary. If you wanted to also change the name of your dictionary using the  `set-` cmdlet, you would just need to add the  `-Name` parameter to what's above with your new dictionary name.</span></span> 
  
## <a name="using-keyword-dictionaries-in-custom-sensitive-information-types-and-dlp-policies"></a><span data-ttu-id="997b4-169">Usar dicionários de palavras-chave em tipos de informação confidencial personalizados e as políticas DLP</span><span class="sxs-lookup"><span data-stu-id="997b4-169">Using keyword dictionaries in custom sensitive information types and DLP policies</span></span>

<span data-ttu-id="997b4-170">Os dicionários de palavras-chave podem ser usados como parte dos requisitos de correspondência para um tipo de informação confidencial personalizado ou como um tipo de informação confidencial.</span><span class="sxs-lookup"><span data-stu-id="997b4-170">Keyword dictionaries can be used as part of the match requirements for a custom sensitive information type, or as a sensitive information type themselves.</span></span> <span data-ttu-id="997b4-171">Ambas exigem que você crie um [tipo de informação confidencial personalizado](create-a-custom-sensitive-information-type-in-scc-powershell.md).</span><span class="sxs-lookup"><span data-stu-id="997b4-171">Both require you to create a [custom sensitive information type](create-a-custom-sensitive-information-type-in-scc-powershell.md).</span></span> <span data-ttu-id="997b4-172">Siga as instruções no artigo vinculado para criar um tipo de informação confidencial.</span><span class="sxs-lookup"><span data-stu-id="997b4-172">Follow the instructions in the linked article to create a sensitive information type.</span></span> <span data-ttu-id="997b4-173">Depois de usar o XML, você precisará do identificador de GUID do dicionário para usá-lo.</span><span class="sxs-lookup"><span data-stu-id="997b4-173">Once you have the XML, you'll need the GUID identifier for the dictionary to use it.</span></span>
  
```
<Entity id="9e5382d0-1b6a-42fd-820e-44e0d3b15b6e" patternsProximity="300" recommendedConfidence="75">
    <Pattern confidenceLevel="75">
        <IdMatch idRef=". . ."/>
    </Pattern>
</Entity>
```

<span data-ttu-id="997b4-174">Para obter a identidade do seu dicionário, execute este comando e copie o valor da propriedade **Identity**:</span><span class="sxs-lookup"><span data-stu-id="997b4-174">To get the identity of your dictionary, run this command and copy the **Identity** property value:</span></span> 
  
```
Get-DlpKeywordDictionary -Name "Diseases"
```

<span data-ttu-id="997b4-175">A saída do comando será parecida com o seguinte:</span><span class="sxs-lookup"><span data-stu-id="997b4-175">The output of the command looks like this:</span></span>
  
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

<span data-ttu-id="997b4-p119">Cole a identidade no XML do seu tipo de informação confidencial personalizado e carregue-a. Agora seu dicionário aparecerá na sua lista de tipos de informação confidencial e você poderá usá-lo direto em sua política, especificando o número de palavras-chave necessário para corresponder.</span><span class="sxs-lookup"><span data-stu-id="997b4-p119">Paste the identity into your custom sensitive information type's XML and upload it. Now your dictionary will appear in your list of sensitive information types and you can use it right in your policy, specifying how many keywords are required to match.</span></span>
  
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


