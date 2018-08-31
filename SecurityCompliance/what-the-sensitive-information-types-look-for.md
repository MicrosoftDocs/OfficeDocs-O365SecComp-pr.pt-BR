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
ms.openlocfilehash: 064606085363ba9de972511642993277451c8ce3
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22524429"
---
# <a name="what-the-sensitive-information-types-look-for"></a><span data-ttu-id="ab3ec-104">O que os tipos de informações confidenciais procuram</span><span class="sxs-lookup"><span data-stu-id="ab3ec-104">What the sensitive information types look for</span></span>

<span data-ttu-id="ab3ec-p102">Prevenção de perda de dados (DLP) no Office 365 Security &amp; Centro de conformidade inclui muitos tipos de informações confidenciais que estão prontos para uso em suas políticas de DLP. Este tópico lista todos esses tipos de informações confidenciais e mostra o que uma política de DLP procura por quando detecta cada tipo. Um tipo de informação confidencial é definido por um padrão que pode ser identificado por uma função ou uma expressão regular. Além disso, a evidência corroborativa como palavras-chave e somas de verificação pode ser usada para identificar um tipo de informações confidenciais. Proximidade e nível de confiança também são usados no processo de avaliação.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-p102">Data loss prevention (DLP) in the Office 365 Security &amp; Compliance Center includes many sensitive information types that are ready for you to use in your DLP policies. This topic lists all of these sensitive information types and shows what a DLP policy looks for when it detects each type. A sensitive information type is defined by a pattern that can be identified by a regular expression or a function. In addition, corroborative evidence such as keywords and checksums can be used to identify a sensitive information type. Confidence level and proximity are also used in the evaluation process.</span></span>
  
## <a name="aba-routing-number"></a><span data-ttu-id="ab3ec-110">Número de roteamento ABA</span><span class="sxs-lookup"><span data-stu-id="ab3ec-110">ABA Routing Number</span></span>

### <a name="format"></a><span data-ttu-id="ab3ec-111">Formato</span><span class="sxs-lookup"><span data-stu-id="ab3ec-111">Format</span></span>

<span data-ttu-id="ab3ec-112">9 dígitos que podem estar em um padrão formatado ou não formatado</span><span class="sxs-lookup"><span data-stu-id="ab3ec-112">9 digits which may be in a formatted or unformatted pattern</span></span>

### <a name="pattern"></a><span data-ttu-id="ab3ec-113">Padrão</span><span class="sxs-lookup"><span data-stu-id="ab3ec-113">Pattern</span></span>

<span data-ttu-id="ab3ec-114">Formatado:</span><span class="sxs-lookup"><span data-stu-id="ab3ec-114">Formatted:</span></span>
- <span data-ttu-id="ab3ec-115">Quatro dígitos, começando com 0, 1, 2, 3, 6, 7 ou 8</span><span class="sxs-lookup"><span data-stu-id="ab3ec-115">Four digits beginning with 0, 1, 2, 3, 6, 7, or 8</span></span>
- <span data-ttu-id="ab3ec-116">Um hífen</span><span class="sxs-lookup"><span data-stu-id="ab3ec-116">A hyphen</span></span>
- <span data-ttu-id="ab3ec-117">Quatro dígitos</span><span class="sxs-lookup"><span data-stu-id="ab3ec-117">Four digits</span></span>
- <span data-ttu-id="ab3ec-118">Um hífen</span><span class="sxs-lookup"><span data-stu-id="ab3ec-118">A hyphen</span></span>
- <span data-ttu-id="ab3ec-119">Um dígito</span><span class="sxs-lookup"><span data-stu-id="ab3ec-119">A digit</span></span>

<span data-ttu-id="ab3ec-120">Não formatada: 9 dígitos consecutivos começando com 0, 1, 2, 3, 6, 7 ou 8</span><span class="sxs-lookup"><span data-stu-id="ab3ec-120">Unformatted: 9 consecutive digits beginning with 0, 1, 2, 3, 6, 7, or 8</span></span> 

### <a name="checksum"></a><span data-ttu-id="ab3ec-121">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="ab3ec-121">Checksum</span></span>

<span data-ttu-id="ab3ec-122">Não</span><span class="sxs-lookup"><span data-stu-id="ab3ec-122">No</span></span>

### <a name="definition"></a><span data-ttu-id="ab3ec-123">Definição</span><span class="sxs-lookup"><span data-stu-id="ab3ec-123">Definition</span></span>

<span data-ttu-id="ab3ec-124">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="ab3ec-124">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="ab3ec-125">A função Func_aba_routing localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-125">The function Func_aba_routing finds content that matches the pattern.</span></span>
- <span data-ttu-id="ab3ec-126">Uma palavra-chave de Keyword_ABA_Routing for encontrada.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-126">A keyword from Keyword_ABA_Routing is found.</span></span>

```
<!-- ABA Routing Number -->
<Entity id="cb353f78-2b72-4c3c-8827-92ebe4f69fdf" patternsProximity="300" recommendedConfidence="75">
      <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_aba_routing" />
        <Match idRef="Keyword_ABA_Routing" />
      </Pattern>
 </Entity>
```


### <a name="keywords"></a><span data-ttu-id="ab3ec-127">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="ab3ec-127">Keywords</span></span>

#### <a name="keywordabarouting"></a><span data-ttu-id="ab3ec-128">Keyword_ABA_Routing</span><span class="sxs-lookup"><span data-stu-id="ab3ec-128">Keyword_ABA_Routing</span></span>

- <span data-ttu-id="ab3ec-129">aba</span><span class="sxs-lookup"><span data-stu-id="ab3ec-129">aba</span></span>
- <span data-ttu-id="ab3ec-130">
aba #</span><span class="sxs-lookup"><span data-stu-id="ab3ec-130">aba #</span></span>
- <span data-ttu-id="ab3ec-131">
aba routing #</span><span class="sxs-lookup"><span data-stu-id="ab3ec-131">aba routing #</span></span>
- <span data-ttu-id="ab3ec-132">
aba routing number</span><span class="sxs-lookup"><span data-stu-id="ab3ec-132">aba routing number</span></span>
- <span data-ttu-id="ab3ec-133">
aba#</span><span class="sxs-lookup"><span data-stu-id="ab3ec-133">aba#</span></span>
- <span data-ttu-id="ab3ec-134">
abarouting#</span><span class="sxs-lookup"><span data-stu-id="ab3ec-134">abarouting#</span></span>
- <span data-ttu-id="ab3ec-135">
aba number</span><span class="sxs-lookup"><span data-stu-id="ab3ec-135">aba number</span></span>
- <span data-ttu-id="ab3ec-136">
abaroutingnumber</span><span class="sxs-lookup"><span data-stu-id="ab3ec-136">abaroutingnumber</span></span>
- <span data-ttu-id="ab3ec-137">
american bank association routing #</span><span class="sxs-lookup"><span data-stu-id="ab3ec-137">american bank association routing #</span></span>
- <span data-ttu-id="ab3ec-138">
american bank association routing number</span><span class="sxs-lookup"><span data-stu-id="ab3ec-138">american bank association routing number</span></span>
- <span data-ttu-id="ab3ec-139">
americanbankassociationrouting#</span><span class="sxs-lookup"><span data-stu-id="ab3ec-139">americanbankassociationrouting#</span></span>
- <span data-ttu-id="ab3ec-140">
americanbankassociationroutingnumber</span><span class="sxs-lookup"><span data-stu-id="ab3ec-140">americanbankassociationroutingnumber</span></span>
- <span data-ttu-id="ab3ec-141">
bank routing number</span><span class="sxs-lookup"><span data-stu-id="ab3ec-141">bank routing number</span></span>
- <span data-ttu-id="ab3ec-142">
bankrouting#</span><span class="sxs-lookup"><span data-stu-id="ab3ec-142">bankrouting#</span></span>
- <span data-ttu-id="ab3ec-143">
bankroutingnumber</span><span class="sxs-lookup"><span data-stu-id="ab3ec-143">bankroutingnumber</span></span>
- <span data-ttu-id="ab3ec-144">
routing transit number</span><span class="sxs-lookup"><span data-stu-id="ab3ec-144">routing transit number</span></span>
- <span data-ttu-id="ab3ec-145">
RTN
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-145">RTN</span></span> 
   
## <a name="argentina-national-identity-dni-number"></a><span data-ttu-id="ab3ec-146">Número de Identidade Nacional (DNI) da Argentina</span><span class="sxs-lookup"><span data-stu-id="ab3ec-146">Argentina National Identity (DNI) Number</span></span>

### <a name="format"></a><span data-ttu-id="ab3ec-147">Formato</span><span class="sxs-lookup"><span data-stu-id="ab3ec-147">Format</span></span>

<span data-ttu-id="ab3ec-148">Oito dígitos separados por pontos</span><span class="sxs-lookup"><span data-stu-id="ab3ec-148">Eight digits separated by periods</span></span>

### <a name="pattern"></a><span data-ttu-id="ab3ec-149">Padrão</span><span class="sxs-lookup"><span data-stu-id="ab3ec-149">Pattern</span></span>

<span data-ttu-id="ab3ec-150">Oito dígitos:</span><span class="sxs-lookup"><span data-stu-id="ab3ec-150">Eight digits:</span></span>
- <span data-ttu-id="ab3ec-151">Dois dígitos</span><span class="sxs-lookup"><span data-stu-id="ab3ec-151">Two digits</span></span>
- <span data-ttu-id="ab3ec-152">Um ponto </span><span class="sxs-lookup"><span data-stu-id="ab3ec-152">A period</span></span>
- <span data-ttu-id="ab3ec-153">Três dígitos</span><span class="sxs-lookup"><span data-stu-id="ab3ec-153">Three digits</span></span>
- <span data-ttu-id="ab3ec-154">Um ponto </span><span class="sxs-lookup"><span data-stu-id="ab3ec-154">A period</span></span>
- <span data-ttu-id="ab3ec-155">Três dígitos</span><span class="sxs-lookup"><span data-stu-id="ab3ec-155">Three digits</span></span>

### <a name="checksum"></a><span data-ttu-id="ab3ec-156">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="ab3ec-156">Checksum</span></span>

<span data-ttu-id="ab3ec-157">Não</span><span class="sxs-lookup"><span data-stu-id="ab3ec-157">No</span></span>

### <a name="definition"></a><span data-ttu-id="ab3ec-158">Definição</span><span class="sxs-lookup"><span data-stu-id="ab3ec-158">Definition</span></span>

<span data-ttu-id="ab3ec-159">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="ab3ec-159">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="ab3ec-160">A expressão regular Regex_argentina_national_id encontra o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-160">The regular expression Regex_argentina_national_id finds content that matches the pattern.</span></span>
- <span data-ttu-id="ab3ec-161">Uma palavra-chave de Keyword_argentina_national_id é encontrada.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-161">A keyword from Keyword_argentina_national_id is found.</span></span>

```
<!-- Argentina National Identity (DNI) Number -->
<Entity id="eefbb00e-8282-433c-8620-8f1da3bffdb2" recommendedConfidence="75" patternsProximity="300">
   <Pattern confidenceLevel="75">
      <IdMatch idRef="Regex_argentina_national_id"/>
      <Match idRef="Keyword_argentina_national_id"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="ab3ec-162">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="ab3ec-162">Keywords</span></span>

#### <a name="keywordargentinanationalid"></a><span data-ttu-id="ab3ec-163">Keyword_argentina_national_id</span><span class="sxs-lookup"><span data-stu-id="ab3ec-163">Keyword_argentina_national_id</span></span>

- <span data-ttu-id="ab3ec-164">Número de Identidade Nacional da Argentina
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-164">Argentina National Identity number</span></span> 
- <span data-ttu-id="ab3ec-165">Identidade</span><span class="sxs-lookup"><span data-stu-id="ab3ec-165">Identity</span></span> 
- <span data-ttu-id="ab3ec-166">Cartão de identificação nacional de identidade</span><span class="sxs-lookup"><span data-stu-id="ab3ec-166">Identification National Identity Card</span></span> 
- <span data-ttu-id="ab3ec-167">DNI
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-167">DNI</span></span> 
- <span data-ttu-id="ab3ec-168">Registro NIC nacional de pessoas</span><span class="sxs-lookup"><span data-stu-id="ab3ec-168">NIC National Registry of Persons</span></span> 
- <span data-ttu-id="ab3ec-169">Documento Nacional de Identidad
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-169">Documento Nacional de Identidad</span></span> 
- <span data-ttu-id="ab3ec-170">Registro Nacional de las Personas
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-170">Registro Nacional de las Personas</span></span> 
- <span data-ttu-id="ab3ec-171">Identidad
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-171">Identidad</span></span> 
- <span data-ttu-id="ab3ec-172">Identificación
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-172">Identificación</span></span> 
   
## <a name="australia-bank-account-number"></a><span data-ttu-id="ab3ec-173">Número de conta de banco da Austrália</span><span class="sxs-lookup"><span data-stu-id="ab3ec-173">Australia Bank Account Number</span></span>

### <a name="format"></a><span data-ttu-id="ab3ec-174">Formato</span><span class="sxs-lookup"><span data-stu-id="ab3ec-174">Format</span></span>

<span data-ttu-id="ab3ec-175">6 a 10 dígitos com ou sem um número BSB</span><span class="sxs-lookup"><span data-stu-id="ab3ec-175">6-10 digits with or without a bank state branch number</span></span>

### <a name="pattern"></a><span data-ttu-id="ab3ec-176">Padrão</span><span class="sxs-lookup"><span data-stu-id="ab3ec-176">Pattern</span></span>

<span data-ttu-id="ab3ec-p103">Número de conta é 6-10 dígitos. Número de filial do estado de banco da Austrália:</span><span class="sxs-lookup"><span data-stu-id="ab3ec-p103">Account number is 6-10 digits. Australia bank state branch number:</span></span>
- <span data-ttu-id="ab3ec-179">Três dígitos</span><span class="sxs-lookup"><span data-stu-id="ab3ec-179">Three digits</span></span> 
- <span data-ttu-id="ab3ec-180">Um hífen</span><span class="sxs-lookup"><span data-stu-id="ab3ec-180">A hyphen</span></span> 
- <span data-ttu-id="ab3ec-181">Três dígitos</span><span class="sxs-lookup"><span data-stu-id="ab3ec-181">Three digits</span></span>

### <a name="checksum"></a><span data-ttu-id="ab3ec-182">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="ab3ec-182">Checksum</span></span>

<span data-ttu-id="ab3ec-183">Não</span><span class="sxs-lookup"><span data-stu-id="ab3ec-183">No</span></span>

### <a name="definition"></a><span data-ttu-id="ab3ec-184">Definição</span><span class="sxs-lookup"><span data-stu-id="ab3ec-184">Definition</span></span>

<span data-ttu-id="ab3ec-185">Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="ab3ec-185">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="ab3ec-186">A expressão regular Regex_australia_bank_account_number localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-186">The regular expression Regex_australia_bank_account_number finds content that matches the pattern..</span></span>
- <span data-ttu-id="ab3ec-187">Uma palavra-chave de Keyword_australia_bank_account_number for encontrada.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-187">A keyword from Keyword_australia_bank_account_number is found.</span></span>
- <span data-ttu-id="ab3ec-188">A expressão regular Regex_australia_bank_account_number_bsb localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-188">The regular expression Regex_australia_bank_account_number_bsb finds content that matches the pattern.</span></span>

<span data-ttu-id="ab3ec-189">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="ab3ec-189">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="ab3ec-190">A expressão regular Regex_australia_bank_account_number localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-190">The regular expression Regex_australia_bank_account_number finds content that matches the pattern..</span></span>
- <span data-ttu-id="ab3ec-191">Uma palavra-chave de Keyword_australia_bank_account_number for encontrada.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-191">A keyword from Keyword_australia_bank_account_number is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="ab3ec-192">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="ab3ec-192">Keywords</span></span>

#### <a name="keywordaustraliabankaccountnumber"></a><span data-ttu-id="ab3ec-193">Keyword_australia_bank_account_number</span><span class="sxs-lookup"><span data-stu-id="ab3ec-193">Keyword_australia_bank_account_number</span></span>

- <span data-ttu-id="ab3ec-194">swift bank code</span><span class="sxs-lookup"><span data-stu-id="ab3ec-194">swift bank code</span></span>
- <span data-ttu-id="ab3ec-195">
correspondent bank</span><span class="sxs-lookup"><span data-stu-id="ab3ec-195">correspondent bank</span></span>
- <span data-ttu-id="ab3ec-196">
base currency</span><span class="sxs-lookup"><span data-stu-id="ab3ec-196">base currency</span></span>
- <span data-ttu-id="ab3ec-197">
usa account</span><span class="sxs-lookup"><span data-stu-id="ab3ec-197">usa account</span></span>
- <span data-ttu-id="ab3ec-198">
holder address</span><span class="sxs-lookup"><span data-stu-id="ab3ec-198">holder address</span></span>
- <span data-ttu-id="ab3ec-199">
bank address</span><span class="sxs-lookup"><span data-stu-id="ab3ec-199">bank address</span></span>
- <span data-ttu-id="ab3ec-200">
information account</span><span class="sxs-lookup"><span data-stu-id="ab3ec-200">information account</span></span>
- <span data-ttu-id="ab3ec-201">
fund transfers</span><span class="sxs-lookup"><span data-stu-id="ab3ec-201">fund transfers</span></span>
- <span data-ttu-id="ab3ec-202">
bank charges</span><span class="sxs-lookup"><span data-stu-id="ab3ec-202">bank charges</span></span>
- <span data-ttu-id="ab3ec-203">
bank details</span><span class="sxs-lookup"><span data-stu-id="ab3ec-203">bank details</span></span>
- <span data-ttu-id="ab3ec-204">
banking information</span><span class="sxs-lookup"><span data-stu-id="ab3ec-204">banking information</span></span>
- <span data-ttu-id="ab3ec-205">
full names</span><span class="sxs-lookup"><span data-stu-id="ab3ec-205">full names</span></span>
- <span data-ttu-id="ab3ec-206">

iaea</span><span class="sxs-lookup"><span data-stu-id="ab3ec-206">iaea</span></span>

   
## <a name="australia-drivers-license-number"></a><span data-ttu-id="ab3ec-207">Número de carteira de motorista da Austrália</span><span class="sxs-lookup"><span data-stu-id="ab3ec-207">Australia Driver's License Number</span></span>

### <a name="format"></a><span data-ttu-id="ab3ec-208">Formato</span><span class="sxs-lookup"><span data-stu-id="ab3ec-208">Format</span></span>

<span data-ttu-id="ab3ec-209">Nove letras e dígitos</span><span class="sxs-lookup"><span data-stu-id="ab3ec-209">Nine letters and digits</span></span>

### <a name="pattern"></a><span data-ttu-id="ab3ec-210">Padrão</span><span class="sxs-lookup"><span data-stu-id="ab3ec-210">Pattern</span></span>

<span data-ttu-id="ab3ec-211">Nove letras e dígitos:</span><span class="sxs-lookup"><span data-stu-id="ab3ec-211">Nine letters and digits:</span></span> 

- <span data-ttu-id="ab3ec-212">Dois dígitos ou letras (não diferenciam maiúsculas de minúsculas)</span><span class="sxs-lookup"><span data-stu-id="ab3ec-212">Two digits or letters (not case sensitive)</span></span> 
- <span data-ttu-id="ab3ec-213">Dois dígitos</span><span class="sxs-lookup"><span data-stu-id="ab3ec-213">Two digits</span></span> 
- <span data-ttu-id="ab3ec-214">Cinco dígitos ou letras (não diferenciam maiúsculas de minúsculas)</span><span class="sxs-lookup"><span data-stu-id="ab3ec-214">Five digits or letters (not case sensitive)</span></span>

<span data-ttu-id="ab3ec-215">OU</span><span class="sxs-lookup"><span data-stu-id="ab3ec-215">OR</span></span>

- <span data-ttu-id="ab3ec-216">1 a 2 letras opcionais (não diferenciam maiúsculas de minúsculas)</span><span class="sxs-lookup"><span data-stu-id="ab3ec-216">1-2 optional letters (not case sensitive)</span></span> 
- <span data-ttu-id="ab3ec-217">4 a 9 dígitos</span><span class="sxs-lookup"><span data-stu-id="ab3ec-217">4-9 digits</span></span>

<span data-ttu-id="ab3ec-218">OU</span><span class="sxs-lookup"><span data-stu-id="ab3ec-218">OR</span></span>

- <span data-ttu-id="ab3ec-219">Nove dígitos ou letras (não diferenciam maiúsculas de minúsculas)</span><span class="sxs-lookup"><span data-stu-id="ab3ec-219">Nine digits or letters (not case sensitive)</span></span>

### <a name="checksum"></a><span data-ttu-id="ab3ec-220">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="ab3ec-220">Checksum</span></span>

<span data-ttu-id="ab3ec-221">Não</span><span class="sxs-lookup"><span data-stu-id="ab3ec-221">No</span></span>

### <a name="definition"></a><span data-ttu-id="ab3ec-222">Definição</span><span class="sxs-lookup"><span data-stu-id="ab3ec-222">Definition</span></span>

<span data-ttu-id="ab3ec-223">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="ab3ec-223">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="ab3ec-224">A expressão regular Regex_australia_drivers_license_number localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-224">The regular expression Regex_australia_drivers_license_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="ab3ec-225">Uma palavra-chave de Keyword_australia_drivers_license_number for encontrada.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-225">A keyword from Keyword_australia_drivers_license_number is found.</span></span>
- <span data-ttu-id="ab3ec-226">Nenhuma palavra-chave de Keyword_australia_drivers_license_number_exclusions for encontrada.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-226">No keyword from Keyword_australia_drivers_license_number_exclusions is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="ab3ec-227">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="ab3ec-227">Keywords</span></span>

#### <a name="keywordaustraliadriverslicensenumber"></a><span data-ttu-id="ab3ec-228">Keyword_australia_drivers_license_number</span><span class="sxs-lookup"><span data-stu-id="ab3ec-228">Keyword_australia_drivers_license_number</span></span>

- <span data-ttu-id="ab3ec-229">international driving permits</span><span class="sxs-lookup"><span data-stu-id="ab3ec-229">international driving permits</span></span>
- <span data-ttu-id="ab3ec-230">
australian automobile association</span><span class="sxs-lookup"><span data-stu-id="ab3ec-230">australian automobile association</span></span>
- <span data-ttu-id="ab3ec-231">
sydney nsw</span><span class="sxs-lookup"><span data-stu-id="ab3ec-231">sydney nsw</span></span>
- <span data-ttu-id="ab3ec-232">
international driving permit</span><span class="sxs-lookup"><span data-stu-id="ab3ec-232">international driving permit</span></span>
- <span data-ttu-id="ab3ec-233">DriverLicence</span><span class="sxs-lookup"><span data-stu-id="ab3ec-233">DriverLicence</span></span>
- <span data-ttu-id="ab3ec-234">DriverLicences</span><span class="sxs-lookup"><span data-stu-id="ab3ec-234">DriverLicences</span></span>
- <span data-ttu-id="ab3ec-235">Driver Lic</span><span class="sxs-lookup"><span data-stu-id="ab3ec-235">Driver Lic</span></span>
- <span data-ttu-id="ab3ec-236">Driver Licence
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-236">Driver Licence</span></span>
- <span data-ttu-id="ab3ec-237">Driver Licences
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-237">Driver Licences</span></span>
- <span data-ttu-id="ab3ec-238">DriversLic</span><span class="sxs-lookup"><span data-stu-id="ab3ec-238">DriversLic</span></span>
- <span data-ttu-id="ab3ec-239">DriversLicence</span><span class="sxs-lookup"><span data-stu-id="ab3ec-239">DriversLicence</span></span>
- <span data-ttu-id="ab3ec-240">DriversLicences</span><span class="sxs-lookup"><span data-stu-id="ab3ec-240">DriversLicences</span></span>
- <span data-ttu-id="ab3ec-241">Drivers Lic</span><span class="sxs-lookup"><span data-stu-id="ab3ec-241">Drivers Lic</span></span>
- <span data-ttu-id="ab3ec-242">Drivers Lics</span><span class="sxs-lookup"><span data-stu-id="ab3ec-242">Drivers Lics</span></span>
- <span data-ttu-id="ab3ec-243">Drivers de licença</span><span class="sxs-lookup"><span data-stu-id="ab3ec-243">Drivers Licence</span></span>
- <span data-ttu-id="ab3ec-244">Licenças de drivers</span><span class="sxs-lookup"><span data-stu-id="ab3ec-244">Drivers Licences</span></span>
- <span data-ttu-id="ab3ec-245">Driver'Lic</span><span class="sxs-lookup"><span data-stu-id="ab3ec-245">Driver'Lic</span></span>
- <span data-ttu-id="ab3ec-246">Driver'Lics</span><span class="sxs-lookup"><span data-stu-id="ab3ec-246">Driver'Lics</span></span>
- <span data-ttu-id="ab3ec-247">Driver'Licence</span><span class="sxs-lookup"><span data-stu-id="ab3ec-247">Driver'Licence</span></span>
- <span data-ttu-id="ab3ec-248">Driver'Licences</span><span class="sxs-lookup"><span data-stu-id="ab3ec-248">Driver'Licences</span></span>
- <span data-ttu-id="ab3ec-249">Driver' Lic</span><span class="sxs-lookup"><span data-stu-id="ab3ec-249">Driver' Lic</span></span>
- <span data-ttu-id="ab3ec-250">Driver' Lics</span><span class="sxs-lookup"><span data-stu-id="ab3ec-250">Driver' Lics</span></span>
- <span data-ttu-id="ab3ec-251">Driver' licença</span><span class="sxs-lookup"><span data-stu-id="ab3ec-251">Driver' Licence</span></span>
- <span data-ttu-id="ab3ec-252">Driver' licenças</span><span class="sxs-lookup"><span data-stu-id="ab3ec-252">Driver' Licences</span></span>
- <span data-ttu-id="ab3ec-253">Driver'sLic</span><span class="sxs-lookup"><span data-stu-id="ab3ec-253">Driver'sLic</span></span>
- <span data-ttu-id="ab3ec-254">Driver'sLics</span><span class="sxs-lookup"><span data-stu-id="ab3ec-254">Driver'sLics</span></span>
- <span data-ttu-id="ab3ec-255">Driver'sLicence</span><span class="sxs-lookup"><span data-stu-id="ab3ec-255">Driver'sLicence</span></span>
- <span data-ttu-id="ab3ec-256">Driver'sLicences</span><span class="sxs-lookup"><span data-stu-id="ab3ec-256">Driver'sLicences</span></span>
- <span data-ttu-id="ab3ec-257">Lic do driver</span><span class="sxs-lookup"><span data-stu-id="ab3ec-257">Driver's Lic</span></span>
- <span data-ttu-id="ab3ec-258">Lics do driver</span><span class="sxs-lookup"><span data-stu-id="ab3ec-258">Driver's Lics</span></span>
- <span data-ttu-id="ab3ec-259">Driver's Licence
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-259">Driver's Licence</span></span>
- <span data-ttu-id="ab3ec-260">Driver's Licences
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-260">Driver's Licences</span></span>
- <span data-ttu-id="ab3ec-261">DriverLic #</span><span class="sxs-lookup"><span data-stu-id="ab3ec-261">DriverLic#</span></span>
- <span data-ttu-id="ab3ec-262">DriverLics #</span><span class="sxs-lookup"><span data-stu-id="ab3ec-262">DriverLics#</span></span>
- <span data-ttu-id="ab3ec-263">DriverLicence #</span><span class="sxs-lookup"><span data-stu-id="ab3ec-263">DriverLicence#</span></span>
- <span data-ttu-id="ab3ec-264">DriverLicences #</span><span class="sxs-lookup"><span data-stu-id="ab3ec-264">DriverLicences#</span></span>
- <span data-ttu-id="ab3ec-265">Driver Lic#</span><span class="sxs-lookup"><span data-stu-id="ab3ec-265">Driver Lic#</span></span>
- <span data-ttu-id="ab3ec-266">
Driver Lics#
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-266">Driver Lics#</span></span>
- <span data-ttu-id="ab3ec-267">Licença do driver #</span><span class="sxs-lookup"><span data-stu-id="ab3ec-267">Driver Licence#</span></span>
- <span data-ttu-id="ab3ec-268">Driver licenças #</span><span class="sxs-lookup"><span data-stu-id="ab3ec-268">Driver Licences#</span></span>
- <span data-ttu-id="ab3ec-269">DriversLic #</span><span class="sxs-lookup"><span data-stu-id="ab3ec-269">DriversLic#</span></span>
- <span data-ttu-id="ab3ec-270">DriversLics #</span><span class="sxs-lookup"><span data-stu-id="ab3ec-270">DriversLics#</span></span>
- <span data-ttu-id="ab3ec-271">DriversLicence #</span><span class="sxs-lookup"><span data-stu-id="ab3ec-271">DriversLicence#</span></span>
- <span data-ttu-id="ab3ec-272">DriversLicences #</span><span class="sxs-lookup"><span data-stu-id="ab3ec-272">DriversLicences#</span></span>
- <span data-ttu-id="ab3ec-273">Drivers Lic #</span><span class="sxs-lookup"><span data-stu-id="ab3ec-273">Drivers Lic#</span></span>
- <span data-ttu-id="ab3ec-274">Drivers Lics #</span><span class="sxs-lookup"><span data-stu-id="ab3ec-274">Drivers Lics#</span></span>
- <span data-ttu-id="ab3ec-275">Drivers licença #</span><span class="sxs-lookup"><span data-stu-id="ab3ec-275">Drivers Licence#</span></span>
- <span data-ttu-id="ab3ec-276">Drivers licenças #</span><span class="sxs-lookup"><span data-stu-id="ab3ec-276">Drivers Licences#</span></span>
- <span data-ttu-id="ab3ec-277">Driver'Lic#
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-277">Driver'Lic#</span></span>
- <span data-ttu-id="ab3ec-278">Driver'Lics#
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-278">Driver'Lics#</span></span>
- <span data-ttu-id="ab3ec-279">Driver'Licence#
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-279">Driver'Licence#</span></span>
- <span data-ttu-id="ab3ec-280">Driver'Licences#
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-280">Driver'Licences#</span></span>
- <span data-ttu-id="ab3ec-281">Driver' Lic#
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-281">Driver' Lic#</span></span>
- <span data-ttu-id="ab3ec-282">Driver' Lics#
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-282">Driver' Lics#</span></span>
- <span data-ttu-id="ab3ec-283">Driver' licença #</span><span class="sxs-lookup"><span data-stu-id="ab3ec-283">Driver' Licence#</span></span>
- <span data-ttu-id="ab3ec-284">Driver' licenças #</span><span class="sxs-lookup"><span data-stu-id="ab3ec-284">Driver' Licences#</span></span>
- <span data-ttu-id="ab3ec-285">Driver'sLic #</span><span class="sxs-lookup"><span data-stu-id="ab3ec-285">Driver'sLic#</span></span>
- <span data-ttu-id="ab3ec-286">Driver'sLics #</span><span class="sxs-lookup"><span data-stu-id="ab3ec-286">Driver'sLics#</span></span>
- <span data-ttu-id="ab3ec-287">Driver'sLicence #</span><span class="sxs-lookup"><span data-stu-id="ab3ec-287">Driver'sLicence#</span></span>
- <span data-ttu-id="ab3ec-288">Driver'sLicences #</span><span class="sxs-lookup"><span data-stu-id="ab3ec-288">Driver'sLicences#</span></span>
- <span data-ttu-id="ab3ec-289">Driver's Lic#
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-289">Driver's Lic#</span></span>
- <span data-ttu-id="ab3ec-290">Driver's Lics#
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-290">Driver's Lics#</span></span>
- <span data-ttu-id="ab3ec-291">Licença # de motorista</span><span class="sxs-lookup"><span data-stu-id="ab3ec-291">Driver's Licence#</span></span>
- <span data-ttu-id="ab3ec-292">Licenças # de motorista</span><span class="sxs-lookup"><span data-stu-id="ab3ec-292">Driver's Licences#</span></span> 

#### <a name="keywordaustraliadriverslicensenumberexclusions"></a><span data-ttu-id="ab3ec-293">Keyword_australia_drivers_license_number_exclusions</span><span class="sxs-lookup"><span data-stu-id="ab3ec-293">Keyword_australia_drivers_license_number_exclusions</span></span>

- <span data-ttu-id="ab3ec-294">aaa</span><span class="sxs-lookup"><span data-stu-id="ab3ec-294">aaa</span></span>
- <span data-ttu-id="ab3ec-295">DriverLicense</span><span class="sxs-lookup"><span data-stu-id="ab3ec-295">DriverLicense</span></span>
- <span data-ttu-id="ab3ec-296">DriverLicenses</span><span class="sxs-lookup"><span data-stu-id="ab3ec-296">DriverLicenses</span></span>
- <span data-ttu-id="ab3ec-297">Driver de licença</span><span class="sxs-lookup"><span data-stu-id="ab3ec-297">Driver License</span></span>
- <span data-ttu-id="ab3ec-298">Licenças de driver</span><span class="sxs-lookup"><span data-stu-id="ab3ec-298">Driver Licenses</span></span>
- <span data-ttu-id="ab3ec-299">CarteiraDeMotorista</span><span class="sxs-lookup"><span data-stu-id="ab3ec-299">DriversLicense</span></span>
- <span data-ttu-id="ab3ec-300">DriversLicenses</span><span class="sxs-lookup"><span data-stu-id="ab3ec-300">DriversLicenses</span></span>
- <span data-ttu-id="ab3ec-301">Carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="ab3ec-301">Drivers License</span></span>
- <span data-ttu-id="ab3ec-302">Licenças de drivers</span><span class="sxs-lookup"><span data-stu-id="ab3ec-302">Drivers Licenses</span></span>
- <span data-ttu-id="ab3ec-303">Driver'License</span><span class="sxs-lookup"><span data-stu-id="ab3ec-303">Driver'License</span></span>
- <span data-ttu-id="ab3ec-304">Driver'Licenses</span><span class="sxs-lookup"><span data-stu-id="ab3ec-304">Driver'Licenses</span></span>
- <span data-ttu-id="ab3ec-305">Driver' licença</span><span class="sxs-lookup"><span data-stu-id="ab3ec-305">Driver' License</span></span>
- <span data-ttu-id="ab3ec-306">Driver' licenças</span><span class="sxs-lookup"><span data-stu-id="ab3ec-306">Driver' Licenses</span></span>
- <span data-ttu-id="ab3ec-307">Driver'sLicense</span><span class="sxs-lookup"><span data-stu-id="ab3ec-307">Driver'sLicense</span></span>
- <span data-ttu-id="ab3ec-308">Driver'sLicenses</span><span class="sxs-lookup"><span data-stu-id="ab3ec-308">Driver'sLicenses</span></span>
- <span data-ttu-id="ab3ec-309">De motorista carteira</span><span class="sxs-lookup"><span data-stu-id="ab3ec-309">Driver's License</span></span>
- <span data-ttu-id="ab3ec-310">Licenças de motorista</span><span class="sxs-lookup"><span data-stu-id="ab3ec-310">Driver's Licenses</span></span>
- <span data-ttu-id="ab3ec-311">DriverLicense #</span><span class="sxs-lookup"><span data-stu-id="ab3ec-311">DriverLicense#</span></span>
- <span data-ttu-id="ab3ec-312">DriverLicenses #</span><span class="sxs-lookup"><span data-stu-id="ab3ec-312">DriverLicenses#</span></span>
- <span data-ttu-id="ab3ec-313">Licença do driver #</span><span class="sxs-lookup"><span data-stu-id="ab3ec-313">Driver License#</span></span>
- <span data-ttu-id="ab3ec-314">Driver licenças #</span><span class="sxs-lookup"><span data-stu-id="ab3ec-314">Driver Licenses#</span></span>
- <span data-ttu-id="ab3ec-315">CarteiraDeMotorista #</span><span class="sxs-lookup"><span data-stu-id="ab3ec-315">DriversLicense#</span></span>
- <span data-ttu-id="ab3ec-316">DriversLicenses #</span><span class="sxs-lookup"><span data-stu-id="ab3ec-316">DriversLicenses#</span></span>
- <span data-ttu-id="ab3ec-317">Drivers licença #</span><span class="sxs-lookup"><span data-stu-id="ab3ec-317">Drivers License#</span></span>
- <span data-ttu-id="ab3ec-318">Drivers licenças #</span><span class="sxs-lookup"><span data-stu-id="ab3ec-318">Drivers Licenses#</span></span>
- <span data-ttu-id="ab3ec-319">Driver'License#
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-319">Driver'License#</span></span>
- <span data-ttu-id="ab3ec-320">Driver'Licenses#
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-320">Driver'Licenses#</span></span>
- <span data-ttu-id="ab3ec-321">Driver' License#
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-321">Driver' License#</span></span>
- <span data-ttu-id="ab3ec-322">Driver' Licenses#
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-322">Driver' Licenses#</span></span>
- <span data-ttu-id="ab3ec-323">Driver'sLicense #</span><span class="sxs-lookup"><span data-stu-id="ab3ec-323">Driver'sLicense#</span></span>
- <span data-ttu-id="ab3ec-324">Driver'sLicenses #</span><span class="sxs-lookup"><span data-stu-id="ab3ec-324">Driver'sLicenses#</span></span>
- <span data-ttu-id="ab3ec-325">Driver's License#
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-325">Driver's License#</span></span>
- <span data-ttu-id="ab3ec-326">

Driver's Licenses#</span><span class="sxs-lookup"><span data-stu-id="ab3ec-326">Driver's Licenses#</span></span>
   
## <a name="australia-medical-account-number"></a><span data-ttu-id="ab3ec-327">Número de conta médica da Austrália</span><span class="sxs-lookup"><span data-stu-id="ab3ec-327">Australia Medical Account Number</span></span>

### <a name="format"></a><span data-ttu-id="ab3ec-328">Formato</span><span class="sxs-lookup"><span data-stu-id="ab3ec-328">Format</span></span>

<span data-ttu-id="ab3ec-329">10 a 11 dígitos</span><span class="sxs-lookup"><span data-stu-id="ab3ec-329">10-11 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="ab3ec-330">Padrão</span><span class="sxs-lookup"><span data-stu-id="ab3ec-330">Pattern</span></span>

<span data-ttu-id="ab3ec-331">10 a 11 dígitos:</span><span class="sxs-lookup"><span data-stu-id="ab3ec-331">10-11 digits:</span></span>
- <span data-ttu-id="ab3ec-332">Primeiro dígito está no intervalo de 2 a 6</span><span class="sxs-lookup"><span data-stu-id="ab3ec-332">First digit is in the range 2-6</span></span>
- <span data-ttu-id="ab3ec-333">O nono dígito é um dígito de verificação</span><span class="sxs-lookup"><span data-stu-id="ab3ec-333">Ninth digit is a check digit</span></span>
- <span data-ttu-id="ab3ec-334">O décimo dígito é o dígito do problema</span><span class="sxs-lookup"><span data-stu-id="ab3ec-334">Tenth digit is the issue digit</span></span>
- <span data-ttu-id="ab3ec-335">O décimo primeiro dígito (opcional) é o número individual</span><span class="sxs-lookup"><span data-stu-id="ab3ec-335">Eleventh digit (optional) is the individual number</span></span>

### <a name="checksum"></a><span data-ttu-id="ab3ec-336">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="ab3ec-336">Checksum</span></span>

<span data-ttu-id="ab3ec-337">Sim</span><span class="sxs-lookup"><span data-stu-id="ab3ec-337">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="ab3ec-338">Definição</span><span class="sxs-lookup"><span data-stu-id="ab3ec-338">Definition</span></span>

<span data-ttu-id="ab3ec-339">Uma política de DLP tem 95% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="ab3ec-339">A DLP policy is 95% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="ab3ec-340">A função Func_australian_medical_account_number localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-340">The function Func_australian_medical_account_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="ab3ec-341">Uma palavra-chave de Keyword_Australia_Medical_Account_Number for encontrada.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-341">A keyword from Keyword_Australia_Medical_Account_Number is found.</span></span>
- <span data-ttu-id="ab3ec-342">A soma de verificação passa.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-342">The checksum passes.</span></span>

<span data-ttu-id="ab3ec-343">Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="ab3ec-343">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="ab3ec-344">A função Func_australian_medical_account_number localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-344">The function Func_australian_medical_account_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="ab3ec-345">A soma de verificação passa.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-345">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="ab3ec-346">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="ab3ec-346">Keywords</span></span>

#### <a name="keywordaustraliamedicalaccountnumber"></a><span data-ttu-id="ab3ec-347">Keyword_Australia_Medical_Account_Number</span><span class="sxs-lookup"><span data-stu-id="ab3ec-347">Keyword_Australia_Medical_Account_Number</span></span>

- <span data-ttu-id="ab3ec-348">bank account details</span><span class="sxs-lookup"><span data-stu-id="ab3ec-348">bank account details</span></span>
- <span data-ttu-id="ab3ec-349">
medicare payments</span><span class="sxs-lookup"><span data-stu-id="ab3ec-349">medicare payments</span></span>
- <span data-ttu-id="ab3ec-350">
mortgage account</span><span class="sxs-lookup"><span data-stu-id="ab3ec-350">mortgage account</span></span>
- <span data-ttu-id="ab3ec-351">
bank payments</span><span class="sxs-lookup"><span data-stu-id="ab3ec-351">bank payments</span></span>
- <span data-ttu-id="ab3ec-352">
information branch</span><span class="sxs-lookup"><span data-stu-id="ab3ec-352">information branch</span></span>
- <span data-ttu-id="ab3ec-353">
credit card loan</span><span class="sxs-lookup"><span data-stu-id="ab3ec-353">credit card loan</span></span>
- <span data-ttu-id="ab3ec-354">
department of human services</span><span class="sxs-lookup"><span data-stu-id="ab3ec-354">department of human services</span></span>
- <span data-ttu-id="ab3ec-355">serviço local</span><span class="sxs-lookup"><span data-stu-id="ab3ec-355">local service</span></span>
- <span data-ttu-id="ab3ec-356">

medicare</span><span class="sxs-lookup"><span data-stu-id="ab3ec-356">medicare</span></span>

   
## <a name="australia-passport-number"></a><span data-ttu-id="ab3ec-357">Número de passaporte da Austrália</span><span class="sxs-lookup"><span data-stu-id="ab3ec-357">Australia Passport Number</span></span>

### <a name="format"></a><span data-ttu-id="ab3ec-358">Formato</span><span class="sxs-lookup"><span data-stu-id="ab3ec-358">Format</span></span>

<span data-ttu-id="ab3ec-359">Uma letra seguida por sete dígitos</span><span class="sxs-lookup"><span data-stu-id="ab3ec-359">A letter followed by seven digits</span></span>

### <a name="pattern"></a><span data-ttu-id="ab3ec-360">Padrão</span><span class="sxs-lookup"><span data-stu-id="ab3ec-360">Pattern</span></span>

<span data-ttu-id="ab3ec-361">Uma letra (não diferencia maiúsculas de minúsculas) seguida de sete dígitos</span><span class="sxs-lookup"><span data-stu-id="ab3ec-361">A letter (not case sensitive) followed by seven digits</span></span>

### <a name="checksum"></a><span data-ttu-id="ab3ec-362">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="ab3ec-362">Checksum</span></span>

<span data-ttu-id="ab3ec-363">Não</span><span class="sxs-lookup"><span data-stu-id="ab3ec-363">No</span></span>

### <a name="definition"></a><span data-ttu-id="ab3ec-364">Definição</span><span class="sxs-lookup"><span data-stu-id="ab3ec-364">Definition</span></span>

<span data-ttu-id="ab3ec-365">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="ab3ec-365">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="ab3ec-366">A expressão regular Regex_australia_passport_number localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-366">The regular expression Regex_australia_passport_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="ab3ec-367">Uma palavra-chave de Keyword_passport ou Keyword_australia_passport_number é encontrada.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-367">A keyword from Keyword_passport or Keyword_australia_passport_number is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="ab3ec-368">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="ab3ec-368">Keywords</span></span>

#### <a name="keywordpassport"></a><span data-ttu-id="ab3ec-369">Keyword_passport</span><span class="sxs-lookup"><span data-stu-id="ab3ec-369">Keyword_passport</span></span>

- <span data-ttu-id="ab3ec-370">Passport Number</span><span class="sxs-lookup"><span data-stu-id="ab3ec-370">Passport Number</span></span>
- <span data-ttu-id="ab3ec-371">
Passport No</span><span class="sxs-lookup"><span data-stu-id="ab3ec-371">Passport No</span></span>
- <span data-ttu-id="ab3ec-372">Passport #
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-372">Passport #</span></span>
- <span data-ttu-id="ab3ec-373">Passport#
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-373">Passport#</span></span>
- <span data-ttu-id="ab3ec-374">PassportID</span><span class="sxs-lookup"><span data-stu-id="ab3ec-374">PassportID</span></span>
- <span data-ttu-id="ab3ec-375">Passportno
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-375">Passportno</span></span>
- <span data-ttu-id="ab3ec-376">passportnumber
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-376">passportnumber</span></span>
- <span data-ttu-id="ab3ec-377">パスポート</span><span class="sxs-lookup"><span data-stu-id="ab3ec-377">パスポート</span></span>
- <span data-ttu-id="ab3ec-378">パスポート番号
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-378">パスポート番号</span></span>
- <span data-ttu-id="ab3ec-379">パスポートのNum
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-379">パスポートのNum</span></span>
- <span data-ttu-id="ab3ec-380">
パスポート ＃
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-380">パスポート ＃</span></span> 
- <span data-ttu-id="ab3ec-381">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="ab3ec-381">Numéro de passeport</span></span>
- <span data-ttu-id="ab3ec-382">
Passeport n °</span><span class="sxs-lookup"><span data-stu-id="ab3ec-382">Passeport n °</span></span>
- <span data-ttu-id="ab3ec-383">Passeport Non
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-383">Passeport Non</span></span>
- <span data-ttu-id="ab3ec-384">Passeport #
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-384">Passeport #</span></span>
- <span data-ttu-id="ab3ec-385">Passeport#
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-385">Passeport#</span></span>
- <span data-ttu-id="ab3ec-386">PasseportNon</span><span class="sxs-lookup"><span data-stu-id="ab3ec-386">PasseportNon</span></span>
- <span data-ttu-id="ab3ec-387">Passeportn °
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-387">Passeportn °</span></span>

#### <a name="keywordaustraliapassportnumber"></a><span data-ttu-id="ab3ec-388">Keyword_australia_passport_number</span><span class="sxs-lookup"><span data-stu-id="ab3ec-388">Keyword_australia_passport_number</span></span>

- <span data-ttu-id="ab3ec-389">passport</span><span class="sxs-lookup"><span data-stu-id="ab3ec-389">passport</span></span>
- <span data-ttu-id="ab3ec-390">
passport details</span><span class="sxs-lookup"><span data-stu-id="ab3ec-390">passport details</span></span>
- <span data-ttu-id="ab3ec-391">
immigration and citizenship</span><span class="sxs-lookup"><span data-stu-id="ab3ec-391">immigration and citizenship</span></span>
- <span data-ttu-id="ab3ec-392">
commonwealth of australia</span><span class="sxs-lookup"><span data-stu-id="ab3ec-392">commonwealth of australia</span></span>
- <span data-ttu-id="ab3ec-393">
department of immigration</span><span class="sxs-lookup"><span data-stu-id="ab3ec-393">department of immigration</span></span>
- <span data-ttu-id="ab3ec-394">
residential address</span><span class="sxs-lookup"><span data-stu-id="ab3ec-394">residential address</span></span>
- <span data-ttu-id="ab3ec-395">
department of immigration and citizenship</span><span class="sxs-lookup"><span data-stu-id="ab3ec-395">department of immigration and citizenship</span></span>
- <span data-ttu-id="ab3ec-396">visa
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-396">visa</span></span>
- <span data-ttu-id="ab3ec-397">
national identity card</span><span class="sxs-lookup"><span data-stu-id="ab3ec-397">national identity card</span></span>
- <span data-ttu-id="ab3ec-398">número de passaporte</span><span class="sxs-lookup"><span data-stu-id="ab3ec-398">passport number</span></span>
- <span data-ttu-id="ab3ec-399">
travel document</span><span class="sxs-lookup"><span data-stu-id="ab3ec-399">travel document</span></span>
- <span data-ttu-id="ab3ec-400">

issuing authority</span><span class="sxs-lookup"><span data-stu-id="ab3ec-400">issuing authority</span></span>
   
## <a name="australia-tax-file-number"></a><span data-ttu-id="ab3ec-401">Número de imposto de renda da Austrália</span><span class="sxs-lookup"><span data-stu-id="ab3ec-401">Australia Tax File Number</span></span>

### <a name="format"></a><span data-ttu-id="ab3ec-402">Formato</span><span class="sxs-lookup"><span data-stu-id="ab3ec-402">Format</span></span>

<span data-ttu-id="ab3ec-403">8 a 9 dígitos</span><span class="sxs-lookup"><span data-stu-id="ab3ec-403">8-9 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="ab3ec-404">Padrão</span><span class="sxs-lookup"><span data-stu-id="ab3ec-404">Pattern</span></span>

<span data-ttu-id="ab3ec-405">8 a 9 dígitos normalmente apresentados com espaços, da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="ab3ec-405">8-9 digits typically presented with spaces as follows:</span></span>
- <span data-ttu-id="ab3ec-406">Três dígitos</span><span class="sxs-lookup"><span data-stu-id="ab3ec-406">Three digits</span></span> 
- <span data-ttu-id="ab3ec-407">Um espaço opcional</span><span class="sxs-lookup"><span data-stu-id="ab3ec-407">An optional space</span></span> 
- <span data-ttu-id="ab3ec-408">Três dígitos</span><span class="sxs-lookup"><span data-stu-id="ab3ec-408">Three digits</span></span> 
- <span data-ttu-id="ab3ec-409">Um espaço opcional</span><span class="sxs-lookup"><span data-stu-id="ab3ec-409">An optional space</span></span> 
- <span data-ttu-id="ab3ec-410">2 a 3 dígitos em que o último dígito é um dígito de verificação</span><span class="sxs-lookup"><span data-stu-id="ab3ec-410">2-3 digits where the last digit is a check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="ab3ec-411">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="ab3ec-411">Checksum</span></span>

<span data-ttu-id="ab3ec-412">Sim</span><span class="sxs-lookup"><span data-stu-id="ab3ec-412">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="ab3ec-413">Definição</span><span class="sxs-lookup"><span data-stu-id="ab3ec-413">Definition</span></span>

<span data-ttu-id="ab3ec-414">Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="ab3ec-414">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="ab3ec-415">A função Func_australian_tax_file_number localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-415">The function Func_australian_tax_file_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="ab3ec-416">Nenhuma palavra-chave de Keyword_Australia_Tax_File_Number ou Keyword_number_exclusions for encontrada.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-416">No keyword from Keyword_Australia_Tax_File_Number or Keyword_number_exclusions is found.</span></span>
- <span data-ttu-id="ab3ec-417">A soma de verificação passa.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-417">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="ab3ec-418">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="ab3ec-418">Keywords</span></span>

#### <a name="keywordaustraliataxfilenumber"></a><span data-ttu-id="ab3ec-419">Keyword_Australia_Tax_File_Number</span><span class="sxs-lookup"><span data-stu-id="ab3ec-419">Keyword_Australia_Tax_File_Number</span></span>

- <span data-ttu-id="ab3ec-420">australian business number</span><span class="sxs-lookup"><span data-stu-id="ab3ec-420">australian business number</span></span>
- <span data-ttu-id="ab3ec-421">
marginal tax rate</span><span class="sxs-lookup"><span data-stu-id="ab3ec-421">marginal tax rate</span></span>
- <span data-ttu-id="ab3ec-422">
medicare levy</span><span class="sxs-lookup"><span data-stu-id="ab3ec-422">medicare levy</span></span>
- <span data-ttu-id="ab3ec-423">
portfolio number</span><span class="sxs-lookup"><span data-stu-id="ab3ec-423">portfolio number</span></span>
- <span data-ttu-id="ab3ec-424">
service veterans</span><span class="sxs-lookup"><span data-stu-id="ab3ec-424">service veterans</span></span>
- <span data-ttu-id="ab3ec-425">
withholding tax</span><span class="sxs-lookup"><span data-stu-id="ab3ec-425">withholding tax</span></span>
- <span data-ttu-id="ab3ec-426">
individual tax return</span><span class="sxs-lookup"><span data-stu-id="ab3ec-426">individual tax return</span></span>
- <span data-ttu-id="ab3ec-427">

tax file number</span><span class="sxs-lookup"><span data-stu-id="ab3ec-427">tax file number</span></span>

#### <a name="keywordnumberexclusions"></a><span data-ttu-id="ab3ec-428">Keyword_number_exclusions</span><span class="sxs-lookup"><span data-stu-id="ab3ec-428">Keyword_number_exclusions</span></span>

- <span data-ttu-id="ab3ec-429">00000000</span><span class="sxs-lookup"><span data-stu-id="ab3ec-429">00000000</span></span>
- <span data-ttu-id="ab3ec-430">11111111</span><span class="sxs-lookup"><span data-stu-id="ab3ec-430">11111111</span></span>
- <span data-ttu-id="ab3ec-431">22222222</span><span class="sxs-lookup"><span data-stu-id="ab3ec-431">22222222</span></span>
- <span data-ttu-id="ab3ec-432">33333333</span><span class="sxs-lookup"><span data-stu-id="ab3ec-432">33333333</span></span>
- <span data-ttu-id="ab3ec-433">44444444</span><span class="sxs-lookup"><span data-stu-id="ab3ec-433">44444444</span></span>
- <span data-ttu-id="ab3ec-434">55555555</span><span class="sxs-lookup"><span data-stu-id="ab3ec-434">55555555</span></span>
- <span data-ttu-id="ab3ec-435">66666666</span><span class="sxs-lookup"><span data-stu-id="ab3ec-435">66666666</span></span>
- <span data-ttu-id="ab3ec-436">77777777</span><span class="sxs-lookup"><span data-stu-id="ab3ec-436">77777777</span></span>
- <span data-ttu-id="ab3ec-437">88888888</span><span class="sxs-lookup"><span data-stu-id="ab3ec-437">88888888</span></span>
- <span data-ttu-id="ab3ec-438">99999999</span><span class="sxs-lookup"><span data-stu-id="ab3ec-438">99999999</span></span>
- <span data-ttu-id="ab3ec-439">000000000</span><span class="sxs-lookup"><span data-stu-id="ab3ec-439">000000000</span></span>
- <span data-ttu-id="ab3ec-440">111111111</span><span class="sxs-lookup"><span data-stu-id="ab3ec-440">111111111</span></span>
- <span data-ttu-id="ab3ec-441">222222222</span><span class="sxs-lookup"><span data-stu-id="ab3ec-441">222222222</span></span>
- <span data-ttu-id="ab3ec-442">333333333</span><span class="sxs-lookup"><span data-stu-id="ab3ec-442">333333333</span></span>
- <span data-ttu-id="ab3ec-443">444444444</span><span class="sxs-lookup"><span data-stu-id="ab3ec-443">444444444</span></span>
- <span data-ttu-id="ab3ec-444">555555555</span><span class="sxs-lookup"><span data-stu-id="ab3ec-444">555555555</span></span>
- <span data-ttu-id="ab3ec-445">666666666</span><span class="sxs-lookup"><span data-stu-id="ab3ec-445">666666666</span></span>
- <span data-ttu-id="ab3ec-446">777777777</span><span class="sxs-lookup"><span data-stu-id="ab3ec-446">777777777</span></span>
- <span data-ttu-id="ab3ec-447">888888888</span><span class="sxs-lookup"><span data-stu-id="ab3ec-447">888888888</span></span>
- <span data-ttu-id="ab3ec-448">999999999</span><span class="sxs-lookup"><span data-stu-id="ab3ec-448">999999999</span></span>
- <span data-ttu-id="ab3ec-449">0000000000</span><span class="sxs-lookup"><span data-stu-id="ab3ec-449">0000000000</span></span>
- <span data-ttu-id="ab3ec-450">1111111111</span><span class="sxs-lookup"><span data-stu-id="ab3ec-450">1111111111</span></span>
- <span data-ttu-id="ab3ec-451">2222222222</span><span class="sxs-lookup"><span data-stu-id="ab3ec-451">2222222222</span></span>
- <span data-ttu-id="ab3ec-452">3333333333</span><span class="sxs-lookup"><span data-stu-id="ab3ec-452">3333333333</span></span>
- <span data-ttu-id="ab3ec-453">4444444444</span><span class="sxs-lookup"><span data-stu-id="ab3ec-453">4444444444</span></span>
- <span data-ttu-id="ab3ec-454">5555555555</span><span class="sxs-lookup"><span data-stu-id="ab3ec-454">5555555555</span></span>
- <span data-ttu-id="ab3ec-455">6666666666</span><span class="sxs-lookup"><span data-stu-id="ab3ec-455">6666666666</span></span>
- <span data-ttu-id="ab3ec-456">7777777777</span><span class="sxs-lookup"><span data-stu-id="ab3ec-456">7777777777</span></span>
- <span data-ttu-id="ab3ec-457">8888888888</span><span class="sxs-lookup"><span data-stu-id="ab3ec-457">8888888888</span></span>
- <span data-ttu-id="ab3ec-458">9999999999</span><span class="sxs-lookup"><span data-stu-id="ab3ec-458">9999999999</span></span>
   
## <a name="belgium-national-number"></a><span data-ttu-id="ab3ec-459">Número Nacional da Bélgica</span><span class="sxs-lookup"><span data-stu-id="ab3ec-459">Belgium National Number</span></span>

### <a name="format"></a><span data-ttu-id="ab3ec-460">Formato</span><span class="sxs-lookup"><span data-stu-id="ab3ec-460">Format</span></span>

<span data-ttu-id="ab3ec-461">11 dígitos mais delimitadores</span><span class="sxs-lookup"><span data-stu-id="ab3ec-461">11 digits plus delimiters</span></span>

### <a name="pattern"></a><span data-ttu-id="ab3ec-462">Padrão</span><span class="sxs-lookup"><span data-stu-id="ab3ec-462">Pattern</span></span>

<span data-ttu-id="ab3ec-463">11 dígitos mais delimitadores.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-463">11 digits plus delimiters:</span></span>
- <span data-ttu-id="ab3ec-464">Seis dígitos e dois pontos no formato AA.MM.DD da data de nascimento </span><span class="sxs-lookup"><span data-stu-id="ab3ec-464">Six digits and two periods in the format YY.MM.DD for date of birth</span></span> 
- <span data-ttu-id="ab3ec-465">Um hífen</span><span class="sxs-lookup"><span data-stu-id="ab3ec-465">A hyphen</span></span> 
- <span data-ttu-id="ab3ec-466">Três dígitos sequenciais (ímpares para homens, pares para mulheres) </span><span class="sxs-lookup"><span data-stu-id="ab3ec-466">Three sequential digits (odd for males, even for females)</span></span> 
- <span data-ttu-id="ab3ec-467">Um ponto </span><span class="sxs-lookup"><span data-stu-id="ab3ec-467">A period</span></span> 
- <span data-ttu-id="ab3ec-468">Dois dígitos que são um dígito de verificação</span><span class="sxs-lookup"><span data-stu-id="ab3ec-468">Two digits that are a check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="ab3ec-469">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="ab3ec-469">Checksum</span></span>

<span data-ttu-id="ab3ec-470">Sim</span><span class="sxs-lookup"><span data-stu-id="ab3ec-470">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="ab3ec-471">Definição</span><span class="sxs-lookup"><span data-stu-id="ab3ec-471">Definition</span></span>

<span data-ttu-id="ab3ec-472">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="ab3ec-472">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="ab3ec-473">A função Func_belgium_national_number encontra o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-473">The function Func_belgium_national_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="ab3ec-474">Uma palavra-chave de Keyword_belgium_national_number é encontrada.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-474">A keyword from Keyword_belgium_national_number is found.</span></span>
- <span data-ttu-id="ab3ec-475">A soma de verificação passa.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-475">The checksum passes.</span></span>

```
<!-- Belgium National Number -->
  <Entity id="fb969c9e-0fd1-4b18-8091-a2123c5e6a54" recommendedConfidence="75" patternsProximity="300">
   <Pattern confidenceLevel="75">
     <IdMatch idRef="Func_belgium_national_number"/>
     <Match idRef="Keyword_belgium_national_number"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="ab3ec-476">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="ab3ec-476">Keywords</span></span>

#### <a name="keywordbelgiumnationalnumber"></a><span data-ttu-id="ab3ec-477">Keyword_belgium_national_number</span><span class="sxs-lookup"><span data-stu-id="ab3ec-477">Keyword_belgium_national_number</span></span>

- <span data-ttu-id="ab3ec-478">Identity</span><span class="sxs-lookup"><span data-stu-id="ab3ec-478">Identity</span></span>
- <span data-ttu-id="ab3ec-479">Registro</span><span class="sxs-lookup"><span data-stu-id="ab3ec-479">Registration</span></span>
- <span data-ttu-id="ab3ec-480">Identificação </span><span class="sxs-lookup"><span data-stu-id="ab3ec-480">Identification</span></span> 
- <span data-ttu-id="ab3ec-481">ID</span><span class="sxs-lookup"><span data-stu-id="ab3ec-481">ID</span></span> 
- <span data-ttu-id="ab3ec-482">Identiteitskaart</span><span class="sxs-lookup"><span data-stu-id="ab3ec-482">Identiteitskaart</span></span>
- <span data-ttu-id="ab3ec-483">Registratie nummer 
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-483">Registratie nummer</span></span> 
- <span data-ttu-id="ab3ec-484">Identificatie nummer
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-484">Identificatie nummer</span></span> 
- <span data-ttu-id="ab3ec-485">Identiteit</span><span class="sxs-lookup"><span data-stu-id="ab3ec-485">Identiteit</span></span>
- <span data-ttu-id="ab3ec-486">Registratie</span><span class="sxs-lookup"><span data-stu-id="ab3ec-486">Registratie</span></span>
- <span data-ttu-id="ab3ec-487">Identificatie

</span><span class="sxs-lookup"><span data-stu-id="ab3ec-487">Identificatie</span></span> 
- <span data-ttu-id="ab3ec-488">Carte d’identité
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-488">Carte d’identité</span></span> 
- <span data-ttu-id="ab3ec-489">numéro d'immatriculation</span><span class="sxs-lookup"><span data-stu-id="ab3ec-489">numéro d'immatriculation</span></span>
- <span data-ttu-id="ab3ec-490">numéro d'identification</span><span class="sxs-lookup"><span data-stu-id="ab3ec-490">numéro d'identification</span></span>
- <span data-ttu-id="ab3ec-491">
identité
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-491">identité</span></span> 
- <span data-ttu-id="ab3ec-492">inscription
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-492">inscription</span></span> 
- <span data-ttu-id="ab3ec-493">Identifikation</span><span class="sxs-lookup"><span data-stu-id="ab3ec-493">Identifikation</span></span>
- <span data-ttu-id="ab3ec-494">Identifizierung</span><span class="sxs-lookup"><span data-stu-id="ab3ec-494">Identifizierung</span></span>
- <span data-ttu-id="ab3ec-495">Identifikationsnummer</span><span class="sxs-lookup"><span data-stu-id="ab3ec-495">Identifikationsnummer</span></span>
- <span data-ttu-id="ab3ec-496">Personalausweis</span><span class="sxs-lookup"><span data-stu-id="ab3ec-496">Personalausweis</span></span>
- <span data-ttu-id="ab3ec-497">Registrierung</span><span class="sxs-lookup"><span data-stu-id="ab3ec-497">Registrierung</span></span>
- <span data-ttu-id="ab3ec-498">Registrationsnummer</span><span class="sxs-lookup"><span data-stu-id="ab3ec-498">Registrationsnummer</span></span>

   
## <a name="brazil-cpf-number"></a><span data-ttu-id="ab3ec-499">Número de CPF do Brasil</span><span class="sxs-lookup"><span data-stu-id="ab3ec-499">Brazil CPF Number</span></span>

### <a name="format"></a><span data-ttu-id="ab3ec-500">Formato</span><span class="sxs-lookup"><span data-stu-id="ab3ec-500">Format</span></span>

<span data-ttu-id="ab3ec-501">11 dígitos que incluem um dígito de verificação e podem ser formatados ou não formatados</span><span class="sxs-lookup"><span data-stu-id="ab3ec-501">11 digits that include a check digit and can be formatted or unformatted</span></span>

### <a name="pattern"></a><span data-ttu-id="ab3ec-502">Padrão</span><span class="sxs-lookup"><span data-stu-id="ab3ec-502">Pattern</span></span>

<span data-ttu-id="ab3ec-503">Formatado:</span><span class="sxs-lookup"><span data-stu-id="ab3ec-503">Formatted:</span></span>
- <span data-ttu-id="ab3ec-504">Três dígitos</span><span class="sxs-lookup"><span data-stu-id="ab3ec-504">Three digits</span></span> 
- <span data-ttu-id="ab3ec-505">Um ponto </span><span class="sxs-lookup"><span data-stu-id="ab3ec-505">A period</span></span> 
- <span data-ttu-id="ab3ec-506">Três dígitos</span><span class="sxs-lookup"><span data-stu-id="ab3ec-506">Three digits</span></span> 
- <span data-ttu-id="ab3ec-507">Um ponto </span><span class="sxs-lookup"><span data-stu-id="ab3ec-507">A period</span></span> 
- <span data-ttu-id="ab3ec-508">Três dígitos</span><span class="sxs-lookup"><span data-stu-id="ab3ec-508">Three digits</span></span> 
- <span data-ttu-id="ab3ec-509">Um hífen</span><span class="sxs-lookup"><span data-stu-id="ab3ec-509">A hyphen</span></span> 
- <span data-ttu-id="ab3ec-510">Dois dígitos que são dígitos de verificação</span><span class="sxs-lookup"><span data-stu-id="ab3ec-510">Two digits which are check digits</span></span>

<span data-ttu-id="ab3ec-511">Não Formatado:</span><span class="sxs-lookup"><span data-stu-id="ab3ec-511">Unformatted:</span></span>
- <span data-ttu-id="ab3ec-512">11 dígitos em que os dois últimos dígitos são dígitos de verificação</span><span class="sxs-lookup"><span data-stu-id="ab3ec-512">11 digits where the last two digits are check digits</span></span>

### <a name="checksum"></a><span data-ttu-id="ab3ec-513">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="ab3ec-513">Checksum</span></span>

<span data-ttu-id="ab3ec-514">Sim</span><span class="sxs-lookup"><span data-stu-id="ab3ec-514">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="ab3ec-515">Definição</span><span class="sxs-lookup"><span data-stu-id="ab3ec-515">Definition</span></span>

<span data-ttu-id="ab3ec-516">Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="ab3ec-516">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="ab3ec-517">A função Func_brazil_cpf encontra o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-517">The function Func_brazil_cpf finds content that matches the pattern.</span></span>
- <span data-ttu-id="ab3ec-518">Uma palavra-chave de Keyword_brazil_cpf é encontrada.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-518">A keyword from Keyword_brazil_cpf is found.</span></span>
- <span data-ttu-id="ab3ec-519">A soma de verificação passa.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-519">The checksum passes.</span></span>

<span data-ttu-id="ab3ec-520">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="ab3ec-520">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="ab3ec-521">A função Func_brazil_cpf encontra o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-521">The function Func_brazil_cpf finds content that matches the pattern.</span></span>
- <span data-ttu-id="ab3ec-522">A soma de verificação passa.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-522">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="ab3ec-523">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="ab3ec-523">Keywords</span></span>

#### <a name="keywordbrazilcpf"></a><span data-ttu-id="ab3ec-524">Keyword_brazil_cpf</span><span class="sxs-lookup"><span data-stu-id="ab3ec-524">Keyword_brazil_cpf</span></span>

- <span data-ttu-id="ab3ec-525">CPF</span><span class="sxs-lookup"><span data-stu-id="ab3ec-525">CPF</span></span>
- <span data-ttu-id="ab3ec-526">Identificação </span><span class="sxs-lookup"><span data-stu-id="ab3ec-526">Identification</span></span>
- <span data-ttu-id="ab3ec-527">Registro</span><span class="sxs-lookup"><span data-stu-id="ab3ec-527">Registration</span></span>
- <span data-ttu-id="ab3ec-528">Receita</span><span class="sxs-lookup"><span data-stu-id="ab3ec-528">Revenue</span></span>
- <span data-ttu-id="ab3ec-529">Cadastro de Pessoas Físicas
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-529">Cadastro de Pessoas Físicas</span></span> 
- <span data-ttu-id="ab3ec-530">Imposto
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-530">Imposto</span></span> 
- <span data-ttu-id="ab3ec-531">Identificação
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-531">Identificação</span></span> 
- <span data-ttu-id="ab3ec-532">Inscrição
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-532">Inscrição</span></span> 
- <span data-ttu-id="ab3ec-533">Receita

</span><span class="sxs-lookup"><span data-stu-id="ab3ec-533">Receita</span></span> 
   
## <a name="brazil-legal-entity-number-cnpj"></a><span data-ttu-id="ab3ec-534">Número de Pessoa Jurídica (CNPJ) do Brasil</span><span class="sxs-lookup"><span data-stu-id="ab3ec-534">Brazil Legal Entity Number (CNPJ)</span></span>

### <a name="format"></a><span data-ttu-id="ab3ec-535">Formato</span><span class="sxs-lookup"><span data-stu-id="ab3ec-535">Format</span></span>

<span data-ttu-id="ab3ec-536">14 dígitos que incluem um número de registro, o número da ramificação e dígitos de verificação, além de delimitadores de seleção</span><span class="sxs-lookup"><span data-stu-id="ab3ec-536">14 digits that include a registration number, branch number, and check digits, plus delimiters</span></span>

### <a name="pattern"></a><span data-ttu-id="ab3ec-537">Padrão</span><span class="sxs-lookup"><span data-stu-id="ab3ec-537">Pattern</span></span>
<span data-ttu-id="ab3ec-538">14 dígitos mais delimitadores:</span><span class="sxs-lookup"><span data-stu-id="ab3ec-538">14 digits, plus delimiters:</span></span>
- <span data-ttu-id="ab3ec-539">Dois dígitos</span><span class="sxs-lookup"><span data-stu-id="ab3ec-539">Two digits</span></span> 
- <span data-ttu-id="ab3ec-540">Um ponto </span><span class="sxs-lookup"><span data-stu-id="ab3ec-540">A period</span></span> 
- <span data-ttu-id="ab3ec-541">Três dígitos</span><span class="sxs-lookup"><span data-stu-id="ab3ec-541">Three digits</span></span> 
- <span data-ttu-id="ab3ec-542">Um ponto </span><span class="sxs-lookup"><span data-stu-id="ab3ec-542">A period</span></span> 
- <span data-ttu-id="ab3ec-543">Três dígitos (esses primeiros oito dígitos são o número de registro) </span><span class="sxs-lookup"><span data-stu-id="ab3ec-543">Three digits (these first eight digits are the registration number)</span></span> 
- <span data-ttu-id="ab3ec-544">Uma barra</span><span class="sxs-lookup"><span data-stu-id="ab3ec-544">A forward slash</span></span> 
- <span data-ttu-id="ab3ec-545">Número da ramificação de quatro dígitos </span><span class="sxs-lookup"><span data-stu-id="ab3ec-545">Four-digit branch number</span></span> 
- <span data-ttu-id="ab3ec-546">Um hífen</span><span class="sxs-lookup"><span data-stu-id="ab3ec-546">A hyphen</span></span> 
- <span data-ttu-id="ab3ec-547">Dois dígitos que são dígitos de verificação</span><span class="sxs-lookup"><span data-stu-id="ab3ec-547">Two digits which are check digits</span></span>

### <a name="checksum"></a><span data-ttu-id="ab3ec-548">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="ab3ec-548">Checksum</span></span>

<span data-ttu-id="ab3ec-549">Sim</span><span class="sxs-lookup"><span data-stu-id="ab3ec-549">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="ab3ec-550">Definição</span><span class="sxs-lookup"><span data-stu-id="ab3ec-550">Definition</span></span>

<span data-ttu-id="ab3ec-551">Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="ab3ec-551">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="ab3ec-552">A função Func_brazil_cnpj encontra o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-552">The function Func_brazil_cnpj finds content that matches the pattern.</span></span>
- <span data-ttu-id="ab3ec-553">Uma palavra-chave de Keyword_brazil_cnpj é encontrada.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-553">A keyword from Keyword_brazil_cnpj is found.</span></span>
- <span data-ttu-id="ab3ec-554">A soma de verificação passa.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-554">The checksum passes.</span></span>

<span data-ttu-id="ab3ec-555">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="ab3ec-555">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="ab3ec-556">A função Func_brazil_cnpj encontra o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-556">The function Func_brazil_cnpj finds content that matches the pattern.</span></span>
- <span data-ttu-id="ab3ec-557">A soma de verificação passa.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-557">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="ab3ec-558">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="ab3ec-558">Keywords</span></span>

#### <a name="keywordbrazilcnpj"></a><span data-ttu-id="ab3ec-559">Keyword_brazil_cnpj</span><span class="sxs-lookup"><span data-stu-id="ab3ec-559">Keyword_brazil_cnpj</span></span>

- <span data-ttu-id="ab3ec-560">CNPJ
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-560">CNPJ</span></span> 
- <span data-ttu-id="ab3ec-561">CNPJ/MF</span><span class="sxs-lookup"><span data-stu-id="ab3ec-561">CNPJ/MF</span></span> 
- <span data-ttu-id="ab3ec-562">CNPJ-MF
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-562">CNPJ-MF</span></span> 
- <span data-ttu-id="ab3ec-563">Registro Nacional de Pessoas Jurídicas
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-563">National Registry of Legal Entities</span></span> 
- <span data-ttu-id="ab3ec-564">Registro de Contribuintes
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-564">Taxpayers Registry</span></span> 
- <span data-ttu-id="ab3ec-565">Pessoa jurídica
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-565">Legal entity</span></span> 
- <span data-ttu-id="ab3ec-566">Pessoas jurídicas
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-566">Legal entities</span></span> 
- <span data-ttu-id="ab3ec-567">Status do Registro
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-567">Registration Status</span></span> 
- <span data-ttu-id="ab3ec-568">Comercial
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-568">Business</span></span> 
- <span data-ttu-id="ab3ec-569">Empresa</span><span class="sxs-lookup"><span data-stu-id="ab3ec-569">Company</span></span>
- <span data-ttu-id="ab3ec-570">CNPJ
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-570">CNPJ</span></span> 
- <span data-ttu-id="ab3ec-571">Cadastro Nacional da Pessoa Jurídica
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-571">Cadastro Nacional da Pessoa Jurídica</span></span> 
- <span data-ttu-id="ab3ec-572">Cadastro Geral de Contribuintes
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-572">Cadastro Geral de Contribuintes</span></span> 
- <span data-ttu-id="ab3ec-573">CGC
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-573">CGC</span></span> 
- <span data-ttu-id="ab3ec-574">Pessoa jurídica
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-574">Pessoa jurídica</span></span> 
- <span data-ttu-id="ab3ec-575">Pessoas jurídicas
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-575">Pessoas jurídicas</span></span> 
- <span data-ttu-id="ab3ec-576">Situação cadastral
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-576">Situação cadastral</span></span> 
- <span data-ttu-id="ab3ec-577">Inscrição
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-577">Inscrição</span></span> 
- <span data-ttu-id="ab3ec-578">Empresa
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-578">Empresa</span></span> 
   
## <a name="brazil-national-id-card-rg"></a><span data-ttu-id="ab3ec-579">	Cartão de Identidade Nacional (RG) do Brasil</span><span class="sxs-lookup"><span data-stu-id="ab3ec-579">Brazil National ID Card (RG)</span></span>

### <a name="format"></a><span data-ttu-id="ab3ec-580">Formato</span><span class="sxs-lookup"><span data-stu-id="ab3ec-580">Format</span></span>

<span data-ttu-id="ab3ec-581">Registro Geral (formato antigo): nove dígitos</span><span class="sxs-lookup"><span data-stu-id="ab3ec-581">Registro Geral (old format): Nine digits</span></span>

<span data-ttu-id="ab3ec-582">Registro de Identidade (RIC) (novo formato): 11 dígitos</span><span class="sxs-lookup"><span data-stu-id="ab3ec-582">Registro de Identidade (RIC) (new format): 11 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="ab3ec-583">Padrão</span><span class="sxs-lookup"><span data-stu-id="ab3ec-583">Pattern</span></span>

<span data-ttu-id="ab3ec-584">Registro Geral (formato antigo):</span><span class="sxs-lookup"><span data-stu-id="ab3ec-584">Registro Geral (old format):</span></span>
- <span data-ttu-id="ab3ec-585">Dois dígitos</span><span class="sxs-lookup"><span data-stu-id="ab3ec-585">Two digits</span></span> 
- <span data-ttu-id="ab3ec-586">Um ponto </span><span class="sxs-lookup"><span data-stu-id="ab3ec-586">A period</span></span> 
- <span data-ttu-id="ab3ec-587">Três dígitos</span><span class="sxs-lookup"><span data-stu-id="ab3ec-587">Three digits</span></span> 
- <span data-ttu-id="ab3ec-588">Um ponto </span><span class="sxs-lookup"><span data-stu-id="ab3ec-588">A period</span></span> 
- <span data-ttu-id="ab3ec-589">Três dígitos</span><span class="sxs-lookup"><span data-stu-id="ab3ec-589">Three digits</span></span> 
- <span data-ttu-id="ab3ec-590">Um hífen</span><span class="sxs-lookup"><span data-stu-id="ab3ec-590">A hyphen</span></span> 
- <span data-ttu-id="ab3ec-591">Um dígito que é um dígito de verificação</span><span class="sxs-lookup"><span data-stu-id="ab3ec-591">One digit which is a check digit</span></span>

<span data-ttu-id="ab3ec-592">Registro de Identidade (RIC) (formato novo):</span><span class="sxs-lookup"><span data-stu-id="ab3ec-592">Registro de Identidade (RIC) (new format):</span></span>
- <span data-ttu-id="ab3ec-593">10 dígitos </span><span class="sxs-lookup"><span data-stu-id="ab3ec-593">10 digits</span></span> 
- <span data-ttu-id="ab3ec-594">Um hífen</span><span class="sxs-lookup"><span data-stu-id="ab3ec-594">A hyphen</span></span> 
- <span data-ttu-id="ab3ec-595">Um dígito que é um dígito de verificação</span><span class="sxs-lookup"><span data-stu-id="ab3ec-595">One digit which is a check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="ab3ec-596">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="ab3ec-596">Checksum</span></span>

<span data-ttu-id="ab3ec-597">Sim</span><span class="sxs-lookup"><span data-stu-id="ab3ec-597">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="ab3ec-598">Definição</span><span class="sxs-lookup"><span data-stu-id="ab3ec-598">Definition</span></span>

<span data-ttu-id="ab3ec-599">Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="ab3ec-599">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="ab3ec-600">A função Func_brazil_rg encontra o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-600">The function Func_brazil_rg finds content that matches the pattern.</span></span>
- <span data-ttu-id="ab3ec-601">Uma palavra-chave de Keyword_brazil_rg é encontrada.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-601">A keyword from Keyword_brazil_rg is found.</span></span>
- <span data-ttu-id="ab3ec-602">A soma de verificação passa.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-602">The checksum passes.</span></span>

<span data-ttu-id="ab3ec-603">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="ab3ec-603">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="ab3ec-604">A função Func_brazil_rg encontra o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-604">The function Func_brazil_rg finds content that matches the pattern.</span></span>
- <span data-ttu-id="ab3ec-605">A soma de verificação passa.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-605">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="ab3ec-606">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="ab3ec-606">Keywords</span></span>

#### <a name="keywordbrazilrg"></a><span data-ttu-id="ab3ec-607">Keyword_brazil_rg</span><span class="sxs-lookup"><span data-stu-id="ab3ec-607">Keyword_brazil_rg</span></span>

<span data-ttu-id="ab3ec-608">Cédula de identidade cartão de identificação id nacional número de rregistro registro de Iidentidade registro geral RG (essa palavra-chave diferencia maiusculas de minúsculas) RIC (essa palavra-chave diferencia maiusculas de minúsculas)</span><span class="sxs-lookup"><span data-stu-id="ab3ec-608">Cédula de identidade identity card national id número de rregistro registro de Iidentidade registro geral RG (this keyword is case sensitive) RIC (this keyword is case sensitive)</span></span> 
   
## <a name="canada-bank-account-number"></a><span data-ttu-id="ab3ec-609">Número de conta bancária do Canadá</span><span class="sxs-lookup"><span data-stu-id="ab3ec-609">Canada Bank Account Number</span></span>

### <a name="format"></a><span data-ttu-id="ab3ec-610">Formato</span><span class="sxs-lookup"><span data-stu-id="ab3ec-610">Format</span></span>

<span data-ttu-id="ab3ec-611">Sete ou doze dígitos</span><span class="sxs-lookup"><span data-stu-id="ab3ec-611">Seven or twelve digits</span></span>

### <a name="pattern"></a><span data-ttu-id="ab3ec-612">Padrão</span><span class="sxs-lookup"><span data-stu-id="ab3ec-612">Pattern</span></span>

<span data-ttu-id="ab3ec-613">Um número de conta bancária do Canadá tem sete ou doze dígitos.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-613">A Canada Bank Account Number is seven or twelve digits.</span></span>

<span data-ttu-id="ab3ec-614">Um número de trânsito de conta bancária do Canadá tem:</span><span class="sxs-lookup"><span data-stu-id="ab3ec-614">A Canada bank account transit number is:</span></span>
- <span data-ttu-id="ab3ec-615">Cinco dígitos</span><span class="sxs-lookup"><span data-stu-id="ab3ec-615">Five digits</span></span> 
- <span data-ttu-id="ab3ec-616">Um hífen</span><span class="sxs-lookup"><span data-stu-id="ab3ec-616">A hyphen</span></span> 
- <span data-ttu-id="ab3ec-617">Três dígitos ou</span><span class="sxs-lookup"><span data-stu-id="ab3ec-617">Three digits OR</span></span>
- <span data-ttu-id="ab3ec-618">Um zero "0"</span><span class="sxs-lookup"><span data-stu-id="ab3ec-618">A zero "0"</span></span> 
- <span data-ttu-id="ab3ec-619">Oito dígitos</span><span class="sxs-lookup"><span data-stu-id="ab3ec-619">Eight digits</span></span>

### <a name="checksum"></a><span data-ttu-id="ab3ec-620">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="ab3ec-620">Checksum</span></span>

<span data-ttu-id="ab3ec-621">Não</span><span class="sxs-lookup"><span data-stu-id="ab3ec-621">No</span></span>

### <a name="definition"></a><span data-ttu-id="ab3ec-622">Definição</span><span class="sxs-lookup"><span data-stu-id="ab3ec-622">Definition</span></span>

<span data-ttu-id="ab3ec-623">Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="ab3ec-623">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="ab3ec-624">A expressão regular Regex_canada_bank_account_number localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-624">The regular expression Regex_canada_bank_account_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="ab3ec-625">Uma palavra-chave de Keyword_canada_bank_account_number for encontrada.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-625">A keyword from Keyword_canada_bank_account_number is found.</span></span>
- <span data-ttu-id="ab3ec-626">A expressão regular Regex_canada_bank_account_transit_number localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-626">The regular expression Regex_canada_bank_account_transit_number finds content that matches the pattern.</span></span>

<span data-ttu-id="ab3ec-627">Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="ab3ec-627">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="ab3ec-628">A expressão regular Regex_canada_bank_account_number localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-628">The regular expression Regex_canada_bank_account_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="ab3ec-629">Uma palavra-chave de Keyword_canada_bank_account_number for encontrada.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-629">A keyword from Keyword_canada_bank_account_number is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="ab3ec-630">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="ab3ec-630">Keywords</span></span>

#### <a name="keywordcanadabankaccountnumber"></a><span data-ttu-id="ab3ec-631">Keyword_canada_bank_account_number</span><span class="sxs-lookup"><span data-stu-id="ab3ec-631">Keyword_canada_bank_account_number</span></span>

- <span data-ttu-id="ab3ec-632">canada savings bonds</span><span class="sxs-lookup"><span data-stu-id="ab3ec-632">canada savings bonds</span></span>
- <span data-ttu-id="ab3ec-633">
canada revenue agency</span><span class="sxs-lookup"><span data-stu-id="ab3ec-633">canada revenue agency</span></span>
- <span data-ttu-id="ab3ec-634">
canadian financial institution</span><span class="sxs-lookup"><span data-stu-id="ab3ec-634">canadian financial institution</span></span>
- <span data-ttu-id="ab3ec-635">
direct deposit form</span><span class="sxs-lookup"><span data-stu-id="ab3ec-635">direct deposit form</span></span>
- <span data-ttu-id="ab3ec-636">
canadian citizen</span><span class="sxs-lookup"><span data-stu-id="ab3ec-636">canadian citizen</span></span>
- <span data-ttu-id="ab3ec-637">
legal representative</span><span class="sxs-lookup"><span data-stu-id="ab3ec-637">legal representative</span></span>
- <span data-ttu-id="ab3ec-638">
notary public</span><span class="sxs-lookup"><span data-stu-id="ab3ec-638">notary public</span></span>
- <span data-ttu-id="ab3ec-639">
commissioner for oaths</span><span class="sxs-lookup"><span data-stu-id="ab3ec-639">commissioner for oaths</span></span>
- <span data-ttu-id="ab3ec-640">
child care benefit</span><span class="sxs-lookup"><span data-stu-id="ab3ec-640">child care benefit</span></span>
- <span data-ttu-id="ab3ec-641">
universal child care</span><span class="sxs-lookup"><span data-stu-id="ab3ec-641">universal child care</span></span>
- <span data-ttu-id="ab3ec-642">
canada child tax benefit</span><span class="sxs-lookup"><span data-stu-id="ab3ec-642">canada child tax benefit</span></span>
- <span data-ttu-id="ab3ec-643">
income tax benefit</span><span class="sxs-lookup"><span data-stu-id="ab3ec-643">income tax benefit</span></span>
- <span data-ttu-id="ab3ec-644">
harmonized sales tax</span><span class="sxs-lookup"><span data-stu-id="ab3ec-644">harmonized sales tax</span></span>
- <span data-ttu-id="ab3ec-645">social insurance number</span><span class="sxs-lookup"><span data-stu-id="ab3ec-645">social insurance number</span></span>
- <span data-ttu-id="ab3ec-646">
income tax refund</span><span class="sxs-lookup"><span data-stu-id="ab3ec-646">income tax refund</span></span>
- <span data-ttu-id="ab3ec-647">
child tax benefit</span><span class="sxs-lookup"><span data-stu-id="ab3ec-647">child tax benefit</span></span>
- <span data-ttu-id="ab3ec-648">
territorial payments</span><span class="sxs-lookup"><span data-stu-id="ab3ec-648">territorial payments</span></span>
- <span data-ttu-id="ab3ec-649">
institution number</span><span class="sxs-lookup"><span data-stu-id="ab3ec-649">institution number</span></span>
- <span data-ttu-id="ab3ec-650">
deposit request</span><span class="sxs-lookup"><span data-stu-id="ab3ec-650">deposit request</span></span>
- <span data-ttu-id="ab3ec-651">
banking information</span><span class="sxs-lookup"><span data-stu-id="ab3ec-651">banking information</span></span>
- <span data-ttu-id="ab3ec-652">

direct deposit</span><span class="sxs-lookup"><span data-stu-id="ab3ec-652">direct deposit</span></span>
   
## <a name="canada-drivers-license-number"></a><span data-ttu-id="ab3ec-653">Número de carteira de motorista do Canadá</span><span class="sxs-lookup"><span data-stu-id="ab3ec-653">Canada Driver's License Number</span></span>

### <a name="format"></a><span data-ttu-id="ab3ec-654">Formato</span><span class="sxs-lookup"><span data-stu-id="ab3ec-654">Format</span></span>

<span data-ttu-id="ab3ec-655">Varia por província</span><span class="sxs-lookup"><span data-stu-id="ab3ec-655">Varies by province</span></span>

### <a name="pattern"></a><span data-ttu-id="ab3ec-656">Padrão</span><span class="sxs-lookup"><span data-stu-id="ab3ec-656">Pattern</span></span>

<span data-ttu-id="ab3ec-657">Vários padrões que abrangem Alberta, Columbia Britânica, Manitoba, New Brunswick, Newfoundland/Labrador, Nova Escócia, Ontário, Ilha do Príncipe Eduardo, Quebec e Saskatchewan</span><span class="sxs-lookup"><span data-stu-id="ab3ec-657">Various patterns covering Alberta, British Columbia, Manitoba, New Brunswick, Newfoundland/Labrador, Nova Scotia, Ontario, Prince Edward Island, Quebec, and Saskatchewan</span></span>

### <a name="checksum"></a><span data-ttu-id="ab3ec-658">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="ab3ec-658">Checksum</span></span>

<span data-ttu-id="ab3ec-659">Não</span><span class="sxs-lookup"><span data-stu-id="ab3ec-659">No</span></span>

### <a name="definition"></a><span data-ttu-id="ab3ec-660">Definição</span><span class="sxs-lookup"><span data-stu-id="ab3ec-660">Definition</span></span>

<span data-ttu-id="ab3ec-661">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="ab3ec-661">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="ab3ec-662">A função Func_[province_name]_drivers_license_number localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-662">The function Func_[province_name]_drivers_license_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="ab3ec-663">Uma palavra-chave de Keyword_[province_name]_drivers_license_name for encontrada.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-663">A keyword from Keyword_[province_name]_drivers_license_name is found.</span></span>
- <span data-ttu-id="ab3ec-664">Uma palavra-chave de Keyword_canada_drivers_license for encontrada.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-664">A keyword from Keyword_canada_drivers_license is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="ab3ec-665">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="ab3ec-665">Keywords</span></span>

#### <a name="keywordprovincenamedriverslicensename"></a><span data-ttu-id="ab3ec-666">Keyword_[province_name]_drivers_license_name</span><span class="sxs-lookup"><span data-stu-id="ab3ec-666">Keyword_[province_name]_drivers_license_name</span></span>

- <span data-ttu-id="ab3ec-667">A abreviação da província, por exemplo AB</span><span class="sxs-lookup"><span data-stu-id="ab3ec-667">The province abbreviation, for example AB</span></span>
- <span data-ttu-id="ab3ec-668">
O nome da província, por exemplo, Alberta</span><span class="sxs-lookup"><span data-stu-id="ab3ec-668">The province name, for example Alberta</span></span>

#### <a name="keywordcanadadriverslicense"></a><span data-ttu-id="ab3ec-669">Keyword_canada_drivers_license</span><span class="sxs-lookup"><span data-stu-id="ab3ec-669">Keyword_canada_drivers_license</span></span>

- <span data-ttu-id="ab3ec-670">DL</span><span class="sxs-lookup"><span data-stu-id="ab3ec-670">DL</span></span>
- <span data-ttu-id="ab3ec-671">DLS</span><span class="sxs-lookup"><span data-stu-id="ab3ec-671">DLS</span></span>
- <span data-ttu-id="ab3ec-672">CDL</span><span class="sxs-lookup"><span data-stu-id="ab3ec-672">CDL</span></span>
- <span data-ttu-id="ab3ec-673">CDLS</span><span class="sxs-lookup"><span data-stu-id="ab3ec-673">CDLS</span></span>
- <span data-ttu-id="ab3ec-674">DriverLic</span><span class="sxs-lookup"><span data-stu-id="ab3ec-674">DriverLic</span></span>
- <span data-ttu-id="ab3ec-675">DriverLics</span><span class="sxs-lookup"><span data-stu-id="ab3ec-675">DriverLics</span></span>
- <span data-ttu-id="ab3ec-676">DriverLicense</span><span class="sxs-lookup"><span data-stu-id="ab3ec-676">DriverLicense</span></span>
- <span data-ttu-id="ab3ec-677">DriverLicenses</span><span class="sxs-lookup"><span data-stu-id="ab3ec-677">DriverLicenses</span></span>
- <span data-ttu-id="ab3ec-678">DriverLicence</span><span class="sxs-lookup"><span data-stu-id="ab3ec-678">DriverLicence</span></span>
- <span data-ttu-id="ab3ec-679">DriverLicences</span><span class="sxs-lookup"><span data-stu-id="ab3ec-679">DriverLicences</span></span>
- <span data-ttu-id="ab3ec-680">Driver Lic</span><span class="sxs-lookup"><span data-stu-id="ab3ec-680">Driver Lic</span></span>
- <span data-ttu-id="ab3ec-681">Driver Lics</span><span class="sxs-lookup"><span data-stu-id="ab3ec-681">Driver Lics</span></span>
- <span data-ttu-id="ab3ec-682">Driver de licença</span><span class="sxs-lookup"><span data-stu-id="ab3ec-682">Driver License</span></span>
- <span data-ttu-id="ab3ec-683">Licenças de driver</span><span class="sxs-lookup"><span data-stu-id="ab3ec-683">Driver Licenses</span></span>
- <span data-ttu-id="ab3ec-684">Driver Licence
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-684">Driver Licence</span></span>
- <span data-ttu-id="ab3ec-685">Driver Licences
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-685">Driver Licences</span></span>
- <span data-ttu-id="ab3ec-686">DriversLic</span><span class="sxs-lookup"><span data-stu-id="ab3ec-686">DriversLic</span></span>
- <span data-ttu-id="ab3ec-687">DriversLics</span><span class="sxs-lookup"><span data-stu-id="ab3ec-687">DriversLics</span></span>
- <span data-ttu-id="ab3ec-688">DriversLicence</span><span class="sxs-lookup"><span data-stu-id="ab3ec-688">DriversLicence</span></span>
- <span data-ttu-id="ab3ec-689">DriversLicences</span><span class="sxs-lookup"><span data-stu-id="ab3ec-689">DriversLicences</span></span>
- <span data-ttu-id="ab3ec-690">CarteiraDeMotorista</span><span class="sxs-lookup"><span data-stu-id="ab3ec-690">DriversLicense</span></span>
- <span data-ttu-id="ab3ec-691">DriversLicenses</span><span class="sxs-lookup"><span data-stu-id="ab3ec-691">DriversLicenses</span></span>
- <span data-ttu-id="ab3ec-692">Drivers Lic</span><span class="sxs-lookup"><span data-stu-id="ab3ec-692">Drivers Lic</span></span>
- <span data-ttu-id="ab3ec-693">Drivers Lics</span><span class="sxs-lookup"><span data-stu-id="ab3ec-693">Drivers Lics</span></span>
- <span data-ttu-id="ab3ec-694">Carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="ab3ec-694">Drivers License</span></span>
- <span data-ttu-id="ab3ec-695">Licenças de drivers</span><span class="sxs-lookup"><span data-stu-id="ab3ec-695">Drivers Licenses</span></span>
- <span data-ttu-id="ab3ec-696">Drivers de licença</span><span class="sxs-lookup"><span data-stu-id="ab3ec-696">Drivers Licence</span></span>
- <span data-ttu-id="ab3ec-697">Licenças de drivers</span><span class="sxs-lookup"><span data-stu-id="ab3ec-697">Drivers Licences</span></span>
- <span data-ttu-id="ab3ec-698">Driver'Lic</span><span class="sxs-lookup"><span data-stu-id="ab3ec-698">Driver'Lic</span></span>
- <span data-ttu-id="ab3ec-699">Driver'Lics</span><span class="sxs-lookup"><span data-stu-id="ab3ec-699">Driver'Lics</span></span>
- <span data-ttu-id="ab3ec-700">Driver'License</span><span class="sxs-lookup"><span data-stu-id="ab3ec-700">Driver'License</span></span>
- <span data-ttu-id="ab3ec-701">Driver'Licenses</span><span class="sxs-lookup"><span data-stu-id="ab3ec-701">Driver'Licenses</span></span>
- <span data-ttu-id="ab3ec-702">Driver'Licence</span><span class="sxs-lookup"><span data-stu-id="ab3ec-702">Driver'Licence</span></span>
- <span data-ttu-id="ab3ec-703">Driver'Licences</span><span class="sxs-lookup"><span data-stu-id="ab3ec-703">Driver'Licences</span></span>
- <span data-ttu-id="ab3ec-704">Driver' Lic</span><span class="sxs-lookup"><span data-stu-id="ab3ec-704">Driver' Lic</span></span>
- <span data-ttu-id="ab3ec-705">Driver' Lics</span><span class="sxs-lookup"><span data-stu-id="ab3ec-705">Driver' Lics</span></span>
- <span data-ttu-id="ab3ec-706">Driver' licença</span><span class="sxs-lookup"><span data-stu-id="ab3ec-706">Driver' License</span></span>
- <span data-ttu-id="ab3ec-707">Driver' licenças</span><span class="sxs-lookup"><span data-stu-id="ab3ec-707">Driver' Licenses</span></span>
- <span data-ttu-id="ab3ec-708">Driver' licença</span><span class="sxs-lookup"><span data-stu-id="ab3ec-708">Driver' Licence</span></span>
- <span data-ttu-id="ab3ec-709">Driver' licenças</span><span class="sxs-lookup"><span data-stu-id="ab3ec-709">Driver' Licences</span></span>
- <span data-ttu-id="ab3ec-710">Driver'sLic</span><span class="sxs-lookup"><span data-stu-id="ab3ec-710">Driver'sLic</span></span>
- <span data-ttu-id="ab3ec-711">Driver'sLics</span><span class="sxs-lookup"><span data-stu-id="ab3ec-711">Driver'sLics</span></span>
- <span data-ttu-id="ab3ec-712">Driver'sLicense</span><span class="sxs-lookup"><span data-stu-id="ab3ec-712">Driver'sLicense</span></span>
- <span data-ttu-id="ab3ec-713">Driver'sLicenses</span><span class="sxs-lookup"><span data-stu-id="ab3ec-713">Driver'sLicenses</span></span>
- <span data-ttu-id="ab3ec-714">Driver'sLicence</span><span class="sxs-lookup"><span data-stu-id="ab3ec-714">Driver'sLicence</span></span>
- <span data-ttu-id="ab3ec-715">Driver'sLicences</span><span class="sxs-lookup"><span data-stu-id="ab3ec-715">Driver'sLicences</span></span>
- <span data-ttu-id="ab3ec-716">Lic do driver</span><span class="sxs-lookup"><span data-stu-id="ab3ec-716">Driver's Lic</span></span>
- <span data-ttu-id="ab3ec-717">Lics do driver</span><span class="sxs-lookup"><span data-stu-id="ab3ec-717">Driver's Lics</span></span>
- <span data-ttu-id="ab3ec-718">De motorista carteira</span><span class="sxs-lookup"><span data-stu-id="ab3ec-718">Driver's License</span></span>
- <span data-ttu-id="ab3ec-719">Licenças de motorista</span><span class="sxs-lookup"><span data-stu-id="ab3ec-719">Driver's Licenses</span></span>
- <span data-ttu-id="ab3ec-720">Driver's Licence
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-720">Driver's Licence</span></span>
- <span data-ttu-id="ab3ec-721">Driver's Licences
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-721">Driver's Licences</span></span>
- <span data-ttu-id="ab3ec-722">Permis de Conduire</span><span class="sxs-lookup"><span data-stu-id="ab3ec-722">Permis de Conduire</span></span>
- <span data-ttu-id="ab3ec-723">id</span><span class="sxs-lookup"><span data-stu-id="ab3ec-723">id</span></span>
- <span data-ttu-id="ab3ec-724">IDs</span><span class="sxs-lookup"><span data-stu-id="ab3ec-724">ids</span></span>
- <span data-ttu-id="ab3ec-725">
idcard number</span><span class="sxs-lookup"><span data-stu-id="ab3ec-725">idcard number</span></span>
- <span data-ttu-id="ab3ec-726">
idcard numbers</span><span class="sxs-lookup"><span data-stu-id="ab3ec-726">idcard numbers</span></span>
- <span data-ttu-id="ab3ec-727">
idcard #</span><span class="sxs-lookup"><span data-stu-id="ab3ec-727">idcard #</span></span>
- <span data-ttu-id="ab3ec-728">
idcard #s</span><span class="sxs-lookup"><span data-stu-id="ab3ec-728">idcard #s</span></span>
- <span data-ttu-id="ab3ec-729">cartão de idcard</span><span class="sxs-lookup"><span data-stu-id="ab3ec-729">idcard card</span></span>
- <span data-ttu-id="ab3ec-730">cartões de idcard</span><span class="sxs-lookup"><span data-stu-id="ab3ec-730">idcard cards</span></span>
- <span data-ttu-id="ab3ec-731">idcard</span><span class="sxs-lookup"><span data-stu-id="ab3ec-731">idcard</span></span>
- <span data-ttu-id="ab3ec-732">identification number
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-732">identification number</span></span>
- <span data-ttu-id="ab3ec-733">identification numbers
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-733">identification numbers</span></span>
- <span data-ttu-id="ab3ec-734">identification #
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-734">identification #</span></span>
- <span data-ttu-id="ab3ec-735">
identification #s</span><span class="sxs-lookup"><span data-stu-id="ab3ec-735">identification #s</span></span>
- <span data-ttu-id="ab3ec-736">cartão de identificação</span><span class="sxs-lookup"><span data-stu-id="ab3ec-736">identification card</span></span>
- <span data-ttu-id="ab3ec-737">cartões de identificação</span><span class="sxs-lookup"><span data-stu-id="ab3ec-737">identification cards</span></span>
- <span data-ttu-id="ab3ec-738">
identification
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-738">identification</span></span> 
- <span data-ttu-id="ab3ec-739">DL#</span><span class="sxs-lookup"><span data-stu-id="ab3ec-739">DL#</span></span>
- <span data-ttu-id="ab3ec-740">
DLS#
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-740">DLS#</span></span> 
- <span data-ttu-id="ab3ec-741">CDL#
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-741">CDL#</span></span> 
- <span data-ttu-id="ab3ec-742">CDLS#
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-742">CDLS#</span></span> 
- <span data-ttu-id="ab3ec-743">DriverLic #</span><span class="sxs-lookup"><span data-stu-id="ab3ec-743">DriverLic#</span></span> 
- <span data-ttu-id="ab3ec-744">DriverLics #</span><span class="sxs-lookup"><span data-stu-id="ab3ec-744">DriverLics#</span></span> 
- <span data-ttu-id="ab3ec-745">DriverLicense #</span><span class="sxs-lookup"><span data-stu-id="ab3ec-745">DriverLicense#</span></span> 
- <span data-ttu-id="ab3ec-746">DriverLicenses #</span><span class="sxs-lookup"><span data-stu-id="ab3ec-746">DriverLicenses#</span></span> 
- <span data-ttu-id="ab3ec-747">DriverLicence #</span><span class="sxs-lookup"><span data-stu-id="ab3ec-747">DriverLicence#</span></span> 
- <span data-ttu-id="ab3ec-748">DriverLicences #</span><span class="sxs-lookup"><span data-stu-id="ab3ec-748">DriverLicences#</span></span> 
- <span data-ttu-id="ab3ec-749">Driver Lic#</span><span class="sxs-lookup"><span data-stu-id="ab3ec-749">Driver Lic#</span></span>
- <span data-ttu-id="ab3ec-750">
Driver Lics#
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-750">Driver Lics#</span></span> 
- <span data-ttu-id="ab3ec-751">Licença do driver #</span><span class="sxs-lookup"><span data-stu-id="ab3ec-751">Driver License#</span></span> 
- <span data-ttu-id="ab3ec-752">Driver licenças #</span><span class="sxs-lookup"><span data-stu-id="ab3ec-752">Driver Licenses#</span></span> 
- <span data-ttu-id="ab3ec-753">Licença do driver #</span><span class="sxs-lookup"><span data-stu-id="ab3ec-753">Driver License#</span></span> 
- <span data-ttu-id="ab3ec-754">Driver licenças #</span><span class="sxs-lookup"><span data-stu-id="ab3ec-754">Driver Licences#</span></span> 
- <span data-ttu-id="ab3ec-755">DriversLic #</span><span class="sxs-lookup"><span data-stu-id="ab3ec-755">DriversLic#</span></span> 
- <span data-ttu-id="ab3ec-756">DriversLics #</span><span class="sxs-lookup"><span data-stu-id="ab3ec-756">DriversLics#</span></span> 
- <span data-ttu-id="ab3ec-757">CarteiraDeMotorista #</span><span class="sxs-lookup"><span data-stu-id="ab3ec-757">DriversLicense#</span></span> 
- <span data-ttu-id="ab3ec-758">DriversLicenses #</span><span class="sxs-lookup"><span data-stu-id="ab3ec-758">DriversLicenses#</span></span> 
- <span data-ttu-id="ab3ec-759">DriversLicence #</span><span class="sxs-lookup"><span data-stu-id="ab3ec-759">DriversLicence#</span></span> 
- <span data-ttu-id="ab3ec-760">DriversLicences #</span><span class="sxs-lookup"><span data-stu-id="ab3ec-760">DriversLicences#</span></span> 
- <span data-ttu-id="ab3ec-761">Drivers Lic #</span><span class="sxs-lookup"><span data-stu-id="ab3ec-761">Drivers Lic#</span></span> 
- <span data-ttu-id="ab3ec-762">Drivers Lics #</span><span class="sxs-lookup"><span data-stu-id="ab3ec-762">Drivers Lics#</span></span> 
- <span data-ttu-id="ab3ec-763">Drivers licença #</span><span class="sxs-lookup"><span data-stu-id="ab3ec-763">Drivers License#</span></span> 
- <span data-ttu-id="ab3ec-764">Drivers licenças #</span><span class="sxs-lookup"><span data-stu-id="ab3ec-764">Drivers Licenses#</span></span> 
- <span data-ttu-id="ab3ec-765">Drivers licença #</span><span class="sxs-lookup"><span data-stu-id="ab3ec-765">Drivers Licence#</span></span> 
- <span data-ttu-id="ab3ec-766">Drivers licenças #</span><span class="sxs-lookup"><span data-stu-id="ab3ec-766">Drivers Licences#</span></span> 
- <span data-ttu-id="ab3ec-767">Driver'Lic#
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-767">Driver'Lic#</span></span> 
- <span data-ttu-id="ab3ec-768">Driver'Lics#
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-768">Driver'Lics#</span></span> 
- <span data-ttu-id="ab3ec-769">Driver'License#
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-769">Driver'License#</span></span> 
- <span data-ttu-id="ab3ec-770">Driver'Licenses#
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-770">Driver'Licenses#</span></span> 
- <span data-ttu-id="ab3ec-771">Driver'Licence#
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-771">Driver'Licence#</span></span> 
- <span data-ttu-id="ab3ec-772">Driver'Licences#
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-772">Driver'Licences#</span></span> 
- <span data-ttu-id="ab3ec-773">Driver' Lic#
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-773">Driver' Lic#</span></span> 
- <span data-ttu-id="ab3ec-774">Driver' Lics#
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-774">Driver' Lics#</span></span> 
- <span data-ttu-id="ab3ec-775">Driver' License#
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-775">Driver' License#</span></span> 
- <span data-ttu-id="ab3ec-776">Driver' Licenses#
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-776">Driver' Licenses#</span></span> 
- <span data-ttu-id="ab3ec-777">Driver' licença #</span><span class="sxs-lookup"><span data-stu-id="ab3ec-777">Driver' Licence#</span></span> 
- <span data-ttu-id="ab3ec-778">Driver' licenças #</span><span class="sxs-lookup"><span data-stu-id="ab3ec-778">Driver' Licences#</span></span> 
- <span data-ttu-id="ab3ec-779">Driver'sLic #</span><span class="sxs-lookup"><span data-stu-id="ab3ec-779">Driver'sLic#</span></span> 
- <span data-ttu-id="ab3ec-780">Driver'sLics #</span><span class="sxs-lookup"><span data-stu-id="ab3ec-780">Driver'sLics#</span></span> 
- <span data-ttu-id="ab3ec-781">Driver'sLicense #</span><span class="sxs-lookup"><span data-stu-id="ab3ec-781">Driver'sLicense#</span></span> 
- <span data-ttu-id="ab3ec-782">Driver'sLicenses #</span><span class="sxs-lookup"><span data-stu-id="ab3ec-782">Driver'sLicenses#</span></span> 
- <span data-ttu-id="ab3ec-783">Driver'sLicence #</span><span class="sxs-lookup"><span data-stu-id="ab3ec-783">Driver'sLicence#</span></span> 
- <span data-ttu-id="ab3ec-784">Driver'sLicences #</span><span class="sxs-lookup"><span data-stu-id="ab3ec-784">Driver'sLicences#</span></span> 
- <span data-ttu-id="ab3ec-785">Driver's Lic#
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-785">Driver's Lic#</span></span> 
- <span data-ttu-id="ab3ec-786">Driver's Lics#
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-786">Driver's Lics#</span></span> 
- <span data-ttu-id="ab3ec-787">Driver's License#
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-787">Driver's License#</span></span> 
- <span data-ttu-id="ab3ec-788">Driver's Licenses#
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-788">Driver's Licenses#</span></span> 
- <span data-ttu-id="ab3ec-789">Licença # de motorista</span><span class="sxs-lookup"><span data-stu-id="ab3ec-789">Driver's Licence#</span></span> 
- <span data-ttu-id="ab3ec-790">Licenças # de motorista</span><span class="sxs-lookup"><span data-stu-id="ab3ec-790">Driver's Licences#</span></span> 
- <span data-ttu-id="ab3ec-791">Permis de Conduire #</span><span class="sxs-lookup"><span data-stu-id="ab3ec-791">Permis de Conduire#</span></span> 
- <span data-ttu-id="ab3ec-792">ID #</span><span class="sxs-lookup"><span data-stu-id="ab3ec-792">id#</span></span> 
- <span data-ttu-id="ab3ec-793">IDs #</span><span class="sxs-lookup"><span data-stu-id="ab3ec-793">ids#</span></span> 
- <span data-ttu-id="ab3ec-794">idcard card#
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-794">idcard card#</span></span> 
- <span data-ttu-id="ab3ec-795">idcard cards#
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-795">idcard cards#</span></span> 
- <span data-ttu-id="ab3ec-796">idcard #
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-796">idcard#</span></span> 
- <span data-ttu-id="ab3ec-797">identification card#
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-797">identification card#</span></span> 
- <span data-ttu-id="ab3ec-798">identification cards#
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-798">identification cards#</span></span> 
- <span data-ttu-id="ab3ec-799">identification #
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-799">identification#</span></span> 
   
## <a name="canada-health-service-number"></a><span data-ttu-id="ab3ec-800">Número de serviço de saúde do Canadá</span><span class="sxs-lookup"><span data-stu-id="ab3ec-800">Canada Health Service Number</span></span>

### <a name="format"></a><span data-ttu-id="ab3ec-801">Formato</span><span class="sxs-lookup"><span data-stu-id="ab3ec-801">Format</span></span>

<span data-ttu-id="ab3ec-802">10 dígitos</span><span class="sxs-lookup"><span data-stu-id="ab3ec-802">10 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="ab3ec-803">Padrão</span><span class="sxs-lookup"><span data-stu-id="ab3ec-803">Pattern</span></span>

<span data-ttu-id="ab3ec-804">10 dígitos</span><span class="sxs-lookup"><span data-stu-id="ab3ec-804">10 digits</span></span>

### <a name="checksum"></a><span data-ttu-id="ab3ec-805">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="ab3ec-805">Checksum</span></span>

<span data-ttu-id="ab3ec-806">Não</span><span class="sxs-lookup"><span data-stu-id="ab3ec-806">No</span></span>

### <a name="definition"></a><span data-ttu-id="ab3ec-807">Definição</span><span class="sxs-lookup"><span data-stu-id="ab3ec-807">Definition</span></span>

<span data-ttu-id="ab3ec-808">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="ab3ec-808">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="ab3ec-809">A expressão regular Regex_canada_health_service_number localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-809">The regular expression Regex_canada_health_service_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="ab3ec-810">Uma palavra-chave de Keyword_canada_health_service_number for encontrada.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-810">A keyword from Keyword_canada_health_service_number is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="ab3ec-811">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="ab3ec-811">Keywords</span></span>

#### <a name="keywordcanadahealthservicenumber"></a><span data-ttu-id="ab3ec-812">Keyword_canada_health_service_number</span><span class="sxs-lookup"><span data-stu-id="ab3ec-812">Keyword_canada_health_service_number</span></span>

- <span data-ttu-id="ab3ec-813">personal health number</span><span class="sxs-lookup"><span data-stu-id="ab3ec-813">personal health number</span></span>
- <span data-ttu-id="ab3ec-814">
patient information</span><span class="sxs-lookup"><span data-stu-id="ab3ec-814">patient information</span></span>
- <span data-ttu-id="ab3ec-815">Serviços de integridade</span><span class="sxs-lookup"><span data-stu-id="ab3ec-815">health services</span></span>
- <span data-ttu-id="ab3ec-816">
speciality services</span><span class="sxs-lookup"><span data-stu-id="ab3ec-816">speciality services</span></span>
- <span data-ttu-id="ab3ec-817">
automobile accident</span><span class="sxs-lookup"><span data-stu-id="ab3ec-817">automobile accident</span></span>
- <span data-ttu-id="ab3ec-818">
patient hospital</span><span class="sxs-lookup"><span data-stu-id="ab3ec-818">patient hospital</span></span>
- <span data-ttu-id="ab3ec-819">
psychiatrist</span><span class="sxs-lookup"><span data-stu-id="ab3ec-819">psychiatrist</span></span>
- <span data-ttu-id="ab3ec-820">
workers compensation</span><span class="sxs-lookup"><span data-stu-id="ab3ec-820">workers compensation</span></span>
- <span data-ttu-id="ab3ec-821">
disability</span><span class="sxs-lookup"><span data-stu-id="ab3ec-821">disability</span></span>
      
## <a name="canada-passport-number"></a><span data-ttu-id="ab3ec-822">Número de passaporte do Canadá</span><span class="sxs-lookup"><span data-stu-id="ab3ec-822">Canada Passport Number</span></span>

### <a name="format"></a><span data-ttu-id="ab3ec-823">Formato</span><span class="sxs-lookup"><span data-stu-id="ab3ec-823">Format</span></span>

<span data-ttu-id="ab3ec-824">Duas letras maiúsculas, seguidas de seis dígitos</span><span class="sxs-lookup"><span data-stu-id="ab3ec-824">Two uppercase letters followed by six digits</span></span>

### <a name="pattern"></a><span data-ttu-id="ab3ec-825">Padrão</span><span class="sxs-lookup"><span data-stu-id="ab3ec-825">Pattern</span></span>

<span data-ttu-id="ab3ec-826">Duas letras maiúsculas, seguidas de seis dígitos</span><span class="sxs-lookup"><span data-stu-id="ab3ec-826">Two uppercase letters followed by six digits</span></span>

### <a name="checksum"></a><span data-ttu-id="ab3ec-827">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="ab3ec-827">Checksum</span></span>

<span data-ttu-id="ab3ec-828">Não</span><span class="sxs-lookup"><span data-stu-id="ab3ec-828">No</span></span>

### <a name="definition"></a><span data-ttu-id="ab3ec-829">Definição</span><span class="sxs-lookup"><span data-stu-id="ab3ec-829">Definition</span></span>

<span data-ttu-id="ab3ec-830">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="ab3ec-830">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="ab3ec-831">A expressão regular Regex_canada_passport_number localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-831">The regular expression Regex_canada_passport_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="ab3ec-832">Uma palavra-chave de Keyword_canada_passport_number ou Keyword_passport é encontrada.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-832">A keyword from Keyword_canada_passport_number or Keyword_passport is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="ab3ec-833">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="ab3ec-833">Keywords</span></span>

#### <a name="keywordcanadapassportnumber"></a><span data-ttu-id="ab3ec-834">Keyword_canada_passport_number</span><span class="sxs-lookup"><span data-stu-id="ab3ec-834">Keyword_canada_passport_number</span></span>

- <span data-ttu-id="ab3ec-835">canadian citizenship</span><span class="sxs-lookup"><span data-stu-id="ab3ec-835">canadian citizenship</span></span>
- <span data-ttu-id="ab3ec-836">
canadian passport</span><span class="sxs-lookup"><span data-stu-id="ab3ec-836">canadian passport</span></span>
- <span data-ttu-id="ab3ec-837">
passport application</span><span class="sxs-lookup"><span data-stu-id="ab3ec-837">passport application</span></span>
- <span data-ttu-id="ab3ec-838">
passport photos</span><span class="sxs-lookup"><span data-stu-id="ab3ec-838">passport photos</span></span>
- <span data-ttu-id="ab3ec-839">
certified translator</span><span class="sxs-lookup"><span data-stu-id="ab3ec-839">certified translator</span></span>
- <span data-ttu-id="ab3ec-840">
canadian citizens</span><span class="sxs-lookup"><span data-stu-id="ab3ec-840">canadian citizens</span></span>
- <span data-ttu-id="ab3ec-841">
processing times</span><span class="sxs-lookup"><span data-stu-id="ab3ec-841">processing times</span></span>
- <span data-ttu-id="ab3ec-842">

renewal application</span><span class="sxs-lookup"><span data-stu-id="ab3ec-842">renewal application</span></span>

#### <a name="keywordpassport"></a><span data-ttu-id="ab3ec-843">Keyword_passport</span><span class="sxs-lookup"><span data-stu-id="ab3ec-843">Keyword_passport</span></span>

- <span data-ttu-id="ab3ec-844">Passport Number</span><span class="sxs-lookup"><span data-stu-id="ab3ec-844">Passport Number</span></span>
- <span data-ttu-id="ab3ec-845">
Passport No</span><span class="sxs-lookup"><span data-stu-id="ab3ec-845">Passport No</span></span>
- <span data-ttu-id="ab3ec-846">Passport #
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-846">Passport #</span></span>
- <span data-ttu-id="ab3ec-847">Passport#
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-847">Passport#</span></span>
- <span data-ttu-id="ab3ec-848">PassportID</span><span class="sxs-lookup"><span data-stu-id="ab3ec-848">PassportID</span></span>
- <span data-ttu-id="ab3ec-849">Passportno
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-849">Passportno</span></span>
- <span data-ttu-id="ab3ec-850">passportnumber
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-850">passportnumber</span></span>
- <span data-ttu-id="ab3ec-851">パスポート</span><span class="sxs-lookup"><span data-stu-id="ab3ec-851">パスポート</span></span>
- <span data-ttu-id="ab3ec-852">パスポート番号
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-852">パスポート番号</span></span>
- <span data-ttu-id="ab3ec-853">パスポートのNum
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-853">パスポートのNum</span></span>
- <span data-ttu-id="ab3ec-854">パスポート＃
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-854">パスポート＃</span></span>
- <span data-ttu-id="ab3ec-855">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="ab3ec-855">Numéro de passeport</span></span>
- <span data-ttu-id="ab3ec-856">
Passeport n °</span><span class="sxs-lookup"><span data-stu-id="ab3ec-856">Passeport n °</span></span>
- <span data-ttu-id="ab3ec-857">Passeport Non
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-857">Passeport Non</span></span>
- <span data-ttu-id="ab3ec-858">Passeport #
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-858">Passeport #</span></span>
- <span data-ttu-id="ab3ec-859">Passeport#
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-859">Passeport#</span></span>
- <span data-ttu-id="ab3ec-860">PasseportNon</span><span class="sxs-lookup"><span data-stu-id="ab3ec-860">PasseportNon</span></span>
- <span data-ttu-id="ab3ec-861">

Passeportn °</span><span class="sxs-lookup"><span data-stu-id="ab3ec-861">Passeportn °</span></span>
   
## <a name="canada-personal-health-identification-number-phin"></a><span data-ttu-id="ab3ec-862">Número de identificação pessoal de saúde do Canadá (PHIN)</span><span class="sxs-lookup"><span data-stu-id="ab3ec-862">Canada Personal Health Identification Number (PHIN)</span></span>

### <a name="format"></a><span data-ttu-id="ab3ec-863">Formato</span><span class="sxs-lookup"><span data-stu-id="ab3ec-863">Format</span></span>

<span data-ttu-id="ab3ec-864">Nove dígitos</span><span class="sxs-lookup"><span data-stu-id="ab3ec-864">Nine digits</span></span>

### <a name="pattern"></a><span data-ttu-id="ab3ec-865">Padrão</span><span class="sxs-lookup"><span data-stu-id="ab3ec-865">Pattern</span></span>

<span data-ttu-id="ab3ec-866">Nove dígitos</span><span class="sxs-lookup"><span data-stu-id="ab3ec-866">Nine digits</span></span>

### <a name="checksum"></a><span data-ttu-id="ab3ec-867">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="ab3ec-867">Checksum</span></span>

<span data-ttu-id="ab3ec-868">Não</span><span class="sxs-lookup"><span data-stu-id="ab3ec-868">No</span></span>

### <a name="definition"></a><span data-ttu-id="ab3ec-869">Definição</span><span class="sxs-lookup"><span data-stu-id="ab3ec-869">Definition</span></span>

<span data-ttu-id="ab3ec-p104">Uma política de DLP é 75% confiante de que detectou esse tipo de informações confidenciais if, dentro de uma proximidade de 300 caracteres: A expressão regular Regex_canada_phin encontra o conteúdo que corresponde ao padrão. Pelo menos duas palavras-chave da Keyword_canada_phin ou Keyword_canada_provinces são encontradas..</span><span class="sxs-lookup"><span data-stu-id="ab3ec-p104">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters: The regular expression Regex_canada_phin finds content that matches the pattern. At least two keywords from Keyword_canada_phin or Keyword_canada_provinces are found..</span></span>

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

### <a name="keywords"></a><span data-ttu-id="ab3ec-872">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="ab3ec-872">Keywords</span></span>

#### <a name="keywordcanadaphin"></a><span data-ttu-id="ab3ec-873">Keyword_canada_phin</span><span class="sxs-lookup"><span data-stu-id="ab3ec-873">Keyword_canada_phin</span></span>

- <span data-ttu-id="ab3ec-874">social insurance number</span><span class="sxs-lookup"><span data-stu-id="ab3ec-874">social insurance number</span></span>
- <span data-ttu-id="ab3ec-875">
health information act</span><span class="sxs-lookup"><span data-stu-id="ab3ec-875">health information act</span></span>
- <span data-ttu-id="ab3ec-876">
income tax information</span><span class="sxs-lookup"><span data-stu-id="ab3ec-876">income tax information</span></span>
- <span data-ttu-id="ab3ec-877">
manitoba health</span><span class="sxs-lookup"><span data-stu-id="ab3ec-877">manitoba health</span></span>
- <span data-ttu-id="ab3ec-878">
health registration</span><span class="sxs-lookup"><span data-stu-id="ab3ec-878">health registration</span></span>
- <span data-ttu-id="ab3ec-879">
prescription purchases</span><span class="sxs-lookup"><span data-stu-id="ab3ec-879">prescription purchases</span></span>
- <span data-ttu-id="ab3ec-880">
benefit eligibility</span><span class="sxs-lookup"><span data-stu-id="ab3ec-880">benefit eligibility</span></span>
- <span data-ttu-id="ab3ec-881">
personal health</span><span class="sxs-lookup"><span data-stu-id="ab3ec-881">personal health</span></span>
- <span data-ttu-id="ab3ec-882">
power of attorney</span><span class="sxs-lookup"><span data-stu-id="ab3ec-882">power of attorney</span></span>
- <span data-ttu-id="ab3ec-883">
registration number</span><span class="sxs-lookup"><span data-stu-id="ab3ec-883">registration number</span></span>
- <span data-ttu-id="ab3ec-884">personal health number</span><span class="sxs-lookup"><span data-stu-id="ab3ec-884">personal health number</span></span>
- <span data-ttu-id="ab3ec-885">
practitioner referral</span><span class="sxs-lookup"><span data-stu-id="ab3ec-885">practitioner referral</span></span>
- <span data-ttu-id="ab3ec-886">
wellness professional</span><span class="sxs-lookup"><span data-stu-id="ab3ec-886">wellness professional</span></span>
- <span data-ttu-id="ab3ec-887">
patient referral</span><span class="sxs-lookup"><span data-stu-id="ab3ec-887">patient referral</span></span>
- <span data-ttu-id="ab3ec-888">

health and wellness</span><span class="sxs-lookup"><span data-stu-id="ab3ec-888">health and wellness</span></span>

#### <a name="keywordcanadaprovinces"></a><span data-ttu-id="ab3ec-889">Keyword_canada_provinces</span><span class="sxs-lookup"><span data-stu-id="ab3ec-889">Keyword_canada_provinces</span></span>

- <span data-ttu-id="ab3ec-890">Nunavut</span><span class="sxs-lookup"><span data-stu-id="ab3ec-890">Nunavut</span></span>
- <span data-ttu-id="ab3ec-891">
Quebec</span><span class="sxs-lookup"><span data-stu-id="ab3ec-891">Quebec</span></span>
- <span data-ttu-id="ab3ec-892">
Northwest Territories</span><span class="sxs-lookup"><span data-stu-id="ab3ec-892">Northwest Territories</span></span>
- <span data-ttu-id="ab3ec-893">
Ontario</span><span class="sxs-lookup"><span data-stu-id="ab3ec-893">Ontario</span></span>
- <span data-ttu-id="ab3ec-894">
British Columbia</span><span class="sxs-lookup"><span data-stu-id="ab3ec-894">British Columbia</span></span>
- <span data-ttu-id="ab3ec-895">
Alberta</span><span class="sxs-lookup"><span data-stu-id="ab3ec-895">Alberta</span></span>
- <span data-ttu-id="ab3ec-896">
Saskatchewan</span><span class="sxs-lookup"><span data-stu-id="ab3ec-896">Saskatchewan</span></span>
- <span data-ttu-id="ab3ec-897">
Manitoba</span><span class="sxs-lookup"><span data-stu-id="ab3ec-897">Manitoba</span></span>
- <span data-ttu-id="ab3ec-898">
Yukon</span><span class="sxs-lookup"><span data-stu-id="ab3ec-898">Yukon</span></span>
- <span data-ttu-id="ab3ec-899">
Newfoundland and Labrador</span><span class="sxs-lookup"><span data-stu-id="ab3ec-899">Newfoundland and Labrador</span></span>
- <span data-ttu-id="ab3ec-900">
New Brunswick</span><span class="sxs-lookup"><span data-stu-id="ab3ec-900">New Brunswick</span></span>
- <span data-ttu-id="ab3ec-901">
Nova Scotia</span><span class="sxs-lookup"><span data-stu-id="ab3ec-901">Nova Scotia</span></span>
- <span data-ttu-id="ab3ec-902">
Prince Edward Island</span><span class="sxs-lookup"><span data-stu-id="ab3ec-902">Prince Edward Island</span></span>
- <span data-ttu-id="ab3ec-903">Canadá</span><span class="sxs-lookup"><span data-stu-id="ab3ec-903">Canada</span></span>
   
## <a name="canada-social-insurance-number"></a><span data-ttu-id="ab3ec-904">Número de seguro social do Canadá</span><span class="sxs-lookup"><span data-stu-id="ab3ec-904">Canada Social Insurance Number</span></span>

### <a name="format"></a><span data-ttu-id="ab3ec-905">Formato</span><span class="sxs-lookup"><span data-stu-id="ab3ec-905">Format</span></span>

<span data-ttu-id="ab3ec-906">Nove dígitos com espaços ou hífens opcionais</span><span class="sxs-lookup"><span data-stu-id="ab3ec-906">Nine digits with optional hyphens or spaces</span></span>

### <a name="pattern"></a><span data-ttu-id="ab3ec-907">Padrão</span><span class="sxs-lookup"><span data-stu-id="ab3ec-907">Pattern</span></span>

<span data-ttu-id="ab3ec-908">Formatado:</span><span class="sxs-lookup"><span data-stu-id="ab3ec-908">Formatted:</span></span>
- <span data-ttu-id="ab3ec-909">Três dígitos</span><span class="sxs-lookup"><span data-stu-id="ab3ec-909">Three digits</span></span> 
- <span data-ttu-id="ab3ec-910">Um hífen ou espaço</span><span class="sxs-lookup"><span data-stu-id="ab3ec-910">A hyphen or space</span></span> 
- <span data-ttu-id="ab3ec-911">Três dígitos</span><span class="sxs-lookup"><span data-stu-id="ab3ec-911">Three digits</span></span> 
- <span data-ttu-id="ab3ec-912">Um hífen ou espaço</span><span class="sxs-lookup"><span data-stu-id="ab3ec-912">A hyphen or space</span></span> 
- <span data-ttu-id="ab3ec-913">Três dígitos</span><span class="sxs-lookup"><span data-stu-id="ab3ec-913">Three digits</span></span>

<span data-ttu-id="ab3ec-914">Formatada: Dígitos de nove</span><span class="sxs-lookup"><span data-stu-id="ab3ec-914">Unformatted: Nine digits</span></span>

### <a name="checksum"></a><span data-ttu-id="ab3ec-915">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="ab3ec-915">Checksum</span></span>

<span data-ttu-id="ab3ec-916">Sim</span><span class="sxs-lookup"><span data-stu-id="ab3ec-916">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="ab3ec-917">Definição</span><span class="sxs-lookup"><span data-stu-id="ab3ec-917">Definition</span></span>

<span data-ttu-id="ab3ec-918">Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="ab3ec-918">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="ab3ec-919">A função Func_canadian_sin localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-919">The function Func_canadian_sin finds content that matches the pattern.</span></span>
- <span data-ttu-id="ab3ec-920">Pelo menos duas de qualquer combinação do seguinte:</span><span class="sxs-lookup"><span data-stu-id="ab3ec-920">At least two of any combination of the following:</span></span>
    - <span data-ttu-id="ab3ec-921">Uma palavra-chave de Keyword_sin for encontrada.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-921">A keyword from Keyword_sin is found.</span></span>
    - <span data-ttu-id="ab3ec-922">Uma palavra-chave de Keyword_sin_collaborative for encontrada.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-922">A keyword from Keyword_sin_collaborative is found.</span></span>
    - <span data-ttu-id="ab3ec-923">A função Func_eu_date encontra uma data no formato de data à direita.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-923">The function Func_eu_date finds a date in the right date format.</span></span>
- <span data-ttu-id="ab3ec-924">A soma de verificação passa.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-924">The checksum passes.</span></span>

<span data-ttu-id="ab3ec-925">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="ab3ec-925">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="ab3ec-926">A função Func_unformatted_canadian_sin localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-926">The function Func_unformatted_canadian_sin finds content that matches the pattern.</span></span>
- <span data-ttu-id="ab3ec-927">Uma palavra-chave de Keyword_sin for encontrada.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-927">A keyword from Keyword_sin is found.</span></span>
- <span data-ttu-id="ab3ec-928">A soma de verificação passa.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-928">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="ab3ec-929">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="ab3ec-929">Keywords</span></span>

#### <a name="keywordsin"></a><span data-ttu-id="ab3ec-930">Keyword_sin</span><span class="sxs-lookup"><span data-stu-id="ab3ec-930">Keyword_sin</span></span>

- <span data-ttu-id="ab3ec-931">sin</span><span class="sxs-lookup"><span data-stu-id="ab3ec-931">sin</span></span> 
- <span data-ttu-id="ab3ec-932">social insurance
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-932">social insurance</span></span> 
- <span data-ttu-id="ab3ec-933">numero d'assurance sociale
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-933">numero d'assurance sociale</span></span> 
- <span data-ttu-id="ab3ec-934">sins
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-934">sins</span></span> 
- <span data-ttu-id="ab3ec-935">SSN</span><span class="sxs-lookup"><span data-stu-id="ab3ec-935">ssn</span></span> 
- <span data-ttu-id="ab3ec-936">números de identificação fiscal</span><span class="sxs-lookup"><span data-stu-id="ab3ec-936">ssns</span></span> 
- <span data-ttu-id="ab3ec-937">seguridade social</span><span class="sxs-lookup"><span data-stu-id="ab3ec-937">social security</span></span> 
- <span data-ttu-id="ab3ec-938">numero d'assurance social
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-938">numero d'assurance social</span></span> 
- <span data-ttu-id="ab3ec-939">número de identificação nacional</span><span class="sxs-lookup"><span data-stu-id="ab3ec-939">national identification number</span></span> 
- <span data-ttu-id="ab3ec-940">
national id</span><span class="sxs-lookup"><span data-stu-id="ab3ec-940">national id</span></span> 
- <span data-ttu-id="ab3ec-941">sin#
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-941">sin#</span></span> 
- <span data-ttu-id="ab3ec-942">soc ins
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-942">soc ins</span></span> 
- <span data-ttu-id="ab3ec-943">social ins
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-943">social ins</span></span> 

#### <a name="keywordsincollaborative"></a><span data-ttu-id="ab3ec-944">Keyword_sin_collaborative</span><span class="sxs-lookup"><span data-stu-id="ab3ec-944">Keyword_sin_collaborative</span></span>

- <span data-ttu-id="ab3ec-945">de motorista carteira</span><span class="sxs-lookup"><span data-stu-id="ab3ec-945">driver's license</span></span> 
- <span data-ttu-id="ab3ec-946">carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="ab3ec-946">drivers license</span></span> 
- <span data-ttu-id="ab3ec-947">licença de motorista</span><span class="sxs-lookup"><span data-stu-id="ab3ec-947">driver's licence</span></span> 
- <span data-ttu-id="ab3ec-948">drivers licence</span><span class="sxs-lookup"><span data-stu-id="ab3ec-948">drivers licence</span></span> 
- <span data-ttu-id="ab3ec-949">DOB
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-949">DOB</span></span> 
- <span data-ttu-id="ab3ec-950">Data de Nascimento</span><span class="sxs-lookup"><span data-stu-id="ab3ec-950">Birthdate</span></span> 
- <span data-ttu-id="ab3ec-951">Aniversário </span><span class="sxs-lookup"><span data-stu-id="ab3ec-951">Birthday</span></span> 
- <span data-ttu-id="ab3ec-952">Date of Birth
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-952">Date of Birth</span></span> 
   
## <a name="chile-identity-card-number"></a><span data-ttu-id="ab3ec-953">	Número do Cartão de Identidade do Chile</span><span class="sxs-lookup"><span data-stu-id="ab3ec-953">Chile Identity Card Number</span></span>

### <a name="format"></a><span data-ttu-id="ab3ec-954">Formato</span><span class="sxs-lookup"><span data-stu-id="ab3ec-954">Format</span></span>

<span data-ttu-id="ab3ec-955">os dígitos plus delimitadores 7 e 8 um dígito de verificação ou uma letra</span><span class="sxs-lookup"><span data-stu-id="ab3ec-955">7-8 digits plus delimiters a check digit or letter</span></span>

### <a name="pattern"></a><span data-ttu-id="ab3ec-956">Padrão</span><span class="sxs-lookup"><span data-stu-id="ab3ec-956">Pattern</span></span>

<span data-ttu-id="ab3ec-957">7 a 8 dígitos mais delimitadores:</span><span class="sxs-lookup"><span data-stu-id="ab3ec-957">7-8 digits plus delimiters:</span></span>
- <span data-ttu-id="ab3ec-958">1 a 2 dígitos</span><span class="sxs-lookup"><span data-stu-id="ab3ec-958">1-2 digits</span></span> 
- <span data-ttu-id="ab3ec-959">Um ponto </span><span class="sxs-lookup"><span data-stu-id="ab3ec-959">A period</span></span> 
- <span data-ttu-id="ab3ec-960">Três dígitos</span><span class="sxs-lookup"><span data-stu-id="ab3ec-960">Three digits</span></span> 
- <span data-ttu-id="ab3ec-961">Um ponto </span><span class="sxs-lookup"><span data-stu-id="ab3ec-961">A period</span></span> 
- <span data-ttu-id="ab3ec-962">Três dígitos</span><span class="sxs-lookup"><span data-stu-id="ab3ec-962">Three digits</span></span> 
- <span data-ttu-id="ab3ec-963">Um traço</span><span class="sxs-lookup"><span data-stu-id="ab3ec-963">A dash</span></span> 
- <span data-ttu-id="ab3ec-964">Um dígito ou letra (não diferencia maiúscula de minúscula) que é um dígito de verificação</span><span class="sxs-lookup"><span data-stu-id="ab3ec-964">One digit or letter (not case sensitive) which is a check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="ab3ec-965">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="ab3ec-965">Checksum</span></span>

<span data-ttu-id="ab3ec-966">Sim</span><span class="sxs-lookup"><span data-stu-id="ab3ec-966">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="ab3ec-967">Definição</span><span class="sxs-lookup"><span data-stu-id="ab3ec-967">Definition</span></span>

<span data-ttu-id="ab3ec-968">Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="ab3ec-968">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="ab3ec-969">A função Func_chile_id_card encontra o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-969">The function Func_chile_id_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="ab3ec-970">Uma palavra-chave de Keyword_chile_id_card é encontrada.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-970">A keyword from Keyword_chile_id_card is found.</span></span>
- <span data-ttu-id="ab3ec-971">A soma de verificação passa.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-971">The checksum passes.</span></span>

<span data-ttu-id="ab3ec-972">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="ab3ec-972">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="ab3ec-973">A função Func_chile_id_card encontra o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-973">The function Func_chile_id_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="ab3ec-974">A soma de verificação passa.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-974">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="ab3ec-975">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="ab3ec-975">Keywords</span></span>

#### <a name="keywordchileidcard"></a><span data-ttu-id="ab3ec-976">Keyword_chile_id_card</span><span class="sxs-lookup"><span data-stu-id="ab3ec-976">Keyword_chile_id_card</span></span>

- <span data-ttu-id="ab3ec-977">Número de Identificação Nacional
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-977">National Identification Number</span></span> 
- <span data-ttu-id="ab3ec-978">Cartão de identidade</span><span class="sxs-lookup"><span data-stu-id="ab3ec-978">Identity card</span></span> 
- <span data-ttu-id="ab3ec-979">ID</span><span class="sxs-lookup"><span data-stu-id="ab3ec-979">ID</span></span> 
- <span data-ttu-id="ab3ec-980">Identificação </span><span class="sxs-lookup"><span data-stu-id="ab3ec-980">Identification</span></span> 
- <span data-ttu-id="ab3ec-981">Rol Único Nacional
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-981">Rol Único Nacional</span></span> 
- <span data-ttu-id="ab3ec-982">EXECUTAR</span><span class="sxs-lookup"><span data-stu-id="ab3ec-982">RUN</span></span> 
- <span data-ttu-id="ab3ec-983">Rol Único Tributario
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-983">Rol Único Tributario</span></span> 
- <span data-ttu-id="ab3ec-984">RUT
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-984">RUT</span></span> 
- <span data-ttu-id="ab3ec-985">Cédula de Identidad
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-985">Cédula de Identidad</span></span> 
- <span data-ttu-id="ab3ec-986">Número De Identificación Nacional
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-986">Número De Identificación Nacional</span></span> 
- <span data-ttu-id="ab3ec-987">Tarjeta de identificación
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-987">Tarjeta de identificación</span></span> 
- <span data-ttu-id="ab3ec-988">Identificación
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-988">Identificación</span></span> 
   
## <a name="china-resident-identity-card-prc-number"></a><span data-ttu-id="ab3ec-989">	Número do Cartão de Identidade de Residentes (PRC) da China</span><span class="sxs-lookup"><span data-stu-id="ab3ec-989">China Resident Identity Card (PRC) Number</span></span>

### <a name="format"></a><span data-ttu-id="ab3ec-990">Formato</span><span class="sxs-lookup"><span data-stu-id="ab3ec-990">Format</span></span>

<span data-ttu-id="ab3ec-991">18 dígitos</span><span class="sxs-lookup"><span data-stu-id="ab3ec-991">18 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="ab3ec-992">Padrão</span><span class="sxs-lookup"><span data-stu-id="ab3ec-992">Pattern</span></span>

<span data-ttu-id="ab3ec-993">18 dígitos:</span><span class="sxs-lookup"><span data-stu-id="ab3ec-993">18 digits:</span></span>
- <span data-ttu-id="ab3ec-994">Seis dígitos que são um código de endereço </span><span class="sxs-lookup"><span data-stu-id="ab3ec-994">Six digits which are an address code</span></span> 
- <span data-ttu-id="ab3ec-995">Oito dígitos no formato AAAAMMDD que são a data de nascimento </span><span class="sxs-lookup"><span data-stu-id="ab3ec-995">Eight digits in the form YYYYMMDD which are the date of birth</span></span> 
- <span data-ttu-id="ab3ec-996">Três dígitos que são um código de pedido </span><span class="sxs-lookup"><span data-stu-id="ab3ec-996">Three digits which are an order code</span></span> 
- <span data-ttu-id="ab3ec-997">Um dígito que é um dígito de verificação</span><span class="sxs-lookup"><span data-stu-id="ab3ec-997">One digit which is a check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="ab3ec-998">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="ab3ec-998">Checksum</span></span>

<span data-ttu-id="ab3ec-999">Sim</span><span class="sxs-lookup"><span data-stu-id="ab3ec-999">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="ab3ec-1000">Definição</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1000">Definition</span></span>

<span data-ttu-id="ab3ec-1001">Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1001">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="ab3ec-1002">A função Func_china_resident_id encontra o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1002">The function Func_china_resident_id finds content that matches the pattern.</span></span>
- <span data-ttu-id="ab3ec-1003">Uma palavra-chave de Keyword_china_resident_id é encontrada.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1003">A keyword from Keyword_china_resident_id is found.</span></span>
- <span data-ttu-id="ab3ec-1004">A soma de verificação passa.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1004">The checksum passes.</span></span>

<span data-ttu-id="ab3ec-1005">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1005">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="ab3ec-1006">A função Func_china_resident_id encontra o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1006">The function Func_china_resident_id finds content that matches the pattern.</span></span>
- <span data-ttu-id="ab3ec-1007">A soma de verificação passa.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1007">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="ab3ec-1008">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1008">Keywords</span></span>

### <a name="keywordchinaresidentid"></a><span data-ttu-id="ab3ec-1009">Keyword_china_resident_id</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1009">Keyword_china_resident_id</span></span>

- <span data-ttu-id="ab3ec-1010">Cartão de Identidade da Polônia
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1010">Resident Identity Card</span></span> 
- <span data-ttu-id="ab3ec-1011">PRC
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1011">PRC</span></span> 
- <span data-ttu-id="ab3ec-1012">Cartão de Identificação Nacional
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1012">National Identification Card</span></span> 
- <span data-ttu-id="ab3ec-1013">身份证 </span><span class="sxs-lookup"><span data-stu-id="ab3ec-1013">身份证</span></span> 
- <span data-ttu-id="ab3ec-1014">居民 身份证 </span><span class="sxs-lookup"><span data-stu-id="ab3ec-1014">居民 身份证</span></span> 
- <span data-ttu-id="ab3ec-1015">居民身份证
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1015">居民身份证</span></span> 
- <span data-ttu-id="ab3ec-1016">鉴定

</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1016">鉴定</span></span> 
- <span data-ttu-id="ab3ec-1017">身分證 </span><span class="sxs-lookup"><span data-stu-id="ab3ec-1017">身分證</span></span> 
- <span data-ttu-id="ab3ec-1018">居民 身份證</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1018">居民 身份證</span></span>
- <span data-ttu-id="ab3ec-1019">鑑定 </span><span class="sxs-lookup"><span data-stu-id="ab3ec-1019">鑑定</span></span> 
   
## <a name="credit-card-number"></a><span data-ttu-id="ab3ec-1020">Credit Card Number</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1020">Credit Card Number</span></span>

### <a name="format"></a><span data-ttu-id="ab3ec-1021">Formato</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1021">Format</span></span>

<span data-ttu-id="ab3ec-1022">16 dígitos que podem ser formatados ou não formatado (dddddddddddddddd) e deve passar o teste de Luhn.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1022">16 digits which can be formatted or unformatted (dddddddddddddddd) and must pass the Luhn test.</span></span>

### <a name="pattern"></a><span data-ttu-id="ab3ec-1023">Padrão</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1023">Pattern</span></span>

<span data-ttu-id="ab3ec-1024">Padrão muito complexo e robusto que detecta cartões de todas as principais marcas em todo o mundo, incluindo Visa, MasterCard, Discover Card, JCB, American Express, vales-presentes e cartões diner.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1024">Very complex and robust pattern that detects cards from all major brands worldwide, including Visa, MasterCard, Discover Card, JCB, American Express, gift cards, and diner cards.</span></span>

### <a name="checksum"></a><span data-ttu-id="ab3ec-1025">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1025">Checksum</span></span>

<span data-ttu-id="ab3ec-1026">Sim, a soma de verificação Luhn</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1026">Yes, the Luhn checksum</span></span>

### <a name="definition"></a><span data-ttu-id="ab3ec-1027">Definição</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1027">Definition</span></span>

<span data-ttu-id="ab3ec-1028">Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1028">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="ab3ec-1029">A função Func_credit_card localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1029">The function Func_credit_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="ab3ec-1030">Uma das seguintes opções for verdadeira:</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1030">One of the following is true:</span></span>
    - <span data-ttu-id="ab3ec-1031">Uma palavra-chave de Keyword_cc_verification for encontrada.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1031">A keyword from Keyword_cc_verification is found.</span></span>
    - <span data-ttu-id="ab3ec-1032">Uma palavra-chave de Keyword_cc_name for encontrada.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1032">A keyword from Keyword_cc_name is found.</span></span>
    - <span data-ttu-id="ab3ec-1033">A função Func_expiration_date encontra uma data no formato de data à direita.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1033">The function Func_expiration_date finds a date in the right date format.</span></span>
- <span data-ttu-id="ab3ec-1034">A soma de verificação passa.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1034">The checksum passes.</span></span>

<span data-ttu-id="ab3ec-1035">Uma política de DLP tem 65% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1035">A DLP policy is 65% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="ab3ec-1036">A função Func_credit_card localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1036">The function Func_credit_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="ab3ec-1037">A soma de verificação passa.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1037">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="ab3ec-1038">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1038">Keywords</span></span>

#### <a name="keywordccverification"></a><span data-ttu-id="ab3ec-1039">Keyword_cc_verification</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1039">Keyword_cc_verification</span></span>

- <span data-ttu-id="ab3ec-1040">card verification</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1040">card verification</span></span>
- <span data-ttu-id="ab3ec-1041">card identification number</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1041">card identification number</span></span>
- <span data-ttu-id="ab3ec-1042">cvn
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1042">cvn</span></span>
- <span data-ttu-id="ab3ec-1043">cid
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1043">cid</span></span>
- <span data-ttu-id="ab3ec-1044">CVC2</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1044">cvc2</span></span>
- <span data-ttu-id="ab3ec-1045">cvv2</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1045">cvv2</span></span>
- <span data-ttu-id="ab3ec-1046">pin block
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1046">pin block</span></span>
- <span data-ttu-id="ab3ec-1047">security code
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1047">security code</span></span>
- <span data-ttu-id="ab3ec-1048">security number
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1048">security number</span></span>
- <span data-ttu-id="ab3ec-1049">security no
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1049">security no</span></span>
- <span data-ttu-id="ab3ec-1050">issue number
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1050">issue number</span></span>
- <span data-ttu-id="ab3ec-1051">issue no
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1051">issue no</span></span>
- <span data-ttu-id="ab3ec-1052">cryptogramme
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1052">cryptogramme</span></span>
- <span data-ttu-id="ab3ec-1053">numéro de sécurité
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1053">numéro de sécurité</span></span>
- <span data-ttu-id="ab3ec-1054">numero de securite
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1054">numero de securite</span></span>
- <span data-ttu-id="ab3ec-1055">kreditkartenprüfnummer
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1055">kreditkartenprüfnummer</span></span>
- <span data-ttu-id="ab3ec-1056">kreditkartenprufnummer
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1056">kreditkartenprufnummer</span></span>
- <span data-ttu-id="ab3ec-1057">prüfziffer
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1057">prüfziffer</span></span>
- <span data-ttu-id="ab3ec-1058">prufziffer
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1058">prufziffer</span></span>
- <span data-ttu-id="ab3ec-1059">sicherheits Kode</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1059">sicherheits Kode</span></span>
- <span data-ttu-id="ab3ec-1060">sicherheitscode
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1060">sicherheitscode</span></span>
- <span data-ttu-id="ab3ec-1061">sicherheitsnummer
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1061">sicherheitsnummer</span></span>
- <span data-ttu-id="ab3ec-1062">verfalldatum
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1062">verfalldatum</span></span>
- <span data-ttu-id="ab3ec-1063">codice di verifica
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1063">codice di verifica</span></span>
- <span data-ttu-id="ab3ec-p105">cod. sicurezza
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-p105">cod. sicurezza</span></span>
- <span data-ttu-id="ab3ec-1066">COD sicurezza</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1066">cod sicurezza</span></span>
- <span data-ttu-id="ab3ec-1067">
n autorizzazione</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1067">n autorizzazione</span></span>
- <span data-ttu-id="ab3ec-1068">código
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1068">código</span></span>
- <span data-ttu-id="ab3ec-1069">codigo
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1069">codigo</span></span>
- <span data-ttu-id="ab3ec-p106">cod. seg
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-p106">cod. seg</span></span>
- <span data-ttu-id="ab3ec-1072">COD seg</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1072">cod seg</span></span>
- <span data-ttu-id="ab3ec-1073">código de segurança
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1073">código de segurança</span></span>
- <span data-ttu-id="ab3ec-1074">codigo de seguranca
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1074">codigo de seguranca</span></span>
- <span data-ttu-id="ab3ec-1075">codigo de segurança
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1075">codigo de segurança</span></span>
- <span data-ttu-id="ab3ec-1076">código de seguranca
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1076">código de seguranca</span></span>
- <span data-ttu-id="ab3ec-p107">cód. segurança
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-p107">cód. segurança</span></span>
- <span data-ttu-id="ab3ec-p108">Cod. segurança cod. segurança</span><span class="sxs-lookup"><span data-stu-id="ab3ec-p108">cod. seguranca cod. segurança</span></span>
- <span data-ttu-id="ab3ec-p109">cód. seguranca
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-p109">cód. seguranca</span></span>
- <span data-ttu-id="ab3ec-1084">segurança Cód</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1084">cód segurança</span></span>
- <span data-ttu-id="ab3ec-1085">bacalhau segurança cod segurança</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1085">cod seguranca cod segurança</span></span>
- <span data-ttu-id="ab3ec-1086">segurança Cód</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1086">cód seguranca</span></span>
- <span data-ttu-id="ab3ec-1087">número de verificação
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1087">número de verificação</span></span>
- <span data-ttu-id="ab3ec-1088">numero de verificacao
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1088">numero de verificacao</span></span>
- <span data-ttu-id="ab3ec-1089">ablauf
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1089">ablauf</span></span>
- <span data-ttu-id="ab3ec-1090">gültig bis
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1090">gültig bis</span></span>
- <span data-ttu-id="ab3ec-1091">gültigkeitsdatum
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1091">gültigkeitsdatum</span></span>
- <span data-ttu-id="ab3ec-1092">gultig bis
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1092">gultig bis</span></span>
- <span data-ttu-id="ab3ec-1093">gultigkeitsdatum
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1093">gultigkeitsdatum</span></span>
- <span data-ttu-id="ab3ec-1094">scadenza
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1094">scadenza</span></span>
- <span data-ttu-id="ab3ec-1095">data scad
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1095">data scad</span></span>
- <span data-ttu-id="ab3ec-1096">fecha de expiracion
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1096">fecha de expiracion</span></span>
- <span data-ttu-id="ab3ec-1097">fecha de venc
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1097">fecha de venc</span></span>
- <span data-ttu-id="ab3ec-1098">vencimiento
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1098">vencimiento</span></span>
- <span data-ttu-id="ab3ec-1099">válido hasta
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1099">válido hasta</span></span>
- <span data-ttu-id="ab3ec-1100">valido hasta
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1100">valido hasta</span></span>
- <span data-ttu-id="ab3ec-1101">vto
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1101">vto</span></span>
- <span data-ttu-id="ab3ec-1102">data de expiração
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1102">data de expiração</span></span>
- <span data-ttu-id="ab3ec-1103">data de expiracao
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1103">data de expiracao</span></span>
- <span data-ttu-id="ab3ec-1104">data em que expira
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1104">data em que expira</span></span>
- <span data-ttu-id="ab3ec-1105">validade
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1105">validade</span></span>
- <span data-ttu-id="ab3ec-1106">valor
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1106">valor</span></span>
- <span data-ttu-id="ab3ec-1107">vencimento
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1107">vencimento</span></span>
- <span data-ttu-id="ab3ec-1108">Venc</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1108">Venc</span></span> 

#### <a name="keywordccname"></a><span data-ttu-id="ab3ec-1109">Keyword_cc_name</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1109">Keyword_cc_name</span></span>

- <span data-ttu-id="ab3ec-1110">amex</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1110">amex</span></span>
- <span data-ttu-id="ab3ec-1111">
american express</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1111">american express</span></span>
- <span data-ttu-id="ab3ec-1112">americanexpress
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1112">americanexpress</span></span>
- <span data-ttu-id="ab3ec-1113">Visa</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1113">Visa</span></span>
- <span data-ttu-id="ab3ec-1114">mastercard
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1114">mastercard</span></span>
- <span data-ttu-id="ab3ec-1115">master card
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1115">master card</span></span>
- <span data-ttu-id="ab3ec-1116">
mc
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1116">mc</span></span> 
- <span data-ttu-id="ab3ec-1117">mastercards</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1117">mastercards</span></span>
- <span data-ttu-id="ab3ec-1118">
master cards</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1118">master cards</span></span>
- <span data-ttu-id="ab3ec-1119">Clube do cliente</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1119">diner's Club</span></span>
- <span data-ttu-id="ab3ec-1120">diners club
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1120">diners club</span></span>
- <span data-ttu-id="ab3ec-1121">dinersclub
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1121">dinersclub</span></span>
- <span data-ttu-id="ab3ec-1122">discover card
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1122">discover card</span></span>
- <span data-ttu-id="ab3ec-1123">discovercard
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1123">discovercard</span></span>
- <span data-ttu-id="ab3ec-1124">discover cards
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1124">discover cards</span></span>
- <span data-ttu-id="ab3ec-1125">JCB</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1125">JCB</span></span>
- <span data-ttu-id="ab3ec-1126">japanese card bureau
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1126">japanese card bureau</span></span>
- <span data-ttu-id="ab3ec-1127">carte blanche
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1127">carte blanche</span></span>
- <span data-ttu-id="ab3ec-1128">carteblanche
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1128">carteblanche</span></span>
- <span data-ttu-id="ab3ec-1129">credit card
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1129">credit card</span></span>
- <span data-ttu-id="ab3ec-1130">Cc #</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1130">cc#</span></span>
- <span data-ttu-id="ab3ec-1131">n º cc:</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1131">cc#:</span></span>
- <span data-ttu-id="ab3ec-1132">
expiration date</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1132">expiration date</span></span>
- <span data-ttu-id="ab3ec-1133">exp date
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1133">exp date</span></span>
- <span data-ttu-id="ab3ec-1134">
expiry date</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1134">expiry date</span></span>
- <span data-ttu-id="ab3ec-1135">
date d’expiration</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1135">date d’expiration</span></span>
- <span data-ttu-id="ab3ec-1136">
date d'exp</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1136">date d'exp</span></span>
- <span data-ttu-id="ab3ec-1137">
date expiration</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1137">date expiration</span></span>
- <span data-ttu-id="ab3ec-1138">bank card
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1138">bank card</span></span>
- <span data-ttu-id="ab3ec-1139">
bankcard</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1139">bankcard</span></span>
- <span data-ttu-id="ab3ec-1140">card number
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1140">card number</span></span>
- <span data-ttu-id="ab3ec-1141">card num
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1141">card num</span></span>
- <span data-ttu-id="ab3ec-1142">cardnumber
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1142">cardnumber</span></span>
- <span data-ttu-id="ab3ec-1143">cardnumbers
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1143">cardnumbers</span></span>
- <span data-ttu-id="ab3ec-1144">card numbers
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1144">card numbers</span></span>
- <span data-ttu-id="ab3ec-1145">creditcard
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1145">creditcard</span></span>
- <span data-ttu-id="ab3ec-1146">credit cards
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1146">credit cards</span></span>
- <span data-ttu-id="ab3ec-1147">creditcards
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1147">creditcards</span></span>
- <span data-ttu-id="ab3ec-1148">ccn
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1148">ccn</span></span>
- <span data-ttu-id="ab3ec-1149">card holder
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1149">card holder</span></span>
- <span data-ttu-id="ab3ec-1150">cardholder
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1150">cardholder</span></span>
- <span data-ttu-id="ab3ec-1151">card holders
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1151">card holders</span></span>
- <span data-ttu-id="ab3ec-1152">cardholders
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1152">cardholders</span></span>
- <span data-ttu-id="ab3ec-1153">check card
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1153">check card</span></span>
- <span data-ttu-id="ab3ec-1154">checkcard
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1154">checkcard</span></span>
- <span data-ttu-id="ab3ec-1155">check cards
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1155">check cards</span></span>
- <span data-ttu-id="ab3ec-1156">checkcards
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1156">checkcards</span></span>
- <span data-ttu-id="ab3ec-1157">debit card
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1157">debit card</span></span>
- <span data-ttu-id="ab3ec-1158">debitcard
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1158">debitcard</span></span>
- <span data-ttu-id="ab3ec-1159">debit cards
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1159">debit cards</span></span>
- <span data-ttu-id="ab3ec-1160">debitcards
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1160">debitcards</span></span>
- <span data-ttu-id="ab3ec-1161">atm card
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1161">atm card</span></span>
- <span data-ttu-id="ab3ec-1162">atmcard
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1162">atmcard</span></span>
- <span data-ttu-id="ab3ec-1163">atm cards
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1163">atm cards</span></span>
- <span data-ttu-id="ab3ec-1164">atmcards
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1164">atmcards</span></span>
- <span data-ttu-id="ab3ec-1165">
enroute</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1165">enroute</span></span>
- <span data-ttu-id="ab3ec-1166">
en route</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1166">en route</span></span>
- <span data-ttu-id="ab3ec-1167">card type
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1167">card type</span></span>
- <span data-ttu-id="ab3ec-1168">carte bancaire
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1168">carte bancaire</span></span>
- <span data-ttu-id="ab3ec-1169">carte de crédit
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1169">carte de crédit</span></span>
- <span data-ttu-id="ab3ec-1170">carte de credit
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1170">carte de credit</span></span>
- <span data-ttu-id="ab3ec-1171">numéro de carte
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1171">numéro de carte</span></span>
- <span data-ttu-id="ab3ec-1172">numero de carte
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1172">numero de carte</span></span>
- <span data-ttu-id="ab3ec-1173">nº de la carte
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1173">nº de la carte</span></span>
- <span data-ttu-id="ab3ec-1174">nº de carte
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1174">nº de carte</span></span>
- <span data-ttu-id="ab3ec-1175">kreditkarte
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1175">kreditkarte</span></span>
- <span data-ttu-id="ab3ec-1176">karte
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1176">karte</span></span>
- <span data-ttu-id="ab3ec-1177">karteninhaber
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1177">karteninhaber</span></span>
- <span data-ttu-id="ab3ec-1178">karteninhabers</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1178">karteninhabers</span></span>
- <span data-ttu-id="ab3ec-1179">kreditkarteninhaber
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1179">kreditkarteninhaber</span></span>
- <span data-ttu-id="ab3ec-1180">kreditkarteninstitut
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1180">kreditkarteninstitut</span></span>
- <span data-ttu-id="ab3ec-1181">kreditkartentyp
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1181">kreditkartentyp</span></span>
- <span data-ttu-id="ab3ec-1182">eigentümername
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1182">eigentümername</span></span>
- <span data-ttu-id="ab3ec-1183">
kartennr
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1183">kartennr</span></span> 
- <span data-ttu-id="ab3ec-1184">kartennummer</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1184">kartennummer</span></span>
- <span data-ttu-id="ab3ec-1185">
kreditkartennummer</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1185">kreditkartennummer</span></span>
- <span data-ttu-id="ab3ec-1186">kreditkarten-nummer</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1186">kreditkarten-nummer</span></span>
- <span data-ttu-id="ab3ec-1187">carta di credito
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1187">carta di credito</span></span>
- <span data-ttu-id="ab3ec-1188">carta credito
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1188">carta credito</span></span>
- <span data-ttu-id="ab3ec-1189">carta</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1189">carta</span></span>
- <span data-ttu-id="ab3ec-1190">carta n</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1190">n carta</span></span>
- <span data-ttu-id="ab3ec-p110">nr. carta
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-p110">nr. carta</span></span>
- <span data-ttu-id="ab3ec-1193">carta nr</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1193">nr carta</span></span>
- <span data-ttu-id="ab3ec-1194">numero carta
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1194">numero carta</span></span>
- <span data-ttu-id="ab3ec-1195">numero della carta
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1195">numero della carta</span></span>
- <span data-ttu-id="ab3ec-1196">numero di carta
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1196">numero di carta</span></span>
- <span data-ttu-id="ab3ec-1197">tarjeta credito
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1197">tarjeta credito</span></span>
- <span data-ttu-id="ab3ec-1198">tarjeta de credito
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1198">tarjeta de credito</span></span>
- <span data-ttu-id="ab3ec-1199">
tarjeta crédito</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1199">tarjeta crédito</span></span>
- <span data-ttu-id="ab3ec-1200">
tarjeta de crédito</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1200">tarjeta de crédito</span></span>
- <span data-ttu-id="ab3ec-1201">tarjeta de atm
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1201">tarjeta de atm</span></span>
- <span data-ttu-id="ab3ec-1202">tarjeta atm
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1202">tarjeta atm</span></span>
- <span data-ttu-id="ab3ec-1203">tarjeta debito
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1203">tarjeta debito</span></span>
- <span data-ttu-id="ab3ec-1204">tarjeta de debito
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1204">tarjeta de debito</span></span>
- <span data-ttu-id="ab3ec-1205">
tarjeta débito</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1205">tarjeta débito</span></span>
- <span data-ttu-id="ab3ec-1206">
tarjeta de débito</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1206">tarjeta de débito</span></span>
- <span data-ttu-id="ab3ec-1207">nº de tarjeta
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1207">nº de tarjeta</span></span>
- <span data-ttu-id="ab3ec-p111">no. de tarjeta
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-p111">no. de tarjeta</span></span>
- <span data-ttu-id="ab3ec-1210">Nenhum tarjeta de</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1210">no de tarjeta</span></span>
- <span data-ttu-id="ab3ec-1211">numero de tarjeta
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1211">numero de tarjeta</span></span>
- <span data-ttu-id="ab3ec-1212">número de tarjeta
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1212">número de tarjeta</span></span>
- <span data-ttu-id="ab3ec-1213">tarjeta no
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1213">tarjeta no</span></span>
- <span data-ttu-id="ab3ec-1214">tarjetahabiente
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1214">tarjetahabiente</span></span>
- <span data-ttu-id="ab3ec-1215">cartão de crédito
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1215">cartão de crédito</span></span>
- <span data-ttu-id="ab3ec-1216">cartão de credito
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1216">cartão de credito</span></span>
- <span data-ttu-id="ab3ec-1217">cartao de crédito
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1217">cartao de crédito</span></span>
- <span data-ttu-id="ab3ec-1218">cartao de credito
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1218">cartao de credito</span></span>
- <span data-ttu-id="ab3ec-1219">cartão de débito
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1219">cartão de débito</span></span>
- <span data-ttu-id="ab3ec-1220">cartao de débito
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1220">cartao de débito</span></span>
- <span data-ttu-id="ab3ec-1221">cartão de debito
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1221">cartão de debito</span></span>
- <span data-ttu-id="ab3ec-1222">cartao de debito
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1222">cartao de debito</span></span>
- <span data-ttu-id="ab3ec-1223">débito automático</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1223">débito automático</span></span>
- <span data-ttu-id="ab3ec-1224">debito automatico
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1224">debito automatico</span></span>
- <span data-ttu-id="ab3ec-1225">
número do cartão</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1225">número do cartão</span></span>
- <span data-ttu-id="ab3ec-1226">
numero do cartão
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1226">numero do cartão</span></span> 
- <span data-ttu-id="ab3ec-1227">número do cartao</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1227">número do cartao</span></span>
- <span data-ttu-id="ab3ec-1228">
numero do cartao</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1228">numero do cartao</span></span>
- <span data-ttu-id="ab3ec-1229">número de cartão
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1229">número de cartão</span></span>
- <span data-ttu-id="ab3ec-1230">numero de cartão
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1230">numero de cartão</span></span>
- <span data-ttu-id="ab3ec-1231">número de cartao
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1231">número de cartao</span></span>
- <span data-ttu-id="ab3ec-1232">numero de cartao
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1232">numero de cartao</span></span>
- <span data-ttu-id="ab3ec-1233">n º cartão</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1233">nº do cartão</span></span>
- <span data-ttu-id="ab3ec-1234">nº do cartao
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1234">nº do cartao</span></span>
- <span data-ttu-id="ab3ec-p112">nº. do cartão
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-p112">nº. do cartão</span></span>
- <span data-ttu-id="ab3ec-1237">Nenhum cartão execute</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1237">no do cartão</span></span>
- <span data-ttu-id="ab3ec-1238">Nenhum cartao execute</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1238">no do cartao</span></span>
- <span data-ttu-id="ab3ec-p113">no. do cartão
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-p113">no. do cartão</span></span>
- <span data-ttu-id="ab3ec-p114">
no. do cartao
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-p114">no. do cartao</span></span> 
   
## <a name="croatia-identity-card-number"></a><span data-ttu-id="ab3ec-1243">	Número do Cartão de Identidade da Croácia</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1243">Croatia Identity Card Number</span></span>

### <a name="format"></a><span data-ttu-id="ab3ec-1244">Formato</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1244">Format</span></span>

<span data-ttu-id="ab3ec-1245">Nove dígitos</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1245">Nine digits</span></span>

### <a name="pattern"></a><span data-ttu-id="ab3ec-1246">Padrão</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1246">Pattern</span></span>

<span data-ttu-id="ab3ec-1247">Nove dígitos consecutivos</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1247">Nine consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="ab3ec-1248">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1248">Checksum</span></span>

<span data-ttu-id="ab3ec-1249">Não</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1249">No</span></span>

### <a name="definition"></a><span data-ttu-id="ab3ec-1250">Definição</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1250">Definition</span></span>

<span data-ttu-id="ab3ec-1251">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1251">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="ab3ec-1252">A função Func_croatia_id_card encontra o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1252">The function Func_croatia_id_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="ab3ec-1253">Uma palavra-chave de Keyword_croatia_id_card é encontrada.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1253">A keyword from Keyword_croatia_id_card is found.</span></span>

```
<!--Croatia Identity Card Number-->
<Entity id="ff12f884-c20a-4189-b185-34c8e7258d47" recommendedConfidence="75" patternsProximity="300">
  <Pattern confidenceLevel="75">
     <IdMatch idRef="Func_croatia_id_card"/>
     <Match idRef="Keyword_croatia_id_card"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="ab3ec-1254">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1254">Keywords</span></span>

#### <a name="keywordcroatiaidcard"></a><span data-ttu-id="ab3ec-1255">Keyword_croatia_id_card</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1255">Keyword_croatia_id_card</span></span>

- <span data-ttu-id="ab3ec-1256">Cartão de identidade croata</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1256">Croatian identity card</span></span>
- <span data-ttu-id="ab3ec-1257">Osobna iskaznica</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1257">Osobna iskaznica</span></span>

   
## <a name="croatia-personal-identification-oib-number"></a><span data-ttu-id="ab3ec-1258">	Número de Identificação Pessoal (OIB) da Croácia</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1258">Croatia Personal Identification (OIB) Number</span></span>

### <a name="format"></a><span data-ttu-id="ab3ec-1259">Formato</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1259">Format</span></span>

<span data-ttu-id="ab3ec-1260">10 dígitos</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1260">10 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="ab3ec-1261">Padrão</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1261">Pattern</span></span>

<span data-ttu-id="ab3ec-1262">10 dígitos:</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1262">10 digits:</span></span>
- <span data-ttu-id="ab3ec-1263">Seis dígitos no formato DDMMAA que são a data de nascimento</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1263">Six digits in the form DDMMYY which are the date of birth</span></span> 
- <span data-ttu-id="ab3ec-1264">Quatro dígitos em que o último é um dígito de verificação</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1264">Four digits where the final digit is a check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="ab3ec-1265">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1265">Checksum</span></span>

<span data-ttu-id="ab3ec-1266">Sim</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1266">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="ab3ec-1267">Definição</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1267">Definition</span></span>

<span data-ttu-id="ab3ec-1268">Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1268">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="ab3ec-1269">A função Func_croatia_oib_number encontra o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1269">The function Func_croatia_oib_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="ab3ec-1270">Uma palavra-chave de Keyword_croatia_oib_number é encontrada.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1270">A keyword from Keyword_croatia_oib_number is found.</span></span>
- <span data-ttu-id="ab3ec-1271">A soma de verificação passa.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1271">The checksum passes.</span></span>

<span data-ttu-id="ab3ec-1272">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1272">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="ab3ec-1273">A função Func_croatia_oib_number encontra o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1273">The function Func_croatia_oib_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="ab3ec-1274">A soma de verificação passa.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1274">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="ab3ec-1275">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1275">Keywords</span></span>

#### <a name="keywordcroatiaoibnumber"></a><span data-ttu-id="ab3ec-1276">Keyword_croatia_oib_number</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1276">Keyword_croatia_oib_number</span></span>

- <span data-ttu-id="ab3ec-1277">Número de Identificação Pessoal</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1277">Personal Identification Number</span></span>
- <span data-ttu-id="ab3ec-1278">Osobni identifikacijski broj
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1278">Osobni identifikacijski broj</span></span> 
- <span data-ttu-id="ab3ec-1279">OIB
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1279">OIB</span></span> 

   
## <a name="czech-national-identity-card-number"></a><span data-ttu-id="ab3ec-1280">	Número do Cartão de Identidade Nacional Tcheco</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1280">Czech National Identity Card Number</span></span>

### <a name="format"></a><span data-ttu-id="ab3ec-1281">Formato</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1281">Format</span></span>

<span data-ttu-id="ab3ec-1282">10 dígitos que contém uma barra</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1282">10 digits containing a forward slash</span></span>

### <a name="pattern"></a><span data-ttu-id="ab3ec-1283">Padrão</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1283">Pattern</span></span>

<span data-ttu-id="ab3ec-1284">10 dígitos:</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1284">10 digits:</span></span>
- <span data-ttu-id="ab3ec-1285">Seis dígitos que são a data de nascimento</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1285">Six digits which are the date of birth</span></span> 
- <span data-ttu-id="ab3ec-1286">Uma barra</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1286">A forward slash</span></span> 
- <span data-ttu-id="ab3ec-1287">Quatro dígitos em que o último é um dígito de verificação</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1287">Four digits where the final digit is a check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="ab3ec-1288">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1288">Checksum</span></span>

<span data-ttu-id="ab3ec-1289">Sim</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1289">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="ab3ec-1290">Definição</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1290">Definition</span></span>

<span data-ttu-id="ab3ec-p115">Uma política DLP é de 85% confiante de que detectou esse tipo de informações confidenciais if, dentro de uma proximidade de 300 caracteres: A função Func_czech_id_card encontra o conteúdo que corresponde ao padrão. Uma palavra-chave de Keyword_czech_id_card é encontrada. A soma de verificação passa.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-p115">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters: The function Func_czech_id_card finds content that matches the pattern. A keyword from Keyword_czech_id_card is found. The checksum passes.</span></span>

```
<!-- Czech National Identity Card Number -->
<Entity id="60c0725a-4eb6-455b-9dda-05d8a7396497" recommendedConfidence="85" patternsProximity="300">
  <Pattern confidenceLevel="85">
     <IdMatch idRef="Func_czech_id_card"/>
     <Match idRef="Keyword_czech_id_card"/>
  </Pattern>
</Entity>
```


### <a name="keywords"></a><span data-ttu-id="ab3ec-1294">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1294">Keywords</span></span>

- <span data-ttu-id="ab3ec-1295">Keyword_czech_id_card</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1295">Keyword_czech_id_card</span></span>
- <span data-ttu-id="ab3ec-1296">Número do cartão de identidade nacional tcheco</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1296">Czech national identity card</span></span>
- <span data-ttu-id="ab3ec-1297">Občanský průka</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1297">Občanský průka</span></span>
   
## <a name="denmark-personal-identification-number"></a><span data-ttu-id="ab3ec-1298">	Número de Identificação Pessoal da Dinamarca</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1298">Denmark Personal Identification Number</span></span>

### <a name="format"></a><span data-ttu-id="ab3ec-1299">Formato</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1299">Format</span></span>

<span data-ttu-id="ab3ec-1300">10 dígitos que contêm um hífen</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1300">10 digits containing a hyphen</span></span>

### <a name="pattern"></a><span data-ttu-id="ab3ec-1301">Padrão</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1301">Pattern</span></span>

<span data-ttu-id="ab3ec-1302">10 dígitos:</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1302">10 digits:</span></span>
- <span data-ttu-id="ab3ec-1303">Seis dígitos no formato DDMMAA que são a data de nascimento</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1303">Six digits in the format DDMMYY which are the date of birth</span></span> 
- <span data-ttu-id="ab3ec-1304">Um hífen</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1304">A hyphen</span></span> 
- <span data-ttu-id="ab3ec-1305">Quatro dígitos em que o último é um dígito de verificação</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1305">Four digits where the final digit is a check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="ab3ec-1306">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1306">Checksum</span></span>

<span data-ttu-id="ab3ec-1307">Sim</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1307">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="ab3ec-1308">Definição</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1308">Definition</span></span>

<span data-ttu-id="ab3ec-p116">Uma política de DLP é 75% confiante de que detectou esse tipo de informações confidenciais if, dentro de uma proximidade de 300 caracteres: A expressão regular Regex_denmark_id encontra o conteúdo que corresponde ao padrão. Uma palavra-chave de Keyword_denmark_id é encontrada. A soma de verificação passa.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-p116">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters: The regular expression Regex_denmark_id finds content that matches the pattern. A keyword from Keyword_denmark_id is found. The checksum passes.</span></span>

```
<!-- Denmark Personal Identification Number -->
<Entity id="6c4f2fef-56e1-4c00-8093-88d7a01cf460" recommendedConfidence="75" patternsProximity="300">
  <Pattern confidenceLevel="75">
     <IdMatch idRef="Regex_denmark_id"/>
     <Match idRef="Keyword_denmark_id"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="ab3ec-1312">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1312">Keywords</span></span>

#### <a name="keyworddenmarkid"></a><span data-ttu-id="ab3ec-1313">Keyword_denmark_id</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1313">Keyword_denmark_id</span></span>

- <span data-ttu-id="ab3ec-1314">Número de Identificação Pessoal</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1314">Personal Identification Number</span></span>
- <span data-ttu-id="ab3ec-1315">CPR</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1315">CPR</span></span>
- <span data-ttu-id="ab3ec-1316">Det Centrale Personregister</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1316">Det Centrale Personregister</span></span>
- <span data-ttu-id="ab3ec-1317">Personnummer</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1317">Personnummer</span></span>
   
## <a name="drug-enforcement-agency-dea-number"></a><span data-ttu-id="ab3ec-1318">Número da Drug Enforcement Agency (DEA)</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1318">Drug Enforcement Agency (DEA) Number</span></span>

### <a name="format"></a><span data-ttu-id="ab3ec-1319">Formato</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1319">Format</span></span>

<span data-ttu-id="ab3ec-1320">Duas letras seguidas por sete dígitos</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1320">Two letters followed by seven digits</span></span>

### <a name="pattern"></a><span data-ttu-id="ab3ec-1321">Padrão</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1321">Pattern</span></span>

<span data-ttu-id="ab3ec-1322">O padrão deve incluir todos os seguintes itens:</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1322">Pattern must include all of the following:</span></span>
- <span data-ttu-id="ab3ec-1323">Uma letra (não diferencia maiúscula de minúscula) deste conjunto de letras possíveis: abcdefghjklmnprstux, que é um código de inscrito</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1323">One letter (not case sensitive) from this set of possible letters: abcdefghjklmnprstux, which is a registrant code</span></span> 
- <span data-ttu-id="ab3ec-1324">Uma letra (não diferencia maiúscula de minúscula), que é a primeira letra do sobrenome do inscrito</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1324">One letter (not case sensitive), which is the first letter of the registrant's last name</span></span> 
- <span data-ttu-id="ab3ec-1325">Sete dígitos, dos quais o último é o dígito de verificação</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1325">Seven digits, the last of which is the check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="ab3ec-1326">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1326">Checksum</span></span>

<span data-ttu-id="ab3ec-1327">Sim</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1327">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="ab3ec-1328">Definição</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1328">Definition</span></span>

<span data-ttu-id="ab3ec-1329">Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1329">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="ab3ec-1330">A função Func_dea_number localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1330">The function Func_dea_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="ab3ec-1331">A soma de verificação passa.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1331">The checksum passes.</span></span>

```
<!-- DEA Number -->
<Entity id="9a5445ad-406e-43eb-8bd7-cac17ab6d0e4" recommendedConfidence="85" patternsProximity="300">
  <Pattern confidenceLevel="85">
     <IdMatch idRef="Func_dea_number"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="ab3ec-1332">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1332">Keywords</span></span>

<span data-ttu-id="ab3ec-1333">Nenhum</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1333">None</span></span>

   
## <a name="eu-debit-card-number"></a><span data-ttu-id="ab3ec-1334">Número de cartão de débito da UE</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1334">EU Debit Card Number</span></span>

### <a name="format"></a><span data-ttu-id="ab3ec-1335">Formato</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1335">Format</span></span>

<span data-ttu-id="ab3ec-1336">16 dígitos</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1336">16 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="ab3ec-1337">Padrão</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1337">Pattern</span></span>

<span data-ttu-id="ab3ec-1338">Padrão muito complexo e robusto</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1338">Very complex and robust pattern</span></span>

### <a name="checksum"></a><span data-ttu-id="ab3ec-1339">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1339">Checksum</span></span>

<span data-ttu-id="ab3ec-1340">Sim</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1340">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="ab3ec-1341">Definição</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1341">Definition</span></span>

<span data-ttu-id="ab3ec-1342">Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1342">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="ab3ec-1343">A função Func_eu_debit_card localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1343">The function Func_eu_debit_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="ab3ec-1344">Pelo menos uma das seguintes opções for verdadeira:</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1344">At least one of the following is true:</span></span>
    - <span data-ttu-id="ab3ec-1345">Uma palavra-chave de Keyword_eu_debit_card for encontrada.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1345">A keyword from Keyword_eu_debit_card is found.</span></span>
    - <span data-ttu-id="ab3ec-1346">Uma palavra-chave de Keyword_card_terms_dict for encontrada.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1346">A keyword from Keyword_card_terms_dict is found.</span></span>
    - <span data-ttu-id="ab3ec-1347">Uma palavra-chave de Keyword_card_security_terms_dict for encontrada.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1347">A keyword from Keyword_card_security_terms_dict is found.</span></span>
    - <span data-ttu-id="ab3ec-1348">Uma palavra-chave de Keyword_card_expiration_terms_dict for encontrada.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1348">A keyword from Keyword_card_expiration_terms_dict is found.</span></span>
    - <span data-ttu-id="ab3ec-1349">A função Func_expiration_date encontra uma data no formato de data à direita.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1349">The function Func_expiration_date finds a date in the right date format.</span></span>
- <span data-ttu-id="ab3ec-1350">A soma de verificação passa.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1350">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="ab3ec-1351">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1351">Keywords</span></span>

#### <a name="keywordeudebitcard"></a><span data-ttu-id="ab3ec-1352">Keyword_eu_debit_card</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1352">Keyword_eu_debit_card</span></span>

- <span data-ttu-id="ab3ec-1353">número de conta</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1353">account number</span></span> 
- <span data-ttu-id="ab3ec-1354">card number
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1354">card number</span></span> 
- <span data-ttu-id="ab3ec-1355">card no.
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1355">card no.</span></span> 
- <span data-ttu-id="ab3ec-1356">security number
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1356">security number</span></span> 
- <span data-ttu-id="ab3ec-1357">Cc #</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1357">cc#</span></span> 

#### <a name="keywordcardtermsdict"></a><span data-ttu-id="ab3ec-1358">Keyword_card_terms_dict</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1358">Keyword_card_terms_dict</span></span>

- <span data-ttu-id="ab3ec-1359">acct nbr
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1359">acct nbr</span></span> 
- <span data-ttu-id="ab3ec-1360">acct num
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1360">acct num</span></span> 
- <span data-ttu-id="ab3ec-1361">acct no
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1361">acct no</span></span> 
- <span data-ttu-id="ab3ec-1362">american express
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1362">american express</span></span> 
- <span data-ttu-id="ab3ec-1363">americanexpress
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1363">americanexpress</span></span> 
- <span data-ttu-id="ab3ec-1364">americano espresso
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1364">americano espresso</span></span> 
- <span data-ttu-id="ab3ec-1365">amex</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1365">amex</span></span> 
- <span data-ttu-id="ab3ec-1366">atm card
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1366">atm card</span></span> 
- <span data-ttu-id="ab3ec-1367">atm cards
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1367">atm cards</span></span> 
- <span data-ttu-id="ab3ec-1368">atm kaart
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1368">atm kaart</span></span> 
- <span data-ttu-id="ab3ec-1369">atmcard
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1369">atmcard</span></span> 
- <span data-ttu-id="ab3ec-1370">atmcards
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1370">atmcards</span></span> 
- <span data-ttu-id="ab3ec-1371">atmkaart
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1371">atmkaart</span></span> 
- <span data-ttu-id="ab3ec-1372">atmkaarten
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1372">atmkaarten</span></span> 
- <span data-ttu-id="ab3ec-1373">bancontact
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1373">bancontact</span></span> 
- <span data-ttu-id="ab3ec-1374">bank card
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1374">bank card</span></span> 
- <span data-ttu-id="ab3ec-1375">bankkaart
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1375">bankkaart</span></span> 
- <span data-ttu-id="ab3ec-1376">card holder
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1376">card holder</span></span> 
- <span data-ttu-id="ab3ec-1377">card holders
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1377">card holders</span></span> 
- <span data-ttu-id="ab3ec-1378">card num
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1378">card num</span></span> 
- <span data-ttu-id="ab3ec-1379">card number
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1379">card number</span></span> 
- <span data-ttu-id="ab3ec-1380">card numbers
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1380">card numbers</span></span> 
- <span data-ttu-id="ab3ec-1381">card type
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1381">card type</span></span> 
- <span data-ttu-id="ab3ec-1382">cardano numerico
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1382">cardano numerico</span></span> 
- <span data-ttu-id="ab3ec-1383">cardholder
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1383">cardholder</span></span> 
- <span data-ttu-id="ab3ec-1384">cardholders
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1384">cardholders</span></span> 
- <span data-ttu-id="ab3ec-1385">cardnumber
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1385">cardnumber</span></span> 
- <span data-ttu-id="ab3ec-1386">cardnumbers
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1386">cardnumbers</span></span> 
- <span data-ttu-id="ab3ec-1387">carta bianca
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1387">carta bianca</span></span> 
- <span data-ttu-id="ab3ec-1388">carta credito
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1388">carta credito</span></span> 
- <span data-ttu-id="ab3ec-1389">carta di credito
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1389">carta di credito</span></span> 
- <span data-ttu-id="ab3ec-1390">cartao de credito
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1390">cartao de credito</span></span> 
- <span data-ttu-id="ab3ec-1391">cartao de crédito
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1391">cartao de crédito</span></span> 
- <span data-ttu-id="ab3ec-1392">cartao de debito
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1392">cartao de debito</span></span> 
- <span data-ttu-id="ab3ec-1393">cartao de débito
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1393">cartao de débito</span></span> 
- <span data-ttu-id="ab3ec-1394">carte bancaire
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1394">carte bancaire</span></span> 
- <span data-ttu-id="ab3ec-1395">carte blanche
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1395">carte blanche</span></span> 
- <span data-ttu-id="ab3ec-1396">carte bleue
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1396">carte bleue</span></span> 
- <span data-ttu-id="ab3ec-1397">carte de credit
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1397">carte de credit</span></span> 
- <span data-ttu-id="ab3ec-1398">carte de crédit
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1398">carte de crédit</span></span> 
- <span data-ttu-id="ab3ec-1399">carte di credito
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1399">carte di credito</span></span> 
- <span data-ttu-id="ab3ec-1400">carteblanche
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1400">carteblanche</span></span> 
- <span data-ttu-id="ab3ec-1401">cartão de credito
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1401">cartão de credito</span></span> 
- <span data-ttu-id="ab3ec-1402">cartão de crédito
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1402">cartão de crédito</span></span> 
- <span data-ttu-id="ab3ec-1403">cartão de debito
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1403">cartão de debito</span></span> 
- <span data-ttu-id="ab3ec-1404">cartão de débito
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1404">cartão de débito</span></span> 
- <span data-ttu-id="ab3ec-1405">cb
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1405">cb</span></span> 
- <span data-ttu-id="ab3ec-1406">ccn
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1406">ccn</span></span> 
- <span data-ttu-id="ab3ec-1407">check card
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1407">check card</span></span> 
- <span data-ttu-id="ab3ec-1408">check cards
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1408">check cards</span></span> 
- <span data-ttu-id="ab3ec-1409">checkcard
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1409">checkcard</span></span>
- <span data-ttu-id="ab3ec-1410">checkcards
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1410">checkcards</span></span> 
- <span data-ttu-id="ab3ec-1411">chequekaart
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1411">chequekaart</span></span> 
- <span data-ttu-id="ab3ec-1412">cirrus
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1412">cirrus</span></span> 
- <span data-ttu-id="ab3ec-1413">cirrus-edc-maestro
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1413">cirrus-edc-maestro</span></span> 
- <span data-ttu-id="ab3ec-1414">controlekaart
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1414">controlekaart</span></span> 
- <span data-ttu-id="ab3ec-1415">controlekaarten
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1415">controlekaarten</span></span> 
- <span data-ttu-id="ab3ec-1416">credit card
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1416">credit card</span></span> 
- <span data-ttu-id="ab3ec-1417">credit cards
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1417">credit cards</span></span> 
- <span data-ttu-id="ab3ec-1418">creditcard
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1418">creditcard</span></span> 
- <span data-ttu-id="ab3ec-1419">creditcards
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1419">creditcards</span></span> 
- <span data-ttu-id="ab3ec-1420">debetkaart
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1420">debetkaart</span></span> 
- <span data-ttu-id="ab3ec-1421">debetkaarten
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1421">debetkaarten</span></span> 
- <span data-ttu-id="ab3ec-1422">debit card
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1422">debit card</span></span> 
- <span data-ttu-id="ab3ec-1423">debit cards
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1423">debit cards</span></span> 
- <span data-ttu-id="ab3ec-1424">debitcard
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1424">debitcard</span></span> 
- <span data-ttu-id="ab3ec-1425">debitcards
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1425">debitcards</span></span> 
- <span data-ttu-id="ab3ec-1426">debito automatico
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1426">debito automatico</span></span> 
- <span data-ttu-id="ab3ec-1427">diners club
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1427">diners club</span></span> 
- <span data-ttu-id="ab3ec-1428">dinersclub
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1428">dinersclub</span></span> 
- <span data-ttu-id="ab3ec-1429">descobrir</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1429">discover</span></span> 
- <span data-ttu-id="ab3ec-1430">discover card
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1430">discover card</span></span> 
- <span data-ttu-id="ab3ec-1431">discover cards
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1431">discover cards</span></span> 
- <span data-ttu-id="ab3ec-1432">discovercard
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1432">discovercard</span></span> 
- <span data-ttu-id="ab3ec-1433">discovercards
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1433">discovercards</span></span> 
- <span data-ttu-id="ab3ec-1434">débito automático</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1434">débito automático</span></span>
- <span data-ttu-id="ab3ec-1435">
edc
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1435">edc</span></span> 
- <span data-ttu-id="ab3ec-1436">eigentümername
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1436">eigentümername</span></span> 
- <span data-ttu-id="ab3ec-1437">european debit card
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1437">european debit card</span></span> 
- <span data-ttu-id="ab3ec-1438">hoofdkaart
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1438">hoofdkaart</span></span> 
- <span data-ttu-id="ab3ec-1439">hoofdkaarten
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1439">hoofdkaarten</span></span> 
- <span data-ttu-id="ab3ec-1440">in viaggio
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1440">in viaggio</span></span> 
- <span data-ttu-id="ab3ec-1441">japanese card bureau
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1441">japanese card bureau</span></span> 
- <span data-ttu-id="ab3ec-1442">japanse kaartdienst
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1442">japanse kaartdienst</span></span> 
- <span data-ttu-id="ab3ec-1443">jcb
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1443">jcb</span></span> 
- <span data-ttu-id="ab3ec-1444">kaart
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1444">kaart</span></span> 
- <span data-ttu-id="ab3ec-1445">kaart num
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1445">kaart num</span></span> 
- <span data-ttu-id="ab3ec-1446">kaartaantal
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1446">kaartaantal</span></span> 
- <span data-ttu-id="ab3ec-1447">kaartaantallen
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1447">kaartaantallen</span></span> 
- <span data-ttu-id="ab3ec-1448">kaarthouder
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1448">kaarthouder</span></span> 
- <span data-ttu-id="ab3ec-1449">kaarthouders
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1449">kaarthouders</span></span> 
- <span data-ttu-id="ab3ec-1450">karte
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1450">karte</span></span>  
- <span data-ttu-id="ab3ec-1451">karteninhaber
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1451">karteninhaber</span></span> 
- <span data-ttu-id="ab3ec-1452">karteninhabers</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1452">karteninhabers</span></span>
- <span data-ttu-id="ab3ec-1453">
kartennr
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1453">kartennr</span></span> 
- <span data-ttu-id="ab3ec-1454">kartennummer</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1454">kartennummer</span></span> 
- <span data-ttu-id="ab3ec-1455">kreditkarte
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1455">kreditkarte</span></span> 
- <span data-ttu-id="ab3ec-1456">kreditkarten-nummer</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1456">kreditkarten-nummer</span></span> 
- <span data-ttu-id="ab3ec-1457">kreditkarteninhaber
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1457">kreditkarteninhaber</span></span> 
- <span data-ttu-id="ab3ec-1458">kreditkarteninstitut
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1458">kreditkarteninstitut</span></span> 
- <span data-ttu-id="ab3ec-1459">kreditkartennummer
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1459">kreditkartennummer</span></span> 
- <span data-ttu-id="ab3ec-1460">kreditkartentyp
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1460">kreditkartentyp</span></span> 
- <span data-ttu-id="ab3ec-1461">maestro
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1461">maestro</span></span> 
- <span data-ttu-id="ab3ec-1462">master card
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1462">master card</span></span> 
- <span data-ttu-id="ab3ec-1463">master cards
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1463">master cards</span></span> 
- <span data-ttu-id="ab3ec-1464">mastercard
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1464">mastercard</span></span> 
- <span data-ttu-id="ab3ec-1465">mastercards</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1465">mastercards</span></span> 
- <span data-ttu-id="ab3ec-1466">MC</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1466">mc</span></span> 
- <span data-ttu-id="ab3ec-1467">mister cash
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1467">mister cash</span></span> 
- <span data-ttu-id="ab3ec-1468">carta n</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1468">n carta</span></span> 
- <span data-ttu-id="ab3ec-1469">carta</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1469">carta</span></span> 
- <span data-ttu-id="ab3ec-1470">Nenhum tarjeta de</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1470">no de tarjeta</span></span> 
- <span data-ttu-id="ab3ec-1471">Nenhum cartao execute</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1471">no do cartao</span></span> 
- <span data-ttu-id="ab3ec-1472">Nenhum cartão execute</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1472">no do cartão</span></span> 
- <span data-ttu-id="ab3ec-p117">no. de tarjeta
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-p117">no. de tarjeta</span></span> 
- <span data-ttu-id="ab3ec-p118">no. do cartao
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-p118">no. do cartao</span></span> 
- <span data-ttu-id="ab3ec-p119">no. do cartão
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-p119">no. do cartão</span></span> 
- <span data-ttu-id="ab3ec-1479">carta nr</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1479">nr carta</span></span> 
- <span data-ttu-id="ab3ec-p120">nr. carta
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-p120">nr. carta</span></span> 
- <span data-ttu-id="ab3ec-1482">numeri di scheda
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1482">numeri di scheda</span></span> 
- <span data-ttu-id="ab3ec-1483">numero carta
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1483">numero carta</span></span> 
- <span data-ttu-id="ab3ec-1484">numero de cartao
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1484">numero de cartao</span></span> 
- <span data-ttu-id="ab3ec-1485">numero de carte
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1485">numero de carte</span></span> 
- <span data-ttu-id="ab3ec-1486">numero de cartão
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1486">numero de cartão</span></span> 
- <span data-ttu-id="ab3ec-1487">numero de tarjeta
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1487">numero de tarjeta</span></span>
- <span data-ttu-id="ab3ec-1488">numero della carta
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1488">numero della carta</span></span> 
- <span data-ttu-id="ab3ec-1489">numero di carta
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1489">numero di carta</span></span> 
- <span data-ttu-id="ab3ec-1490">numero di scheda
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1490">numero di scheda</span></span> 
- <span data-ttu-id="ab3ec-1491">numero do cartao
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1491">numero do cartao</span></span> 
- <span data-ttu-id="ab3ec-1492">numero do cartão
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1492">numero do cartão</span></span> 
- <span data-ttu-id="ab3ec-1493">numéro de carte
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1493">numéro de carte</span></span> 
- <span data-ttu-id="ab3ec-1494">nº carta
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1494">nº carta</span></span> 
- <span data-ttu-id="ab3ec-1495">nº de carte
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1495">nº de carte</span></span> 
- <span data-ttu-id="ab3ec-1496">nº de la carte
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1496">nº de la carte</span></span> 
- <span data-ttu-id="ab3ec-1497">nº de tarjeta
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1497">nº de tarjeta</span></span> 
- <span data-ttu-id="ab3ec-1498">nº do cartao
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1498">nº do cartao</span></span> 
- <span data-ttu-id="ab3ec-1499">n º cartão</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1499">nº do cartão</span></span> 
- <span data-ttu-id="ab3ec-p121">nº. do cartão
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-p121">nº. do cartão</span></span> 
- <span data-ttu-id="ab3ec-1502">número de cartao
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1502">número de cartao</span></span> 
- <span data-ttu-id="ab3ec-1503">número de cartão
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1503">número de cartão</span></span> 
- <span data-ttu-id="ab3ec-1504">número de tarjeta
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1504">número de tarjeta</span></span> 
- <span data-ttu-id="ab3ec-1505">número do cartao</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1505">número do cartao</span></span> 
- <span data-ttu-id="ab3ec-1506">scheda dell'assegno
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1506">scheda dell'assegno</span></span> 
- <span data-ttu-id="ab3ec-1507">scheda dell'atmosfera
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1507">scheda dell'atmosfera</span></span> 
- <span data-ttu-id="ab3ec-1508">scheda dell'atmosfera
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1508">scheda dell'atmosfera</span></span> 
- <span data-ttu-id="ab3ec-1509">scheda della banca
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1509">scheda della banca</span></span> 
- <span data-ttu-id="ab3ec-1510">scheda di controllo
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1510">scheda di controllo</span></span> 
- <span data-ttu-id="ab3ec-1511">scheda di debito
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1511">scheda di debito</span></span> 
- <span data-ttu-id="ab3ec-1512">scheda matrice
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1512">scheda matrice</span></span> 
- <span data-ttu-id="ab3ec-1513">schede dell'atmosfera
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1513">schede dell'atmosfera</span></span> 
- <span data-ttu-id="ab3ec-1514">schede di controllo
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1514">schede di controllo</span></span> 
- <span data-ttu-id="ab3ec-1515">schede di debito
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1515">schede di debito</span></span> 
- <span data-ttu-id="ab3ec-1516">schede matrici
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1516">schede matrici</span></span> 
- <span data-ttu-id="ab3ec-1517">scoprono la scheda
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1517">scoprono la scheda</span></span> 
- <span data-ttu-id="ab3ec-1518">scoprono le schede
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1518">scoprono le schede</span></span> 
- <span data-ttu-id="ab3ec-1519">solo
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1519">solo</span></span> 
- <span data-ttu-id="ab3ec-1520">supporti di scheda
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1520">supporti di scheda</span></span> 
- <span data-ttu-id="ab3ec-1521">supporto di scheda
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1521">supporto di scheda</span></span> 
- <span data-ttu-id="ab3ec-1522">opção</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1522">switch</span></span> 
- <span data-ttu-id="ab3ec-1523">tarjeta atm
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1523">tarjeta atm</span></span> 
- <span data-ttu-id="ab3ec-1524">tarjeta credito
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1524">tarjeta credito</span></span> 
- <span data-ttu-id="ab3ec-1525">tarjeta de atm
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1525">tarjeta de atm</span></span> 
- <span data-ttu-id="ab3ec-1526">tarjeta de credito
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1526">tarjeta de credito</span></span> 
- <span data-ttu-id="ab3ec-1527">tarjeta de debito
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1527">tarjeta de debito</span></span> 
- <span data-ttu-id="ab3ec-1528">tarjeta debito
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1528">tarjeta debito</span></span> 
- <span data-ttu-id="ab3ec-1529">tarjeta no
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1529">tarjeta no</span></span>
- <span data-ttu-id="ab3ec-1530">tarjetahabiente
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1530">tarjetahabiente</span></span> 
- <span data-ttu-id="ab3ec-1531">tipo della scheda
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1531">tipo della scheda</span></span> 
- <span data-ttu-id="ab3ec-1532">ufficio giapponese della</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1532">ufficio giapponese della</span></span> 
- <span data-ttu-id="ab3ec-1533">scheda
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1533">scheda</span></span> 
- <span data-ttu-id="ab3ec-1534">v pay
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1534">v pay</span></span> 
- <span data-ttu-id="ab3ec-1535">Salário-v</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1535">v-pay</span></span> 
- <span data-ttu-id="ab3ec-1536">visa
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1536">visa</span></span> 
- <span data-ttu-id="ab3ec-1537">visa plus
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1537">visa plus</span></span> 
- <span data-ttu-id="ab3ec-1538">visa electron
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1538">visa electron</span></span> 
- <span data-ttu-id="ab3ec-1539">visto
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1539">visto</span></span> 
- <span data-ttu-id="ab3ec-1540">visum
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1540">visum</span></span> 
- <span data-ttu-id="ab3ec-1541">vpay
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1541">vpay</span></span>   

#### <a name="keywordcardsecuritytermsdict"></a><span data-ttu-id="ab3ec-1542">Keyword_card_security_terms_dict</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1542">Keyword_card_security_terms_dict</span></span>

- <span data-ttu-id="ab3ec-1543">card identification number</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1543">card identification number</span></span>
- <span data-ttu-id="ab3ec-1544">card verification</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1544">card verification</span></span> 
- <span data-ttu-id="ab3ec-1545">cardi la verifica
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1545">cardi la verifica</span></span> 
- <span data-ttu-id="ab3ec-1546">cid
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1546">cid</span></span> 
- <span data-ttu-id="ab3ec-1547">COD seg</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1547">cod seg</span></span> 
- <span data-ttu-id="ab3ec-1548">segurança de COD</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1548">cod seguranca</span></span> 
- <span data-ttu-id="ab3ec-1549">segurança de COD</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1549">cod segurança</span></span> 
- <span data-ttu-id="ab3ec-1550">COD sicurezza</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1550">cod sicurezza</span></span> 
- <span data-ttu-id="ab3ec-p122">cod. seg
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-p122">cod. seg</span></span> 
- <span data-ttu-id="ab3ec-p123">cod. seguranca
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-p123">cod. seguranca</span></span> 
- <span data-ttu-id="ab3ec-p124">cod. segurança
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-p124">cod. segurança</span></span> 
- <span data-ttu-id="ab3ec-p125">cod. sicurezza
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-p125">cod. sicurezza</span></span> 
- <span data-ttu-id="ab3ec-1559">codice di sicurezza
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1559">codice di sicurezza</span></span> 
- <span data-ttu-id="ab3ec-1560">codice di verifica
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1560">codice di verifica</span></span> 
- <span data-ttu-id="ab3ec-1561">codigo
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1561">codigo</span></span> 
- <span data-ttu-id="ab3ec-1562">codigo de seguranca
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1562">codigo de seguranca</span></span> 
- <span data-ttu-id="ab3ec-1563">codigo de segurança
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1563">codigo de segurança</span></span> 
- <span data-ttu-id="ab3ec-1564">crittogramma
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1564">crittogramma</span></span> 
- <span data-ttu-id="ab3ec-1565">cryptogram
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1565">cryptogram</span></span> 
- <span data-ttu-id="ab3ec-1566">cryptogramme
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1566">cryptogramme</span></span> 
- <span data-ttu-id="ab3ec-1567">CV2</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1567">cv2</span></span> 
- <span data-ttu-id="ab3ec-1568">cvc
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1568">cvc</span></span> 
- <span data-ttu-id="ab3ec-1569">CVC2</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1569">cvc2</span></span> 
- <span data-ttu-id="ab3ec-1570">cvn
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1570">cvn</span></span> 
- <span data-ttu-id="ab3ec-1571">cvv
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1571">cvv</span></span> 
- <span data-ttu-id="ab3ec-1572">cvv2</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1572">cvv2</span></span> 
- <span data-ttu-id="ab3ec-1573">segurança Cód</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1573">cód seguranca</span></span> 
- <span data-ttu-id="ab3ec-1574">segurança Cód</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1574">cód segurança</span></span> 
- <span data-ttu-id="ab3ec-p126">cód. seguranca
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-p126">cód. seguranca</span></span> 
- <span data-ttu-id="ab3ec-p127">cód. segurança
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-p127">cód. segurança</span></span> 
- <span data-ttu-id="ab3ec-1579">código
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1579">código</span></span> 
- <span data-ttu-id="ab3ec-1580">código de seguranca
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1580">código de seguranca</span></span> 
- <span data-ttu-id="ab3ec-1581">código de segurança
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1581">código de segurança</span></span> 
- <span data-ttu-id="ab3ec-1582">de kaart controle
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1582">de kaart controle</span></span> 
- <span data-ttu-id="ab3ec-1583">geeft nr uit
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1583">geeft nr uit</span></span> 
- <span data-ttu-id="ab3ec-1584">issue no
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1584">issue no</span></span> 
- <span data-ttu-id="ab3ec-1585">issue number
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1585">issue number</span></span> 
- <span data-ttu-id="ab3ec-1586">kaartidentificatienummer
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1586">kaartidentificatienummer</span></span> 
- <span data-ttu-id="ab3ec-1587">kreditkartenprufnummer
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1587">kreditkartenprufnummer</span></span> 
- <span data-ttu-id="ab3ec-1588">kreditkartenprüfnummer
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1588">kreditkartenprüfnummer</span></span> 
- <span data-ttu-id="ab3ec-1589">kwestieaantal
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1589">kwestieaantal</span></span> 
- <span data-ttu-id="ab3ec-p128">no. dell'edizione
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-p128">no. dell'edizione</span></span> 
- <span data-ttu-id="ab3ec-p129">no. di sicurezza
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-p129">no. di sicurezza</span></span> 
- <span data-ttu-id="ab3ec-1594">numero de securite
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1594">numero de securite</span></span> 
- <span data-ttu-id="ab3ec-1595">numero de verificacao
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1595">numero de verificacao</span></span> 
- <span data-ttu-id="ab3ec-1596">numero dell'edizione
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1596">numero dell'edizione</span></span> 
- <span data-ttu-id="ab3ec-1597">numero di identificazione della</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1597">numero di identificazione della</span></span> 
- <span data-ttu-id="ab3ec-1598">scheda
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1598">scheda</span></span> 
- <span data-ttu-id="ab3ec-1599">numero di sicurezza
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1599">numero di sicurezza</span></span> 
- <span data-ttu-id="ab3ec-1600">numero van veiligheid
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1600">numero van veiligheid</span></span> 
- <span data-ttu-id="ab3ec-1601">numéro de sécurité
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1601">numéro de sécurité</span></span> 
- <span data-ttu-id="ab3ec-1602">nº autorizzazione
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1602">nº autorizzazione</span></span> 
- <span data-ttu-id="ab3ec-1603">número de verificação
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1603">número de verificação</span></span> 
- <span data-ttu-id="ab3ec-1604">perno il blocco
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1604">perno il blocco</span></span> 
- <span data-ttu-id="ab3ec-1605">pin block
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1605">pin block</span></span> 
- <span data-ttu-id="ab3ec-1606">prufziffer
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1606">prufziffer</span></span> 
- <span data-ttu-id="ab3ec-1607">prüfziffer
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1607">prüfziffer</span></span> 
- <span data-ttu-id="ab3ec-1608">security code
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1608">security code</span></span> 
- <span data-ttu-id="ab3ec-1609">security no
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1609">security no</span></span> 
- <span data-ttu-id="ab3ec-1610">security number
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1610">security number</span></span> 
- <span data-ttu-id="ab3ec-1611">sicherheits kode
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1611">sicherheits kode</span></span> 
- <span data-ttu-id="ab3ec-1612">sicherheitscode
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1612">sicherheitscode</span></span> 
- <span data-ttu-id="ab3ec-1613">sicherheitsnummer
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1613">sicherheitsnummer</span></span> 
- <span data-ttu-id="ab3ec-1614">speldblok
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1614">speldblok</span></span> 
- <span data-ttu-id="ab3ec-1615">veiligheid nr
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1615">veiligheid nr</span></span> 
- <span data-ttu-id="ab3ec-1616">veiligheidsaantal
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1616">veiligheidsaantal</span></span> 
- <span data-ttu-id="ab3ec-1617">veiligheidscode
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1617">veiligheidscode</span></span> 
- <span data-ttu-id="ab3ec-1618">veiligheidsnummer
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1618">veiligheidsnummer</span></span> 
- <span data-ttu-id="ab3ec-1619">verfalldatum
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1619">verfalldatum</span></span> 

#### <a name="keywordcardexpirationtermsdict"></a><span data-ttu-id="ab3ec-1620">Keyword_card_expiration_terms_dict</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1620">Keyword_card_expiration_terms_dict</span></span>

- <span data-ttu-id="ab3ec-1621">ablauf
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1621">ablauf</span></span> 
- <span data-ttu-id="ab3ec-1622">data de expiracao
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1622">data de expiracao</span></span> 
- <span data-ttu-id="ab3ec-1623">data de expiração
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1623">data de expiração</span></span> 
- <span data-ttu-id="ab3ec-1624">data del exp
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1624">data del exp</span></span> 
- <span data-ttu-id="ab3ec-1625">data di exp
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1625">data di exp</span></span> 
- <span data-ttu-id="ab3ec-1626">data di scadenza
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1626">data di scadenza</span></span> 
- <span data-ttu-id="ab3ec-1627">data em que expira
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1627">data em que expira</span></span> 
- <span data-ttu-id="ab3ec-1628">data scad
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1628">data scad</span></span> 
- <span data-ttu-id="ab3ec-1629">data scadenza
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1629">data scadenza</span></span> 
- <span data-ttu-id="ab3ec-1630">date de validité
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1630">date de validité</span></span> 
- <span data-ttu-id="ab3ec-1631">datum afloop
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1631">datum afloop</span></span> 
- <span data-ttu-id="ab3ec-1632">datum van exp
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1632">datum van exp</span></span> 
- <span data-ttu-id="ab3ec-1633">de afloop
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1633">de afloop</span></span> 
- <span data-ttu-id="ab3ec-1634">espira
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1634">espira</span></span> 
- <span data-ttu-id="ab3ec-1635">espira
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1635">espira</span></span> 
- <span data-ttu-id="ab3ec-1636">exp date
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1636">exp date</span></span> 
- <span data-ttu-id="ab3ec-1637">exp datum
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1637">exp datum</span></span> 
- <span data-ttu-id="ab3ec-1638">expiração</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1638">expiration</span></span> 
- <span data-ttu-id="ab3ec-1639">expire
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1639">expire</span></span> 
- <span data-ttu-id="ab3ec-1640">expires
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1640">expires</span></span> 
- <span data-ttu-id="ab3ec-1641">expiry
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1641">expiry</span></span> 
- <span data-ttu-id="ab3ec-1642">fecha de expiracion
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1642">fecha de expiracion</span></span> 
- <span data-ttu-id="ab3ec-1643">fecha de venc
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1643">fecha de venc</span></span> 
- <span data-ttu-id="ab3ec-1644">gultig bis
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1644">gultig bis</span></span> 
- <span data-ttu-id="ab3ec-1645">gultigkeitsdatum
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1645">gultigkeitsdatum</span></span> 
- <span data-ttu-id="ab3ec-1646">gültig bis
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1646">gültig bis</span></span> 
- <span data-ttu-id="ab3ec-1647">gültigkeitsdatum
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1647">gültigkeitsdatum</span></span> 
- <span data-ttu-id="ab3ec-1648">la scadenza
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1648">la scadenza</span></span> 
- <span data-ttu-id="ab3ec-1649">scadenza
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1649">scadenza</span></span> 
- <span data-ttu-id="ab3ec-1650">valable
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1650">valable</span></span> 
- <span data-ttu-id="ab3ec-1651">validade
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1651">validade</span></span> 
- <span data-ttu-id="ab3ec-1652">valido hasta
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1652">valido hasta</span></span> 
- <span data-ttu-id="ab3ec-1653">valor
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1653">valor</span></span> 
- <span data-ttu-id="ab3ec-1654">venc
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1654">venc</span></span> 
- <span data-ttu-id="ab3ec-1655">vencimento
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1655">vencimento</span></span> 
- <span data-ttu-id="ab3ec-1656">vencimiento
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1656">vencimiento</span></span> 
- <span data-ttu-id="ab3ec-1657">verloopt
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1657">verloopt</span></span> 
- <span data-ttu-id="ab3ec-1658">vervaldag
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1658">vervaldag</span></span> 
- <span data-ttu-id="ab3ec-1659">vervaldatum
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1659">vervaldatum</span></span> 
- <span data-ttu-id="ab3ec-1660">vto
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1660">vto</span></span> 
- <span data-ttu-id="ab3ec-1661">válido hasta
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1661">válido hasta</span></span> 
   
## <a name="eu-drivers-license-number"></a><span data-ttu-id="ab3ec-1662">Número de carteira de motorista da UE</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1662">EU Driver's License Number</span></span>

<span data-ttu-id="ab3ec-1663">Para saber mais, consulte o [tipo de informação confidencial do número de carteira de motorista da UE](eu-driver-s-license-number.md).</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1663">To learn more, see [EU Driver's License Number sensitive information type](eu-driver-s-license-number.md).</span></span>
  
## <a name="eu-national-identification-number"></a><span data-ttu-id="ab3ec-1664">Número de identificação nacional da UE</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1664">EU National Identification Number</span></span>

<span data-ttu-id="ab3ec-1665">Para saber mais, consulte o [tipo de informação confidencial do número de identificação nacional da UE](eu-national-identification-number.md).</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1665">To learn more, see [EU National Identification Number sensitive information type](eu-national-identification-number.md).</span></span>
  
## <a name="eu-passport-number"></a><span data-ttu-id="ab3ec-1666">Número de passaporte da UE</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1666">EU Passport Number</span></span>

<span data-ttu-id="ab3ec-1667">Para saber mais, consulte o [tipo de informação confidencial do número de passaporte da UE](eu-passport-number.md).</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1667">To learn more, see [EU Passport Number sensitive information type](eu-passport-number.md).</span></span>
  
## <a name="eu-social-security-number-or-equivalent-id"></a><span data-ttu-id="ab3ec-1668">ID do número de Seguridade Social da UE ou equivalente</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1668">EU Social Security Number or Equivalent ID</span></span>

<span data-ttu-id="ab3ec-1669">Para saber mais, consulte o [número de Seguridade Social da UE ou tipo de informação confidencial ID equivalente](eu-social-security-number-or-equivalent-id.md).</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1669">To learn more, see [EU Social Security Number or Equivalent ID sensitive information type](eu-social-security-number-or-equivalent-id.md).</span></span>
  
## <a name="eu-tax-identification-number"></a><span data-ttu-id="ab3ec-1670">Número de identificação de imposto da UE</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1670">EU Tax Identification Number</span></span>

<span data-ttu-id="ab3ec-1671">Para saber mais, consulte o [tipo de informação confidencial do número de identificação de imposto da UE](eu-tax-identification-number.md).</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1671">To learn more, see [EU Tax Identification Number sensitive information type](eu-tax-identification-number.md).</span></span>
  
## <a name="finland-national-id"></a><span data-ttu-id="ab3ec-1672">ID nacional da Finlândia</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1672">Finland National ID</span></span>

### <a name="format"></a><span data-ttu-id="ab3ec-1673">Formato</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1673">Format</span></span>

<span data-ttu-id="ab3ec-1674">Seis dígitos mais um caractere indicando um século mais três dígitos mais um dígito de verificação</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1674">Six digits plus a character indicating a century plus three digits plus a check digit</span></span>

### <a name="pattern"></a><span data-ttu-id="ab3ec-1675">Padrão</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1675">Pattern</span></span>

<span data-ttu-id="ab3ec-1676">O padrão deve incluir todos os seguintes itens:</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1676">Pattern must include all of the following:</span></span>
- <span data-ttu-id="ab3ec-1677">Seis dígitos no formato DDMMAA que é uma data de nascimento</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1677">Six digits in the format format DDMMYY which are a date of birth</span></span> 
- <span data-ttu-id="ab3ec-1678">Marcador do século (qualquer '-', '+' ou 'a')</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1678">Century marker (either '-', '+' or 'a')</span></span> 
- <span data-ttu-id="ab3ec-1679">Número de identificação pessoal de três dígitos</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1679">Three-digit personal identification number</span></span> 
- <span data-ttu-id="ab3ec-1680">Um dígito ou letra (não diferencia maiúscula de minúscula), que é um dígito de verificação</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1680">A digit or letter (case insensitive) which is a check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="ab3ec-1681">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1681">Checksum</span></span>

<span data-ttu-id="ab3ec-1682">Sim</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1682">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="ab3ec-1683">Definição</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1683">Definition</span></span>

<span data-ttu-id="ab3ec-1684">Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1684">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="ab3ec-1685">A função Func_finnish_national_id localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1685">The function Func_finnish_national_id finds content that matches the pattern.</span></span>
- <span data-ttu-id="ab3ec-1686">Uma palavra-chave de Keyword_finnish_national_id for encontrada.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1686">A keyword from Keyword_finnish_national_id is found.</span></span>
- <span data-ttu-id="ab3ec-1687">A soma de verificação passa.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1687">The checksum passes.</span></span>

```
<!-- Finnish National ID-->
<Entity id="338FD995-4CB5-4F87-AD35-79BD1DD926C1" patternsProximity="300" recommendedConfidence="85">
  <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_finnish_national_id" />
          <Match idRef="Keyword_finnish_national_id" />
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="ab3ec-1688">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1688">Keywords</span></span>

- <span data-ttu-id="ab3ec-1689">Keyword_finnish_national_id</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1689">Keyword_finnish_national_id</span></span>
- <span data-ttu-id="ab3ec-1690">

Sosiaaliturvatunnus</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1690">Sosiaaliturvatunnus</span></span>
- <span data-ttu-id="ab3ec-1691">SOTU Henkilötunnus HETU</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1691">SOTU Henkilötunnus HETU</span></span>
- <span data-ttu-id="ab3ec-1692">Personbeteckning</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1692">Personbeteckning</span></span>
- <span data-ttu-id="ab3ec-1693">Personnummer</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1693">Personnummer</span></span>
   
## <a name="finland-passport-number"></a><span data-ttu-id="ab3ec-1694">Número de Passaporte da Finlândia</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1694">Finland Passport Number</span></span>

<span data-ttu-id="ab3ec-p130">Formatar a combinação de nove letras e dígitos combinação de padrão de nove letras e dígitos: política de DLP de uma soma de verificação não definição do duas letras (não maiusculas de minúsculas) sete dígitos é 75% confiante de que detectou esse tipo de informações confidenciais se, contido em um proximidade de 300 caracteres: A expressão regular Regex_finland_passport_number encontra o conteúdo que corresponde ao padrão. Uma palavra-chave de Keyword_finland_passport_number é encontrada. <!-- Finland Passport Number --> 
 <Entity id="d1685ac3-1d3a-40f8-8198-32ef5669c7a5" recommendedConfidence="75" patternsProximity="300"> <Pattern confidenceLevel="75"> <IdMatch idRef="Regex_finland_passport_number"/> <Match idRef="Keyword_finland_passport_number"/> </Pattern> 
 </Entity> Palavras-chave Keyword_finland_passport_number Passport Passi</span><span class="sxs-lookup"><span data-stu-id="ab3ec-p130">Format Combination of nine letters and digits Pattern Combination of nine letters and digits: Two letters (not case sensitive) Seven digits Checksum No Definition A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters: The regular expression Regex_finland_passport_number finds content that matches the pattern. A keyword from Keyword_finland_passport_number is found. <!-- Finland Passport Number -->
<Entity id="d1685ac3-1d3a-40f8-8198-32ef5669c7a5" recommendedConfidence="75" patternsProximity="300"> <Pattern confidenceLevel="75"> <IdMatch idRef="Regex_finland_passport_number"/> <Match idRef="Keyword_finland_passport_number"/> </Pattern>
</Entity> Keywords Keyword_finland_passport_number Passport Passi</span></span>
   
## <a name="france-drivers-license-number"></a><span data-ttu-id="ab3ec-1699">Número de carteira de motorista da França</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1699">France Driver's License Number</span></span>

### <a name="format"></a><span data-ttu-id="ab3ec-1700">Formato</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1700">Format</span></span>

<span data-ttu-id="ab3ec-1701">12 dígitos</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1701">12 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="ab3ec-1702">Padrão</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1702">Pattern</span></span>

<span data-ttu-id="ab3ec-1703">12 dígitos com a validação para descontar padrões similares, como números de telefone em francês</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1703">12 digits with validation to discount similar patterns such as French telephone numbers</span></span>

### <a name="checksum"></a><span data-ttu-id="ab3ec-1704">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1704">Checksum</span></span>

<span data-ttu-id="ab3ec-1705">Não</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1705">No</span></span>

### <a name="definition"></a><span data-ttu-id="ab3ec-1706">Definição</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1706">Definition</span></span>

<span data-ttu-id="ab3ec-1707">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1707">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="ab3ec-1708">A função Func_french_drivers_license localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1708">The function Func_french_drivers_license finds content that matches the pattern.</span></span>
- <span data-ttu-id="ab3ec-1709">Pelo menos uma das seguintes opções for verdadeira:</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1709">At least one of the following is true:</span></span>
- <span data-ttu-id="ab3ec-1710">Uma palavra-chave de Keyword_french_drivers_license for encontrada.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1710">A keyword from Keyword_french_drivers_license is found.</span></span>
- <span data-ttu-id="ab3ec-1711">A função Func_eu_date encontra uma data no formato de data à direita.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1711">The function Func_eu_date finds a date in the right date format.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="ab3ec-1712">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1712">Keywords</span></span>

#### <a name="keywordfrenchdriverslicense"></a><span data-ttu-id="ab3ec-1713">Keyword_french_drivers_license</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1713">Keyword_french_drivers_license</span></span>

- <span data-ttu-id="ab3ec-1714">drivers licence</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1714">drivers licence</span></span>
- <span data-ttu-id="ab3ec-1715">
drivers license</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1715">drivers license</span></span>
- <span data-ttu-id="ab3ec-1716">driving licence
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1716">driving licence</span></span>
- <span data-ttu-id="ab3ec-1717">orientando licença</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1717">driving license</span></span>
- <span data-ttu-id="ab3ec-1718">
permis de conduire</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1718">permis de conduire</span></span>
- <span data-ttu-id="ab3ec-1719">
licence number</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1719">licence number</span></span>
- <span data-ttu-id="ab3ec-1720">
license number</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1720">license number</span></span>
- <span data-ttu-id="ab3ec-1721">
licence numbers</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1721">licence numbers</span></span>
- <span data-ttu-id="ab3ec-1722">

license numbers</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1722">license numbers</span></span>

## <a name="france-national-id-card-cni"></a><span data-ttu-id="ab3ec-1723">Cartão de identificação nacional da França (CNI)</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1723">France National ID Card (CNI)</span></span>

### <a name="format"></a><span data-ttu-id="ab3ec-1724">Formato</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1724">Format</span></span>

<span data-ttu-id="ab3ec-1725">12 dígitos</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1725">12 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="ab3ec-1726">Padrão</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1726">Pattern</span></span>

<span data-ttu-id="ab3ec-1727">12 dígitos</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1727">12 digits</span></span>

### <a name="checksum"></a><span data-ttu-id="ab3ec-1728">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1728">Checksum</span></span>

<span data-ttu-id="ab3ec-1729">Não</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1729">No</span></span>

### <a name="definition"></a><span data-ttu-id="ab3ec-1730">Definição</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1730">Definition</span></span>

<span data-ttu-id="ab3ec-1731">Uma política de DLP tem 65% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1731">A DLP policy is 65% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="ab3ec-1732">A expressão regular Regex_france_cni localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1732">The regular expression Regex_france_cni finds content that matches the pattern.</span></span>

```
<!-- France CNI -->
<Entity id="f741ac74-1bc0-4665-b69b-f0c7f927c0c4" patternsProximity="300" recommendedConfidence="65">
  <Pattern confidenceLevel="65">
        <IdMatch idRef="Regex_france_cni" />
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="ab3ec-1733">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1733">Keywords</span></span>

<span data-ttu-id="ab3ec-1734">Nenhum</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1734">None</span></span>
   
## <a name="france-passport-number"></a><span data-ttu-id="ab3ec-1735">Número de passaporte da França</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1735">France Passport Number</span></span>

### <a name="format"></a><span data-ttu-id="ab3ec-1736">Formato</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1736">Format</span></span>

<span data-ttu-id="ab3ec-1737">Nove letras e dígitos</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1737">Nine digits and letters</span></span>

### <a name="pattern"></a><span data-ttu-id="ab3ec-1738">Padrão</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1738">Pattern</span></span>

<span data-ttu-id="ab3ec-1739">Nove letras e dígitos:</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1739">Nine digits and letters:</span></span>
- <span data-ttu-id="ab3ec-1740">Dois dígitos</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1740">Two digits</span></span> 
- <span data-ttu-id="ab3ec-1741">Duas letras (não diferenciam maiúsculas de minúsculas)</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1741">Two letters (not case sensitive)</span></span> 
- <span data-ttu-id="ab3ec-1742">Cinco dígitos</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1742">Five digits</span></span>

### <a name="checksum"></a><span data-ttu-id="ab3ec-1743">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1743">Checksum</span></span>

<span data-ttu-id="ab3ec-1744">Não</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1744">No</span></span>

### <a name="definition"></a><span data-ttu-id="ab3ec-1745">Definição</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1745">Definition</span></span>

<span data-ttu-id="ab3ec-1746">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1746">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="ab3ec-1747">A função Func_fr_passport localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1747">The function Func_fr_passport finds content that matches the pattern.</span></span>
- <span data-ttu-id="ab3ec-1748">Uma palavra-chave de Keyword_passport for encontrada.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1748">A keyword from Keyword_passport is found.</span></span>

```
<!-- France Passport Number -->
<Entity id="3008b884-8c8c-4cd8-a289-99f34fc7ff5d" patternsProximity="300" recommendedConfidence="75">
  <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_fr_passport" />
        <Match idRef="Keyword_passport" />
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="ab3ec-1749">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1749">Keywords</span></span>

#### <a name="keywordpassport"></a><span data-ttu-id="ab3ec-1750">Keyword_passport</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1750">Keyword_passport</span></span>

- <span data-ttu-id="ab3ec-1751">Passport Number</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1751">Passport Number</span></span>
- <span data-ttu-id="ab3ec-1752">
Passport No</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1752">Passport No</span></span>
- <span data-ttu-id="ab3ec-1753">Passport #
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1753">Passport #</span></span>
- <span data-ttu-id="ab3ec-1754">Passport#
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1754">Passport#</span></span>
- <span data-ttu-id="ab3ec-1755">PassportID</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1755">PassportID</span></span>
- <span data-ttu-id="ab3ec-1756">Passportno
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1756">Passportno</span></span>
- <span data-ttu-id="ab3ec-1757">passportnumber
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1757">passportnumber</span></span>
- <span data-ttu-id="ab3ec-1758">パスポート</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1758">パスポート</span></span>
- <span data-ttu-id="ab3ec-1759">パスポート番号
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1759">パスポート番号</span></span>
- <span data-ttu-id="ab3ec-1760">パスポートのNum
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1760">パスポートのNum</span></span>
- <span data-ttu-id="ab3ec-1761">
パスポート ＃
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1761">パスポート ＃</span></span> 
- <span data-ttu-id="ab3ec-1762">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1762">Numéro de passeport</span></span>
- <span data-ttu-id="ab3ec-1763">
Passeport n °</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1763">Passeport n °</span></span>
- <span data-ttu-id="ab3ec-1764">Passeport Non
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1764">Passeport Non</span></span>
- <span data-ttu-id="ab3ec-1765">Passeport #
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1765">Passeport #</span></span>
- <span data-ttu-id="ab3ec-1766">Passeport#
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1766">Passeport#</span></span>
- <span data-ttu-id="ab3ec-1767">PasseportNon</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1767">PasseportNon</span></span>
- <span data-ttu-id="ab3ec-1768">

Passeportn °</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1768">Passeportn °</span></span>

      
## <a name="france-social-security-number-insee"></a><span data-ttu-id="ab3ec-1769">Número de seguridade social da França (INSEE)</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1769">France Social Security Number (INSEE)</span></span>

### <a name="format"></a><span data-ttu-id="ab3ec-1770">Formato</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1770">Format</span></span>

<span data-ttu-id="ab3ec-1771">15 dígitos</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1771">15 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="ab3ec-1772">Padrão</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1772">Pattern</span></span>

<span data-ttu-id="ab3ec-1773">Deve corresponder a um dos dois padrões:</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1773">Must match one of two patterns:</span></span>
- <span data-ttu-id="ab3ec-1774">13 dígitos seguidos por um espaço seguido por dois dígitos</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1774">13 digits followed by a space followed by two digits</span></span></br>
<span data-ttu-id="ab3ec-1775">ou</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1775">or</span></span>
- <span data-ttu-id="ab3ec-1776">15 dígitos consecutivos</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1776">15 consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="ab3ec-1777">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1777">Checksum</span></span>

<span data-ttu-id="ab3ec-1778">Sim</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1778">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="ab3ec-1779">Definição</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1779">Definition</span></span>

<span data-ttu-id="ab3ec-1780">Uma política de DLP tem 95% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1780">A DLP policy is 95% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="ab3ec-1781">A função Func_french_insee ou Func_fr_insee encontra o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1781">The function Func_french_insee or Func_fr_insee finds content that matches the pattern.</span></span>
- <span data-ttu-id="ab3ec-1782">Uma palavra-chave de Keyword_fr_insee for encontrada.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1782">A keyword from Keyword_fr_insee is found.</span></span>
- <span data-ttu-id="ab3ec-1783">A soma de verificação passa.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1783">The checksum passes.</span></span>

<span data-ttu-id="ab3ec-1784">Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1784">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="ab3ec-1785">A função Func_french_insee ou Func_fr_insee encontra o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1785">The function Func_french_insee or Func_fr_insee finds content that matches the pattern.</span></span>
- <span data-ttu-id="ab3ec-1786">Nenhuma palavra-chave de Keyword_fr_insee for encontrada.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1786">No keyword from Keyword_fr_insee is found.</span></span>
- <span data-ttu-id="ab3ec-1787">A soma de verificação passa.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1787">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="ab3ec-1788">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1788">Keywords</span></span>

#### <a name="keywordfrinsee"></a><span data-ttu-id="ab3ec-1789">Keyword_fr_insee</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1789">Keyword_fr_insee</span></span>

- <span data-ttu-id="ab3ec-1790">insee</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1790">insee</span></span>
- <span data-ttu-id="ab3ec-1791">
securité sociale</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1791">securité sociale</span></span>
- <span data-ttu-id="ab3ec-1792">
securite sociale</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1792">securite sociale</span></span>
- <span data-ttu-id="ab3ec-1793">
national id</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1793">national id</span></span>
- <span data-ttu-id="ab3ec-1794">
national identification</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1794">national identification</span></span>
- <span data-ttu-id="ab3ec-1795">
numéro d'identité</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1795">numéro d'identité</span></span>
- <span data-ttu-id="ab3ec-1796">Nenhum d'identité</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1796">no d'identité</span></span>
- <span data-ttu-id="ab3ec-p131">
no. d'identité</span><span class="sxs-lookup"><span data-stu-id="ab3ec-p131">no. d'identité</span></span>
- <span data-ttu-id="ab3ec-1799">
numero d'identite</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1799">numero d'identite</span></span>
- <span data-ttu-id="ab3ec-1800">Nenhum d'identite</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1800">no d'identite</span></span>
- <span data-ttu-id="ab3ec-p132">
no. d'identite</span><span class="sxs-lookup"><span data-stu-id="ab3ec-p132">no. d'identite</span></span>
- <span data-ttu-id="ab3ec-1803">social security number
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1803">social security number</span></span>
- <span data-ttu-id="ab3ec-1804">
social security code</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1804">social security code</span></span>
- <span data-ttu-id="ab3ec-1805">social insurance number</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1805">social insurance number</span></span>
- <span data-ttu-id="ab3ec-1806">
le numéro d'identification nationale</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1806">le numéro d'identification nationale</span></span>
- <span data-ttu-id="ab3ec-1807">
d'identité nationale</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1807">d'identité nationale</span></span>
- <span data-ttu-id="ab3ec-1808">
numéro de sécurité sociale</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1808">numéro de sécurité sociale</span></span>
- <span data-ttu-id="ab3ec-1809">
le code de la sécurité sociale</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1809">le code de la sécurité sociale</span></span>
- <span data-ttu-id="ab3ec-1810">
numéro d'assurance sociale</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1810">numéro d'assurance sociale</span></span>
- <span data-ttu-id="ab3ec-1811">
numéro de sécu</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1811">numéro de sécu</span></span>
- <span data-ttu-id="ab3ec-1812">
code sécu
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1812">code sécu</span></span> 
   
## <a name="german-drivers-license-number"></a><span data-ttu-id="ab3ec-1813">Número de carteira de motorista da Alemanha</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1813">German Driver's License Number</span></span>

### <a name="format"></a><span data-ttu-id="ab3ec-1814">Formato</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1814">Format</span></span>

<span data-ttu-id="ab3ec-1815">Combinação de 11 dígitos e letras</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1815">Combination of 11 digits and letters</span></span>

### <a name="pattern"></a><span data-ttu-id="ab3ec-1816">Padrão</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1816">Pattern</span></span>

<span data-ttu-id="ab3ec-1817">11 dígitos e letras (não diferenciam maiúsculas de minúsculas):</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1817">11 digits and letters (not case sensitive):</span></span>
- <span data-ttu-id="ab3ec-1818">Um dígito ou letra</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1818">A digit or letter</span></span> 
- <span data-ttu-id="ab3ec-1819">Dois dígitos</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1819">Two digits</span></span> 
- <span data-ttu-id="ab3ec-1820">Seis dígitos ou letras</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1820">Six digits or letters</span></span> 
- <span data-ttu-id="ab3ec-1821">Um dígito</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1821">A digit</span></span> 
- <span data-ttu-id="ab3ec-1822">Um dígito ou letra</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1822">A digit or letter</span></span>

### <a name="checksum"></a><span data-ttu-id="ab3ec-1823">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1823">Checksum</span></span>

<span data-ttu-id="ab3ec-1824">Sim</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1824">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="ab3ec-1825">Definição</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1825">Definition</span></span>

<span data-ttu-id="ab3ec-1826">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1826">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="ab3ec-1827">A função Func_german_drivers_license localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1827">The function Func_german_drivers_license finds content that matches the pattern.</span></span>
- <span data-ttu-id="ab3ec-1828">Pelo menos uma das seguintes opções for verdadeira:</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1828">At least one of the following is true:</span></span>
    - <span data-ttu-id="ab3ec-1829">Uma palavra-chave de Keyword_german_drivers_license_number for encontrada.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1829">A keyword from Keyword_german_drivers_license_number is found.</span></span>
    - <span data-ttu-id="ab3ec-1830">Uma palavra-chave de Keyword_german_drivers_license_collaborative for encontrada.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1830">A keyword from Keyword_german_drivers_license_collaborative is found.</span></span>
    - <span data-ttu-id="ab3ec-1831">Uma palavra-chave de Keyword_german_drivers_license for encontrada.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1831">A keyword from Keyword_german_drivers_license is found.</span></span>
- <span data-ttu-id="ab3ec-1832">A soma de verificação passa.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1832">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="ab3ec-1833">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1833">Keywords</span></span>

#### <a name="keywordgermandriverslicensenumber"></a><span data-ttu-id="ab3ec-1834">Keyword_german_drivers_license_number</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1834">Keyword_german_drivers_license_number</span></span>

- <span data-ttu-id="ab3ec-1835">Führerschein</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1835">Führerschein</span></span>
- <span data-ttu-id="ab3ec-1836">
Fuhrerschein</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1836">Fuhrerschein</span></span>
- <span data-ttu-id="ab3ec-1837">Fuehrerschein</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1837">Fuehrerschein</span></span>
- <span data-ttu-id="ab3ec-1838">
Führerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1838">Führerscheinnummer</span></span>
- <span data-ttu-id="ab3ec-1839">
Fuhrerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1839">Fuhrerscheinnummer</span></span>
- <span data-ttu-id="ab3ec-1840">
Fuehrerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1840">Fuehrerscheinnummer</span></span>
- <span data-ttu-id="ab3ec-1841">
Führerschein-
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1841">Führerschein-</span></span> 
- <span data-ttu-id="ab3ec-1842">Fuhrerschein-
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1842">Fuhrerschein-</span></span> 
- <span data-ttu-id="ab3ec-1843">Fuehrerschein-
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1843">Fuehrerschein-</span></span> 
- <span data-ttu-id="ab3ec-1844">FührerscheinnummerNr</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1844">FührerscheinnummerNr</span></span>
- <span data-ttu-id="ab3ec-1845">FuhrerscheinnummerNr</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1845">FuhrerscheinnummerNr</span></span>
- <span data-ttu-id="ab3ec-1846">FuehrerscheinnummerNr</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1846">FuehrerscheinnummerNr</span></span>
- <span data-ttu-id="ab3ec-1847">FührerscheinnummerKlasse</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1847">FührerscheinnummerKlasse</span></span>
- <span data-ttu-id="ab3ec-1848">FuhrerscheinnummerKlasse</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1848">FuhrerscheinnummerKlasse</span></span>
- <span data-ttu-id="ab3ec-1849">FuehrerscheinnummerKlasse</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1849">FuehrerscheinnummerKlasse</span></span>
- <span data-ttu-id="ab3ec-1850">Führerschein- Nr
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1850">Führerschein- Nr</span></span>
- <span data-ttu-id="ab3ec-1851">Fuhrerschein- Nr
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1851">Fuhrerschein- Nr</span></span>
- <span data-ttu-id="ab3ec-1852">Fuehrerschein- Nr
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1852">Fuehrerschein- Nr</span></span> 
- <span data-ttu-id="ab3ec-1853">Führerschein- Klasse
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1853">Führerschein- Klasse</span></span> 
- <span data-ttu-id="ab3ec-1854">Fuhrerschein- Klasse
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1854">Fuhrerschein- Klasse</span></span> 
- <span data-ttu-id="ab3ec-1855">Fuehrerschein- Klasse</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1855">Fuehrerschein- Klasse</span></span>
- <span data-ttu-id="ab3ec-1856">FührerscheinnummerNr</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1856">FührerscheinnummerNr</span></span> 
- <span data-ttu-id="ab3ec-1857">FuhrerscheinnummerNr</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1857">FuhrerscheinnummerNr</span></span> 
- <span data-ttu-id="ab3ec-1858">FuehrerscheinnummerNr</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1858">FuehrerscheinnummerNr</span></span> 
- <span data-ttu-id="ab3ec-1859">FührerscheinnummerKlasse</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1859">FührerscheinnummerKlasse</span></span> 
- <span data-ttu-id="ab3ec-1860">FuhrerscheinnummerKlasse</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1860">FuhrerscheinnummerKlasse</span></span> 
- <span data-ttu-id="ab3ec-1861">FuehrerscheinnummerKlasse</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1861">FuehrerscheinnummerKlasse</span></span> 
- <span data-ttu-id="ab3ec-1862">Führerschein- Nr
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1862">Führerschein- Nr</span></span> 
- <span data-ttu-id="ab3ec-1863">Fuhrerschein- Nr
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1863">Fuhrerschein- Nr</span></span> 
- <span data-ttu-id="ab3ec-1864">Fuehrerschein- Nr
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1864">Fuehrerschein- Nr</span></span> 
- <span data-ttu-id="ab3ec-1865">Führerschein- Klasse
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1865">Führerschein- Klasse</span></span> 
- <span data-ttu-id="ab3ec-1866">Fuhrerschein- Klasse
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1866">Fuhrerschein- Klasse</span></span> 
- <span data-ttu-id="ab3ec-1867">Fuehrerschein- Klasse</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1867">Fuehrerschein- Klasse</span></span> 
- <span data-ttu-id="ab3ec-1868">DL</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1868">DL</span></span> 
- <span data-ttu-id="ab3ec-1869">DLS</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1869">DLS</span></span>
- <span data-ttu-id="ab3ec-1870">
Driv Lic
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1870">Driv Lic</span></span> 
- <span data-ttu-id="ab3ec-1871">Driv Licen
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1871">Driv Licen</span></span> 
- <span data-ttu-id="ab3ec-1872">Driv License</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1872">Driv License</span></span>
- <span data-ttu-id="ab3ec-1873">
Driv Licenses
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1873">Driv Licenses</span></span> 
- <span data-ttu-id="ab3ec-1874">Driv Licence
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1874">Driv Licence</span></span> 
- <span data-ttu-id="ab3ec-1875">Driv Licences
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1875">Driv Licences</span></span> 
- <span data-ttu-id="ab3ec-1876">Driv Lic
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1876">Driv Lic</span></span> 
- <span data-ttu-id="ab3ec-1877">Driver Licen
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1877">Driver Licen</span></span> 
- <span data-ttu-id="ab3ec-1878">Driver de licença</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1878">Driver License</span></span> 
- <span data-ttu-id="ab3ec-1879">Licenças de driver</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1879">Driver Licenses</span></span> 
- <span data-ttu-id="ab3ec-1880">Driver Licence
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1880">Driver Licence</span></span> 
- <span data-ttu-id="ab3ec-1881">Driver Licences
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1881">Driver Licences</span></span> 
- <span data-ttu-id="ab3ec-1882">Drivers Lic</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1882">Drivers Lic</span></span> 
- <span data-ttu-id="ab3ec-1883">Drivers Licen</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1883">Drivers Licen</span></span> 
- <span data-ttu-id="ab3ec-1884">Carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1884">Drivers License</span></span> 
- <span data-ttu-id="ab3ec-1885">Licenças de drivers</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1885">Drivers Licenses</span></span> 
- <span data-ttu-id="ab3ec-1886">Drivers de licença</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1886">Drivers Licence</span></span> 
- <span data-ttu-id="ab3ec-1887">Licenças de drivers</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1887">Drivers Licences</span></span> 
- <span data-ttu-id="ab3ec-1888">Lic do driver</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1888">Driver's Lic</span></span> 
- <span data-ttu-id="ab3ec-1889">Driver's Licen
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1889">Driver's Licen</span></span> 
- <span data-ttu-id="ab3ec-1890">De motorista carteira</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1890">Driver's License</span></span> 
- <span data-ttu-id="ab3ec-1891">Licenças de motorista</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1891">Driver's Licenses</span></span> 
- <span data-ttu-id="ab3ec-1892">Driver's Licence
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1892">Driver's Licence</span></span> 
- <span data-ttu-id="ab3ec-1893">Driver's Licences
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1893">Driver's Licences</span></span> 
- <span data-ttu-id="ab3ec-1894">Driving Lic
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1894">Driving Lic</span></span> 
- <span data-ttu-id="ab3ec-1895">Driving Licen
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1895">Driving Licen</span></span> 
- <span data-ttu-id="ab3ec-1896">Driving License
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1896">Driving License</span></span> 
- <span data-ttu-id="ab3ec-1897">Driving Licenses
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1897">Driving Licenses</span></span> 
- <span data-ttu-id="ab3ec-1898">Driving Licence

</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1898">Driving Licence</span></span> 
- <span data-ttu-id="ab3ec-1899">Driving Licences</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1899">Driving Licences</span></span>

#### <a name="keywordgermandriverslicensecollaborative"></a><span data-ttu-id="ab3ec-1900">Keyword_german_drivers_license_collaborative</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1900">Keyword_german_drivers_license_collaborative</span></span>

- <span data-ttu-id="ab3ec-1901">
Nr-Führerschein
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1901">Nr-Führerschein</span></span> 
- <span data-ttu-id="ab3ec-1902">Nr-Fuhrerschein
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1902">Nr-Fuhrerschein</span></span> 
- <span data-ttu-id="ab3ec-1903">Nr-Fuehrerschein
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1903">Nr-Fuehrerschein</span></span> 
- <span data-ttu-id="ab3ec-1904">No-Führerschein
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1904">No-Führerschein</span></span> 
- <span data-ttu-id="ab3ec-1905">No-Fuhrerschein
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1905">No-Fuhrerschein</span></span> 
- <span data-ttu-id="ab3ec-1906">No-Fuehrerschein
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1906">No-Fuehrerschein</span></span> 
- <span data-ttu-id="ab3ec-1907">N-Führerschein
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1907">N-Führerschein</span></span> 
- <span data-ttu-id="ab3ec-1908">N-Fuhrerschein
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1908">N-Fuhrerschein</span></span> 
- <span data-ttu-id="ab3ec-1909">N-Fuehrerschein</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1909">N-Fuehrerschein</span></span>
- <span data-ttu-id="ab3ec-1910">
Nr-Führerschein
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1910">Nr-Führerschein</span></span> 
- <span data-ttu-id="ab3ec-1911">Nr-Fuhrerschein
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1911">Nr-Fuhrerschein</span></span> 
- <span data-ttu-id="ab3ec-1912">Nr-Fuehrerschein
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1912">Nr-Fuehrerschein</span></span> 
- <span data-ttu-id="ab3ec-1913">No-Führerschein
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1913">No-Führerschein</span></span> 
- <span data-ttu-id="ab3ec-1914">No-Fuhrerschein
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1914">No-Fuhrerschein</span></span> 
- <span data-ttu-id="ab3ec-1915">No-Fuehrerschein
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1915">No-Fuehrerschein</span></span> 
- <span data-ttu-id="ab3ec-1916">N-Führerschein
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1916">N-Führerschein</span></span> 
- <span data-ttu-id="ab3ec-1917">N-Fuhrerschein
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1917">N-Fuhrerschein</span></span> 
- <span data-ttu-id="ab3ec-1918">N-Fuehrerschein</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1918">N-Fuehrerschein</span></span> 

#### <a name="keywordgermandriverslicense"></a><span data-ttu-id="ab3ec-1919">Keyword_german_drivers_license</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1919">Keyword_german_drivers_license</span></span>

- <span data-ttu-id="ab3ec-1920">ausstellungsdatum</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1920">ausstellungsdatum</span></span>
- <span data-ttu-id="ab3ec-1921">
ausstellungsort</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1921">ausstellungsort</span></span>
- <span data-ttu-id="ab3ec-1922">
ausstellende behöde</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1922">ausstellende behöde</span></span>
- <span data-ttu-id="ab3ec-1923">
ausstellende behorde</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1923">ausstellende behorde</span></span>
- <span data-ttu-id="ab3ec-1924">

ausstellende behoerde</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1924">ausstellende behoerde</span></span>
   
## <a name="german-passport-number"></a><span data-ttu-id="ab3ec-1925">Número de passaporte da Alemanha</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1925">German Passport Number</span></span>

### <a name="format"></a><span data-ttu-id="ab3ec-1926">Formato</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1926">Format</span></span>

<span data-ttu-id="ab3ec-1927">10 dígitos ou letras</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1927">10 digits or letters</span></span>

### <a name="pattern"></a><span data-ttu-id="ab3ec-1928">Padrão</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1928">Pattern</span></span>

<span data-ttu-id="ab3ec-1929">O padrão deve incluir todos os seguintes itens:</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1929">Pattern must include all of the following:</span></span>
- <span data-ttu-id="ab3ec-1930">Primeiro caractere é um dígito ou uma letra desse conjunto (C, F, G, H, J, K)</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1930">First character is a digit or a letter from this set (C, F, G, H, J, K)</span></span> 
- <span data-ttu-id="ab3ec-1931">Três dígitos</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1931">Three digits</span></span> 
- <span data-ttu-id="ab3ec-1932">Cinco dígitos ou letras a partir desse conjunto (C, -H, J N, P, R, T, V-Z)</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1932">Five digits or letters from this set (C, -H, J-N, P, R, T, V-Z)</span></span> 
- <span data-ttu-id="ab3ec-1933">Um dígito</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1933">A digit</span></span>

### <a name="checksum"></a><span data-ttu-id="ab3ec-1934">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1934">Checksum</span></span>

<span data-ttu-id="ab3ec-1935">Sim</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1935">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="ab3ec-1936">Definição</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1936">Definition</span></span>

<span data-ttu-id="ab3ec-1937">Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1937">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="ab3ec-1938">A função Func_german_passport localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1938">The function Func_german_passport finds content that matches the pattern.</span></span>
- <span data-ttu-id="ab3ec-1939">Uma palavra-chave de qualquer uma das cinco listas de palavras-chave for encontrada.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1939">A keyword from any of the five keyword lists is found.</span></span>
- <span data-ttu-id="ab3ec-1940">A soma de verificação passa.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1940">The checksum passes.</span></span>

<span data-ttu-id="ab3ec-1941">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1941">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="ab3ec-1942">A função Func_german_passport_data localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1942">The function Func_german_passport_data finds content that matches the pattern.</span></span>
- <span data-ttu-id="ab3ec-1943">Uma palavra-chave de qualquer uma das cinco listas de palavras-chave for encontrada.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1943">A keyword from any of the five keyword lists is found.</span></span>
- <span data-ttu-id="ab3ec-1944">A soma de verificação passa.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1944">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="ab3ec-1945">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1945">Keywords</span></span>

#### <a name="keywordgermanpassport"></a><span data-ttu-id="ab3ec-1946">Keyword_german_passport</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1946">Keyword_german_passport</span></span>

- <span data-ttu-id="ab3ec-1947">reisepass</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1947">reisepass</span></span>
- <span data-ttu-id="ab3ec-1948">
reisepasse</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1948">reisepasse</span></span>
- <span data-ttu-id="ab3ec-1949">
reisepassnummer</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1949">reisepassnummer</span></span>
- <span data-ttu-id="ab3ec-1950">passport</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1950">passport</span></span>
- <span data-ttu-id="ab3ec-1951">

passports</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1951">passports</span></span>

#### <a name="keywordgermanpassportcollaborative"></a><span data-ttu-id="ab3ec-1952">Keyword_german_passport_collaborative</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1952">Keyword_german_passport_collaborative</span></span>

- <span data-ttu-id="ab3ec-1953">geburtsdatum</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1953">geburtsdatum</span></span>
- <span data-ttu-id="ab3ec-1954">ausstellungsdatum</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1954">ausstellungsdatum</span></span>
- <span data-ttu-id="ab3ec-1955">
ausstellungsort</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1955">ausstellungsort</span></span>

#### <a name="keywordgermanpassportnumber"></a><span data-ttu-id="ab3ec-1956">Keyword_german_passport_number</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1956">Keyword_german_passport_number</span></span>

<span data-ttu-id="ab3ec-1957">Não-Reisepass Nr-Reisepass</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1957">No-Reisepass Nr-Reisepass</span></span>

#### <a name="keywordgermanpassport1"></a><span data-ttu-id="ab3ec-1958">Keyword_german_passport1</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1958">Keyword_german_passport1</span></span>

<span data-ttu-id="ab3ec-1959">Reisepass-Nr
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1959">Reisepass-Nr</span></span>

#### <a name="keywordgermanpassport2"></a><span data-ttu-id="ab3ec-1960">Keyword_german_passport2</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1960">Keyword_german_passport2</span></span>

<span data-ttu-id="ab3ec-1961">bnationalit.t</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1961">bnationalit.t</span></span>
   
## <a name="germany-identity-card-number"></a><span data-ttu-id="ab3ec-1962">Número da carteira de identidade alemã</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1962">Germany Identity Card Number</span></span>

### <a name="format"></a><span data-ttu-id="ab3ec-1963">Formato</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1963">Format</span></span>

<span data-ttu-id="ab3ec-1964">Desde 1 de novembro de 2010: nove letras e dígitos</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1964">Since 1 November 2010: Nine letters and digits</span></span>

<span data-ttu-id="ab3ec-1965">De 1987 1 de abril até 31 dígitos 2010:10 de outubro</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1965">From 1 April 1987 until 31 October 2010: 10 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="ab3ec-1966">Padrão</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1966">Pattern</span></span>

<span data-ttu-id="ab3ec-1967">Desde 1º de novembro de 2010:</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1967">Since 1 November 2010:</span></span>
- <span data-ttu-id="ab3ec-1968">Uma letra (não diferencia maiúscula de minúscula)</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1968">One letter (not case sensitive)</span></span> 
- <span data-ttu-id="ab3ec-1969">Oito dígitos</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1969">Eight digits</span></span>

<span data-ttu-id="ab3ec-1970">De 1 de abril de 1987 até 31 de outubro de 2010:</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1970">From 1 April 1987 until 31 October 2010:</span></span>
- <span data-ttu-id="ab3ec-1971">10 dígitos</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1971">10 digits</span></span>

### <a name="checksum"></a><span data-ttu-id="ab3ec-1972">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1972">Checksum</span></span>

<span data-ttu-id="ab3ec-1973">Não</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1973">No</span></span>

### <a name="definition"></a><span data-ttu-id="ab3ec-1974">Definição</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1974">Definition</span></span>

<span data-ttu-id="ab3ec-1975">Uma política de DLP tem 65% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1975">A DLP policy is 65% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="ab3ec-1976">A expressão regular Regex_germany_id_card encontra o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1976">The regular expression Regex_germany_id_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="ab3ec-1977">Uma palavra-chave de Keyword_germany_id_card é encontrada.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1977">A keyword from Keyword_germany_id_card is found.</span></span>

```
<!-- Germany Identity Card Number -->
<Entity id="e577372f-c42e-47a0-9d85-bebed1c237d4" recommendedConfidence="65" patternsProximity="300">
  <Pattern confidenceLevel="65">
     <IdMatch idRef="Regex_germany_id_card"/>
     <Match idRef="Keyword_germany_id_card"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="ab3ec-1978">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1978">Keywords</span></span>

#### <a name="keywordgermanyidcard"></a><span data-ttu-id="ab3ec-1979">Keyword_germany_id_card</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1979">Keyword_germany_id_card</span></span>

- <span data-ttu-id="ab3ec-1980">Cartão de Identidade</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1980">Identity Card</span></span>
- <span data-ttu-id="ab3ec-1981">ID</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1981">ID</span></span>
- <span data-ttu-id="ab3ec-1982">Identificação </span><span class="sxs-lookup"><span data-stu-id="ab3ec-1982">Identification</span></span>
- <span data-ttu-id="ab3ec-1983">Personalausweis</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1983">Personalausweis</span></span>
- <span data-ttu-id="ab3ec-1984">Identifizierungsnummer</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1984">Identifizierungsnummer</span></span>
- <span data-ttu-id="ab3ec-1985">Ausweis</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1985">Ausweis</span></span>
- <span data-ttu-id="ab3ec-1986">Identifikation</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1986">Identifikation</span></span>
   
## <a name="greece-national-id-card"></a><span data-ttu-id="ab3ec-1987">Cartão de Identificação Nacional da Grécia</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1987">Greece National ID Card</span></span>

### <a name="format"></a><span data-ttu-id="ab3ec-1988">Formato</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1988">Format</span></span>

<span data-ttu-id="ab3ec-1989">Combinação de 7 a 8 letras e números mais um traço</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1989">Combination of 7-8 letters and numbers plus a dash</span></span>

### <a name="pattern"></a><span data-ttu-id="ab3ec-1990">Padrão</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1990">Pattern</span></span>

<span data-ttu-id="ab3ec-1991">Sete letras e números (formato antigo):</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1991">Seven letters and numbers (old format):</span></span>
- <span data-ttu-id="ab3ec-1992">Uma letra (qualquer letra do alfabeto grego) </span><span class="sxs-lookup"><span data-stu-id="ab3ec-1992">One letter (any letter of the Greek alphabet)</span></span> 
- <span data-ttu-id="ab3ec-1993">Um traço</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1993">A dash</span></span> 
- <span data-ttu-id="ab3ec-1994">Seis dígitos</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1994">Six digits</span></span>

<span data-ttu-id="ab3ec-1995">Oito letras e números (novo formato):</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1995">Eight letters and numbers (new format):</span></span>
- <span data-ttu-id="ab3ec-1996">Duas letras cujos caracteres maiúsculos ocorre em alfabetos latino e grego (ABEZHIKMNOPTYX) </span><span class="sxs-lookup"><span data-stu-id="ab3ec-1996">Two letters whose uppercase character occurs in both the Greek and Latin alphabets (ABEZHIKMNOPTYX)</span></span> 
- <span data-ttu-id="ab3ec-1997">Um traço</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1997">A dash</span></span> 
- <span data-ttu-id="ab3ec-1998">Seis dígitos</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1998">Six digits</span></span>

### <a name="checksum"></a><span data-ttu-id="ab3ec-1999">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="ab3ec-1999">Checksum</span></span>

<span data-ttu-id="ab3ec-2000">Não</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2000">No</span></span>

### <a name="definition"></a><span data-ttu-id="ab3ec-2001">Definição</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2001">Definition</span></span>

<span data-ttu-id="ab3ec-2002">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2002">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="ab3ec-2003">A expressão regular Regex_greece_id_card encontra o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2003">The regular expression Regex_greece_id_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="ab3ec-2004">Uma palavra-chave de Keyword_greece_id_card é encontrada.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2004">A keyword from Keyword_greece_id_card is found.</span></span>

```
<!-- Greece National ID Card -->
<Entity id="82568215-1da1-46d3-874a-d2294d81b5ac" recommendedConfidence="85" patternsProximity="300">
  <Pattern confidenceLevel="85">
     <IdMatch idRef="Regex_greece_id_card"/>
     <Match idRef="Keyword_greece_id_card"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="ab3ec-2005">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2005">Keywords</span></span>

#### <a name="keywordgreeceidcard"></a><span data-ttu-id="ab3ec-2006">Keyword_greece_id_card</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2006">Keyword_greece_id_card</span></span>

- <span data-ttu-id="ab3ec-2007">Cartão de identidade grego</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2007">Greek identity Card</span></span>
- <span data-ttu-id="ab3ec-2008">Tautotita</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2008">Tautotita</span></span>
- <span data-ttu-id="ab3ec-2009">Δελτίο αστυνομικής ταυτότητας</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2009">Δελτίο αστυνομικής ταυτότητας</span></span>
- <span data-ttu-id="ab3ec-2010">Ταυτότητα</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2010">Ταυτότητα</span></span>
   
## <a name="hong-kong-identity-card-hkid-number"></a><span data-ttu-id="ab3ec-2011">Número do Cartão de Identidade de Hong Kong (HKID)</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2011">Hong Kong Identity Card (HKID) Number</span></span>

### <a name="format"></a><span data-ttu-id="ab3ec-2012">Formato</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2012">Format</span></span>

<span data-ttu-id="ab3ec-2013">Combinação de 8 a 9 letras e números mais parênteses opcionais ao redor do caractere final</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2013">Combination of 8-9 letters and numbers plus optional parentheses around the final character</span></span>

### <a name="pattern"></a><span data-ttu-id="ab3ec-2014">Padrão</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2014">Pattern</span></span>

<span data-ttu-id="ab3ec-2015">Combinação de 8 a 9 letras:</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2015">Combination of 8-9 letters:</span></span>
- <span data-ttu-id="ab3ec-2016">1 a 2 letras (não diferenciam maiúsculas de minúsculas)</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2016">1-2 letters (not case sensitive)</span></span> 
- <span data-ttu-id="ab3ec-2017">Seis dígitos</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2017">Six digits</span></span> 
- <span data-ttu-id="ab3ec-2018">O caractere final (qualquer dígito ou a letra A), que é o dígito de verificação e é opcionalmente colocado entre parênteses.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2018">The final character (any digit or the letter A), which is the check digit and is optionally enclosed in parentheses.</span></span>

### <a name="checksum"></a><span data-ttu-id="ab3ec-2019">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2019">Checksum</span></span>

<span data-ttu-id="ab3ec-2020">Sim</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2020">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="ab3ec-2021">Definição</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2021">Definition</span></span>

<span data-ttu-id="ab3ec-2022">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2022">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="ab3ec-2023">A função Func_hong_kong_id_card encontra o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2023">The function Func_hong_kong_id_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="ab3ec-2024">Uma palavra-chave de Keyword_hong_kong_id_card é encontrada.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2024">A keyword from Keyword_hong_kong_id_card is found.</span></span>
- <span data-ttu-id="ab3ec-2025">A soma de verificação passa.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2025">The checksum passes.</span></span>

<span data-ttu-id="ab3ec-2026">Uma política de DLP tem 65% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2026">A DLP policy is 65% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="ab3ec-2027">A função Func_hong_kong_id_card encontra o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2027">The function Func_hong_kong_id_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="ab3ec-2028">A soma de verificação passa.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2028">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="ab3ec-2029">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2029">Keywords</span></span>

#### <a name="keywordhongkongidcard"></a><span data-ttu-id="ab3ec-2030">Keyword_hong_kong_id_card</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2030">Keyword_hong_kong_id_card</span></span>

- <span data-ttu-id="ab3ec-2031">Número do Cartão de Identidade de Hong Kong</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2031">Hong Kong Identity Card</span></span>
- <span data-ttu-id="ab3ec-2032">HKID</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2032">HKID</span></span>
- <span data-ttu-id="ab3ec-2033">Cartão de identificação</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2033">ID card</span></span>
- <span data-ttu-id="ab3ec-2034">香港身份證
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2034">香港身份證</span></span> 
- <span data-ttu-id="ab3ec-2035">香港永久性居民身份證
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2035">香港永久性居民身份證</span></span> 
   
## <a name="india-permanent-account-number-pan"></a><span data-ttu-id="ab3ec-2036">Número da Conta Permanente da Índia (PAN)</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2036">India Permanent Account Number (PAN)</span></span>

### <a name="format"></a><span data-ttu-id="ab3ec-2037">Formato</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2037">Format</span></span>

<span data-ttu-id="ab3ec-2038">10 letras ou dígitos</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2038">10 letters or digits</span></span>

### <a name="pattern"></a><span data-ttu-id="ab3ec-2039">Padrão</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2039">Pattern</span></span>

<span data-ttu-id="ab3ec-2040">10 letras ou dígitos.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2040">10 letters or digits:</span></span>
- <span data-ttu-id="ab3ec-2041">Cinco letras (não diferenciam maiúsculas de minúsculas)</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2041">Five letters (not case sensitive)</span></span> 
- <span data-ttu-id="ab3ec-2042">Quatro dígitos</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2042">Four digits</span></span> 
- <span data-ttu-id="ab3ec-2043">Uma letra que é um dígito de verificação alfabético</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2043">A letter which is an alphabetic check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="ab3ec-2044">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2044">Checksum</span></span>

<span data-ttu-id="ab3ec-2045">Sim</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2045">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="ab3ec-2046">Definição</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2046">Definition</span></span>

<span data-ttu-id="ab3ec-2047">Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2047">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="ab3ec-2048">A expressão regular Regex_india_permanent_account_number encontra o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2048">The regular expression Regex_india_permanent_account_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="ab3ec-2049">Uma palavra-chave de Keyword_india_permanent_account_number é encontrada.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2049">A keyword from Keyword_india_permanent_account_number is found.</span></span>
- <span data-ttu-id="ab3ec-2050">A soma de verificação passa.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2050">The checksum passes.</span></span>

```
<!-- India Permanent Account Number -->
<Entity id="2602bfee-9bb0-47a5-a7a6-2bf3053e2804" recommendedConfidence="85" patternsProximity="300">
  <Pattern confidenceLevel="85">
     <IdMatch idRef="Regex_india_permanent_account_number"/>
     <Match idRef="Keyword_india_permanent_account_number"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="ab3ec-2051">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2051">Keywords</span></span>

#### <a name="keywordindiapermanentaccountnumber"></a><span data-ttu-id="ab3ec-2052">Keyword_india_permanent_account_number</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2052">Keyword_india_permanent_account_number</span></span>

- <span data-ttu-id="ab3ec-2053">Número da Conta Permanente
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2053">Permanent Account Number</span></span> 
- <span data-ttu-id="ab3ec-2054">PAN
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2054">PAN</span></span> 
   
## <a name="india-unique-identification-aadhaar-number"></a><span data-ttu-id="ab3ec-2055">Número de Identificação Exclusivo da Índia (Aadhaar)</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2055">India Unique Identification (Aadhaar) Number</span></span>

### <a name="format"></a><span data-ttu-id="ab3ec-2056">Formato</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2056">Format</span></span>

<span data-ttu-id="ab3ec-2057">12 dígitos contendo espaços opcionais ou traços</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2057">12 digits containing optional spaces or dashes</span></span>

### <a name="pattern"></a><span data-ttu-id="ab3ec-2058">Padrão</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2058">Pattern</span></span>

<span data-ttu-id="ab3ec-2059">12 dígitos:</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2059">12 digits:</span></span>
- <span data-ttu-id="ab3ec-2060">Quatro dígitos</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2060">Four digits</span></span> 
- <span data-ttu-id="ab3ec-2061">Um espaço ou um traço opcional </span><span class="sxs-lookup"><span data-stu-id="ab3ec-2061">An optional space or dash</span></span> 
- <span data-ttu-id="ab3ec-2062">Quatro dígitos</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2062">Four digits</span></span> 
- <span data-ttu-id="ab3ec-2063">Um espaço ou um traço opcional </span><span class="sxs-lookup"><span data-stu-id="ab3ec-2063">An optional space or dash</span></span> 
- <span data-ttu-id="ab3ec-2064">O dígito final que é o dígito de verificação</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2064">The final digit which is the check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="ab3ec-2065">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2065">Checksum</span></span>

<span data-ttu-id="ab3ec-2066">Sim</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2066">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="ab3ec-2067">Definição</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2067">Definition</span></span>

<span data-ttu-id="ab3ec-p133">Uma política DLP é de 85% confiante de que detectou esse tipo de informações confidenciais if, dentro de uma proximidade de 300 caracteres: A função Func_india_aadhaar encontra o conteúdo que corresponde ao padrão. Uma palavra-chave de Keyword_india_aadhar é encontrada. A soma de verificação passa. Uma política de DLP é 75% confiante de que detectou esse tipo de informações confidenciais if, dentro de uma proximidade de 300 caracteres: A função Func_india_aadhaar encontra o conteúdo que corresponde ao padrão. A soma de verificação passa. <!-- India Unique Identification (Aadhaar) number -->
<Entity id="1ca46b29-76f5-4f46-9383-cfa15e91048f" recommendedConfidence="85" patternsProximity="300"> <Pattern confidenceLevel="85"> <IdMatch idRef="Func_india_aadhaar"/> <Match idRef="Keyword_india_aadhar"/> </Pattern> <Pattern confidenceLevel="75"> <IdMatch idRef="Func_india_aadhaar"/> </Pattern>
</Entity></span><span class="sxs-lookup"><span data-stu-id="ab3ec-p133">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters: The function Func_india_aadhaar finds content that matches the pattern. A keyword from Keyword_india_aadhar is found. The checksum passes. A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters: The function Func_india_aadhaar finds content that matches the pattern. The checksum passes. <!-- India Unique Identification (Aadhaar) number -->
<Entity id="1ca46b29-76f5-4f46-9383-cfa15e91048f" recommendedConfidence="85" patternsProximity="300"> <Pattern confidenceLevel="85"> <IdMatch idRef="Func_india_aadhaar"/> <Match idRef="Keyword_india_aadhar"/> </Pattern> <Pattern confidenceLevel="75"> <IdMatch idRef="Func_india_aadhaar"/> </Pattern>
</Entity></span></span>

### <a name="keywords"></a><span data-ttu-id="ab3ec-2074">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2074">Keywords</span></span>
   
#### <a name="keywordindiaaadhar"></a><span data-ttu-id="ab3ec-2075">Keyword_india_aadhar</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2075">Keyword_india_aadhar</span></span>
- <span data-ttu-id="ab3ec-2076">Aadhar</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2076">Aadhar</span></span>
- <span data-ttu-id="ab3ec-2077">Aadhaar</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2077">Aadhaar</span></span>
- <span data-ttu-id="ab3ec-2078">UID</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2078">UID</span></span>
- <span data-ttu-id="ab3ec-2079">आधार</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2079">आधार</span></span>
   
## <a name="indonesia-identity-card-ktp-number"></a><span data-ttu-id="ab3ec-2080">Número do Cartão de Identidade da Indonésia (KTP)</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2080">Indonesia Identity Card (KTP) Number</span></span>

### <a name="format"></a><span data-ttu-id="ab3ec-2081">Formato</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2081">Format</span></span>

<span data-ttu-id="ab3ec-2082">16 dígitos contendo pontos opcionais</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2082">16 digits containing optional periods</span></span>

### <a name="pattern"></a><span data-ttu-id="ab3ec-2083">Padrão</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2083">Pattern</span></span>

<span data-ttu-id="ab3ec-2084">16 dígitos:</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2084">16 digits:</span></span>
- <span data-ttu-id="ab3ec-2085">Código de província de dois dígitos </span><span class="sxs-lookup"><span data-stu-id="ab3ec-2085">Two-digit province code</span></span> 
- <span data-ttu-id="ab3ec-2086">Um ponto (opcional) </span><span class="sxs-lookup"><span data-stu-id="ab3ec-2086">A period (optional)</span></span> 
- <span data-ttu-id="ab3ec-2087">Código de dois dígitos da regência ou da cidade </span><span class="sxs-lookup"><span data-stu-id="ab3ec-2087">Two-digit regency or city code</span></span> 
- <span data-ttu-id="ab3ec-2088">Código de dois dígitos do subdistrito </span><span class="sxs-lookup"><span data-stu-id="ab3ec-2088">Two-digit subdistrict code</span></span> 
- <span data-ttu-id="ab3ec-2089">Um ponto (opcional) </span><span class="sxs-lookup"><span data-stu-id="ab3ec-2089">A period (optional)</span></span> 
- <span data-ttu-id="ab3ec-2090">Seis dígitos no formato DDMMAA que são a data de nascimento</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2090">Six digits in the format DDMMYY which are the date of birth</span></span> 
- <span data-ttu-id="ab3ec-2091">Um ponto (opcional) </span><span class="sxs-lookup"><span data-stu-id="ab3ec-2091">A period (optional)</span></span> 
- <span data-ttu-id="ab3ec-2092">Quatro dígitos</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2092">Four digits</span></span>

### <a name="checksum"></a><span data-ttu-id="ab3ec-2093">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2093">Checksum</span></span>

<span data-ttu-id="ab3ec-2094">Não</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2094">No</span></span>

### <a name="definition"></a><span data-ttu-id="ab3ec-2095">Definição</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2095">Definition</span></span>

<span data-ttu-id="ab3ec-2096">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2096">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="ab3ec-2097">A expressão regular Regex_indonesia_id_card encontra o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2097">The regular expression Regex_indonesia_id_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="ab3ec-2098">Uma palavra-chave de Keyword_indonesia_id_card é encontrada.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2098">A keyword from Keyword_indonesia_id_card is found.</span></span>

<span data-ttu-id="ab3ec-2099">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2099">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="ab3ec-2100">A expressão regular Regex_indonesia_id_card encontra o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2100">The regular expression Regex_indonesia_id_card finds content that matches the pattern.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="ab3ec-2101">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2101">Keywords</span></span>
   
#### <a name="keywordindonesiaidcard"></a><span data-ttu-id="ab3ec-2102">Keyword_indonesia_id_card</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2102">Keyword_indonesia_id_card</span></span>

- <span data-ttu-id="ab3ec-2103">KTP</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2103">KTP</span></span>
- <span data-ttu-id="ab3ec-2104">Kartu Tanda Penduduk
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2104">Kartu Tanda Penduduk</span></span> 
- <span data-ttu-id="ab3ec-2105">Nomor Induk Kependudukan
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2105">Nomor Induk Kependudukan</span></span> 
   
## <a name="international-banking-account-number-iban"></a><span data-ttu-id="ab3ec-2106">Número da Conta Bancária Internacional (IBAN)</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2106">International Banking Account Number (IBAN)</span></span>

### <a name="format"></a><span data-ttu-id="ab3ec-2107">Formato</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2107">Format</span></span>

<span data-ttu-id="ab3ec-2108">Verificar o código de país (duas letras) mais dígitos (dois dígitos) plus /bbO número (até 30 caracteres)</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2108">Country code (two letters) plus check digits (two digits) plus bban number (up to 30 characters)</span></span>

### <a name="pattern"></a><span data-ttu-id="ab3ec-2109">Padrão</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2109">Pattern</span></span>

<span data-ttu-id="ab3ec-2110">O padrão deve incluir todos os seguintes itens:</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2110">Pattern must include all of the following:</span></span>

- <span data-ttu-id="ab3ec-2111">Código de país com duas letras</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2111">Two-letter country code</span></span>
- <span data-ttu-id="ab3ec-2112">Dois dígitos de verificação (seguidos por um espaço opcional)</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2112">Two check digits (followed by an optional space)</span></span> 
- <span data-ttu-id="ab3ec-2113">grupos de 1 a 7 de quatro letras ou dígitos (pode ser separada por espaços)</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2113">1-7 groups of four letters or digits (can be separated by spaces)</span></span>
- <span data-ttu-id="ab3ec-2114">1 a 3 letras ou dígitos</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2114">1-3 letters or digits</span></span>

<span data-ttu-id="ab3ec-p134">O formato para cada país é ligeiramente diferente. O tipo de informações confidenciais IBAN aborda essas 60 países:</span><span class="sxs-lookup"><span data-stu-id="ab3ec-p134">The format for each country is slightly different. The IBAN sensitive information type covers these 60 countries:</span></span>

<span data-ttu-id="ab3ec-2117">AD, ae, al, at, az, ba, ser, bg, bbH, ESC, cr, cy, cz, de, dk, execute, ee, es, fi, fo, fr, gb, ge, gi, gl, GA, RH, hu, isto é, il, há, ele, kw, kz, lb, li, lt, lu, lv, mc, md, me, mk, mr, mt, mu , nl, não pl, pt, LIN, rs, sa, se, si, sk, sm, tn, tr, vg</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2117">ad, ae, al, at, az, ba, be, bg, bh, ch, cr, cy, cz, de, dk, do, ee, es, fi, fo, fr, gb, ge, gi, gl, gr, hr, hu, ie, il, is, it, kw, kz, lb, li, lt, lu, lv, mc, md, me, mk, mr, mt, mu, nl, no, pl, pt, ro, rs, sa, se, si, sk, sm, tn, tr, vg</span></span>

### <a name="checksum"></a><span data-ttu-id="ab3ec-2118">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2118">Checksum</span></span>

<span data-ttu-id="ab3ec-2119">Sim</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2119">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="ab3ec-2120">Definição</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2120">Definition</span></span>

<span data-ttu-id="ab3ec-2121">Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2121">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="ab3ec-2122">A função Func_iban localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2122">The function Func_iban finds content that matches the pattern.</span></span>
- <span data-ttu-id="ab3ec-2123">A soma de verificação passa.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2123">The checksum passes.</span></span>

```
<Entity id="e7dc4711-11b7-4cb0-b88b-2c394a771f0e" patternsProximity="300" recommendedConfidence="85">
  <Pattern confidenceLevel="85">
        <IdMatch idRef="Func_iban" />
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="ab3ec-2124">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2124">Keywords</span></span>

<span data-ttu-id="ab3ec-2125">Nenhum</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2125">None</span></span>

   
## <a name="ip-address"></a><span data-ttu-id="ab3ec-2126">Endereço IP</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2126">IP Address</span></span>

### <a name="format"></a><span data-ttu-id="ab3ec-2127">Formato</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2127">Format</span></span>

#### <a name="ipv4"></a><span data-ttu-id="ab3ec-2128">IPv4:</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2128">IPv4:</span></span>
<span data-ttu-id="ab3ec-2129">Padrão complexo que é responsável por versões formatadas (pontos) e não formatadas (sem pontos) dos endereços IPv4</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2129">Complex pattern which accounts for formatted (periods) and unformatted (no periods) versions of the IPv4 addresses</span></span>

#### <a name="ipv6"></a><span data-ttu-id="ab3ec-2130">IPv6:</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2130">IPv6:</span></span>
<span data-ttu-id="ab3ec-2131">Padrão complexo que é responsável por números IPv6 formatados (que incluem dois pontos)</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2131">Complex pattern which accounts for formatted IPv6 numbers (which include colons)</span></span>

### <a name="pattern"></a><span data-ttu-id="ab3ec-2132">Padrão</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2132">Pattern</span></span>

### <a name="checksum"></a><span data-ttu-id="ab3ec-2133">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2133">Checksum</span></span>

<span data-ttu-id="ab3ec-2134">Não</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2134">No</span></span>

### <a name="definition"></a><span data-ttu-id="ab3ec-2135">Definição</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2135">Definition</span></span>

<span data-ttu-id="ab3ec-2136">Para IPv6, uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2136">For IPv6, a DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="ab3ec-2137">A expressão regular Regex_ipv6_address localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2137">The regular expression Regex_ipv6_address finds content that matches the pattern.</span></span>
- <span data-ttu-id="ab3ec-2138">Nenhuma palavra-chave de Keyword_ipaddress for encontrada.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2138">No keyword from Keyword_ipaddress is found.</span></span>

<span data-ttu-id="ab3ec-2139">Para IPv4, uma política de DLP tem 95% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2139">For IPv4, a DLP policy is 95% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="ab3ec-2140">A expressão regular Regex_ipv4_address localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2140">The regular expression Regex_ipv4_address finds content that matches the pattern.</span></span>
- <span data-ttu-id="ab3ec-2141">Uma palavra-chave de Keyword_ipaddress for encontrada.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2141">A keyword from Keyword_ipaddress is found.</span></span>

<span data-ttu-id="ab3ec-2142">Para IPv6, uma política de DLP tem 95% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2142">For IPv6, a DLP policy is 95% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="ab3ec-2143">A expressão regular Regex_ipv6_address localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2143">The regular expression Regex_ipv6_address finds content that matches the pattern.</span></span>
- <span data-ttu-id="ab3ec-2144">Nenhuma palavra-chave de Keyword_ipaddress for encontrada.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2144">No keyword from Keyword_ipaddress is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="ab3ec-2145">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2145">Keywords</span></span>

#### <a name="keywordipaddress"></a><span data-ttu-id="ab3ec-2146">Keyword_ipaddress</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2146">Keyword_ipaddress</span></span>

- <span data-ttu-id="ab3ec-2147">IP (esta palavra-chave diferencia maiúsculas de minúsculas)</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2147">IP (this keyword is case sensitive)</span></span>
- <span data-ttu-id="ab3ec-2148">ip address
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2148">ip address</span></span> 
- <span data-ttu-id="ab3ec-2149">endereços ip</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2149">ip addresses</span></span>
- <span data-ttu-id="ab3ec-2150">internet protocol</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2150">internet protocol</span></span>
- <span data-ttu-id="ab3ec-2151">
IP כתובת ה
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2151">IP-כתובת ה</span></span> 
   
## <a name="international-classification-of-diseases-icd-10-cm"></a><span data-ttu-id="ab3ec-2152">Classificação internacional de doenças (ICD-10-CM)</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2152">International Classification of Diseases (ICD-10-CM)</span></span>

### <a name="format"></a><span data-ttu-id="ab3ec-2153">Formato</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2153">Format</span></span>

<span data-ttu-id="ab3ec-2154">Dicionário</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2154">Dictionary</span></span>

### <a name="pattern"></a><span data-ttu-id="ab3ec-2155">Padrão</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2155">Pattern</span></span>

<span data-ttu-id="ab3ec-2156">Palavra-chave</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2156">Keyword</span></span>

### <a name="checksum"></a><span data-ttu-id="ab3ec-2157">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2157">Checksum</span></span>

<span data-ttu-id="ab3ec-2158">Não</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2158">No</span></span>

### <a name="definition"></a><span data-ttu-id="ab3ec-2159">Definição</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2159">Definition</span></span>

<span data-ttu-id="ab3ec-2160">Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2160">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="ab3ec-2161">Uma palavra-chave de Dictionary_icd_10_cm é encontrada.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2161">A keyword from Dictionary_icd_10_cm is found.</span></span>

```
      <!-- ICD-10 CM -->
      <Entity id="3356946c-6bb7-449b-b253-6ffa419c0ce7" patternsProximity="300" recommendedConfidence="85">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Dictionary_icd_10_cm" />
        </Pattern>
      </Entity>
```

<span data-ttu-id="ab3ec-2162">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2162">Keywords</span></span>

<span data-ttu-id="ab3ec-p135">Qualquer termo do dicionário Dictionary_icd_10_cm palavra-chave, que é baseada na [classificação de internacional de doenças, décimo revisão, a modificação de início de estudos clínicos (ICD-10-CM)](https://go.microsoft.com/fwlink/?linkid=852604). Esse tipo de procura apenas o termo, e não os códigos de seguros.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-p135">Any term from the Dictionary_icd_10_cm keyword dictionary, which is based on the [International Classification of Diseases, Tenth Revision, Clinical Modification (ICD-10-CM)](https://go.microsoft.com/fwlink/?linkid=852604). This type looks only for the term, not the insurance codes.</span></span>

   
## <a name="international-classification-of-diseases-icd-9-cm"></a><span data-ttu-id="ab3ec-2165">Classificação internacional de doenças (ICD-9-CM)</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2165">International Classification of Diseases (ICD-9-CM)</span></span>

### <a name="format"></a><span data-ttu-id="ab3ec-2166">Formato</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2166">Format</span></span>

<span data-ttu-id="ab3ec-2167">Dicionário</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2167">Dictionary</span></span>

### <a name="pattern"></a><span data-ttu-id="ab3ec-2168">Padrão</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2168">Pattern</span></span>

<span data-ttu-id="ab3ec-2169">Palavra-chave</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2169">Keyword</span></span>

### <a name="checksum"></a><span data-ttu-id="ab3ec-2170">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2170">Checksum</span></span>

<span data-ttu-id="ab3ec-2171">Não</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2171">No</span></span>

### <a name="definition"></a><span data-ttu-id="ab3ec-2172">Definição</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2172">Definition</span></span>

<span data-ttu-id="ab3ec-2173">Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2173">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="ab3ec-2174">Uma palavra-chave de Dictionary_icd_9_cm é encontrada.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2174">A keyword from Dictionary_icd_9_cm is found.</span></span>

```
      <Entity id="fa3f9c74-ee07-4c52-b5f2-085d6b2c0ec4" patternsProximity="300" recommendedConfidence="85">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Dictionary_icd_9_cm" />
        </Pattern>
      </Entity>
```

### <a name="keywords"></a><span data-ttu-id="ab3ec-2175">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2175">Keywords</span></span>

<span data-ttu-id="ab3ec-p136">Qualquer termo do dicionário Dictionary_icd_9_cm palavra-chave, que é baseada na [classificação de internacional de doenças, nono revisão, a modificação de início de estudos clínicos (ICD-9-CM)](https://go.microsoft.com/fwlink/?linkid=852605). Esse tipo de procura apenas o termo, e não os códigos de seguros.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-p136">Any term from the Dictionary_icd_9_cm keyword dictionary, which is based on the [International Classification of Diseases,Ninth Revision, Clinical Modification (ICD-9-CM)](https://go.microsoft.com/fwlink/?linkid=852605). This type looks only for the term, not the insurance codes.</span></span>
   
## <a name="ireland-personal-public-service-pps-number"></a><span data-ttu-id="ab3ec-2178">Número de Serviço Público Pessoal (PPS) da Irlanda</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2178">Ireland Personal Public Service (PPS) Number</span></span>

### <a name="format"></a><span data-ttu-id="ab3ec-2179">Formato</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2179">Format</span></span>

<span data-ttu-id="ab3ec-2180">Formato antigo (até 31 de dezembro de 2012):</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2180">Old format (until 31 Dec 2012):</span></span>
- <span data-ttu-id="ab3ec-2181">Sete dígitos seguidos de 1 a 2 letras </span><span class="sxs-lookup"><span data-stu-id="ab3ec-2181">Seven digits followed by 1-2 letters</span></span> 

<span data-ttu-id="ab3ec-2182">Novo formato (1 de janeiro de 2013 e depois):</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2182">New format (1 Jan 2013 and after):</span></span>
- <span data-ttu-id="ab3ec-2183">Sete dígitos seguidos de duas letras</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2183">Seven digits followed by two letters</span></span>

### <a name="pattern"></a><span data-ttu-id="ab3ec-2184">Padrão</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2184">Pattern</span></span>

<span data-ttu-id="ab3ec-2185">Formato antigo (até 31 de dezembro de 2012):</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2185">Old format (until 31 Dec 2012):</span></span>
- <span data-ttu-id="ab3ec-2186">Sete dígitos </span><span class="sxs-lookup"><span data-stu-id="ab3ec-2186">Seven digits</span></span> 
- <span data-ttu-id="ab3ec-2187">1 a 2 letras (não diferenciam maiúsculas de minúsculas)</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2187">1-2 letters (not case sensitive)</span></span> 

<span data-ttu-id="ab3ec-2188">Novo formato (1 de janeiro de 2013 e depois):</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2188">New format (1 Jan 2013 and after):</span></span>
- <span data-ttu-id="ab3ec-2189">Sete dígitos </span><span class="sxs-lookup"><span data-stu-id="ab3ec-2189">Seven digits</span></span> 
- <span data-ttu-id="ab3ec-2190">Uma letra (não diferencia maiúsculas de minúsculas) que é um dígito de verificação alfabético </span><span class="sxs-lookup"><span data-stu-id="ab3ec-2190">A letter (not case sensitive) which is an alphabetic check digit</span></span> 
- <span data-ttu-id="ab3ec-2191">A letra "A" ou "H" (não diferencia maiúsculas de minúsculas)</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2191">The letter "A" or "H" (not case sensitive)</span></span>

### <a name="checksum"></a><span data-ttu-id="ab3ec-2192">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2192">Checksum</span></span>

<span data-ttu-id="ab3ec-2193">Sim</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2193">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="ab3ec-2194">Definição</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2194">Definition</span></span>

<span data-ttu-id="ab3ec-2195">Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2195">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="ab3ec-2196">A função Func_ireland_pps encontra o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2196">The function Func_ireland_pps finds content that matches the pattern.</span></span>
- <span data-ttu-id="ab3ec-2197">Uma das seguintes opções for verdadeira:</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2197">One of the following is true:</span></span>
    - <span data-ttu-id="ab3ec-2198">Uma palavra-chave de Keyword_ireland_pps é encontrada.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2198">A keyword from Keyword_ireland_pps is found.</span></span>
    - <span data-ttu-id="ab3ec-2199">A função Func_eu_date encontra uma data no formato de data à direita.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2199">The function Func_eu_date finds a date in the right date format.</span></span>
- <span data-ttu-id="ab3ec-2200">A soma de verificação passa.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2200">The checksum passes.</span></span>

<span data-ttu-id="ab3ec-2201">Uma política de DLP tem 65% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2201">A DLP policy is 65% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="ab3ec-2202">A função Func_ireland_pps encontra o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2202">The function Func_ireland_pps finds content that matches the pattern.</span></span>
- <span data-ttu-id="ab3ec-2203">A soma de verificação passa.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2203">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="ab3ec-2204">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2204">Keywords</span></span>

#### <a name="keywordirelandpps"></a><span data-ttu-id="ab3ec-2205">Keyword_ireland_pps</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2205">Keyword_ireland_pps</span></span>

- <span data-ttu-id="ab3ec-2206">Número do Serviço Público Pessoal 
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2206">Personal Public Service Number</span></span> 
- <span data-ttu-id="ab3ec-2207">Número PPS
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2207">PPS Number</span></span> 
- <span data-ttu-id="ab3ec-2208">Núm PPS
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2208">PPS Num</span></span> 
- <span data-ttu-id="ab3ec-2209">Nº PPS
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2209">PPS No.</span></span> 
- <span data-ttu-id="ab3ec-2210"># PPS
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2210">PPS #</span></span> 
- <span data-ttu-id="ab3ec-2211">#PPS
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2211">PPS#</span></span> 
- <span data-ttu-id="ab3ec-2212">NPPS
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2212">PPSN</span></span> 
- <span data-ttu-id="ab3ec-2213">Cartão dos Serviços Públicos
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2213">Public Services Card</span></span> 
- <span data-ttu-id="ab3ec-2214">Uimhir Phearsanta Seirbhíse Poiblí
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2214">Uimhir Phearsanta Seirbhíse Poiblí</span></span> 
- <span data-ttu-id="ab3ec-p137">Uimh. PSP
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-p137">Uimh. PSP</span></span> 
- <span data-ttu-id="ab3ec-2217">PSP
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2217">PSP</span></span> 
   
## <a name="israel-bank-account-number"></a><span data-ttu-id="ab3ec-2218">Número de conta bancária de Israel</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2218">Israel Bank Account Number</span></span>

### <a name="format"></a><span data-ttu-id="ab3ec-2219">Formato</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2219">Format</span></span>

<span data-ttu-id="ab3ec-2220">13 dígitos</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2220">13 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="ab3ec-2221">Padrão</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2221">Pattern</span></span>

<span data-ttu-id="ab3ec-2222">Formatado:</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2222">Formatted:</span></span>
- <span data-ttu-id="ab3ec-2223">Dois dígitos</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2223">Two digits</span></span> 
- <span data-ttu-id="ab3ec-2224">Um traço</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2224">A dash</span></span> 
- <span data-ttu-id="ab3ec-2225">Três dígitos</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2225">Three digits</span></span> 
- <span data-ttu-id="ab3ec-2226">Um traço</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2226">A dash</span></span> 
- <span data-ttu-id="ab3ec-2227">Oito dígitos</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2227">Eight digits</span></span>

<span data-ttu-id="ab3ec-2228">Não Formatado:</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2228">Unformatted:</span></span>
- <span data-ttu-id="ab3ec-2229">13 dígitos consecutivos</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2229">13 consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="ab3ec-2230">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2230">Checksum</span></span>

<span data-ttu-id="ab3ec-2231">Não</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2231">No</span></span>

### <a name="definition"></a><span data-ttu-id="ab3ec-2232">Definição</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2232">Definition</span></span>

<span data-ttu-id="ab3ec-2233">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2233">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="ab3ec-2234">A expressão regular Regex_israel_bank_account_number localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2234">The regular expression Regex_israel_bank_account_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="ab3ec-2235">Uma palavra-chave de Keyword_israel_bank_account_number for encontrada.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2235">A keyword from Keyword_israel_bank_account_number is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="ab3ec-2236">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2236">Keywords</span></span>

#### <a name="keywordisraelbankaccountnumber"></a><span data-ttu-id="ab3ec-2237">Keyword_israel_bank_account_number</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2237">Keyword_israel_bank_account_number</span></span>

- <span data-ttu-id="ab3ec-2238">Bank Account Number
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2238">Bank Account Number</span></span> 
- <span data-ttu-id="ab3ec-2239">Bank Account
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2239">Bank Account</span></span> 
- <span data-ttu-id="ab3ec-2240">Account Number
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2240">Account Number</span></span> 
- <span data-ttu-id="ab3ec-2241">מספר חשבון בנק
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2241">מספר חשבון בנק</span></span> 
   
## <a name="israel-national-id"></a><span data-ttu-id="ab3ec-2242">ID nacional de Israel</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2242">Israel National ID</span></span>

### <a name="format"></a><span data-ttu-id="ab3ec-2243">Formato</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2243">Format</span></span>

<span data-ttu-id="ab3ec-2244">Nove dígitos</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2244">Nine digits</span></span>

### <a name="pattern"></a><span data-ttu-id="ab3ec-2245">Padrão</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2245">Pattern</span></span>

<span data-ttu-id="ab3ec-2246">Nove dígitos consecutivos</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2246">Nine consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="ab3ec-2247">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2247">Checksum</span></span>

<span data-ttu-id="ab3ec-2248">Sim</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2248">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="ab3ec-2249">Definição</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2249">Definition</span></span>

<span data-ttu-id="ab3ec-2250">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2250">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="ab3ec-2251">A função Func_israeli_national_id_number localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2251">The function Func_israeli_national_id_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="ab3ec-2252">Uma palavra-chave de Keyword_Israel_National_ID for encontrada.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2252">A keyword from Keyword_Israel_National_ID is found.</span></span>
- <span data-ttu-id="ab3ec-2253">A soma de verificação passa.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2253">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="ab3ec-2254">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2254">Keywords</span></span>

#### <a name="keywordisraelnationalid"></a><span data-ttu-id="ab3ec-2255">Keyword_Israel_National_ID</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2255">Keyword_Israel_National_ID</span></span>

- <span data-ttu-id="ab3ec-2256">מספר זהות
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2256">מספר זהות</span></span> 
- <span data-ttu-id="ab3ec-2257">Número de identificação nacional</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2257">National ID Number</span></span>
   
## <a name="italy-drivers-license-number"></a><span data-ttu-id="ab3ec-2258">Número de carteira de motorista da Itália</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2258">Italy Driver's License Number</span></span>

### <a name="format"></a><span data-ttu-id="ab3ec-2259">Formato</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2259">Format</span></span>

<span data-ttu-id="ab3ec-2260">Uma combinação de 10 letras e dígitos</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2260">A combination of 10 letters and digits</span></span>

### <a name="pattern"></a><span data-ttu-id="ab3ec-2261">Padrão</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2261">Pattern</span></span>

- <span data-ttu-id="ab3ec-2262">Uma combinação de 10 letras e dígitos:</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2262">A combination of 10 letters and digits:</span></span>
- <span data-ttu-id="ab3ec-2263">Uma letra (não diferencia maiúscula de minúscula)</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2263">One letter (not case sensitive)</span></span> 
- <span data-ttu-id="ab3ec-2264">A letra "A" ou "V" (não diferencia maiúscula de minúscula)</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2264">The letter "A" or "V" (not case sensitive)</span></span> 
- <span data-ttu-id="ab3ec-2265">Sete letras (não diferenciam maiúsculas de minúsculas), dígitos ou o caractere de sublinhado</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2265">Seven letters (not case sensitive), digits, or the underscore character</span></span> 
- <span data-ttu-id="ab3ec-2266">Uma letra (não diferencia maiúscula de minúscula)</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2266">One letter (not case sensitive)</span></span>

### <a name="checksum"></a><span data-ttu-id="ab3ec-2267">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2267">Checksum</span></span>

<span data-ttu-id="ab3ec-2268">Não</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2268">No</span></span>

### <a name="definition"></a><span data-ttu-id="ab3ec-2269">Definição</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2269">Definition</span></span>

<span data-ttu-id="ab3ec-2270">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2270">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="ab3ec-2271">A expressão regular Regex_italy_drivers_license_number localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2271">The regular expression Regex_italy_drivers_license_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="ab3ec-2272">Uma palavra-chave de Keyword_italy_drivers_license_number for encontrada.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2272">A keyword from Keyword_italy_drivers_license_number is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="ab3ec-2273">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2273">Keywords</span></span>

#### <a name="keyworditalydriverslicensenumber"></a><span data-ttu-id="ab3ec-2274">Keyword_italy_drivers_license_number</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2274">Keyword_italy_drivers_license_number</span></span>

- <span data-ttu-id="ab3ec-2275">numero di patente di guida
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2275">numero di patente di guida</span></span> 
- <span data-ttu-id="ab3ec-2276">patente di guida
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2276">patente di guida</span></span> 
   
## <a name="japan-bank-account-number"></a><span data-ttu-id="ab3ec-2277">Número de conta bancária do Japão</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2277">Japan Bank Account Number</span></span>

### <a name="format"></a><span data-ttu-id="ab3ec-2278">Formato</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2278">Format</span></span>

<span data-ttu-id="ab3ec-2279">Sete ou oito dígitos</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2279">Seven or eight digits</span></span>

### <a name="pattern"></a><span data-ttu-id="ab3ec-2280">Padrão</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2280">Pattern</span></span>

<span data-ttu-id="ab3ec-2281">Número da Conta Bancária:</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2281">Bank account number:</span></span>
- <span data-ttu-id="ab3ec-2282">Sete ou oito dígitos</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2282">Seven or eight digits</span></span>
- <span data-ttu-id="ab3ec-2283">Código da agência de conta bancária:</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2283">Bank account branch code:</span></span>
- <span data-ttu-id="ab3ec-2284">Quatro dígitos</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2284">Four digits</span></span> 
- <span data-ttu-id="ab3ec-2285">Um espaço ou um traço (opcional)</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2285">A space or dash (optional)</span></span> 
- <span data-ttu-id="ab3ec-2286">Três dígitos</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2286">Three digits</span></span>

<span data-ttu-id="ab3ec-2287">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2287">Checksum</span></span>

<span data-ttu-id="ab3ec-2288">Não</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2288">No</span></span>

### <a name="definition"></a><span data-ttu-id="ab3ec-2289">Definição</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2289">Definition</span></span>

<span data-ttu-id="ab3ec-2290">Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2290">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="ab3ec-2291">A função Func_jp_bank_account localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2291">The function Func_jp_bank_account finds content that matches the pattern.</span></span>
- <span data-ttu-id="ab3ec-2292">Uma palavra-chave de Keyword_jp_bank_account for encontrada.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2292">A keyword from Keyword_jp_bank_account is found.</span></span>
- <span data-ttu-id="ab3ec-2293">Uma das seguintes opções for verdadeira:</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2293">One of the following is true:</span></span>
- <span data-ttu-id="ab3ec-2294">A função Func_jp_bank_account_branch_code localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2294">The function Func_jp_bank_account_branch_code finds content that matches the pattern.</span></span>
- <span data-ttu-id="ab3ec-2295">Uma palavra-chave de Keyword_jp_bank_branch_code for encontrada.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2295">A keyword from Keyword_jp_bank_branch_code is found.</span></span>

<span data-ttu-id="ab3ec-2296">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2296">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="ab3ec-2297">A função Func_jp_bank_account localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2297">The function Func_jp_bank_account finds content that matches the pattern.</span></span>
- <span data-ttu-id="ab3ec-2298">Uma palavra-chave de Keyword_jp_bank_account for encontrada.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2298">A keyword from Keyword_jp_bank_account is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="ab3ec-2299">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2299">Keywords</span></span>

#### <a name="keywordjpbankaccount"></a><span data-ttu-id="ab3ec-2300">Keyword_jp_bank_account</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2300">Keyword_jp_bank_account</span></span>

- <span data-ttu-id="ab3ec-2301">Checking Account Number
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2301">Checking Account Number</span></span> 
- <span data-ttu-id="ab3ec-2302">Checking Account
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2302">Checking Account</span></span> 
- <span data-ttu-id="ab3ec-2303">Checking Account #
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2303">Checking Account #</span></span> 
- <span data-ttu-id="ab3ec-2304">Checking Acct Number
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2304">Checking Acct Number</span></span> 
- <span data-ttu-id="ab3ec-2305">Checking Acct #
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2305">Checking Acct #</span></span> 
- <span data-ttu-id="ab3ec-2306">Checking Acct No.
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2306">Checking Acct No.</span></span> 
- <span data-ttu-id="ab3ec-2307">Checking Account No.
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2307">Checking Account No.</span></span> 
- <span data-ttu-id="ab3ec-2308">Bank Account Number
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2308">Bank Account Number</span></span> 
- <span data-ttu-id="ab3ec-2309">Bank Account
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2309">Bank Account</span></span> 
- <span data-ttu-id="ab3ec-2310">Bank Account #
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2310">Bank Account #</span></span> 
- <span data-ttu-id="ab3ec-2311">Bank Acct Number
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2311">Bank Acct Number</span></span> 
- <span data-ttu-id="ab3ec-2312">Bank Acct #
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2312">Bank Acct #</span></span> 
- <span data-ttu-id="ab3ec-2313">Bank Acct No.
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2313">Bank Acct No.</span></span> 
- <span data-ttu-id="ab3ec-2314">Bank Account No.
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2314">Bank Account No.</span></span> 
- <span data-ttu-id="ab3ec-2315">Savings Account Number
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2315">Savings Account Number</span></span> 
- <span data-ttu-id="ab3ec-2316">Conta de economia</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2316">Savings Account</span></span> 
- <span data-ttu-id="ab3ec-2317">Savings Account #
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2317">Savings Account #</span></span> 
- <span data-ttu-id="ab3ec-2318">Savings Acct Number
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2318">Savings Acct Number</span></span> 
- <span data-ttu-id="ab3ec-2319">Savings Acct #
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2319">Savings Acct #</span></span> 
- <span data-ttu-id="ab3ec-2320">Savings Acct No.
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2320">Savings Acct No.</span></span> 
- <span data-ttu-id="ab3ec-2321">Savings Account No.
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2321">Savings Account No.</span></span> 
- <span data-ttu-id="ab3ec-2322">Debit Account Number
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2322">Debit Account Number</span></span> 
- <span data-ttu-id="ab3ec-2323">Debit Account
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2323">Debit Account</span></span> 
- <span data-ttu-id="ab3ec-2324">Debit Account #
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2324">Debit Account #</span></span> 
- <span data-ttu-id="ab3ec-2325">Debit Acct Number
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2325">Debit Acct Number</span></span> 
- <span data-ttu-id="ab3ec-2326">Debit Acct #
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2326">Debit Acct #</span></span> 
- <span data-ttu-id="ab3ec-2327">Debit Acct No.
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2327">Debit Acct No.</span></span> 
- <span data-ttu-id="ab3ec-2328">Debit Account No.
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2328">Debit Account No.</span></span> 
- <span data-ttu-id="ab3ec-2329">口座番号を当座預金口座の確認
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2329">口座番号を当座預金口座の確認</span></span> 
- <span data-ttu-id="ab3ec-2330">＃アカウントの確認、勘定番号の確認
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2330">＃アカウントの確認、勘定番号の確認</span></span> 
- <span data-ttu-id="ab3ec-2331">＃勘定の確認
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2331">＃勘定の確認</span></span> 
- <span data-ttu-id="ab3ec-2332">勘定番号の確認
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2332">勘定番号の確認</span></span> 
- <span data-ttu-id="ab3ec-2333">口座番号の確認
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2333">口座番号の確認</span></span> 
- <span data-ttu-id="ab3ec-2334">銀行口座番号</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2334">銀行口座番号</span></span> 
- <span data-ttu-id="ab3ec-2335">銀行口座</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2335">銀行口座</span></span> 
- <span data-ttu-id="ab3ec-2336">銀行口座＃
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2336">銀行口座＃</span></span> 
- <span data-ttu-id="ab3ec-2337">銀行の勘定番号
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2337">銀行の勘定番号</span></span> 
- <span data-ttu-id="ab3ec-2338">銀行のacct＃
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2338">銀行のacct＃</span></span> 
- <span data-ttu-id="ab3ec-2339">銀行の勘定いいえ
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2339">銀行の勘定いいえ</span></span> 
- <span data-ttu-id="ab3ec-2340">銀行口座番号</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2340">銀行口座番号</span></span>
- <span data-ttu-id="ab3ec-2341">
普通預金口座番号
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2341">普通預金口座番号</span></span> 
- <span data-ttu-id="ab3ec-2342">預金口座
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2342">預金口座</span></span> 
- <span data-ttu-id="ab3ec-2343">貯蓄口座＃
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2343">貯蓄口座＃</span></span> 
- <span data-ttu-id="ab3ec-2344">貯蓄勘定の数
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2344">貯蓄勘定の数</span></span> 
- <span data-ttu-id="ab3ec-2345">貯蓄勘定＃
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2345">貯蓄勘定＃</span></span> 
- <span data-ttu-id="ab3ec-2346">貯蓄勘定番号
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2346">貯蓄勘定番号</span></span> 
- <span data-ttu-id="ab3ec-2347">普通預金口座番号
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2347">普通預金口座番号</span></span> 
- <span data-ttu-id="ab3ec-2348">引き落とし口座番号
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2348">引き落とし口座番号</span></span> 
- <span data-ttu-id="ab3ec-2349">口座番号</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2349">口座番号</span></span> 
- <span data-ttu-id="ab3ec-2350">口座番号＃
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2350">口座番号＃</span></span> 
- <span data-ttu-id="ab3ec-2351">デビットのacct番号
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2351">デビットのacct番号</span></span> 
- <span data-ttu-id="ab3ec-2352">デビット勘定＃
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2352">デビット勘定＃</span></span> 
- <span data-ttu-id="ab3ec-2353">デビットACCTの番号
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2353">デビットACCTの番号</span></span> 
- <span data-ttu-id="ab3ec-2354">デビット口座番号
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2354">デビット口座番号</span></span> 

#### <a name="keywordjpbankbranchcode"></a><span data-ttu-id="ab3ec-2355">Keyword_jp_bank_branch_code</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2355">Keyword_jp_bank_branch_code</span></span>

<span data-ttu-id="ab3ec-2356">Otemachi</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2356">Otemachi</span></span>

## <a name="japan-drivers-license-number"></a><span data-ttu-id="ab3ec-2357">Número de carteira de motorista do Japão</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2357">Japan Driver's License Number</span></span>

### <a name="format"></a><span data-ttu-id="ab3ec-2358">Formato</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2358">Format</span></span>

<span data-ttu-id="ab3ec-2359">12 dígitos</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2359">12 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="ab3ec-2360">Padrão</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2360">Pattern</span></span>

<span data-ttu-id="ab3ec-2361">12 dígitos consecutivos</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2361">12 consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="ab3ec-2362">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2362">Checksum</span></span>

<span data-ttu-id="ab3ec-2363">Não</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2363">No</span></span>

### <a name="definition"></a><span data-ttu-id="ab3ec-2364">Definição</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2364">Definition</span></span>

<span data-ttu-id="ab3ec-2365">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2365">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="ab3ec-2366">A função Func_jp_drivers_license_number localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2366">The function Func_jp_drivers_license_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="ab3ec-2367">Uma palavra-chave de Keyword_jp_drivers_license_number for encontrada.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2367">A keyword from Keyword_jp_drivers_license_number is found.</span></span>

```
<!-- Japan Driver's License Number -->
<Entity id="c6011143-d087-451c-8313-7f6d4aed2270" patternsProximity="300" recommendedConfidence="75">
    <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_jp_drivers_license_number" />
        <Match idRef ="Keyword_jp_drivers_license_number" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="ab3ec-2368">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2368">Keywords</span></span>

#### <a name="keywordjpdriverslicensenumber"></a><span data-ttu-id="ab3ec-2369">Keyword_jp_drivers_license_number</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2369">Keyword_jp_drivers_license_number</span></span>

- <span data-ttu-id="ab3ec-2370">dl#
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2370">dl#</span></span> 
- <span data-ttu-id="ab3ec-2371">DL #</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2371">DL＃</span></span> 
- <span data-ttu-id="ab3ec-2372">DLs #</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2372">dls#</span></span> 
- <span data-ttu-id="ab3ec-2373">DLS #</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2373">DLS＃</span></span> 
- <span data-ttu-id="ab3ec-2374">licença de driver</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2374">driver license</span></span> 
- <span data-ttu-id="ab3ec-2375">licenças de driver</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2375">driver licenses</span></span> 
- <span data-ttu-id="ab3ec-2376">carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2376">drivers license</span></span> 
- <span data-ttu-id="ab3ec-2377">de motorista carteira</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2377">driver's license</span></span> 
- <span data-ttu-id="ab3ec-2378">licenças de drivers</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2378">drivers licenses</span></span> 
- <span data-ttu-id="ab3ec-2379">licenças de motorista</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2379">driver's licenses</span></span> 
- <span data-ttu-id="ab3ec-2380">driving licence
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2380">driving licence</span></span> 
- <span data-ttu-id="ab3ec-2381">lic #</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2381">lic#</span></span> 
- <span data-ttu-id="ab3ec-2382">LIC #</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2382">LIC＃</span></span> 
- <span data-ttu-id="ab3ec-2383">lics#
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2383">lics#</span></span> 
- <span data-ttu-id="ab3ec-2384">id de estado</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2384">state id</span></span> 
- <span data-ttu-id="ab3ec-2385">state identification
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2385">state identification</span></span> 
- <span data-ttu-id="ab3ec-2386">state identification number
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2386">state identification number</span></span> 
- <span data-ttu-id="ab3ec-2387">低所得国＃
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2387">低所得国＃</span></span> 
- <span data-ttu-id="ab3ec-2388">免許証
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2388">免許証</span></span> 
- <span data-ttu-id="ab3ec-2389">状態ID</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2389">状態ID</span></span>
- <span data-ttu-id="ab3ec-2390">
状態の識別
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2390">状態の識別</span></span> 
- <span data-ttu-id="ab3ec-2391">状態の識別番号
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2391">状態の識別番号</span></span> 
- <span data-ttu-id="ab3ec-2392">運転免許
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2392">運転免許</span></span> 
- <span data-ttu-id="ab3ec-2393">運転免許証
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2393">運転免許証</span></span> 
- <span data-ttu-id="ab3ec-2394">運転免許証番号
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2394">運転免許証番号</span></span> 
   
## <a name="japan-passport-number"></a><span data-ttu-id="ab3ec-2395">Número de passaporte do Japão</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2395">Japan Passport Number</span></span>

### <a name="format"></a><span data-ttu-id="ab3ec-2396">Formato</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2396">Format</span></span>

<span data-ttu-id="ab3ec-2397">Duas letras seguidas por sete dígitos</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2397">Two letters followed by seven digits</span></span>

### <a name="pattern"></a><span data-ttu-id="ab3ec-2398">Padrão</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2398">Pattern</span></span>

<span data-ttu-id="ab3ec-2399">Duas letras (não diferencia maiúsculas de minúsculas) seguidas de sete dígitos</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2399">Two letters (not case sensitive) followed by seven digits</span></span>

### <a name="checksum"></a><span data-ttu-id="ab3ec-2400">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2400">Checksum</span></span>

<span data-ttu-id="ab3ec-2401">Não</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2401">No</span></span>

### <a name="definition"></a><span data-ttu-id="ab3ec-2402">Definição</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2402">Definition</span></span>

<span data-ttu-id="ab3ec-2403">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2403">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="ab3ec-2404">A função Func_jp_passport localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2404">The function Func_jp_passport finds content that matches the pattern.</span></span>
- <span data-ttu-id="ab3ec-2405">Uma palavra-chave de Keyword_jp_passport for encontrada.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2405">A keyword from Keyword_jp_passport is found.</span></span>

```
<!-- Japan Passport Number -->
<Entity id="75177310-1a09-4613-bf6d-833aae3743f8" patternsProximity="300" recommendedConfidence="75">
    <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_jp_passport" />
        <Match idRef="Keyword_jp_passport" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="ab3ec-2406">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2406">Keywords</span></span>

#### <a name="keywordjppassport"></a><span data-ttu-id="ab3ec-2407">Keyword_jp_passport</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2407">Keyword_jp_passport</span></span>

- <span data-ttu-id="ab3ec-2408">パスポート
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2408">パスポート</span></span> 
- <span data-ttu-id="ab3ec-2409">パスポート番号
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2409">パスポート番号</span></span> 
- <span data-ttu-id="ab3ec-2410">パスポートのNum
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2410">パスポートのNum</span></span> 
- <span data-ttu-id="ab3ec-2411">パスポート ＃
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2411">パスポート＃</span></span> 
   
## <a name="japan-resident-registration-number"></a><span data-ttu-id="ab3ec-2412">Número de registro de residente do Japão</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2412">Japan Resident Registration Number</span></span>

### <a name="format"></a><span data-ttu-id="ab3ec-2413">Formato</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2413">Format</span></span>

<span data-ttu-id="ab3ec-2414">11 dígitos</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2414">11 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="ab3ec-2415">Padrão</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2415">Pattern</span></span>

<span data-ttu-id="ab3ec-2416">11 dígitos consecutivos</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2416">11 consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="ab3ec-2417">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2417">Checksum</span></span>

<span data-ttu-id="ab3ec-2418">Não</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2418">No</span></span>

### <a name="definition"></a><span data-ttu-id="ab3ec-2419">Definição</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2419">Definition</span></span>

<span data-ttu-id="ab3ec-2420">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2420">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="ab3ec-2421">A função Func_jp_resident_registration_number localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2421">The function Func_jp_resident_registration_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="ab3ec-2422">Uma palavra-chave de Keyword_jp_resident_registration_number for encontrada.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2422">A keyword from Keyword_jp_resident_registration_number is found.</span></span>

```
<!-- Japan Resident Registration Number -->
<Entity id="01c1209b-6389-4faf-a5f8-3f7e13899652" patternsProximity="300" recommendedConfidence="75">
    <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_jp_resident_registration_number" />
        <Match idRef ="Keyword_jp_resident_registration_number" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="ab3ec-2423">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2423">Keywords</span></span>

#### <a name="keywordjpresidentregistrationnumber"></a><span data-ttu-id="ab3ec-2424">Keyword_jp_resident_registration_number</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2424">Keyword_jp_resident_registration_number</span></span>

- <span data-ttu-id="ab3ec-2425">Resident Registration Number</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2425">Resident Registration Number</span></span>
- <span data-ttu-id="ab3ec-2426">Resident Register Number
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2426">Resident Register Number</span></span> 
- <span data-ttu-id="ab3ec-2427">Residents Basic Registry Number
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2427">Residents Basic Registry Number</span></span> 
- <span data-ttu-id="ab3ec-2428">Resident Registration No.
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2428">Resident Registration No.</span></span> 
- <span data-ttu-id="ab3ec-2429">Resident Register No.
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2429">Resident Register No.</span></span> 
- <span data-ttu-id="ab3ec-2430">Residents Basic Registry No.
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2430">Residents Basic Registry No.</span></span> 
- <span data-ttu-id="ab3ec-2431">Basic Resident Register No.
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2431">Basic Resident Register No.</span></span> 
- <span data-ttu-id="ab3ec-2432">住民登録番号、登録番号をレジデント
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2432">住民登録番号、登録番号をレジデント</span></span> 
- <span data-ttu-id="ab3ec-2433">住民基本登録番号、登録番号
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2433">住民基本登録番号、登録番号</span></span> 
- <span data-ttu-id="ab3ec-2434">住民基本レジストリ番号を常駐
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2434">住民基本レジストリ番号を常駐</span></span> 
- <span data-ttu-id="ab3ec-2435">登録番号を常駐住民基本台帳登録番号
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2435">登録番号を常駐住民基本台帳登録番号</span></span> 

   
## <a name="japan-social-insurance-number-sin"></a><span data-ttu-id="ab3ec-2436">Número de seguro social do Japão (SIN)</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2436">Japan Social Insurance Number (SIN)</span></span>

### <a name="format"></a><span data-ttu-id="ab3ec-2437">Formato</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2437">Format</span></span>

<span data-ttu-id="ab3ec-2438">7 a 12 dígitos</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2438">7-12 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="ab3ec-2439">Padrão</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2439">Pattern</span></span>

<span data-ttu-id="ab3ec-2440">7 a 12 dígitos:</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2440">7-12 digits:</span></span>
- <span data-ttu-id="ab3ec-2441">Quatro dígitos</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2441">Four digits</span></span> 
- <span data-ttu-id="ab3ec-2442">Um hífen (opcional)</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2442">A hyphen (optional)</span></span> 
- <span data-ttu-id="ab3ec-2443">Seis dígitos ou</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2443">Six digits OR</span></span>
- <span data-ttu-id="ab3ec-2444">7 a 12 dígitos consecutivos</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2444">7-12 consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="ab3ec-2445">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2445">Checksum</span></span>

<span data-ttu-id="ab3ec-2446">Não</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2446">No</span></span>

### <a name="definition"></a><span data-ttu-id="ab3ec-2447">Definição</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2447">Definition</span></span>

<span data-ttu-id="ab3ec-2448">Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2448">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="ab3ec-2449">A função Func_jp_sin localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2449">The function Func_jp_sin finds content that matches the pattern.</span></span>
- <span data-ttu-id="ab3ec-2450">Uma palavra-chave de Keyword_jp_sin for encontrada.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2450">A keyword from Keyword_jp_sin is found.</span></span>

<span data-ttu-id="ab3ec-2451">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2451">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="ab3ec-2452">A função Func_jp_sin_pre_1997 localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2452">The function Func_jp_sin_pre_1997 finds content that matches the pattern.</span></span>
- <span data-ttu-id="ab3ec-2453">Uma palavra-chave de Keyword_jp_sin for encontrada.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2453">A keyword from Keyword_jp_sin is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="ab3ec-2454">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2454">Keywords</span></span>

#### <a name="keywordjpsin"></a><span data-ttu-id="ab3ec-2455">Keyword_jp_sin</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2455">Keyword_jp_sin</span></span>

- <span data-ttu-id="ab3ec-2456">Social Insurance No.
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2456">Social Insurance No.</span></span> 
- <span data-ttu-id="ab3ec-2457">Social Insurance Num
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2457">Social Insurance Num</span></span> 
- <span data-ttu-id="ab3ec-2458">Social Insurance Number
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2458">Social Insurance Number</span></span> 
- <span data-ttu-id="ab3ec-2459">社会保険のテンキー
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2459">社会保険のテンキー</span></span> 
- <span data-ttu-id="ab3ec-2460">社会保険番号
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2460">社会保険番号</span></span> 
   
## <a name="malaysia-id-card-number"></a><span data-ttu-id="ab3ec-2461">Número do Cartão de Identificação da Malásia</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2461">Malaysia ID Card Number</span></span>

### <a name="format"></a><span data-ttu-id="ab3ec-2462">Formato</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2462">Format</span></span>

<span data-ttu-id="ab3ec-2463">12 dígitos contendo hifens opcionais</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2463">12 digits containing optional hyphens</span></span>

### <a name="pattern"></a><span data-ttu-id="ab3ec-2464">Padrão</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2464">Pattern</span></span>

<span data-ttu-id="ab3ec-2465">12 dígitos:</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2465">12 digits:</span></span>
- <span data-ttu-id="ab3ec-2466">Seis dígitos no formato AAMMDD que são a data de nascimento</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2466">Six digits in the format YYMMDD which are the date of birth</span></span> 
- <span data-ttu-id="ab3ec-2467">Um traço (opcional)</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2467">A dash (optional)</span></span> 
- <span data-ttu-id="ab3ec-2468">Código do local de nascimento de duas letras </span><span class="sxs-lookup"><span data-stu-id="ab3ec-2468">Two-letter place-of-birth code</span></span> 
- <span data-ttu-id="ab3ec-2469">Um traço (opcional)</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2469">A dash (optional)</span></span> 
- <span data-ttu-id="ab3ec-2470">Três dígitos aleatórios </span><span class="sxs-lookup"><span data-stu-id="ab3ec-2470">Three random digits</span></span> 
- <span data-ttu-id="ab3ec-2471">Código de sexo de um dígito</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2471">One-digit gender code</span></span>

### <a name="checksum"></a><span data-ttu-id="ab3ec-2472">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2472">Checksum</span></span>

<span data-ttu-id="ab3ec-2473">Não</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2473">No</span></span>

### <a name="definition"></a><span data-ttu-id="ab3ec-2474">Definição</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2474">Definition</span></span>

<span data-ttu-id="ab3ec-2475">Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2475">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="ab3ec-2476">A expressão regular Regex_malaysia_id_card_number encontra o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2476">The regular expression Regex_malaysia_id_card_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="ab3ec-2477">Uma palavra-chave de Keyword_malaysia_id_card_number é encontrada.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2477">A keyword from Keyword_malaysia_id_card_number is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="ab3ec-2478">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2478">Keywords</span></span>
   
#### <a name="keywordmalaysiaidcardnumber"></a><span data-ttu-id="ab3ec-2479">Keyword_malaysia_id_card_number</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2479">Keyword_malaysia_id_card_number</span></span>

- <span data-ttu-id="ab3ec-2480">MyKad</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2480">MyKad</span></span> 
- <span data-ttu-id="ab3ec-2481">Cartão de Identidade</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2481">Identity Card</span></span> 
- <span data-ttu-id="ab3ec-2482">Cartão de identificação</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2482">ID Card</span></span> 
- <span data-ttu-id="ab3ec-2483">Cartão de identificação</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2483">Identification Card</span></span> 
- <span data-ttu-id="ab3ec-2484">Cartão do Aplicativo Digital
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2484">Digital Application Card</span></span> 
- <span data-ttu-id="ab3ec-2485">Kad Akuan Diri
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2485">Kad Akuan Diri</span></span> 
- <span data-ttu-id="ab3ec-2486">Kad Aplikasi Digital
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2486">Kad Aplikasi Digital</span></span> 
   
## <a name="netherlands-citizens-service-bsn-number"></a><span data-ttu-id="ab3ec-2487">Número do Serviço do Cidadão (BSN) da Holland</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2487">Netherlands Citizen's Service (BSN) Number</span></span>

### <a name="format"></a><span data-ttu-id="ab3ec-2488">Formato</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2488">Format</span></span>

<span data-ttu-id="ab3ec-2489">8 a 9 dígitos contendo espaços opcionais</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2489">8-9 digits containing optional spaces</span></span>

### <a name="pattern"></a><span data-ttu-id="ab3ec-2490">Padrão</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2490">Pattern</span></span>

<span data-ttu-id="ab3ec-2491">8 a 9 dígitos.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2491">8-9 digits:</span></span>
- <span data-ttu-id="ab3ec-2492">Três dígitos</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2492">Three digits</span></span> 
- <span data-ttu-id="ab3ec-2493">Um espaço (opcional)</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2493">A space (optional)</span></span> 
- <span data-ttu-id="ab3ec-2494">Três dígitos</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2494">Three digits</span></span> 
- <span data-ttu-id="ab3ec-2495">Um espaço (opcional)</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2495">A space (optional)</span></span> 
- <span data-ttu-id="ab3ec-2496">2 a 3 dígitos</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2496">2-3 digits</span></span>

### <a name="checksum"></a><span data-ttu-id="ab3ec-2497">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2497">Checksum</span></span>

<span data-ttu-id="ab3ec-2498">Sim</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2498">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="ab3ec-2499">Definição</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2499">Definition</span></span>

<span data-ttu-id="ab3ec-2500">Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2500">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="ab3ec-2501">A função Func_netherlands_bsn encontra o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2501">The function Func_netherlands_bsn finds content that matches the pattern.</span></span>
- <span data-ttu-id="ab3ec-2502">Uma palavra-chave de Keyword_netherlands_bsn é encontrada.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2502">A keyword from Keyword_netherlands_bsn is found.</span></span>
- <span data-ttu-id="ab3ec-2503">A função Func_eu_date2 encontra uma data no formato de data à direita.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2503">The function Func_eu_date2 finds a date in the right date format.</span></span>
- <span data-ttu-id="ab3ec-2504">A soma de verificação passa.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2504">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="ab3ec-2505">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2505">Keywords</span></span>

#### <a name="keywordnetherlandsbsn"></a><span data-ttu-id="ab3ec-2506">Keyword_netherlands_bsn</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2506">Keyword_netherlands_bsn</span></span>

- <span data-ttu-id="ab3ec-2507">Número do serviço do cidadão
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2507">Citizen service number</span></span> 
- <span data-ttu-id="ab3ec-2508">BSN

</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2508">BSN</span></span> 
- <span data-ttu-id="ab3ec-2509">Burgerservicenummer
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2509">Burgerservicenummer</span></span> 
- <span data-ttu-id="ab3ec-2510">Sofinummer
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2510">Sofinummer</span></span> 
- <span data-ttu-id="ab3ec-2511">Persoonsgebonden nummer
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2511">Persoonsgebonden nummer</span></span> 
- <span data-ttu-id="ab3ec-2512">Persoonsnummer
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2512">Persoonsnummer</span></span>    

   
## <a name="new-zealand-ministry-of-health-number"></a><span data-ttu-id="ab3ec-2513">Número do Ministério da Saúde da Nova Zelândia</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2513">New Zealand Ministry of Health Number</span></span>

### <a name="format"></a><span data-ttu-id="ab3ec-2514">Formato</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2514">Format</span></span>

<span data-ttu-id="ab3ec-2515">Três letras, um espaço (opcional) e quatro dígitos</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2515">Three letters, a space (optional), and four digits</span></span>

### <a name="pattern"></a><span data-ttu-id="ab3ec-2516">Padrão</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2516">Pattern</span></span>

<span data-ttu-id="ab3ec-2517">Três letras (não diferenciar maiusculas de minúsculas) um quatro dígitos (opcional) espaço</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2517">Three letters (not case sensitive) a space (optional) four digits</span></span>

### <a name="checksum"></a><span data-ttu-id="ab3ec-2518">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2518">Checksum</span></span>

<span data-ttu-id="ab3ec-2519">Sim</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2519">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="ab3ec-2520">Definição</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2520">Definition</span></span>

<span data-ttu-id="ab3ec-2521">Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2521">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="ab3ec-2522">A função Func_new_zealand_ministry_of_health_number localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2522">The function Func_new_zealand_ministry_of_health_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="ab3ec-2523">Uma palavra-chave de Keyword_nz_terms for encontrada.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2523">A keyword from Keyword_nz_terms is found.</span></span>
- <span data-ttu-id="ab3ec-2524">A soma de verificação passa.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2524">The checksum passes.</span></span>

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

<span data-ttu-id="ab3ec-2525">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2525">Keywords</span></span>

<span data-ttu-id="ab3ec-2526">Keyword_nz_terms</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2526">Keyword_nz_terms</span></span>

- <span data-ttu-id="ab3ec-2527">NHI
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2527">NHI</span></span> 
- <span data-ttu-id="ab3ec-2528">Nova Zelândia</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2528">New Zealand</span></span> 
- <span data-ttu-id="ab3ec-2529">Integridade</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2529">Health</span></span> 
- <span data-ttu-id="ab3ec-2530">tratamento
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2530">treatment</span></span> 
   
## <a name="norway-identification-number"></a><span data-ttu-id="ab3ec-2531">Número de Identificação da Noruega</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2531">Norway Identification Number</span></span>

### <a name="format"></a><span data-ttu-id="ab3ec-2532">Formato</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2532">Format</span></span>

<span data-ttu-id="ab3ec-2533">11 dígitos</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2533">11 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="ab3ec-2534">Padrão</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2534">Pattern</span></span>

<span data-ttu-id="ab3ec-2535">11 dígitos:</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2535">11 digits:</span></span>
- <span data-ttu-id="ab3ec-2536">Seis dígitos no formato DDMMAA que são a data de nascimento</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2536">Six digits in the format DDMMYY which are the date of birth</span></span> 
- <span data-ttu-id="ab3ec-2537">Número individual de três dígitos </span><span class="sxs-lookup"><span data-stu-id="ab3ec-2537">Three-digit individual number</span></span> 
- <span data-ttu-id="ab3ec-2538">Dois dígitos de verificação</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2538">Two check digits</span></span>

### <a name="checksum"></a><span data-ttu-id="ab3ec-2539">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2539">Checksum</span></span>

<span data-ttu-id="ab3ec-2540">Sim</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2540">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="ab3ec-2541">Definição</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2541">Definition</span></span>

<span data-ttu-id="ab3ec-2542">Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2542">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="ab3ec-2543">A função Func_norway_id_number encontra o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2543">The function Func_norway_id_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="ab3ec-2544">Uma palavra-chave de Keyword_norway_id_number é encontrada.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2544">A keyword from Keyword_norway_id_number is found.</span></span>
- <span data-ttu-id="ab3ec-2545">A soma de verificação passa.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2545">The checksum passes.</span></span>
- <span data-ttu-id="ab3ec-2546">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2546">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="ab3ec-2547">A função Func_norway_id_numbe encontra o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2547">The function Func_norway_id_numbe finds content that matches the pattern.</span></span>
- <span data-ttu-id="ab3ec-2548">A soma de verificação passa.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2548">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="ab3ec-2549">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2549">Keywords</span></span>

#### <a name="keywordnorwayidnumber"></a><span data-ttu-id="ab3ec-2550">Keyword_norway_id_number</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2550">Keyword_norway_id_number</span></span>

- <span data-ttu-id="ab3ec-2551">Número de identificação pessoal</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2551">Personal identification number</span></span>
- <span data-ttu-id="ab3ec-2552">Número de Identificação Norueguês</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2552">Norwegian ID Number</span></span>
- <span data-ttu-id="ab3ec-2553">Número de Identificação</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2553">ID Number</span></span>
- <span data-ttu-id="ab3ec-2554">Identificação </span><span class="sxs-lookup"><span data-stu-id="ab3ec-2554">Identification</span></span>
- <span data-ttu-id="ab3ec-2555">Personnummer</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2555">Personnummer</span></span>
- <span data-ttu-id="ab3ec-2556">Fødselsnummer</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2556">Fødselsnummer</span></span>

   
## <a name="philippines-unified-multi-purpose-id-number"></a><span data-ttu-id="ab3ec-2557">Número de Identificação Multiuso Unificada das Filipinas</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2557">Philippines Unified Multi-Purpose ID Number</span></span>

### <a name="format"></a><span data-ttu-id="ab3ec-2558">Formato</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2558">Format</span></span>

<span data-ttu-id="ab3ec-2559">12 dígitos separados por hifens</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2559">12 digits separated by hyphens</span></span>

### <a name="pattern"></a><span data-ttu-id="ab3ec-2560">Padrão</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2560">Pattern</span></span>

<span data-ttu-id="ab3ec-2561">12 dígitos:</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2561">12 digits:</span></span>
- <span data-ttu-id="ab3ec-2562">Quatro dígitos</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2562">Four digits</span></span> 
- <span data-ttu-id="ab3ec-2563">Um hífen</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2563">A hyphen</span></span> 
- <span data-ttu-id="ab3ec-2564">Sete dígitos </span><span class="sxs-lookup"><span data-stu-id="ab3ec-2564">Seven digits</span></span> 
- <span data-ttu-id="ab3ec-2565">Um hífen</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2565">A hyphen</span></span> 
- <span data-ttu-id="ab3ec-2566">Um dígito</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2566">One digit</span></span>

### <a name="checksum"></a><span data-ttu-id="ab3ec-2567">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2567">Checksum</span></span>

<span data-ttu-id="ab3ec-2568">Não</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2568">No</span></span>

### <a name="definition"></a><span data-ttu-id="ab3ec-2569">Definição</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2569">Definition</span></span>

<span data-ttu-id="ab3ec-2570">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2570">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="ab3ec-2571">A expressão regular Regex_philippines_unified_id encontra o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2571">The regular expression Regex_philippines_unified_id finds content that matches the pattern.</span></span>
- <span data-ttu-id="ab3ec-2572">Uma palavra-chave de Keyword_philippines_id é encontrada.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2572">A keyword from Keyword_philippines_id is found.</span></span>

```
<!-- Philippines Unified Multi-Purpose ID number -->
<Entity id="019b39dd-8c25-4765-91a3-d9c6baf3c3b3" recommendedConfidence="75" patternsProximity="300">
  <Pattern confidenceLevel="75">
     <IdMatch idRef="Regex_philippines_unified_id"/>
     <Match idRef="Keyword_philippines_id"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="ab3ec-2573">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2573">Keywords</span></span>
   
#### <a name="keywordphilippinesid"></a><span data-ttu-id="ab3ec-2574">Keyword_philippines_id</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2574">Keyword_philippines_id</span></span>

- <span data-ttu-id="ab3ec-2575">Identificação Multiuso Unificada
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2575">Unified Multi-Purpose ID</span></span> 
- <span data-ttu-id="ab3ec-2576">IMU
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2576">UMID</span></span> 
- <span data-ttu-id="ab3ec-2577">Cartão de Identidade</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2577">Identity Card</span></span> 
- <span data-ttu-id="ab3ec-2578">Pinag-isang Multi-Layunin ID</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2578">Pinag-isang Multi-Layunin ID</span></span>
   
## <a name="poland-identity-card"></a><span data-ttu-id="ab3ec-2579">Cartão de Identificação da Polônia</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2579">Poland Identity Card</span></span>

### <a name="format"></a><span data-ttu-id="ab3ec-2580">Formato</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2580">Format</span></span>

<span data-ttu-id="ab3ec-2581">Três letras e seis dígitos</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2581">Three letters and six digits</span></span>

### <a name="pattern"></a><span data-ttu-id="ab3ec-2582">Padrão</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2582">Pattern</span></span>

<span data-ttu-id="ab3ec-2583">Três letras (não diferenciam maiúsculas de minúsculas) seguidas de seis dígitos</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2583">Three letters (not case sensitive) followed by six digits</span></span>

### <a name="checksum"></a><span data-ttu-id="ab3ec-2584">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2584">Checksum</span></span>

<span data-ttu-id="ab3ec-2585">Sim</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2585">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="ab3ec-2586">Definição</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2586">Definition</span></span>

<span data-ttu-id="ab3ec-p138">Uma política de DLP é 75% confiante de que detectou esse tipo de informações confidenciais if, dentro de uma proximidade de 300 caracteres: A função Func_polish_national_id encontra o conteúdo que corresponde ao padrão. Uma palavra-chave de Keyword_polish_national_id_passport_number é encontrada. A soma de verificação passa.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-p138">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters: The function Func_polish_national_id finds content that matches the pattern. A keyword from Keyword_polish_national_id_passport_number is found. The checksum passes.</span></span>

```
<!-- Poland Identity Card-->
<Entity id="25E64989-ED5D-40CA-A939-6C14183BB7BF" patternsProximity="300" recommendedConfidence="85">
      <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_polish_national_id" />
          <Match idRef="Keyword_polish_national_id_passport_number" />
      </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="ab3ec-2590">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2590">Keywords</span></span>

#### <a name="keywordpolishnationalidpassportnumber"></a><span data-ttu-id="ab3ec-2591">Keyword_polish_national_id_passport_number</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2591">Keyword_polish_national_id_passport_number</span></span>

- <span data-ttu-id="ab3ec-2592">Nazwa i nr dowodu tożsamości
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2592">Nazwa i nr dowodu tożsamości</span></span> 
- <span data-ttu-id="ab3ec-2593">Dowód Tożsamości
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2593">Dowód Tożsamości</span></span> 
- <span data-ttu-id="ab3ec-p139">dow. os.
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-p139">dow. os.</span></span> 

   
## <a name="poland-national-id-pesel"></a><span data-ttu-id="ab3ec-2596">ID nacional da Polônia (PESEL)</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2596">Poland National ID (PESEL)</span></span>

### <a name="format"></a><span data-ttu-id="ab3ec-2597">Formato</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2597">Format</span></span>

<span data-ttu-id="ab3ec-2598">11 dígitos</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2598">11 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="ab3ec-2599">Padrão</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2599">Pattern</span></span>

<span data-ttu-id="ab3ec-2600">11 dígitos consecutivos</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2600">11 consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="ab3ec-2601">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2601">Checksum</span></span>

<span data-ttu-id="ab3ec-2602">Sim</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2602">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="ab3ec-2603">Definição</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2603">Definition</span></span>

<span data-ttu-id="ab3ec-2604">Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2604">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="ab3ec-2605">A função Func_pesel_identification_number localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2605">The function Func_pesel_identification_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="ab3ec-2606">Uma palavra-chave de Keyword_pesel_identification_number for encontrada.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2606">A keyword from Keyword_pesel_identification_number is found.</span></span>
- <span data-ttu-id="ab3ec-2607">A soma de verificação passa.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2607">The checksum passes.</span></span>

```
<!-- Poland National ID (PESEL) -->      
<Entity id="E3AAF206-4297-412F-9E06-BA8487E22456" patternsProximity="300" recommendedConfidence="85">
      <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_pesel_identification_number" />
          <Match idRef="Keyword_pesel_identification_number" />
      </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="ab3ec-2608">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2608">Keywords</span></span>

#### <a name="keywordpeselidentificationnumber"></a><span data-ttu-id="ab3ec-2609">Keyword_pesel_identification_number</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2609">Keyword_pesel_identification_number</span></span>

- <span data-ttu-id="ab3ec-2610">Nr PESEL</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2610">Nr PESEL</span></span>
- <span data-ttu-id="ab3ec-2611">PESEL</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2611">PESEL</span></span>   

   
## <a name="poland-passport"></a><span data-ttu-id="ab3ec-2612">Passaporte da Polônia</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2612">Poland Passport</span></span>

### <a name="format"></a><span data-ttu-id="ab3ec-2613">Formato</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2613">Format</span></span>

<span data-ttu-id="ab3ec-2614">Duas letras e sete dígitos</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2614">Two letters and seven digits</span></span>

### <a name="pattern"></a><span data-ttu-id="ab3ec-2615">Padrão</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2615">Pattern</span></span>

<span data-ttu-id="ab3ec-2616">Duas letras (não diferencia maiúsculas de minúsculas) seguidas de sete dígitos</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2616">Two letters (not case sensitive) followed by seven digits</span></span>

### <a name="checksum"></a><span data-ttu-id="ab3ec-2617">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2617">Checksum</span></span>

<span data-ttu-id="ab3ec-2618">Sim</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2618">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="ab3ec-2619">Definição</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2619">Definition</span></span>

<span data-ttu-id="ab3ec-2620">Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2620">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="ab3ec-2621">A função Func_polish_passport_number localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2621">The function Func_polish_passport_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="ab3ec-2622">Uma palavra-chave de Keyword_polish_national_id_passport_number for encontrada.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2622">A keyword from Keyword_polish_national_id_passport_number is found.</span></span>
- <span data-ttu-id="ab3ec-2623">A soma de verificação passa.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2623">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="ab3ec-2624">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2624">Keywords</span></span>

#### <a name="keywordpolishnationalidpassportnumber"></a><span data-ttu-id="ab3ec-2625">Keyword_polish_national_id_passport_number</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2625">Keyword_polish_national_id_passport_number</span></span>

- <span data-ttu-id="ab3ec-2626">Nazwa i nr dowodu tożsamości
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2626">Nazwa i nr dowodu tożsamości</span></span> 
- <span data-ttu-id="ab3ec-2627">Dowód Tożsamości
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2627">Dowód Tożsamości</span></span> 
- <span data-ttu-id="ab3ec-p140">dow. os.
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-p140">dow. os.</span></span> 

   
## <a name="portugal-citizen-card-number"></a><span data-ttu-id="ab3ec-2630">Número do Cartão de Cidadão de Portugal</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2630">Portugal Citizen Card Number</span></span>

### <a name="format"></a><span data-ttu-id="ab3ec-2631">Formato</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2631">Format</span></span>

<span data-ttu-id="ab3ec-2632">Oito dígitos</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2632">Eight digits</span></span>

### <a name="pattern"></a><span data-ttu-id="ab3ec-2633">Padrão</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2633">Pattern</span></span>

<span data-ttu-id="ab3ec-2634">Oito dígitos</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2634">Eight digits</span></span>

### <a name="checksum"></a><span data-ttu-id="ab3ec-2635">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2635">Checksum</span></span>

<span data-ttu-id="ab3ec-2636">Não</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2636">No</span></span>

### <a name="definition"></a><span data-ttu-id="ab3ec-2637">Definição</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2637">Definition</span></span>

<span data-ttu-id="ab3ec-2638">Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2638">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="ab3ec-2639">A expressão regular Regex_portugal_citizen_card encontra o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2639">The regular expression Regex_portugal_citizen_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="ab3ec-2640">Uma palavra-chave de Keyword_portugal_citizen_card é encontrada.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2640">A keyword from Keyword_portugal_citizen_card is found.</span></span>

```
<!-- Portugal Citizen Card Number -->
<Entity id="91a7ece2-add4-4986-9a15-c84544d81ecd" recommendedConfidence="85" patternsProximity="300">
  <Pattern confidenceLevel="85">
     <IdMatch idRef="Regex_portugal_citizen_card"/>
     <Match idRef="Keyword_portugal_citizen_card"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="ab3ec-2641">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2641">Keywords</span></span>

#### <a name="keywordportugalcitizencard"></a><span data-ttu-id="ab3ec-2642">Keyword_portugal_citizen_card</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2642">Keyword_portugal_citizen_card</span></span>

- <span data-ttu-id="ab3ec-2643">Cartão de Cidadão</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2643">Citizen Card</span></span>
- <span data-ttu-id="ab3ec-2644">Cartão de Identidade Nacional</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2644">National ID Card</span></span>
- <span data-ttu-id="ab3ec-2645">CC</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2645">CC</span></span>
- <span data-ttu-id="ab3ec-2646">Cartão de Cidadão</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2646">Cartão de Cidadão</span></span>
- <span data-ttu-id="ab3ec-2647">Bilhete de Identidade</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2647">Bilhete de Identidade</span></span>
   
## <a name="saudi-arabia-national-id"></a><span data-ttu-id="ab3ec-2648">ID nacional da Arábia Saudita</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2648">Saudi Arabia National ID</span></span>

### <a name="format"></a><span data-ttu-id="ab3ec-2649">Formato</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2649">Format</span></span>

<span data-ttu-id="ab3ec-2650">10 dígitos</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2650">10 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="ab3ec-2651">Padrão</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2651">Pattern</span></span>

<span data-ttu-id="ab3ec-2652">10 dígitos consecutivos</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2652">10 consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="ab3ec-2653">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2653">Checksum</span></span>

<span data-ttu-id="ab3ec-2654">Não</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2654">No</span></span>

### <a name="definition"></a><span data-ttu-id="ab3ec-2655">Definição</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2655">Definition</span></span>

<span data-ttu-id="ab3ec-2656">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2656">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="ab3ec-2657">A expressão regular Regex_saudi_arabia_national_id localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2657">The regular expression Regex_saudi_arabia_national_id finds content that matches the pattern.</span></span>
- <span data-ttu-id="ab3ec-2658">Uma palavra-chave de Keyword_saudi_arabia_national_id for encontrada.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2658">A keyword from Keyword_saudi_arabia_national_id is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="ab3ec-2659">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2659">Keywords</span></span>

#### <a name="keywordsaudiarabianationalid"></a><span data-ttu-id="ab3ec-2660">Keyword_saudi_arabia_national_id</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2660">Keyword_saudi_arabia_national_id</span></span>

- <span data-ttu-id="ab3ec-2661">Identification Card
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2661">Identification Card</span></span> 
- <span data-ttu-id="ab3ec-2662">I card number
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2662">I card number</span></span> 
- <span data-ttu-id="ab3ec-2663">número de identificação</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2663">ID number</span></span> 
- <span data-ttu-id="ab3ec-2664">الوطنية الهوية بطاقة رقم
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2664">الوطنية الهوية بطاقة رقم</span></span> 

   
## <a name="singapore-national-registration-identity-card-nric-number"></a><span data-ttu-id="ab3ec-2665">Número do Cartão de Identidade do Registro Nacional (NRIC) de Cingapura</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2665">Singapore National Registration Identity Card (NRIC) Number</span></span>

### <a name="format"></a><span data-ttu-id="ab3ec-2666">Formato</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2666">Format</span></span>

<span data-ttu-id="ab3ec-2667">Nove letras e dígitos</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2667">Nine letters and digits</span></span>

### <a name="pattern"></a><span data-ttu-id="ab3ec-2668">Padrão</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2668">Pattern</span></span>

- <span data-ttu-id="ab3ec-2669">Nove letras e dígitos:</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2669">Nine letters and digits:</span></span>
- <span data-ttu-id="ab3ec-2670">A letra "F", "G", "S" ou "T" (não diferenciam maiúsculas de minúsculas) </span><span class="sxs-lookup"><span data-stu-id="ab3ec-2670">The letter "F", "G", "S", or "T" (not case sensitive)</span></span> 
- <span data-ttu-id="ab3ec-2671">Sete dígitos </span><span class="sxs-lookup"><span data-stu-id="ab3ec-2671">Seven digits</span></span> 
- <span data-ttu-id="ab3ec-2672">Um dígito de verificação alfabético</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2672">An alphabetic check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="ab3ec-2673">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2673">Checksum</span></span>

<span data-ttu-id="ab3ec-2674">Sim</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2674">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="ab3ec-2675">Definição</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2675">Definition</span></span>

<span data-ttu-id="ab3ec-2676">Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2676">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="ab3ec-2677">A expressão regular Regex_singapore_nric encontra o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2677">The regular expression Regex_singapore_nric finds content that matches the pattern.</span></span>
- <span data-ttu-id="ab3ec-2678">Uma palavra-chave de Keyword_singapore_nric é encontrada.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2678">A keyword from Keyword_singapore_nric is found.</span></span>
- <span data-ttu-id="ab3ec-2679">A soma de verificação passa.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2679">The checksum passes.</span></span>

<span data-ttu-id="ab3ec-2680">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2680">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="ab3ec-2681">A expressão regular Regex_singapore_nric encontra o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2681">The regular expression Regex_singapore_nric finds content that matches the pattern.</span></span>
- <span data-ttu-id="ab3ec-2682">A soma de verificação passa.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2682">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="ab3ec-2683">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2683">Keywords</span></span>
   
#### <a name="keywordsingaporenric"></a><span data-ttu-id="ab3ec-2684">Keyword_singapore_nric</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2684">Keyword_singapore_nric</span></span>

- <span data-ttu-id="ab3ec-2685">Número do Cartão de Identidade do Registro Nacional
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2685">National Registration Identity Card</span></span> 
- <span data-ttu-id="ab3ec-2686">Número do Cartão de Identidade
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2686">Identity Card Number</span></span> 
- <span data-ttu-id="ab3ec-2687">NRIC
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2687">NRIC</span></span> 
- <span data-ttu-id="ab3ec-2688">IC
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2688">IC</span></span> 
- <span data-ttu-id="ab3ec-2689">Número de Identificação Estrangeira
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2689">Foreign Identification Number</span></span> 
- <span data-ttu-id="ab3ec-2690">FIN
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2690">FIN</span></span> 
- <span data-ttu-id="ab3ec-2691">身份证 </span><span class="sxs-lookup"><span data-stu-id="ab3ec-2691">身份证</span></span> 
- <span data-ttu-id="ab3ec-2692">身份證
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2692">身份證</span></span> 
   
## <a name="south-africa-identification-number"></a><span data-ttu-id="ab3ec-2693">Número de Identificação da África do Sul</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2693">South Africa Identification Number</span></span>

### <a name="format"></a><span data-ttu-id="ab3ec-2694">Formato</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2694">Format</span></span>

<span data-ttu-id="ab3ec-2695">13 dígitos que podem conter espaços</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2695">13 digits that may contain spaces</span></span>

### <a name="pattern"></a><span data-ttu-id="ab3ec-2696">Padrão</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2696">Pattern</span></span>

<span data-ttu-id="ab3ec-2697">13 dígitos:</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2697">13 digits:</span></span>
- <span data-ttu-id="ab3ec-2698">Seis dígitos no formato AAMMDD que são a data de nascimento</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2698">Six digits in the format YYMMDD which are the date of birth</span></span> 
- <span data-ttu-id="ab3ec-2699">Quatro dígitos</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2699">Four digits</span></span> 
- <span data-ttu-id="ab3ec-2700">Indicador de cidadania de um dígito </span><span class="sxs-lookup"><span data-stu-id="ab3ec-2700">A single-digit citizenship indicator</span></span> 
- <span data-ttu-id="ab3ec-2701">O dígito "8" ou "9" </span><span class="sxs-lookup"><span data-stu-id="ab3ec-2701">The digit "8" or "9"</span></span> 
- <span data-ttu-id="ab3ec-2702">Um dígito que é um dígito de soma de verificação</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2702">One digit which is a checksum digit</span></span>

### <a name="checksum"></a><span data-ttu-id="ab3ec-2703">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2703">Checksum</span></span>

<span data-ttu-id="ab3ec-2704">Sim</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2704">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="ab3ec-2705">Definição</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2705">Definition</span></span>

<span data-ttu-id="ab3ec-2706">Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2706">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="ab3ec-2707">A função Func_south_africa_identification_number encontra o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2707">The function Func_south_africa_identification_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="ab3ec-2708">Uma palavra-chave de Keyword_south_africa_identification_number é encontrada.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2708">A keyword from Keyword_south_africa_identification_number is found.</span></span>
- <span data-ttu-id="ab3ec-2709">A soma de verificação passa.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2709">The checksum passes.</span></span>

```
<!-- South Africa Identification Number -->
<Entity id="e2adf7cb-8ea6-4048-a2ed-d89eb65f2780" recommendedConfidence="85" patternsProximity="300">
  <Pattern confidenceLevel="85">
     <IdMatch idRef="Func_south_africa_identification_number"/>
     <Match idRef="Keyword_south_africa_identification_number"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="ab3ec-2710">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2710">Keywords</span></span>
   
#### <a name="keywordsouthafricaidentificationnumber"></a><span data-ttu-id="ab3ec-2711">Keyword_south_africa_identification_number</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2711">Keyword_south_africa_identification_number</span></span>

- <span data-ttu-id="ab3ec-2712">Cartão de identidade</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2712">Identity card</span></span>
- <span data-ttu-id="ab3ec-2713">ID</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2713">ID</span></span>
- <span data-ttu-id="ab3ec-2714">Identificação </span><span class="sxs-lookup"><span data-stu-id="ab3ec-2714">Identification</span></span> 
   
## <a name="south-korea-resident-registration-number"></a><span data-ttu-id="ab3ec-2715">Número do Registro de Residentes da Coreia do Sul</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2715">South Korea Resident Registration Number</span></span>

### <a name="format"></a><span data-ttu-id="ab3ec-2716">Formato</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2716">Format</span></span>

<span data-ttu-id="ab3ec-2717">13 dígitos que contém um hifen</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2717">13 digits containing a hyphen</span></span>

### <a name="pattern"></a><span data-ttu-id="ab3ec-2718">Padrão</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2718">Pattern</span></span>

<span data-ttu-id="ab3ec-2719">13 dígitos:</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2719">13 digits:</span></span>
- <span data-ttu-id="ab3ec-2720">Seis dígitos no formato AAMMDD que são a data de nascimento</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2720">Six digits in the format YYMMDD which are the date of birth</span></span> 
- <span data-ttu-id="ab3ec-2721">Um hífen</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2721">A hyphen</span></span> 
- <span data-ttu-id="ab3ec-2722">Um dígito determinado pelo século e pelo sexo </span><span class="sxs-lookup"><span data-stu-id="ab3ec-2722">One digit determined by the century and gender</span></span> 
- <span data-ttu-id="ab3ec-2723">Código da região de nascimento de quatro dígitos </span><span class="sxs-lookup"><span data-stu-id="ab3ec-2723">Four-digit region-of-birth code</span></span> 
- <span data-ttu-id="ab3ec-2724">Um dígito usado para diferenciar as pessoas para as quais os números anteriores são idênticos </span><span class="sxs-lookup"><span data-stu-id="ab3ec-2724">One digit used to differentiate people for whom the preceding numbers are identical</span></span> 
- <span data-ttu-id="ab3ec-2725">Um dígito de verificação.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2725">A check digit.</span></span>

### <a name="checksum"></a><span data-ttu-id="ab3ec-2726">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2726">Checksum</span></span>

<span data-ttu-id="ab3ec-2727">Sim</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2727">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="ab3ec-2728">Definição</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2728">Definition</span></span>

<span data-ttu-id="ab3ec-2729">Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2729">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="ab3ec-2730">A função Func_south_korea_resident_number encontra o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2730">The function Func_south_korea_resident_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="ab3ec-2731">Uma palavra-chave de Keyword_south_korea_resident_number é encontrada.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2731">A keyword from Keyword_south_korea_resident_number is found.</span></span>
- <span data-ttu-id="ab3ec-2732">A soma de verificação passa.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2732">The checksum passes.</span></span>

<span data-ttu-id="ab3ec-2733">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2733">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="ab3ec-2734">A função Func_south_korea_resident_number encontra o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2734">The function Func_south_korea_resident_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="ab3ec-2735">A soma de verificação passa.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2735">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="ab3ec-2736">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2736">Keywords</span></span>
   
#### <a name="keywordsouthkorearesidentnumber"></a><span data-ttu-id="ab3ec-2737">Keyword_south_korea_resident_number</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2737">Keyword_south_korea_resident_number</span></span>

- <span data-ttu-id="ab3ec-2738">Cartão de identidade nacional
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2738">National ID card</span></span> 
- <span data-ttu-id="ab3ec-2739">Número de Registro do Cidadão
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2739">Citizen's Registration Number</span></span> 
- <span data-ttu-id="ab3ec-2740">Jumin deungnok beonho
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2740">Jumin deungnok beonho</span></span> 
- <span data-ttu-id="ab3ec-2741">RRN
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2741">RRN</span></span> 
- <span data-ttu-id="ab3ec-2742">주민등록번호</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2742">주민등록번호</span></span>
   
## <a name="spain-social-security-number-ssn"></a><span data-ttu-id="ab3ec-2743">Número de seguridade social da Espanha (SSN)</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2743">Spain Social Security Number (SSN)</span></span>

### <a name="format"></a><span data-ttu-id="ab3ec-2744">Formato</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2744">Format</span></span>

<span data-ttu-id="ab3ec-2745">11 a 12 dígitos</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2745">11-12 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="ab3ec-2746">Padrão</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2746">Pattern</span></span>

<span data-ttu-id="ab3ec-2747">12 de 11 dígitos:</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2747">11-12 digits:</span></span>
- <span data-ttu-id="ab3ec-2748">Dois dígitos</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2748">Two digits</span></span> 
- <span data-ttu-id="ab3ec-2749">Uma barra (opcional)</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2749">A forward slash (optional)</span></span> 
- <span data-ttu-id="ab3ec-2750">7 a 8 dígitos</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2750">7-8 digits</span></span> 
- <span data-ttu-id="ab3ec-2751">Uma barra (opcional)</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2751">A forward slash (optional)</span></span> 
- <span data-ttu-id="ab3ec-2752">Dois dígitos</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2752">Two digits</span></span>

### <a name="checksum"></a><span data-ttu-id="ab3ec-2753">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2753">Checksum</span></span>

<span data-ttu-id="ab3ec-2754">Sim</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2754">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="ab3ec-2755">Definição</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2755">Definition</span></span>

<span data-ttu-id="ab3ec-2756">Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2756">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="ab3ec-2757">A função Func_spanish_social_security_number localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2757">The function Func_spanish_social_security_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="ab3ec-2758">A soma de verificação passa.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2758">The checksum passes.</span></span>

```
<!-- Spain SSN -->
<Entity id="5df987c0-8eae-4bce-ace7-b316347f3070" patternsProximity="300" recommendedConfidence="85">
    <Pattern confidenceLevel="85">
        <IdMatch idRef="Func_spanish_social_security_number" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="ab3ec-2759">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2759">Keywords</span></span>

<span data-ttu-id="ab3ec-2760">Nenhum</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2760">None</span></span>
   
## <a name="sweden-national-id"></a><span data-ttu-id="ab3ec-2761">ID nacional da Suécia</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2761">Sweden National ID</span></span>

### <a name="format"></a><span data-ttu-id="ab3ec-2762">Formato</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2762">Format</span></span>

<span data-ttu-id="ab3ec-2763">10 ou 12 dígitos e um delimitador opcional</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2763">10 or 12 digits and an optional delimiter</span></span>

### <a name="pattern"></a><span data-ttu-id="ab3ec-2764">Padrão</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2764">Pattern</span></span>

<span data-ttu-id="ab3ec-2765">10 ou 12 dígitos e um delimitador opcional:</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2765">10 or 12 digits and an optional delimiter:</span></span>
- <span data-ttu-id="ab3ec-2766">2 a 4 dígitos (opcionais)</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2766">2-4 digits (optional)</span></span> 
- <span data-ttu-id="ab3ec-2767">Seis dígitos no formato de data AAMMDD</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2767">Six digits in date format YYMMDD</span></span> 
- <span data-ttu-id="ab3ec-2768">Um delimitador de "-" ou "+" (opcional), mais</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2768">Delimiter of "-" or "+" (optional), plus</span></span>
- <span data-ttu-id="ab3ec-2769">Quatro dígitos</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2769">Four digits</span></span>

### <a name="checksum"></a><span data-ttu-id="ab3ec-2770">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2770">Checksum</span></span>

<span data-ttu-id="ab3ec-2771">Sim</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2771">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="ab3ec-2772">Definição</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2772">Definition</span></span>

<span data-ttu-id="ab3ec-2773">Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2773">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="ab3ec-2774">A função Func_swedish_national_identifier localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2774">The function Func_swedish_national_identifier finds content that matches the pattern.</span></span>
- <span data-ttu-id="ab3ec-2775">A soma de verificação passa.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2775">The checksum passes.</span></span>

```
<!-- Sweden National ID -->
<Entity id="f69aaf40-79be-4fac-8f05-fd1910d272c8" patternsProximity="300" recommendedConfidence="85">
    <Pattern confidenceLevel="85">
        <IdMatch idRef="Func_swedish_national_identifier" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="ab3ec-2776">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2776">Keywords</span></span>

<span data-ttu-id="ab3ec-2777">Não</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2777">No</span></span>
   
## <a name="sweden-passport-number"></a><span data-ttu-id="ab3ec-2778">Número de passaporte da Suécia</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2778">Sweden Passport Number</span></span>

### <a name="format"></a><span data-ttu-id="ab3ec-2779">Formato</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2779">Format</span></span>

<span data-ttu-id="ab3ec-2780">Oito dígitos</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2780">Eight digits</span></span>

### <a name="pattern"></a><span data-ttu-id="ab3ec-2781">Padrão</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2781">Pattern</span></span>

<span data-ttu-id="ab3ec-2782">Oito dígitos consecutivos</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2782">Eight consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="ab3ec-2783">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2783">Checksum</span></span>

<span data-ttu-id="ab3ec-2784">Não</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2784">No</span></span>

### <a name="definition"></a><span data-ttu-id="ab3ec-2785">Definição</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2785">Definition</span></span>

<span data-ttu-id="ab3ec-2786">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2786">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="ab3ec-2787">A expressão regular Regex_sweden_passport_number localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2787">The regular expression Regex_sweden_passport_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="ab3ec-2788">Uma das seguintes opções for verdadeira:</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2788">One of the following is true:</span></span>
    - <span data-ttu-id="ab3ec-2789">Uma palavra-chave de Keyword_passport for encontrada.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2789">A keyword from Keyword_passport is found.</span></span>
    - <span data-ttu-id="ab3ec-2790">Uma palavra-chave de Keyword_sweden_passport for encontrada.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2790">A keyword from Keyword_sweden_passport is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="ab3ec-2791">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2791">Keywords</span></span>
   
#### <a name="keywordswedenpassport"></a><span data-ttu-id="ab3ec-2792">Keyword_sweden_passport</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2792">Keyword_sweden_passport</span></span>

- <span data-ttu-id="ab3ec-2793">visa requirements
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2793">visa requirements</span></span> 
- <span data-ttu-id="ab3ec-2794">Alien Registration Card
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2794">Alien Registration Card</span></span> 
- <span data-ttu-id="ab3ec-2795">Schengen visas
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2795">Schengen visas</span></span> 
- <span data-ttu-id="ab3ec-2796">Schengen visa
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2796">Schengen visa</span></span> 
- <span data-ttu-id="ab3ec-2797">Visa Processing
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2797">Visa Processing</span></span> 
- <span data-ttu-id="ab3ec-2798">Visa Type
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2798">Visa Type</span></span> 
- <span data-ttu-id="ab3ec-2799">Single Entry
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2799">Single Entry</span></span> 
- <span data-ttu-id="ab3ec-2800">Multiple Entry
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2800">Multiple Entry</span></span> 
- <span data-ttu-id="ab3ec-2801">G3 Processing Fees

</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2801">G3 Processing Fees</span></span> 

#### <a name="keywordpassport"></a><span data-ttu-id="ab3ec-2802">Keyword_passport</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2802">Keyword_passport</span></span>

- <span data-ttu-id="ab3ec-2803">Passport Number</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2803">Passport Number</span></span> 
- <span data-ttu-id="ab3ec-2804">
Passport No</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2804">Passport No</span></span> 
- <span data-ttu-id="ab3ec-2805">Passport #
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2805">Passport #</span></span> 
- <span data-ttu-id="ab3ec-2806">Passport#
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2806">Passport#</span></span> 
- <span data-ttu-id="ab3ec-2807">PassportID</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2807">PassportID</span></span> 
- <span data-ttu-id="ab3ec-2808">Passportno
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2808">Passportno</span></span> 
- <span data-ttu-id="ab3ec-2809">passportnumber
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2809">passportnumber</span></span> 
- <span data-ttu-id="ab3ec-2810">パスポート</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2810">パスポート</span></span> 
- <span data-ttu-id="ab3ec-2811">パスポート番号
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2811">パスポート番号</span></span> 
- <span data-ttu-id="ab3ec-2812">パスポートのNum
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2812">パスポートのNum</span></span> 
- <span data-ttu-id="ab3ec-2813">パスポート＃
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2813">パスポート＃</span></span> 
- <span data-ttu-id="ab3ec-2814">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2814">Numéro de passeport</span></span> 
- <span data-ttu-id="ab3ec-2815">
Passeport n °</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2815">Passeport n °</span></span> 
- <span data-ttu-id="ab3ec-2816">Passeport Non
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2816">Passeport Non</span></span> 
- <span data-ttu-id="ab3ec-2817">Passeport #
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2817">Passeport #</span></span> 
- <span data-ttu-id="ab3ec-2818">Passeport#
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2818">Passeport#</span></span> 
- <span data-ttu-id="ab3ec-2819">PasseportNon</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2819">PasseportNon</span></span> 
- <span data-ttu-id="ab3ec-2820">Passeportn °
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2820">Passeportn °</span></span> 
   
## <a name="swift-code"></a><span data-ttu-id="ab3ec-2821">Código SWIFT</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2821">SWIFT Code</span></span>

### <a name="format"></a><span data-ttu-id="ab3ec-2822">Formato</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2822">Format</span></span>

<span data-ttu-id="ab3ec-2823">Quatro letras seguidas por 5 a 31 letras ou dígitos</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2823">Four letters followed by 5-31 letters or digits</span></span>

### <a name="pattern"></a><span data-ttu-id="ab3ec-2824">Padrão</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2824">Pattern</span></span>

<span data-ttu-id="ab3ec-2825">Quatro letras seguidas por 5 a 31 letras ou dígitos:</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2825">Four letters followed by 5-31 letters or digits:</span></span>
- <span data-ttu-id="ab3ec-2826">Código bancário de quatro letras (não diferencia maiúsculas de minúsculas)</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2826">Four-letter bank code (not case sensitive)</span></span> 
- <span data-ttu-id="ab3ec-2827">Um espaço opcional</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2827">An optional space</span></span> 
- <span data-ttu-id="ab3ec-2828">4 a 28 letras ou dígitos (o número de conta bancária básica (BBAN))</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2828">4-28 letters or digits (the Basic Bank Account Number (BBAN))</span></span> 
- <span data-ttu-id="ab3ec-2829">Um espaço opcional</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2829">An optional space</span></span> 
- <span data-ttu-id="ab3ec-2830">1 a 3 letras ou dígitos (restante do BBAN)</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2830">1-3 letters or digits (remainder of the BBAN)</span></span>

### <a name="checksum"></a><span data-ttu-id="ab3ec-2831">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2831">Checksum</span></span>

<span data-ttu-id="ab3ec-2832">Não</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2832">No</span></span>

### <a name="definition"></a><span data-ttu-id="ab3ec-2833">Definição</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2833">Definition</span></span>

<span data-ttu-id="ab3ec-2834">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2834">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="ab3ec-2835">A expressão regular Regex_swift localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2835">The regular expression Regex_swift finds content that matches the pattern.</span></span>
- <span data-ttu-id="ab3ec-2836">Uma palavra-chave de Keyword_swift for encontrada.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2836">A keyword from Keyword_swift is found.</span></span>

```
<Entity id="cb2ab58c-9cb8-4c81-baf8-a4e106791df4" patternsProximity="300" recommendedConfidence="75">
<Pattern confidenceLevel="75">
        <IdMatch idRef="Regex_swift" />
        <Match idRef="Keyword_swift" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="ab3ec-2837">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2837">Keywords</span></span>
   
#### <a name="keywordswift"></a><span data-ttu-id="ab3ec-2838">Keyword_swift</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2838">Keyword_swift</span></span>

- <span data-ttu-id="ab3ec-2839">international organization for standardization 9362
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2839">international organization for standardization 9362</span></span> 
- <span data-ttu-id="ab3ec-2840">iso 9362
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2840">iso 9362</span></span> 
- <span data-ttu-id="ab3ec-2841">iso9362</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2841">iso9362</span></span> 
- <span data-ttu-id="ab3ec-2842">SWIFT\#</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2842">swift\#</span></span> 
- <span data-ttu-id="ab3ec-2843">swiftcode
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2843">swiftcode</span></span> 
- <span data-ttu-id="ab3ec-2844">swiftnumber
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2844">swiftnumber</span></span> 
- <span data-ttu-id="ab3ec-2845">swiftroutingnumber
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2845">swiftroutingnumber</span></span> 
- <span data-ttu-id="ab3ec-2846">swift code
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2846">swift code</span></span> 
- <span data-ttu-id="ab3ec-2847">swift number #
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2847">swift number #</span></span> 
- <span data-ttu-id="ab3ec-2848">swift routing number
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2848">swift routing number</span></span> 
- <span data-ttu-id="ab3ec-2849">bic number
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2849">bic number</span></span> 
- <span data-ttu-id="ab3ec-2850">bic code
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2850">bic code</span></span> 
- <span data-ttu-id="ab3ec-2851">BIC\#</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2851">bic \#</span></span> 
- <span data-ttu-id="ab3ec-2852">BIC\#</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2852">bic\#</span></span> 
- <span data-ttu-id="ab3ec-2853">bank identifier code
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2853">bank identifier code</span></span> 
- <span data-ttu-id="ab3ec-2854">標準化9362</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2854">標準化9362</span></span> 
- <span data-ttu-id="ab3ec-2855">迅速＃
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2855">迅速＃</span></span> 
- <span data-ttu-id="ab3ec-2856">SWIFTコード
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2856">SWIFTコード</span></span> 
- <span data-ttu-id="ab3ec-2857">SWIFT番号
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2857">SWIFT番号</span></span> 
- <span data-ttu-id="ab3ec-2858">迅速なルーティング番号
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2858">迅速なルーティング番号</span></span> 
- <span data-ttu-id="ab3ec-2859">BIC番号
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2859">BIC番号</span></span> 
- <span data-ttu-id="ab3ec-2860">BICコード
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2860">BICコード</span></span> 
- <span data-ttu-id="ab3ec-2861">銀行識別コードのための国際組織
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2861">銀行識別コードのための国際組織</span></span> 
- <span data-ttu-id="ab3ec-2862">Organisation internationale de normalisation 9362
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2862">Organisation internationale de normalisation 9362</span></span> 
- <span data-ttu-id="ab3ec-2863">rapide\#</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2863">rapide \#</span></span> 
- <span data-ttu-id="ab3ec-2864">code SWIFT
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2864">code SWIFT</span></span> 
- <span data-ttu-id="ab3ec-2865">le numéro de swift
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2865">le numéro de swift</span></span> 
- <span data-ttu-id="ab3ec-2866">swift numéro d'acheminement
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2866">swift numéro d'acheminement</span></span> 
- <span data-ttu-id="ab3ec-2867">le numéro BIC
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2867">le numéro BIC</span></span> 
- <span data-ttu-id="ab3ec-2868">\#BIC</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2868">\# BIC</span></span> 
- <span data-ttu-id="ab3ec-2869">code identificateur de banque
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2869">code identificateur de banque</span></span> 
   
## <a name="taiwan-national-id"></a><span data-ttu-id="ab3ec-2870">ID nacional de Taiwan</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2870">Taiwan National ID</span></span>

### <a name="format"></a><span data-ttu-id="ab3ec-2871">Formato</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2871">Format</span></span>

<span data-ttu-id="ab3ec-2872">Uma letra (em inglês) seguida de nove dígitos</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2872">One letter (in English) followed by nine digits</span></span>

### <a name="pattern"></a><span data-ttu-id="ab3ec-2873">Padrão</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2873">Pattern</span></span>

<span data-ttu-id="ab3ec-2874">Uma letra (em inglês) seguida de nove dígitos:</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2874">One letter (in English) followed by nine digits:</span></span>
- <span data-ttu-id="ab3ec-2875">Uma letra (em inglês, não diferencia maiúscula de minúscula)</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2875">One letter (in English, not case sensitive)</span></span> 
- <span data-ttu-id="ab3ec-2876">O dígito "1" ou "2"</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2876">The digit "1" or "2"</span></span> 
- <span data-ttu-id="ab3ec-2877">Oito dígitos</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2877">Eight digits</span></span>

### <a name="checksum"></a><span data-ttu-id="ab3ec-2878">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2878">Checksum</span></span>

<span data-ttu-id="ab3ec-2879">Sim</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2879">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="ab3ec-2880">Definição</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2880">Definition</span></span>

<span data-ttu-id="ab3ec-2881">Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2881">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="ab3ec-2882">A função Func_taiwanese_national_id localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2882">The function Func_taiwanese_national_id finds content that matches the pattern.</span></span>
- <span data-ttu-id="ab3ec-2883">Uma palavra-chave de Keyword_taiwanese_national_id for encontrada.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2883">A keyword from Keyword_taiwanese_national_id is found.</span></span>
- <span data-ttu-id="ab3ec-2884">A soma de verificação passa.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2884">The checksum passes.</span></span>

```
<!-- Taiwanese National ID -->
<Entity id="4C7BFC34-8DD1-421D-8FB7-6C6182C2AF03" patternsProximity="300" recommendedConfidence="85">
      <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_taiwanese_national_id" />
          <Match idRef="Keyword_taiwanese_national_id" />
      </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="ab3ec-2885">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2885">Keywords</span></span>

#### <a name="keywordtaiwanesenationalid"></a><span data-ttu-id="ab3ec-2886">Keyword_taiwanese_national_id</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2886">Keyword_taiwanese_national_id</span></span>

- <span data-ttu-id="ab3ec-2887">身份證字號
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2887">身份證字號</span></span> 
- <span data-ttu-id="ab3ec-2888">身份證
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2888">身份證</span></span> 
- <span data-ttu-id="ab3ec-2889">身份證號碼
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2889">身份證號碼</span></span> 
- <span data-ttu-id="ab3ec-2890">身份證號
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2890">身份證號</span></span> 
- <span data-ttu-id="ab3ec-2891">身分證字號
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2891">身分證字號</span></span> 
- <span data-ttu-id="ab3ec-2892">身分證 </span><span class="sxs-lookup"><span data-stu-id="ab3ec-2892">身分證</span></span> 
- <span data-ttu-id="ab3ec-2893">身分證號碼
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2893">身分證號碼</span></span> 
- <span data-ttu-id="ab3ec-2894">身份證號
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2894">身份證號</span></span> 
- <span data-ttu-id="ab3ec-2895">身分證統一編號
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2895">身分證統一編號</span></span> 
- <span data-ttu-id="ab3ec-2896">國民身分證統一編號
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2896">國民身分證統一編號</span></span> 
- <span data-ttu-id="ab3ec-2897">簽名
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2897">簽名</span></span> 
- <span data-ttu-id="ab3ec-2898">蓋章
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2898">蓋章</span></span> 
- <span data-ttu-id="ab3ec-2899">簽名或蓋章

</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2899">簽名或蓋章</span></span> 
- <span data-ttu-id="ab3ec-2900">簽章</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2900">簽章</span></span>   
   
## <a name="taiwan-passport-number"></a><span data-ttu-id="ab3ec-2901">	Número de passaporte de Taiwan</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2901">Taiwan Passport Number</span></span>

### <a name="format"></a><span data-ttu-id="ab3ec-2902">Formato</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2902">Format</span></span>

- <span data-ttu-id="ab3ec-2903">Número de passaporte biométrica: nove dígitos</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2903">Biometric passport number: Nine digits</span></span>
- <span data-ttu-id="ab3ec-2904">Número de passaporte Non-biométrica: nove dígitos</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2904">Non-biometric passport number: Nine digits</span></span>

### <a name="pattern"></a><span data-ttu-id="ab3ec-2905">Padrão</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2905">Pattern</span></span>
<span data-ttu-id="ab3ec-2906">Número de passaporte biométrica:</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2906">Biometric passport number:</span></span>
- <span data-ttu-id="ab3ec-2907">O dígito "3" </span><span class="sxs-lookup"><span data-stu-id="ab3ec-2907">The digit "3"</span></span> 
- <span data-ttu-id="ab3ec-2908">Oito dígitos</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2908">Eight digits</span></span>

<span data-ttu-id="ab3ec-2909">Número de passaporte Non-biométrica:</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2909">Non-biometric passport number:</span></span>
- <span data-ttu-id="ab3ec-2910">Nove dígitos</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2910">Nine digits</span></span>

### <a name="checksum"></a><span data-ttu-id="ab3ec-2911">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2911">Checksum</span></span>

<span data-ttu-id="ab3ec-2912">Não</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2912">No</span></span>

### <a name="definition"></a><span data-ttu-id="ab3ec-2913">Definição</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2913">Definition</span></span>

<span data-ttu-id="ab3ec-2914">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2914">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="ab3ec-2915">A expressão regular Regex_taiwan_passport encontra o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2915">The regular expression Regex_taiwan_passport finds content that matches the pattern.</span></span>
- <span data-ttu-id="ab3ec-2916">Uma palavra-chave de Keyword_taiwan_passport é encontrada.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2916">A keyword from Keyword_taiwan_passport is found.</span></span>

```
<!-- Taiwan Passport Number -->
<Entity id="e7251cb4-4c2c-41df-963e-924eb3dae04a" recommendedConfidence="75" patternsProximity="300">
  <Pattern confidenceLevel="75">
     <IdMatch idRef="Regex_taiwan_passport"/>
     <Match idRef="Keyword_taiwan_passport"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="ab3ec-2917">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2917">Keywords</span></span>

#### <a name="keywordtaiwanpassport"></a><span data-ttu-id="ab3ec-2918">Keyword_taiwan_passport</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2918">Keyword_taiwan_passport</span></span>

- <span data-ttu-id="ab3ec-2919">Número de passaporte ROC
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2919">ROC passport number</span></span> 
- <span data-ttu-id="ab3ec-2920">Número de passaporte</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2920">Passport number</span></span> 
- <span data-ttu-id="ab3ec-2921">Passport nenhum</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2921">Passport no</span></span> 
- <span data-ttu-id="ab3ec-2922">Núm de Passaporte
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2922">Passport Num</span></span> 
- <span data-ttu-id="ab3ec-2923">Passport #
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2923">Passport #</span></span> 
- <span data-ttu-id="ab3ec-2924">护照
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2924">护照</span></span> 
- <span data-ttu-id="ab3ec-2925">中華民國護照
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2925">中華民國護照</span></span> 
- <span data-ttu-id="ab3ec-2926">Zhōnghuá Mínguó hùzhào</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2926">Zhōnghuá Mínguó hùzhào</span></span>
   
## <a name="taiwan-resident-certificate-arctarc-number"></a><span data-ttu-id="ab3ec-2927">Número do Certificado de residente de Taiwan (ARC/TARC)</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2927">Taiwan Resident Certificate (ARC/TARC) Number</span></span>

### <a name="format"></a><span data-ttu-id="ab3ec-2928">Formato</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2928">Format</span></span>

<span data-ttu-id="ab3ec-2929">10 letras e dígitos</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2929">10 letters and digits</span></span>

### <a name="pattern"></a><span data-ttu-id="ab3ec-2930">Padrão</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2930">Pattern</span></span>

<span data-ttu-id="ab3ec-2931">10 letras e dígitos:</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2931">10 letters and digits:</span></span>
- <span data-ttu-id="ab3ec-2932">Duas letras (não diferenciam maiúsculas de minúsculas)</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2932">Two letters (not case sensitive)</span></span> 
- <span data-ttu-id="ab3ec-2933">Oito dígitos</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2933">Eight digits</span></span>

### <a name="checksum"></a><span data-ttu-id="ab3ec-2934">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2934">Checksum</span></span>

<span data-ttu-id="ab3ec-2935">Não</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2935">No</span></span>

### <a name="definition"></a><span data-ttu-id="ab3ec-2936">Definição</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2936">Definition</span></span>

<span data-ttu-id="ab3ec-2937">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2937">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="ab3ec-2938">A expressão regular Regex_taiwan_resident_certificate encontra o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2938">The regular expression Regex_taiwan_resident_certificate finds content that matches the pattern.</span></span>
- <span data-ttu-id="ab3ec-2939">Uma palavra-chave de Keyword_taiwan_resident_certificate é encontrada.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2939">A keyword from Keyword_taiwan_resident_certificate is found.</span></span>

```
<!-- Taiwan Resident Certificate (ARC/TARC) -->
<Entity id="48269fec-05ea-46ea-b326-f5623a58c6e9" recommendedConfidence="75" patternsProximity="300">
  <Pattern confidenceLevel="75">
     <IdMatch idRef="Regex_taiwan_resident_certificate"/>
     <Match idRef="Keyword_taiwan_resident_certificate"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="ab3ec-2940">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2940">Keywords</span></span>

#### <a name="keywordtaiwanresidentcertificate"></a><span data-ttu-id="ab3ec-2941">Keyword_taiwan_resident_certificate</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2941">Keyword_taiwan_resident_certificate</span></span>

- <span data-ttu-id="ab3ec-2942">Certificado de Residente
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2942">Resident Certificate</span></span> 
- <span data-ttu-id="ab3ec-2943">Cert residente</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2943">Resident Cert</span></span> 
- <span data-ttu-id="ab3ec-2944">Cert. de Residente
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2944">Resident Cert.</span></span> 
- <span data-ttu-id="ab3ec-2945">Cartão de identificação</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2945">Identification card</span></span> 
- <span data-ttu-id="ab3ec-2946">Certificado de Residente Alien
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2946">Alien Resident Certificate</span></span> 
- <span data-ttu-id="ab3ec-2947">ARC
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2947">ARC</span></span> 
- <span data-ttu-id="ab3ec-2948">Certificado de Residente da Área de Taiwan
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2948">Taiwan Area Resident Certificate</span></span> 
- <span data-ttu-id="ab3ec-2949">TARC
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2949">TARC</span></span> 
- <span data-ttu-id="ab3ec-2950">居留證
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2950">居留證</span></span> 
- <span data-ttu-id="ab3ec-2951">外僑居留證
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2951">外僑居留證</span></span> 
- <span data-ttu-id="ab3ec-2952">台灣地區居留證
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2952">台灣地區居留證</span></span> 
   
## <a name="uk-drivers-license-number"></a><span data-ttu-id="ab3ec-p141">Número de carteira de motorista do Reino Unido</span><span class="sxs-lookup"><span data-stu-id="ab3ec-p141">U.K. Driver's License Number</span></span>

### <a name="format"></a><span data-ttu-id="ab3ec-2955">Formato</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2955">Format</span></span>

<span data-ttu-id="ab3ec-2956">Combinação de 18 letras e dígitos no formato especificado</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2956">Combination of 18 letters and digits in the specified format</span></span>

### <a name="pattern"></a><span data-ttu-id="ab3ec-2957">Padrão</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2957">Pattern</span></span>

<span data-ttu-id="ab3ec-2958">18 letras e dígitos:</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2958">18 letters and digits:</span></span>
- <span data-ttu-id="ab3ec-2959">Cinco letras (não diferenciam maiúsculas de minúsculas) ou o dígito "9" em vez de uma letra</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2959">Five letters (not case sensitive) or the digit "9" in place of a letter</span></span> 
- <span data-ttu-id="ab3ec-2960">Um dígito</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2960">One digit</span></span> 
- <span data-ttu-id="ab3ec-2961">Cinco dígitos no formato de data DDMMA para data de nascimento</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2961">Five digits in the date format DDMMY for date of birth</span></span> 
- <span data-ttu-id="ab3ec-2962">Duas letras (não diferenciam maiúsculas de minúsculas) ou o dígito "9" em vez de uma letra</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2962">Two letters (not case sensitive) or the digit "9" in place of a letter</span></span> 
- <span data-ttu-id="ab3ec-2963">Cinco dígitos</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2963">Five digits</span></span>

### <a name="checksum"></a><span data-ttu-id="ab3ec-2964">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2964">Checksum</span></span>

<span data-ttu-id="ab3ec-2965">Sim</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2965">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="ab3ec-2966">Definição</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2966">Definition</span></span>

<span data-ttu-id="ab3ec-2967">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2967">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="ab3ec-2968">A função Func_uk_drivers_license localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2968">The function Func_uk_drivers_license finds content that matches the pattern.</span></span>
- <span data-ttu-id="ab3ec-2969">Uma palavra-chave de Keyword_uk_drivers_license for encontrada.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2969">A keyword from Keyword_uk_drivers_license is found.</span></span>
- <span data-ttu-id="ab3ec-2970">A soma de verificação passa.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2970">The checksum passes.</span></span>

```
<!-- U.K. Driver's License Number -->
<Entity id="f93de4be-d94c-40df-a8be-461738047551" patternsProximity="300" recommendedConfidence="75">
    <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_uk_drivers_license" />
        <Match idRef="Keyword_uk_drivers_license" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="ab3ec-2971">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2971">Keywords</span></span>

#### <a name="keywordukdriverslicense"></a><span data-ttu-id="ab3ec-2972">Keyword_uk_drivers_license</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2972">Keyword_uk_drivers_license</span></span>

- <span data-ttu-id="ab3ec-2973">DVLA
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2973">DVLA</span></span> 
- <span data-ttu-id="ab3ec-2974">light vans
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2974">light vans</span></span> 
- <span data-ttu-id="ab3ec-2975">quadbikes
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2975">quadbikes</span></span> 
- <span data-ttu-id="ab3ec-2976">motor cars
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2976">motor cars</span></span> 
- <span data-ttu-id="ab3ec-2977">125cc</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2977">125cc</span></span> 
- <span data-ttu-id="ab3ec-2978">sidecar
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2978">sidecar</span></span> 
- <span data-ttu-id="ab3ec-2979">tricycles
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2979">tricycles</span></span> 
- <span data-ttu-id="ab3ec-2980">motorcycles
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2980">motorcycles</span></span> 
- <span data-ttu-id="ab3ec-2981">photocard licence
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2981">photocard licence</span></span> 
- <span data-ttu-id="ab3ec-2982">learner drivers
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2982">learner drivers</span></span> 
- <span data-ttu-id="ab3ec-2983">licence holder
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2983">licence holder</span></span> 
- <span data-ttu-id="ab3ec-2984">licence holders
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2984">licence holders</span></span> 
- <span data-ttu-id="ab3ec-2985">driving licences
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2985">driving licences</span></span> 
- <span data-ttu-id="ab3ec-2986">driving licence
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2986">driving licence</span></span> 
- <span data-ttu-id="ab3ec-2987">dual control car
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2987">dual control car</span></span> 
   
## <a name="uk-electoral-roll-number"></a><span data-ttu-id="ab3ec-p142">Número de Título de Eleitor do Reino Unido</span><span class="sxs-lookup"><span data-stu-id="ab3ec-p142">U.K. Electoral Roll Number</span></span>

### <a name="format"></a><span data-ttu-id="ab3ec-2990">Formato</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2990">Format</span></span>

<span data-ttu-id="ab3ec-2991">Duas letras seguidas por 1 a 4 dígitos</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2991">Two letters followed by 1-4 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="ab3ec-2992">Padrão</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2992">Pattern</span></span>

<span data-ttu-id="ab3ec-2993">Duas letras (não diferencia maiúsculas de minúsculas) seguidas de 1 a 4 anos</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2993">Two letters (not case sensitive) followed by 1-4 numbers</span></span>

### <a name="checksum"></a><span data-ttu-id="ab3ec-2994">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2994">Checksum</span></span>

<span data-ttu-id="ab3ec-2995">Não</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2995">No</span></span>

### <a name="definition"></a><span data-ttu-id="ab3ec-2996">Definição</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2996">Definition</span></span>

<span data-ttu-id="ab3ec-2997">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2997">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="ab3ec-2998">A expressão regular Regex_uk_electoral localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2998">The regular expression Regex_uk_electoral finds content that matches the pattern.</span></span>
- <span data-ttu-id="ab3ec-2999">Uma palavra-chave de Keyword_uk_electoral for encontrada.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-2999">A keyword from Keyword_uk_electoral is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="ab3ec-3000">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3000">Keywords</span></span>

#### <a name="keywordukelectoral"></a><span data-ttu-id="ab3ec-3001">Keyword_uk_electoral</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3001">Keyword_uk_electoral</span></span>

- <span data-ttu-id="ab3ec-3002">council nomination
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3002">council nomination</span></span> 
- <span data-ttu-id="ab3ec-3003">nomination form
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3003">nomination form</span></span> 
- <span data-ttu-id="ab3ec-3004">electoral register

</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3004">electoral register</span></span> 
- <span data-ttu-id="ab3ec-3005">electoral roll</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3005">electoral roll</span></span>

   
## <a name="uk-national-health-service-number"></a><span data-ttu-id="ab3ec-p143">Número do serviço de saúde nacional do Reino Unido</span><span class="sxs-lookup"><span data-stu-id="ab3ec-p143">U.K. National Health Service Number</span></span>

### <a name="format"></a><span data-ttu-id="ab3ec-3008">Formato</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3008">Format</span></span>

<span data-ttu-id="ab3ec-3009">10 a 17 dígitos separados por espaços</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3009">10-17 digits separated by spaces</span></span>

### <a name="pattern"></a><span data-ttu-id="ab3ec-3010">Padrão</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3010">Pattern</span></span>

<span data-ttu-id="ab3ec-3011">10 a 17 dígitos:</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3011">10-17 digits:</span></span>
- <span data-ttu-id="ab3ec-3012">3 ou 10 dígitos</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3012">Either 3 or 10 digits</span></span> 
- <span data-ttu-id="ab3ec-3013">Um espaço</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3013">A space</span></span> 
- <span data-ttu-id="ab3ec-3014">Três dígitos</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3014">Three digits</span></span> 
- <span data-ttu-id="ab3ec-3015">Um espaço</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3015">A space</span></span> 
- <span data-ttu-id="ab3ec-3016">Quatro dígitos</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3016">Four digits</span></span>

### <a name="checksum"></a><span data-ttu-id="ab3ec-3017">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3017">Checksum</span></span>

<span data-ttu-id="ab3ec-3018">Sim</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3018">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="ab3ec-3019">Definição</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3019">Definition</span></span>

<span data-ttu-id="ab3ec-3020">Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3020">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="ab3ec-3021">A função Func_uk_nhs_number localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3021">The function Func_uk_nhs_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="ab3ec-3022">Uma das seguintes opções for verdadeira:</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3022">One of the following is true:</span></span>
    - <span data-ttu-id="ab3ec-3023">Uma palavra-chave de Keyword_uk_nhs_number for encontrada.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3023">A keyword from Keyword_uk_nhs_number is found.</span></span>
    - <span data-ttu-id="ab3ec-3024">Uma palavra-chave de Keyword_uk_nhs_number1 for encontrada.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3024">A keyword from Keyword_uk_nhs_number1 is found.</span></span>
    - <span data-ttu-id="ab3ec-3025">Uma palavra-chave de Keyword_uk_nhs_number_dob for encontrada.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3025">A keyword from Keyword_uk_nhs_number_dob is found.</span></span>
- <span data-ttu-id="ab3ec-3026">A soma de verificação passa.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3026">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="ab3ec-3027">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3027">Keywords</span></span>
   
#### <a name="keyworduknhsnumber"></a><span data-ttu-id="ab3ec-3028">Keyword_uk_nhs_number</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3028">Keyword_uk_nhs_number</span></span>

- <span data-ttu-id="ab3ec-3029">national health service
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3029">national health service</span></span> 
- <span data-ttu-id="ab3ec-3030">nhs
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3030">nhs</span></span> 
- <span data-ttu-id="ab3ec-3031">health services authority

</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3031">health services authority</span></span> 
- <span data-ttu-id="ab3ec-3032">health authority</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3032">health authority</span></span>

#### <a name="keyworduknhsnumber1"></a><span data-ttu-id="ab3ec-3033">Keyword_uk_nhs_number1</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3033">Keyword_uk_nhs_number1</span></span>

- <span data-ttu-id="ab3ec-3034">patient id
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3034">patient id</span></span> 
- <span data-ttu-id="ab3ec-3035">patient identification
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3035">patient identification</span></span> 
- <span data-ttu-id="ab3ec-3036">patient no

</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3036">patient no</span></span> 
- <span data-ttu-id="ab3ec-3037">patient number</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3037">patient number</span></span>

#### <a name="keyworduknhsnumberdob"></a><span data-ttu-id="ab3ec-3038">Keyword_uk_nhs_number_dob</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3038">Keyword_uk_nhs_number_dob</span></span>

- <span data-ttu-id="ab3ec-3039">GP</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3039">GP</span></span> 
- <span data-ttu-id="ab3ec-3040">DOB
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3040">DOB</span></span> 
- <span data-ttu-id="ab3ec-3041">D.O.B</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3041">D.O.B</span></span> 
- <span data-ttu-id="ab3ec-3042">Date of Birth
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3042">Date of Birth</span></span> 
- <span data-ttu-id="ab3ec-3043">Birth Date
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3043">Birth Date</span></span> 
   
## <a name="uk-national-insurance-number-nino"></a><span data-ttu-id="ab3ec-p144">Número de seguro nacional do Reino Unido (NINO)</span><span class="sxs-lookup"><span data-stu-id="ab3ec-p144">U.K. National Insurance Number (NINO)</span></span>

### <a name="format"></a><span data-ttu-id="ab3ec-3046">Formato</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3046">Format</span></span>

<span data-ttu-id="ab3ec-3047">7 caracteres ou 9 caracteres separados por espaços nem traços</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3047">7 characters or 9 characters separated by spaces or dashes</span></span>

### <a name="pattern"></a><span data-ttu-id="ab3ec-3048">Padrão</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3048">Pattern</span></span>

<span data-ttu-id="ab3ec-3049">Dois padrões possíveis:</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3049">Two possible patterns:</span></span>

- <span data-ttu-id="ab3ec-3050">Duas letras (NINOs válidos usam apenas determinados caracteres nesse prefixo, que valida a este padrão; não diferencia maiusculas de minúsculas)</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3050">Two letters (valid NINOs use only certain characters in this prefix, which this pattern validates; not case sensitive)</span></span>
- <span data-ttu-id="ab3ec-3051">Seis dígitos</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3051">Six digits</span></span>
- <span data-ttu-id="ab3ec-3052">Qualquer um dos '', 'B', 'C, ou tinha ' (como o prefixo, apenas determinados caracteres são permitidos no sufixo; não diferenciam maiusculas de minúsculas)</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3052">Either 'A', 'B', 'C', or 'D' (like the prefix, only certain characters are allowed in the suffix; not case sensitive)</span></span>

<span data-ttu-id="ab3ec-3053">OU</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3053">OR</span></span>

- <span data-ttu-id="ab3ec-3054">Duas letras</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3054">Two letters</span></span>
- <span data-ttu-id="ab3ec-3055">Um espaço ou um traço</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3055">A space or dash</span></span>
- <span data-ttu-id="ab3ec-3056">Dois dígitos</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3056">Two digits</span></span>
- <span data-ttu-id="ab3ec-3057">Um espaço ou um traço</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3057">A space or dash</span></span>
- <span data-ttu-id="ab3ec-3058">Dois dígitos</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3058">Two digits</span></span>
- <span data-ttu-id="ab3ec-3059">Um espaço ou um traço</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3059">A space or dash</span></span>
- <span data-ttu-id="ab3ec-3060">Dois dígitos</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3060">Two digits</span></span>
- <span data-ttu-id="ab3ec-3061">Um espaço ou um traço</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3061">A space or dash</span></span>
- <span data-ttu-id="ab3ec-3062">Qualquer um dos 'A', 'B', 'C, ou tinha '</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3062">Either 'A', 'B', 'C', or 'D'</span></span>

### <a name="checksum"></a><span data-ttu-id="ab3ec-3063">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3063">Checksum</span></span>

<span data-ttu-id="ab3ec-3064">Não</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3064">No</span></span>

### <a name="definition"></a><span data-ttu-id="ab3ec-3065">Definição</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3065">Definition</span></span>

<span data-ttu-id="ab3ec-3066">Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3066">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="ab3ec-3067">A função Func_uk_nino localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3067">The function Func_uk_nino finds content that matches the pattern.</span></span>
- <span data-ttu-id="ab3ec-3068">Uma palavra-chave de Keyword_uk_nino for encontrada.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3068">A keyword from Keyword_uk_nino is found.</span></span>

<span data-ttu-id="ab3ec-3069">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3069">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="ab3ec-3070">A função Func_uk_nino localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3070">The function Func_uk_nino finds content that matches the pattern.</span></span>
- <span data-ttu-id="ab3ec-3071">Nenhuma palavra-chave de Keyword_uk_nino for encontrada.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3071">No keyword from Keyword_uk_nino is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="ab3ec-3072">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3072">Keywords</span></span>

#### <a name="keyworduknino"></a><span data-ttu-id="ab3ec-3073">Keyword_uk_nino</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3073">Keyword_uk_nino</span></span>

- <span data-ttu-id="ab3ec-3074">national insurance number
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3074">national insurance number</span></span> 
- <span data-ttu-id="ab3ec-3075">national insurance contributions
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3075">national insurance contributions</span></span> 
- <span data-ttu-id="ab3ec-3076">protection act
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3076">protection act</span></span> 
- <span data-ttu-id="ab3ec-3077">insurance
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3077">insurance</span></span> 
- <span data-ttu-id="ab3ec-3078">social security number
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3078">social security number</span></span> 
- <span data-ttu-id="ab3ec-3079">insurance application
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3079">insurance application</span></span> 
- <span data-ttu-id="ab3ec-3080">medical application
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3080">medical application</span></span> 
- <span data-ttu-id="ab3ec-3081">social insurance
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3081">social insurance</span></span> 
- <span data-ttu-id="ab3ec-3082">medical attention
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3082">medical attention</span></span> 
- <span data-ttu-id="ab3ec-3083">seguridade social</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3083">social security</span></span> 
- <span data-ttu-id="ab3ec-3084">great britain
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3084">great britain</span></span> 
- <span data-ttu-id="ab3ec-3085">insurance
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3085">insurance</span></span>    
   
## <a name="us--uk-passport-number"></a><span data-ttu-id="ab3ec-p145">Número de passaporte dos EUA/Reino Unido</span><span class="sxs-lookup"><span data-stu-id="ab3ec-p145">U.S. / U.K. Passport Number</span></span>

### <a name="format"></a><span data-ttu-id="ab3ec-3088">Formato</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3088">Format</span></span>

<span data-ttu-id="ab3ec-3089">Nove dígitos</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3089">Nine digits</span></span>

### <a name="pattern"></a><span data-ttu-id="ab3ec-3090">Padrão</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3090">Pattern</span></span>

<span data-ttu-id="ab3ec-3091">Nove dígitos consecutivos</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3091">Nine consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="ab3ec-3092">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3092">Checksum</span></span>

<span data-ttu-id="ab3ec-3093">Não</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3093">No</span></span>

### <a name="definition"></a><span data-ttu-id="ab3ec-3094">Definição</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3094">Definition</span></span>

<span data-ttu-id="ab3ec-3095">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3095">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="ab3ec-3096">A função Func_usa_uk_passport localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3096">The function Func_usa_uk_passport finds content that matches the pattern.</span></span>
- <span data-ttu-id="ab3ec-3097">Uma palavra-chave de Keyword_passport for encontrada.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3097">A keyword from Keyword_passport is found.</span></span>

```
<Entity id="178ec42a-18b4-47cc-85c7-d62c92fd67f8" patternsProximity="300" recommendedConfidence="75">
    <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_usa_uk_passport" />
        <Match idRef="Keyword_passport" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="ab3ec-3098">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3098">Keywords</span></span>

#### <a name="keywordpassport"></a><span data-ttu-id="ab3ec-3099">Keyword_passport</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3099">Keyword_passport</span></span>

- <span data-ttu-id="ab3ec-3100">Passport Number</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3100">Passport Number</span></span> 
- <span data-ttu-id="ab3ec-3101">
Passport No</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3101">Passport No</span></span> 
- <span data-ttu-id="ab3ec-3102">Passport #
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3102">Passport #</span></span> 
- <span data-ttu-id="ab3ec-3103">Passport#
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3103">Passport#</span></span> 
- <span data-ttu-id="ab3ec-3104">PassportID</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3104">PassportID</span></span> 
- <span data-ttu-id="ab3ec-3105">Passportno
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3105">Passportno</span></span> 
- <span data-ttu-id="ab3ec-3106">passportnumber
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3106">passportnumber</span></span> 
- <span data-ttu-id="ab3ec-3107">パスポート</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3107">パスポート</span></span> 
- <span data-ttu-id="ab3ec-3108">パスポート番号
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3108">パスポート番号</span></span> 
- <span data-ttu-id="ab3ec-3109">パスポートのNum
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3109">パスポートのNum</span></span> 
- <span data-ttu-id="ab3ec-3110">パスポート＃
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3110">パスポート＃</span></span> 
- <span data-ttu-id="ab3ec-3111">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3111">Numéro de passeport</span></span> 
- <span data-ttu-id="ab3ec-3112">
Passeport n °</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3112">Passeport n °</span></span> 
- <span data-ttu-id="ab3ec-3113">Passeport Non
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3113">Passeport Non</span></span> 
- <span data-ttu-id="ab3ec-3114">Passeport #
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3114">Passeport #</span></span> 
- <span data-ttu-id="ab3ec-3115">Passeport#
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3115">Passeport#</span></span> 
- <span data-ttu-id="ab3ec-3116">PasseportNon</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3116">PasseportNon</span></span> 
- <span data-ttu-id="ab3ec-3117">Passeportn °
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3117">Passeportn °</span></span> 
   
## <a name="us-bank-account-number"></a><span data-ttu-id="ab3ec-3118">Número de conta bancária dos EUA</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3118">U.S. Bank Account Number</span></span>

### <a name="format"></a><span data-ttu-id="ab3ec-3119">Formato</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3119">Format</span></span>

<span data-ttu-id="ab3ec-3120">8 a 17 dígitos</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3120">8-17 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="ab3ec-3121">Padrão</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3121">Pattern</span></span>

<span data-ttu-id="ab3ec-3122">8 a 17 dígitos consecutivos</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3122">8-17 consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="ab3ec-3123">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3123">Checksum</span></span>

<span data-ttu-id="ab3ec-3124">Não</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3124">No</span></span>

### <a name="definition"></a><span data-ttu-id="ab3ec-3125">Definição</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3125">Definition</span></span>

<span data-ttu-id="ab3ec-3126">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3126">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="ab3ec-3127">A expressão regular Regex_usa_bank_account_number localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3127">The regular expression Regex_usa_bank_account_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="ab3ec-3128">Uma palavra-chave de Keyword_usa_Bank_Account for encontrada.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3128">A keyword from Keyword_usa_Bank_Account is found.</span></span>

```
<!-- U.S. Bank Account Number -->
<Entity id="a2ce32a8-f935-4bb6-8e96-2a5157672e2c" patternsProximity="300" recommendedConfidence="75">
    <Pattern confidenceLevel="75">
        <IdMatch idRef="Regex_usa_bank_account_number" />
        <Match idRef="Keyword_usa_Bank_Account" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="ab3ec-3129">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3129">Keywords</span></span>

#### <a name="keywordusabankaccount"></a><span data-ttu-id="ab3ec-3130">Keyword_usa_Bank_Account</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3130">Keyword_usa_Bank_Account</span></span>

- <span data-ttu-id="ab3ec-3131">Checking Account Number
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3131">Checking Account Number</span></span> 
- <span data-ttu-id="ab3ec-3132">Checking Account
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3132">Checking Account</span></span> 
- <span data-ttu-id="ab3ec-3133">Checking Account #
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3133">Checking Account #</span></span> 
- <span data-ttu-id="ab3ec-3134">Checking Acct Number
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3134">Checking Acct Number</span></span> 
- <span data-ttu-id="ab3ec-3135">Checking Acct #
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3135">Checking Acct #</span></span> 
- <span data-ttu-id="ab3ec-3136">Checking Acct No.
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3136">Checking Acct No.</span></span> 
- <span data-ttu-id="ab3ec-3137">Checking Account No.
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3137">Checking Account No.</span></span> 
- <span data-ttu-id="ab3ec-3138">Bank Account Number
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3138">Bank Account Number</span></span> 
- <span data-ttu-id="ab3ec-3139">Bank Account #
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3139">Bank Account #</span></span> 
- <span data-ttu-id="ab3ec-3140">Bank Acct Number
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3140">Bank Acct Number</span></span> 
- <span data-ttu-id="ab3ec-3141">Bank Acct #
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3141">Bank Acct #</span></span> 
- <span data-ttu-id="ab3ec-3142">Bank Acct No.
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3142">Bank Acct No.</span></span> 
- <span data-ttu-id="ab3ec-3143">Bank Account No.
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3143">Bank Account No.</span></span> 
- <span data-ttu-id="ab3ec-3144">Savings Account Number
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3144">Savings Account Number</span></span> 
- <span data-ttu-id="ab3ec-3145">Savings Account.
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3145">Savings Account.</span></span> 
- <span data-ttu-id="ab3ec-3146">Savings Account #
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3146">Savings Account #</span></span> 
- <span data-ttu-id="ab3ec-3147">Savings Acct Number
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3147">Savings Acct Number</span></span> 
- <span data-ttu-id="ab3ec-3148">Savings Acct #
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3148">Savings Acct #</span></span> 
- <span data-ttu-id="ab3ec-3149">Savings Acct No.
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3149">Savings Acct No.</span></span> 
- <span data-ttu-id="ab3ec-3150">Savings Account No.
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3150">Savings Account No.</span></span> 
- <span data-ttu-id="ab3ec-3151">Debit Account Number
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3151">Debit Account Number</span></span> 
- <span data-ttu-id="ab3ec-3152">Debit Account
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3152">Debit Account</span></span> 
- <span data-ttu-id="ab3ec-3153">Debit Account #
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3153">Debit Account #</span></span> 
- <span data-ttu-id="ab3ec-3154">Debit Acct Number
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3154">Debit Acct Number</span></span> 
- <span data-ttu-id="ab3ec-3155">Debit Acct #
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3155">Debit Acct #</span></span> 
- <span data-ttu-id="ab3ec-3156">Debit Acct No.
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3156">Debit Acct No.</span></span> 
- <span data-ttu-id="ab3ec-3157">Debit Account No.
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3157">Debit Account No.</span></span> 
   
## <a name="us-drivers-license-number"></a><span data-ttu-id="ab3ec-3158">Número de carteira de motorista dos EUA</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3158">U.S. Driver's License Number</span></span>

### <a name="format"></a><span data-ttu-id="ab3ec-3159">Formato</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3159">Format</span></span>

<span data-ttu-id="ab3ec-3160">Depende do estado</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3160">Depends on the state</span></span>

### <a name="pattern"></a><span data-ttu-id="ab3ec-3161">Padrão</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3161">Pattern</span></span>

<span data-ttu-id="ab3ec-3162">Depende do estado – por exemplo, Nova York:</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3162">Depends on the state -- for example, New York:</span></span>
- <span data-ttu-id="ab3ec-3163">Nove dígitos formatado como ddd ddd ddd corresponderá.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3163">Nine digits formatted like ddd ddd ddd will match.</span></span>
- <span data-ttu-id="ab3ec-3164">Nove dígitos como ddddddddd não corresponderá.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3164">Nine digits like ddddddddd will not match.</span></span>

### <a name="checksum"></a><span data-ttu-id="ab3ec-3165">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3165">Checksum</span></span>

<span data-ttu-id="ab3ec-3166">Não</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3166">No</span></span>

### <a name="definition"></a><span data-ttu-id="ab3ec-3167">Definição</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3167">Definition</span></span>

<span data-ttu-id="ab3ec-3168">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3168">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="ab3ec-3169">A função Func_new_york_drivers_license_number localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3169">The function Func_new_york_drivers_license_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="ab3ec-3170">Uma palavra-chave de Keyword_[state_name]_drivers_license_name for encontrada.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3170">A keyword from Keyword_[state_name]_drivers_license_name is found.</span></span>
- <span data-ttu-id="ab3ec-3171">Uma palavra-chave de Keyword_us_drivers_license é encontrada.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3171">A keyword from Keyword_us_drivers_license is found.</span></span>

<span data-ttu-id="ab3ec-3172">Uma política de DLP tem 65% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3172">A DLP policy is 65% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="ab3ec-3173">A função Func_new_york_drivers_license_number localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3173">The function Func_new_york_drivers_license_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="ab3ec-3174">Uma palavra-chave de Keyword_[state_name]_drivers_license_name for encontrada.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3174">A keyword from Keyword_[state_name]_drivers_license_name is found.</span></span>
- <span data-ttu-id="ab3ec-3175">Uma palavra-chave de Keyword_us_drivers_license_abbreviations for encontrada.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3175">A keyword from Keyword_us_drivers_license_abbreviations is found.</span></span>
- <span data-ttu-id="ab3ec-3176">Nenhuma palavra-chave de Keyword_us_drivers_license for encontrada.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3176">No keyword from Keyword_us_drivers_license is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="ab3ec-3177">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3177">Keywords</span></span>

#### <a name="keywordusdriverslicenseabbreviations"></a><span data-ttu-id="ab3ec-3178">Keyword_us_drivers_license_abbreviations</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3178">Keyword_us_drivers_license_abbreviations</span></span>

- <span data-ttu-id="ab3ec-3179">DL</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3179">DL</span></span> 
- <span data-ttu-id="ab3ec-3180">DLS</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3180">DLS</span></span> 
- <span data-ttu-id="ab3ec-3181">CDL</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3181">CDL</span></span> 
- <span data-ttu-id="ab3ec-3182">CDLS</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3182">CDLS</span></span> 
- <span data-ttu-id="ab3ec-3183">ID</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3183">ID</span></span> 
- <span data-ttu-id="ab3ec-3184">IDs</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3184">IDs</span></span> 
- <span data-ttu-id="ab3ec-3185">DL#</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3185">DL#</span></span> 
- <span data-ttu-id="ab3ec-3186">
DLS#
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3186">DLS#</span></span> 
- <span data-ttu-id="ab3ec-3187">CDL#
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3187">CDL#</span></span> 
- <span data-ttu-id="ab3ec-3188">CDLS#
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3188">CDLS#</span></span> 
- <span data-ttu-id="ab3ec-3189">ID#</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3189">ID#</span></span>
- <span data-ttu-id="ab3ec-3190">
IDs#
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3190">IDs#</span></span> 
- <span data-ttu-id="ab3ec-3191">número de identificação</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3191">ID number</span></span> 
- <span data-ttu-id="ab3ec-3192">ID numbers
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3192">ID numbers</span></span> 
- <span data-ttu-id="ab3ec-3193">LIC</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3193">LIC</span></span> 
- <span data-ttu-id="ab3ec-3194">LIC#
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3194">LIC#</span></span> 

#### <a name="keywordusdriverslicense"></a><span data-ttu-id="ab3ec-3195">Keyword_us_drivers_license</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3195">Keyword_us_drivers_license</span></span>

- <span data-ttu-id="ab3ec-3196">DriverLic</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3196">DriverLic</span></span> 
- <span data-ttu-id="ab3ec-3197">DriverLics</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3197">DriverLics</span></span> 
- <span data-ttu-id="ab3ec-3198">DriverLicense</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3198">DriverLicense</span></span> 
- <span data-ttu-id="ab3ec-3199">DriverLicenses</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3199">DriverLicenses</span></span> 
- <span data-ttu-id="ab3ec-3200">Driver Lic</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3200">Driver Lic</span></span> 
- <span data-ttu-id="ab3ec-3201">Driver Lics</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3201">Driver Lics</span></span> 
- <span data-ttu-id="ab3ec-3202">Driver de licença</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3202">Driver License</span></span> 
- <span data-ttu-id="ab3ec-3203">Licenças de driver</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3203">Driver Licenses</span></span> 
- <span data-ttu-id="ab3ec-3204">DriversLic</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3204">DriversLic</span></span> 
- <span data-ttu-id="ab3ec-3205">DriversLics</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3205">DriversLics</span></span> 
- <span data-ttu-id="ab3ec-3206">CarteiraDeMotorista</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3206">DriversLicense</span></span> 
- <span data-ttu-id="ab3ec-3207">DriversLicenses</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3207">DriversLicenses</span></span> 
- <span data-ttu-id="ab3ec-3208">Drivers Lic</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3208">Drivers Lic</span></span> 
- <span data-ttu-id="ab3ec-3209">Drivers Lics</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3209">Drivers Lics</span></span> 
- <span data-ttu-id="ab3ec-3210">Carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3210">Drivers License</span></span> 
- <span data-ttu-id="ab3ec-3211">Licenças de drivers</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3211">Drivers Licenses</span></span> 
- <span data-ttu-id="ab3ec-3212">Driver'Lic</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3212">Driver'Lic</span></span> 
- <span data-ttu-id="ab3ec-3213">Driver'Lics</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3213">Driver'Lics</span></span> 
- <span data-ttu-id="ab3ec-3214">Driver'License</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3214">Driver'License</span></span> 
- <span data-ttu-id="ab3ec-3215">Driver'Licenses</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3215">Driver'Licenses</span></span> 
- <span data-ttu-id="ab3ec-3216">Driver' Lic</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3216">Driver' Lic</span></span> 
- <span data-ttu-id="ab3ec-3217">Driver' Lics</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3217">Driver' Lics</span></span> 
- <span data-ttu-id="ab3ec-3218">Driver' licença</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3218">Driver' License</span></span> 
- <span data-ttu-id="ab3ec-3219">Driver' licenças</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3219">Driver' Licenses</span></span>
- <span data-ttu-id="ab3ec-3220">Driver'sLic</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3220">Driver'sLic</span></span> 
- <span data-ttu-id="ab3ec-3221">Driver'sLics</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3221">Driver'sLics</span></span> 
- <span data-ttu-id="ab3ec-3222">Driver'sLicense</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3222">Driver'sLicense</span></span> 
- <span data-ttu-id="ab3ec-3223">Driver'sLicenses</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3223">Driver'sLicenses</span></span> 
- <span data-ttu-id="ab3ec-3224">Lic do driver</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3224">Driver's Lic</span></span> 
- <span data-ttu-id="ab3ec-3225">Lics do driver</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3225">Driver's Lics</span></span> 
- <span data-ttu-id="ab3ec-3226">De motorista carteira</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3226">Driver's License</span></span> 
- <span data-ttu-id="ab3ec-3227">Licenças de motorista</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3227">Driver's Licenses</span></span> 
- <span data-ttu-id="ab3ec-3228">identification number
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3228">identification number</span></span> 
- <span data-ttu-id="ab3ec-3229">identification numbers
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3229">identification numbers</span></span> 
- <span data-ttu-id="ab3ec-3230">identification #
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3230">identification #</span></span> 
- <span data-ttu-id="ab3ec-3231">cartão de identificação</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3231">id card</span></span> 
- <span data-ttu-id="ab3ec-3232">cartões de ID</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3232">id cards</span></span> 
- <span data-ttu-id="ab3ec-3233">cartão de identificação</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3233">identification card</span></span> 
- <span data-ttu-id="ab3ec-3234">cartões de identificação</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3234">identification cards</span></span> 
- <span data-ttu-id="ab3ec-3235">DriverLic #</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3235">DriverLic#</span></span> 
- <span data-ttu-id="ab3ec-3236">DriverLics #</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3236">DriverLics#</span></span> 
- <span data-ttu-id="ab3ec-3237">DriverLicense #</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3237">DriverLicense#</span></span> 
- <span data-ttu-id="ab3ec-3238">DriverLicenses #</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3238">DriverLicenses#</span></span> 
- <span data-ttu-id="ab3ec-3239">Driver Lic#</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3239">Driver Lic#</span></span> 
- <span data-ttu-id="ab3ec-3240">
Driver Lics#
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3240">Driver Lics#</span></span> 
- <span data-ttu-id="ab3ec-3241">Licença do driver #</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3241">Driver License#</span></span> 
- <span data-ttu-id="ab3ec-3242">Driver licenças #</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3242">Driver Licenses#</span></span> 
- <span data-ttu-id="ab3ec-3243">DriversLic #</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3243">DriversLic#</span></span> 
- <span data-ttu-id="ab3ec-3244">DriversLics #</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3244">DriversLics#</span></span> 
- <span data-ttu-id="ab3ec-3245">CarteiraDeMotorista #</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3245">DriversLicense#</span></span> 
- <span data-ttu-id="ab3ec-3246">DriversLicenses #</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3246">DriversLicenses#</span></span> 
- <span data-ttu-id="ab3ec-3247">Drivers Lic #</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3247">Drivers Lic#</span></span> 
- <span data-ttu-id="ab3ec-3248">Drivers Lics #</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3248">Drivers Lics#</span></span> 
- <span data-ttu-id="ab3ec-3249">Drivers licença #</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3249">Drivers License#</span></span> 
- <span data-ttu-id="ab3ec-3250">Drivers licenças #</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3250">Drivers Licenses#</span></span> 
- <span data-ttu-id="ab3ec-3251">Driver'Lic#
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3251">Driver'Lic#</span></span> 
- <span data-ttu-id="ab3ec-3252">Driver'Lics#
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3252">Driver'Lics#</span></span> 
- <span data-ttu-id="ab3ec-3253">Driver'License#
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3253">Driver'License#</span></span> 
- <span data-ttu-id="ab3ec-3254">Driver'Licenses#
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3254">Driver'Licenses#</span></span> 
- <span data-ttu-id="ab3ec-3255">Driver' Lic#
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3255">Driver' Lic#</span></span> 
- <span data-ttu-id="ab3ec-3256">Driver' Lics#
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3256">Driver' Lics#</span></span> 
- <span data-ttu-id="ab3ec-3257">Driver' License#
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3257">Driver' License#</span></span> 
- <span data-ttu-id="ab3ec-3258">Driver' Licenses#
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3258">Driver' Licenses#</span></span> 
- <span data-ttu-id="ab3ec-3259">Driver'sLic #</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3259">Driver'sLic#</span></span> 
- <span data-ttu-id="ab3ec-3260">Driver'sLics #</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3260">Driver'sLics#</span></span> 
- <span data-ttu-id="ab3ec-3261">Driver'sLicense #</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3261">Driver'sLicense#</span></span> 
- <span data-ttu-id="ab3ec-3262">Driver'sLicenses #</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3262">Driver'sLicenses#</span></span> 
- <span data-ttu-id="ab3ec-3263">Driver's Lic#
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3263">Driver's Lic#</span></span> 
- <span data-ttu-id="ab3ec-3264">Driver's Lics#
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3264">Driver's Lics#</span></span> 
- <span data-ttu-id="ab3ec-3265">Driver's License#
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3265">Driver's License#</span></span> 
- <span data-ttu-id="ab3ec-3266">Driver's Licenses#
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3266">Driver's Licenses#</span></span> 
- <span data-ttu-id="ab3ec-3267">cartão de identificação #</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3267">id card#</span></span> 
- <span data-ttu-id="ab3ec-3268">id cards#
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3268">id cards#</span></span> 
- <span data-ttu-id="ab3ec-3269">identification card#
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3269">identification card#</span></span> 
- <span data-ttu-id="ab3ec-3270">identification cards#
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3270">identification cards#</span></span> 


#### <a name="keywordstatenamedriverslicensename"></a><span data-ttu-id="ab3ec-3271">Keyword_[state_name]_drivers_license_name</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3271">Keyword_[state_name]_drivers_license_name</span></span>

- <span data-ttu-id="ab3ec-3272">Abreviação do estado (por exemplo, "NY")
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3272">State abbreviation (for example, "NY")</span></span> 
- <span data-ttu-id="ab3ec-3273">Nome do estado (por exemplo, "Nova York")
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3273">State name (for example, "New York")</span></span>    
   
## <a name="us-individual-taxpayer-identification-number-itin"></a><span data-ttu-id="ab3ec-3274">Número de identificação de contribuinte individual (ITIN) dos EUA</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3274">U.S. Individual Taxpayer Identification Number (ITIN)</span></span>

### <a name="format"></a><span data-ttu-id="ab3ec-3275">Formato</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3275">Format</span></span>

<span data-ttu-id="ab3ec-3276">Nove dígitos que começam com "9" e contêm um "7" ou "8" como o quarto dígito, opcionalmente formatado com espaços ou traços</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3276">Nine digits that start with a "9" and contain a "7" or "8" as the fourth digit, optionally formatted with spaces or dashes</span></span>

### <a name="pattern"></a><span data-ttu-id="ab3ec-3277">Padrão</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3277">Pattern</span></span>

<span data-ttu-id="ab3ec-3278">Formatado:</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3278">Formatted:</span></span>
- <span data-ttu-id="ab3ec-3279">O dígito "9"</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3279">The digit "9"</span></span> 
- <span data-ttu-id="ab3ec-3280">Dois dígitos</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3280">Two digits</span></span> 
- <span data-ttu-id="ab3ec-3281">Um espaço ou um traço</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3281">A space or dash</span></span> 
- <span data-ttu-id="ab3ec-3282">Um "7" ou "8"</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3282">A "7" or "8"</span></span> 
- <span data-ttu-id="ab3ec-3283">Um dígito</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3283">A digit</span></span> 
- <span data-ttu-id="ab3ec-3284">Um espaço ou um traço</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3284">A space, or dash</span></span> 
- <span data-ttu-id="ab3ec-3285">Quatro dígitos</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3285">Four digits</span></span>

<span data-ttu-id="ab3ec-3286">Não Formatado:</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3286">Unformatted:</span></span>
- <span data-ttu-id="ab3ec-3287">O dígito "9"</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3287">The digit "9"</span></span> 
- <span data-ttu-id="ab3ec-3288">Dois dígitos</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3288">Two digits</span></span> 
- <span data-ttu-id="ab3ec-3289">Um "7" ou "8"</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3289">A "7" or "8"</span></span> 
- <span data-ttu-id="ab3ec-3290">Cinco dígitos</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3290">Five digits</span></span>

### <a name="checksum"></a><span data-ttu-id="ab3ec-3291">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3291">Checksum</span></span>

<span data-ttu-id="ab3ec-3292">Não</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3292">No</span></span>

### <a name="definition"></a><span data-ttu-id="ab3ec-3293">Definição</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3293">Definition</span></span>

<span data-ttu-id="ab3ec-3294">Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3294">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="ab3ec-3295">A função Func_formatted_itin localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3295">The function Func_formatted_itin finds content that matches the pattern.</span></span>
- <span data-ttu-id="ab3ec-3296">Pelo menos uma das seguintes opções for verdadeira:</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3296">At least one of the following is true:</span></span>
    - <span data-ttu-id="ab3ec-3297">Uma palavra-chave de Keyword_itin for encontrada.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3297">A keyword from Keyword_itin is found.</span></span>
    - <span data-ttu-id="ab3ec-3298">A função Func_us_address encontrar um endereço no formato de data à direita.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3298">The function Func_us_address finds an address in the right date format.</span></span>
    - <span data-ttu-id="ab3ec-3299">A função Func_us_date encontra uma data no formato de data à direita.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3299">The function Func_us_date finds a date in the right date format.</span></span>
    - <span data-ttu-id="ab3ec-3300">Uma palavra-chave de Keyword_itin_collaborative for encontrada.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3300">A keyword from Keyword_itin_collaborative is found.</span></span>

<span data-ttu-id="ab3ec-3301">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3301">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="ab3ec-3302">A função Func_unformatted_itin localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3302">The function Func_unformatted_itin finds content that matches the pattern.</span></span>
- <span data-ttu-id="ab3ec-3303">Pelo menos uma das seguintes opções for verdadeira:</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3303">At least one of the following is true:</span></span>
    - <span data-ttu-id="ab3ec-3304">Uma palavra-chave de Keyword_itin_collaborative for encontrada.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3304">A keyword from Keyword_itin_collaborative is found.</span></span>
    - <span data-ttu-id="ab3ec-3305">A função Func_us_address encontrar um endereço no formato de data à direita.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3305">The function Func_us_address finds an address in the right date format.</span></span>
    - <span data-ttu-id="ab3ec-3306">A função Func_us_date encontra uma data no formato de data à direita.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3306">The function Func_us_date finds a date in the right date format.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="ab3ec-3307">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3307">Keywords</span></span>

#### <a name="keyworditin"></a><span data-ttu-id="ab3ec-3308">Keyword_itin</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3308">Keyword_itin</span></span>

- <span data-ttu-id="ab3ec-3309">taxpayer
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3309">taxpayer</span></span> 
- <span data-ttu-id="ab3ec-3310">tax id
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3310">tax id</span></span> 
- <span data-ttu-id="ab3ec-3311">tax identification
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3311">tax identification</span></span> 
- <span data-ttu-id="ab3ec-3312">itin
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3312">itin</span></span> 
- <span data-ttu-id="ab3ec-3313">SSN</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3313">ssn</span></span> 
- <span data-ttu-id="ab3ec-3314">tin
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3314">tin</span></span> 
- <span data-ttu-id="ab3ec-3315">seguridade social</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3315">social security</span></span> 
- <span data-ttu-id="ab3ec-3316">tax payer
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3316">tax payer</span></span> 
- <span data-ttu-id="ab3ec-3317">itins
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3317">itins</span></span> 
- <span data-ttu-id="ab3ec-3318">taxid

</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3318">taxid</span></span> 
- <span data-ttu-id="ab3ec-3319">individual taxpayer
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3319">individual taxpayer</span></span> 

#### <a name="keyworditincollaborative"></a><span data-ttu-id="ab3ec-3320">Keyword_itin_collaborative</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3320">Keyword_itin_collaborative</span></span>

- <span data-ttu-id="ab3ec-3321">License</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3321">License</span></span> 
- <span data-ttu-id="ab3ec-3322">DL</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3322">DL</span></span> 
- <span data-ttu-id="ab3ec-3323">DOB
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3323">DOB</span></span> 
- <span data-ttu-id="ab3ec-3324">Data de Nascimento</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3324">Birthdate</span></span> 
- <span data-ttu-id="ab3ec-3325">Aniversário </span><span class="sxs-lookup"><span data-stu-id="ab3ec-3325">Birthday</span></span> 
- <span data-ttu-id="ab3ec-3326">Date of Birth
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3326">Date of Birth</span></span> 
   
## <a name="us-social-security-number-ssn"></a><span data-ttu-id="ab3ec-3327">Número de seguridade social dos EUA (SSN)</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3327">U.S. Social Security Number (SSN)</span></span>

### <a name="format"></a><span data-ttu-id="ab3ec-3328">Formato</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3328">Format</span></span>

<span data-ttu-id="ab3ec-3329">9 dígitos que podem estar em um padrão formatado ou não formatado</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3329">9 digits, which may be in a formatted or unformatted pattern</span></span>

> [!NOTE]
> <span data-ttu-id="ab3ec-3330">Se emitido antes de meados de 2011, um SSN possui formatação forte onde determinadas partes do número devem se enquadra determinados intervalos seja válido (mas não há nenhum soma de verificação).</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3330">If issued before mid-2011, an SSN has strong formatting where certain parts of the number must fall within certain ranges to be valid (but there's no checksum).</span></span>

### <a name="pattern"></a><span data-ttu-id="ab3ec-3331">Padrão</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3331">Pattern</span></span>

<span data-ttu-id="ab3ec-3332">Quatro funções procurado números de identificação fiscal nas quatro diferentes padrões:</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3332">Four functions look for SSNs in four different patterns:</span></span>
- <span data-ttu-id="ab3ec-3333">Func_ssn encontra os números de identificação fiscal com pré-2011 forte formatação formatados com travessões ou espaços (ddd-dd-dddd OR ddd dd dddd)</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3333">Func_ssn finds SSNs with pre-2011 strong formatting that are formatted with dashes or spaces (ddd-dd-dddd OR ddd dd dddd)</span></span>
- <span data-ttu-id="ab3ec-3334">Func_unformatted_ssn encontra os números de identificação fiscal com pré-2011 forte formatação que estão não formatado como nove dígitos consecutivos (ddddddddd)</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3334">Func_unformatted_ssn finds SSNs with pre-2011 strong formatting that are unformatted as nine consecutive digits (ddddddddd)</span></span>
- <span data-ttu-id="ab3ec-3335">Func_randomized_formatted_ssn encontrar números de identificação fiscal post-2011 formatados com travessões ou espaços (ddd-dd-dddd OR ddd dd dddd)</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3335">Func_randomized_formatted_ssn finds post-2011 SSNs that are formatted with dashes or spaces (ddd-dd-dddd OR ddd dd dddd)</span></span>
- <span data-ttu-id="ab3ec-3336">Func_randomized_unformatted_ssn encontrar números de identificação fiscal post-2011 que estão não formatados como nove dígitos consecutivos (ddddddddd)</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3336">Func_randomized_unformatted_ssn finds post-2011 SSNs that are unformatted as nine consecutive digits (ddddddddd)</span></span>

### <a name="checksum"></a><span data-ttu-id="ab3ec-3337">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3337">Checksum</span></span>

<span data-ttu-id="ab3ec-3338">Não</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3338">No</span></span>


### <a name="definition"></a><span data-ttu-id="ab3ec-3339">Definição</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3339">Definition</span></span>

<span data-ttu-id="ab3ec-3340">Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3340">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="ab3ec-3341">A função Func_ssn localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3341">The function Func_ssn finds content that matches the pattern.</span></span>
- <span data-ttu-id="ab3ec-3342">Uma palavra-chave de Keyword_ssn for encontrada.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3342">A keyword from Keyword_ssn is found.</span></span>

<span data-ttu-id="ab3ec-3343">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3343">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="ab3ec-3344">A função Func_unformatted_ssn encontra o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3344">The function Func_unformatted_ssn finds content that matches the pattern.</span></span>
- <span data-ttu-id="ab3ec-3345">Uma palavra-chave de Keyword_ssn for encontrada.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3345">A keyword from Keyword_ssn is found.</span></span>

<span data-ttu-id="ab3ec-3346">Uma política de DLP tem 65% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3346">A DLP policy is 65% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="ab3ec-3347">A função Func_randomized_formatted_ssn localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3347">The function Func_randomized_formatted_ssn finds content that matches the pattern.</span></span>
- <span data-ttu-id="ab3ec-3348">Uma palavra-chave de Keyword_ssn for encontrada.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3348">A keyword from Keyword_ssn is found.</span></span>
- <span data-ttu-id="ab3ec-3349">A função Func_ssn não localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3349">The function Func_ssn does not find content that matches the pattern.</span></span>

<span data-ttu-id="ab3ec-3350">Uma política de DLP tem 55% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3350">A DLP policy is 55% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="ab3ec-3351">A função Func_randomized_unformatted_ssn localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3351">The function Func_randomized_unformatted_ssn finds content that matches the pattern.</span></span>
- <span data-ttu-id="ab3ec-3352">Uma palavra-chave de Keyword_ssn for encontrada.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3352">A keyword from Keyword_ssn is found.</span></span>
- <span data-ttu-id="ab3ec-3353">A função Func_unformatted_ssn não localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3353">The function Func_unformatted_ssn does not find content that matches the pattern.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="ab3ec-3354">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3354">Keywords</span></span>

#### <a name="keywordssn"></a><span data-ttu-id="ab3ec-3355">Keyword_ssn</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3355">Keyword_ssn</span></span>

- <span data-ttu-id="ab3ec-3356">Social Security
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3356">Social Security</span></span> 
- <span data-ttu-id="ab3ec-3357">Social Security#
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3357">Social Security#</span></span> 
- <span data-ttu-id="ab3ec-3358">Soc Sec
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3358">Soc Sec</span></span> 
- <span data-ttu-id="ab3ec-3359">SSN</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3359">SSN</span></span> 
- <span data-ttu-id="ab3ec-3360">SSNS
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3360">SSNS</span></span> 
- <span data-ttu-id="ab3ec-3361">SSN#
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3361">SSN#</span></span> 
- <span data-ttu-id="ab3ec-3362">SS#
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3362">SS#</span></span> 
- <span data-ttu-id="ab3ec-3363">SSID
</span><span class="sxs-lookup"><span data-stu-id="ab3ec-3363">SSID</span></span> 
   

