---
title: Criar um tipo personalizado de informação confidencial no Centro de Conformidade e Segurança
ms.author: chrfox
author: chrfox
manager: laurawi
audience: Admin
ms.topic: article
ms.service: O365-seccomp
ms.date: 04/17/2019
localization_priority: Priority
ms.collection:
- M365-security-compliance
search.appverid:
- MOE150
- MET150
description: Saiba como criar, modificar, remover e testar tipos de informações confidenciais personalizados para DLP na interface gráfica do usuário, no Centro de Conformidade e Segurança.
ms.openlocfilehash: e7b2d07c64d97eafee5b269bbc0e395855c2ab44
ms.sourcegitcommit: 0a0d9c1325b4b0581018c31037dcc707d3d679b4
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/09/2019
ms.locfileid: "36279153"
---
# <a name="create-a-custom-sensitive-information-type-in-the-security--compliance-center"></a><span data-ttu-id="8ffcc-103">Criar um tipo personalizado de informação confidencial no Centro de Conformidade e Segurança</span><span class="sxs-lookup"><span data-stu-id="8ffcc-103">Create a custom sensitive information type in Security & Compliance Center PowerShell</span></span>

## <a name="summary"></a><span data-ttu-id="8ffcc-104">Resumo</span><span class="sxs-lookup"><span data-stu-id="8ffcc-104">Summary</span></span>

<span data-ttu-id="8ffcc-105">Leia este artigo para criar um [ tipo personalizado de informação confidencial](custom-sensitive-info-types.md) no Centro de Conformidade e Segurança ([https://protection.office.com](https://protection.office.com)).</span><span class="sxs-lookup"><span data-stu-id="8ffcc-105">Read this article to create a [custom sensitive information type](custom-sensitive-info-types.md) in the Security & Compliance Center ([https://protection.office.com](https://protection.office.com)).</span></span> <span data-ttu-id="8ffcc-106">Os tipos personalizados de informações confidenciais criados através desse método são adicionados ao pacote de regras chamado `Microsoft.SCCManaged.CustomRulePack`.</span><span class="sxs-lookup"><span data-stu-id="8ffcc-106">The custom sensitive information types that you create by using this method are added to the rule package named `Microsoft.SCCManaged.CustomRulePack`.</span></span>

<span data-ttu-id="8ffcc-107">Também é possível criar tipos personalizados de informações confidenciais usando os recursos PowerShell e Exact Data Match.</span><span class="sxs-lookup"><span data-stu-id="8ffcc-107">You can also create custom sensitive information types by using PowerShell and Exact Data Match capabilities.</span></span> <span data-ttu-id="8ffcc-108">Para saber mais sobre esses métodos, confira:</span><span class="sxs-lookup"><span data-stu-id="8ffcc-108">To learn more about those methods, see:</span></span>
- [<span data-ttu-id="8ffcc-109">Crie um tipo personalizado de informação confidencial no PowerShell do Centro de Conformidade e Segurança</span><span class="sxs-lookup"><span data-stu-id="8ffcc-109">Create a custom sensitive information type in Security &amp; Compliance Center PowerShell</span></span>](create-a-custom-sensitive-information-type-in-scc-powershell.md)
- <span data-ttu-id="8ffcc-110">[Criar um tipo personalizado de informações confidenciais com Correspondência Exata de Dados (visualização)](create-custom-sensitive-information-types-with-exact-data-match-based-classification.md)</span><span class="sxs-lookup"><span data-stu-id="8ffcc-110">See [Create a custom sensitive information type with Exact Data Match based classification (Preview)](create-custom-sensitive-information-types-with-exact-data-match-based-classification.md).</span></span>

## <a name="before-you-begin"></a><span data-ttu-id="8ffcc-111">Antes de começar...</span><span class="sxs-lookup"><span data-stu-id="8ffcc-111">Before you begin</span></span>

- <span data-ttu-id="8ffcc-112">Sua organização deve ter uma assinatura, como o Office 365 Enterprise, que inclua Prevenção Contra Perda de Dados (DLP)</span><span class="sxs-lookup"><span data-stu-id="8ffcc-112">Your organization must have a subscription, such as Office 365 Enterprise, that includes Data Loss Prevention (DLP).</span></span> <span data-ttu-id="8ffcc-113">Consulte [Política de Mensagens e Descrição do Serviço de Conformidade](https://docs.microsoft.com/office365/servicedescriptions/exchange-online-protection-service-description/messaging-policy-and-compliance-servicedesc).</span><span class="sxs-lookup"><span data-stu-id="8ffcc-113">See [Messaging Policy and Compliance ServiceDescription](https://docs.microsoft.com/office365/servicedescriptions/exchange-online-protection-service-description/messaging-policy-and-compliance-servicedesc).</span></span> 

- <span data-ttu-id="8ffcc-p104">Os tipos de informações confidenciais personalizados exigem familiaridade com expressões regulares (RegEx). Para saber mais sobre o mecanismo de RegEx (anteriormente conhecido como RegEx++) usado para processar o texto, confira [Boost.RegEx 5.1.3](https://www.boost.org/doc/libs/1_68_0/libs/regex/doc/html/).</span><span class="sxs-lookup"><span data-stu-id="8ffcc-p104">Custom sensitive information types require familiarity with regular expressions (RegEx). For more information about the Boost.RegEx (formerly known as RegEx++) engine that's used for processing the text, see [Boost.Regex 5.1.3](https://www.boost.org/doc/libs/1_68_0/libs/regex/doc/html/).</span></span>

  <span data-ttu-id="8ffcc-p105">O Suporte da Microsoft não pode ajudar no fornecimento de definições de correspondência de conteúdo personalizado (criação de classificações personalizadas ou padrões de expressões regulares). Os engenheiros de suporte podem fornecer suporte limitado para o recurso (por exemplo, fornecer padrões de expressões regulares de exemplo para fins de teste ou a assistência para solução de problemas de um padrão de expressão regular existente que não está sendo disparado conforme o esperado), mas não podem fornecer garantias de que qualquer desenvolvimento de correspondência de conteúdo personalizado atenderá a seus requisitos ou obrigações.</span><span class="sxs-lookup"><span data-stu-id="8ffcc-p105">Microsoft Customer Service & Support can't assist with providing custom content-matching definitions (creating custom classifications or regular expression patterns). Support engineers can provide limited support for the feature (for example, providing sample regular expression patterns for testing purposes, or assisting with troubleshooting an existing regular expression pattern that's not triggering as expected), but can't provide assurances that any custom content-matching development will fulfill your requirements or obligations.</span></span>

- <span data-ttu-id="8ffcc-p106">A DLP usa o rastreador de pesquisa para identificar e classificar informações confidenciais em sites do OneDrive e do SharePoint Online for Business. Para identificar o novo tipo personalizado de informações confidenciais no conteúdo existente, o conteúdo deve ser rastreado novamente. O conteúdo é rastreado novamente com base em uma agenda, mas você pode repetir manualmente o rastreamento do conteúdo de um conjunto de sites, uma lista ou uma biblioteca. Para saber mais, confira [Solicitar manualmente o rastreamento e a reindexação de um site, uma biblioteca ou uma lista](https://docs.microsoft.com/sharepoint/crawl-site-content).</span><span class="sxs-lookup"><span data-stu-id="8ffcc-p106">DLP uses the search crawler to identify and classify sensitive information in SharePoint Online and OneDrive for Business sites. To identify your new custom sensitive information type in existing content, the content must be recrawled. Content is recrawled based on a schedule, but you can manually recrawl content for a site collection, list, or library. For more information, see [Manually request crawling and re-indexing of a site, a library or a list](https://docs.microsoft.com/sharepoint/crawl-site-content).</span></span>

## <a name="create-custom-sensitive-information-types-in-the-security--compliance-center"></a><span data-ttu-id="8ffcc-122">Criar tipos de informações confidenciais personalizados no Centro de Conformidade e Segurança</span><span class="sxs-lookup"><span data-stu-id="8ffcc-122">Create custom sensitive information types in the Security & Compliance Center</span></span>

<span data-ttu-id="8ffcc-123">No Centro de Conformidade e Segurança, acesse **Classificações** \> **Tipos de informações confidenciais** e clique em **Criar**.</span><span class="sxs-lookup"><span data-stu-id="8ffcc-123">In the Security & Compliance Center, go to **Classifications** \> **Sensitive info types** and click **Create**.</span></span>

<span data-ttu-id="8ffcc-124">As configurações são bastante óbvias e são explicadas na página associada do assistente:</span><span class="sxs-lookup"><span data-stu-id="8ffcc-124">The settings are fairly self-evident, and are explained on the associate page of the wizard:</span></span>

- <span data-ttu-id="8ffcc-125">**Nome**</span><span class="sxs-lookup"><span data-stu-id="8ffcc-125">**Name**</span></span>

- <span data-ttu-id="8ffcc-126">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="8ffcc-126">**Description**</span></span>

- <span data-ttu-id="8ffcc-127">**Proximidade**</span><span class="sxs-lookup"><span data-stu-id="8ffcc-127">**Proximity**</span></span>

- <span data-ttu-id="8ffcc-128">**Nível de confiança**</span><span class="sxs-lookup"><span data-stu-id="8ffcc-128">**Confidence level**</span></span>

- <span data-ttu-id="8ffcc-129">**Elemento de padrão principal** (palavras-chave, expressão regular ou dicionário)</span><span class="sxs-lookup"><span data-stu-id="8ffcc-129">**Primary pattern element** (keywords, regular expression, or dictionary)</span></span>

- <span data-ttu-id="8ffcc-130">**Elementos de padrão de suporte** opcionais (palavras-chave, expressão regular ou dicionário) e um valor de **Custo mínimo** correspondente.</span><span class="sxs-lookup"><span data-stu-id="8ffcc-130">Optional **Supporting pattern elements** (keywords, regular expression, or dictionary) and a corresponding **Minimum cost** value.</span></span>

<span data-ttu-id="8ffcc-p107">Aqui está um cenário: você deseja um tipo personalizado de informação confidencial que detecte os números de funcionários com nove dígitos no conteúdo, juntamente com as palavras-chave "funcionário", "ID" e "crachá". Para criar esse tipo personalizado de informação confidencial, faça o seguinte:</span><span class="sxs-lookup"><span data-stu-id="8ffcc-p107">Here's a scenario: You want a custom sensitive information type that detects 9-digit employee numbers in content, along with the keywords "employee" "ID" and "badge". To create this custom sensitive information type, do the following steps:</span></span>

1. <span data-ttu-id="8ffcc-133">No Centro de Conformidade e Segurança, acesse **Classificações** \> **Tipos de informações confidenciais** e clique em **Criar**.</span><span class="sxs-lookup"><span data-stu-id="8ffcc-133">In the Security & Compliance Center, go to **Classifications** \> **Sensitive info types** and click **Create**.</span></span>

    ![Local dos tipos de informações confidenciais e botão Criar](media/scc-cust-sens-info-type-new.png)

2. <span data-ttu-id="8ffcc-135">Na página **Escolher um nome e uma descrição** que é aberta, insira os seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="8ffcc-135">In the **Choose a name and description** page that opens, enter the following values:</span></span>

  - <span data-ttu-id="8ffcc-136">**Nome**: ID de funcionário.</span><span class="sxs-lookup"><span data-stu-id="8ffcc-136">**Name**: Employee ID.</span></span>

  - <span data-ttu-id="8ffcc-137">**Descrição** detectar os números de nove dígitos de ID de funcionário da Contoso.</span><span class="sxs-lookup"><span data-stu-id="8ffcc-137">**Description**: Detect nine-digit Contoso employee ID numbers.</span></span>

    ![Página de nome e descrição](media/scc-cust-sens-info-type-new-name-desc.png)

    <span data-ttu-id="8ffcc-139">Quando terminar, clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="8ffcc-139">When you're finished, click **Next**.</span></span>

3. <span data-ttu-id="8ffcc-140">Na página **Requisitos para correspondência** que é aberta, clique em **Adicionar um elemento** e defina as seguintes configurações:</span><span class="sxs-lookup"><span data-stu-id="8ffcc-140">In the **Requirements for matching** page that opens, click **Add an element** configure the following settings:</span></span>

    - <span data-ttu-id="8ffcc-141">**Detectar conteúdo que tenha**:</span><span class="sxs-lookup"><span data-stu-id="8ffcc-141">**Detect content containing**:</span></span>
 
      <span data-ttu-id="8ffcc-p108">a. Clique em **Qualquer um destes elementos** e selecione **Expressão regular**.</span><span class="sxs-lookup"><span data-stu-id="8ffcc-p108">a. Click **Any of these** and select **Regular expression**.</span></span>

      <span data-ttu-id="8ffcc-p109">b. Na caixa de expressão regular, insira `(\s)(\d{9})(\s)` (números de nove dígitos delimitados por espaço em branco)</span><span class="sxs-lookup"><span data-stu-id="8ffcc-p109">b. In the regular expression box, enter `(\s)(\d{9})(\s)` (nine-digit numbers surrounded by white space).</span></span>
  
    - <span data-ttu-id="8ffcc-146">**Elementos de suporte**: clique em **Adicionar elementos de suporte** e selecione **Contém esta lista de palavras-chave**.</span><span class="sxs-lookup"><span data-stu-id="8ffcc-146">**Supporting elements**: Click **Add supporting elements** and select **Contains this keyword list**.</span></span>

    - <span data-ttu-id="8ffcc-147">Na área **Contém esta lista de palavra-chave** que é exibida, defina as seguintes configurações:</span><span class="sxs-lookup"><span data-stu-id="8ffcc-147">In the **Contains this keyword list** area that appears, configure the following settings:</span></span>

      - <span data-ttu-id="8ffcc-148">**Lista de palavra-chave**: insira o seguinte valor: funcionário,ID,crachá.</span><span class="sxs-lookup"><span data-stu-id="8ffcc-148">**Keyword list**: Enter the following value: employee,ID,badge.</span></span>

      - <span data-ttu-id="8ffcc-149">**Contagem mínima**: mantenha o valor padrão 1.</span><span class="sxs-lookup"><span data-stu-id="8ffcc-149">**Minimum count**: Leave the default value 1.</span></span>

    - <span data-ttu-id="8ffcc-150">Mantenha o valor padrão de 60 para o **Nível de confiança**.</span><span class="sxs-lookup"><span data-stu-id="8ffcc-150">Leave the default **Confidence level** value 60.</span></span> 

    - <span data-ttu-id="8ffcc-151">Mantenha o valor padrão de 300 para a **Proximidade de caracteres**.</span><span class="sxs-lookup"><span data-stu-id="8ffcc-151">Leave the default **Character proximity** value 300.</span></span>

    ![Requisitos para a página correspondente](media/scc-cust-sens-info-type-new-reqs.png)

    <span data-ttu-id="8ffcc-153">Quando terminar, clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="8ffcc-153">When you're finished, click **Next**.</span></span>

4. <span data-ttu-id="8ffcc-154">Na página **Examinar e finalizar** que é aberta, examine as configurações e clique em **Concluir**.</span><span class="sxs-lookup"><span data-stu-id="8ffcc-154">On the **Review and finalize** page that opens, review the settings and click **Finish**.</span></span>

    ![Examine e finalizar a página](media/scc-cust-sens-info-type-new-review.png)

5. <span data-ttu-id="8ffcc-p110">A próxima página incentiva você a testar o novo tipo personalizado de informação confidencial clicando em **Sim**. Para saber mais, confira [Tipos de informações confidenciais personalizados no Centro de Conformidade e Segurança](#test-custom-sensitive-information-types-in-the-security--compliance-center). Para testar a regra mais tarde, clique em **Não**.</span><span class="sxs-lookup"><span data-stu-id="8ffcc-p110">The next page encourages you to test the new custom sensitive information type by clicking **Yes**. For more information, see [Test custom sensitive information types in the Security & Compliance Center](#test-custom-sensitive-information-types-in-the-security--compliance-center). To test the rule later, click **No**.</span></span>

    ![Página de recomendações de teste](media/scc-cust-sens-info-type-new-test.png)

### <a name="how-do-you-know-this-worked"></a><span data-ttu-id="8ffcc-160">Como saber se funcionou?</span><span class="sxs-lookup"><span data-stu-id="8ffcc-160">How do you know this worked?</span></span>

<span data-ttu-id="8ffcc-161">Para confirmar que você criou um novo tipo de informação confidencial com êxito, execute uma destas etapas:</span><span class="sxs-lookup"><span data-stu-id="8ffcc-161">To verify that you've successfully created a new sensitive information type, do any of the following steps:</span></span>

  - <span data-ttu-id="8ffcc-162">Vá para **Classificações** \> **Tipos de informações confidenciais** e verifique se o novo tipo personalizado de informações confidenciais está listado.</span><span class="sxs-lookup"><span data-stu-id="8ffcc-162">Go to **Classifications** \> **Sensitive info types** and verify the new custom sensitive information type is listed.</span></span>

  - <span data-ttu-id="8ffcc-p111">Teste o novo tipo personalizado de informação confidencial. Para saber mais, confira [Testar tipos de informações confidenciais personalizados no Centro de Conformidade e Segurança](#test-custom-sensitive-information-types-in-the-security--compliance-center).</span><span class="sxs-lookup"><span data-stu-id="8ffcc-p111">Test the new custom sensitive information type. For more information, see [Test custom sensitive information types in the Security & Compliance Center](#test-custom-sensitive-information-types-in-the-security--compliance-center).</span></span>

## <a name="modify-custom-sensitive-information-types-in-the-security--compliance-center"></a><span data-ttu-id="8ffcc-165">Modificar tipos de informações confidenciais personalizados no Centro de Conformidade e Segurança</span><span class="sxs-lookup"><span data-stu-id="8ffcc-165">Modify custom sensitive information types in the Security & Compliance Center</span></span>

<span data-ttu-id="8ffcc-166">**Observações**:</span><span class="sxs-lookup"><span data-stu-id="8ffcc-166">**Notes**:</span></span>

- <span data-ttu-id="8ffcc-p112">Você só pode modificar tipos de informações confidenciais personalizados. Não é possível modificar tipos internos de informações confidenciais. Porém, você pode usar o PowerShell para exportar tipos de informações confidenciais personalizados internos, personalizá-los e importá-los como tipos de informações confidenciais personalizados. Para saber mais, confira [Personalizar um tipo de informação confidencial interno](customize-a-built-in-sensitive-information-type.md).</span><span class="sxs-lookup"><span data-stu-id="8ffcc-p112">You can only modify custom sensitive information types; you can't modify built-in sensitive information types. But you can use PowerShell to export built-in custom sensitive information types, customize them, and import them as custom sensitive information types. For more information, see [Customize a built-in sensitive information type](customize-a-built-in-sensitive-information-type.md).</span></span>

- <span data-ttu-id="8ffcc-p113">Somente você pode modificar os tipos de informações confidenciais personalizados que criou na interface do usuário. Se você tiver usado o [procedimento do PowerShell](create-a-custom-sensitive-information-type-in-scc-powershell.md) para importar um pacote de regras de tipo personalizado de informações confidenciais, você receberá um erro.</span><span class="sxs-lookup"><span data-stu-id="8ffcc-p113">You can only modify custom sensitive information types that you created in the UI. If you used the [PowerShell procedure](create-a-custom-sensitive-information-type-in-scc-powershell.md) to import a custom sensitive information type rule package, you'll get an error.</span></span>

<span data-ttu-id="8ffcc-172">No Centro de Conformidade e Segurança, acesse **Classificações** \> **Tipos de informações confidenciais**, selecione os tipos de informações confidenciais personalizados que você deseja modificar e clique em **Editar**.</span><span class="sxs-lookup"><span data-stu-id="8ffcc-172">In the Security & Compliance Center, go to **Classifications** \> **Sensitive info types**, select the custom sensitive information type that you want to modify, and then click **Edit**.</span></span>

  ![Local dos tipos de informações confidenciais e botão Editar](media/scc-cust-sens-info-type-edit.png)

<span data-ttu-id="8ffcc-p114">Aqui estão disponíveis as mesmas opções oferecidas quando você criou o tipo de informação confidencial personalizado no Centro de Conformidade e Segurança. Para saber mais, confira [Criar tipos de informações confidenciais personalizados no Centro de Conformidade e Segurança](#create-custom-sensitive-information-types-in-the-security--compliance-center).</span><span class="sxs-lookup"><span data-stu-id="8ffcc-p114">The same options are available here as when you created the custom sensitive information type in the Security & Compliance Center. For more information, see [Create custom sensitive information types in the Security & Compliance Center](#create-custom-sensitive-information-types-in-the-security--compliance-center).</span></span>

### <a name="how-do-you-know-this-worked"></a><span data-ttu-id="8ffcc-176">Como saber se funcionou?</span><span class="sxs-lookup"><span data-stu-id="8ffcc-176">How do you know this worked?</span></span>

<span data-ttu-id="8ffcc-177">Para confirmar que você modificou um tipo de informação confidencial com êxito, execute uma destas etapas:</span><span class="sxs-lookup"><span data-stu-id="8ffcc-177">To verify that you've successfully modified a sensitive information type, do any of the following steps:</span></span>

  - <span data-ttu-id="8ffcc-178">Vá para **classificações** \> **Tipos de informações confidenciais** para verificar as propriedades do tipo personalizado de informação confidencial modificado.</span><span class="sxs-lookup"><span data-stu-id="8ffcc-178">Go to **Classifications** \> **Sensitive info types** to verify the properties of the modified custom sensitive information type.</span></span> 

  - <span data-ttu-id="8ffcc-p115">Teste o tipo personalizado de informação confidencial modificada. Para saber mais, confira [Testar tipos de informações confidenciais personalizados no Centro de Conformidade e Segurança](#test-custom-sensitive-information-types-in-the-security--compliance-center).</span><span class="sxs-lookup"><span data-stu-id="8ffcc-p115">Test the modified custom sensitive information type. For more information, see [Test custom sensitive information types in the Security & Compliance Center](#test-custom-sensitive-information-types-in-the-security--compliance-center).</span></span>

## <a name="remove-custom-sensitive-information-types-in-the-security--compliance-center"></a><span data-ttu-id="8ffcc-181">Remover tipos de informações confidenciais personalizados no Centro de Conformidade e Segurança</span><span class="sxs-lookup"><span data-stu-id="8ffcc-181">Remove custom sensitive information types in the Security & Compliance Center</span></span> 

<span data-ttu-id="8ffcc-182">**Observações**:</span><span class="sxs-lookup"><span data-stu-id="8ffcc-182">**Notes**:</span></span>

- <span data-ttu-id="8ffcc-183">Você só pode remover tipos de informações confidenciais personalizados. Não é possível remover tipos internos de informações confidenciais.</span><span class="sxs-lookup"><span data-stu-id="8ffcc-183">You can only remove custom sensitive information types; you can't remove built-in sensitive information types.</span></span>

- <span data-ttu-id="8ffcc-184">Antes de remover um tipo personalizado de informação confidencial, verifique se nenhuma política de DLP ou regras de fluxo de emails do Exchange (também conhecidas como regras de transporte) ainda fazem referência ao tipo de informação confidencial.</span><span class="sxs-lookup"><span data-stu-id="8ffcc-184">Before your remove a custom sensitive information type, verify that no DLP policies or Exchange mail flow rules (also known as transport rules) still reference the sensitive information type.</span></span>

1. <span data-ttu-id="8ffcc-185">No Centro de Conformidade e Segurança, acesse **Classificações** \> **Tipos de informações confidenciais** e selecione um ou mais tipos de informações confidenciais personalizados que você deseja remover.</span><span class="sxs-lookup"><span data-stu-id="8ffcc-185">In the Security & Compliance Center, go to **Classifications** \> **Sensitive info types** and select one or more custom sensitive information types that you want to remove.</span></span>

2. <span data-ttu-id="8ffcc-186">No submenu que é aberto, clique em **Excluir** (ou **Excluir tipos de informações confidenciais** se você tiver selecionado mais de um).</span><span class="sxs-lookup"><span data-stu-id="8ffcc-186">In the fly-out that opens, click **Delete** (or **Delete sensitive info types** if you selected more than one).</span></span>

    ![Local dos tipos de informações confidenciais e botão Excluir](media/scc-cust-sens-info-type-delete.png)

3. <span data-ttu-id="8ffcc-188">Na mensagem de aviso exibida, clique em **Sim**.</span><span class="sxs-lookup"><span data-stu-id="8ffcc-188">In the warning message that appears, click **Yes**.</span></span>

### <a name="how-do-you-know-this-worked"></a><span data-ttu-id="8ffcc-189">Como saber se funcionou?</span><span class="sxs-lookup"><span data-stu-id="8ffcc-189">How do you know this worked?</span></span>

<span data-ttu-id="8ffcc-190">Para verificar se você removeu um tipo personalizado de informação confidencial com êxito, vá até **Classificações** \> **Tipos de informações confidenciais** para verificar se o tipo personalizado de informação confidencial não está mais presente.</span><span class="sxs-lookup"><span data-stu-id="8ffcc-190">To verify that you've successfully removed a custom sensitive information type, go to **Classifications** \> **Sensitive info types** to verify the custom sensitive information type is no longer listed.</span></span>

## <a name="test-custom-sensitive-information-types-in-the-security--compliance-center"></a><span data-ttu-id="8ffcc-191">Teste tipos de informações confidenciais personalizados no Centro de Conformidade e Segurança</span><span class="sxs-lookup"><span data-stu-id="8ffcc-191">Test custom sensitive information types in the Security & Compliance Center</span></span>

1. <span data-ttu-id="8ffcc-192">No Centro de Conformidade e Segurança, acesse **Classificações** \> **Tipos de informações confidenciais**.</span><span class="sxs-lookup"><span data-stu-id="8ffcc-192">In the Security & Compliance Center, go to **Classifications** \> **Sensitive info types**.</span></span>

2. <span data-ttu-id="8ffcc-p116">Selecione um ou mais tipos de informações confidenciais personalizados para testar. No submenu suspenso que é aberto, clique em **Testar tipo** (ou **Testar tipos de informações confidenciais** se você tiver selecionado mais de um).</span><span class="sxs-lookup"><span data-stu-id="8ffcc-p116">Select one or more custom sensitive information types to test. In the fly-out that opens, click **Test type** (or **Test sensitive info types** if you selected more than one).</span></span>

    ![Local dos tipos de informações confidenciais e botão de tipo de Teste](media/scc-cust-sens-info-type-test.png)

3. <span data-ttu-id="8ffcc-196">Na página **Carregar arquivo para teste** que se abre, carregue um documento para teste arrastando e soltando um arquivo, ou então clicando em **Procurar** e selecionando um arquivo.</span><span class="sxs-lookup"><span data-stu-id="8ffcc-196">On the **Upload file to test** page that opens, upload a document to test by dragging and dropping a file or by clicking **Browse** and selecting a file.</span></span>

    ![Carregar arquivos na página de teste](media/scc-cust-sens-info-type-test-upload.png)

4. <span data-ttu-id="8ffcc-198">Clique no botão **Testar** para testar o documento em busca de correspondências de padrão no arquivo.</span><span class="sxs-lookup"><span data-stu-id="8ffcc-198">Click the **Test** button to test the document for pattern matches in the file.</span></span>

5. <span data-ttu-id="8ffcc-199">Na página **Resultados da correspondência**, clique em **Concluir**.</span><span class="sxs-lookup"><span data-stu-id="8ffcc-199">On the **Match results** page, click **Finish**.</span></span>

    ![Resultados da correspondência](media/scc-cust-sens-info-type-test-results.png)