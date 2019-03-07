---
title: Criar um tipo de informação confidencial personalizado
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Priority
ms.collection:
- M365-security-compliance
search.appverid:
- MOE150
- MET150
description: Saiba como criar, modificar, remover e testar tipos de informações confidenciais personalizados para DLP na interface gráfica do usuário no Centro de Conformidade e Segurança do Office 365.
ms.openlocfilehash: 5e20fac290a7d06c843a0043d95669d9c7f7cd05
ms.sourcegitcommit: 6aa82374eef09d2c1921f93bda3eabeeb28aadeb
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/06/2019
ms.locfileid: "30455133"
---
# <a name="create-a-custom-sensitive-information-type"></a><span data-ttu-id="7a151-103">Criar um tipo de informação confidencial personalizado</span><span class="sxs-lookup"><span data-stu-id="7a151-103">Create a custom sensitive information type</span></span>

<span data-ttu-id="7a151-p101">A Prevenção contra perda de dados (DLP) no Office 365 inclui vários [tipos de informações confidenciais](what-the-sensitive-information-types-look-for.md) que estão prontos para uso nas suas políticas DLP. Esses tipos internos podem ajudar a identificar e proteger números de cartão de crédito, números de contas bancárias, números de passaporte e muito mais.</span><span class="sxs-lookup"><span data-stu-id="7a151-p101">Data loss prevention (DLP) in Office 365 includes many built-in [sensitive information types](what-the-sensitive-information-types-look-for.md) that are ready for you to use in your DLP policies. These built-in types can help identify and protect credit card numbers, bank account numbers, passport numbers, and more.</span></span> 

<span data-ttu-id="7a151-106">Porém, se você precisar identificar e proteger um tipo diferente de informação confidencial, como IDs de funcionário ou números de projeto que usam um formato específico para sua organização, será possível criar um tipo personalizado de informação confidencial.</span><span class="sxs-lookup"><span data-stu-id="7a151-106">But if you need to identify and protect a different type of sensitive information (for example, employee IDs or project numbers that uses a format specific to your organization) you can create a custom sensitive information type.</span></span>

<span data-ttu-id="7a151-107">As partes fundamentais de um tipo personalizado de informações confidenciais são:</span><span class="sxs-lookup"><span data-stu-id="7a151-107">The fundamental parts of a custom sensitive information type are:</span></span>

- <span data-ttu-id="7a151-108">**Padrão principal**: números de ID de funcionário, números de projeto etc. Isso geralmente é identificado por uma expressão regular (RegEx), mas também pode ser uma lista de palavras-chave.</span><span class="sxs-lookup"><span data-stu-id="7a151-108">**Primary pattern**: employee ID numbers, project numbers, etc. This is typically identified by a regular expression (RegEx), but it can also be a list of keywords.</span></span>

- <span data-ttu-id="7a151-p102">**Evidências adicionais**: digamos que você esteja procurando por um número de ID de funcionário de nove dígitos. Nem todos os números de nove dígitos são números de ID de funcionário. Portanto, você pode pesquisar por texto adicional: palavras-chave como "funcionário", "crachá", "ID" ou outros padrões de texto com base em expressões regulares adicionais. Evidências de suporte (também chamadas de _suporte_ ou evidências _comprobatórias_) aumentam a probabilidade de que o número de nove dígitos no conteúdo seja realmente um número de ID de funcionário.</span><span class="sxs-lookup"><span data-stu-id="7a151-p102">**Additional evidence**: Suppose you're looking for a nine-digit employee ID number. Not all nine-digit numbers are employee ID numbers, so you can look for additional text: keywords like "employee", "badge", "ID", or other text patterns based on additional regular expressions. This supporting evidence (also known as _supporting_ or _corroborative_ evidence) increases the likelihood that nine-digit number found in content is really an employee ID number.</span></span>

- <span data-ttu-id="7a151-p103">**Caractere de proximidade**: faz sentido que quanto mais próximos o padrão principal e as evidências de suporte estejam entre si, mais provável seja que o conteúdo detectado seja o que você está procurando. Você pode especificar a distância de caracteres entre o padrão principal e as evidências de suporte (também conhecido como a _janela de proximidade_), conforme mostrado no seguinte diagrama:</span><span class="sxs-lookup"><span data-stu-id="7a151-p103">**Character proximity**: It makes sense that the closer the primary pattern and the supporting evidence are to each other, the more likely the detected content is going to be what you're looking for. You can specify the character distance between the primary pattern and the supporting evidence (also known as the _proximity window_) as shown in the following diagram:</span></span>

    ![Diagrama da janela de proximidade e evidências comprobatórias](media/dc68e38e-dfa1-45b8-b204-89c8ba121f96.png)

- <span data-ttu-id="7a151-p104">**Nível de confiança**: quanto mais evidências de suporte você tiver, maior será a probabilidade de que uma correspondência contenha as informações confidenciais que está procurando. Você pode atribuir níveis mais altos de confiança para correspondências detectadas usando mais evidências.</span><span class="sxs-lookup"><span data-stu-id="7a151-p104">**Confidence level**: The more supporting evidence you have, the higher the likelihood that a match contains the sensitive information you're looking for. You can assign higher levels of confidence for matches that are detected by using more evidence.</span></span>

  <span data-ttu-id="7a151-p105">Quando satisfeito, um padrão retorna uma contagem e um nível de confiança, que você pode usar nas condições de políticas DLP. Ao adicionar uma condição para detectar um tipo de informação confidencial a uma política DLP, você poderá editar o nível de confiança e a contagem, conforme mostrado no seguinte diagrama:</span><span class="sxs-lookup"><span data-stu-id="7a151-p105">When satisfied, a pattern returns a count and confidence level, which you can use in the conditions in your DLP policies. When you add a condition for detecting a sensitive information type to a DLP policy, you can edit the count and confidence level as shown in the following diagram:</span></span>

    ![Contagem de instâncias e opções de precisão de correspondência](media/11d0b51e-7c3f-4cc6-96d8-b29bcdae1aeb.png)

<span data-ttu-id="7a151-120">Para criar tipos de informações confidenciais personalizados no Centro de Conformidade e Segurança do Office 365, você tem as seguintes opções:</span><span class="sxs-lookup"><span data-stu-id="7a151-120">To create custom sensitive information types in the Office 365 Security & Compliance Center, you have the following options:</span></span>

- <span data-ttu-id="7a151-p106">**Usar a interface do usuário**: este método é mais fácil e rápido, mas você tem menos opções de configuração do PowerShell. O restante deste tópico descreve esses procedimentos.</span><span class="sxs-lookup"><span data-stu-id="7a151-p106">**Use the UI**: This method is easier and faster, but you have less configuration options than PowerShell. The rest of this topic describes these procedures.</span></span>

- <span data-ttu-id="7a151-p107">**Usar o PowerShell**: este método requer que você crie primeiro um arquivo XML (chamado de _pacote de regras_) que contém um ou mais tipos de informações confidenciais e use o PowerShell para importar o pacote de regras (a importação do pacote de regras é simples em comparação com a criação do pacote de regras). Esse método é muito mais complexo do que a interface do usuário, mas você tem mais opções de configuração. Para obter instruções, confira [Criar um tipo personalizado de informações confidenciais no PowerShell no Centro de Conformidade e Segurança do Office 365](create-a-custom-sensitive-information-type-in-scc-powershell.md).</span><span class="sxs-lookup"><span data-stu-id="7a151-p107">**Use PowerShell**: This method requires that you first create an XML file (called a _rule package_) that contains one or more sensitive information types, and then you use PowerShell to import the rule package (importing the rule package is trivial compared to creating the rule package. This method is much more complex than the UI, but you have more configuration options. For instructions, see [Create a custom sensitive information type in Office 365 Security & Compliance Center PowerShell](create-a-custom-sensitive-information-type-in-scc-powershell.md).</span></span>

<span data-ttu-id="7a151-126">As principais diferenças são descritas na seguinte tabela:</span><span class="sxs-lookup"><span data-stu-id="7a151-126">The key differences are described in the following table:</span></span>

|<span data-ttu-id="7a151-127">**Tipos de informações confidenciais personalizados na interface de usuário**</span><span class="sxs-lookup"><span data-stu-id="7a151-127">**Custom sensitive information types in the UI**</span></span>|<span data-ttu-id="7a151-128">**Tipos de informações confidenciais personalizados no PowerShell**</span><span class="sxs-lookup"><span data-stu-id="7a151-128">**Custom sensitive information types in PowerShell**</span></span>|
|:-----|:-----|
|<span data-ttu-id="7a151-129">O Nome e a Descrição estão em um idioma.</span><span class="sxs-lookup"><span data-stu-id="7a151-129">Name and Description are in one language.</span></span>|<span data-ttu-id="7a151-130">Dá suporte a vários idiomas para Nome e Descrição.</span><span class="sxs-lookup"><span data-stu-id="7a151-130">Supports multiple languages for Name and Description.</span></span>|
|<span data-ttu-id="7a151-131">Compatível com um padrão.</span><span class="sxs-lookup"><span data-stu-id="7a151-131">Supports one pattern.</span></span>|<span data-ttu-id="7a151-132">Compatível com vários padrões.</span><span class="sxs-lookup"><span data-stu-id="7a151-132">Supports multiple patterns.</span></span>|
|<span data-ttu-id="7a151-133">As evidências de suporte podem ser:</span><span class="sxs-lookup"><span data-stu-id="7a151-133">Supporting evidence can be:</span></span> <br/><span data-ttu-id="7a151-134">• Expressões regulares</span><span class="sxs-lookup"><span data-stu-id="7a151-134">• Regular expressions</span></span> <br/><span data-ttu-id="7a151-135">• Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="7a151-135">• Keywords</span></span> <br/><span data-ttu-id="7a151-136">• Dicionários de palavras-chave</span><span class="sxs-lookup"><span data-stu-id="7a151-136">• Keyword dictionaries</span></span>|<span data-ttu-id="7a151-137">As evidências de suporte podem ser:</span><span class="sxs-lookup"><span data-stu-id="7a151-137">Supporting evidence can be:</span></span> <br/><span data-ttu-id="7a151-138">• Expressões regulares</span><span class="sxs-lookup"><span data-stu-id="7a151-138">• Regular expressions</span></span> <br/><span data-ttu-id="7a151-139">• Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="7a151-139">• Keywords</span></span> <br/><span data-ttu-id="7a151-140">• Dicionários de palavras-chave</span><span class="sxs-lookup"><span data-stu-id="7a151-140">• Keyword dictionaries</span></span> <br/><span data-ttu-id="7a151-141">• [Funções DLP internas](what-the-dlp-functions-look-for.md)</span><span class="sxs-lookup"><span data-stu-id="7a151-141">• [Built-in DLP functions](what-the-dlp-functions-look-for.md)</span></span>|
|<span data-ttu-id="7a151-142">Os tipos de informações confidenciais personalizados são adicionados ao pacote de regras chamado Microsoft.SCCManaged.CustomRulePack</span><span class="sxs-lookup"><span data-stu-id="7a151-142">Custom sensitive information types are added to the rule package named Microsoft.SCCManaged.CustomRulePack</span></span>|<span data-ttu-id="7a151-143">Você pode criar até 10 pacotes de regras com tipos de informações confidenciais personalizados.</span><span class="sxs-lookup"><span data-stu-id="7a151-143">You can create up to 10 rule packages that contain custom sensitive information types.</span></span>|
|<span data-ttu-id="7a151-144">O padrão de comparação requer a detecção do padrão principal e todas as evidências de suporte (o operador AND implícito é usado).</span><span class="sxs-lookup"><span data-stu-id="7a151-144">Pattern match requires the detection of the primary pattern and all supporting evidence (the implicit AND operator is used).</span></span>|<span data-ttu-id="7a151-145">O padrão de comparação requer a detecção do padrão principal e uma quantidade de evidências de suporte configurável (podem ser usados os operadores AND e OR implícitos).</span><span class="sxs-lookup"><span data-stu-id="7a151-145">Pattern match requires the detection of the primary pattern and a configurable amount of supporting evidence (implicit AND and OR operators can be used).</span></span>|

## <a name="what-do-you-need-to-know-before-you-begin"></a><span data-ttu-id="7a151-146">O que você precisa saber antes de começar?</span><span class="sxs-lookup"><span data-stu-id="7a151-146">What do you need to know before you begin?</span></span>

- <span data-ttu-id="7a151-147">Para abrir o Centro de Conformidade e Segurança, confira [Acessar o Centro de Conformidade e Segurança do Office 365](go-to-the-securitycompliance-center.md).</span><span class="sxs-lookup"><span data-stu-id="7a151-147">To open the Security & Compliance Center, see [Go to the Office 365 Security & Compliance Center](go-to-the-securitycompliance-center.md).</span></span>

- <span data-ttu-id="7a151-p108">Os tipos de informações confidenciais personalizados exigem familiaridade com expressões regulares (RegEx). Para saber mais sobre o mecanismo de RegEx (anteriormente conhecido como RegEx++) usado para processar o texto, confira [Boost.RegEx 5.1.3](https://www.boost.org/doc/libs/1_68_0/libs/regex/doc/html/).</span><span class="sxs-lookup"><span data-stu-id="7a151-p108">Custom sensitive information types require familiarity with regular expressions (RegEx). For more information about the Boost.RegEx (formerly known as RegEx++) engine that's used for processing the text, see [Boost.Regex 5.1.3](https://www.boost.org/doc/libs/1_68_0/libs/regex/doc/html/).</span></span>

  <span data-ttu-id="7a151-p109">O Suporte da Microsoft não pode ajudar no fornecimento de definições de correspondência de conteúdo personalizado (criação de classificações personalizadas ou padrões de expressões regulares). Os engenheiros de suporte podem fornecer suporte limitado para o recurso (por exemplo, fornecer padrões de expressões regulares de exemplo para fins de teste ou a assistência para solução de problemas de um padrão de expressão regular existente que não está sendo disparado conforme o esperado), mas não podem fornecer garantias de que qualquer desenvolvimento de correspondência de conteúdo personalizado atenderá a seus requisitos ou obrigações.</span><span class="sxs-lookup"><span data-stu-id="7a151-p109">Microsoft Customer Service & Support can't assist with providing custom content-matching definitions (creating custom classifications or regular expression patterns). Support engineers can provide limited support for the feature (for example, providing sample regular expression patterns for testing purposes, or assisting with troubleshooting an existing regular expression pattern that's not triggering as expected), but can't provide assurances that any custom content-matching development will fulfill your requirements or obligations.</span></span>

- <span data-ttu-id="7a151-p110">A DLP usa o rastreador de pesquisa para identificar e classificar informações confidenciais em sites do OneDrive e do SharePoint Online for Business. Para identificar o novo tipo personalizado de informações confidenciais no conteúdo existente, o conteúdo deve ser rastreado novamente. O conteúdo é rastreado novamente com base em uma agenda, mas você pode repetir manualmente o rastreamento do conteúdo de um conjunto de sites, uma lista ou uma biblioteca. Para saber mais, confira [Solicitar manualmente o rastreamento e a reindexação de um site, uma biblioteca ou uma lista](https://docs.microsoft.com/sharepoint/crawl-site-content).</span><span class="sxs-lookup"><span data-stu-id="7a151-p110">DLP uses the search crawler to identify and classify sensitive information in SharePoint Online and OneDrive for Business sites. To identify your new custom sensitive information type in existing content, the content must be recrawled. Content is recrawled based on a schedule, but you can manually recrawl content for a site collection, list, or library. For more information, see [Manually request crawling and re-indexing of a site, a library or a list](https://docs.microsoft.com/sharepoint/crawl-site-content).</span></span>

## <a name="create-custom-sensitive-information-types-in-the-security--compliance-center"></a><span data-ttu-id="7a151-156">Criar tipos de informações confidenciais personalizados no Centro de Conformidade e Segurança</span><span class="sxs-lookup"><span data-stu-id="7a151-156">Create custom sensitive information types in the Security & Compliance Center</span></span>

<span data-ttu-id="7a151-157">No Centro de Conformidade e Segurança, acesse **Classificações** \> **Tipos de informações confidenciais** e clique em **Criar**.</span><span class="sxs-lookup"><span data-stu-id="7a151-157">In the Security & Compliance Center, go to **Classifications** \> **Sensitive info types** and click **Create**.</span></span>

<span data-ttu-id="7a151-158">As configurações são bastante óbvias e são explicadas na página associada do assistente:</span><span class="sxs-lookup"><span data-stu-id="7a151-158">The settings are fairly self-evident, and are explained on the associate page of the wizard:</span></span>

- <span data-ttu-id="7a151-159">**Nome**</span><span class="sxs-lookup"><span data-stu-id="7a151-159">**Name**</span></span>

- <span data-ttu-id="7a151-160">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="7a151-160">**Description**</span></span>

- <span data-ttu-id="7a151-161">**Proximidade**</span><span class="sxs-lookup"><span data-stu-id="7a151-161">**Proximity**</span></span>

- <span data-ttu-id="7a151-162">**Nível de confiança**</span><span class="sxs-lookup"><span data-stu-id="7a151-162">**Confidence level**</span></span>

- <span data-ttu-id="7a151-163">**Elemento de padrão principal** (palavras-chave, expressão regular ou dicionário)</span><span class="sxs-lookup"><span data-stu-id="7a151-163">**Primary pattern element** (keywords, regular expression, or dictionary)</span></span>

- <span data-ttu-id="7a151-164">**Elementos de padrão de suporte** opcionais (palavras-chave, expressão regular ou dicionário) e um valor de **Custo mínimo** correspondente.</span><span class="sxs-lookup"><span data-stu-id="7a151-164">Optional **Supporting pattern elements** (keywords, regular expression, or dictionary) and a corresponding **Minimum cost** value.</span></span>

<span data-ttu-id="7a151-p111">Aqui está um cenário: você deseja um tipo personalizado de informação confidencial que detecte os números de funcionários com nove dígitos no conteúdo, juntamente com as palavras-chave "funcionário", "ID" e "crachá". Para criar esse tipo personalizado de informação confidencial, faça o seguinte:</span><span class="sxs-lookup"><span data-stu-id="7a151-p111">Here's a scenario: You want a custom sensitive information type that detects 9-digit employee numbers in content, along with the keywords "employee" "ID" and "badge". To create this custom sensitive information type, do the following steps:</span></span>

1. <span data-ttu-id="7a151-167">No Centro de Conformidade e Segurança, acesse **Classificações** \> **Tipos de informações confidenciais** e clique em **Criar**.</span><span class="sxs-lookup"><span data-stu-id="7a151-167">In the Security & Compliance Center, go to **Classifications** \> **Sensitive info types** and click **Create**.</span></span>

    ![Local dos tipos de informações confidenciais e botão Criar](media/scc-cust-sens-info-type-new.png)

2. <span data-ttu-id="7a151-169">Na página **Escolher um nome e uma descrição** que é aberta, insira os seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="7a151-169">In the **Choose a name and description** page that opens, enter the following values:</span></span>

  - <span data-ttu-id="7a151-170">**Nome**: ID de funcionário.</span><span class="sxs-lookup"><span data-stu-id="7a151-170">**Name**: Employee ID.</span></span>

  - <span data-ttu-id="7a151-171">**Descrição** detectar os números de nove dígitos de ID de funcionário da Contoso.</span><span class="sxs-lookup"><span data-stu-id="7a151-171">**Description**: Detect nine-digit Contoso employee ID numbers.</span></span>

    ![Página de nome e descrição](media/scc-cust-sens-info-type-new-name-desc.png)

    <span data-ttu-id="7a151-173">Quando terminar, clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="7a151-173">When you're finished, click **Next**.</span></span>

3. <span data-ttu-id="7a151-174">Na página **Requisitos para correspondência** que é aberta, clique em **Adicionar um elemento** e defina as seguintes configurações:</span><span class="sxs-lookup"><span data-stu-id="7a151-174">In the **Requirements for matching** page that opens, click **Add an element** configure the following settings:</span></span>

    - <span data-ttu-id="7a151-175">**Detectar conteúdo que tenha**:</span><span class="sxs-lookup"><span data-stu-id="7a151-175">**Detect content containing**:</span></span>
 
      <span data-ttu-id="7a151-p112">a. Clique em **Qualquer um destes elementos** e selecione **Expressão regular**.</span><span class="sxs-lookup"><span data-stu-id="7a151-p112">a. Click **Any of these** and select **Regular expression**.</span></span>

      <span data-ttu-id="7a151-p113">b. Na caixa de expressão regular, insira `(\s)(\d{9})(\s)` (números de nove dígitos delimitados por espaço em branco)</span><span class="sxs-lookup"><span data-stu-id="7a151-p113">b. In the regular expression box, enter `(\s)(\d{9})(\s)` (nine-digit numbers surrounded by white space).</span></span>
  
    - <span data-ttu-id="7a151-180">**Elementos de suporte**: clique em **Adicionar elementos de suporte** e selecione **Contém esta lista de palavras-chave**.</span><span class="sxs-lookup"><span data-stu-id="7a151-180">**Supporting elements**: Click **Add supporting elements** and select **Contains this keyword list**.</span></span>

    - <span data-ttu-id="7a151-181">Na área **Contém esta lista de palavra-chave** que é exibida, defina as seguintes configurações:</span><span class="sxs-lookup"><span data-stu-id="7a151-181">In the **Contains this keyword list** area that appears, configure the following settings:</span></span>

      - <span data-ttu-id="7a151-182">**Lista de palavra-chave**: insira o seguinte valor: funcionário,ID,crachá.</span><span class="sxs-lookup"><span data-stu-id="7a151-182">**Keyword list**: Enter the following value: employee,ID,badge.</span></span>

      - <span data-ttu-id="7a151-183">**Contagem mínima**: mantenha o valor padrão 1.</span><span class="sxs-lookup"><span data-stu-id="7a151-183">**Minimum count**: Leave the default value 1.</span></span>

    - <span data-ttu-id="7a151-184">Mantenha o valor padrão de 60 para o **Nível de confiança**.</span><span class="sxs-lookup"><span data-stu-id="7a151-184">Leave the default **Confidence level** value 60.</span></span> 

    - <span data-ttu-id="7a151-185">Mantenha o valor padrão de 300 para a **Proximidade de caracteres**.</span><span class="sxs-lookup"><span data-stu-id="7a151-185">Leave the default **Character proximity** value 300.</span></span>

    ![Requisitos para a página correspondente](media/scc-cust-sens-info-type-new-reqs.png)

    <span data-ttu-id="7a151-187">Quando terminar, clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="7a151-187">When you're finished, click **Next**.</span></span>

4. <span data-ttu-id="7a151-188">Na página **Examinar e finalizar** que é aberta, examine as configurações e clique em **Concluir**.</span><span class="sxs-lookup"><span data-stu-id="7a151-188">On the **Review and finalize** page that opens, review the settings and click **Finish**.</span></span>

    ![Examine e finalizar a página](media/scc-cust-sens-info-type-new-review.png)

5. <span data-ttu-id="7a151-p114">A próxima página incentiva você a testar o novo tipo personalizado de informação confidencial clicando em **Sim**. Para saber mais, confira [Tipos de informações confidenciais personalizados no Centro de Conformidade e Segurança](#test-custom-sensitive-information-types-in-the-security--compliance-center). Para testar a regra mais tarde, clique em **Não**.</span><span class="sxs-lookup"><span data-stu-id="7a151-p114">The next page encourages you to test the new custom sensitive information type by clicking **Yes**. For more information, see [Test custom sensitive information types in the Security & Compliance Center](#test-custom-sensitive-information-types-in-the-security--compliance-center). To test the rule later, click **No**.</span></span>

    ![Página de recomendações de teste](media/scc-cust-sens-info-type-new-test.png)

### <a name="how-do-you-know-this-worked"></a><span data-ttu-id="7a151-194">Como saber se funcionou?</span><span class="sxs-lookup"><span data-stu-id="7a151-194">How do you know this worked?</span></span>

<span data-ttu-id="7a151-195">Para confirmar que você criou um novo tipo de informação confidencial com êxito, execute uma destas etapas:</span><span class="sxs-lookup"><span data-stu-id="7a151-195">To verify that you've successfully created a new sensitive information type, do any of the following steps:</span></span>

  - <span data-ttu-id="7a151-196">Vá para **Classificações** \> **Tipos de informações confidenciais** e verifique se o novo tipo personalizado de informações confidenciais está listado.</span><span class="sxs-lookup"><span data-stu-id="7a151-196">Go to **Classifications** \> **Sensitive info types** and verify the new custom sensitive information type is listed.</span></span>

  - <span data-ttu-id="7a151-p115">Teste o novo tipo personalizado de informação confidencial. Para saber mais, confira [Testar tipos de informações confidenciais personalizados no Centro de Conformidade e Segurança](#test-custom-sensitive-information-types-in-the-security--compliance-center).</span><span class="sxs-lookup"><span data-stu-id="7a151-p115">Test the new custom sensitive information type. For more information, see [Test custom sensitive information types in the Security & Compliance Center](#test-custom-sensitive-information-types-in-the-security--compliance-center).</span></span>

## <a name="modify-custom-sensitive-information-types-in-the-security--compliance-center"></a><span data-ttu-id="7a151-199">Modificar tipos de informações confidenciais personalizados no Centro de Conformidade e Segurança</span><span class="sxs-lookup"><span data-stu-id="7a151-199">Modify custom sensitive information types in the Security & Compliance Center</span></span>

<span data-ttu-id="7a151-200">**Observações**:</span><span class="sxs-lookup"><span data-stu-id="7a151-200">**Notes**:</span></span>

- <span data-ttu-id="7a151-p116">Você só pode modificar tipos de informações confidenciais personalizados. Não é possível modificar tipos internos de informações confidenciais. Porém, você pode usar o PowerShell para exportar tipos de informações confidenciais personalizados internos, personalizá-los e importá-los como tipos de informações confidenciais personalizados. Para saber mais, confira [Personalizar um tipo de informação confidencial interno](customize-a-built-in-sensitive-information-type.md).</span><span class="sxs-lookup"><span data-stu-id="7a151-p116">You can only modify custom sensitive information types; you can't modify built-in sensitive information types. But you can use PowerShell to export built-in custom sensitive information types, customize them, and import them as custom sensitive information types. For more information, see [Customize a built-in sensitive information type](customize-a-built-in-sensitive-information-type.md).</span></span>

- <span data-ttu-id="7a151-p117">Somente você pode modificar os tipos de informações confidenciais personalizados que criou na interface do usuário. Se você tiver usado o [procedimento do PowerShell](create-a-custom-sensitive-information-type-in-scc-powershell.md) para importar um pacote de regras de tipo personalizado de informações confidenciais, você receberá um erro.</span><span class="sxs-lookup"><span data-stu-id="7a151-p117">You can only modify custom sensitive information types that you created in the UI. If you used the [PowerShell procedure](create-a-custom-sensitive-information-type-in-scc-powershell.md) to import a custom sensitive information type rule package, you'll get an error.</span></span>

<span data-ttu-id="7a151-206">No Centro de Conformidade e Segurança, acesse **Classificações** \> **Tipos de informações confidenciais**, selecione os tipos de informações confidenciais personalizados que você deseja modificar e clique em **Editar**.</span><span class="sxs-lookup"><span data-stu-id="7a151-206">In the Security & Compliance Center, go to **Classifications** \> **Sensitive info types**, select the custom sensitive information type that you want to modify, and then click **Edit**.</span></span>

  ![Local dos tipos de informações confidenciais e botão Editar](media/scc-cust-sens-info-type-edit.png)

<span data-ttu-id="7a151-p118">Aqui estão disponíveis as mesmas opções oferecidas quando você criou o tipo de informação confidencial personalizado no Centro de Conformidade e Segurança. Para saber mais, confira [Criar tipos de informações confidenciais personalizados no Centro de Conformidade e Segurança](#create-custom-sensitive-information-types-in-the-security--compliance-center).</span><span class="sxs-lookup"><span data-stu-id="7a151-p118">The same options are available here as when you created the custom sensitive information type in the Security & Compliance Center. For more information, see [Create custom sensitive information types in the Security & Compliance Center](#create-custom-sensitive-information-types-in-the-security--compliance-center).</span></span>

### <a name="how-do-you-know-this-worked"></a><span data-ttu-id="7a151-210">Como saber se funcionou?</span><span class="sxs-lookup"><span data-stu-id="7a151-210">How do you know this worked?</span></span>

<span data-ttu-id="7a151-211">Para confirmar que você modificou um tipo de informação confidencial com êxito, execute uma destas etapas:</span><span class="sxs-lookup"><span data-stu-id="7a151-211">To verify that you've successfully modified a sensitive information type, do any of the following steps:</span></span>

  - <span data-ttu-id="7a151-212">Vá para **classificações** \> **Tipos de informações confidenciais** para verificar as propriedades do tipo personalizado de informação confidencial modificado.</span><span class="sxs-lookup"><span data-stu-id="7a151-212">Go to **Classifications** \> **Sensitive info types** to verify the properties of the modified custom sensitive information type.</span></span> 

  - <span data-ttu-id="7a151-p119">Teste o tipo personalizado de informação confidencial modificada. Para saber mais, confira [Testar tipos de informações confidenciais personalizados no Centro de Conformidade e Segurança](#test-custom-sensitive-information-types-in-the-security--compliance-center).</span><span class="sxs-lookup"><span data-stu-id="7a151-p119">Test the modified custom sensitive information type. For more information, see [Test custom sensitive information types in the Security & Compliance Center](#test-custom-sensitive-information-types-in-the-security--compliance-center).</span></span>

## <a name="remove-custom-sensitive-information-types-in-the-security--compliance-center"></a><span data-ttu-id="7a151-215">Remover tipos de informações confidenciais personalizados no Centro de Conformidade e Segurança</span><span class="sxs-lookup"><span data-stu-id="7a151-215">Remove custom sensitive information types in the Security & Compliance Center</span></span> 

<span data-ttu-id="7a151-216">**Observações**:</span><span class="sxs-lookup"><span data-stu-id="7a151-216">**Notes**:</span></span>

- <span data-ttu-id="7a151-217">Você só pode remover tipos de informações confidenciais personalizados. Não é possível remover tipos internos de informações confidenciais.</span><span class="sxs-lookup"><span data-stu-id="7a151-217">You can only remove custom sensitive information types; you can't remove built-in sensitive information types.</span></span>

- <span data-ttu-id="7a151-218">Antes de remover um tipo personalizado de informação confidencial, verifique se nenhuma política de DLP ou regras de fluxo de emails do Exchange (também conhecidas como regras de transporte) ainda fazem referência ao tipo de informação confidencial.</span><span class="sxs-lookup"><span data-stu-id="7a151-218">Before your remove a custom sensitive information type, verify that no DLP policies or Exchange mail flow rules (also known as transport rules) still reference the sensitive information type.</span></span>

1. <span data-ttu-id="7a151-219">No Centro de Conformidade e Segurança, acesse **Classificações** \> **Tipos de informações confidenciais** e selecione um ou mais tipos de informações confidenciais personalizados que você deseja remover.</span><span class="sxs-lookup"><span data-stu-id="7a151-219">In the Security & Compliance Center, go to **Classifications** \> **Sensitive info types** and select one or more custom sensitive information types that you want to remove.</span></span>

2. <span data-ttu-id="7a151-220">No submenu que é aberto, clique em **Excluir** (ou **Excluir tipos de informações confidenciais** se você tiver selecionado mais de um).</span><span class="sxs-lookup"><span data-stu-id="7a151-220">In the fly-out that opens, click **Delete** (or **Delete sensitive info types** if you selected more than one).</span></span>

    ![Local dos tipos de informações confidenciais e botão Excluir](media/scc-cust-sens-info-type-delete.png)

3. <span data-ttu-id="7a151-222">Na mensagem de aviso exibida, clique em **Sim**.</span><span class="sxs-lookup"><span data-stu-id="7a151-222">In the warning message that appears, click **Yes**.</span></span>

### <a name="how-do-you-know-this-worked"></a><span data-ttu-id="7a151-223">Como saber se funcionou?</span><span class="sxs-lookup"><span data-stu-id="7a151-223">How do you know this worked?</span></span>

<span data-ttu-id="7a151-224">Para verificar se você removeu um tipo personalizado de informação confidencial com êxito, vá até **Classificações** \> **Tipos de informações confidenciais** para verificar se o tipo personalizado de informação confidencial não está mais presente.</span><span class="sxs-lookup"><span data-stu-id="7a151-224">To verify that you've successfully removed a custom sensitive information type, go to **Classifications** \> **Sensitive info types** to verify the custom sensitive information type is no longer listed.</span></span>

## <a name="test-custom-sensitive-information-types-in-the-security--compliance-center"></a><span data-ttu-id="7a151-225">Teste tipos de informações confidenciais personalizados no Centro de Conformidade e Segurança</span><span class="sxs-lookup"><span data-stu-id="7a151-225">Test custom sensitive information types in the Security & Compliance Center</span></span>

1. <span data-ttu-id="7a151-226">No Centro de Conformidade e Segurança, acesse **Classificações** \> **Tipos de informações confidenciais**.</span><span class="sxs-lookup"><span data-stu-id="7a151-226">In the Security & Compliance Center, go to **Classifications** \> **Sensitive info types**.</span></span>

2. <span data-ttu-id="7a151-p120">Selecione um ou mais tipos de informações confidenciais personalizados para testar. No submenu suspenso que é aberto, clique em **Testar tipo** (ou **Testar tipos de informações confidenciais** se você tiver selecionado mais de um).</span><span class="sxs-lookup"><span data-stu-id="7a151-p120">Select one or more custom sensitive information types to test. In the fly-out that opens, click **Test type** (or **Test sensitive info types** if you selected more than one).</span></span>

    ![Local dos tipos de informações confidenciais e botão de tipo de Teste](media/scc-cust-sens-info-type-test.png)

3. <span data-ttu-id="7a151-230">Na página **Carregar arquivo para teste** que se abre, carregue um documento para teste arrastando e soltando um arquivo, ou então clicando em **Procurar** e selecionando um arquivo.</span><span class="sxs-lookup"><span data-stu-id="7a151-230">On the **Upload file to test** page that opens, upload a document to test by dragging and dropping a file or by clicking **Browse** and selecting a file.</span></span>

    ![Carregar arquivos na página de teste](media/scc-cust-sens-info-type-test-upload.png)

4. <span data-ttu-id="7a151-232">Clique no botão **Testar** para testar o documento em busca de correspondências de padrão no arquivo.</span><span class="sxs-lookup"><span data-stu-id="7a151-232">Click the **Test** button to test the document for pattern matches in the file.</span></span>

5. <span data-ttu-id="7a151-233">Na página **Resultados da correspondência**, clique em **Concluir**.</span><span class="sxs-lookup"><span data-stu-id="7a151-233">On the **Match results** page, click **Finish**.</span></span>

    ![Resultados da correspondência](media/scc-cust-sens-info-type-test-results.png)