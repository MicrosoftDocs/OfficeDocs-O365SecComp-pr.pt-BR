---
title: Personalizar um tipo de informação confidencial interno
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: 6/25/2018
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Priority
ms.collection: Strat_O365_IP
search.appverid:
- MOE150
- MET150
ms.assetid: 2164ce3d-4d64-4283-b6b1-b81fbe835e8e
description: Ao procurar informações confidenciais no conteúdo, você precisa descrevê-las no que é chamado de regra. A Prevenção contra perda de dados (DLP) inclui regras para os tipos de informações confidenciais mais comuns que você pode usar imediatamente. Para usar essas regras, você precisa incluí-las em uma política. Se quiser ajustar essas regras internas para atender às necessidades específicas da sua organização, basta criar um tipo de informação confidencial personalizado. Este tópico mostra como personalizar o arquivo XML que contém a coleção de regras existente para detectar um intervalo maior de possíveis informações de cartão de crédito.
ms.openlocfilehash: e0a2751ff8d89e664343e91937713af6af74264f
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22523712"
---
# <a name="customize-a-built-in-sensitive-information-type"></a><span data-ttu-id="4d07f-107">Personalizar um tipo de informação confidencial interno</span><span class="sxs-lookup"><span data-stu-id="4d07f-107">Customize a built-in sensitive information type</span></span>

<span data-ttu-id="4d07f-p102">Ao procurar informações confidenciais no conteúdo, você precisa descrevê-las no que é chamado de *regra*. A Prevenção contra perda de dados (DLP) inclui regras para os tipos de informações confidenciais mais comuns que você pode usar imediatamente. Para usar essas regras, você precisa incluí-las em uma política. Se quiser ajustar essas regras internas para atender às necessidades específicas da sua organização, basta criar um tipo de informação confidencial personalizado. Este tópico mostra como personalizar o arquivo XML que contém a coleção de regras existente para detectar um intervalo maior de possíveis informações de cartão de crédito.</span><span class="sxs-lookup"><span data-stu-id="4d07f-p102">When looking for sensitive information in content, you need to describe that information in what's called a  *rule*  . Data loss prevention (DLP) includes rules for the most-common sensitive information types that you can use right away. To use these rules, you have to include them in a policy. You might find that you want to adjust these built-in rules to meet your organization's specific needs, and you can do that by creating a custom sensitive information type. This topic shows you how to customize the XML file that contains the existing rule collection to detect a wider range of potential credit-card information.</span></span> 
  
<span data-ttu-id="4d07f-p103">Você pode aplicar este exemplo a outros tipos internos de informações confidenciais. Confira uma lista de tipos de informações confidenciais padrão e definições de XML em [O que se procura nos tipos de informações confidenciais](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="4d07f-p103">You can take this example and apply it to other built-in sensitive information types. For a list of default sensitive information types and XML definitions, see [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span> 
  
## <a name="export-the-xml-file-of-the-current-rules"></a><span data-ttu-id="4d07f-115">Exportar o arquivo XML das regras atuais</span><span class="sxs-lookup"><span data-stu-id="4d07f-115">Export the XML file of the current rules</span></span>

<span data-ttu-id="4d07f-116">Para exportar o XML, é necessário [conectar-se ao Centro de Conformidade e Segurança por meio do PowerShell Remoto.](https://go.microsoft.com/fwlink/?linkid=799771).</span><span class="sxs-lookup"><span data-stu-id="4d07f-116">To export the XML, you need to [connect to the Security and Compliance Center via Remote PowerShell.](https://go.microsoft.com/fwlink/?linkid=799771).</span></span>
  
1. <span data-ttu-id="4d07f-p104">No PowerShell, digite o seguinte para exibir as regras da sua organização na tela. Se você ainda não criou uma, verá apenas o padrão, as regras internas, rotuladas como "Pacote de Regras da Microsoft".</span><span class="sxs-lookup"><span data-stu-id="4d07f-p104">In the PowerShell, type the following to display your organization's rules on screen. If you haven't created your own, you'll only see the default, built-in rules, labeled "Microsoft Rule Package."</span></span>
    
     `Get-DlpSensitiveInformationTypeRulePackage`
    
2. <span data-ttu-id="4d07f-p105">Armazene as regras da sua organização em uma variável de entrada, digitando o seguinte. Armazenar algo em uma variável o torna facilmente disponível posteriormente em um formato que funciona para comandos remotos do PowerShell.</span><span class="sxs-lookup"><span data-stu-id="4d07f-p105">Store your organization's rules in a in a variable by typing the following. Storing something in a variable makes it easily available later in a format that works for remote PowerShell commands.</span></span>
    
     `$ruleCollections = Get-DlpSensitiveInformationTypeRulePackage`
    
3. <span data-ttu-id="4d07f-p106">Crie um arquivo XML formatado com todos os dados digitando o seguinte. `Set-content` faz parte do cmdlet que grava o XML no arquivo.</span><span class="sxs-lookup"><span data-stu-id="4d07f-p106">Make a formatted XML file with all that data by typing the following. ( `Set-content` is the part of the cmdlet that writes the XML to the file.)</span></span> 
    
     `Set-Content -path "C:\custompath\exportedRules.xml" -Encoding Byte -Value $ruleCollections.SerializedClassificationRuleCollection`
    
    > [!IMPORTANT]
    > <span data-ttu-id="4d07f-p107">Use o local do arquivo onde o pacote de regras está realmente armazenado. `C:\custompath\` é um espaço reservado.</span><span class="sxs-lookup"><span data-stu-id="4d07f-p107">Make sure that you use the file location where your rule pack is actually stored.  `C:\custompath\` is a placeholder.</span></span> 
  
## <a name="find-the-rule-that-you-want-to-modify-in-the-xml"></a><span data-ttu-id="4d07f-125">Localizar a regra que você deseja modificar no XML</span><span class="sxs-lookup"><span data-stu-id="4d07f-125">Find the rule that you want to modify in the XML</span></span>

<span data-ttu-id="4d07f-p108">Os cmdlets acima exportam todo o *conjunto de regras*, que inclui as regras padrão fornecidas. Em seguida, será necessário procurar especificamente a regra de Número do cartão de crédito que você deseja modificar.</span><span class="sxs-lookup"><span data-stu-id="4d07f-p108">The cmdlets above exported the entire  *rule collection*  , which includes the default rules we provide. Next you'll need to look specifically for the Credit Card Number rule that you want to modify.</span></span> 
  
1. <span data-ttu-id="4d07f-128">Use um editor de texto para abrir o arquivo XML exportado na seção anterior.</span><span class="sxs-lookup"><span data-stu-id="4d07f-128">Use a text editor to open the XML file that you exported in the previous section.</span></span>
    
2. <span data-ttu-id="4d07f-p109">Role para baixo até a marca `<Rules>`, que é o início da seção que contém as regras DLP. Como esse arquivo XML contém as informações de toda a coleção de regras, ele contém outras informações na parte superior que você precisa rolar para acessar as regras.</span><span class="sxs-lookup"><span data-stu-id="4d07f-p109">Scroll down to the  `<Rules>` tag, which is the start of the section that contains the DLP rules. (Because this XML file contains the information for the entire rule collection, it contains other information at the top that you need to scroll past to get to the rules.)</span></span> 
    
3. <span data-ttu-id="4d07f-p110">Procure *Func_credit_card* para encontrar a definição de regra de Número do cartão de crédito. No XML, os nomes de regras não podem conter espaços, então geralmente os espaços são substituídos por sublinhados, e às vezes os nomes de regra são abreviados. Um exemplo disto é a regra de números de Previdência Social dos EUA, que é abreviado como "SSN". O XML da regra de Número do cartão de crédito deve parecer com o exemplo a seguir.</span><span class="sxs-lookup"><span data-stu-id="4d07f-p110">Look for  *Func_credit_card*  to find the Credit Card Number rule definition. (In the XML, rule names can't contain spaces, so the spaces are usually replaced with underscores, and rule names are sometimes abbreviated. An example of this is the U.S. Social Security number rule, which is abbreviated "SSN." The Credit Card Number rule XML should look like the following code sample.</span></span> 
    
  ```
  <Entity id="50842eb7-edc8-4019-85dd-5a5c1f2bb085"
         patternsProximity="300" recommendedConfidence="85">
        <Pattern confidenceLevel="85">
         <IdMatch idRef="Func_credit_card" />
          <Any minMatches="1">
            <Match idRef="Keyword_cc_verification" />
            <Match idRef="Keyword_cc_name" />
            <Match idRef="Func_expiration_date" />
          </Any>
        </Pattern>
      </Entity>
  ```

<span data-ttu-id="4d07f-p111">Agora que você localizou a definição de regra de Número do cartão de crédito no XML, é possível personalizar o XML da regra para atender às suas necessidades. Para saber mais sobre as definições de XML, confira o [Glossário de termos](#term-glossary) no final deste tópico.</span><span class="sxs-lookup"><span data-stu-id="4d07f-p111">Now that you have located the Credit Card Number rule definition in the XML, you can customize the rule's XML to meet your needs. (For a refresher on the XML definitions, see the [Term glossary](#term-glossary) at the end of this topic.)</span></span> 
  
## <a name="modify-the-xml-and-create-a-new-sensitive-information-type"></a><span data-ttu-id="4d07f-137">Modificar o XML e criar um novo tipo de informações confidenciais</span><span class="sxs-lookup"><span data-stu-id="4d07f-137">Modify the XML and create a new sensitive information type</span></span>

<span data-ttu-id="4d07f-p112">Primeiro, você precisa criar um novo tipo de informações confidenciais, porque você não pode modificar diretamente as regras padrão. É possível fazer várias coisas com os tipos de informações confidenciais personalizados que são descritos em [Criar um tipo de informação confidencial personalizado](create-a-custom-sensitive-information-type.md). Neste exemplo, vamos manter a simplicidade, remover apenas as evidências comprobatórias e adicionar palavras-chave À regra de Número do cartão de crédito.</span><span class="sxs-lookup"><span data-stu-id="4d07f-p112">First, you need to create a new sensitive information type because you can't directly modify the default rules. You can do a wide variety of things with custom sensitive information types, which are outlined in [Create a custom sensitive information type](create-a-custom-sensitive-information-type.md). For this example, we'll keep it simple and only remove corroborative evidence and add keywords to the Credit Card Number rule.</span></span>
  
<span data-ttu-id="4d07f-p113">Todas as definições de regra XML são criadas no modelo geral a seguir. É necessário copiar e colar o XML da definição de Número do cartão de crédito no modelo, modificar alguns valores (observe os espaços reservados ". . ." no exemplo a seguir) e carregar o XML modificado como uma nova regra que pode ser usada nas políticas.</span><span class="sxs-lookup"><span data-stu-id="4d07f-p113">All XML rule definitions are built on the following general template. You need to copy and paste the Credit Card Number definition XML in the template, modify some values (notice the ". . ." placeholders in the following example), and then upload the modified XML as a new rule that can be used in policies.</span></span>
  
```
<?xml version="1.0" encoding="utf-16"?>
<RulePackage xmlns="http://schemas.microsoft.com/office/2011/mce">
  <RulePack id=". . .">
    <Version major="1" minor="0" build="0" revision="0" />
    <Publisher id=". . ." /> 
    <Details defaultLangCode=". . .">
      <LocalizedDetails langcode=" . . . ">
         <PublisherName>. . .</PublisherName>
         <Name>. . .</Name>
         <Description>. . .</Description>
      </LocalizedDetails>
    </Details>
  </RulePack>
  
 <Rules>
   <!-- Paste the Credit Card Number rule definition here.--> 
      <LocalizedStrings>
         <Resource idRef=". . .">
           <Name default="true" langcode=" . . . ">. . .</Name>
           <Description default="true" langcode=". . ."> . . .</Description>
         </Resource>
      </LocalizedStrings>
   </Rules>
</RulePackage>
```

<span data-ttu-id="4d07f-p114">Agora, você tem algo parecido com o XML a seguir. Como os pacotes de regras e as regras são identificados pelos GUIDs exclusivos, é necessário gerar dois GUIDs: um para o pacote de regras e outro para substituir o GUID da regra de Número do cartão de crédito. O GUID da ID de entidade no exemplo de código a seguir é aquele da definição de regra interna que você precisa substituir por um novo. Há várias maneiras de gerar GUIDs, mas é possível fazer isso com facilidade no PowerShell digitando **[guid]::NewGuid()**.</span><span class="sxs-lookup"><span data-stu-id="4d07f-p114">Now, you have something that looks similar to the following XML. Because rule packages and rules are identified by their unique GUIDs, you need to generate two GUIDs: one for the rule package and one to replace the GUID for the Credit Card Number rule. (The GUID for the entity ID in the following code sample is the one for our built-in rule definition, which you need to replace with a new one.) There are several ways to generate GUIDs, but you can do it easily in PowerShell by typing **[guid]::NewGuid()**.</span></span> 
  
```
<?xml version="1.0" encoding="utf-16"?>
<RulePackage xmlns="http://schemas.microsoft.com/office/2011/mce">
  <RulePack id="8aac8390-e99f-4487-8d16-7f0cdee8defc">
    <Version major="1" minor="0" build="0" revision="0" />
    <Publisher id="8d34806e-cd65-4178-ba0e-5d7d712e5b66" />
    <Details defaultLangCode="en">
      <LocalizedDetails langcode="en">
        <PublisherName>Contoso Ltd.</PublisherName>
        <Name>Financial Information</Name>
        <Description>Modified versions of the Microsoft rule package</Description>
      </LocalizedDetails>
    </Details>
  </RulePack>
  
 <Rules>
    <Entity id="db80b3da-0056-436e-b0ca-1f4cf7080d1f"
       patternsProximity="300" recommendedConfidence="85">
      <Pattern confidenceLevel="85">
        <IdMatch idRef="Func_credit_card" />
        <Any minMatches="1">
          <Match idRef="Keyword_cc_verification" />
          <Match idRef="Keyword_cc_name" />
          <Match idRef="Func_expiration_date" />
        </Any>
      </Pattern>
    </Entity>
      <LocalizedStrings>
         <Resource idRef="db80b3da-0056-436e-b0ca-1f4cf7080d1f"> 
<!-- This is the GUID for the preceding Credit Card Number entity because the following text is for that Entity. -->
           <Name default="true" langcode="en-us">Modified Credit Card Number</Name>
           <Description default="true" langcode="en-us">Credit Card Number that looks for additional keywords, and another version of Credit Card Number that doesn't require keywords (but has a lower confidence level)</Description>
         </Resource>
      </LocalizedStrings>
   </Rules>
</RulePackage>
```

## <a name="remove-the-corroborative-evidence-requirement-from-a-sensitive-information-type"></a><span data-ttu-id="4d07f-149">Remover o requisito de evidências comprobatórias de um tipo de informação confidencial</span><span class="sxs-lookup"><span data-stu-id="4d07f-149">Remove the corroborative evidence requirement from a sensitive information type</span></span>

<span data-ttu-id="4d07f-p115">Agora que você tem um novo tipo de informação confidencial para carregar no Centro de Conformidade e Segurança, a próxima etapa é tornar a regra mais específica. Modifique-a para que procure apenas um número de 16 dígitos que passe na soma de verificação, mas não exija evidências adicionais (comprobatórias, como palavras-chave). Para isso, você precisa remover a parte do XML que procura evidências comprobatórias. A evidência comprobatória é muito útil para reduzir falsos positivos porque normalmente há determinadas palavras-chave ou uma data de vencimento próxima do número de cartão de crédito. Se você remover essa evidência, também deverá ajustar o quanto de certeza você tem de que encontrou um número de cartão de crédito, ao reduzir o `confidenceLevel`, que é 85 no exemplo.</span><span class="sxs-lookup"><span data-stu-id="4d07f-p115">Now that you have a new sensitive information type that you're able to upload to the Security &amp; Compliance Center, the next step is to make the rule more specific. Modify the rule so that it only looks for a 16-digit number that passes the checksum but doesn't require additional (corroborative) evidence (for example keywords). To do this, you need to remove the part of the XML that looks for corroborative evidence. Corroborative evidence is very helpful in reducing false positives because usually there are certain keywords or an expiration date near the credit card number. If you remove that evidence, you should also adjust how confident you are that you found a credit card number by lowering the  `confidenceLevel`, which is 85 in the example.</span></span>
  
```
<Entity id="db80b3da-0056-436e-b0ca-1f4cf7080d1f" patternsProximity="300"
      <Pattern confidenceLevel="85">
        <IdMatch idRef="Func_credit_card" />
      </Pattern>
    </Entity>
```

## <a name="look-for-keywords-that-are-specific-to-your-organization"></a><span data-ttu-id="4d07f-155">Procurar palavras-chave específicas da sua organização</span><span class="sxs-lookup"><span data-stu-id="4d07f-155">Look for keywords that are specific to your organization</span></span>

<span data-ttu-id="4d07f-p116">Talvez você queira exigir evidência comprobatória, mas precise de palavras-chave diferentes ou adicionais, e pode ser que você queira alterar onde procurar essa evidência. Você pode ajustar a `patternsProximity` para expandir ou reduzir a janela de evidência comprobatória para aproximadamente 16 dígitos. Para adicionar as próprias palavras-chave, você precisa definir uma lista de palavras-chave e fazer referência a ela na regra. O XML a seguir adiciona as palavras-chave "cartão da empresa" e "Cartão Contoso" de modo que qualquer mensagem que contenha essas frases em até 150 caracteres de um número de cartão de crédito seja identificada como um número de cartão de crédito.</span><span class="sxs-lookup"><span data-stu-id="4d07f-p116">You might want to require corroborative evidence but want different or additional keywords, and perhaps you want to change where to look for that evidence. You can adjust the  `patternsProximity` to expand or shrink the window for corroborative evidence around the 16-digit number. To add your own keywords, you need to define a keyword list and reference it within your rule. The following XML adds the keywords "company card" and "Contoso card" so that any message that contains those phrases within 150 characters of a credit card number will be identified as a credit card number.</span></span> 
  
```
<Rules>
<! -- Modify the patternsProximity to be "150" rather than "300." -->
    <Entity id="db80b3da-0056-436e-b0ca-1f4cf7080d1f" patternsProximity="150" recommendedConfidence="85">
      <Pattern confidenceLevel="85">
        <IdMatch idRef="Func_credit_card" />
        <Any minMatches="1">
          <Match idRef="Keyword_cc_verification" />
          <Match idRef="Keyword_cc_name" />
<!-- Add the following XML, which references the keywords at the end of the XML sample. -->
          <Match idRef="My_Additional_Keywords" />
          <Match idRef="Func_expiration_date" />
        </Any>
      </Pattern>
    </Entity>
<!-- Add the following XML, and update the information inside the <Term> tags with the keywords that you want to detect. -->
    <Keyword id="My_Additional_Keywords">
      <Group matchStyle="word">
        <Term caseSensitive="false">company card</Term>
        <Term caseSensitive="false">Contoso card</Term>
      </Group>
    </Keyword>
```

## <a name="upload-your-rule"></a><span data-ttu-id="4d07f-160">Carregar a regra</span><span class="sxs-lookup"><span data-stu-id="4d07f-160">Upload your rule</span></span>

<span data-ttu-id="4d07f-161">Para carregar a regra, é necessário fazer o seguinte.</span><span class="sxs-lookup"><span data-stu-id="4d07f-161">To upload your rule, you need to do the following.</span></span>
  
1. <span data-ttu-id="4d07f-p117">Salve como um arquivo .xml com codificação Unicode. Isso é importante porque a regra não funcionará se o arquivo for salvo com uma codificação diferente.</span><span class="sxs-lookup"><span data-stu-id="4d07f-p117">Save it as an .xml file with Unicode encoding. This is important because the rule won't work if the file is saved with a different encoding.</span></span>
    
2. [<span data-ttu-id="4d07f-164">Conecte-se ao Centro de Conformidade e Segurança usando o PowerShell Remoto.</span><span class="sxs-lookup"><span data-stu-id="4d07f-164">Connect to the Security and Compliance Center via Remote PowerShell.</span></span>](https://go.microsoft.com/fwlink/?linkid=799771)
    
3. <span data-ttu-id="4d07f-165">No PowerShell, digite o seguinte.</span><span class="sxs-lookup"><span data-stu-id="4d07f-165">In the PowerShell command prompt, type the following:</span></span>
    
     <span data-ttu-id="4d07f-166">`New-DlpSensitiveInformationTypeRulePackage -FileData (Get-Content -Path "C:\custompath\MyNewRulePack.xml" -Encoding Byte)`.</span><span class="sxs-lookup"><span data-stu-id="4d07f-166"></span></span>
    
    > [!IMPORTANT]
    > <span data-ttu-id="4d07f-p118">Use o local do arquivo onde o pacote de regras está realmente armazenado. `C:\custompath\` é um espaço reservado.</span><span class="sxs-lookup"><span data-stu-id="4d07f-p118">Make sure that you use the file location where your rule pack is actually stored.  `C:\custompath\` is a placeholder.</span></span> 
  
4. <span data-ttu-id="4d07f-169">Para confirmar, digite S e pressione **Enter**.</span><span class="sxs-lookup"><span data-stu-id="4d07f-169">To confirm, type Y, and then press **Enter**.</span></span>
    
5. <span data-ttu-id="4d07f-170">Verifique se a nova regra foi carregada, digitando `Get-DlpSensitiveInformationType`, que agora exibe o nome da regra.</span><span class="sxs-lookup"><span data-stu-id="4d07f-170">Verify that your new rule was uploaded by typing  `Get-DlpSensitiveInformationType`, which now displays the name of your rule.</span></span>
    
<span data-ttu-id="4d07f-p119">Para começar a usar a nova regra para detectar informações confidenciais, é necessário adicionar a regra a uma política DLP. Saiba como adicionar a regra a uma política em [Criar uma política DLP a partir de um modelo](create-a-dlp-policy-from-a-template.md).</span><span class="sxs-lookup"><span data-stu-id="4d07f-p119">To start using the new rule to detect sensitive information, you need to add the rule to a DLP policy. To learn how to add the rule to a policy, see [Create a DLP policy from a template](create-a-dlp-policy-from-a-template.md).</span></span>
  
## <a name="term-glossary"></a><span data-ttu-id="4d07f-173">Glossário de termos</span><span class="sxs-lookup"><span data-stu-id="4d07f-173">Term glossary</span></span>

<span data-ttu-id="4d07f-174">Estas são as definições dos termos encontrados durante este procedimento.</span><span class="sxs-lookup"><span data-stu-id="4d07f-174">These are the definitions for the terms you encountered during this procedure.</span></span>
  
|<span data-ttu-id="4d07f-175">**Termo**</span><span class="sxs-lookup"><span data-stu-id="4d07f-175">**Term**</span></span>|<span data-ttu-id="4d07f-176">**Definição**</span><span class="sxs-lookup"><span data-stu-id="4d07f-176">**Definition**</span></span>|
|:-----|:-----|
|<span data-ttu-id="4d07f-177">Entidade</span><span class="sxs-lookup"><span data-stu-id="4d07f-177">Entity</span></span>  <br/> |<span data-ttu-id="4d07f-p120">Entidades são o que chamamos de tipos de informações confidenciais, como os números de cartão de crédito. Cada entidade tem um GUID exclusivo como ID. Quando você copia um GUID e pesquisa por ele no XML, encontra a definição de regra XML e todas as traduções localizadas dessa regra XML. Também é possível encontrar essa definição localizando o GUID para a tradução e depois pesquisando por este GUID.</span><span class="sxs-lookup"><span data-stu-id="4d07f-p120">Entities are what we call sensitive information types, such as credit card numbers. Each entity has a unique GUID as its ID. If you copy a GUID and search for it in the XML, you'll find the XML rule definition and all the localized translations of that XML rule. You can also find this definition by locating the GUID for the translation and then searching for that GUID.</span></span>  <br/> |
|<span data-ttu-id="4d07f-182">Funções</span><span class="sxs-lookup"><span data-stu-id="4d07f-182">Functions</span></span>  <br/> |<span data-ttu-id="4d07f-p121">As referências `Func_credit_card` do arquivo XML são uma função no código compilado. Funções são usadas para executar expressões regulares complexas e confirmam se as somas de verificação correspondem às nossas regras internas. Como isso ocorre no código, algumas das variáveis não aparecem no arquivo XML.  </span><span class="sxs-lookup"><span data-stu-id="4d07f-p121">The XML file references  `Func_credit_card`, which is a function in compiled code. Functions are used to run complex regexes and verify that checksums match for our built-in rules.) Because this happens in the code, some of the variables don't appear in the XML file.  </span></span><br/> |
|<span data-ttu-id="4d07f-185">IdMatch</span><span class="sxs-lookup"><span data-stu-id="4d07f-185">IdMatch idRef=Regex_email_address</span></span>  <br/> |<span data-ttu-id="4d07f-p122">É com esse identificador que o padrão está tentando fazer a correspondência, por exemplo, com um número de cartão de crédito. Saiba mais sobre isso e sobre as marcas `Match` em [Regras de entidades](https://support.office.com/article/c4ab8707-0839-4855-9390-3dbcb43475a7.aspx#dlp-entity).  </span><span class="sxs-lookup"><span data-stu-id="4d07f-p122">This is the identifier that the pattern is to trying to match—for example, a credit card number. You can read more about this and about the  `Match` tags in [Entity rules](https://support.office.com/article/c4ab8707-0839-4855-9390-3dbcb43475a7.aspx#dlp-entity).  </span></span><br/> |
|<span data-ttu-id="4d07f-188">Lista de palavras-chave</span><span class="sxs-lookup"><span data-stu-id="4d07f-188">Keyword lists</span></span>  <br/> |<span data-ttu-id="4d07f-p123">O arquivo XML também faz referência a `keyword_cc_verification` e a `keyword_cc_name`, que são listas de palavras-chave, nas quais procuramos por correspondência em `patternsProximity` com a entidade. Atualmente elas não são exibidas no XML.  </span><span class="sxs-lookup"><span data-stu-id="4d07f-p123">The XML file also references  `keyword_cc_verification` and  `keyword_cc_name`, which are lists of keywords from which we are looking for matches within the  `patternsProximity` for the entity. These aren't currently displayed in the XML.  </span></span><br/> |
|<span data-ttu-id="4d07f-191">Padrão</span><span class="sxs-lookup"><span data-stu-id="4d07f-191">Pattern</span></span>  <br/> |<span data-ttu-id="4d07f-p124">O padrão contém a lista daquilo que o tipo confidencial está procurando, o que inclui expressões regulares, palavras-chave e funções internas (que realizam tarefas como verificar as somas de verificação). Os tipos de informações confidenciais podem ter vários padrões com confianças exclusivas, o que é útil na criação de um tipo de informações confidenciais que retornará uma confiança alta se a evidência comprobatória for encontrada e uma confiança baixa se pouca ou nenhuma evidência comprobatória for encontrada.</span><span class="sxs-lookup"><span data-stu-id="4d07f-p124">The pattern contains the list of what the sensitive type is looking for. This includes keywords, regexes, and internal functions (that perform tasks like verifying checksums). Sensitive information types can have multiple patterns with unique confidences. This is useful when creating a sensitive information type that returns a high confidence if corroborative evidence is found and a lower confidence if little or no corroborative evidence is found.</span></span>  <br/> |
|<span data-ttu-id="4d07f-196">confidenceLevel padrão</span><span class="sxs-lookup"><span data-stu-id="4d07f-196">Pattern confidenceLevel</span></span>  <br/> |<span data-ttu-id="4d07f-p125">Esse é o nível de confiança que o mecanismo de DLP encontrou na correspondência. Esse nível de confiança está associado a uma correspondência para o padrão se os requisitos do padrão são atendidos. Essa é a medida de confiança que deve ser considerada ao usar as regras de transporte do Exchange (ETRs).</span><span class="sxs-lookup"><span data-stu-id="4d07f-p125">This is the level of confidence that the DLP engine found a match. This level of confidence is associated with a match for the pattern if the pattern's requirements are met. This is the confidence measure you should consider when using Exchange transport rules (ETRs).</span></span>  <br/> |
|<span data-ttu-id="4d07f-200">patternsProximity</span><span class="sxs-lookup"><span data-stu-id="4d07f-200">patternsProximity</span></span>  <br/> |<span data-ttu-id="4d07f-201">Quando encontramos algo que parece um padrão de número de cartão de crédito, o `patternsProximity` é a proximidade em torno desse número, onde procuraremos evidências corroborativas.</span><span class="sxs-lookup"><span data-stu-id="4d07f-201">When we find what looks like a credit card number pattern,  `patternsProximity` is the proximity around that number where we'll look for corroborative evidence.</span></span>  <br/> |
|<span data-ttu-id="4d07f-202">recommendedConfidence</span><span class="sxs-lookup"><span data-stu-id="4d07f-202">recommendedConfidence</span></span>  <br/> |<span data-ttu-id="4d07f-p126">Esse é o nível de confiança recomendável para esta regra. A confiança recomendada se aplica às entidades e afinidades. Para entidades, esse número nunca é avaliado em relação ao `confidenceLevel` do padrão. É simplesmente uma sugestão para ajudá-lo a escolher um nível de confiança, caso deseje usar um. Com afinidades, o `confidenceLevel` do padrão deve ser maior do que o número de `recommendedConfidence` para uma ação ETR ser chamada. A `recommendedConfidence` é o nível de confiança padrão usado em ETRs que chamam uma ação. Se quiser, é possível alterar manualmente o ETR que será chamado com base no nível de confiança do padrão.  </span><span class="sxs-lookup"><span data-stu-id="4d07f-p126">This is the confidence level we recommend for this rule. The recommended confidence applies to entities and affinities. For entities, this number is never evaluated against the  `confidenceLevel` for the pattern. It's merely a suggestion to help you choose a confidence level if you want to apply one. For affinities, the  `confidenceLevel` of the pattern must be higher than the  `recommendedConfidence` number for an ETR action to be invoked. The  `recommendedConfidence` is the default confidence level used in ETRs that invokes an action. If you want, you can manually change the ETR to be invoked based off the pattern's confidence level, instead.  </span></span><br/> |
   
## <a name="for-more-information"></a><span data-ttu-id="4d07f-210">Para saber mais</span><span class="sxs-lookup"><span data-stu-id="4d07f-210">For more information</span></span>

- [<span data-ttu-id="4d07f-211">O que os tipos de informações confidenciais procuram</span><span class="sxs-lookup"><span data-stu-id="4d07f-211">What the sensitive information types look for</span></span>](what-the-sensitive-information-types-look-for.md)
    
- [<span data-ttu-id="4d07f-212">Criar um tipo de informação confidencial personalizado</span><span class="sxs-lookup"><span data-stu-id="4d07f-212">Create a custom sensitive information type</span></span>](create-a-custom-sensitive-information-type.md)
    
- [<span data-ttu-id="4d07f-213">Visão geral das políticas de prevenção contra perda de dados</span><span class="sxs-lookup"><span data-stu-id="4d07f-213">Overview of data loss prevention policies</span></span>](data-loss-prevention-policies.md)
    
