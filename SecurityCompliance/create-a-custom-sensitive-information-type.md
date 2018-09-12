---
title: Criar um tipo de informação confidencial personalizado
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: 10/5/2017
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Priority
ms.collection: Strat_O365_IP
search.appverid:
- MOE150
- MET150
ms.assetid: 82c382a5-b6db-44fd-995d-b333b3c7fc30
description: Se você precisa identificar e proteger um tipo diferente de informações confidenciais, como uma ID de funcionário que usa um formato específico para sua organização, poderá criar um tipo personalizado de informações confidenciais. Um tipo de informação confidencial é definido em um arquivo XML chamado de pacote de regras. Este tópico mostra como criar um arquivo XML que define seu próprio tipo personalizado de informações confidenciais. Você precisa saber criar uma expressão regular.
ms.openlocfilehash: 56683dd8ceac286f79084d2c2f19f48f5849a02f
ms.sourcegitcommit: 4be502d1fc6cbaef4c72d599758d51efe3a173c9
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/06/2018
ms.locfileid: "23849424"
---
# <a name="create-a-custom-sensitive-information-type"></a>Criar um tipo de informação confidencial personalizado

A Prevenção contra perda de dados (DLP) no Office 365 inclui vários [tipos de informações confidenciais](what-the-sensitive-information-types-look-for.md) que estão prontos para usar nas suas políticas DLP. Esses tipos internos podem ajudar a identificar e proteger números de cartão de crédito, números de contas bancárias, números de passaporte e muito mais. 
  
Mas, se você precisa identificar e proteger um tipo diferente de informações confidenciais, como uma ID de funcionário que usa um formato específico para sua organização, poderá criar um tipo personalizado de informações confidenciais. Um tipo de informação confidencial é definido em um arquivo XML chamado de pacote de regras.
  
Este tópico mostra como criar um arquivo XML que define seu próprio tipo personalizado de informações confidenciais. Você precisa saber criar uma expressão regular. Como exemplo, este tópico cria um tipo personalizado de informações confidenciais que identifica uma ID de funcionário. Você pode usar esse XML de exemplo como ponto de partida para seu próprio arquivo XML.
  
Depois de criar um arquivo XML bem formado, você poderá carregá-lo para o Office 365 usando o PowerShell. Você estará pronto para usar seu tipo personalizado de informações confidenciais nas suas políticas DLP e testar se ele está detectando as informações confidenciais conforme o planejado.

## <a name="important-disclaimer"></a>Aviso de isenção de responsabilidade importante

Devido às variações nos ambientes do cliente e nos requisitos de correspondência de conteúdo, o Suporte da Microsoft não pode ajudar no fornecimento de definições de correspondência de conteúdo personalizado; por exemplo, definindo classificações personalizadas ou padrões de expressões regulares ("RegEx"). Para desenvolvimento, teste e depuração de correspondência de conteúdo personalizado, os clientes do Office 365 devem contar com recursos de TI internos ou usar um recurso de consultoria externo, como os Serviços de Consultoria Microsoft. Os engenheiros de suporte podem fornecer suporte limitado para o recurso, mas não podem garantir que o desenvolvimento de correspondência de conteúdo personalizado atenda aos requisitos ou à conformidade do cliente. Como exemplo do tipo de auxílio disponível, o suporte pode fornecer padrões de expressões regulares de amostra para fins de teste ou ajudar na solução de um padrão RegEx existente, que não esteja sendo acionado como esperado, com um único exemplo de conteúdo específico.

 Para saber mais sobre o mecanismo de RegEx do .NET usado para processamento de texto, confira a documentação sobre [Expressões regulares no .NET](https://docs.microsoft.com/pt-BR/dotnet/standard/base-types/regular-expressions).
    
## <a name="sample-xml-of-a-rule-package"></a>XML de exemplo de um pacote de regras

Eis um XML de exemplo do pacote de regras que criaremos neste tópico. Os elementos e os atributos são explicados nas seções abaixo.
  
```
<?xml version="1.0" encoding="UTF-16"?>
<RulePackage xmlns="http://schemas.microsoft.com/office/2011/mce">
<RulePack id="DAD86A92-AB18-43BB-AB35-96F7C594ADAA">
    <Version build="0" major="1" minor="0" revision="0"/>
    <Publisher id="619DD8C3-7B80-4998-A312-4DF0402BAC04"/>
    <Details defaultLangCode="en-us">
        <LocalizedDetails langcode="en-us">
            <PublisherName>Contoso</PublisherName>
            <Name>Employee ID Custom Rule Pack</Name>
            <Description>
            This rule package contains the custom Employee ID entity.
            </Description>
        </LocalizedDetails>
    </Details>
</RulePack>
<Rules>
<!-- Employee ID -->
    <Entity id="E1CC861E-3FE9-4A58-82DF-4BD259EAB378" patternsProximity="300" recommendedConfidence="70">
        <Pattern confidenceLevel="60">
            <IdMatch idRef="Regex_employee_id"/>
        </Pattern>
        <Pattern confidenceLevel="70">
            <IdMatch idRef="Regex_employee_id"/>
            <Match idRef="Func_us_date"/>
        </Pattern>
        <Pattern confidenceLevel="80">
            <IdMatch idRef="Regex_employee_id"/>
            <Match idRef="Func_us_date"/>
            <Any minMatches="1">
                <Match idRef="Keyword_badge" minCount="2"/>
                <Match idRef="Keyword_employee"/>
            </Any>
            <Any minMatches="0" maxMatches="0">
                <Match idRef="Keyword_false_positives_local"/>
                <Match idRef="Keyword_false_positives_intl"/>
            </Any>
        </Pattern>
    </Entity>
    <Regex id="Regex_employee_id">(\s)(\d{9})(\s)</Regex>
    <Keyword id="Keyword_employee">
        <Group matchStyle="word">
            <Term>Identification</Term>
            <Term>Contoso Employee</Term>
        </Group>
    </Keyword>
    <Keyword id="Keyword_badge">
        <Group matchStyle="string">
            <Term>card</Term>
            <Term>badge</Term>
            <Term caseSensitive="true">ID</Term>
        </Group>
    </Keyword>
    <Keyword id="Keyword_false_positives_local">
        <Group matchStyle="word">
            <Term>credit card</Term>
            <Term>national ID</Term>
        </Group>
    </Keyword>
    <Keyword id="Keyword_false_positives_intl">
        <Group matchStyle="word">
            <Term>identity card</Term>
            <Term>national ID</Term>
            <Term>EU debit card</Term>
        </Group>
    </Keyword>
    <LocalizedStrings>
        <Resource idRef="E1CC861E-3FE9-4A58-82DF-4BD259EAB378">
            <Name default="true" langcode="en-us">Employee ID</Name>
            <Description default="true" langcode="en-us">
            A custom classification for detecting Employee IDs.
            </Description>
            <Name default="true" langcode="de-de">Name for German locale</Name>
            <Description default="true" langcode="de-de">
            Description for German locale.
            </Description>
        </Resource>
    </LocalizedStrings>
</Rules>
</RulePackage>

```

## <a name="what-are-your-key-requirements-rule-entity-pattern-elements"></a>Quais são seus principais requisitos? [elementos Rule, Entity, Pattern]

Antes de começar, é importante compreender a estrutura básica do esquema XML para uma regra e como você pode usar essa estrutura para definir seu tipo personalizado de informações confidenciais para que ele identifique o conteúdo certo.
  
Uma regra define uma ou mais entidades (tipos de informações confidenciais) e cada entidade define um ou mais padrões. Um padrão é o que a DLP procura ao avaliar conteúdo como emails e documentos.
  
(Uma breve observação sobre a terminologia: se você estiver familiarizado com as políticas DLP, saberá que uma política contém uma ou mais regras formadas por condições e ações. No entanto, neste tópico, a marcação XML usa regras para significar os padrões que definem uma entidade, também conhecido como tipo de informação confidencial. Neste tópico, ao ver uma regra, pense em entidade ou tipo de informação confidencial e não em condições e ações.)
  
### <a name="simplest-scenario-entity-with-one-pattern"></a>Cenário mais simples: entidade com um padrão

Aqui está o cenário mais simples. Você quer que sua política DLP identifique conteúdo que inclua a ID de funcionário da sua organização, com o formato de um número de nove dígitos. Assim, o padrão faz referência a uma expressão regular contida na regra que identifica números de nove dígitos. Qualquer conteúdo que contiver um número de nove dígitos corresponderá a esse padrão.
  
![Diagrama de entidade com um padrão](media/4cc82dcf-068f-43ff-99b2-bac3892e9819.png)
  
No entanto, embora seja simples, esse padrão poderá identificar muitos falsos positivos combinando conteúdo que contém qualquer número de nove dígitos que não seja necessariamente uma ID de funcionário.
  
### <a name="more-common-scenario-entity-with-multiple-patterns"></a>Cenário mais comum: entidade com vários padrões

Por esse motivo, é mais comum definir uma entidade usando mais de um padrão, em que os padrões identificam evidências de suporte (como uma palavra-chave ou data) além da entidade (como um número de nove dígitos).
  
Por exemplo, para aumentar as chances de identificar o conteúdo com uma ID de funcionário, você poderá definir outro padrão que também identifica a data de contratação ou definir outro padrão que identifica a data de contratação e uma palavra-chave (como "ID do funcionário"), além do número de nove dígitos.
  
![Diagrama de entidade com vários padrões](media/c8dc2c9d-00c6-4ebc-889a-53b41a90024a.png)
  
Observe alguns aspectos importantes dessa estrutura:
  
- Os padrões que exigem mais evidência têm maior nível de confiança. Isso é útil porque, quando você usa esse tipo de informação confidencial em uma política DLP, pode usar ações mais restritivas (como bloquear conteúdo) com apenas as correspondências de maior confiança e poderá usar ações menos restritivas (como enviar notificação) com correspondências de menor confiança.
    
- Os elementos IdMatch e Match de suporte fazem referência a expressões regulares e palavras-chave que são na verdade filhas do elemento Rule, não o Pattern. Esses elementos de suporte são referenciados pelo Pattern, mas incluídos na Rule. Isso significa que uma única definição de um elemento de suporte, como uma expressão regular ou uma lista de palavras-chave, pode ser referenciada por várias entidades e padrões.
    
## <a name="what-entity-do-you-need-to-identify-entity-element-id-attribute"></a>De que entidade você precisa para identificar? [elemento Entity, atributo de id]

Uma entidade é um tipo de informação confidencial, como um número de cartão de crédito, que tem um padrão bem definido. Cada entidade tem um GUID exclusivo como sua ID.
  
### <a name="name-the-entity-and-generate-its-guid"></a>Nomear a entidade e gerar seu GUID

Adicione elementos Rules e Entity. Em seguida, adicione um comentário que contém o nome da sua entidade personalizada. Neste exemplo, ID do funcionário. Posteriormente, você adicionará o nome da entidade à seção de cadeias de caracteres localizadas, e esse nome será exibido na interface de usuário quando você criar uma política DLP.
  
Em seguida, gere um GUID para a sua entidade. Há várias maneiras de gerar GUIDs, mas você pode fazer isso facilmente no PowerShell digitando [guid]::NewGuid(). Mais tarde, você também adicionará a GUID de entidade à seção de cadeias de caracteres localizadas.
  
![Marcação XML mostrando os elementos Rules e Entity](media/c46c0209-0947-44e0-ac3a-8fd5209a81aa.png)
  
## <a name="what-pattern-do-you-want-to-match-pattern-element-idmatch-element-regex-element"></a>Que padrão você deseja corresponder? [elemento Pattern, elemento IdMatch, elemento Regex]

O padrão contém a lista do que o tipo de informação confidencial está procurando. Isso pode incluir expressões regulares, palavras-chave e funções internas (que realizam tarefas como executar expressões regulares para localizar datas ou endereços). Os tipos de informações confidenciais podem ter vários padrões com confianças exclusivas.
  
O que todos os padrões abaixo têm em comum é que eles fazem referência à mesma expressão regular, que procura um número de nove dígitos (\d{9}) delimitado por espaço em branco (\s)... (\s). Essa expressão regular é referenciada pelo elemento IdMatch e é o requisito comum de todos os padrões que procuram a entidade ID do funcionário. IdMatch é o identificador que o padrão está tentando corresponder, como número de cartão de crédito ou ID do funcionário ou número da previdência social. Um elemento Pattern deve ter exatamente um elemento IdMatch.
  
![Marcação XML mostrando vários elementos Pattern fazendo referência a um único elemento Regex](media/8f3f497b-3b8b-4bad-9c6a-d9abf0520854.png)
  
Quando satisfeito, um padrão retorna uma contagem e um nível de confiança, que você pode usar nas condições da sua política DLP. Quando você adiciona uma condição para detectar um tipo de informação confidencial a uma política DLP, você pode editar a contagem e o nível de confiança como mostrado aqui. O nível de confiança (também chamado de precisão de correspondência) é explicado mais adiante neste tópico.
  
![Contagem de instâncias e opções de precisão de correspondência](media/11d0b51e-7c3f-4cc6-96d8-b29bcdae1aeb.png)
  
Ao criar sua expressão regular, lembre-se de que há possíveis problemas a serem considerados. Por exemplo, se você escrever e carregar uma expressão regular que identifica conteúdo demais, isso poderá afetar o desempenho. Para saber mais sobre esses possíveis problemas, confira a seção posterior [Possíveis problemas de validação a serem considerados](#potential-validation-issues-to-be-aware-of).
  
## <a name="do-you-want-to-require-additional-evidence-match-element-mincount-attribute"></a>Você deseja exigir evidências adicionais? [elemento Match, atributo minCount]

Além de IdMatch, um padrão pode usar o elemento Match para exigir evidências adicionais, como uma palavra-chave, expressão regular, data ou endereço.
  
Um padrão pode incluir vários elementos Match; eles podem ser incluídos diretamente no elemento Pattern ou combinados usando o elemento Any. Os elementos Match são unidos por um operador AND implícito; todos os elementos Match devem ser satisfeitos para que o padrão seja correspondido. Você pode usar o elemento Any para introduzir os operadores AND ou OR (veja mais sobre isso em uma seção posterior).
  
Você pode usar o atributo opcional minCount para especificar quantas instâncias de uma correspondência precisam ser encontradas para cada um dos elementos Match. Por exemplo, você pode especificar que um padrão apenas será satisfeito quando pelo menos duas palavras-chave de uma lista de palavra-chave forem encontradas.
  
![Marcação XML mostrando o elemento Match com o atributo minOccurs](media/607f6b5e-2c7d-43a5-a131-a649f122e15a.png)
  
### <a name="keywords-keyword-group-and-term-elements-matchstyle-and-casesensitive-attributes"></a>Palavras-chave [elementos Keyword, Group e Term, atributos matchStyle e caseSensitive]

Ao identificar informações confidenciais, como uma ID de funcionário, muitas vezes você deseja exigir palavras-chave como evidências comprobatórias. Por exemplo, além de corresponder a um número de nove dígitos, talvez você queira procurar palavras como "cartão", "crachá" ou "ID". Para fazer isso, use o elemento Keyword. O elemento Keyword tem um atributo id que pode ser referenciado por vários elementos Match em vários padrões ou entidades.
  
Palavras-chave são incluídas como uma lista de elementos Term em um elemento Group. O elemento Group tem um atributo matchStyle com dois valores possíveis:
  
- **matchStyle="word"** A correspondência por palavra identifica palavras inteiras delimitadas por espaços em branco ou outros delimitadores. Você sempre deve usar palavra, a menos que precise corresponder partes de palavras ou corresponder palavras em idiomas asiáticos. 
    
- **matchStyle="string"** A correspondência por cadeia de caracteres identifica cadeias de caracteres independentemente do que está em volta. Por exemplo, "id" terá correspondência com "cidade" e "ideia". Use cadeia de caracteres somente quando precisar corresponder palavras asiáticas ou se a palavra-chave puder ser incluída como parte de outras cadeias de caracteres. 
    
Por fim, você pode usar o atributo caseSensitive do elemento Term para especificar que o conteúdo deve corresponder à palavra-chave exatamente, incluindo letras minúsculas e maiúsculas.
  
![Marcação XML mostrando elementos Match fazendo referência a palavras-chave](media/e729ba27-dec6-46f4-9242-584c6c12fd85.png)
  
### <a name="regular-expressions-regex-element"></a>Expressões regulares [elemento Regex]

Neste exemplo, a entidade ID do funcionário já usa o elemento IdMatch para fazer referência a uma expressão regular para o padrão, um número de nove dígitos delimitado por espaços em branco. Além disso, um padrão pode usar um elemento Match para fazer referência a um elemento Regex adicional a fim de identificar evidências comprobatórias, como um número de cinco ou nove dígitos no formato de um código postal americano.
  
### <a name="additional-patterns-such-as-dates-or-addresses-built-in-functions"></a>Padrões adicionais, como datas ou endereços [funções internas]

Além dos tipos internos de informações confidenciais, a DLP também inclui funções internas capazes de identificar evidências comprobatórias, como uma data dos EUA, data da UE, data de vencimento ou um endereço nos EUA. A DLP não dá suporte ao carregamento de suas próprias funções personalizadas, mas quando você cria um tipo personalizado de informações confidenciais, sua entidade poderá fazer referência às funções internas.
  
Por exemplo, um crachá de ID do funcionário tem uma data de contratação; portanto, essa entidade personalizada pode usar a função interna `Func_us_date` para identificar uma data no formato comumente utilizado nos EUA. 
  
Para saber mais, confira [O que as funções DLP procuram](what-the-dlp-functions-look-for.md).
  
![Marcação XML mostrando elementos Match fazendo referência a funções internas](media/dac6eae3-9c52-4537-b984-f9f127cc9c33.png)
  
## <a name="different-combinations-of-evidence-any-element-minmatches-and-maxmatches-attributes"></a>Diferentes combinações de evidências [elemento Any, atributos minMatches e maxMatches]

Em um elemento Pattern, todos os elementos IdMatch e Match são unidos por um operador AND implícito, todas as correspondências devem ser satisfeitas para que o padrão possa ser satisfeito. No entanto, você pode criar a lógica de correspondência mais flexível usando o elemento Any para agrupar elementos Match. Por exemplo, você pode usar o elemento Any para corresponder a todos, nenhum ou um subconjunto exato de seus elementos Match filhos.
  
O elemento Any tem atributos opcionais minMatches e maxMatches que você pode usar para definir quantos elementos Match filhos devem ser satisfeitos para que esse padrão seja correspondido. Observe que esses atributos definem o número de elementos Match que devem ser satisfeitos, e não o número de instâncias de evidências encontradas para as correspondências. Para definir um número mínimo de instâncias para uma correspondência específica, como duas palavras-chave de uma lista, use o atributo minCount para um elemento Match (veja acima).
  
### <a name="match-at-least-one-child-match-element"></a>Corresponder pelo menos um elemento Match filho

Se você quiser exigir que apenas um número mínimo de elementos Match seja atendido, use o atributo minMatches. De fato, esses elementos Match são unidos por um operador OR implícito. Esse elemento Any será satisfeito se uma data no formato dos EUA ou uma palavra-chave de ambas as listas for encontrada.
  
![Marcação XML mostrando o elemento Any com o atributo minMatches](media/385db1b1-571b-4a05-81b3-db28f5099c17.png)
  
### <a name="match-an-exact-subset-of-any-children-match-elements"></a>Corresponder um subconjunto exato dos elementos filhos de Match

Se você quiser exigir que um número exato de elementos Match seja atendido, defina minMatches e maxMatches como o mesmo valor. Esse elemento Any apenas será satisfeito se exatamente uma data ou uma palavra-chave for encontrada: qualquer coisa além disso e o padrão não será correspondido.
  
![Marcação XML mostrando o elemento Any com o atributo minMatches e maxMatches](media/97b10002-7781-42e8-ac5a-20ad8c5a887e.png)
  
### <a name="match-none-of-children-match-elements"></a>Corresponder nenhum dos elementos filhos de Match

Se você quiser exigir a ausência de evidências específicas para que um padrão seja satisfeito, defina minMatches e maxMatches como 0. Isso poderá ser útil se você tiver uma lista de palavra-chave ou outras evidências com grandes chances de indicarem um falso positivo.
  
Por exemplo, a entidade ID do funcionário procura a palavra-chave "cartão" porque ela pode fazer referência a um "cartão de ID". No entanto, se o cartão aparecer apenas na frase "cartão de crédito", "cartão" neste conteúdo é improvável que signifique um "cartão de ID". Portanto, você pode adicionar "cartão de crédito" como uma palavra-chave a uma lista de termos que você deseja excluir na hora de satisfazer o padrão.
  
![Marcação XML mostrando o valor zero do atributo maxMatches](media/f81d44e5-3db8-48a8-8919-f483a386afdf.png)
  
## <a name="how-close-to-the-entity-must-the-other-evidence-be-patternsproximity-attribute"></a>Qual a proximidade das outras evidências com a entidade? [atributo patternsProximity]

O seu tipo de informação confidencial está procurando um padrão que represente uma ID de funcionário e, como parte desse padrão, ele também está à procura de evidências comprobatórias, como uma palavra-chave como "ID". Faz sentido que, quanto mais próxima essa evidência estiver, mais provavelmente o padrão será uma ID de funcionário real. Você pode determinar a proximidade outras evidências do padrão com a entidade usando o atributo necessário patternsProximity do elemento Entity.
  
![Marcação XML mostrando o atributo patternsProximity](media/e97eb7dc-b897-4e11-9325-91c742d9839b.png)
  
Para cada padrão na entidade, o valor do atributo patternsProximity define a distância (em caracteres Unicode) do local de IdMatch para todas as outras correspondências especificadas para esse padrão. A janela de proximidade é ancorada pela localização de IdMatch e se estende à esquerda e à direita de IdMatch.
  
![Janela de diagrama de proximidade](media/b593dfd1-5eef-4d79-8726-a28923f7c31e.png)
  
O exemplo abaixo ilustra como a janela de proximidade afeta a correspondência de padrões em que o elemento IdMatch para a entidade personalizada ID do funcionário exige pelo menos uma correspondência comprobatória da palavra-chave ou data. Apenas ID1 tem correspondência porque, para ID2 e ID3, nenhuma ou apenas evidência comprobatória parcial foi localizada dentro da janela de proximidade.
  
![Diagrama da janela de proximidade e evidências comprobatórias](media/dc68e38e-dfa1-45b8-b204-89c8ba121f96.png)
  
Observe que, para email, o corpo da mensagem e cada anexo são tratados como itens separados. Isso significa que a janela de proximidade não se estende para além do final de cada um desses itens. Para cada item (anexo ou corpo), o idMatch e as evidências comprobatórias precisam residir nesse item.
  
## <a name="what-are-the-right-confidence-levels-for-different-patterns-confidencelevel-attribute-recommendedconfidence-attribute"></a>Quais são os níveis de confiança certos para diferentes padrões? [atributo confidenceLevel, atributo recommendedConfidence]

Quanto mais evidências um padrão exigir, mais confiança você terá que uma entidade real (como ID do funcionário) será identificada quando esse padrão for correspondido. Por exemplo, você tem mais confiança em um padrão que exige um número de ID de nove dígitos, uma data de contratação e palavras-chave com proximidade imediata do que em um padrão que exige apenas um número de ID de nove dígitos.
  
O elemento Pattern tem um atributo confidenceLevel obrigatório. Você pode pensar no valor de confidenceLevel (um inteiro entre 1 e 100) como uma ID exclusiva para cada padrão em uma entidade; os padrões em uma entidade devem ter níveis de confiança diferentes que você atribui. O valor preciso do inteiro não importa: basta escolher números que façam sentido para sua equipe de conformidade. Depois de carregar seu tipo personalizado de informações confidenciais e criar uma política DLP, você poderá fazer referência a esses níveis de confiança nas condições das regras que você criar.
  
![Marcação XML mostrando elementos Pattern com valores diferentes para o atributo confidenceLevel](media/301e0ba1-2deb-4add-977b-f6e9e18fba8b.png)
  
Além do atributo confidenceLevel para cada Pattern, a Entity tem um atributo recommendedConfidence, o atributo de confiança recomendada pode ser visto como o nível de confiança padrão para a regra. Quando você cria uma regra em uma política DLP, se você não especificar um nível de confiança para a regra usar, ela será correspondida com base no nível de confiança recomendado para a entidade.
  
## <a name="do-you-want-to-support-other-languages-in-the-ui-of-the-security-amp-compliance-center-localizedstrings-element"></a>Deseja oferecer suporte a outros idiomas na interface de usuário do Centro de Conformidade e Segurança? [elemento LocalizedStrings]

Se a sua equipe de conformidade usa o Centro de Conformidade e Segurança do Office 365 para criar políticas DLP em localidades e idiomas diferentes, você pode fornecer versões localizadas do nome e da descrição do seu tipo personalizado de informações confidenciais. Quando sua equipe de conformidade usa o Office 365 em um idioma compatível, ela pode ver o nome localizado na interface do usuário.
  
![Contagem de instâncias e opções de precisão de correspondência](media/11d0b51e-7c3f-4cc6-96d8-b29bcdae1aeb.png)
  
O elemento Rules deve conter um elemento LocalizedStrings, que contém um elemento Resource que faz referência à GUID da sua entidade personalizada. Por sua vez, cada elemento Resource contém um ou mais elementos Name e Description, cada um utilizando o atributo langcode para fornecer uma cadeia de caracteres localizada para um idioma específico.
  
![Marcação XML mostrando o conteúdo do elemento LocalizedStrings](media/a96fc34a-b93d-498f-8b92-285b16a7bbe6.png)
  
Observe que você utiliza cadeias de caracteres localizadas apenas para o modo como o seu tipo personalizado de informações confidenciais é exibido na interface de usuário do Centro de Conformidade e Segurança. Não é possível usar cadeias de caracteres localizadas para fornecer diferentes versões localizadas de uma lista de palavra-chave ou expressão regular.
  
## <a name="other-rule-package-markup-rulepack-guid"></a>Outra marcação de pacote de regras [GUID RulePack]

Por fim, o início de cada RulePackage contém algumas informações gerais que você precisa preencher. Use a marcação a seguir como um modelo e substitua os espaços reservados "..." pelas suas próprias informações.
  
O mais importante: você precisará gerar um GUID para o RulePack. Acima, você gerou um GUID para a entidade; este é um segundo GUID para o RulePack. Há várias maneiras de gerar GUIDs, mas você pode fazer isso facilmente no PowerShell digitando [guid]::NewGuid().
  
O elemento Version também é importante. Ao carregar seu pacote de regras pela primeira vez, o Office 365 anotará o número da versão. Mais tarde, se você atualizar o pacote de regras e carregar uma nova versão, verifique se atualizou o número da versão ou o Office 365 não implantará o pacote de regras.
  
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
    . . .
 </Rules>
</RulePackage>

```

Ao concluir, seu elemento RulePack deve ter esta aparência.
  
![Marcação XML mostrando o elementos RulePack](media/fd0f31a7-c3ee-43cd-a71b-6a3813b21155.png)
  
## <a name="changes-for-exchange-online"></a>Mudanças para o Exchange Online

Anteriormente, você podia usar o Exchange Online PowerShell para importar os tipos personalizados de informações confidenciais para a DLP. Agora os tipos personalizados de informações confidenciais podem ser usados no Centro de Administração do Exchange e o Centro de Conformidade e Segurança. Como parte dessa melhoria, você deve usar o PowerShell do Centro de Conformidade e Segurança para importar tipos de informações confidenciais personalizados, você não poderá mais importá-los do Exchange PowerShell. Os tipos personalizados de informações confidenciais continuarão a funcionar como antes; no entanto, pode levar até uma hora para que as alterações feitas nos tipos personalizados de informações confidenciais no Centro de Conformidade e Segurança apareçam no Centro de Administração do Exchange.
  
Observe que, no Centro de Conformidade e Segurança, o cmdlet `DlpSensitiveInformationTypeRulePackage` é usado para carregar um pacote de regras. Anteriormente, no Centro de Administração do Exchange, o cmdlet `ClassificationRuleCollection` era usado. 
  
## <a name="upload-your-rule-package"></a>Carregar o pacote de regras

Para carregar o pacote de regras, faça o seguinte.
  
1. Salve-o como um arquivo .xml com codificação Unicode.
    
2. [Conectar ao Centro de Conformidade e Segurança do Office 365 usando o PowerShell remoto](http://go.microsoft.com/fwlink/?LinkID=799771&amp;clcid=0x409)
    
3. No PowerShell do Centro de Conformidade e Segurança, digite New-DlpSensitiveInformationTypeRulePackage -FileData (Get-Content -Path "C:\caminhopersonalizado\MyNewRulePack.xml" -Encoding Byte).
    
    Use o local do arquivo onde o pacote de regras está realmente armazenado. C:\caminhopersonalizado\ é um espaço reservado.
    
4. Para confirmar, digite S e pressione Enter.
    
5. Verifique se o novo tipo de informação confidencial foi carregado, digitando Get-DlpSensitiveInformationType para ver uma lista de todos os tipos confidenciais. Você pode separar rapidamente os tipos de informações confidenciais personalizados dos internos observando a coluna Publisher. Você pode filtrar a lista para um tipo específico de informações confidenciais executando Get-DlpSensitiveInformationType-Identity "nome do tipo de informação confidencial".
    
## <a name="potential-validation-issues-to-be-aware-of"></a>Possíveis problemas de validação a serem considerados

Ao carregar seu arquivo XML do pacote de regras, o sistema validará o XML e verificará se há padrões inválidos conhecidos e problemas óbvios de desempenho. Aqui estão alguns problemas conhecidos procurados pela validação, uma expressão regular:
  
- Não comece ou termine com um alternador "|", que corresponde tudo por ser considerado uma correspondência vazia.
    
    Por exemplo, "| a" ou "b |" não passará na validação.
    
- Não comece ou termine com um padrão ".{0,m}", que não tem finalidade funcional e apenas prejudica o desempenho.
    
    Por exemplo, ".{0,50}ASDF" ou "ASDF.{0,50}" não passará na validação.
    
- Não é possível instalar ".{0,m}" ou ".{1,m}" em grupos e não pode ter".\*" ou ". + "em grupos.
    
    Por exemplo, "(.{0,50000})" não passará na validação.
    
- Não é possível ter caracteres com "{0,m}" ou os repetidores "{1,m}" em grupos.
    
    Por exemplo, "(a\*)" não passará na validação.
    
- Não comece ou termine com ".{1,m}"; em vez disso, use simplesmente "."
    
    Por exemplo, ".{1,m}asdf "não passará na validação; use apenas ".asdf".
    
- Não pode ter um repetidor não vinculado (como "\*" ou "+") em um grupo.
    
    Por exemplo, "(xx)\*" e "(xx)+" não passarão na validação.
    
Se um tipo personalizado de informações confidenciais contiver um problema que pode afetar o desempenho, ele não será carregado e você poderá ver uma dessas mensagens de erro:
  
- **Quantificadores genéricos que correspondem a mais conteúdo do que o esperado (por exemplo, "+", "\*")**
    
- **Declarações de pesquisa**
    
- **Agrupamento complexo em conjunção com quantificadores genéricos**
    
## <a name="recrawl-your-content-to-identify-the-sensitive-information"></a>Repetir o rastreamento de seu conteúdo para identificar informações confidenciais

A DLP usa o rastreador de pesquisa para identificar e classificar informações confidenciais no conteúdo do site. O conteúdo em sites no SharePoint Online e no OneDrive for Business será novamente rastreado automaticamente sempre que ele for atualizado. Mas, para identificar seu novo tipo personalizado de informações confidenciais em todo o conteúdo existente, esse conteúdo deve ser novamente rastreado.
  
No Office 365, não é possível solicitar manualmente um novo rastreamento de um locatário inteiro, mas você pode fazer isso para um conjunto de sites, lista ou biblioteca. Confira [Solicitar manualmente o rastreamento e a reindexação de um site, biblioteca ou lista](https://support.office.com/article/9afa977d-39de-4321-b4ca-8c7c7e6d264e).
  
## <a name="remove-a-custom-sensitive-information-type"></a>Remover um tipo de informação confidencial personalizado

1. [Conectar ao Centro de Conformidade e Segurança do Office 365 usando o PowerShell remoto](http://go.microsoft.com/fwlink/?LinkID=799771&amp;clcid=0x409)
    
2. No PowerShell do Centro de Conformidade e Segurança, siga um destes procedimentos:
    
  - Para remover um pacote de regras inteiro e todas as entidades que ele contém
    
    Digite Remove-DlpSensitiveInformationTypeRulePackage "NameOfYourRulePack" - para o XML de exemplo acima, digite Remove-DlpSensitiveInformationTypeRulePackage "Employee ID Custom Rule Pack".
    
    Observe que, para identificar seu pacote de regras, você pode usar o elemento \<Name\> (para qualquer idioma) no elemento \<Rule Pack\> ou o GUID do atributo id do elemento RulePack.
    
  - Para remover uma única entidade de um pacote de regras
    
    Você deve carregar uma nova versão do seu pacote de regras com essa entidade específica removida, usando Set-DlpSensitiveInformationTypeRulePackage. Será necessário garantir que nenhuma política DLP ou regras de transporte do Exchange ainda faça referência ao tipo de informação confidencial antes de removê-lo.
    
3. Para confirmar, digite S e pressione Enter.
    
4. Verifique se a nova regra foi removida, digitando Get- DlpSensitiveInformationType, que deixará de exibir o nome do tipo de informação confidencial.
    
## <a name="reference-rule-package-xml-schema-definition"></a>Referência: Definição do esquema XML do pacote de regras

Você pode copiar essa marcação, salvá-la como um arquivo XSD e usá-la para validar o arquivo XML do seu pacote de regras.
  
```
<?xml version="1.0" encoding="utf-8"?>
<xs:schema xmlns:mce="http://schemas.microsoft.com/office/2011/mce"
           targetNamespace="http://schemas.microsoft.com/office/2011/mce" 
           xmlns:xs="http://www.w3.org/2001/XMLSchema"
           elementFormDefault="qualified"
           attributeFormDefault="unqualified"
           id="RulePackageSchema">
  <!-- Use include if this schema has the same target namespace as the schema being referenced, otherwise use import -->
  <xs:element name="RulePackage" type="mce:RulePackageType"/>
  <xs:simpleType name="LangType">
    <xs:union memberTypes="xs:language">
      <xs:simpleType>
        <xs:restriction base="xs:string">
          <xs:enumeration value=""/>
        </xs:restriction>
      </xs:simpleType>
    </xs:union>
  </xs:simpleType>
  <xs:simpleType name="GuidType" final="#all">
    <xs:restriction base="xs:token">
      <xs:pattern value="[0-9a-fA-F]{8}\-([0-9a-fA-F]{4}\-){3}[0-9a-fA-F]{12}"/>
    </xs:restriction>
  </xs:simpleType>
  <xs:complexType name="RulePackageType">
    <xs:sequence>
      <xs:element name="RulePack" type="mce:RulePackType"/>
      <xs:element name="Rules" type="mce:RulesType">
        <xs:key name="UniqueRuleId">
          <xs:selector xpath="mce:Entity|mce:Affinity|mce:Version/mce:Entity|mce:Version/mce:Affinity"/>
          <xs:field xpath="@id"/>
        </xs:key>
        <xs:key name="UniqueProcessorId">
          <xs:selector xpath="mce:Regex|mce:Keyword|mce:Fingerprint"></xs:selector>
          <xs:field xpath="@id"/>
        </xs:key>
        <xs:key name="UniqueResourceIdRef">
          <xs:selector xpath="mce:LocalizedStrings/mce:Resource"/>
          <xs:field xpath="@idRef"/>
        </xs:key>        
        <xs:keyref name="ReferencedRuleMustExist" refer="mce:UniqueRuleId">
          <xs:selector xpath="mce:LocalizedStrings/mce:Resource"/>
          <xs:field xpath="@idRef"/>
        </xs:keyref>
        <xs:keyref name="RuleMustHaveResource" refer="mce:UniqueResourceIdRef">
          <xs:selector xpath="mce:Entity|mce:Affinity|mce:Version/mce:Entity|mce:Version/mce:Affinity"/>
          <xs:field xpath="@id"/>
        </xs:keyref>
      </xs:element>
    </xs:sequence>
  </xs:complexType>
  <xs:complexType name="RulePackType">
    <xs:sequence>
      <xs:element name="Version" type="mce:VersionType"/>
      <xs:element name="Publisher" type="mce:PublisherType"/>
      <xs:element name="Details" type="mce:DetailsType">
        <xs:key name="UniqueLangCodeInLocalizedDetails">
          <xs:selector xpath="mce:LocalizedDetails"/>
          <xs:field xpath="@langcode"/>
        </xs:key>
        <xs:keyref name="DefaultLangCodeMustExist" refer="mce:UniqueLangCodeInLocalizedDetails">
          <xs:selector xpath="."/>
          <xs:field xpath="@defaultLangCode"/>
        </xs:keyref>
      </xs:element>
      <xs:element name="Encryption" type="mce:EncryptionType" minOccurs="0" maxOccurs="1"/>
    </xs:sequence>
    <xs:attribute name="id" type="mce:GuidType" use="required"/>
  </xs:complexType>
  <xs:complexType name="VersionType">
    <xs:attribute name="major" type="xs:unsignedShort" use="required"/>
    <xs:attribute name="minor" type="xs:unsignedShort" use="required"/>
    <xs:attribute name="build" type="xs:unsignedShort" use="required"/>
    <xs:attribute name="revision" type="xs:unsignedShort" use="required"/>
  </xs:complexType>
  <xs:complexType name="PublisherType">
    <xs:attribute name="id" type="mce:GuidType" use="required"/>
  </xs:complexType>
  <xs:complexType name="LocalizedDetailsType">
    <xs:sequence>
      <xs:element name="PublisherName" type="mce:NameType"/>
      <xs:element name="Name" type="mce:RulePackNameType"/>
      <xs:element name="Description" type="mce:OptionalNameType"/>
    </xs:sequence>
    <xs:attribute name="langcode" type="mce:LangType" use="required"/>
  </xs:complexType>
  <xs:complexType name="DetailsType">
    <xs:sequence>
      <xs:element name="LocalizedDetails" type="mce:LocalizedDetailsType" maxOccurs="unbounded"/>
    </xs:sequence>
    <xs:attribute name="defaultLangCode" type="mce:LangType" use="required"/>
  </xs:complexType>
  <xs:complexType name="EncryptionType">
    <xs:sequence>
      <xs:element name="Key" type="xs:normalizedString"/>
      <xs:element name="IV" type="xs:normalizedString"/>
    </xs:sequence>
  </xs:complexType>
  <xs:simpleType name="RulePackNameType">
    <xs:restriction base="xs:token">
      <xs:minLength value="1"/>
      <xs:maxLength value="64"/>
    </xs:restriction>
  </xs:simpleType>
  <xs:simpleType name="NameType">
    <xs:restriction base="xs:normalizedString">
      <xs:minLength value="1"/>
      <xs:maxLength value="256"/>
    </xs:restriction>
  </xs:simpleType>
  <xs:simpleType name="OptionalNameType">
    <xs:restriction base="xs:normalizedString">
      <xs:minLength value="0"/>
      <xs:maxLength value="256"/>
    </xs:restriction>
  </xs:simpleType>
  <xs:simpleType name="RestrictedTermType">
    <xs:restriction base="xs:string">
      <xs:minLength value="1"/>
      <xs:maxLength value="100"/>
    </xs:restriction>
  </xs:simpleType>
  <xs:complexType name="RulesType">
    <xs:sequence>
      <xs:choice maxOccurs="unbounded">
        <xs:element name="Entity" type="mce:EntityType"/>
        <xs:element name="Affinity" type="mce:AffinityType"/>
        <xs:element name="Version" type="mce:VersionedRuleType"/>
      </xs:choice>
      <xs:choice minOccurs="0" maxOccurs="unbounded">
        <xs:element name="Regex" type="mce:RegexType"/>
        <xs:element name="Keyword" type="mce:KeywordType"/>
        <xs:element name="Fingerprint" type="mce:FingerprintType"/>
        <xs:element name="ExtendedKeyword" type="mce:ExtendedKeywordType"/>
      </xs:choice>
      <xs:element name="LocalizedStrings" type="mce:LocalizedStringsType"/>
    </xs:sequence>
  </xs:complexType>
  <xs:complexType name="EntityType">
    <xs:sequence>
      <xs:element name="Pattern" type="mce:PatternType" maxOccurs="unbounded"/>
      <xs:element name="Version" type="mce:VersionedPatternType" minOccurs="0" maxOccurs="unbounded" />
    </xs:sequence>
    <xs:attribute name="id" type="mce:GuidType" use="required"/>
    <xs:attribute name="patternsProximity" type="mce:ProximityType" use="required"/>
    <xs:attribute name="recommendedConfidence" type="mce:ProbabilityType"/>
    <xs:attribute name="workload" type="mce:WorkloadType"/>
  </xs:complexType>
  <xs:complexType name="PatternType">
    <xs:sequence>
      <xs:element name="IdMatch" type="mce:IdMatchType"/>
      <xs:choice minOccurs="0" maxOccurs="unbounded">
        <xs:element name="Match" type="mce:MatchType"/>
        <xs:element name="Any" type="mce:AnyType"/>
      </xs:choice>
    </xs:sequence>
    <xs:attribute name="confidenceLevel" type="mce:ProbabilityType" use="required"/>
  </xs:complexType>
  <xs:complexType name="AffinityType">
    <xs:sequence>
      <xs:element name="Evidence" type="mce:EvidenceType" maxOccurs="unbounded"/>
      <xs:element name="Version" type="mce:VersionedEvidenceType" minOccurs="0" maxOccurs="unbounded" />
    </xs:sequence>
    <xs:attribute name="id" type="mce:GuidType" use="required"/>
    <xs:attribute name="evidencesProximity" type="mce:ProximityType" use="required"/>
    <xs:attribute name="thresholdConfidenceLevel" type="mce:ProbabilityType" use="required"/>
    <xs:attribute name="workload" type="mce:WorkloadType"/>
  </xs:complexType>
  <xs:complexType name="EvidenceType">
    <xs:sequence>
      <xs:choice maxOccurs="unbounded">
        <xs:element name="Match" type="mce:MatchType"/>
        <xs:element name="Any" type="mce:AnyType"/>
      </xs:choice>
    </xs:sequence>
    <xs:attribute name="confidenceLevel" type="mce:ProbabilityType" use="required"/>
  </xs:complexType>
  <xs:complexType name="IdMatchType">
    <xs:attribute name="idRef" type="xs:string" use="required"/>
  </xs:complexType>
  <xs:complexType name="MatchType">
    <xs:attribute name="idRef" type="xs:string" use="required"/>
    <xs:attribute name="minCount" type="xs:positiveInteger" use="optional"/>
    <xs:attribute name="uniqueResults" type="xs:boolean" use="optional"/>
  </xs:complexType>
  <xs:complexType name="AnyType">
    <xs:sequence>
      <xs:choice maxOccurs="unbounded">
        <xs:element name="Match" type="mce:MatchType"/>
        <xs:element name="Any" type="mce:AnyType"/>
      </xs:choice>
    </xs:sequence>
    <xs:attribute name="minMatches" type="xs:nonNegativeInteger" default="1"/>
    <xs:attribute name="maxMatches" type="xs:nonNegativeInteger" use="optional"/>
  </xs:complexType>
  <xs:simpleType name="ProximityType">
    <xs:union>
      <xs:simpleType>
        <xs:restriction base='xs:string'>
          <xs:enumeration value="unlimited"/>
        </xs:restriction>
      </xs:simpleType>
      <xs:simpleType>
        <xs:restriction base="xs:positiveInteger">
          <xs:minInclusive value="1"/>
        </xs:restriction>
      </xs:simpleType>
    </xs:union>
  </xs:simpleType>
  <xs:simpleType name="ProbabilityType">
    <xs:restriction base="xs:integer">
      <xs:minInclusive value="1"/>
      <xs:maxInclusive value="100"/>
    </xs:restriction>
  </xs:simpleType>
  <xs:simpleType name="WorkloadType">
    <xs:restriction base="xs:string">
      <xs:enumeration value="Exchange"/>
      <xs:enumeration value="Outlook"/>
    </xs:restriction>
  </xs:simpleType>
  <xs:simpleType name="EngineVersionType">
    <xs:restriction base="xs:token">
      <xs:pattern value="^\d{2}\.01?\.\d{3,4}\.\d{1,3}$"/>
    </xs:restriction>
  </xs:simpleType>
  <xs:complexType name="VersionedRuleType">
    <xs:choice maxOccurs="unbounded">
      <xs:element name="Entity" type="mce:EntityType"/>
      <xs:element name="Affinity" type="mce:AffinityType"/>
    </xs:choice>
    <xs:attribute name="minEngineVersion" type="mce:EngineVersionType" use="required" />
  </xs:complexType>
  <xs:complexType name="VersionedPatternType">
    <xs:sequence>
      <xs:element name="Pattern" type="mce:PatternType" maxOccurs="unbounded"/>
    </xs:sequence>
    <xs:attribute name="minEngineVersion" type="mce:EngineVersionType" use="required" />
  </xs:complexType>
  <xs:complexType name="VersionedEvidenceType">
    <xs:sequence>
      <xs:element name="Evidence" type="mce:EvidenceType" maxOccurs="unbounded"/>
    </xs:sequence>
    <xs:attribute name="minEngineVersion" type="mce:EngineVersionType" use="required" />
  </xs:complexType>
  <xs:simpleType name="FingerprintValueType">
    <xs:restriction base="xs:string">
      <xs:minLength value="2732"/>
      <xs:maxLength value="2732"/>
    </xs:restriction>
  </xs:simpleType>
  <xs:complexType name="FingerprintType">
    <xs:simpleContent>
      <xs:extension base="mce:FingerprintValueType">
        <xs:attribute name="id" type="xs:token" use="required"/>
        <xs:attribute name="threshold" type="mce:ProbabilityType" use="required"/>
        <xs:attribute name="shingleCount" type="xs:positiveInteger" use="required"/>
        <xs:attribute name="description" type="xs:string" use="optional"/>
      </xs:extension>
    </xs:simpleContent>
  </xs:complexType>
  <xs:complexType name="RegexType">
    <xs:simpleContent>
      <xs:extension base="xs:string">
        <xs:attribute name="id" type="xs:token" use="required"/>
      </xs:extension>
    </xs:simpleContent>
  </xs:complexType>
  <xs:complexType name="KeywordType">
    <xs:sequence>
      <xs:element name="Group" type="mce:GroupType" maxOccurs="unbounded"/>
    </xs:sequence>
    <xs:attribute name="id" type="xs:token" use="required"/>
  </xs:complexType>
  <xs:complexType name="GroupType">
    <xs:sequence>
      <xs:choice>
        <xs:element name="Term" type="mce:TermType" maxOccurs="unbounded"/>
      </xs:choice>
    </xs:sequence>
    <xs:attribute name="matchStyle" default="word">
      <xs:simpleType>
        <xs:restriction base="xs:NMTOKEN">
          <xs:enumeration value="word"/>
          <xs:enumeration value="string"/>
        </xs:restriction>
      </xs:simpleType>
    </xs:attribute>
  </xs:complexType>
  <xs:complexType name="TermType">
    <xs:simpleContent>
      <xs:extension base="mce:RestrictedTermType">
        <xs:attribute name="caseSensitive" type="xs:boolean" default="false"/>
      </xs:extension>
    </xs:simpleContent>
  </xs:complexType>
  <xs:complexType name="ExtendedKeywordType">
    <xs:simpleContent>
      <xs:extension base="xs:string">
        <xs:attribute name="id" type="xs:token" use="required"/>
      </xs:extension>
    </xs:simpleContent>
  </xs:complexType>
  <xs:complexType name="LocalizedStringsType">
    <xs:sequence>
      <xs:element name="Resource" type="mce:ResourceType" maxOccurs="unbounded">
      <xs:key name="UniqueLangCodeUsedInNamePerResource">
        <xs:selector xpath="mce:Name"/>
        <xs:field xpath="@langcode"/>
      </xs:key>
      <xs:key name="UniqueLangCodeUsedInDescriptionPerResource">
        <xs:selector xpath="mce:Description"/>
        <xs:field xpath="@langcode"/>
      </xs:key>
    </xs:element>
    </xs:sequence>
  </xs:complexType>
  <xs:complexType name="ResourceType">
    <xs:sequence>
      <xs:element name="Name" type="mce:ResourceNameType" maxOccurs="unbounded"/>
      <xs:element name="Description" type="mce:DescriptionType" minOccurs="0" maxOccurs="unbounded"/>
    </xs:sequence>
    <xs:attribute name="idRef" type="mce:GuidType" use="required"/>
  </xs:complexType>
  <xs:complexType name="ResourceNameType">
    <xs:simpleContent>
      <xs:extension base="xs:string">
        <xs:attribute name="default" type="xs:boolean" default="false"/>
        <xs:attribute name="langcode" type="mce:LangType" use="required"/>
      </xs:extension>
    </xs:simpleContent>
  </xs:complexType>
  <xs:complexType name="DescriptionType">
    <xs:simpleContent>
      <xs:extension base="xs:string">
        <xs:attribute name="default" type="xs:boolean" default="false"/>
        <xs:attribute name="langcode" type="mce:LangType" use="required"/>
      </xs:extension>
    </xs:simpleContent>
  </xs:complexType>
</xs:schema>

```

## <a name="more-information"></a>Mais informações

- [Visão geral das políticas de prevenção contra perda de dados](data-loss-prevention-policies.md)
    
- [O que os tipos de informações confidenciais procuram](what-the-sensitive-information-types-look-for.md)
    
- [O que as funções DLP procuram](what-the-dlp-functions-look-for.md)
    

