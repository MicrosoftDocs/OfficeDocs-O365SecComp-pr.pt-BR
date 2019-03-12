---
title: O que os tipos de informações confidenciais procuram
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: 6/29/2018
ms.audience: Admin
search.appverid: MET150
ms.topic: reference
f1_keywords:
- ms.o365.cc.UnifiedDLPRuleContainsSensitiveInformation
ms.service: O365-seccomp
localization_priority: Normal
ms.collection:
- M365-security-compliance
description: A prevenção de perda de dados (DLP) no centro &amp; de conformidade de segurança do Office 365 inclui tipos de informações confidenciais que estão prontos para uso nas suas políticas de DLP. Este tópico lista todos os tipos de informações confidenciais e mostra o que uma política de DLP procura ao detectar cada tipo.
ms.openlocfilehash: e9811b285e98a791570dc91e275cb5cead4f8bc9
ms.sourcegitcommit: 6e8e2b43a4bea31c1e835c5b050824651c6a0094
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/11/2019
ms.locfileid: "30537638"
---
# <a name="what-the-sensitive-information-types-look-for"></a><span data-ttu-id="cc14d-104">O que os tipos de informações confidenciais procuram</span><span class="sxs-lookup"><span data-stu-id="cc14d-104">What the sensitive information types look for</span></span>

<span data-ttu-id="cc14d-105">A prevenção de perda de dados (DLP) no centro &amp; de conformidade de segurança do Office 365 inclui muitos tipos de informações confidenciais que estão prontos para uso nas suas políticas de DLP.</span><span class="sxs-lookup"><span data-stu-id="cc14d-105">Data loss prevention (DLP) in the Office 365 Security &amp; Compliance Center includes many sensitive information types that are ready for you to use in your DLP policies.</span></span> <span data-ttu-id="cc14d-106">Este tópico lista todos os tipos de informações confidenciais e mostra o que uma política de DLP procura ao detectar cada tipo.</span><span class="sxs-lookup"><span data-stu-id="cc14d-106">This topic lists all of these sensitive information types and shows what a DLP policy looks for when it detects each type.</span></span> <span data-ttu-id="cc14d-107">Um tipo de informação confidencial é definido por um padrão que pode ser identificado por uma função ou uma expressão regular.</span><span class="sxs-lookup"><span data-stu-id="cc14d-107">A sensitive information type is defined by a pattern that can be identified by a regular expression or a function.</span></span> <span data-ttu-id="cc14d-108">Além disso, evidências corroborativas, como palavras-chave e somas de verificação, podem ser usadas para identificar um tipo de informação confidencial.</span><span class="sxs-lookup"><span data-stu-id="cc14d-108">In addition, corroborative evidence such as keywords and checksums can be used to identify a sensitive information type.</span></span> <span data-ttu-id="cc14d-109">O nível de confiança e a proximidade também são usados no processo de avaliação.</span><span class="sxs-lookup"><span data-stu-id="cc14d-109">Confidence level and proximity are also used in the evaluation process.</span></span>
  
## <a name="aba-routing-number"></a><span data-ttu-id="cc14d-110">Número de roteamento ABA</span><span class="sxs-lookup"><span data-stu-id="cc14d-110">ABA Routing Number</span></span>

### <a name="format"></a><span data-ttu-id="cc14d-111">Format</span><span class="sxs-lookup"><span data-stu-id="cc14d-111">Format</span></span>

<span data-ttu-id="cc14d-112">9 dígitos que podem estar em um padrão formatado ou não formatado</span><span class="sxs-lookup"><span data-stu-id="cc14d-112">9 digits which may be in a formatted or unformatted pattern</span></span>

### <a name="pattern"></a><span data-ttu-id="cc14d-113">Padrão</span><span class="sxs-lookup"><span data-stu-id="cc14d-113">Pattern</span></span>

<span data-ttu-id="cc14d-114">Binário</span><span class="sxs-lookup"><span data-stu-id="cc14d-114">Formatted:</span></span>
- <span data-ttu-id="cc14d-115">Quatro dígitos, começando com 0, 1, 2, 3, 6, 7 ou 8</span><span class="sxs-lookup"><span data-stu-id="cc14d-115">Four digits beginning with 0, 1, 2, 3, 6, 7, or 8</span></span>
- <span data-ttu-id="cc14d-116">Um hífen</span><span class="sxs-lookup"><span data-stu-id="cc14d-116">A hyphen</span></span>
- <span data-ttu-id="cc14d-117">Quatro dígitos</span><span class="sxs-lookup"><span data-stu-id="cc14d-117">Four digits</span></span>
- <span data-ttu-id="cc14d-118">Um hífen</span><span class="sxs-lookup"><span data-stu-id="cc14d-118">A hyphen</span></span>
- <span data-ttu-id="cc14d-119">Um dígito</span><span class="sxs-lookup"><span data-stu-id="cc14d-119">A digit</span></span>

<span data-ttu-id="cc14d-120">Não formatado: 9 dígitos consecutivos começando com 0, 1, 2, 3, 6, 7 ou 8</span><span class="sxs-lookup"><span data-stu-id="cc14d-120">Unformatted: 9 consecutive digits beginning with 0, 1, 2, 3, 6, 7, or 8</span></span> 

### <a name="checksum"></a><span data-ttu-id="cc14d-121">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="cc14d-121">Checksum</span></span>

<span data-ttu-id="cc14d-122">Não</span><span class="sxs-lookup"><span data-stu-id="cc14d-122">No</span></span>

### <a name="definition"></a><span data-ttu-id="cc14d-123">Definição</span><span class="sxs-lookup"><span data-stu-id="cc14d-123">Definition</span></span>

<span data-ttu-id="cc14d-124">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="cc14d-124">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="cc14d-125">A função Func_aba_routing localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="cc14d-125">The function Func_aba_routing finds content that matches the pattern.</span></span>
- <span data-ttu-id="cc14d-126">Uma palavra-chave de Keyword_ABA_Routing for encontrada.</span><span class="sxs-lookup"><span data-stu-id="cc14d-126">A keyword from Keyword_ABA_Routing is found.</span></span>

```
<!-- ABA Routing Number -->
<Entity id="cb353f78-2b72-4c3c-8827-92ebe4f69fdf" patternsProximity="300" recommendedConfidence="75">
      <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_aba_routing" />
        <Match idRef="Keyword_ABA_Routing" />
      </Pattern>
 </Entity>
```


### <a name="keywords"></a><span data-ttu-id="cc14d-127">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="cc14d-127">Keywords</span></span>

#### <a name="keywordabarouting"></a><span data-ttu-id="cc14d-128">Keyword_ABA_Routing</span><span class="sxs-lookup"><span data-stu-id="cc14d-128">Keyword_ABA_Routing</span></span>

- <span data-ttu-id="cc14d-129">aba</span><span class="sxs-lookup"><span data-stu-id="cc14d-129">aba</span></span>
- <span data-ttu-id="cc14d-130">aba #</span><span class="sxs-lookup"><span data-stu-id="cc14d-130">aba #</span></span>
- <span data-ttu-id="cc14d-131">aba routing #</span><span class="sxs-lookup"><span data-stu-id="cc14d-131">aba routing #</span></span>
- <span data-ttu-id="cc14d-132">aba routing number</span><span class="sxs-lookup"><span data-stu-id="cc14d-132">aba routing number</span></span>
- <span data-ttu-id="cc14d-133">aba #</span><span class="sxs-lookup"><span data-stu-id="cc14d-133">aba#</span></span>
- <span data-ttu-id="cc14d-134">abarouting #</span><span class="sxs-lookup"><span data-stu-id="cc14d-134">abarouting#</span></span>
- <span data-ttu-id="cc14d-135">aba number</span><span class="sxs-lookup"><span data-stu-id="cc14d-135">aba number</span></span>
- <span data-ttu-id="cc14d-136">abaroutingnumber</span><span class="sxs-lookup"><span data-stu-id="cc14d-136">abaroutingnumber</span></span>
- <span data-ttu-id="cc14d-137">american bank association routing #</span><span class="sxs-lookup"><span data-stu-id="cc14d-137">american bank association routing #</span></span>
- <span data-ttu-id="cc14d-138">american bank association routing number</span><span class="sxs-lookup"><span data-stu-id="cc14d-138">american bank association routing number</span></span>
- <span data-ttu-id="cc14d-139">americanbankassociationrouting #</span><span class="sxs-lookup"><span data-stu-id="cc14d-139">americanbankassociationrouting#</span></span>
- <span data-ttu-id="cc14d-140">americanbankassociationroutingnumber</span><span class="sxs-lookup"><span data-stu-id="cc14d-140">americanbankassociationroutingnumber</span></span>
- <span data-ttu-id="cc14d-141">bank routing number</span><span class="sxs-lookup"><span data-stu-id="cc14d-141">bank routing number</span></span>
- <span data-ttu-id="cc14d-142">bankrouting #</span><span class="sxs-lookup"><span data-stu-id="cc14d-142">bankrouting#</span></span>
- <span data-ttu-id="cc14d-143">bankroutingnumber</span><span class="sxs-lookup"><span data-stu-id="cc14d-143">bankroutingnumber</span></span>
- <span data-ttu-id="cc14d-144">routing transit number</span><span class="sxs-lookup"><span data-stu-id="cc14d-144">routing transit number</span></span>
- <span data-ttu-id="cc14d-145">RTN</span><span class="sxs-lookup"><span data-stu-id="cc14d-145">RTN</span></span> 
   
## <a name="argentina-national-identity-dni-number"></a><span data-ttu-id="cc14d-146">Número de Identidade Nacional (DNI) da Argentina</span><span class="sxs-lookup"><span data-stu-id="cc14d-146">Argentina National Identity (DNI) Number</span></span>

### <a name="format"></a><span data-ttu-id="cc14d-147">Format</span><span class="sxs-lookup"><span data-stu-id="cc14d-147">Format</span></span>

<span data-ttu-id="cc14d-148">Oito dígitos separados por pontos</span><span class="sxs-lookup"><span data-stu-id="cc14d-148">Eight digits separated by periods</span></span>

### <a name="pattern"></a><span data-ttu-id="cc14d-149">Padrão</span><span class="sxs-lookup"><span data-stu-id="cc14d-149">Pattern</span></span>

<span data-ttu-id="cc14d-150">Oito dígitos:</span><span class="sxs-lookup"><span data-stu-id="cc14d-150">Eight digits:</span></span>
- <span data-ttu-id="cc14d-151">Dois dígitos</span><span class="sxs-lookup"><span data-stu-id="cc14d-151">Two digits</span></span>
- <span data-ttu-id="cc14d-152">Um ponto </span><span class="sxs-lookup"><span data-stu-id="cc14d-152">A period</span></span>
- <span data-ttu-id="cc14d-153">Três dígitos</span><span class="sxs-lookup"><span data-stu-id="cc14d-153">Three digits</span></span>
- <span data-ttu-id="cc14d-154">Um ponto </span><span class="sxs-lookup"><span data-stu-id="cc14d-154">A period</span></span>
- <span data-ttu-id="cc14d-155">Três dígitos</span><span class="sxs-lookup"><span data-stu-id="cc14d-155">Three digits</span></span>

### <a name="checksum"></a><span data-ttu-id="cc14d-156">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="cc14d-156">Checksum</span></span>

<span data-ttu-id="cc14d-157">Não</span><span class="sxs-lookup"><span data-stu-id="cc14d-157">No</span></span>

### <a name="definition"></a><span data-ttu-id="cc14d-158">Definição</span><span class="sxs-lookup"><span data-stu-id="cc14d-158">Definition</span></span>

<span data-ttu-id="cc14d-159">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="cc14d-159">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="cc14d-160">A expressão regular Regex_argentina_national_id localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="cc14d-160">The regular expression Regex_argentina_national_id finds content that matches the pattern.</span></span>
- <span data-ttu-id="cc14d-161">Uma palavra-chave de Keyword_argentina_national_id for encontrada.</span><span class="sxs-lookup"><span data-stu-id="cc14d-161">A keyword from Keyword_argentina_national_id is found.</span></span>

```
<!-- Argentina National Identity (DNI) Number -->
<Entity id="eefbb00e-8282-433c-8620-8f1da3bffdb2" recommendedConfidence="75" patternsProximity="300">
   <Pattern confidenceLevel="75">
      <IdMatch idRef="Regex_argentina_national_id"/>
      <Match idRef="Keyword_argentina_national_id"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="cc14d-162">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="cc14d-162">Keywords</span></span>

#### <a name="keywordargentinanationalid"></a><span data-ttu-id="cc14d-163">Keyword_argentina_national_id</span><span class="sxs-lookup"><span data-stu-id="cc14d-163">Keyword_argentina_national_id</span></span>

- <span data-ttu-id="cc14d-164">Número de Identidade Nacional da Argentina</span><span class="sxs-lookup"><span data-stu-id="cc14d-164">Argentina National Identity number</span></span> 
- <span data-ttu-id="cc14d-165">Identidade</span><span class="sxs-lookup"><span data-stu-id="cc14d-165">Identity</span></span> 
- <span data-ttu-id="cc14d-166">Identificar cartão de identidade nacional</span><span class="sxs-lookup"><span data-stu-id="cc14d-166">Identification National Identity Card</span></span> 
- <span data-ttu-id="cc14d-167">DNI</span><span class="sxs-lookup"><span data-stu-id="cc14d-167">DNI</span></span> 
- <span data-ttu-id="cc14d-168">Registro Nacional de pessoas da NIC</span><span class="sxs-lookup"><span data-stu-id="cc14d-168">NIC National Registry of Persons</span></span> 
- <span data-ttu-id="cc14d-169">Documento Nacional de Identidad</span><span class="sxs-lookup"><span data-stu-id="cc14d-169">Documento Nacional de Identidad</span></span> 
- <span data-ttu-id="cc14d-170">Registro Nacional de las Personas</span><span class="sxs-lookup"><span data-stu-id="cc14d-170">Registro Nacional de las Personas</span></span> 
- <span data-ttu-id="cc14d-171">Identidad</span><span class="sxs-lookup"><span data-stu-id="cc14d-171">Identidad</span></span> 
- <span data-ttu-id="cc14d-172">Identificación</span><span class="sxs-lookup"><span data-stu-id="cc14d-172">Identificación</span></span> 
   
## <a name="australia-bank-account-number"></a><span data-ttu-id="cc14d-173">Número de conta de banco da Austrália</span><span class="sxs-lookup"><span data-stu-id="cc14d-173">Australia Bank Account Number</span></span>

### <a name="format"></a><span data-ttu-id="cc14d-174">Format</span><span class="sxs-lookup"><span data-stu-id="cc14d-174">Format</span></span>

<span data-ttu-id="cc14d-175">6 a 10 dígitos com ou sem um número BSB</span><span class="sxs-lookup"><span data-stu-id="cc14d-175">6-10 digits with or without a bank state branch number</span></span>

### <a name="pattern"></a><span data-ttu-id="cc14d-176">Padrão</span><span class="sxs-lookup"><span data-stu-id="cc14d-176">Pattern</span></span>

<span data-ttu-id="cc14d-177">Número de conta é 6 de 10 dígitos.</span><span class="sxs-lookup"><span data-stu-id="cc14d-177">Account number is 6-10 digits.</span></span>
<span data-ttu-id="cc14d-178">Número BSB da Austrália:</span><span class="sxs-lookup"><span data-stu-id="cc14d-178">Australia bank state branch number:</span></span>
- <span data-ttu-id="cc14d-179">Três dígitos</span><span class="sxs-lookup"><span data-stu-id="cc14d-179">Three digits</span></span> 
- <span data-ttu-id="cc14d-180">Um hífen</span><span class="sxs-lookup"><span data-stu-id="cc14d-180">A hyphen</span></span> 
- <span data-ttu-id="cc14d-181">Três dígitos</span><span class="sxs-lookup"><span data-stu-id="cc14d-181">Three digits</span></span>

### <a name="checksum"></a><span data-ttu-id="cc14d-182">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="cc14d-182">Checksum</span></span>

<span data-ttu-id="cc14d-183">Não</span><span class="sxs-lookup"><span data-stu-id="cc14d-183">No</span></span>

### <a name="definition"></a><span data-ttu-id="cc14d-184">Definição</span><span class="sxs-lookup"><span data-stu-id="cc14d-184">Definition</span></span>

<span data-ttu-id="cc14d-185">Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="cc14d-185">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="cc14d-186">A expressão regular Regex_australia_bank_account_number localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="cc14d-186">The regular expression Regex_australia_bank_account_number finds content that matches the pattern..</span></span>
- <span data-ttu-id="cc14d-187">Uma palavra-chave de Keyword_australia_bank_account_number for encontrada.</span><span class="sxs-lookup"><span data-stu-id="cc14d-187">A keyword from Keyword_australia_bank_account_number is found.</span></span>
- <span data-ttu-id="cc14d-188">A expressão regular Regex_australia_bank_account_number_bsb localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="cc14d-188">The regular expression Regex_australia_bank_account_number_bsb finds content that matches the pattern.</span></span>

<span data-ttu-id="cc14d-189">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="cc14d-189">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="cc14d-190">A expressão regular Regex_australia_bank_account_number localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="cc14d-190">The regular expression Regex_australia_bank_account_number finds content that matches the pattern..</span></span>
- <span data-ttu-id="cc14d-191">Uma palavra-chave de Keyword_australia_bank_account_number for encontrada.</span><span class="sxs-lookup"><span data-stu-id="cc14d-191">A keyword from Keyword_australia_bank_account_number is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="cc14d-192">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="cc14d-192">Keywords</span></span>

#### <a name="keywordaustraliabankaccountnumber"></a><span data-ttu-id="cc14d-193">Keyword_australia_bank_account_number</span><span class="sxs-lookup"><span data-stu-id="cc14d-193">Keyword_australia_bank_account_number</span></span>

- <span data-ttu-id="cc14d-194">swift bank code</span><span class="sxs-lookup"><span data-stu-id="cc14d-194">swift bank code</span></span>
- <span data-ttu-id="cc14d-195">correspondent bank</span><span class="sxs-lookup"><span data-stu-id="cc14d-195">correspondent bank</span></span>
- <span data-ttu-id="cc14d-196">base currency</span><span class="sxs-lookup"><span data-stu-id="cc14d-196">base currency</span></span>
- <span data-ttu-id="cc14d-197">usa account</span><span class="sxs-lookup"><span data-stu-id="cc14d-197">usa account</span></span>
- <span data-ttu-id="cc14d-198">holder address</span><span class="sxs-lookup"><span data-stu-id="cc14d-198">holder address</span></span>
- <span data-ttu-id="cc14d-199">bank address</span><span class="sxs-lookup"><span data-stu-id="cc14d-199">bank address</span></span>
- <span data-ttu-id="cc14d-200">information account</span><span class="sxs-lookup"><span data-stu-id="cc14d-200">information account</span></span>
- <span data-ttu-id="cc14d-201">fund transfers</span><span class="sxs-lookup"><span data-stu-id="cc14d-201">fund transfers</span></span>
- <span data-ttu-id="cc14d-202">bank charges</span><span class="sxs-lookup"><span data-stu-id="cc14d-202">bank charges</span></span>
- <span data-ttu-id="cc14d-203">bank details</span><span class="sxs-lookup"><span data-stu-id="cc14d-203">bank details</span></span>
- <span data-ttu-id="cc14d-204">banking information</span><span class="sxs-lookup"><span data-stu-id="cc14d-204">banking information</span></span>
- <span data-ttu-id="cc14d-205">full names</span><span class="sxs-lookup"><span data-stu-id="cc14d-205">full names</span></span>
- <span data-ttu-id="cc14d-206">IAEA</span><span class="sxs-lookup"><span data-stu-id="cc14d-206">iaea</span></span>

   
## <a name="australia-drivers-license-number"></a><span data-ttu-id="cc14d-207">Número de carteira de motorista da Austrália</span><span class="sxs-lookup"><span data-stu-id="cc14d-207">Australia Driver's License Number</span></span>

### <a name="format"></a><span data-ttu-id="cc14d-208">Format</span><span class="sxs-lookup"><span data-stu-id="cc14d-208">Format</span></span>

<span data-ttu-id="cc14d-209">Nove letras e dígitos</span><span class="sxs-lookup"><span data-stu-id="cc14d-209">Nine letters and digits</span></span>

### <a name="pattern"></a><span data-ttu-id="cc14d-210">Padrão</span><span class="sxs-lookup"><span data-stu-id="cc14d-210">Pattern</span></span>

<span data-ttu-id="cc14d-211">Nove letras e dígitos:</span><span class="sxs-lookup"><span data-stu-id="cc14d-211">Nine letters and digits:</span></span> 

- <span data-ttu-id="cc14d-212">Dois dígitos ou letras (não diferenciam maiúsculas de minúsculas)</span><span class="sxs-lookup"><span data-stu-id="cc14d-212">Two digits or letters (not case sensitive)</span></span> 
- <span data-ttu-id="cc14d-213">Dois dígitos</span><span class="sxs-lookup"><span data-stu-id="cc14d-213">Two digits</span></span> 
- <span data-ttu-id="cc14d-214">Cinco dígitos ou letras (não diferenciam maiúsculas de minúsculas)</span><span class="sxs-lookup"><span data-stu-id="cc14d-214">Five digits or letters (not case sensitive)</span></span>

<span data-ttu-id="cc14d-215">OU</span><span class="sxs-lookup"><span data-stu-id="cc14d-215">OR</span></span>

- <span data-ttu-id="cc14d-216">1 a 2 letras opcionais (não diferenciam maiúsculas de minúsculas)</span><span class="sxs-lookup"><span data-stu-id="cc14d-216">1-2 optional letters (not case sensitive)</span></span> 
- <span data-ttu-id="cc14d-217">4 a 9 dígitos</span><span class="sxs-lookup"><span data-stu-id="cc14d-217">4-9 digits</span></span>

<span data-ttu-id="cc14d-218">OU</span><span class="sxs-lookup"><span data-stu-id="cc14d-218">OR</span></span>

- <span data-ttu-id="cc14d-219">Nove dígitos ou letras (não diferenciam maiúsculas de minúsculas)</span><span class="sxs-lookup"><span data-stu-id="cc14d-219">Nine digits or letters (not case sensitive)</span></span>

### <a name="checksum"></a><span data-ttu-id="cc14d-220">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="cc14d-220">Checksum</span></span>

<span data-ttu-id="cc14d-221">Não</span><span class="sxs-lookup"><span data-stu-id="cc14d-221">No</span></span>

### <a name="definition"></a><span data-ttu-id="cc14d-222">Definição</span><span class="sxs-lookup"><span data-stu-id="cc14d-222">Definition</span></span>

<span data-ttu-id="cc14d-223">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="cc14d-223">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="cc14d-224">A expressão regular Regex_australia_drivers_license_number localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="cc14d-224">The regular expression Regex_australia_drivers_license_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="cc14d-225">Uma palavra-chave de Keyword_australia_drivers_license_number for encontrada.</span><span class="sxs-lookup"><span data-stu-id="cc14d-225">A keyword from Keyword_australia_drivers_license_number is found.</span></span>
- <span data-ttu-id="cc14d-226">Nenhuma palavra-chave de Keyword_australia_drivers_license_number_exclusions for encontrada.</span><span class="sxs-lookup"><span data-stu-id="cc14d-226">No keyword from Keyword_australia_drivers_license_number_exclusions is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="cc14d-227">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="cc14d-227">Keywords</span></span>

#### <a name="keywordaustraliadriverslicensenumber"></a><span data-ttu-id="cc14d-228">Keyword_australia_drivers_license_number</span><span class="sxs-lookup"><span data-stu-id="cc14d-228">Keyword_australia_drivers_license_number</span></span>

- <span data-ttu-id="cc14d-229">international driving permits</span><span class="sxs-lookup"><span data-stu-id="cc14d-229">international driving permits</span></span>
- <span data-ttu-id="cc14d-230">australian automobile association</span><span class="sxs-lookup"><span data-stu-id="cc14d-230">australian automobile association</span></span>
- <span data-ttu-id="cc14d-231">international driving permit</span><span class="sxs-lookup"><span data-stu-id="cc14d-231">international driving permit</span></span>
- <span data-ttu-id="cc14d-232">DriverLicence</span><span class="sxs-lookup"><span data-stu-id="cc14d-232">DriverLicence</span></span>
- <span data-ttu-id="cc14d-233">DriverLicences</span><span class="sxs-lookup"><span data-stu-id="cc14d-233">DriverLicences</span></span>
- <span data-ttu-id="cc14d-234">Driver Lic</span><span class="sxs-lookup"><span data-stu-id="cc14d-234">Driver Lic</span></span>
- <span data-ttu-id="cc14d-235">Driver Licence</span><span class="sxs-lookup"><span data-stu-id="cc14d-235">Driver Licence</span></span>
- <span data-ttu-id="cc14d-236">Driver Licences</span><span class="sxs-lookup"><span data-stu-id="cc14d-236">Driver Licences</span></span>
- <span data-ttu-id="cc14d-237">DriversLic</span><span class="sxs-lookup"><span data-stu-id="cc14d-237">DriversLic</span></span>
- <span data-ttu-id="cc14d-238">DriversLicence</span><span class="sxs-lookup"><span data-stu-id="cc14d-238">DriversLicence</span></span>
- <span data-ttu-id="cc14d-239">DriversLicences</span><span class="sxs-lookup"><span data-stu-id="cc14d-239">DriversLicences</span></span>
- <span data-ttu-id="cc14d-240">Drivers Lic</span><span class="sxs-lookup"><span data-stu-id="cc14d-240">Drivers Lic</span></span>
- <span data-ttu-id="cc14d-241">Drivers Lics</span><span class="sxs-lookup"><span data-stu-id="cc14d-241">Drivers Lics</span></span>
- <span data-ttu-id="cc14d-242">Drivers Licence</span><span class="sxs-lookup"><span data-stu-id="cc14d-242">Drivers Licence</span></span>
- <span data-ttu-id="cc14d-243">Drivers Licences</span><span class="sxs-lookup"><span data-stu-id="cc14d-243">Drivers Licences</span></span>
- <span data-ttu-id="cc14d-244">Driver'Lic</span><span class="sxs-lookup"><span data-stu-id="cc14d-244">Driver'Lic</span></span>
- <span data-ttu-id="cc14d-245">Driver'Lics</span><span class="sxs-lookup"><span data-stu-id="cc14d-245">Driver'Lics</span></span>
- <span data-ttu-id="cc14d-246">Driver'Licence</span><span class="sxs-lookup"><span data-stu-id="cc14d-246">Driver'Licence</span></span>
- <span data-ttu-id="cc14d-247">Driver'Licences</span><span class="sxs-lookup"><span data-stu-id="cc14d-247">Driver'Licences</span></span>
- <span data-ttu-id="cc14d-248">Driver'Lic</span><span class="sxs-lookup"><span data-stu-id="cc14d-248">Driver' Lic</span></span>
- <span data-ttu-id="cc14d-249">Driver'Lics</span><span class="sxs-lookup"><span data-stu-id="cc14d-249">Driver' Lics</span></span>
- <span data-ttu-id="cc14d-250">Driver'Licence</span><span class="sxs-lookup"><span data-stu-id="cc14d-250">Driver' Licence</span></span>
- <span data-ttu-id="cc14d-251">Driver'Licences</span><span class="sxs-lookup"><span data-stu-id="cc14d-251">Driver' Licences</span></span>
- <span data-ttu-id="cc14d-252">Driver'sLic</span><span class="sxs-lookup"><span data-stu-id="cc14d-252">Driver'sLic</span></span>
- <span data-ttu-id="cc14d-253">Driver'sLics</span><span class="sxs-lookup"><span data-stu-id="cc14d-253">Driver'sLics</span></span>
- <span data-ttu-id="cc14d-254">Driver'sLicence</span><span class="sxs-lookup"><span data-stu-id="cc14d-254">Driver'sLicence</span></span>
- <span data-ttu-id="cc14d-255">Driver'sLicences</span><span class="sxs-lookup"><span data-stu-id="cc14d-255">Driver'sLicences</span></span>
- <span data-ttu-id="cc14d-256">Driver's Lic</span><span class="sxs-lookup"><span data-stu-id="cc14d-256">Driver's Lic</span></span>
- <span data-ttu-id="cc14d-257">Driver's Lics</span><span class="sxs-lookup"><span data-stu-id="cc14d-257">Driver's Lics</span></span>
- <span data-ttu-id="cc14d-258">Driver's Licence</span><span class="sxs-lookup"><span data-stu-id="cc14d-258">Driver's Licence</span></span>
- <span data-ttu-id="cc14d-259">Driver's Licences</span><span class="sxs-lookup"><span data-stu-id="cc14d-259">Driver's Licences</span></span>
- <span data-ttu-id="cc14d-260">DriverLic #</span><span class="sxs-lookup"><span data-stu-id="cc14d-260">DriverLic#</span></span>
- <span data-ttu-id="cc14d-261">DriverLics #</span><span class="sxs-lookup"><span data-stu-id="cc14d-261">DriverLics#</span></span>
- <span data-ttu-id="cc14d-262">DriverLicence #</span><span class="sxs-lookup"><span data-stu-id="cc14d-262">DriverLicence#</span></span>
- <span data-ttu-id="cc14d-263">DriverLicences #</span><span class="sxs-lookup"><span data-stu-id="cc14d-263">DriverLicences#</span></span>
- <span data-ttu-id="cc14d-264">Driver Lic#</span><span class="sxs-lookup"><span data-stu-id="cc14d-264">Driver Lic#</span></span>
- <span data-ttu-id="cc14d-265">Driver Lics#</span><span class="sxs-lookup"><span data-stu-id="cc14d-265">Driver Lics#</span></span>
- <span data-ttu-id="cc14d-266">Driver Licence#</span><span class="sxs-lookup"><span data-stu-id="cc14d-266">Driver Licence#</span></span>
- <span data-ttu-id="cc14d-267">Driver Licences#</span><span class="sxs-lookup"><span data-stu-id="cc14d-267">Driver Licences#</span></span>
- <span data-ttu-id="cc14d-268">DriversLic #</span><span class="sxs-lookup"><span data-stu-id="cc14d-268">DriversLic#</span></span>
- <span data-ttu-id="cc14d-269">DriversLics #</span><span class="sxs-lookup"><span data-stu-id="cc14d-269">DriversLics#</span></span>
- <span data-ttu-id="cc14d-270">DriversLicence #</span><span class="sxs-lookup"><span data-stu-id="cc14d-270">DriversLicence#</span></span>
- <span data-ttu-id="cc14d-271">DriversLicences #</span><span class="sxs-lookup"><span data-stu-id="cc14d-271">DriversLicences#</span></span>
- <span data-ttu-id="cc14d-272">Drivers Lic#</span><span class="sxs-lookup"><span data-stu-id="cc14d-272">Drivers Lic#</span></span>
- <span data-ttu-id="cc14d-273">Drivers Lics#</span><span class="sxs-lookup"><span data-stu-id="cc14d-273">Drivers Lics#</span></span>
- <span data-ttu-id="cc14d-274">Drivers Licence#</span><span class="sxs-lookup"><span data-stu-id="cc14d-274">Drivers Licence#</span></span>
- <span data-ttu-id="cc14d-275">Drivers Licences#</span><span class="sxs-lookup"><span data-stu-id="cc14d-275">Drivers Licences#</span></span>
- <span data-ttu-id="cc14d-276">Driver'Lic #</span><span class="sxs-lookup"><span data-stu-id="cc14d-276">Driver'Lic#</span></span>
- <span data-ttu-id="cc14d-277">Driver'Lics #</span><span class="sxs-lookup"><span data-stu-id="cc14d-277">Driver'Lics#</span></span>
- <span data-ttu-id="cc14d-278">Driver'Licence #</span><span class="sxs-lookup"><span data-stu-id="cc14d-278">Driver'Licence#</span></span>
- <span data-ttu-id="cc14d-279">Driver'Licences #</span><span class="sxs-lookup"><span data-stu-id="cc14d-279">Driver'Licences#</span></span>
- <span data-ttu-id="cc14d-280">Driver'Lic#</span><span class="sxs-lookup"><span data-stu-id="cc14d-280">Driver' Lic#</span></span>
- <span data-ttu-id="cc14d-281">Driver'Lics#</span><span class="sxs-lookup"><span data-stu-id="cc14d-281">Driver' Lics#</span></span>
- <span data-ttu-id="cc14d-282">Driver'Licence#</span><span class="sxs-lookup"><span data-stu-id="cc14d-282">Driver' Licence#</span></span>
- <span data-ttu-id="cc14d-283">Driver'Licences#</span><span class="sxs-lookup"><span data-stu-id="cc14d-283">Driver' Licences#</span></span>
- <span data-ttu-id="cc14d-284">Driver'sLic #</span><span class="sxs-lookup"><span data-stu-id="cc14d-284">Driver'sLic#</span></span>
- <span data-ttu-id="cc14d-285">Driver'sLics #</span><span class="sxs-lookup"><span data-stu-id="cc14d-285">Driver'sLics#</span></span>
- <span data-ttu-id="cc14d-286">Driver'sLicence #</span><span class="sxs-lookup"><span data-stu-id="cc14d-286">Driver'sLicence#</span></span>
- <span data-ttu-id="cc14d-287">Driver'sLicences #</span><span class="sxs-lookup"><span data-stu-id="cc14d-287">Driver'sLicences#</span></span>
- <span data-ttu-id="cc14d-288">Driver's Lic#</span><span class="sxs-lookup"><span data-stu-id="cc14d-288">Driver's Lic#</span></span>
- <span data-ttu-id="cc14d-289">Driver's Lics#</span><span class="sxs-lookup"><span data-stu-id="cc14d-289">Driver's Lics#</span></span>
- <span data-ttu-id="cc14d-290">Driver's Licence#</span><span class="sxs-lookup"><span data-stu-id="cc14d-290">Driver's Licence#</span></span>
- <span data-ttu-id="cc14d-291">Driver's Licences#</span><span class="sxs-lookup"><span data-stu-id="cc14d-291">Driver's Licences#</span></span> 

#### <a name="keywordaustraliadriverslicensenumberexclusions"></a><span data-ttu-id="cc14d-292">Keyword_australia_drivers_license_number_exclusions</span><span class="sxs-lookup"><span data-stu-id="cc14d-292">Keyword_australia_drivers_license_number_exclusions</span></span>

- <span data-ttu-id="cc14d-293">AAA</span><span class="sxs-lookup"><span data-stu-id="cc14d-293">aaa</span></span>
- <span data-ttu-id="cc14d-294">DriverLicense</span><span class="sxs-lookup"><span data-stu-id="cc14d-294">DriverLicense</span></span>
- <span data-ttu-id="cc14d-295">DriverLicenses</span><span class="sxs-lookup"><span data-stu-id="cc14d-295">DriverLicenses</span></span>
- <span data-ttu-id="cc14d-296">Driver License</span><span class="sxs-lookup"><span data-stu-id="cc14d-296">Driver License</span></span>
- <span data-ttu-id="cc14d-297">Driver Licenses</span><span class="sxs-lookup"><span data-stu-id="cc14d-297">Driver Licenses</span></span>
- <span data-ttu-id="cc14d-298">DriversLicense</span><span class="sxs-lookup"><span data-stu-id="cc14d-298">DriversLicense</span></span>
- <span data-ttu-id="cc14d-299">DriversLicenses</span><span class="sxs-lookup"><span data-stu-id="cc14d-299">DriversLicenses</span></span>
- <span data-ttu-id="cc14d-300">Drivers License</span><span class="sxs-lookup"><span data-stu-id="cc14d-300">Drivers License</span></span>
- <span data-ttu-id="cc14d-301">Drivers Licenses</span><span class="sxs-lookup"><span data-stu-id="cc14d-301">Drivers Licenses</span></span>
- <span data-ttu-id="cc14d-302">Driver'License</span><span class="sxs-lookup"><span data-stu-id="cc14d-302">Driver'License</span></span>
- <span data-ttu-id="cc14d-303">Driver'Licenses</span><span class="sxs-lookup"><span data-stu-id="cc14d-303">Driver'Licenses</span></span>
- <span data-ttu-id="cc14d-304">Driver'License</span><span class="sxs-lookup"><span data-stu-id="cc14d-304">Driver' License</span></span>
- <span data-ttu-id="cc14d-305">Driver'Licenses</span><span class="sxs-lookup"><span data-stu-id="cc14d-305">Driver' Licenses</span></span>
- <span data-ttu-id="cc14d-306">Driver'sLicense</span><span class="sxs-lookup"><span data-stu-id="cc14d-306">Driver'sLicense</span></span>
- <span data-ttu-id="cc14d-307">Driver'sLicenses</span><span class="sxs-lookup"><span data-stu-id="cc14d-307">Driver'sLicenses</span></span>
- <span data-ttu-id="cc14d-308">Driver's License</span><span class="sxs-lookup"><span data-stu-id="cc14d-308">Driver's License</span></span>
- <span data-ttu-id="cc14d-309">Driver's Licenses</span><span class="sxs-lookup"><span data-stu-id="cc14d-309">Driver's Licenses</span></span>
- <span data-ttu-id="cc14d-310">DriverLicense #</span><span class="sxs-lookup"><span data-stu-id="cc14d-310">DriverLicense#</span></span>
- <span data-ttu-id="cc14d-311">DriverLicenses #</span><span class="sxs-lookup"><span data-stu-id="cc14d-311">DriverLicenses#</span></span>
- <span data-ttu-id="cc14d-312">Driver License#</span><span class="sxs-lookup"><span data-stu-id="cc14d-312">Driver License#</span></span>
- <span data-ttu-id="cc14d-313">Driver Licenses#</span><span class="sxs-lookup"><span data-stu-id="cc14d-313">Driver Licenses#</span></span>
- <span data-ttu-id="cc14d-314">DriversLicense #</span><span class="sxs-lookup"><span data-stu-id="cc14d-314">DriversLicense#</span></span>
- <span data-ttu-id="cc14d-315">DriversLicenses #</span><span class="sxs-lookup"><span data-stu-id="cc14d-315">DriversLicenses#</span></span>
- <span data-ttu-id="cc14d-316">Drivers License#</span><span class="sxs-lookup"><span data-stu-id="cc14d-316">Drivers License#</span></span>
- <span data-ttu-id="cc14d-317">Drivers Licenses#</span><span class="sxs-lookup"><span data-stu-id="cc14d-317">Drivers Licenses#</span></span>
- <span data-ttu-id="cc14d-318">Driver'License #</span><span class="sxs-lookup"><span data-stu-id="cc14d-318">Driver'License#</span></span>
- <span data-ttu-id="cc14d-319">Driver'Licenses #</span><span class="sxs-lookup"><span data-stu-id="cc14d-319">Driver'Licenses#</span></span>
- <span data-ttu-id="cc14d-320">Driver'License#</span><span class="sxs-lookup"><span data-stu-id="cc14d-320">Driver' License#</span></span>
- <span data-ttu-id="cc14d-321">Driver'Licenses#</span><span class="sxs-lookup"><span data-stu-id="cc14d-321">Driver' Licenses#</span></span>
- <span data-ttu-id="cc14d-322">Driver'sLicense #</span><span class="sxs-lookup"><span data-stu-id="cc14d-322">Driver'sLicense#</span></span>
- <span data-ttu-id="cc14d-323">Driver'sLicenses #</span><span class="sxs-lookup"><span data-stu-id="cc14d-323">Driver'sLicenses#</span></span>
- <span data-ttu-id="cc14d-324">Driver's License#</span><span class="sxs-lookup"><span data-stu-id="cc14d-324">Driver's License#</span></span>
- <span data-ttu-id="cc14d-325">Driver's Licenses#</span><span class="sxs-lookup"><span data-stu-id="cc14d-325">Driver's Licenses#</span></span>
   
## <a name="australia-medical-account-number"></a><span data-ttu-id="cc14d-326">Número de conta médica da Austrália</span><span class="sxs-lookup"><span data-stu-id="cc14d-326">Australia Medical Account Number</span></span>

### <a name="format"></a><span data-ttu-id="cc14d-327">Format</span><span class="sxs-lookup"><span data-stu-id="cc14d-327">Format</span></span>

<span data-ttu-id="cc14d-328">10 a 11 dígitos</span><span class="sxs-lookup"><span data-stu-id="cc14d-328">10-11 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="cc14d-329">Padrão</span><span class="sxs-lookup"><span data-stu-id="cc14d-329">Pattern</span></span>

<span data-ttu-id="cc14d-330">10 a 11 dígitos:</span><span class="sxs-lookup"><span data-stu-id="cc14d-330">10-11 digits:</span></span>
- <span data-ttu-id="cc14d-331">Primeiro dígito está no intervalo de 2 a 6</span><span class="sxs-lookup"><span data-stu-id="cc14d-331">First digit is in the range 2-6</span></span>
- <span data-ttu-id="cc14d-332">O nono dígito é um dígito de verificação</span><span class="sxs-lookup"><span data-stu-id="cc14d-332">Ninth digit is a check digit</span></span>
- <span data-ttu-id="cc14d-333">O décimo dígito é o dígito do problema</span><span class="sxs-lookup"><span data-stu-id="cc14d-333">Tenth digit is the issue digit</span></span>
- <span data-ttu-id="cc14d-334">O décimo primeiro dígito (opcional) é o número individual</span><span class="sxs-lookup"><span data-stu-id="cc14d-334">Eleventh digit (optional) is the individual number</span></span>

### <a name="checksum"></a><span data-ttu-id="cc14d-335">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="cc14d-335">Checksum</span></span>

<span data-ttu-id="cc14d-336">Sim</span><span class="sxs-lookup"><span data-stu-id="cc14d-336">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="cc14d-337">Definição</span><span class="sxs-lookup"><span data-stu-id="cc14d-337">Definition</span></span>

<span data-ttu-id="cc14d-338">Uma política de DLP tem 95% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="cc14d-338">A DLP policy is 95% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="cc14d-339">A função Func_australian_medical_account_number localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="cc14d-339">The function Func_australian_medical_account_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="cc14d-340">Uma palavra-chave de Keyword_Australia_Medical_Account_Number for encontrada.</span><span class="sxs-lookup"><span data-stu-id="cc14d-340">A keyword from Keyword_Australia_Medical_Account_Number is found.</span></span>
- <span data-ttu-id="cc14d-341">A soma de verificação passa.</span><span class="sxs-lookup"><span data-stu-id="cc14d-341">The checksum passes.</span></span>

<span data-ttu-id="cc14d-342">Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="cc14d-342">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="cc14d-343">A função Func_australian_medical_account_number localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="cc14d-343">The function Func_australian_medical_account_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="cc14d-344">A soma de verificação passa.</span><span class="sxs-lookup"><span data-stu-id="cc14d-344">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="cc14d-345">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="cc14d-345">Keywords</span></span>

#### <a name="keywordaustraliamedicalaccountnumber"></a><span data-ttu-id="cc14d-346">Keyword_Australia_Medical_Account_Number</span><span class="sxs-lookup"><span data-stu-id="cc14d-346">Keyword_Australia_Medical_Account_Number</span></span>

- <span data-ttu-id="cc14d-347">bank account details</span><span class="sxs-lookup"><span data-stu-id="cc14d-347">bank account details</span></span>
- <span data-ttu-id="cc14d-348">medicare payments</span><span class="sxs-lookup"><span data-stu-id="cc14d-348">medicare payments</span></span>
- <span data-ttu-id="cc14d-349">mortgage account</span><span class="sxs-lookup"><span data-stu-id="cc14d-349">mortgage account</span></span>
- <span data-ttu-id="cc14d-350">bank payments</span><span class="sxs-lookup"><span data-stu-id="cc14d-350">bank payments</span></span>
- <span data-ttu-id="cc14d-351">information branch</span><span class="sxs-lookup"><span data-stu-id="cc14d-351">information branch</span></span>
- <span data-ttu-id="cc14d-352">credit card loan</span><span class="sxs-lookup"><span data-stu-id="cc14d-352">credit card loan</span></span>
- <span data-ttu-id="cc14d-353">department of human services</span><span class="sxs-lookup"><span data-stu-id="cc14d-353">department of human services</span></span>
- <span data-ttu-id="cc14d-354">local service</span><span class="sxs-lookup"><span data-stu-id="cc14d-354">local service</span></span>
- <span data-ttu-id="cc14d-355">Medicare</span><span class="sxs-lookup"><span data-stu-id="cc14d-355">medicare</span></span>

   
## <a name="australia-passport-number"></a><span data-ttu-id="cc14d-356">Número de passaporte da Austrália</span><span class="sxs-lookup"><span data-stu-id="cc14d-356">Australia Passport Number</span></span>

### <a name="format"></a><span data-ttu-id="cc14d-357">Format</span><span class="sxs-lookup"><span data-stu-id="cc14d-357">Format</span></span>

<span data-ttu-id="cc14d-358">Uma letra seguida por sete dígitos</span><span class="sxs-lookup"><span data-stu-id="cc14d-358">A letter followed by seven digits</span></span>

### <a name="pattern"></a><span data-ttu-id="cc14d-359">Padrão</span><span class="sxs-lookup"><span data-stu-id="cc14d-359">Pattern</span></span>

<span data-ttu-id="cc14d-360">Uma letra (não diferencia maiúsculas de minúsculas) seguida de sete dígitos</span><span class="sxs-lookup"><span data-stu-id="cc14d-360">A letter (not case sensitive) followed by seven digits</span></span>

### <a name="checksum"></a><span data-ttu-id="cc14d-361">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="cc14d-361">Checksum</span></span>

<span data-ttu-id="cc14d-362">Não</span><span class="sxs-lookup"><span data-stu-id="cc14d-362">No</span></span>

### <a name="definition"></a><span data-ttu-id="cc14d-363">Definição</span><span class="sxs-lookup"><span data-stu-id="cc14d-363">Definition</span></span>

<span data-ttu-id="cc14d-364">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="cc14d-364">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="cc14d-365">A expressão regular Regex_australia_passport_number localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="cc14d-365">The regular expression Regex_australia_passport_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="cc14d-366">Uma palavra-chave de Keyword_passport ou Keyword_australia_passport_number for encontrada.</span><span class="sxs-lookup"><span data-stu-id="cc14d-366">A keyword from Keyword_passport or Keyword_australia_passport_number is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="cc14d-367">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="cc14d-367">Keywords</span></span>

#### <a name="keywordpassport"></a><span data-ttu-id="cc14d-368">Keyword_passport</span><span class="sxs-lookup"><span data-stu-id="cc14d-368">Keyword_passport</span></span>

- <span data-ttu-id="cc14d-369">Passport Number</span><span class="sxs-lookup"><span data-stu-id="cc14d-369">Passport Number</span></span>
- <span data-ttu-id="cc14d-370">Passport No</span><span class="sxs-lookup"><span data-stu-id="cc14d-370">Passport No</span></span>
- <span data-ttu-id="cc14d-371">Passport #</span><span class="sxs-lookup"><span data-stu-id="cc14d-371">Passport #</span></span>
- <span data-ttu-id="cc14d-372">Passaport</span><span class="sxs-lookup"><span data-stu-id="cc14d-372">Passport#</span></span>
- <span data-ttu-id="cc14d-373">Passportid</span><span class="sxs-lookup"><span data-stu-id="cc14d-373">PassportID</span></span>
- <span data-ttu-id="cc14d-374">Passportno</span><span class="sxs-lookup"><span data-stu-id="cc14d-374">Passportno</span></span>
- <span data-ttu-id="cc14d-375">passportnumber</span><span class="sxs-lookup"><span data-stu-id="cc14d-375">passportnumber</span></span>
- <span data-ttu-id="cc14d-376">パスポート</span><span class="sxs-lookup"><span data-stu-id="cc14d-376">パスポート</span></span>
- <span data-ttu-id="cc14d-377">パスポート番号</span><span class="sxs-lookup"><span data-stu-id="cc14d-377">パスポート番号</span></span>
- <span data-ttu-id="cc14d-378">パスポートのNum</span><span class="sxs-lookup"><span data-stu-id="cc14d-378">パスポートのNum</span></span>
- <span data-ttu-id="cc14d-379">パスポート ＃</span><span class="sxs-lookup"><span data-stu-id="cc14d-379">パスポート ＃</span></span> 
- <span data-ttu-id="cc14d-380">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="cc14d-380">Numéro de passeport</span></span>
- <span data-ttu-id="cc14d-381">Passeport n °</span><span class="sxs-lookup"><span data-stu-id="cc14d-381">Passeport n °</span></span>
- <span data-ttu-id="cc14d-382">Passeport Non</span><span class="sxs-lookup"><span data-stu-id="cc14d-382">Passeport Non</span></span>
- <span data-ttu-id="cc14d-383">Passeport #</span><span class="sxs-lookup"><span data-stu-id="cc14d-383">Passeport #</span></span>
- <span data-ttu-id="cc14d-384">Passeport #</span><span class="sxs-lookup"><span data-stu-id="cc14d-384">Passeport#</span></span>
- <span data-ttu-id="cc14d-385">PasseportNon</span><span class="sxs-lookup"><span data-stu-id="cc14d-385">PasseportNon</span></span>
- <span data-ttu-id="cc14d-386">Passeportn °</span><span class="sxs-lookup"><span data-stu-id="cc14d-386">Passeportn °</span></span>

#### <a name="keywordaustraliapassportnumber"></a><span data-ttu-id="cc14d-387">Keyword_australia_passport_number</span><span class="sxs-lookup"><span data-stu-id="cc14d-387">Keyword_australia_passport_number</span></span>

- <span data-ttu-id="cc14d-388">Passaport</span><span class="sxs-lookup"><span data-stu-id="cc14d-388">passport</span></span>
- <span data-ttu-id="cc14d-389">passport details</span><span class="sxs-lookup"><span data-stu-id="cc14d-389">passport details</span></span>
- <span data-ttu-id="cc14d-390">immigration and citizenship</span><span class="sxs-lookup"><span data-stu-id="cc14d-390">immigration and citizenship</span></span>
- <span data-ttu-id="cc14d-391">commonwealth of australia</span><span class="sxs-lookup"><span data-stu-id="cc14d-391">commonwealth of australia</span></span>
- <span data-ttu-id="cc14d-392">department of immigration</span><span class="sxs-lookup"><span data-stu-id="cc14d-392">department of immigration</span></span>
- <span data-ttu-id="cc14d-393">residential address</span><span class="sxs-lookup"><span data-stu-id="cc14d-393">residential address</span></span>
- <span data-ttu-id="cc14d-394">department of immigration and citizenship</span><span class="sxs-lookup"><span data-stu-id="cc14d-394">department of immigration and citizenship</span></span>
- <span data-ttu-id="cc14d-395">cartões</span><span class="sxs-lookup"><span data-stu-id="cc14d-395">visa</span></span>
- <span data-ttu-id="cc14d-396">national identity card</span><span class="sxs-lookup"><span data-stu-id="cc14d-396">national identity card</span></span>
- <span data-ttu-id="cc14d-397">passport number</span><span class="sxs-lookup"><span data-stu-id="cc14d-397">passport number</span></span>
- <span data-ttu-id="cc14d-398">travel document</span><span class="sxs-lookup"><span data-stu-id="cc14d-398">travel document</span></span>
- <span data-ttu-id="cc14d-399">issuing authority</span><span class="sxs-lookup"><span data-stu-id="cc14d-399">issuing authority</span></span>
   
## <a name="australia-tax-file-number"></a><span data-ttu-id="cc14d-400">Número de imposto de renda da Austrália</span><span class="sxs-lookup"><span data-stu-id="cc14d-400">Australia Tax File Number</span></span>

### <a name="format"></a><span data-ttu-id="cc14d-401">Format</span><span class="sxs-lookup"><span data-stu-id="cc14d-401">Format</span></span>

<span data-ttu-id="cc14d-402">8 a 9 dígitos</span><span class="sxs-lookup"><span data-stu-id="cc14d-402">8-9 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="cc14d-403">Padrão</span><span class="sxs-lookup"><span data-stu-id="cc14d-403">Pattern</span></span>

<span data-ttu-id="cc14d-404">8 a 9 dígitos normalmente apresentados com espaços, da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="cc14d-404">8-9 digits typically presented with spaces as follows:</span></span>
- <span data-ttu-id="cc14d-405">Três dígitos</span><span class="sxs-lookup"><span data-stu-id="cc14d-405">Three digits</span></span> 
- <span data-ttu-id="cc14d-406">Um espaço opcional</span><span class="sxs-lookup"><span data-stu-id="cc14d-406">An optional space</span></span> 
- <span data-ttu-id="cc14d-407">Três dígitos</span><span class="sxs-lookup"><span data-stu-id="cc14d-407">Three digits</span></span> 
- <span data-ttu-id="cc14d-408">Um espaço opcional</span><span class="sxs-lookup"><span data-stu-id="cc14d-408">An optional space</span></span> 
- <span data-ttu-id="cc14d-409">2 a 3 dígitos em que o último dígito é um dígito de verificação</span><span class="sxs-lookup"><span data-stu-id="cc14d-409">2-3 digits where the last digit is a check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="cc14d-410">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="cc14d-410">Checksum</span></span>

<span data-ttu-id="cc14d-411">Sim</span><span class="sxs-lookup"><span data-stu-id="cc14d-411">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="cc14d-412">Definição</span><span class="sxs-lookup"><span data-stu-id="cc14d-412">Definition</span></span>

<span data-ttu-id="cc14d-413">Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="cc14d-413">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="cc14d-414">A função Func_australian_tax_file_number localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="cc14d-414">The function Func_australian_tax_file_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="cc14d-415">Nenhuma palavra-chave de Keyword_Australia_Tax_File_Number ou Keyword_number_exclusions for encontrada.</span><span class="sxs-lookup"><span data-stu-id="cc14d-415">No keyword from Keyword_Australia_Tax_File_Number or Keyword_number_exclusions is found.</span></span>
- <span data-ttu-id="cc14d-416">A soma de verificação passa.</span><span class="sxs-lookup"><span data-stu-id="cc14d-416">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="cc14d-417">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="cc14d-417">Keywords</span></span>

#### <a name="keywordaustraliataxfilenumber"></a><span data-ttu-id="cc14d-418">Keyword_Australia_Tax_File_Number</span><span class="sxs-lookup"><span data-stu-id="cc14d-418">Keyword_Australia_Tax_File_Number</span></span>

- <span data-ttu-id="cc14d-419">australian business number</span><span class="sxs-lookup"><span data-stu-id="cc14d-419">australian business number</span></span>
- <span data-ttu-id="cc14d-420">marginal tax rate</span><span class="sxs-lookup"><span data-stu-id="cc14d-420">marginal tax rate</span></span>
- <span data-ttu-id="cc14d-421">medicare levy</span><span class="sxs-lookup"><span data-stu-id="cc14d-421">medicare levy</span></span>
- <span data-ttu-id="cc14d-422">portfolio number</span><span class="sxs-lookup"><span data-stu-id="cc14d-422">portfolio number</span></span>
- <span data-ttu-id="cc14d-423">service veterans</span><span class="sxs-lookup"><span data-stu-id="cc14d-423">service veterans</span></span>
- <span data-ttu-id="cc14d-424">withholding tax</span><span class="sxs-lookup"><span data-stu-id="cc14d-424">withholding tax</span></span>
- <span data-ttu-id="cc14d-425">individual tax return</span><span class="sxs-lookup"><span data-stu-id="cc14d-425">individual tax return</span></span>
- <span data-ttu-id="cc14d-426">tax file number</span><span class="sxs-lookup"><span data-stu-id="cc14d-426">tax file number</span></span>

#### <a name="keywordnumberexclusions"></a><span data-ttu-id="cc14d-427">Keyword_number_exclusions</span><span class="sxs-lookup"><span data-stu-id="cc14d-427">Keyword_number_exclusions</span></span>

- <span data-ttu-id="cc14d-428">00000000</span><span class="sxs-lookup"><span data-stu-id="cc14d-428">00000000</span></span>
- <span data-ttu-id="cc14d-429">11111111</span><span class="sxs-lookup"><span data-stu-id="cc14d-429">11111111</span></span>
- <span data-ttu-id="cc14d-430">22222222</span><span class="sxs-lookup"><span data-stu-id="cc14d-430">22222222</span></span>
- <span data-ttu-id="cc14d-431">33333333</span><span class="sxs-lookup"><span data-stu-id="cc14d-431">33333333</span></span>
- <span data-ttu-id="cc14d-432">44444444</span><span class="sxs-lookup"><span data-stu-id="cc14d-432">44444444</span></span>
- <span data-ttu-id="cc14d-433">55555555</span><span class="sxs-lookup"><span data-stu-id="cc14d-433">55555555</span></span>
- <span data-ttu-id="cc14d-434">66666666</span><span class="sxs-lookup"><span data-stu-id="cc14d-434">66666666</span></span>
- <span data-ttu-id="cc14d-435">77777777</span><span class="sxs-lookup"><span data-stu-id="cc14d-435">77777777</span></span>
- <span data-ttu-id="cc14d-436">88888888</span><span class="sxs-lookup"><span data-stu-id="cc14d-436">88888888</span></span>
- <span data-ttu-id="cc14d-437">99999999</span><span class="sxs-lookup"><span data-stu-id="cc14d-437">99999999</span></span>
- <span data-ttu-id="cc14d-438">000000000</span><span class="sxs-lookup"><span data-stu-id="cc14d-438">000000000</span></span>
- <span data-ttu-id="cc14d-439">111111111</span><span class="sxs-lookup"><span data-stu-id="cc14d-439">111111111</span></span>
- <span data-ttu-id="cc14d-440">222222222</span><span class="sxs-lookup"><span data-stu-id="cc14d-440">222222222</span></span>
- <span data-ttu-id="cc14d-441">333333333</span><span class="sxs-lookup"><span data-stu-id="cc14d-441">333333333</span></span>
- <span data-ttu-id="cc14d-442">444444444</span><span class="sxs-lookup"><span data-stu-id="cc14d-442">444444444</span></span>
- <span data-ttu-id="cc14d-443">555555555</span><span class="sxs-lookup"><span data-stu-id="cc14d-443">555555555</span></span>
- <span data-ttu-id="cc14d-444">666666666</span><span class="sxs-lookup"><span data-stu-id="cc14d-444">666666666</span></span>
- <span data-ttu-id="cc14d-445">777777777</span><span class="sxs-lookup"><span data-stu-id="cc14d-445">777777777</span></span>
- <span data-ttu-id="cc14d-446">888888888</span><span class="sxs-lookup"><span data-stu-id="cc14d-446">888888888</span></span>
- <span data-ttu-id="cc14d-447">999999999</span><span class="sxs-lookup"><span data-stu-id="cc14d-447">999999999</span></span>
- <span data-ttu-id="cc14d-448">0000000000</span><span class="sxs-lookup"><span data-stu-id="cc14d-448">0000000000</span></span>
- <span data-ttu-id="cc14d-449">1111111111</span><span class="sxs-lookup"><span data-stu-id="cc14d-449">1111111111</span></span>
- <span data-ttu-id="cc14d-450">2222222222</span><span class="sxs-lookup"><span data-stu-id="cc14d-450">2222222222</span></span>
- <span data-ttu-id="cc14d-451">3333333333</span><span class="sxs-lookup"><span data-stu-id="cc14d-451">3333333333</span></span>
- <span data-ttu-id="cc14d-452">4444444444</span><span class="sxs-lookup"><span data-stu-id="cc14d-452">4444444444</span></span>
- <span data-ttu-id="cc14d-453">5555555555</span><span class="sxs-lookup"><span data-stu-id="cc14d-453">5555555555</span></span>
- <span data-ttu-id="cc14d-454">6666666666</span><span class="sxs-lookup"><span data-stu-id="cc14d-454">6666666666</span></span>
- <span data-ttu-id="cc14d-455">7777777777</span><span class="sxs-lookup"><span data-stu-id="cc14d-455">7777777777</span></span>
- <span data-ttu-id="cc14d-456">8888888888</span><span class="sxs-lookup"><span data-stu-id="cc14d-456">8888888888</span></span>
- <span data-ttu-id="cc14d-457">9999999999</span><span class="sxs-lookup"><span data-stu-id="cc14d-457">9999999999</span></span>

## <a name="azure-documentdb-auth-key"></a><span data-ttu-id="cc14d-458">Chave de autenticação do Azure DocumentDB</span><span class="sxs-lookup"><span data-stu-id="cc14d-458">Azure DocumentDB Auth Key</span></span>

### <a name="format"></a><span data-ttu-id="cc14d-459">Format</span><span class="sxs-lookup"><span data-stu-id="cc14d-459">Format</span></span>

<span data-ttu-id="cc14d-460">A cadeia de caracteres "DocumentDb" seguida dos caracteres e cadeias de caracteres descritos no padrão abaixo.</span><span class="sxs-lookup"><span data-stu-id="cc14d-460">The string "DocumentDb" followed by the characters and strings outlined in the pattern below.</span></span>

### <a name="pattern"></a><span data-ttu-id="cc14d-461">Padrão</span><span class="sxs-lookup"><span data-stu-id="cc14d-461">Pattern</span></span>

- <span data-ttu-id="cc14d-462">A cadeia de caracteres "DocumentDb"</span><span class="sxs-lookup"><span data-stu-id="cc14d-462">The string "DocumentDb"</span></span>
- <span data-ttu-id="cc14d-463">Qualquer combinação entre 3-200 letras minúsculas ou maiúsculas, dígitos, símbolos, caracteres especiais ou espaços</span><span class="sxs-lookup"><span data-stu-id="cc14d-463">Any combination of between 3-200 lower- or uppercase letters, digits, symbols, special characters, or spaces</span></span>
- <span data-ttu-id="cc14d-464">Um símbolo maior que (>), um sinal de igual (=), uma aspa (") ou um apóstrofo (')</span><span class="sxs-lookup"><span data-stu-id="cc14d-464">A greater than symbol (>), an equal sign (=), a quotation mark ("), or an apostrophe (')</span></span>
- <span data-ttu-id="cc14d-465">Qualquer combinação de 86 letras minúsculas ou maiúsculas, dígitos, barra de avanço (/) ou sinal de adição (+)</span><span class="sxs-lookup"><span data-stu-id="cc14d-465">Any combination of 86 lower- or uppercase letters, digits, forward slash (/), or plus sign (+)</span></span>
- <span data-ttu-id="cc14d-466">Dois sinais de igual (=)</span><span class="sxs-lookup"><span data-stu-id="cc14d-466">Two equal signs (=)</span></span>

### <a name="checksum"></a><span data-ttu-id="cc14d-467">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="cc14d-467">Checksum</span></span>

<span data-ttu-id="cc14d-468">Não</span><span class="sxs-lookup"><span data-stu-id="cc14d-468">No</span></span>

### <a name="definition"></a><span data-ttu-id="cc14d-469">Definição</span><span class="sxs-lookup"><span data-stu-id="cc14d-469">Definition</span></span>

<span data-ttu-id="cc14d-470">Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="cc14d-470">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="cc14d-471">A expressão regular CEP_Regex_AzureDocumentDBAuthKey localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="cc14d-471">The regular expression CEP_Regex_AzureDocumentDBAuthKey finds content that matches the pattern.</span></span>
- <span data-ttu-id="cc14d-472">A expressão regular CEP_CommonExampleKeywords não \*\*\*\* localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="cc14d-472">The regular expression CEP_CommonExampleKeywords does **not** find content that matches the pattern.</span></span>

```
<!-- Azure Document DB Auth Key -->
<Entity id="0f587d92-eb28-44a9-bd1c-90f2892b47aa" patternsProximity="300" recommendedConfidence="85">
  <Pattern confidenceLevel="85">
        <IdMatch idRef="CEP_Regex_AzureDocumentDBAuthKey" />
        <Any minMatches="0" maxMatches="0">
            <Match idRef="CEP_CommonExampleKeywords" />
          </Any>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="cc14d-473">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="cc14d-473">Keywords</span></span>

#### <a name="cepcommonexamplekeywords"></a><span data-ttu-id="cc14d-474">CEP_CommonExampleKeywords</span><span class="sxs-lookup"><span data-stu-id="cc14d-474">CEP_CommonExampleKeywords</span></span>

<span data-ttu-id="cc14d-475">(Observe que tecnicamente, esse tipo de informação confidencial identifica essas palavras-chave usando uma expressão regular, não uma lista de palavras-chave.)</span><span class="sxs-lookup"><span data-stu-id="cc14d-475">(Note that technically, this sensitive information type identifies these keywords by using a regular expression, not a keyword list.)</span></span>

- <span data-ttu-id="cc14d-476">contoso</span><span class="sxs-lookup"><span data-stu-id="cc14d-476">contoso</span></span>
- <span data-ttu-id="cc14d-477">fabrikam</span><span class="sxs-lookup"><span data-stu-id="cc14d-477">fabrikam</span></span>
- <span data-ttu-id="cc14d-478">Northwind</span><span class="sxs-lookup"><span data-stu-id="cc14d-478">northwind</span></span>
- <span data-ttu-id="cc14d-479">área restrita</span><span class="sxs-lookup"><span data-stu-id="cc14d-479">sandbox</span></span>
- <span data-ttu-id="cc14d-480">Onebox</span><span class="sxs-lookup"><span data-stu-id="cc14d-480">onebox</span></span>
- <span data-ttu-id="cc14d-481">localhost</span><span class="sxs-lookup"><span data-stu-id="cc14d-481">localhost</span></span>
- <span data-ttu-id="cc14d-482">127.0.0.1</span><span class="sxs-lookup"><span data-stu-id="cc14d-482">127.0.0.1</span></span>
- <span data-ttu-id="cc14d-483">testacs. <!--no-hyperlink-->com</span><span class="sxs-lookup"><span data-stu-id="cc14d-483">testacs.<!--no-hyperlink-->com</span></span>
- <span data-ttu-id="cc14d-484">s-int.<!--no-hyperlink-->net</span><span class="sxs-lookup"><span data-stu-id="cc14d-484">s-int.<!--no-hyperlink-->net</span></span>

## <a name="azure-iaas-database-connection-string-and-azure-sql-connection-string"></a><span data-ttu-id="cc14d-485">Cadeia de conexão de banco de dados Azure IAAS e cadeia de conexão do Azure SQL</span><span class="sxs-lookup"><span data-stu-id="cc14d-485">Azure IAAS Database Connection String and Azure SQL Connection String</span></span>

### <a name="format"></a><span data-ttu-id="cc14d-486">Format</span><span class="sxs-lookup"><span data-stu-id="cc14d-486">Format</span></span>

<span data-ttu-id="cc14d-487">A cadeia de caracteres "Server", "Server" ou "Data Source" seguida dos caracteres e cadeias de caracteres descritos no padrão abaixo, incluindo a cadeia de caracteres "cloudapp. Azure. <!--no-hyperlink-->com "ou" cloudapp. Azure. <!--no-hyperlink-->net "ou" Database. Windows. <!--no-hyperlink-->net ", e a cadeia de caracteres" password "ou" password "ou" pwd ".</span><span class="sxs-lookup"><span data-stu-id="cc14d-487">The string "Server", "server", or "data source" followed by the characters and strings outlined in the pattern below, including the string "cloudapp.azure.<!--no-hyperlink-->com" or "cloudapp.azure.<!--no-hyperlink-->net" or "database.windows.<!--no-hyperlink-->net", and the string "Password" or "password" or "pwd".</span></span>

### <a name="pattern"></a><span data-ttu-id="cc14d-488">Padrão</span><span class="sxs-lookup"><span data-stu-id="cc14d-488">Pattern</span></span>

- <span data-ttu-id="cc14d-489">A cadeia de caracteres "Server", "Server" ou "Data Source"</span><span class="sxs-lookup"><span data-stu-id="cc14d-489">The string "Server", "server", or "data source"</span></span>
- <span data-ttu-id="cc14d-490">0-2 caracteres de espaço em branco</span><span class="sxs-lookup"><span data-stu-id="cc14d-490">0-2 whitespace characters</span></span>
- <span data-ttu-id="cc14d-491">Um sinal de igual (=)</span><span class="sxs-lookup"><span data-stu-id="cc14d-491">An equal sign (=)</span></span>
- <span data-ttu-id="cc14d-492">0-2 caracteres de espaço em branco</span><span class="sxs-lookup"><span data-stu-id="cc14d-492">0-2 whitespace characters</span></span>
- <span data-ttu-id="cc14d-493">Qualquer combinação entre 1-200 letras minúsculas ou maiúsculas, dígitos, símbolos, caracteres especiais ou espaços</span><span class="sxs-lookup"><span data-stu-id="cc14d-493">Any combination of between 1-200 lower- or uppercase letters, digits, symbols, special characters, or spaces</span></span>
- <span data-ttu-id="cc14d-494">A cadeia de caracteres "cloudapp. Azure. <!--no-hyperlink-->com "," cloudapp. Azure. <!--no-hyperlink-->net "ou" Database. Windows. <!--no-hyperlink-->net "</span><span class="sxs-lookup"><span data-stu-id="cc14d-494">The string "cloudapp.azure.<!--no-hyperlink-->com", "cloudapp.azure.<!--no-hyperlink-->net", or "database.windows.<!--no-hyperlink-->net"</span></span>
- <span data-ttu-id="cc14d-495">Qualquer combinação entre 1-300 letras minúsculas ou maiúsculas, dígitos, símbolos, caracteres especiais ou espaços</span><span class="sxs-lookup"><span data-stu-id="cc14d-495">Any combination of between 1-300 lower- or uppercase letters, digits, symbols, special characters, or spaces</span></span>
- <span data-ttu-id="cc14d-496">A cadeia de caracteres "password", "password" ou "pwd"</span><span class="sxs-lookup"><span data-stu-id="cc14d-496">The string "Password", "password", or "pwd"</span></span>
- <span data-ttu-id="cc14d-497">0-2 caracteres de espaço em branco</span><span class="sxs-lookup"><span data-stu-id="cc14d-497">0-2 whitespace characters</span></span>
- <span data-ttu-id="cc14d-498">Um sinal de igual (=)</span><span class="sxs-lookup"><span data-stu-id="cc14d-498">An equal sign (=)</span></span>
- <span data-ttu-id="cc14d-499">0-2 caracteres de espaço em branco</span><span class="sxs-lookup"><span data-stu-id="cc14d-499">0-2 whitespace characters</span></span>
- <span data-ttu-id="cc14d-500">Um ou mais caracteres que não são ponto-e-vírgula (;), aspas (") ou apóstrofo (')</span><span class="sxs-lookup"><span data-stu-id="cc14d-500">One or more characters that is not a semicolon (;), quotation mark ("), or apostrophe (')</span></span>
- <span data-ttu-id="cc14d-501">Um ponto e vírgula (;), aspas (") ou apóstrofo (')</span><span class="sxs-lookup"><span data-stu-id="cc14d-501">A semicolon (;), quotation mark ("), or apostrophe (')</span></span>

### <a name="checksum"></a><span data-ttu-id="cc14d-502">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="cc14d-502">Checksum</span></span>

<span data-ttu-id="cc14d-503">Não</span><span class="sxs-lookup"><span data-stu-id="cc14d-503">No</span></span>

### <a name="definition"></a><span data-ttu-id="cc14d-504">Definição</span><span class="sxs-lookup"><span data-stu-id="cc14d-504">Definition</span></span>

<span data-ttu-id="cc14d-505">Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="cc14d-505">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="cc14d-506">A expressão regular CEP_Regex_AzureConnectionString localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="cc14d-506">The regular expression CEP_Regex_AzureConnectionString finds content that matches the pattern.</span></span>
- <span data-ttu-id="cc14d-507">A expressão regular CEP_CommonExampleKeywords não \*\*\*\* localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="cc14d-507">The regular expression CEP_CommonExampleKeywords does **not** find content that matches the pattern.</span></span>

```
<!--Azure IAAS Database Connection String and Azure SQL Connection String-->
<Entity id="ce1a126d-186f-4700-8c0c-486157b953fd" patternsProximity="300" recommendedConfidence="85">
  <Pattern confidenceLevel="85">
        <IdMatch idRef="CEP_Regex_AzureConnectionString" />
        <Any minMatches="0" maxMatches="0">
            <Match idRef="CEP_CommonExampleKeywords" />
        </Any>
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="cc14d-508">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="cc14d-508">Keywords</span></span>

#### <a name="cepcommonexamplekeywords"></a><span data-ttu-id="cc14d-509">CEP_CommonExampleKeywords</span><span class="sxs-lookup"><span data-stu-id="cc14d-509">CEP_CommonExampleKeywords</span></span>

<span data-ttu-id="cc14d-510">(Observe que tecnicamente, esse tipo de informação confidencial identifica essas palavras-chave usando uma expressão regular, não uma lista de palavras-chave.)</span><span class="sxs-lookup"><span data-stu-id="cc14d-510">(Note that technically, this sensitive information type identifies these keywords by using a regular expression, not a keyword list.)</span></span>

- <span data-ttu-id="cc14d-511">contoso</span><span class="sxs-lookup"><span data-stu-id="cc14d-511">contoso</span></span>
- <span data-ttu-id="cc14d-512">fabrikam</span><span class="sxs-lookup"><span data-stu-id="cc14d-512">fabrikam</span></span>
- <span data-ttu-id="cc14d-513">Northwind</span><span class="sxs-lookup"><span data-stu-id="cc14d-513">northwind</span></span>
- <span data-ttu-id="cc14d-514">área restrita</span><span class="sxs-lookup"><span data-stu-id="cc14d-514">sandbox</span></span>
- <span data-ttu-id="cc14d-515">Onebox</span><span class="sxs-lookup"><span data-stu-id="cc14d-515">onebox</span></span>
- <span data-ttu-id="cc14d-516">localhost</span><span class="sxs-lookup"><span data-stu-id="cc14d-516">localhost</span></span>
- <span data-ttu-id="cc14d-517">127.0.0.1</span><span class="sxs-lookup"><span data-stu-id="cc14d-517">127.0.0.1</span></span>
- <span data-ttu-id="cc14d-518">testacs. <!--no-hyperlink-->com</span><span class="sxs-lookup"><span data-stu-id="cc14d-518">testacs.<!--no-hyperlink-->com</span></span>
- <span data-ttu-id="cc14d-519">s-int.<!--no-hyperlink-->net</span><span class="sxs-lookup"><span data-stu-id="cc14d-519">s-int.<!--no-hyperlink-->net</span></span>

## <a name="azure-iot-connection-string"></a><span data-ttu-id="cc14d-520">Cadeia de conexão IoT do Azure</span><span class="sxs-lookup"><span data-stu-id="cc14d-520">Azure IoT Connection String</span></span>

### <a name="format"></a><span data-ttu-id="cc14d-521">Format</span><span class="sxs-lookup"><span data-stu-id="cc14d-521">Format</span></span>

<span data-ttu-id="cc14d-522">A cadeia de caracteres "HostName" seguida dos caracteres e cadeias de caracteres descritos no padrão abaixo, incluindo as cadeias de caracteres "Azure-Devices. <!--no-hyperlink-->net "e" SharedAccessKey ".</span><span class="sxs-lookup"><span data-stu-id="cc14d-522">The string "HostName" followed by the characters and strings outlined in the pattern below, including the strings "azure-devices.<!--no-hyperlink-->net" and "SharedAccessKey".</span></span>

### <a name="pattern"></a><span data-ttu-id="cc14d-523">Padrão</span><span class="sxs-lookup"><span data-stu-id="cc14d-523">Pattern</span></span>

- <span data-ttu-id="cc14d-524">A cadeia de caracteres "HostName"</span><span class="sxs-lookup"><span data-stu-id="cc14d-524">The string "HostName"</span></span>
- <span data-ttu-id="cc14d-525">0-2 caracteres de espaço em branco</span><span class="sxs-lookup"><span data-stu-id="cc14d-525">0-2 whitespace characters</span></span>
- <span data-ttu-id="cc14d-526">Um sinal de igual (=)</span><span class="sxs-lookup"><span data-stu-id="cc14d-526">An equal sign (=)</span></span>
- <span data-ttu-id="cc14d-527">0-2 caracteres de espaço em branco</span><span class="sxs-lookup"><span data-stu-id="cc14d-527">0-2 whitespace characters</span></span>
- <span data-ttu-id="cc14d-528">Qualquer combinação entre 1-200 letras minúsculas ou maiúsculas, dígitos, símbolos, caracteres especiais ou espaços</span><span class="sxs-lookup"><span data-stu-id="cc14d-528">Any combination of between 1-200 lower- or uppercase letters, digits, symbols, special characters, or spaces</span></span>
- <span data-ttu-id="cc14d-529">A cadeia de caracteres "Azure-Devices. <!--no-hyperlink-->net "</span><span class="sxs-lookup"><span data-stu-id="cc14d-529">The string "azure-devices.<!--no-hyperlink-->net"</span></span>
- <span data-ttu-id="cc14d-530">Qualquer combinação entre 1-200 letras minúsculas ou maiúsculas, dígitos, símbolos, caracteres especiais ou espaços</span><span class="sxs-lookup"><span data-stu-id="cc14d-530">Any combination of between 1-200 lower- or uppercase letters, digits, symbols, special characters, or spaces</span></span>
- <span data-ttu-id="cc14d-531">A cadeia de caracteres "SharedAccessKey"</span><span class="sxs-lookup"><span data-stu-id="cc14d-531">The string "SharedAccessKey"</span></span>
- <span data-ttu-id="cc14d-532">0-2 caracteres de espaço em branco</span><span class="sxs-lookup"><span data-stu-id="cc14d-532">0-2 whitespace characters</span></span>
- <span data-ttu-id="cc14d-533">Um sinal de igual (=)</span><span class="sxs-lookup"><span data-stu-id="cc14d-533">An equal sign (=)</span></span>
- <span data-ttu-id="cc14d-534">0-2 caracteres de espaço em branco</span><span class="sxs-lookup"><span data-stu-id="cc14d-534">0-2 whitespace characters</span></span>
- <span data-ttu-id="cc14d-535">Qualquer combinação de 43 letras minúsculas ou maiúsculas, dígitos, barra de avanço (/) ou sinal de adição (+)</span><span class="sxs-lookup"><span data-stu-id="cc14d-535">Any combination of 43 lower- or uppercase letters, digits, forward slash (/), or plus sign (+)</span></span>
- <span data-ttu-id="cc14d-536">Um sinal de igual (=)</span><span class="sxs-lookup"><span data-stu-id="cc14d-536">An equal sign (=)</span></span>

### <a name="checksum"></a><span data-ttu-id="cc14d-537">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="cc14d-537">Checksum</span></span>

<span data-ttu-id="cc14d-538">Não</span><span class="sxs-lookup"><span data-stu-id="cc14d-538">No</span></span>

### <a name="definition"></a><span data-ttu-id="cc14d-539">Definição</span><span class="sxs-lookup"><span data-stu-id="cc14d-539">Definition</span></span>

<span data-ttu-id="cc14d-540">Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="cc14d-540">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="cc14d-541">A expressão regular CEP_Regex_AzureIoTConnectionString localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="cc14d-541">The regular expression CEP_Regex_AzureIoTConnectionString finds content that matches the pattern.</span></span>
- <span data-ttu-id="cc14d-542">A expressão regular CEP_CommonExampleKeywords não \*\*\*\* localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="cc14d-542">The regular expression CEP_CommonExampleKeywords does **not** find content that matches the pattern.</span></span>

```
<!--Azure IoT Connection String-->
<Entity id="0b34bec3-d5d6-4974-b7b0-dcdb5c90c29d" patternsProximity="300" recommendedConfidence="85">
  <Pattern confidenceLevel="85">
        <IdMatch idRef="CEP_Regex_AzureIoTConnectionString" />
        <Any minMatches="0" maxMatches="0">
            <Match idRef="CEP_CommonExampleKeywords" />
        </Any>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="cc14d-543">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="cc14d-543">Keywords</span></span>

#### <a name="cepcommonexamplekeywords"></a><span data-ttu-id="cc14d-544">CEP_CommonExampleKeywords</span><span class="sxs-lookup"><span data-stu-id="cc14d-544">CEP_CommonExampleKeywords</span></span>

<span data-ttu-id="cc14d-545">(Observe que tecnicamente, esse tipo de informação confidencial identifica essas palavras-chave usando uma expressão regular, não uma lista de palavras-chave.)</span><span class="sxs-lookup"><span data-stu-id="cc14d-545">(Note that technically, this sensitive information type identifies these keywords by using a regular expression, not a keyword list.)</span></span>

- <span data-ttu-id="cc14d-546">contoso</span><span class="sxs-lookup"><span data-stu-id="cc14d-546">contoso</span></span>
- <span data-ttu-id="cc14d-547">fabrikam</span><span class="sxs-lookup"><span data-stu-id="cc14d-547">fabrikam</span></span>
- <span data-ttu-id="cc14d-548">Northwind</span><span class="sxs-lookup"><span data-stu-id="cc14d-548">northwind</span></span>
- <span data-ttu-id="cc14d-549">área restrita</span><span class="sxs-lookup"><span data-stu-id="cc14d-549">sandbox</span></span>
- <span data-ttu-id="cc14d-550">Onebox</span><span class="sxs-lookup"><span data-stu-id="cc14d-550">onebox</span></span>
- <span data-ttu-id="cc14d-551">localhost</span><span class="sxs-lookup"><span data-stu-id="cc14d-551">localhost</span></span>
- <span data-ttu-id="cc14d-552">127.0.0.1</span><span class="sxs-lookup"><span data-stu-id="cc14d-552">127.0.0.1</span></span>
- <span data-ttu-id="cc14d-553">testacs. <!--no-hyperlink-->com</span><span class="sxs-lookup"><span data-stu-id="cc14d-553">testacs.<!--no-hyperlink-->com</span></span>
- <span data-ttu-id="cc14d-554">s-int.<!--no-hyperlink-->net</span><span class="sxs-lookup"><span data-stu-id="cc14d-554">s-int.<!--no-hyperlink-->net</span></span>

## <a name="azure-publish-setting-password"></a><span data-ttu-id="cc14d-555">Senha de configuração de publicação do Azure</span><span class="sxs-lookup"><span data-stu-id="cc14d-555">Azure Publish Setting Password</span></span>

### <a name="format"></a><span data-ttu-id="cc14d-556">Format</span><span class="sxs-lookup"><span data-stu-id="cc14d-556">Format</span></span>

<span data-ttu-id="cc14d-557">A cadeia de caracteres "userpwd =" seguida de uma cadeia de caracteres alfanumérica.</span><span class="sxs-lookup"><span data-stu-id="cc14d-557">The string "userpwd=" followed by an alphanumeric string.</span></span>

### <a name="pattern"></a><span data-ttu-id="cc14d-558">Padrão</span><span class="sxs-lookup"><span data-stu-id="cc14d-558">Pattern</span></span>

- <span data-ttu-id="cc14d-559">A cadeia de caracteres "userpwd ="</span><span class="sxs-lookup"><span data-stu-id="cc14d-559">The string "userpwd="</span></span>
- <span data-ttu-id="cc14d-560">Qualquer combinação de letras minúsculas ou dígitos de 60</span><span class="sxs-lookup"><span data-stu-id="cc14d-560">Any combination of 60 lowercase letters or digits</span></span>
- <span data-ttu-id="cc14d-561">Aspas (")</span><span class="sxs-lookup"><span data-stu-id="cc14d-561">A quotation mark (")</span></span>

### <a name="checksum"></a><span data-ttu-id="cc14d-562">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="cc14d-562">Checksum</span></span>

<span data-ttu-id="cc14d-563">Não</span><span class="sxs-lookup"><span data-stu-id="cc14d-563">No</span></span>

### <a name="definition"></a><span data-ttu-id="cc14d-564">Definição</span><span class="sxs-lookup"><span data-stu-id="cc14d-564">Definition</span></span>

<span data-ttu-id="cc14d-565">Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="cc14d-565">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="cc14d-566">A expressão regular CEP_Regex_AzurePublishSettingPasswords localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="cc14d-566">The regular expression CEP_Regex_AzurePublishSettingPasswords finds content that matches the pattern.</span></span>
- <span data-ttu-id="cc14d-567">A expressão regular CEP_CommonExampleKeywords não \*\*\*\* localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="cc14d-567">The regular expression CEP_CommonExampleKeywords does **not** find content that matches the pattern.</span></span>


```
<!--Azure Publish Setting Password-->
<Entity id="75f4cc8a-a68e-49e5-89ce-fa8f03d286a5" patternsProximity="300" recommendedConfidence="85">
  <Pattern confidenceLevel="85">
       <IdMatch idRef="CEP_Regex_AzurePublishSettingPasswords" />
       <Any minMatches="0" maxMatches="0">
           <Match idRef="CEP_CommonExampleKeywords" />
       </Any>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="cc14d-568">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="cc14d-568">Keywords</span></span>

#### <a name="cepcommonexamplekeywords"></a><span data-ttu-id="cc14d-569">CEP_CommonExampleKeywords</span><span class="sxs-lookup"><span data-stu-id="cc14d-569">CEP_CommonExampleKeywords</span></span>

<span data-ttu-id="cc14d-570">(Observe que tecnicamente, esse tipo de informação confidencial identifica essas palavras-chave usando uma expressão regular, não uma lista de palavras-chave.)</span><span class="sxs-lookup"><span data-stu-id="cc14d-570">(Note that technically, this sensitive information type identifies these keywords by using a regular expression, not a keyword list.)</span></span>

- <span data-ttu-id="cc14d-571">contoso</span><span class="sxs-lookup"><span data-stu-id="cc14d-571">contoso</span></span>
- <span data-ttu-id="cc14d-572">fabrikam</span><span class="sxs-lookup"><span data-stu-id="cc14d-572">fabrikam</span></span>
- <span data-ttu-id="cc14d-573">Northwind</span><span class="sxs-lookup"><span data-stu-id="cc14d-573">northwind</span></span>
- <span data-ttu-id="cc14d-574">área restrita</span><span class="sxs-lookup"><span data-stu-id="cc14d-574">sandbox</span></span>
- <span data-ttu-id="cc14d-575">Onebox</span><span class="sxs-lookup"><span data-stu-id="cc14d-575">onebox</span></span>
- <span data-ttu-id="cc14d-576">localhost</span><span class="sxs-lookup"><span data-stu-id="cc14d-576">localhost</span></span>
- <span data-ttu-id="cc14d-577">127.0.0.1</span><span class="sxs-lookup"><span data-stu-id="cc14d-577">127.0.0.1</span></span>
- <span data-ttu-id="cc14d-578">testacs. <!--no-hyperlink-->com</span><span class="sxs-lookup"><span data-stu-id="cc14d-578">testacs.<!--no-hyperlink-->com</span></span>
- <span data-ttu-id="cc14d-579">s-int.<!--no-hyperlink-->net</span><span class="sxs-lookup"><span data-stu-id="cc14d-579">s-int.<!--no-hyperlink-->net</span></span>

## <a name="azure-redis-cache-connection-string"></a><span data-ttu-id="cc14d-580">Cadeia de conexão do cache do Redis do Azure</span><span class="sxs-lookup"><span data-stu-id="cc14d-580">Azure Redis Cache Connection String</span></span>

### <a name="format"></a><span data-ttu-id="cc14d-581">Format</span><span class="sxs-lookup"><span data-stu-id="cc14d-581">Format</span></span>

<span data-ttu-id="cc14d-582">A cadeia de caracteres "Redis. cache. Windows. <!--no-hyperlink-->net "seguido pelos caracteres e cadeias de caracteres descritos no padrão abaixo, incluindo a cadeia de caracteres" password "ou" pwd ".</span><span class="sxs-lookup"><span data-stu-id="cc14d-582">The string "redis.cache.windows.<!--no-hyperlink-->net" followed by the characters and strings outlined in the pattern below, including the string "password" or "pwd".</span></span>

### <a name="pattern"></a><span data-ttu-id="cc14d-583">Padrão</span><span class="sxs-lookup"><span data-stu-id="cc14d-583">Pattern</span></span>

- <span data-ttu-id="cc14d-584">A cadeia de caracteres "Redis. cache. Windows. <!--no-hyperlink-->net "</span><span class="sxs-lookup"><span data-stu-id="cc14d-584">The string "redis.cache.windows.<!--no-hyperlink-->net"</span></span>
- <span data-ttu-id="cc14d-585">Qualquer combinação entre 1-200 letras minúsculas ou maiúsculas, dígitos, símbolos, caracteres especiais ou espaços</span><span class="sxs-lookup"><span data-stu-id="cc14d-585">Any combination of between 1-200 lower- or uppercase letters, digits, symbols, special characters, or spaces</span></span>
- <span data-ttu-id="cc14d-586">A cadeia de caracteres "password" ou "pwd"</span><span class="sxs-lookup"><span data-stu-id="cc14d-586">The string "password" or "pwd"</span></span>
- <span data-ttu-id="cc14d-587">0-2 caracteres de espaço em branco</span><span class="sxs-lookup"><span data-stu-id="cc14d-587">0-2 whitespace characters</span></span>
- <span data-ttu-id="cc14d-588">Um sinal de igual (=)</span><span class="sxs-lookup"><span data-stu-id="cc14d-588">An equal sign (=)</span></span>
- <span data-ttu-id="cc14d-589">0-2 caracteres de espaço em branco</span><span class="sxs-lookup"><span data-stu-id="cc14d-589">0-2 whitespace characters</span></span>
- <span data-ttu-id="cc14d-590">Qualquer combinação de 43 caracteres que sejam letras minúsculas ou maiúsculas, dígitos, barra de avanço (/) ou sinal de adição (+)</span><span class="sxs-lookup"><span data-stu-id="cc14d-590">Any combination of 43 characters that are lower- or uppercase letters, digits, forward slash (/), or plus sign (+)</span></span>
- <span data-ttu-id="cc14d-591">Um sinal de igual (=)</span><span class="sxs-lookup"><span data-stu-id="cc14d-591">An equal sign (=)</span></span>

### <a name="checksum"></a><span data-ttu-id="cc14d-592">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="cc14d-592">Checksum</span></span>

<span data-ttu-id="cc14d-593">Não</span><span class="sxs-lookup"><span data-stu-id="cc14d-593">No</span></span>

### <a name="definition"></a><span data-ttu-id="cc14d-594">Definição</span><span class="sxs-lookup"><span data-stu-id="cc14d-594">Definition</span></span>

<span data-ttu-id="cc14d-595">Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="cc14d-595">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="cc14d-596">A expressão regular CEP_Regex_AzureRedisCacheConnectionString localiza o conteúdo que corresponde ao padrão..</span><span class="sxs-lookup"><span data-stu-id="cc14d-596">The regular expression CEP_Regex_AzureRedisCacheConnectionString finds content that matches the pattern..</span></span>
- <span data-ttu-id="cc14d-597">A expressão regular CEP_CommonExampleKeywords não \*\*\*\* localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="cc14d-597">The regular expression CEP_CommonExampleKeywords does **not** find content that matches the pattern.</span></span>

```
<!--Azure Redis Cache Connection String-->
<Entity id="095a7e6c-efd8-46d5-af7b-5298d53a49fc" patternsProximity="300" recommendedConfidence="85">
  <Pattern confidenceLevel="85">
        <IdMatch idRef="CEP_Regex_AzureRedisCacheConnectionString" />
        <Any minMatches="0" maxMatches="0">
            <Match idRef="CEP_CommonExampleKeywords" />
        </Any>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="cc14d-598">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="cc14d-598">Keywords</span></span>

#### <a name="cepcommonexamplekeywords"></a><span data-ttu-id="cc14d-599">CEP_CommonExampleKeywords</span><span class="sxs-lookup"><span data-stu-id="cc14d-599">CEP_CommonExampleKeywords</span></span>

<span data-ttu-id="cc14d-600">(Observe que tecnicamente, esse tipo de informação confidencial identifica essas palavras-chave usando uma expressão regular, não uma lista de palavras-chave.)</span><span class="sxs-lookup"><span data-stu-id="cc14d-600">(Note that technically, this sensitive information type identifies these keywords by using a regular expression, not a keyword list.)</span></span>

- <span data-ttu-id="cc14d-601">contoso</span><span class="sxs-lookup"><span data-stu-id="cc14d-601">contoso</span></span>
- <span data-ttu-id="cc14d-602">fabrikam</span><span class="sxs-lookup"><span data-stu-id="cc14d-602">fabrikam</span></span>
- <span data-ttu-id="cc14d-603">Northwind</span><span class="sxs-lookup"><span data-stu-id="cc14d-603">northwind</span></span>
- <span data-ttu-id="cc14d-604">área restrita</span><span class="sxs-lookup"><span data-stu-id="cc14d-604">sandbox</span></span>
- <span data-ttu-id="cc14d-605">Onebox</span><span class="sxs-lookup"><span data-stu-id="cc14d-605">onebox</span></span>
- <span data-ttu-id="cc14d-606">localhost</span><span class="sxs-lookup"><span data-stu-id="cc14d-606">localhost</span></span>
- <span data-ttu-id="cc14d-607">127.0.0.1</span><span class="sxs-lookup"><span data-stu-id="cc14d-607">127.0.0.1</span></span>
- <span data-ttu-id="cc14d-608">testacs. <!--no-hyperlink-->com</span><span class="sxs-lookup"><span data-stu-id="cc14d-608">testacs.<!--no-hyperlink-->com</span></span>
- <span data-ttu-id="cc14d-609">s-int.<!--no-hyperlink-->net</span><span class="sxs-lookup"><span data-stu-id="cc14d-609">s-int.<!--no-hyperlink-->net</span></span>

## <a name="azure-sas"></a><span data-ttu-id="cc14d-610">SAS do Azure</span><span class="sxs-lookup"><span data-stu-id="cc14d-610">Azure SAS</span></span>

### <a name="format"></a><span data-ttu-id="cc14d-611">Format</span><span class="sxs-lookup"><span data-stu-id="cc14d-611">Format</span></span>

<span data-ttu-id="cc14d-612">A cadeia de caracteres "SIG" seguida pelos caracteres e cadeias de caracteres descritos no padrão abaixo.</span><span class="sxs-lookup"><span data-stu-id="cc14d-612">The string "sig" followed by the characters and strings outlined in the pattern below.</span></span>

### <a name="pattern"></a><span data-ttu-id="cc14d-613">Padrão</span><span class="sxs-lookup"><span data-stu-id="cc14d-613">Pattern</span></span>

- <span data-ttu-id="cc14d-614">A cadeia de caracteres "SIG"</span><span class="sxs-lookup"><span data-stu-id="cc14d-614">The string "sig"</span></span>
- <span data-ttu-id="cc14d-615">0-2 caracteres de espaço em branco</span><span class="sxs-lookup"><span data-stu-id="cc14d-615">0-2 whitespace characters</span></span>
- <span data-ttu-id="cc14d-616">Um sinal de igual (=)</span><span class="sxs-lookup"><span data-stu-id="cc14d-616">An equal sign (=)</span></span>
- <span data-ttu-id="cc14d-617">0-2 caracteres de espaço em branco</span><span class="sxs-lookup"><span data-stu-id="cc14d-617">0-2 whitespace characters</span></span>
- <span data-ttu-id="cc14d-618">Qualquer combinação entre 43-53 caracteres que são letras minúsculas ou maiúsculas, dígitos ou o sinal de porcentagem (%)</span><span class="sxs-lookup"><span data-stu-id="cc14d-618">Any combination of between 43-53 characters that are lower- or uppercase letters, digits, or the percent sign (%)</span></span>
- <span data-ttu-id="cc14d-619">A cadeia de caracteres "% 3D"</span><span class="sxs-lookup"><span data-stu-id="cc14d-619">The string "%3d"</span></span>
- <span data-ttu-id="cc14d-620">Qualquer caractere que não seja letras minúsculas, dígitos ou sinal de porcentagem (%)</span><span class="sxs-lookup"><span data-stu-id="cc14d-620">Any character that is not a lower- or uppercase letter, digit, or percent sign (%)</span></span>

### <a name="checksum"></a><span data-ttu-id="cc14d-621">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="cc14d-621">Checksum</span></span>

<span data-ttu-id="cc14d-622">Não</span><span class="sxs-lookup"><span data-stu-id="cc14d-622">No</span></span>

### <a name="definition"></a><span data-ttu-id="cc14d-623">Definição</span><span class="sxs-lookup"><span data-stu-id="cc14d-623">Definition</span></span>

<span data-ttu-id="cc14d-624">Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="cc14d-624">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="cc14d-625">A expressão regular CEP_Regex_AzureSAS localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="cc14d-625">The regular expression CEP_Regex_AzureSAS finds content that matches the pattern.</span></span>

```
<!--Azure SAS-->
<Entity id="4d235014-e564-47f4-a6fb-6ebb4a826834" patternsProximity="300" recommendedConfidence="85">
  <Pattern confidenceLevel="85">
        <IdMatch idRef="CEP_Regex_AzureSAS" />
  </Pattern>
</Entity>
```

## <a name="azure-service-bus-connection-string"></a><span data-ttu-id="cc14d-626">Cadeia de conexão do barramento de serviço do Azure</span><span class="sxs-lookup"><span data-stu-id="cc14d-626">Azure Service Bus Connection String</span></span>

### <a name="format"></a><span data-ttu-id="cc14d-627">Format</span><span class="sxs-lookup"><span data-stu-id="cc14d-627">Format</span></span>

<span data-ttu-id="cc14d-628">A cadeia de caracteres "EndPoint" seguida dos caracteres e cadeias de caracteres descritos no padrão abaixo, incluindo as cadeias de caracteres "ServiceBus. Windows. <!--no-hyperlink-->net "e" SharedAccesKey ".</span><span class="sxs-lookup"><span data-stu-id="cc14d-628">The string "EndPoint" followed by the characters and strings outlined in the pattern below, including the strings "servicebus.windows.<!--no-hyperlink-->net" and "SharedAccesKey".</span></span>

### <a name="pattern"></a><span data-ttu-id="cc14d-629">Padrão</span><span class="sxs-lookup"><span data-stu-id="cc14d-629">Pattern</span></span>

- <span data-ttu-id="cc14d-630">A cadeia de caracteres "EndPoint"</span><span class="sxs-lookup"><span data-stu-id="cc14d-630">The string "EndPoint"</span></span>
- <span data-ttu-id="cc14d-631">0-2 caracteres de espaço em branco</span><span class="sxs-lookup"><span data-stu-id="cc14d-631">0-2 whitespace characters</span></span>
- <span data-ttu-id="cc14d-632">Um sinal de igual (=)</span><span class="sxs-lookup"><span data-stu-id="cc14d-632">An equal sign (=)</span></span>
- <span data-ttu-id="cc14d-633">0-2 caracteres de espaço em branco</span><span class="sxs-lookup"><span data-stu-id="cc14d-633">0-2 whitespace characters</span></span>
- <span data-ttu-id="cc14d-634">Qualquer combinação entre 1-200 letras minúsculas ou maiúsculas, dígitos, símbolos, caracteres especiais ou espaços</span><span class="sxs-lookup"><span data-stu-id="cc14d-634">Any combination of between 1-200 lower- or uppercase letters, digits, symbols, special characters, or spaces</span></span>
- <span data-ttu-id="cc14d-635">A cadeia de caracteres "ServiceBus. Windows. <!--no-hyperlink-->net "</span><span class="sxs-lookup"><span data-stu-id="cc14d-635">The string "servicebus.windows.<!--no-hyperlink-->net"</span></span>
- <span data-ttu-id="cc14d-636">Qualquer combinação entre 1-200 letras minúsculas ou maiúsculas, dígitos, símbolos, caracteres especiais ou espaços</span><span class="sxs-lookup"><span data-stu-id="cc14d-636">Any combination of between 1-200 lower- or uppercase letters, digits, symbols, special characters, or spaces</span></span>
- <span data-ttu-id="cc14d-637">A cadeia de caracteres "SharedAccessKey"</span><span class="sxs-lookup"><span data-stu-id="cc14d-637">The string "SharedAccessKey"</span></span>
- <span data-ttu-id="cc14d-638">0-2 caracteres de espaço em branco</span><span class="sxs-lookup"><span data-stu-id="cc14d-638">0-2 whitespace characters</span></span>
- <span data-ttu-id="cc14d-639">Um sinal de igual (=)</span><span class="sxs-lookup"><span data-stu-id="cc14d-639">An equal sign (=)</span></span>
- <span data-ttu-id="cc14d-640">0-2 caracteres de espaço em branco</span><span class="sxs-lookup"><span data-stu-id="cc14d-640">0-2 whitespace characters</span></span>
- <span data-ttu-id="cc14d-641">Qualquer combinação de 43 caracteres que sejam letras minúsculas ou maiúsculas, dígitos, barra de avanço (/) ou sinal de adição (+)</span><span class="sxs-lookup"><span data-stu-id="cc14d-641">Any combination of 43 characters that are lower- or uppercase letters, digits, forward slash (/), or plus sign (+)</span></span>
- <span data-ttu-id="cc14d-642">Um sinal de igual (=)</span><span class="sxs-lookup"><span data-stu-id="cc14d-642">An equal sign (=)</span></span>

### <a name="checksum"></a><span data-ttu-id="cc14d-643">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="cc14d-643">Checksum</span></span>

<span data-ttu-id="cc14d-644">Não</span><span class="sxs-lookup"><span data-stu-id="cc14d-644">No</span></span>

### <a name="definition"></a><span data-ttu-id="cc14d-645">Definição</span><span class="sxs-lookup"><span data-stu-id="cc14d-645">Definition</span></span>

<span data-ttu-id="cc14d-646">Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="cc14d-646">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="cc14d-647">A expressão regular CEP_Regex_AzureServiceBusConnectionString localiza o conteúdo que corresponde ao padrão..</span><span class="sxs-lookup"><span data-stu-id="cc14d-647">The regular expression CEP_Regex_AzureServiceBusConnectionString finds content that matches the pattern..</span></span>
- <span data-ttu-id="cc14d-648">A expressão regular CEP_CommonExampleKeywords não \*\*\*\* localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="cc14d-648">The regular expression CEP_CommonExampleKeywords does **not** find content that matches the pattern.</span></span>

```
<!--Azure Service Bus Connection String-->
<Entity id="b9a6578f-a83f-4fcd-bf44-2130bae49a6f" patternsProximity="300" recommendedConfidence="85">
  <Pattern confidenceLevel="85">
        <IdMatch idRef="CEP_Regex_AzureServiceBusConnectionString" />
        <Any minMatches="0" maxMatches="0">
            <Match idRef="CEP_CommonExampleKeywords" />
        </Any>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="cc14d-649">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="cc14d-649">Keywords</span></span>

#### <a name="cepcommonexamplekeywords"></a><span data-ttu-id="cc14d-650">CEP_CommonExampleKeywords</span><span class="sxs-lookup"><span data-stu-id="cc14d-650">CEP_CommonExampleKeywords</span></span>

<span data-ttu-id="cc14d-651">(Observe que tecnicamente, esse tipo de informação confidencial identifica essas palavras-chave usando uma expressão regular, não uma lista de palavras-chave.)</span><span class="sxs-lookup"><span data-stu-id="cc14d-651">(Note that technically, this sensitive information type identifies these keywords by using a regular expression, not a keyword list.)</span></span>

- <span data-ttu-id="cc14d-652">contoso</span><span class="sxs-lookup"><span data-stu-id="cc14d-652">contoso</span></span>
- <span data-ttu-id="cc14d-653">fabrikam</span><span class="sxs-lookup"><span data-stu-id="cc14d-653">fabrikam</span></span>
- <span data-ttu-id="cc14d-654">Northwind</span><span class="sxs-lookup"><span data-stu-id="cc14d-654">northwind</span></span>
- <span data-ttu-id="cc14d-655">área restrita</span><span class="sxs-lookup"><span data-stu-id="cc14d-655">sandbox</span></span>
- <span data-ttu-id="cc14d-656">Onebox</span><span class="sxs-lookup"><span data-stu-id="cc14d-656">onebox</span></span>
- <span data-ttu-id="cc14d-657">localhost</span><span class="sxs-lookup"><span data-stu-id="cc14d-657">localhost</span></span>
- <span data-ttu-id="cc14d-658">127.0.0.1</span><span class="sxs-lookup"><span data-stu-id="cc14d-658">127.0.0.1</span></span>
- <span data-ttu-id="cc14d-659">testacs. <!--no-hyperlink-->com</span><span class="sxs-lookup"><span data-stu-id="cc14d-659">testacs.<!--no-hyperlink-->com</span></span>
- <span data-ttu-id="cc14d-660">s-int.<!--no-hyperlink-->net</span><span class="sxs-lookup"><span data-stu-id="cc14d-660">s-int.<!--no-hyperlink-->net</span></span>

## <a name="azure-storage-account-key"></a><span data-ttu-id="cc14d-661">Chave da conta de armazenamento do Azure</span><span class="sxs-lookup"><span data-stu-id="cc14d-661">Azure Storage Account Key</span></span>

### <a name="format"></a><span data-ttu-id="cc14d-662">Format</span><span class="sxs-lookup"><span data-stu-id="cc14d-662">Format</span></span>

<span data-ttu-id="cc14d-663">A cadeia de caracteres "DefaultEndpointsProtocol" seguida dos caracteres e cadeias de caracteres descritos no padrão abaixo, incluindo a cadeia de caracteres "AccountKey".</span><span class="sxs-lookup"><span data-stu-id="cc14d-663">The string "DefaultEndpointsProtocol" followed by the characters and strings outlined in the pattern below, including the string "AccountKey".</span></span>

### <a name="pattern"></a><span data-ttu-id="cc14d-664">Padrão</span><span class="sxs-lookup"><span data-stu-id="cc14d-664">Pattern</span></span>

- <span data-ttu-id="cc14d-665">A cadeia de caracteres "DefaultEndpointsProtocol"</span><span class="sxs-lookup"><span data-stu-id="cc14d-665">The string "DefaultEndpointsProtocol"</span></span>
- <span data-ttu-id="cc14d-666">0-2 caracteres de espaço em branco</span><span class="sxs-lookup"><span data-stu-id="cc14d-666">0-2 whitespace characters</span></span>
- <span data-ttu-id="cc14d-667">Um sinal de igual (=)</span><span class="sxs-lookup"><span data-stu-id="cc14d-667">An equal sign (=)</span></span>
- <span data-ttu-id="cc14d-668">0-2 caracteres de espaço em branco</span><span class="sxs-lookup"><span data-stu-id="cc14d-668">0-2 whitespace characters</span></span>
- <span data-ttu-id="cc14d-669">Qualquer combinação entre 1-200 letras minúsculas ou maiúsculas, dígitos, símbolos, caracteres especiais ou espaços</span><span class="sxs-lookup"><span data-stu-id="cc14d-669">Any combination of between 1-200 lower- or uppercase letters, digits, symbols, special characters, or spaces</span></span>
- <span data-ttu-id="cc14d-670">A cadeia de caracteres "AccountKey"</span><span class="sxs-lookup"><span data-stu-id="cc14d-670">The string "AccountKey"</span></span>
- <span data-ttu-id="cc14d-671">0-2 caracteres de espaço em branco</span><span class="sxs-lookup"><span data-stu-id="cc14d-671">0-2 whitespace characters</span></span>
- <span data-ttu-id="cc14d-672">Um sinal de igual (=)</span><span class="sxs-lookup"><span data-stu-id="cc14d-672">An equal sign (=)</span></span>
- <span data-ttu-id="cc14d-673">0-2 caracteres de espaço em branco</span><span class="sxs-lookup"><span data-stu-id="cc14d-673">0-2 whitespace characters</span></span>
- <span data-ttu-id="cc14d-674">Qualquer combinação de 86 caracteres que sejam letras minúsculas ou maiúsculas, dígitos, barra de avanço (/) ou sinal de adição (+)</span><span class="sxs-lookup"><span data-stu-id="cc14d-674">Any combination of 86 characters that are lower- or uppercase letters, digits, forward slash (/), or plus sign (+)</span></span>
- <span data-ttu-id="cc14d-675">Dois sinais de igual (=)</span><span class="sxs-lookup"><span data-stu-id="cc14d-675">Two equal signs (=)</span></span>

### <a name="checksum"></a><span data-ttu-id="cc14d-676">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="cc14d-676">Checksum</span></span>

<span data-ttu-id="cc14d-677">Não</span><span class="sxs-lookup"><span data-stu-id="cc14d-677">No</span></span>

### <a name="definition"></a><span data-ttu-id="cc14d-678">Definição</span><span class="sxs-lookup"><span data-stu-id="cc14d-678">Definition</span></span>

<span data-ttu-id="cc14d-679">Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="cc14d-679">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="cc14d-680">A expressão regular CEP_Regex_AzureStorageAccountKey localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="cc14d-680">The regular expression CEP_Regex_AzureStorageAccountKey finds content that matches the pattern.</span></span>
- <span data-ttu-id="cc14d-681">A expressão regular CEP_AzureEmulatorStorageAccountFilter não \*\*\*\* localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="cc14d-681">The regular expression CEP_AzureEmulatorStorageAccountFilter does **not** find content that matches the pattern.</span></span>
- <span data-ttu-id="cc14d-682">A expressão regular CEP_CommonExampleKeywords não \*\*\*\* localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="cc14d-682">The regular expression CEP_CommonExampleKeywords does **not** find content that matches the pattern.</span></span>

```
<!--Azure Storage Account Key-->
<Entity id="c7bc98e8-551a-4c35-a92d-d2c8cda714a7" patternsProximity="300" recommendedConfidence="85">
  <Pattern confidenceLevel="85">
        <IdMatch idRef="CEP_Regex_AzureStorageAccountKey" />
        <Any minMatches="0" maxMatches="0">
            <Match idRef="CEP_AzureEmulatorStorageAccountFilter" />
            <Match idRef="CEP_CommonExampleKeywords" />
        </Any>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="cc14d-683">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="cc14d-683">Keywords</span></span>

#### <a name="cepazureemulatorstorageaccountfilter"></a><span data-ttu-id="cc14d-684">CEP_AzureEmulatorStorageAccountFilter</span><span class="sxs-lookup"><span data-stu-id="cc14d-684">CEP_AzureEmulatorStorageAccountFilter</span></span>

<span data-ttu-id="cc14d-685">(Observe que tecnicamente, esse tipo de informação confidencial identifica essas palavras-chave usando uma expressão regular, não uma lista de palavras-chave.)</span><span class="sxs-lookup"><span data-stu-id="cc14d-685">(Note that technically, this sensitive information type identifies these keywords by using a regular expression, not a keyword list.)</span></span>

- <span data-ttu-id="cc14d-686">Eby8vdM02xNOcqFlqUwJPLlmEtlCDXJ1OUzFT50uSRZ6IFsuFq2UVErCz4I6tq/K1SZFPTOtr/KBHBeksoGMGw = =</span><span class="sxs-lookup"><span data-stu-id="cc14d-686">Eby8vdM02xNOcqFlqUwJPLlmEtlCDXJ1OUzFT50uSRZ6IFsuFq2UVErCz4I6tq/K1SZFPTOtr/KBHBeksoGMGw==</span></span>

#### <a name="cepcommonexamplekeywords"></a><span data-ttu-id="cc14d-687">CEP_CommonExampleKeywords</span><span class="sxs-lookup"><span data-stu-id="cc14d-687">CEP_CommonExampleKeywords</span></span>

<span data-ttu-id="cc14d-688">(Observe que tecnicamente, esse tipo de informação confidencial identifica essas palavras-chave usando uma expressão regular, não uma lista de palavras-chave.)</span><span class="sxs-lookup"><span data-stu-id="cc14d-688">(Note that technically, this sensitive information type identifies these keywords by using a regular expression, not a keyword list.)</span></span>

- <span data-ttu-id="cc14d-689">contoso</span><span class="sxs-lookup"><span data-stu-id="cc14d-689">contoso</span></span>
- <span data-ttu-id="cc14d-690">fabrikam</span><span class="sxs-lookup"><span data-stu-id="cc14d-690">fabrikam</span></span>
- <span data-ttu-id="cc14d-691">Northwind</span><span class="sxs-lookup"><span data-stu-id="cc14d-691">northwind</span></span>
- <span data-ttu-id="cc14d-692">área restrita</span><span class="sxs-lookup"><span data-stu-id="cc14d-692">sandbox</span></span>
- <span data-ttu-id="cc14d-693">Onebox</span><span class="sxs-lookup"><span data-stu-id="cc14d-693">onebox</span></span>
- <span data-ttu-id="cc14d-694">localhost</span><span class="sxs-lookup"><span data-stu-id="cc14d-694">localhost</span></span>
- <span data-ttu-id="cc14d-695">127.0.0.1</span><span class="sxs-lookup"><span data-stu-id="cc14d-695">127.0.0.1</span></span>
- <span data-ttu-id="cc14d-696">testacs. <!--no-hyperlink-->com</span><span class="sxs-lookup"><span data-stu-id="cc14d-696">testacs.<!--no-hyperlink-->com</span></span>
- <span data-ttu-id="cc14d-697">s-int.<!--no-hyperlink-->net</span><span class="sxs-lookup"><span data-stu-id="cc14d-697">s-int.<!--no-hyperlink-->net</span></span>

## <a name="azure-storage-account-key-generic"></a><span data-ttu-id="cc14d-698">Chave da conta de armazenamento do Azure (genérico)</span><span class="sxs-lookup"><span data-stu-id="cc14d-698">Azure Storage Account Key (Generic)</span></span>

### <a name="format"></a><span data-ttu-id="cc14d-699">Format</span><span class="sxs-lookup"><span data-stu-id="cc14d-699">Format</span></span>

<span data-ttu-id="cc14d-700">Qualquer combinação de letras maiúsculas ou minúsculas de 86, dígitos, barra (/) ou sinal de adição (+), precedida ou seguida dos caracteres descritos no padrão abaixo.</span><span class="sxs-lookup"><span data-stu-id="cc14d-700">Any combination of 86 lower- or uppercase letters, digits, the forward slash (/), or plus sign (+), preceded or followed by the characters outlined in the pattern below.</span></span>

### <a name="pattern"></a><span data-ttu-id="cc14d-701">Padrão</span><span class="sxs-lookup"><span data-stu-id="cc14d-701">Pattern</span></span>

- <span data-ttu-id="cc14d-702">0-1 do símbolo maior que (>), apóstrofo ('), sinal de igual (=), aspas (") ou sinal de número (#)</span><span class="sxs-lookup"><span data-stu-id="cc14d-702">0-1 of the greater than symbol (>), apostrophe ('), equal sign (=), quotation mark ("), or number sign (#)</span></span>
- <span data-ttu-id="cc14d-703">Qualquer combinação de 86 caracteres que sejam letras minúsculas ou maiúsculas, dígitos, a barra (/) ou sinal de adição (+)</span><span class="sxs-lookup"><span data-stu-id="cc14d-703">Any combination of 86 characters that are lower- or uppercase letters, digits, the forward slash (/), or plus sign (+)</span></span>
- <span data-ttu-id="cc14d-704">Dois sinais de igual (=)</span><span class="sxs-lookup"><span data-stu-id="cc14d-704">Two equal signs (=)</span></span>


### <a name="checksum"></a><span data-ttu-id="cc14d-705">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="cc14d-705">Checksum</span></span>

<span data-ttu-id="cc14d-706">Não</span><span class="sxs-lookup"><span data-stu-id="cc14d-706">No</span></span>

### <a name="definition"></a><span data-ttu-id="cc14d-707">Definição</span><span class="sxs-lookup"><span data-stu-id="cc14d-707">Definition</span></span>

<span data-ttu-id="cc14d-708">Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="cc14d-708">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="cc14d-709">A expressão regular CEP_Regex_AzureStorageAccountKeyGeneric localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="cc14d-709">The regular expression CEP_Regex_AzureStorageAccountKeyGeneric finds content that matches the pattern.</span></span>

```
<!--Azure Storage Account Key (Generic)-->
<Entity id="7ff41bd0-5419-4523-91d6-383b3a37f084" patternsProximity="300" recommendedConfidence="85">
  <Pattern confidenceLevel="85">
        <IdMatch idRef="CEP_Regex_AzureStorageAccountKeyGeneric" />
  </Pattern>
</Entity>
```

## <a name="belgium-national-number"></a><span data-ttu-id="cc14d-710">Número Nacional da Bélgica</span><span class="sxs-lookup"><span data-stu-id="cc14d-710">Belgium National Number</span></span>

### <a name="format"></a><span data-ttu-id="cc14d-711">Format</span><span class="sxs-lookup"><span data-stu-id="cc14d-711">Format</span></span>

<span data-ttu-id="cc14d-712">11 dígitos mais delimitadores</span><span class="sxs-lookup"><span data-stu-id="cc14d-712">11 digits plus delimiters</span></span>

### <a name="pattern"></a><span data-ttu-id="cc14d-713">Padrão</span><span class="sxs-lookup"><span data-stu-id="cc14d-713">Pattern</span></span>

<span data-ttu-id="cc14d-714">11 dígitos mais delimitadores.</span><span class="sxs-lookup"><span data-stu-id="cc14d-714">11 digits plus delimiters:</span></span>
- <span data-ttu-id="cc14d-715">Seis dígitos e dois pontos no formato AA.MM.DD da data de nascimento </span><span class="sxs-lookup"><span data-stu-id="cc14d-715">Six digits and two periods in the format YY.MM.DD for date of birth</span></span> 
- <span data-ttu-id="cc14d-716">Um hífen</span><span class="sxs-lookup"><span data-stu-id="cc14d-716">A hyphen</span></span> 
- <span data-ttu-id="cc14d-717">Três dígitos sequenciais (ímpares para homens, pares para mulheres) </span><span class="sxs-lookup"><span data-stu-id="cc14d-717">Three sequential digits (odd for males, even for females)</span></span> 
- <span data-ttu-id="cc14d-718">Um ponto</span><span class="sxs-lookup"><span data-stu-id="cc14d-718">A period</span></span> 
- <span data-ttu-id="cc14d-719">Dois dígitos que são um dígito de verificação</span><span class="sxs-lookup"><span data-stu-id="cc14d-719">Two digits that are a check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="cc14d-720">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="cc14d-720">Checksum</span></span>

<span data-ttu-id="cc14d-721">Sim</span><span class="sxs-lookup"><span data-stu-id="cc14d-721">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="cc14d-722">Definição</span><span class="sxs-lookup"><span data-stu-id="cc14d-722">Definition</span></span>

<span data-ttu-id="cc14d-723">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="cc14d-723">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="cc14d-724">A função Func_belgium_national_number localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="cc14d-724">The function Func_belgium_national_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="cc14d-725">Uma palavra-chave de Keyword_belgium_national_number for encontrada.</span><span class="sxs-lookup"><span data-stu-id="cc14d-725">A keyword from Keyword_belgium_national_number is found.</span></span>
- <span data-ttu-id="cc14d-726">A soma de verificação passa.</span><span class="sxs-lookup"><span data-stu-id="cc14d-726">The checksum passes.</span></span>

```
<!-- Belgium National Number -->
  <Entity id="fb969c9e-0fd1-4b18-8091-a2123c5e6a54" recommendedConfidence="75" patternsProximity="300">
   <Pattern confidenceLevel="75">
     <IdMatch idRef="Func_belgium_national_number"/>
     <Match idRef="Keyword_belgium_national_number"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="cc14d-727">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="cc14d-727">Keywords</span></span>

#### <a name="keywordbelgiumnationalnumber"></a><span data-ttu-id="cc14d-728">Keyword_belgium_national_number</span><span class="sxs-lookup"><span data-stu-id="cc14d-728">Keyword_belgium_national_number</span></span>

- <span data-ttu-id="cc14d-729">Identidade</span><span class="sxs-lookup"><span data-stu-id="cc14d-729">Identity</span></span>
- <span data-ttu-id="cc14d-730">Registro</span><span class="sxs-lookup"><span data-stu-id="cc14d-730">Registration</span></span>
- <span data-ttu-id="cc14d-731">Identificador</span><span class="sxs-lookup"><span data-stu-id="cc14d-731">Identification</span></span> 
- <span data-ttu-id="cc14d-732">ID</span><span class="sxs-lookup"><span data-stu-id="cc14d-732">ID</span></span> 
- <span data-ttu-id="cc14d-733">Identiteitskaart</span><span class="sxs-lookup"><span data-stu-id="cc14d-733">Identiteitskaart</span></span>
- <span data-ttu-id="cc14d-734">Registratie nummer</span><span class="sxs-lookup"><span data-stu-id="cc14d-734">Registratie nummer</span></span> 
- <span data-ttu-id="cc14d-735">Identificatie nummer</span><span class="sxs-lookup"><span data-stu-id="cc14d-735">Identificatie nummer</span></span> 
- <span data-ttu-id="cc14d-736">Identiteit</span><span class="sxs-lookup"><span data-stu-id="cc14d-736">Identiteit</span></span>
- <span data-ttu-id="cc14d-737">Registratie</span><span class="sxs-lookup"><span data-stu-id="cc14d-737">Registratie</span></span>
- <span data-ttu-id="cc14d-738">Identificatie</span><span class="sxs-lookup"><span data-stu-id="cc14d-738">Identificatie</span></span> 
- <span data-ttu-id="cc14d-739">Carte d’identité</span><span class="sxs-lookup"><span data-stu-id="cc14d-739">Carte d’identité</span></span> 
- <span data-ttu-id="cc14d-740">numéro d'immatriculation</span><span class="sxs-lookup"><span data-stu-id="cc14d-740">numéro d'immatriculation</span></span>
- <span data-ttu-id="cc14d-741">numéro d'identification</span><span class="sxs-lookup"><span data-stu-id="cc14d-741">numéro d'identification</span></span>
- <span data-ttu-id="cc14d-742">identité</span><span class="sxs-lookup"><span data-stu-id="cc14d-742">identité</span></span> 
- <span data-ttu-id="cc14d-743">inscription</span><span class="sxs-lookup"><span data-stu-id="cc14d-743">inscription</span></span> 
- <span data-ttu-id="cc14d-744">Identifikation</span><span class="sxs-lookup"><span data-stu-id="cc14d-744">Identifikation</span></span>
- <span data-ttu-id="cc14d-745">Identifizierung</span><span class="sxs-lookup"><span data-stu-id="cc14d-745">Identifizierung</span></span>
- <span data-ttu-id="cc14d-746">Identifikationsnummer</span><span class="sxs-lookup"><span data-stu-id="cc14d-746">Identifikationsnummer</span></span>
- <span data-ttu-id="cc14d-747">Personalausweis</span><span class="sxs-lookup"><span data-stu-id="cc14d-747">Personalausweis</span></span>
- <span data-ttu-id="cc14d-748">Registrierung</span><span class="sxs-lookup"><span data-stu-id="cc14d-748">Registrierung</span></span>
- <span data-ttu-id="cc14d-749">Registrationsnummer</span><span class="sxs-lookup"><span data-stu-id="cc14d-749">Registrationsnummer</span></span>

   
## <a name="brazil-cpf-number"></a><span data-ttu-id="cc14d-750">Número de CPF do Brasil</span><span class="sxs-lookup"><span data-stu-id="cc14d-750">Brazil CPF Number</span></span>

### <a name="format"></a><span data-ttu-id="cc14d-751">Format</span><span class="sxs-lookup"><span data-stu-id="cc14d-751">Format</span></span>

<span data-ttu-id="cc14d-752">11 dígitos que incluem um dígito de verificação e podem ser formatados ou não formatados</span><span class="sxs-lookup"><span data-stu-id="cc14d-752">11 digits that include a check digit and can be formatted or unformatted</span></span>

### <a name="pattern"></a><span data-ttu-id="cc14d-753">Padrão</span><span class="sxs-lookup"><span data-stu-id="cc14d-753">Pattern</span></span>

<span data-ttu-id="cc14d-754">Binário</span><span class="sxs-lookup"><span data-stu-id="cc14d-754">Formatted:</span></span>
- <span data-ttu-id="cc14d-755">Três dígitos</span><span class="sxs-lookup"><span data-stu-id="cc14d-755">Three digits</span></span> 
- <span data-ttu-id="cc14d-756">Um ponto </span><span class="sxs-lookup"><span data-stu-id="cc14d-756">A period</span></span> 
- <span data-ttu-id="cc14d-757">Três dígitos</span><span class="sxs-lookup"><span data-stu-id="cc14d-757">Three digits</span></span> 
- <span data-ttu-id="cc14d-758">Um ponto </span><span class="sxs-lookup"><span data-stu-id="cc14d-758">A period</span></span> 
- <span data-ttu-id="cc14d-759">Três dígitos</span><span class="sxs-lookup"><span data-stu-id="cc14d-759">Three digits</span></span> 
- <span data-ttu-id="cc14d-760">Um hífen</span><span class="sxs-lookup"><span data-stu-id="cc14d-760">A hyphen</span></span> 
- <span data-ttu-id="cc14d-761">Dois dígitos que são dígitos de verificação</span><span class="sxs-lookup"><span data-stu-id="cc14d-761">Two digits which are check digits</span></span>

<span data-ttu-id="cc14d-762">Não formatado</span><span class="sxs-lookup"><span data-stu-id="cc14d-762">Unformatted:</span></span>
- <span data-ttu-id="cc14d-763">11 dígitos em que os dois últimos dígitos são dígitos de verificação</span><span class="sxs-lookup"><span data-stu-id="cc14d-763">11 digits where the last two digits are check digits</span></span>

### <a name="checksum"></a><span data-ttu-id="cc14d-764">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="cc14d-764">Checksum</span></span>

<span data-ttu-id="cc14d-765">Sim</span><span class="sxs-lookup"><span data-stu-id="cc14d-765">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="cc14d-766">Definição</span><span class="sxs-lookup"><span data-stu-id="cc14d-766">Definition</span></span>

<span data-ttu-id="cc14d-767">Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="cc14d-767">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="cc14d-768">A função Func_brazil_cpf localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="cc14d-768">The function Func_brazil_cpf finds content that matches the pattern.</span></span>
- <span data-ttu-id="cc14d-769">Uma palavra-chave de Keyword_brazil_cpf for encontrada.</span><span class="sxs-lookup"><span data-stu-id="cc14d-769">A keyword from Keyword_brazil_cpf is found.</span></span>
- <span data-ttu-id="cc14d-770">A soma de verificação passa.</span><span class="sxs-lookup"><span data-stu-id="cc14d-770">The checksum passes.</span></span>

<span data-ttu-id="cc14d-771">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="cc14d-771">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="cc14d-772">A função Func_brazil_cpf localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="cc14d-772">The function Func_brazil_cpf finds content that matches the pattern.</span></span>
- <span data-ttu-id="cc14d-773">A soma de verificação passa.</span><span class="sxs-lookup"><span data-stu-id="cc14d-773">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="cc14d-774">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="cc14d-774">Keywords</span></span>

#### <a name="keywordbrazilcpf"></a><span data-ttu-id="cc14d-775">Keyword_brazil_cpf</span><span class="sxs-lookup"><span data-stu-id="cc14d-775">Keyword_brazil_cpf</span></span>

- <span data-ttu-id="cc14d-776">CPF</span><span class="sxs-lookup"><span data-stu-id="cc14d-776">CPF</span></span>
- <span data-ttu-id="cc14d-777">Identificador</span><span class="sxs-lookup"><span data-stu-id="cc14d-777">Identification</span></span>
- <span data-ttu-id="cc14d-778">Registro</span><span class="sxs-lookup"><span data-stu-id="cc14d-778">Registration</span></span>
- <span data-ttu-id="cc14d-779">Participação</span><span class="sxs-lookup"><span data-stu-id="cc14d-779">Revenue</span></span>
- <span data-ttu-id="cc14d-780">Cadastro de Pessoas Físicas</span><span class="sxs-lookup"><span data-stu-id="cc14d-780">Cadastro de Pessoas Físicas</span></span> 
- <span data-ttu-id="cc14d-781">Imposto</span><span class="sxs-lookup"><span data-stu-id="cc14d-781">Imposto</span></span> 
- <span data-ttu-id="cc14d-782">Identificação</span><span class="sxs-lookup"><span data-stu-id="cc14d-782">Identificação</span></span> 
- <span data-ttu-id="cc14d-783">Inscrição</span><span class="sxs-lookup"><span data-stu-id="cc14d-783">Inscrição</span></span> 
- <span data-ttu-id="cc14d-784">Receita</span><span class="sxs-lookup"><span data-stu-id="cc14d-784">Receita</span></span> 
   
## <a name="brazil-legal-entity-number-cnpj"></a><span data-ttu-id="cc14d-785">Número de Pessoa Jurídica (CNPJ) do Brasil</span><span class="sxs-lookup"><span data-stu-id="cc14d-785">Brazil Legal Entity Number (CNPJ)</span></span>

### <a name="format"></a><span data-ttu-id="cc14d-786">Format</span><span class="sxs-lookup"><span data-stu-id="cc14d-786">Format</span></span>

<span data-ttu-id="cc14d-787">14 dígitos que incluem um número de registro, o número da ramificação e dígitos de verificação, além de delimitadores de seleção</span><span class="sxs-lookup"><span data-stu-id="cc14d-787">14 digits that include a registration number, branch number, and check digits, plus delimiters</span></span>

### <a name="pattern"></a><span data-ttu-id="cc14d-788">Padrão</span><span class="sxs-lookup"><span data-stu-id="cc14d-788">Pattern</span></span>
<span data-ttu-id="cc14d-789">14 dígitos mais delimitadores:</span><span class="sxs-lookup"><span data-stu-id="cc14d-789">14 digits, plus delimiters:</span></span>
- <span data-ttu-id="cc14d-790">Dois dígitos</span><span class="sxs-lookup"><span data-stu-id="cc14d-790">Two digits</span></span> 
- <span data-ttu-id="cc14d-791">Um ponto </span><span class="sxs-lookup"><span data-stu-id="cc14d-791">A period</span></span> 
- <span data-ttu-id="cc14d-792">Três dígitos</span><span class="sxs-lookup"><span data-stu-id="cc14d-792">Three digits</span></span> 
- <span data-ttu-id="cc14d-793">Um ponto </span><span class="sxs-lookup"><span data-stu-id="cc14d-793">A period</span></span> 
- <span data-ttu-id="cc14d-794">Três dígitos (esses primeiros oito dígitos são o número de registro) </span><span class="sxs-lookup"><span data-stu-id="cc14d-794">Three digits (these first eight digits are the registration number)</span></span> 
- <span data-ttu-id="cc14d-795">Uma barra</span><span class="sxs-lookup"><span data-stu-id="cc14d-795">A forward slash</span></span> 
- <span data-ttu-id="cc14d-796">Número da ramificação de quatro dígitos </span><span class="sxs-lookup"><span data-stu-id="cc14d-796">Four-digit branch number</span></span> 
- <span data-ttu-id="cc14d-797">Um hífen</span><span class="sxs-lookup"><span data-stu-id="cc14d-797">A hyphen</span></span> 
- <span data-ttu-id="cc14d-798">Dois dígitos que são dígitos de verificação</span><span class="sxs-lookup"><span data-stu-id="cc14d-798">Two digits which are check digits</span></span>

### <a name="checksum"></a><span data-ttu-id="cc14d-799">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="cc14d-799">Checksum</span></span>

<span data-ttu-id="cc14d-800">Sim</span><span class="sxs-lookup"><span data-stu-id="cc14d-800">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="cc14d-801">Definição</span><span class="sxs-lookup"><span data-stu-id="cc14d-801">Definition</span></span>

<span data-ttu-id="cc14d-802">Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="cc14d-802">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="cc14d-803">A função Func_brazil_cnpj localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="cc14d-803">The function Func_brazil_cnpj finds content that matches the pattern.</span></span>
- <span data-ttu-id="cc14d-804">Uma palavra-chave de Keyword_brazil_cnpj for encontrada.</span><span class="sxs-lookup"><span data-stu-id="cc14d-804">A keyword from Keyword_brazil_cnpj is found.</span></span>
- <span data-ttu-id="cc14d-805">A soma de verificação passa.</span><span class="sxs-lookup"><span data-stu-id="cc14d-805">The checksum passes.</span></span>

<span data-ttu-id="cc14d-806">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="cc14d-806">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="cc14d-807">A função Func_brazil_cnpj localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="cc14d-807">The function Func_brazil_cnpj finds content that matches the pattern.</span></span>
- <span data-ttu-id="cc14d-808">A soma de verificação passa.</span><span class="sxs-lookup"><span data-stu-id="cc14d-808">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="cc14d-809">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="cc14d-809">Keywords</span></span>

#### <a name="keywordbrazilcnpj"></a><span data-ttu-id="cc14d-810">Keyword_brazil_cnpj</span><span class="sxs-lookup"><span data-stu-id="cc14d-810">Keyword_brazil_cnpj</span></span>

- <span data-ttu-id="cc14d-811">CNPJ</span><span class="sxs-lookup"><span data-stu-id="cc14d-811">CNPJ</span></span> 
- <span data-ttu-id="cc14d-812">CNPJ/MF</span><span class="sxs-lookup"><span data-stu-id="cc14d-812">CNPJ/MF</span></span> 
- <span data-ttu-id="cc14d-813">CNPJ-MF</span><span class="sxs-lookup"><span data-stu-id="cc14d-813">CNPJ-MF</span></span> 
- <span data-ttu-id="cc14d-814">Registro Nacional de Pessoas Jurídicas</span><span class="sxs-lookup"><span data-stu-id="cc14d-814">National Registry of Legal Entities</span></span> 
- <span data-ttu-id="cc14d-815">Registro de Contribuintes</span><span class="sxs-lookup"><span data-stu-id="cc14d-815">Taxpayers Registry</span></span> 
- <span data-ttu-id="cc14d-816">Pessoa jurídica</span><span class="sxs-lookup"><span data-stu-id="cc14d-816">Legal entity</span></span> 
- <span data-ttu-id="cc14d-817">Pessoas jurídicas</span><span class="sxs-lookup"><span data-stu-id="cc14d-817">Legal entities</span></span> 
- <span data-ttu-id="cc14d-818">Status do Registro</span><span class="sxs-lookup"><span data-stu-id="cc14d-818">Registration Status</span></span> 
- <span data-ttu-id="cc14d-819">Negócios</span><span class="sxs-lookup"><span data-stu-id="cc14d-819">Business</span></span> 
- <span data-ttu-id="cc14d-820">Empresa</span><span class="sxs-lookup"><span data-stu-id="cc14d-820">Company</span></span>
- <span data-ttu-id="cc14d-821">CNPJ</span><span class="sxs-lookup"><span data-stu-id="cc14d-821">CNPJ</span></span> 
- <span data-ttu-id="cc14d-822">Cadastro Nacional da Pessoa Jurídica</span><span class="sxs-lookup"><span data-stu-id="cc14d-822">Cadastro Nacional da Pessoa Jurídica</span></span> 
- <span data-ttu-id="cc14d-823">Cadastro Geral de Contribuintes</span><span class="sxs-lookup"><span data-stu-id="cc14d-823">Cadastro Geral de Contribuintes</span></span> 
- <span data-ttu-id="cc14d-824">CGC</span><span class="sxs-lookup"><span data-stu-id="cc14d-824">CGC</span></span> 
- <span data-ttu-id="cc14d-825">Pessoa jurídica</span><span class="sxs-lookup"><span data-stu-id="cc14d-825">Pessoa jurídica</span></span> 
- <span data-ttu-id="cc14d-826">Pessoas jurídicas</span><span class="sxs-lookup"><span data-stu-id="cc14d-826">Pessoas jurídicas</span></span> 
- <span data-ttu-id="cc14d-827">Situação cadastral</span><span class="sxs-lookup"><span data-stu-id="cc14d-827">Situação cadastral</span></span> 
- <span data-ttu-id="cc14d-828">Inscrição</span><span class="sxs-lookup"><span data-stu-id="cc14d-828">Inscrição</span></span> 
- <span data-ttu-id="cc14d-829">Empresa</span><span class="sxs-lookup"><span data-stu-id="cc14d-829">Empresa</span></span> 
   
## <a name="brazil-national-id-card-rg"></a><span data-ttu-id="cc14d-830">	Cartão de Identidade Nacional (RG) do Brasil</span><span class="sxs-lookup"><span data-stu-id="cc14d-830">Brazil National ID Card (RG)</span></span>

### <a name="format"></a><span data-ttu-id="cc14d-831">Format</span><span class="sxs-lookup"><span data-stu-id="cc14d-831">Format</span></span>

<span data-ttu-id="cc14d-832">Registro geral (formato antigo): nove dígitos</span><span class="sxs-lookup"><span data-stu-id="cc14d-832">Registro Geral (old format): Nine digits</span></span>

<span data-ttu-id="cc14d-833">Registro de identidade (RIC) (novo formato): 11 dígitos</span><span class="sxs-lookup"><span data-stu-id="cc14d-833">Registro de Identidade (RIC) (new format): 11 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="cc14d-834">Padrão</span><span class="sxs-lookup"><span data-stu-id="cc14d-834">Pattern</span></span>

<span data-ttu-id="cc14d-835">Registro Geral (formato antigo):</span><span class="sxs-lookup"><span data-stu-id="cc14d-835">Registro Geral (old format):</span></span>
- <span data-ttu-id="cc14d-836">Dois dígitos</span><span class="sxs-lookup"><span data-stu-id="cc14d-836">Two digits</span></span> 
- <span data-ttu-id="cc14d-837">Um ponto </span><span class="sxs-lookup"><span data-stu-id="cc14d-837">A period</span></span> 
- <span data-ttu-id="cc14d-838">Três dígitos</span><span class="sxs-lookup"><span data-stu-id="cc14d-838">Three digits</span></span> 
- <span data-ttu-id="cc14d-839">Um ponto </span><span class="sxs-lookup"><span data-stu-id="cc14d-839">A period</span></span> 
- <span data-ttu-id="cc14d-840">Três dígitos</span><span class="sxs-lookup"><span data-stu-id="cc14d-840">Three digits</span></span> 
- <span data-ttu-id="cc14d-841">Um hífen</span><span class="sxs-lookup"><span data-stu-id="cc14d-841">A hyphen</span></span> 
- <span data-ttu-id="cc14d-842">Um dígito que é um dígito de verificação</span><span class="sxs-lookup"><span data-stu-id="cc14d-842">One digit which is a check digit</span></span>

<span data-ttu-id="cc14d-843">Registro de identidade (RIC) (novo formato):</span><span class="sxs-lookup"><span data-stu-id="cc14d-843">Registro de Identidade (RIC) (new format):</span></span>
- <span data-ttu-id="cc14d-844">10 dígitos</span><span class="sxs-lookup"><span data-stu-id="cc14d-844">10 digits</span></span> 
- <span data-ttu-id="cc14d-845">Um hífen</span><span class="sxs-lookup"><span data-stu-id="cc14d-845">A hyphen</span></span> 
- <span data-ttu-id="cc14d-846">Um dígito que é um dígito de verificação</span><span class="sxs-lookup"><span data-stu-id="cc14d-846">One digit which is a check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="cc14d-847">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="cc14d-847">Checksum</span></span>

<span data-ttu-id="cc14d-848">Sim</span><span class="sxs-lookup"><span data-stu-id="cc14d-848">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="cc14d-849">Definição</span><span class="sxs-lookup"><span data-stu-id="cc14d-849">Definition</span></span>

<span data-ttu-id="cc14d-850">Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="cc14d-850">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="cc14d-851">A função Func_brazil_rg localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="cc14d-851">The function Func_brazil_rg finds content that matches the pattern.</span></span>
- <span data-ttu-id="cc14d-852">Uma palavra-chave de Keyword_brazil_rg for encontrada.</span><span class="sxs-lookup"><span data-stu-id="cc14d-852">A keyword from Keyword_brazil_rg is found.</span></span>
- <span data-ttu-id="cc14d-853">A soma de verificação passa.</span><span class="sxs-lookup"><span data-stu-id="cc14d-853">The checksum passes.</span></span>

<span data-ttu-id="cc14d-854">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="cc14d-854">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="cc14d-855">A função Func_brazil_rg localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="cc14d-855">The function Func_brazil_rg finds content that matches the pattern.</span></span>
- <span data-ttu-id="cc14d-856">A soma de verificação passa.</span><span class="sxs-lookup"><span data-stu-id="cc14d-856">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="cc14d-857">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="cc14d-857">Keywords</span></span>

#### <a name="keywordbrazilrg"></a><span data-ttu-id="cc14d-858">Keyword_brazil_rg</span><span class="sxs-lookup"><span data-stu-id="cc14d-858">Keyword_brazil_rg</span></span>

<span data-ttu-id="cc14d-859">Cédula de identidade ID nacional número de registro registro de identidade registro de geral RG (esta palavra-chave diferencia maiúsculas de minúsculas) RIC (essa palavra-chave diferencia maiúsculas de minúsculas)</span><span class="sxs-lookup"><span data-stu-id="cc14d-859">Cédula de identidade identity card national id número de rregistro registro de Iidentidade registro geral RG (this keyword is case sensitive) RIC (this keyword is case sensitive)</span></span> 
   
## <a name="canada-bank-account-number"></a><span data-ttu-id="cc14d-860">Número de conta bancária do Canadá</span><span class="sxs-lookup"><span data-stu-id="cc14d-860">Canada Bank Account Number</span></span>

### <a name="format"></a><span data-ttu-id="cc14d-861">Format</span><span class="sxs-lookup"><span data-stu-id="cc14d-861">Format</span></span>

<span data-ttu-id="cc14d-862">Sete ou doze dígitos</span><span class="sxs-lookup"><span data-stu-id="cc14d-862">Seven or twelve digits</span></span>

### <a name="pattern"></a><span data-ttu-id="cc14d-863">Padrão</span><span class="sxs-lookup"><span data-stu-id="cc14d-863">Pattern</span></span>

<span data-ttu-id="cc14d-864">Um número de conta bancária do Canadá tem sete ou doze dígitos.</span><span class="sxs-lookup"><span data-stu-id="cc14d-864">A Canada Bank Account Number is seven or twelve digits.</span></span>

<span data-ttu-id="cc14d-865">Um número de trânsito de conta bancária do Canadá tem:</span><span class="sxs-lookup"><span data-stu-id="cc14d-865">A Canada bank account transit number is:</span></span>
- <span data-ttu-id="cc14d-866">Cinco dígitos</span><span class="sxs-lookup"><span data-stu-id="cc14d-866">Five digits</span></span> 
- <span data-ttu-id="cc14d-867">Um hífen</span><span class="sxs-lookup"><span data-stu-id="cc14d-867">A hyphen</span></span> 
- <span data-ttu-id="cc14d-868">Três dígitos ou</span><span class="sxs-lookup"><span data-stu-id="cc14d-868">Three digits OR</span></span>
- <span data-ttu-id="cc14d-869">Um zero "0"</span><span class="sxs-lookup"><span data-stu-id="cc14d-869">A zero "0"</span></span> 
- <span data-ttu-id="cc14d-870">Oito dígitos</span><span class="sxs-lookup"><span data-stu-id="cc14d-870">Eight digits</span></span>

### <a name="checksum"></a><span data-ttu-id="cc14d-871">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="cc14d-871">Checksum</span></span>

<span data-ttu-id="cc14d-872">Não</span><span class="sxs-lookup"><span data-stu-id="cc14d-872">No</span></span>

### <a name="definition"></a><span data-ttu-id="cc14d-873">Definição</span><span class="sxs-lookup"><span data-stu-id="cc14d-873">Definition</span></span>

<span data-ttu-id="cc14d-874">Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="cc14d-874">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="cc14d-875">A expressão regular Regex_canada_bank_account_number localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="cc14d-875">The regular expression Regex_canada_bank_account_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="cc14d-876">Uma palavra-chave de Keyword_canada_bank_account_number for encontrada.</span><span class="sxs-lookup"><span data-stu-id="cc14d-876">A keyword from Keyword_canada_bank_account_number is found.</span></span>
- <span data-ttu-id="cc14d-877">A expressão regular Regex_canada_bank_account_transit_number localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="cc14d-877">The regular expression Regex_canada_bank_account_transit_number finds content that matches the pattern.</span></span>

<span data-ttu-id="cc14d-878">Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="cc14d-878">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="cc14d-879">A expressão regular Regex_canada_bank_account_number localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="cc14d-879">The regular expression Regex_canada_bank_account_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="cc14d-880">Uma palavra-chave de Keyword_canada_bank_account_number for encontrada.</span><span class="sxs-lookup"><span data-stu-id="cc14d-880">A keyword from Keyword_canada_bank_account_number is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="cc14d-881">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="cc14d-881">Keywords</span></span>

#### <a name="keywordcanadabankaccountnumber"></a><span data-ttu-id="cc14d-882">Keyword_canada_bank_account_number</span><span class="sxs-lookup"><span data-stu-id="cc14d-882">Keyword_canada_bank_account_number</span></span>

- <span data-ttu-id="cc14d-883">canada savings bonds</span><span class="sxs-lookup"><span data-stu-id="cc14d-883">canada savings bonds</span></span>
- <span data-ttu-id="cc14d-884">canada revenue agency</span><span class="sxs-lookup"><span data-stu-id="cc14d-884">canada revenue agency</span></span>
- <span data-ttu-id="cc14d-885">canadian financial institution</span><span class="sxs-lookup"><span data-stu-id="cc14d-885">canadian financial institution</span></span>
- <span data-ttu-id="cc14d-886">direct deposit form</span><span class="sxs-lookup"><span data-stu-id="cc14d-886">direct deposit form</span></span>
- <span data-ttu-id="cc14d-887">canadian citizen</span><span class="sxs-lookup"><span data-stu-id="cc14d-887">canadian citizen</span></span>
- <span data-ttu-id="cc14d-888">legal representative</span><span class="sxs-lookup"><span data-stu-id="cc14d-888">legal representative</span></span>
- <span data-ttu-id="cc14d-889">notary public</span><span class="sxs-lookup"><span data-stu-id="cc14d-889">notary public</span></span>
- <span data-ttu-id="cc14d-890">commissioner for oaths</span><span class="sxs-lookup"><span data-stu-id="cc14d-890">commissioner for oaths</span></span>
- <span data-ttu-id="cc14d-891">child care benefit</span><span class="sxs-lookup"><span data-stu-id="cc14d-891">child care benefit</span></span>
- <span data-ttu-id="cc14d-892">universal child care</span><span class="sxs-lookup"><span data-stu-id="cc14d-892">universal child care</span></span>
- <span data-ttu-id="cc14d-893">canada child tax benefit</span><span class="sxs-lookup"><span data-stu-id="cc14d-893">canada child tax benefit</span></span>
- <span data-ttu-id="cc14d-894">income tax benefit</span><span class="sxs-lookup"><span data-stu-id="cc14d-894">income tax benefit</span></span>
- <span data-ttu-id="cc14d-895">harmonized sales tax</span><span class="sxs-lookup"><span data-stu-id="cc14d-895">harmonized sales tax</span></span>
- <span data-ttu-id="cc14d-896">social insurance number</span><span class="sxs-lookup"><span data-stu-id="cc14d-896">social insurance number</span></span>
- <span data-ttu-id="cc14d-897">income tax refund</span><span class="sxs-lookup"><span data-stu-id="cc14d-897">income tax refund</span></span>
- <span data-ttu-id="cc14d-898">child tax benefit</span><span class="sxs-lookup"><span data-stu-id="cc14d-898">child tax benefit</span></span>
- <span data-ttu-id="cc14d-899">territorial payments</span><span class="sxs-lookup"><span data-stu-id="cc14d-899">territorial payments</span></span>
- <span data-ttu-id="cc14d-900">institution number</span><span class="sxs-lookup"><span data-stu-id="cc14d-900">institution number</span></span>
- <span data-ttu-id="cc14d-901">deposit request</span><span class="sxs-lookup"><span data-stu-id="cc14d-901">deposit request</span></span>
- <span data-ttu-id="cc14d-902">banking information</span><span class="sxs-lookup"><span data-stu-id="cc14d-902">banking information</span></span>
- <span data-ttu-id="cc14d-903">direct deposit</span><span class="sxs-lookup"><span data-stu-id="cc14d-903">direct deposit</span></span>
   
## <a name="canada-drivers-license-number"></a><span data-ttu-id="cc14d-904">Número de carteira de motorista do Canadá</span><span class="sxs-lookup"><span data-stu-id="cc14d-904">Canada Driver's License Number</span></span>

### <a name="format"></a><span data-ttu-id="cc14d-905">Format</span><span class="sxs-lookup"><span data-stu-id="cc14d-905">Format</span></span>

<span data-ttu-id="cc14d-906">Varia por província</span><span class="sxs-lookup"><span data-stu-id="cc14d-906">Varies by province</span></span>

### <a name="pattern"></a><span data-ttu-id="cc14d-907">Padrão</span><span class="sxs-lookup"><span data-stu-id="cc14d-907">Pattern</span></span>

<span data-ttu-id="cc14d-908">Vários padrões que abrangem Alberta, Columbia Britânica, Manitoba, New Brunswick, Newfoundland/Labrador, Nova Escócia, Ontário, Ilha do Príncipe Eduardo, Quebec e Saskatchewan</span><span class="sxs-lookup"><span data-stu-id="cc14d-908">Various patterns covering Alberta, British Columbia, Manitoba, New Brunswick, Newfoundland/Labrador, Nova Scotia, Ontario, Prince Edward Island, Quebec, and Saskatchewan</span></span>

### <a name="checksum"></a><span data-ttu-id="cc14d-909">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="cc14d-909">Checksum</span></span>

<span data-ttu-id="cc14d-910">Não</span><span class="sxs-lookup"><span data-stu-id="cc14d-910">No</span></span>

### <a name="definition"></a><span data-ttu-id="cc14d-911">Definição</span><span class="sxs-lookup"><span data-stu-id="cc14d-911">Definition</span></span>

<span data-ttu-id="cc14d-912">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="cc14d-912">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="cc14d-913">A função Func_[province_name]_drivers_license_number localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="cc14d-913">The function Func_[province_name]_drivers_license_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="cc14d-914">Uma palavra-chave de Keyword_[province_name]_drivers_license_name for encontrada.</span><span class="sxs-lookup"><span data-stu-id="cc14d-914">A keyword from Keyword_[province_name]_drivers_license_name is found.</span></span>
- <span data-ttu-id="cc14d-915">Uma palavra-chave de Keyword_canada_drivers_license for encontrada.</span><span class="sxs-lookup"><span data-stu-id="cc14d-915">A keyword from Keyword_canada_drivers_license is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="cc14d-916">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="cc14d-916">Keywords</span></span>

#### <a name="keywordprovincenamedriverslicensename"></a><span data-ttu-id="cc14d-917">Keyword_ [province_name] _drivers_license_name</span><span class="sxs-lookup"><span data-stu-id="cc14d-917">Keyword_[province_name]_drivers_license_name</span></span>

- <span data-ttu-id="cc14d-918">A abreviação da província, por exemplo AB</span><span class="sxs-lookup"><span data-stu-id="cc14d-918">The province abbreviation, for example AB</span></span>
- <span data-ttu-id="cc14d-919">O nome da província, por exemplo, Alberta</span><span class="sxs-lookup"><span data-stu-id="cc14d-919">The province name, for example Alberta</span></span>

#### <a name="keywordcanadadriverslicense"></a><span data-ttu-id="cc14d-920">Keyword_canada_drivers_license</span><span class="sxs-lookup"><span data-stu-id="cc14d-920">Keyword_canada_drivers_license</span></span>

- <span data-ttu-id="cc14d-921">DISTRIBUIÇÃO</span><span class="sxs-lookup"><span data-stu-id="cc14d-921">DL</span></span>
- <span data-ttu-id="cc14d-922">DL</span><span class="sxs-lookup"><span data-stu-id="cc14d-922">DLS</span></span>
- <span data-ttu-id="cc14d-923">CDL</span><span class="sxs-lookup"><span data-stu-id="cc14d-923">CDL</span></span>
- <span data-ttu-id="cc14d-924">CDLS</span><span class="sxs-lookup"><span data-stu-id="cc14d-924">CDLS</span></span>
- <span data-ttu-id="cc14d-925">DriverLic</span><span class="sxs-lookup"><span data-stu-id="cc14d-925">DriverLic</span></span>
- <span data-ttu-id="cc14d-926">DriverLics</span><span class="sxs-lookup"><span data-stu-id="cc14d-926">DriverLics</span></span>
- <span data-ttu-id="cc14d-927">DriverLicense</span><span class="sxs-lookup"><span data-stu-id="cc14d-927">DriverLicense</span></span>
- <span data-ttu-id="cc14d-928">DriverLicenses</span><span class="sxs-lookup"><span data-stu-id="cc14d-928">DriverLicenses</span></span>
- <span data-ttu-id="cc14d-929">DriverLicence</span><span class="sxs-lookup"><span data-stu-id="cc14d-929">DriverLicence</span></span>
- <span data-ttu-id="cc14d-930">DriverLicences</span><span class="sxs-lookup"><span data-stu-id="cc14d-930">DriverLicences</span></span>
- <span data-ttu-id="cc14d-931">Driver Lic</span><span class="sxs-lookup"><span data-stu-id="cc14d-931">Driver Lic</span></span>
- <span data-ttu-id="cc14d-932">Driver Lics</span><span class="sxs-lookup"><span data-stu-id="cc14d-932">Driver Lics</span></span>
- <span data-ttu-id="cc14d-933">Driver License</span><span class="sxs-lookup"><span data-stu-id="cc14d-933">Driver License</span></span>
- <span data-ttu-id="cc14d-934">Driver Licenses</span><span class="sxs-lookup"><span data-stu-id="cc14d-934">Driver Licenses</span></span>
- <span data-ttu-id="cc14d-935">Driver Licence</span><span class="sxs-lookup"><span data-stu-id="cc14d-935">Driver Licence</span></span>
- <span data-ttu-id="cc14d-936">Driver Licences</span><span class="sxs-lookup"><span data-stu-id="cc14d-936">Driver Licences</span></span>
- <span data-ttu-id="cc14d-937">DriversLic</span><span class="sxs-lookup"><span data-stu-id="cc14d-937">DriversLic</span></span>
- <span data-ttu-id="cc14d-938">DriversLics</span><span class="sxs-lookup"><span data-stu-id="cc14d-938">DriversLics</span></span>
- <span data-ttu-id="cc14d-939">DriversLicence</span><span class="sxs-lookup"><span data-stu-id="cc14d-939">DriversLicence</span></span>
- <span data-ttu-id="cc14d-940">DriversLicences</span><span class="sxs-lookup"><span data-stu-id="cc14d-940">DriversLicences</span></span>
- <span data-ttu-id="cc14d-941">DriversLicense</span><span class="sxs-lookup"><span data-stu-id="cc14d-941">DriversLicense</span></span>
- <span data-ttu-id="cc14d-942">DriversLicenses</span><span class="sxs-lookup"><span data-stu-id="cc14d-942">DriversLicenses</span></span>
- <span data-ttu-id="cc14d-943">Drivers Lic</span><span class="sxs-lookup"><span data-stu-id="cc14d-943">Drivers Lic</span></span>
- <span data-ttu-id="cc14d-944">Drivers Lics</span><span class="sxs-lookup"><span data-stu-id="cc14d-944">Drivers Lics</span></span>
- <span data-ttu-id="cc14d-945">Drivers License</span><span class="sxs-lookup"><span data-stu-id="cc14d-945">Drivers License</span></span>
- <span data-ttu-id="cc14d-946">Drivers Licenses</span><span class="sxs-lookup"><span data-stu-id="cc14d-946">Drivers Licenses</span></span>
- <span data-ttu-id="cc14d-947">Drivers Licence</span><span class="sxs-lookup"><span data-stu-id="cc14d-947">Drivers Licence</span></span>
- <span data-ttu-id="cc14d-948">Drivers Licences</span><span class="sxs-lookup"><span data-stu-id="cc14d-948">Drivers Licences</span></span>
- <span data-ttu-id="cc14d-949">Driver'Lic</span><span class="sxs-lookup"><span data-stu-id="cc14d-949">Driver'Lic</span></span>
- <span data-ttu-id="cc14d-950">Driver'Lics</span><span class="sxs-lookup"><span data-stu-id="cc14d-950">Driver'Lics</span></span>
- <span data-ttu-id="cc14d-951">Driver'License</span><span class="sxs-lookup"><span data-stu-id="cc14d-951">Driver'License</span></span>
- <span data-ttu-id="cc14d-952">Driver'Licenses</span><span class="sxs-lookup"><span data-stu-id="cc14d-952">Driver'Licenses</span></span>
- <span data-ttu-id="cc14d-953">Driver'Licence</span><span class="sxs-lookup"><span data-stu-id="cc14d-953">Driver'Licence</span></span>
- <span data-ttu-id="cc14d-954">Driver'Licences</span><span class="sxs-lookup"><span data-stu-id="cc14d-954">Driver'Licences</span></span>
- <span data-ttu-id="cc14d-955">Driver'Lic</span><span class="sxs-lookup"><span data-stu-id="cc14d-955">Driver' Lic</span></span>
- <span data-ttu-id="cc14d-956">Driver' Lics</span><span class="sxs-lookup"><span data-stu-id="cc14d-956">Driver' Lics</span></span>
- <span data-ttu-id="cc14d-957">Driver' License</span><span class="sxs-lookup"><span data-stu-id="cc14d-957">Driver' License</span></span>
- <span data-ttu-id="cc14d-958">Driver'Licenses</span><span class="sxs-lookup"><span data-stu-id="cc14d-958">Driver' Licenses</span></span>
- <span data-ttu-id="cc14d-959">Driver'Licence</span><span class="sxs-lookup"><span data-stu-id="cc14d-959">Driver' Licence</span></span>
- <span data-ttu-id="cc14d-960">Driver'Licences</span><span class="sxs-lookup"><span data-stu-id="cc14d-960">Driver' Licences</span></span>
- <span data-ttu-id="cc14d-961">Driver'sLic</span><span class="sxs-lookup"><span data-stu-id="cc14d-961">Driver'sLic</span></span>
- <span data-ttu-id="cc14d-962">Driver'sLics</span><span class="sxs-lookup"><span data-stu-id="cc14d-962">Driver'sLics</span></span>
- <span data-ttu-id="cc14d-963">Driver'sLicense</span><span class="sxs-lookup"><span data-stu-id="cc14d-963">Driver'sLicense</span></span>
- <span data-ttu-id="cc14d-964">Driver'sLicenses</span><span class="sxs-lookup"><span data-stu-id="cc14d-964">Driver'sLicenses</span></span>
- <span data-ttu-id="cc14d-965">Driver'sLicence</span><span class="sxs-lookup"><span data-stu-id="cc14d-965">Driver'sLicence</span></span>
- <span data-ttu-id="cc14d-966">Driver'sLicences</span><span class="sxs-lookup"><span data-stu-id="cc14d-966">Driver'sLicences</span></span>
- <span data-ttu-id="cc14d-967">Driver's Lic</span><span class="sxs-lookup"><span data-stu-id="cc14d-967">Driver's Lic</span></span>
- <span data-ttu-id="cc14d-968">Driver's Lics</span><span class="sxs-lookup"><span data-stu-id="cc14d-968">Driver's Lics</span></span>
- <span data-ttu-id="cc14d-969">Driver's License</span><span class="sxs-lookup"><span data-stu-id="cc14d-969">Driver's License</span></span>
- <span data-ttu-id="cc14d-970">Driver's Licenses</span><span class="sxs-lookup"><span data-stu-id="cc14d-970">Driver's Licenses</span></span>
- <span data-ttu-id="cc14d-971">Driver's Licence</span><span class="sxs-lookup"><span data-stu-id="cc14d-971">Driver's Licence</span></span>
- <span data-ttu-id="cc14d-972">Driver's Licences</span><span class="sxs-lookup"><span data-stu-id="cc14d-972">Driver's Licences</span></span>
- <span data-ttu-id="cc14d-973">Permis de Conduire</span><span class="sxs-lookup"><span data-stu-id="cc14d-973">Permis de Conduire</span></span>
- <span data-ttu-id="cc14d-974">id</span><span class="sxs-lookup"><span data-stu-id="cc14d-974">id</span></span>
- <span data-ttu-id="cc14d-975">ids</span><span class="sxs-lookup"><span data-stu-id="cc14d-975">ids</span></span>
- <span data-ttu-id="cc14d-976">idcard number</span><span class="sxs-lookup"><span data-stu-id="cc14d-976">idcard number</span></span>
- <span data-ttu-id="cc14d-977">idcard numbers</span><span class="sxs-lookup"><span data-stu-id="cc14d-977">idcard numbers</span></span>
- <span data-ttu-id="cc14d-978">idcard #</span><span class="sxs-lookup"><span data-stu-id="cc14d-978">idcard #</span></span>
- <span data-ttu-id="cc14d-979">idcard #s</span><span class="sxs-lookup"><span data-stu-id="cc14d-979">idcard #s</span></span>
- <span data-ttu-id="cc14d-980">idcard card</span><span class="sxs-lookup"><span data-stu-id="cc14d-980">idcard card</span></span>
- <span data-ttu-id="cc14d-981">idcard cards</span><span class="sxs-lookup"><span data-stu-id="cc14d-981">idcard cards</span></span>
- <span data-ttu-id="cc14d-982">idcard</span><span class="sxs-lookup"><span data-stu-id="cc14d-982">idcard</span></span>
- <span data-ttu-id="cc14d-983">identification number</span><span class="sxs-lookup"><span data-stu-id="cc14d-983">identification number</span></span>
- <span data-ttu-id="cc14d-984">identification numbers</span><span class="sxs-lookup"><span data-stu-id="cc14d-984">identification numbers</span></span>
- <span data-ttu-id="cc14d-985">identification #</span><span class="sxs-lookup"><span data-stu-id="cc14d-985">identification #</span></span>
- <span data-ttu-id="cc14d-986">identification #s</span><span class="sxs-lookup"><span data-stu-id="cc14d-986">identification #s</span></span>
- <span data-ttu-id="cc14d-987">identification card</span><span class="sxs-lookup"><span data-stu-id="cc14d-987">identification card</span></span>
- <span data-ttu-id="cc14d-988">identification cards</span><span class="sxs-lookup"><span data-stu-id="cc14d-988">identification cards</span></span>
- <span data-ttu-id="cc14d-989">identificador</span><span class="sxs-lookup"><span data-stu-id="cc14d-989">identification</span></span> 
- <span data-ttu-id="cc14d-990">DISTRIBUIÇÃO</span><span class="sxs-lookup"><span data-stu-id="cc14d-990">DL#</span></span>
- <span data-ttu-id="cc14d-991">DL</span><span class="sxs-lookup"><span data-stu-id="cc14d-991">DLS#</span></span> 
- <span data-ttu-id="cc14d-992">CDL</span><span class="sxs-lookup"><span data-stu-id="cc14d-992">CDL#</span></span> 
- <span data-ttu-id="cc14d-993">CDLS #</span><span class="sxs-lookup"><span data-stu-id="cc14d-993">CDLS#</span></span> 
- <span data-ttu-id="cc14d-994">DriverLic #</span><span class="sxs-lookup"><span data-stu-id="cc14d-994">DriverLic#</span></span> 
- <span data-ttu-id="cc14d-995">DriverLics #</span><span class="sxs-lookup"><span data-stu-id="cc14d-995">DriverLics#</span></span> 
- <span data-ttu-id="cc14d-996">DriverLicense #</span><span class="sxs-lookup"><span data-stu-id="cc14d-996">DriverLicense#</span></span> 
- <span data-ttu-id="cc14d-997">DriverLicenses #</span><span class="sxs-lookup"><span data-stu-id="cc14d-997">DriverLicenses#</span></span> 
- <span data-ttu-id="cc14d-998">DriverLicence #</span><span class="sxs-lookup"><span data-stu-id="cc14d-998">DriverLicence#</span></span> 
- <span data-ttu-id="cc14d-999">DriverLicences #</span><span class="sxs-lookup"><span data-stu-id="cc14d-999">DriverLicences#</span></span> 
- <span data-ttu-id="cc14d-1000">Driver Lic#</span><span class="sxs-lookup"><span data-stu-id="cc14d-1000">Driver Lic#</span></span>
- <span data-ttu-id="cc14d-1001">Driver Lics#</span><span class="sxs-lookup"><span data-stu-id="cc14d-1001">Driver Lics#</span></span> 
- <span data-ttu-id="cc14d-1002">Driver License#</span><span class="sxs-lookup"><span data-stu-id="cc14d-1002">Driver License#</span></span> 
- <span data-ttu-id="cc14d-1003">Driver Licenses#</span><span class="sxs-lookup"><span data-stu-id="cc14d-1003">Driver Licenses#</span></span> 
- <span data-ttu-id="cc14d-1004">Driver License#</span><span class="sxs-lookup"><span data-stu-id="cc14d-1004">Driver License#</span></span> 
- <span data-ttu-id="cc14d-1005">Driver Licences#</span><span class="sxs-lookup"><span data-stu-id="cc14d-1005">Driver Licences#</span></span> 
- <span data-ttu-id="cc14d-1006">DriversLic #</span><span class="sxs-lookup"><span data-stu-id="cc14d-1006">DriversLic#</span></span> 
- <span data-ttu-id="cc14d-1007">DriversLics #</span><span class="sxs-lookup"><span data-stu-id="cc14d-1007">DriversLics#</span></span> 
- <span data-ttu-id="cc14d-1008">DriversLicense #</span><span class="sxs-lookup"><span data-stu-id="cc14d-1008">DriversLicense#</span></span> 
- <span data-ttu-id="cc14d-1009">DriversLicenses #</span><span class="sxs-lookup"><span data-stu-id="cc14d-1009">DriversLicenses#</span></span> 
- <span data-ttu-id="cc14d-1010">DriversLicence #</span><span class="sxs-lookup"><span data-stu-id="cc14d-1010">DriversLicence#</span></span> 
- <span data-ttu-id="cc14d-1011">DriversLicences #</span><span class="sxs-lookup"><span data-stu-id="cc14d-1011">DriversLicences#</span></span> 
- <span data-ttu-id="cc14d-1012">Drivers Lic#</span><span class="sxs-lookup"><span data-stu-id="cc14d-1012">Drivers Lic#</span></span> 
- <span data-ttu-id="cc14d-1013">Drivers Lics#</span><span class="sxs-lookup"><span data-stu-id="cc14d-1013">Drivers Lics#</span></span> 
- <span data-ttu-id="cc14d-1014">Drivers License#</span><span class="sxs-lookup"><span data-stu-id="cc14d-1014">Drivers License#</span></span> 
- <span data-ttu-id="cc14d-1015">Drivers Licenses#</span><span class="sxs-lookup"><span data-stu-id="cc14d-1015">Drivers Licenses#</span></span> 
- <span data-ttu-id="cc14d-1016">Drivers Licence#</span><span class="sxs-lookup"><span data-stu-id="cc14d-1016">Drivers Licence#</span></span> 
- <span data-ttu-id="cc14d-1017">Drivers Licences#</span><span class="sxs-lookup"><span data-stu-id="cc14d-1017">Drivers Licences#</span></span> 
- <span data-ttu-id="cc14d-1018">Driver'Lic #</span><span class="sxs-lookup"><span data-stu-id="cc14d-1018">Driver'Lic#</span></span> 
- <span data-ttu-id="cc14d-1019">Driver'Lics #</span><span class="sxs-lookup"><span data-stu-id="cc14d-1019">Driver'Lics#</span></span> 
- <span data-ttu-id="cc14d-1020">Driver'License #</span><span class="sxs-lookup"><span data-stu-id="cc14d-1020">Driver'License#</span></span> 
- <span data-ttu-id="cc14d-1021">Driver'Licenses #</span><span class="sxs-lookup"><span data-stu-id="cc14d-1021">Driver'Licenses#</span></span> 
- <span data-ttu-id="cc14d-1022">Driver'Licence #</span><span class="sxs-lookup"><span data-stu-id="cc14d-1022">Driver'Licence#</span></span> 
- <span data-ttu-id="cc14d-1023">Driver'Licences #</span><span class="sxs-lookup"><span data-stu-id="cc14d-1023">Driver'Licences#</span></span> 
- <span data-ttu-id="cc14d-1024">Driver'Lic#</span><span class="sxs-lookup"><span data-stu-id="cc14d-1024">Driver' Lic#</span></span> 
- <span data-ttu-id="cc14d-1025">Driver' Lics#</span><span class="sxs-lookup"><span data-stu-id="cc14d-1025">Driver' Lics#</span></span> 
- <span data-ttu-id="cc14d-1026">Driver' License#</span><span class="sxs-lookup"><span data-stu-id="cc14d-1026">Driver' License#</span></span> 
- <span data-ttu-id="cc14d-1027">Driver'Licenses#</span><span class="sxs-lookup"><span data-stu-id="cc14d-1027">Driver' Licenses#</span></span> 
- <span data-ttu-id="cc14d-1028">Driver'Licence#</span><span class="sxs-lookup"><span data-stu-id="cc14d-1028">Driver' Licence#</span></span> 
- <span data-ttu-id="cc14d-1029">Driver'Licences#</span><span class="sxs-lookup"><span data-stu-id="cc14d-1029">Driver' Licences#</span></span> 
- <span data-ttu-id="cc14d-1030">Driver'sLic #</span><span class="sxs-lookup"><span data-stu-id="cc14d-1030">Driver'sLic#</span></span> 
- <span data-ttu-id="cc14d-1031">Driver'sLics #</span><span class="sxs-lookup"><span data-stu-id="cc14d-1031">Driver'sLics#</span></span> 
- <span data-ttu-id="cc14d-1032">Driver'sLicense #</span><span class="sxs-lookup"><span data-stu-id="cc14d-1032">Driver'sLicense#</span></span> 
- <span data-ttu-id="cc14d-1033">Driver'sLicenses #</span><span class="sxs-lookup"><span data-stu-id="cc14d-1033">Driver'sLicenses#</span></span> 
- <span data-ttu-id="cc14d-1034">Driver'sLicence #</span><span class="sxs-lookup"><span data-stu-id="cc14d-1034">Driver'sLicence#</span></span> 
- <span data-ttu-id="cc14d-1035">Driver'sLicences #</span><span class="sxs-lookup"><span data-stu-id="cc14d-1035">Driver'sLicences#</span></span> 
- <span data-ttu-id="cc14d-1036">Driver's Lic#</span><span class="sxs-lookup"><span data-stu-id="cc14d-1036">Driver's Lic#</span></span> 
- <span data-ttu-id="cc14d-1037">Driver's Lics#</span><span class="sxs-lookup"><span data-stu-id="cc14d-1037">Driver's Lics#</span></span> 
- <span data-ttu-id="cc14d-1038">Driver's License#</span><span class="sxs-lookup"><span data-stu-id="cc14d-1038">Driver's License#</span></span> 
- <span data-ttu-id="cc14d-1039">Driver's Licenses#</span><span class="sxs-lookup"><span data-stu-id="cc14d-1039">Driver's Licenses#</span></span> 
- <span data-ttu-id="cc14d-1040">Driver's Licence#</span><span class="sxs-lookup"><span data-stu-id="cc14d-1040">Driver's Licence#</span></span> 
- <span data-ttu-id="cc14d-1041">Driver's Licences#</span><span class="sxs-lookup"><span data-stu-id="cc14d-1041">Driver's Licences#</span></span> 
- <span data-ttu-id="cc14d-1042">Permis de Conduire#</span><span class="sxs-lookup"><span data-stu-id="cc14d-1042">Permis de Conduire#</span></span> 
- <span data-ttu-id="cc14d-1043">ID</span><span class="sxs-lookup"><span data-stu-id="cc14d-1043">id#</span></span> 
- <span data-ttu-id="cc14d-1044">código</span><span class="sxs-lookup"><span data-stu-id="cc14d-1044">ids#</span></span> 
- <span data-ttu-id="cc14d-1045">idcard card#</span><span class="sxs-lookup"><span data-stu-id="cc14d-1045">idcard card#</span></span> 
- <span data-ttu-id="cc14d-1046">idcard cards#</span><span class="sxs-lookup"><span data-stu-id="cc14d-1046">idcard cards#</span></span> 
- <span data-ttu-id="cc14d-1047">idcard #</span><span class="sxs-lookup"><span data-stu-id="cc14d-1047">idcard#</span></span> 
- <span data-ttu-id="cc14d-1048">identification card#</span><span class="sxs-lookup"><span data-stu-id="cc14d-1048">identification card#</span></span> 
- <span data-ttu-id="cc14d-1049">identification cards#</span><span class="sxs-lookup"><span data-stu-id="cc14d-1049">identification cards#</span></span> 
- <span data-ttu-id="cc14d-1050">identificador</span><span class="sxs-lookup"><span data-stu-id="cc14d-1050">identification#</span></span> 
   
## <a name="canada-health-service-number"></a><span data-ttu-id="cc14d-1051">Número de serviço de saúde do Canadá</span><span class="sxs-lookup"><span data-stu-id="cc14d-1051">Canada Health Service Number</span></span>

### <a name="format"></a><span data-ttu-id="cc14d-1052">Format</span><span class="sxs-lookup"><span data-stu-id="cc14d-1052">Format</span></span>

<span data-ttu-id="cc14d-1053">10 dígitos</span><span class="sxs-lookup"><span data-stu-id="cc14d-1053">10 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="cc14d-1054">Padrão</span><span class="sxs-lookup"><span data-stu-id="cc14d-1054">Pattern</span></span>

<span data-ttu-id="cc14d-1055">10 dígitos</span><span class="sxs-lookup"><span data-stu-id="cc14d-1055">10 digits</span></span>

### <a name="checksum"></a><span data-ttu-id="cc14d-1056">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="cc14d-1056">Checksum</span></span>

<span data-ttu-id="cc14d-1057">Não</span><span class="sxs-lookup"><span data-stu-id="cc14d-1057">No</span></span>

### <a name="definition"></a><span data-ttu-id="cc14d-1058">Definição</span><span class="sxs-lookup"><span data-stu-id="cc14d-1058">Definition</span></span>

<span data-ttu-id="cc14d-1059">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="cc14d-1059">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="cc14d-1060">A expressão regular Regex_canada_health_service_number localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="cc14d-1060">The regular expression Regex_canada_health_service_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="cc14d-1061">Uma palavra-chave de Keyword_canada_health_service_number for encontrada.</span><span class="sxs-lookup"><span data-stu-id="cc14d-1061">A keyword from Keyword_canada_health_service_number is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="cc14d-1062">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="cc14d-1062">Keywords</span></span>

#### <a name="keywordcanadahealthservicenumber"></a><span data-ttu-id="cc14d-1063">Keyword_canada_health_service_number</span><span class="sxs-lookup"><span data-stu-id="cc14d-1063">Keyword_canada_health_service_number</span></span>

- <span data-ttu-id="cc14d-1064">personal health number</span><span class="sxs-lookup"><span data-stu-id="cc14d-1064">personal health number</span></span>
- <span data-ttu-id="cc14d-1065">patient information</span><span class="sxs-lookup"><span data-stu-id="cc14d-1065">patient information</span></span>
- <span data-ttu-id="cc14d-1066">health services</span><span class="sxs-lookup"><span data-stu-id="cc14d-1066">health services</span></span>
- <span data-ttu-id="cc14d-1067">speciality services</span><span class="sxs-lookup"><span data-stu-id="cc14d-1067">speciality services</span></span>
- <span data-ttu-id="cc14d-1068">automobile accident</span><span class="sxs-lookup"><span data-stu-id="cc14d-1068">automobile accident</span></span>
- <span data-ttu-id="cc14d-1069">patient hospital</span><span class="sxs-lookup"><span data-stu-id="cc14d-1069">patient hospital</span></span>
- <span data-ttu-id="cc14d-1070">psychiatrist</span><span class="sxs-lookup"><span data-stu-id="cc14d-1070">psychiatrist</span></span>
- <span data-ttu-id="cc14d-1071">workers compensation</span><span class="sxs-lookup"><span data-stu-id="cc14d-1071">workers compensation</span></span>
- <span data-ttu-id="cc14d-1072">Deficiência</span><span class="sxs-lookup"><span data-stu-id="cc14d-1072">disability</span></span>
      
## <a name="canada-passport-number"></a><span data-ttu-id="cc14d-1073">Número de passaporte do Canadá</span><span class="sxs-lookup"><span data-stu-id="cc14d-1073">Canada Passport Number</span></span>

### <a name="format"></a><span data-ttu-id="cc14d-1074">Format</span><span class="sxs-lookup"><span data-stu-id="cc14d-1074">Format</span></span>

<span data-ttu-id="cc14d-1075">Duas letras maiúsculas, seguidas de seis dígitos</span><span class="sxs-lookup"><span data-stu-id="cc14d-1075">Two uppercase letters followed by six digits</span></span>

### <a name="pattern"></a><span data-ttu-id="cc14d-1076">Padrão</span><span class="sxs-lookup"><span data-stu-id="cc14d-1076">Pattern</span></span>

<span data-ttu-id="cc14d-1077">Duas letras maiúsculas, seguidas de seis dígitos</span><span class="sxs-lookup"><span data-stu-id="cc14d-1077">Two uppercase letters followed by six digits</span></span>

### <a name="checksum"></a><span data-ttu-id="cc14d-1078">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="cc14d-1078">Checksum</span></span>

<span data-ttu-id="cc14d-1079">Não</span><span class="sxs-lookup"><span data-stu-id="cc14d-1079">No</span></span>

### <a name="definition"></a><span data-ttu-id="cc14d-1080">Definição</span><span class="sxs-lookup"><span data-stu-id="cc14d-1080">Definition</span></span>

<span data-ttu-id="cc14d-1081">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="cc14d-1081">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="cc14d-1082">A expressão regular Regex_canada_passport_number localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="cc14d-1082">The regular expression Regex_canada_passport_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="cc14d-1083">Uma palavra-chave de Keyword_canada_passport_number ou Keyword_passport for encontrada.</span><span class="sxs-lookup"><span data-stu-id="cc14d-1083">A keyword from Keyword_canada_passport_number or Keyword_passport is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="cc14d-1084">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="cc14d-1084">Keywords</span></span>

#### <a name="keywordcanadapassportnumber"></a><span data-ttu-id="cc14d-1085">Keyword_canada_passport_number</span><span class="sxs-lookup"><span data-stu-id="cc14d-1085">Keyword_canada_passport_number</span></span>

- <span data-ttu-id="cc14d-1086">canadian citizenship</span><span class="sxs-lookup"><span data-stu-id="cc14d-1086">canadian citizenship</span></span>
- <span data-ttu-id="cc14d-1087">canadian passport</span><span class="sxs-lookup"><span data-stu-id="cc14d-1087">canadian passport</span></span>
- <span data-ttu-id="cc14d-1088">passport application</span><span class="sxs-lookup"><span data-stu-id="cc14d-1088">passport application</span></span>
- <span data-ttu-id="cc14d-1089">passport photos</span><span class="sxs-lookup"><span data-stu-id="cc14d-1089">passport photos</span></span>
- <span data-ttu-id="cc14d-1090">certified translator</span><span class="sxs-lookup"><span data-stu-id="cc14d-1090">certified translator</span></span>
- <span data-ttu-id="cc14d-1091">canadian citizens</span><span class="sxs-lookup"><span data-stu-id="cc14d-1091">canadian citizens</span></span>
- <span data-ttu-id="cc14d-1092">processing times</span><span class="sxs-lookup"><span data-stu-id="cc14d-1092">processing times</span></span>
- <span data-ttu-id="cc14d-1093">renewal application</span><span class="sxs-lookup"><span data-stu-id="cc14d-1093">renewal application</span></span>

#### <a name="keywordpassport"></a><span data-ttu-id="cc14d-1094">Keyword_passport</span><span class="sxs-lookup"><span data-stu-id="cc14d-1094">Keyword_passport</span></span>

- <span data-ttu-id="cc14d-1095">Passport Number</span><span class="sxs-lookup"><span data-stu-id="cc14d-1095">Passport Number</span></span>
- <span data-ttu-id="cc14d-1096">Passport No</span><span class="sxs-lookup"><span data-stu-id="cc14d-1096">Passport No</span></span>
- <span data-ttu-id="cc14d-1097">Passport #</span><span class="sxs-lookup"><span data-stu-id="cc14d-1097">Passport #</span></span>
- <span data-ttu-id="cc14d-1098">Passaport</span><span class="sxs-lookup"><span data-stu-id="cc14d-1098">Passport#</span></span>
- <span data-ttu-id="cc14d-1099">Passportid</span><span class="sxs-lookup"><span data-stu-id="cc14d-1099">PassportID</span></span>
- <span data-ttu-id="cc14d-1100">Passportno</span><span class="sxs-lookup"><span data-stu-id="cc14d-1100">Passportno</span></span>
- <span data-ttu-id="cc14d-1101">passportnumber</span><span class="sxs-lookup"><span data-stu-id="cc14d-1101">passportnumber</span></span>
- <span data-ttu-id="cc14d-1102">パスポート</span><span class="sxs-lookup"><span data-stu-id="cc14d-1102">パスポート</span></span>
- <span data-ttu-id="cc14d-1103">パスポート番号</span><span class="sxs-lookup"><span data-stu-id="cc14d-1103">パスポート番号</span></span>
- <span data-ttu-id="cc14d-1104">パスポートのNum</span><span class="sxs-lookup"><span data-stu-id="cc14d-1104">パスポートのNum</span></span>
- <span data-ttu-id="cc14d-1105">パスポート #</span><span class="sxs-lookup"><span data-stu-id="cc14d-1105">パスポート＃</span></span>
- <span data-ttu-id="cc14d-1106">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="cc14d-1106">Numéro de passeport</span></span>
- <span data-ttu-id="cc14d-1107">Passeport n °</span><span class="sxs-lookup"><span data-stu-id="cc14d-1107">Passeport n °</span></span>
- <span data-ttu-id="cc14d-1108">Passeport Non</span><span class="sxs-lookup"><span data-stu-id="cc14d-1108">Passeport Non</span></span>
- <span data-ttu-id="cc14d-1109">Passeport #</span><span class="sxs-lookup"><span data-stu-id="cc14d-1109">Passeport #</span></span>
- <span data-ttu-id="cc14d-1110">Passeport #</span><span class="sxs-lookup"><span data-stu-id="cc14d-1110">Passeport#</span></span>
- <span data-ttu-id="cc14d-1111">PasseportNon</span><span class="sxs-lookup"><span data-stu-id="cc14d-1111">PasseportNon</span></span>
- <span data-ttu-id="cc14d-1112">Passeportn °</span><span class="sxs-lookup"><span data-stu-id="cc14d-1112">Passeportn °</span></span>
   
## <a name="canada-personal-health-identification-number-phin"></a><span data-ttu-id="cc14d-1113">Número de identificação pessoal de saúde do Canadá (PHIN)</span><span class="sxs-lookup"><span data-stu-id="cc14d-1113">Canada Personal Health Identification Number (PHIN)</span></span>

### <a name="format"></a><span data-ttu-id="cc14d-1114">Format</span><span class="sxs-lookup"><span data-stu-id="cc14d-1114">Format</span></span>

<span data-ttu-id="cc14d-1115">Nove dígitos</span><span class="sxs-lookup"><span data-stu-id="cc14d-1115">Nine digits</span></span>

### <a name="pattern"></a><span data-ttu-id="cc14d-1116">Padrão</span><span class="sxs-lookup"><span data-stu-id="cc14d-1116">Pattern</span></span>

<span data-ttu-id="cc14d-1117">Nove dígitos</span><span class="sxs-lookup"><span data-stu-id="cc14d-1117">Nine digits</span></span>

### <a name="checksum"></a><span data-ttu-id="cc14d-1118">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="cc14d-1118">Checksum</span></span>

<span data-ttu-id="cc14d-1119">Não</span><span class="sxs-lookup"><span data-stu-id="cc14d-1119">No</span></span>

### <a name="definition"></a><span data-ttu-id="cc14d-1120">Definição</span><span class="sxs-lookup"><span data-stu-id="cc14d-1120">Definition</span></span>

<span data-ttu-id="cc14d-1121">Uma política de DLP é de 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres: a expressão regular Regex_canada_phin localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="cc14d-1121">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters: The regular expression Regex_canada_phin finds content that matches the pattern.</span></span>
<span data-ttu-id="cc14d-1122">São encontradas pelo menos duas palavras-chave do Keyword_canada_phin ou do Keyword_canada_provinces..</span><span class="sxs-lookup"><span data-stu-id="cc14d-1122">At least two keywords from Keyword_canada_phin or Keyword_canada_provinces are found..</span></span>

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

### <a name="keywords"></a><span data-ttu-id="cc14d-1123">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="cc14d-1123">Keywords</span></span>

#### <a name="keywordcanadaphin"></a><span data-ttu-id="cc14d-1124">Keyword_canada_phin</span><span class="sxs-lookup"><span data-stu-id="cc14d-1124">Keyword_canada_phin</span></span>

- <span data-ttu-id="cc14d-1125">social insurance number</span><span class="sxs-lookup"><span data-stu-id="cc14d-1125">social insurance number</span></span>
- <span data-ttu-id="cc14d-1126">health information act</span><span class="sxs-lookup"><span data-stu-id="cc14d-1126">health information act</span></span>
- <span data-ttu-id="cc14d-1127">income tax information</span><span class="sxs-lookup"><span data-stu-id="cc14d-1127">income tax information</span></span>
- <span data-ttu-id="cc14d-1128">manitoba health</span><span class="sxs-lookup"><span data-stu-id="cc14d-1128">manitoba health</span></span>
- <span data-ttu-id="cc14d-1129">health registration</span><span class="sxs-lookup"><span data-stu-id="cc14d-1129">health registration</span></span>
- <span data-ttu-id="cc14d-1130">prescription purchases</span><span class="sxs-lookup"><span data-stu-id="cc14d-1130">prescription purchases</span></span>
- <span data-ttu-id="cc14d-1131">benefit eligibility</span><span class="sxs-lookup"><span data-stu-id="cc14d-1131">benefit eligibility</span></span>
- <span data-ttu-id="cc14d-1132">personal health</span><span class="sxs-lookup"><span data-stu-id="cc14d-1132">personal health</span></span>
- <span data-ttu-id="cc14d-1133">power of attorney</span><span class="sxs-lookup"><span data-stu-id="cc14d-1133">power of attorney</span></span>
- <span data-ttu-id="cc14d-1134">registration number</span><span class="sxs-lookup"><span data-stu-id="cc14d-1134">registration number</span></span>
- <span data-ttu-id="cc14d-1135">personal health number</span><span class="sxs-lookup"><span data-stu-id="cc14d-1135">personal health number</span></span>
- <span data-ttu-id="cc14d-1136">practitioner referral</span><span class="sxs-lookup"><span data-stu-id="cc14d-1136">practitioner referral</span></span>
- <span data-ttu-id="cc14d-1137">wellness professional</span><span class="sxs-lookup"><span data-stu-id="cc14d-1137">wellness professional</span></span>
- <span data-ttu-id="cc14d-1138">patient referral</span><span class="sxs-lookup"><span data-stu-id="cc14d-1138">patient referral</span></span>
- <span data-ttu-id="cc14d-1139">health and wellness</span><span class="sxs-lookup"><span data-stu-id="cc14d-1139">health and wellness</span></span>

#### <a name="keywordcanadaprovinces"></a><span data-ttu-id="cc14d-1140">Keyword_canada_provinces</span><span class="sxs-lookup"><span data-stu-id="cc14d-1140">Keyword_canada_provinces</span></span>

- <span data-ttu-id="cc14d-1141">Nunavut</span><span class="sxs-lookup"><span data-stu-id="cc14d-1141">Nunavut</span></span>
- <span data-ttu-id="cc14d-1142">Quebec</span><span class="sxs-lookup"><span data-stu-id="cc14d-1142">Quebec</span></span>
- <span data-ttu-id="cc14d-1143">Northwest Territories</span><span class="sxs-lookup"><span data-stu-id="cc14d-1143">Northwest Territories</span></span>
- <span data-ttu-id="cc14d-1144">Ontário</span><span class="sxs-lookup"><span data-stu-id="cc14d-1144">Ontario</span></span>
- <span data-ttu-id="cc14d-1145">British Columbia</span><span class="sxs-lookup"><span data-stu-id="cc14d-1145">British Columbia</span></span>
- <span data-ttu-id="cc14d-1146">Alberta</span><span class="sxs-lookup"><span data-stu-id="cc14d-1146">Alberta</span></span>
- <span data-ttu-id="cc14d-1147">Saskatchewan</span><span class="sxs-lookup"><span data-stu-id="cc14d-1147">Saskatchewan</span></span>
- <span data-ttu-id="cc14d-1148">Manitoba</span><span class="sxs-lookup"><span data-stu-id="cc14d-1148">Manitoba</span></span>
- <span data-ttu-id="cc14d-1149">Yukon</span><span class="sxs-lookup"><span data-stu-id="cc14d-1149">Yukon</span></span>
- <span data-ttu-id="cc14d-1150">Newfoundland and Labrador</span><span class="sxs-lookup"><span data-stu-id="cc14d-1150">Newfoundland and Labrador</span></span>
- <span data-ttu-id="cc14d-1151">New Brunswick</span><span class="sxs-lookup"><span data-stu-id="cc14d-1151">New Brunswick</span></span>
- <span data-ttu-id="cc14d-1152">Nova Scotia</span><span class="sxs-lookup"><span data-stu-id="cc14d-1152">Nova Scotia</span></span>
- <span data-ttu-id="cc14d-1153">Prince Edward Island</span><span class="sxs-lookup"><span data-stu-id="cc14d-1153">Prince Edward Island</span></span>
- <span data-ttu-id="cc14d-1154">Canadá</span><span class="sxs-lookup"><span data-stu-id="cc14d-1154">Canada</span></span>
   
## <a name="canada-social-insurance-number"></a><span data-ttu-id="cc14d-1155">Número de seguro social do Canadá</span><span class="sxs-lookup"><span data-stu-id="cc14d-1155">Canada Social Insurance Number</span></span>

### <a name="format"></a><span data-ttu-id="cc14d-1156">Format</span><span class="sxs-lookup"><span data-stu-id="cc14d-1156">Format</span></span>

<span data-ttu-id="cc14d-1157">Nove dígitos com espaços ou hífens opcionais</span><span class="sxs-lookup"><span data-stu-id="cc14d-1157">Nine digits with optional hyphens or spaces</span></span>

### <a name="pattern"></a><span data-ttu-id="cc14d-1158">Padrão</span><span class="sxs-lookup"><span data-stu-id="cc14d-1158">Pattern</span></span>

<span data-ttu-id="cc14d-1159">Binário</span><span class="sxs-lookup"><span data-stu-id="cc14d-1159">Formatted:</span></span>
- <span data-ttu-id="cc14d-1160">Três dígitos</span><span class="sxs-lookup"><span data-stu-id="cc14d-1160">Three digits</span></span> 
- <span data-ttu-id="cc14d-1161">Um hífen ou espaço</span><span class="sxs-lookup"><span data-stu-id="cc14d-1161">A hyphen or space</span></span> 
- <span data-ttu-id="cc14d-1162">Três dígitos</span><span class="sxs-lookup"><span data-stu-id="cc14d-1162">Three digits</span></span> 
- <span data-ttu-id="cc14d-1163">Um hífen ou espaço</span><span class="sxs-lookup"><span data-stu-id="cc14d-1163">A hyphen or space</span></span> 
- <span data-ttu-id="cc14d-1164">Três dígitos</span><span class="sxs-lookup"><span data-stu-id="cc14d-1164">Three digits</span></span>

<span data-ttu-id="cc14d-1165">Não formatado: nove dígitos</span><span class="sxs-lookup"><span data-stu-id="cc14d-1165">Unformatted: Nine digits</span></span>

### <a name="checksum"></a><span data-ttu-id="cc14d-1166">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="cc14d-1166">Checksum</span></span>

<span data-ttu-id="cc14d-1167">Sim</span><span class="sxs-lookup"><span data-stu-id="cc14d-1167">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="cc14d-1168">Definição</span><span class="sxs-lookup"><span data-stu-id="cc14d-1168">Definition</span></span>

<span data-ttu-id="cc14d-1169">Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="cc14d-1169">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="cc14d-1170">A função Func_canadian_sin localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="cc14d-1170">The function Func_canadian_sin finds content that matches the pattern.</span></span>
- <span data-ttu-id="cc14d-1171">Pelo menos duas de qualquer combinação do seguinte:</span><span class="sxs-lookup"><span data-stu-id="cc14d-1171">At least two of any combination of the following:</span></span>
    - <span data-ttu-id="cc14d-1172">Uma palavra-chave de Keyword_sin for encontrada.</span><span class="sxs-lookup"><span data-stu-id="cc14d-1172">A keyword from Keyword_sin is found.</span></span>
    - <span data-ttu-id="cc14d-1173">Uma palavra-chave de Keyword_sin_collaborative for encontrada.</span><span class="sxs-lookup"><span data-stu-id="cc14d-1173">A keyword from Keyword_sin_collaborative is found.</span></span>
    - <span data-ttu-id="cc14d-1174">A função Func_eu_date encontra uma data no formato de data à direita.</span><span class="sxs-lookup"><span data-stu-id="cc14d-1174">The function Func_eu_date finds a date in the right date format.</span></span>
- <span data-ttu-id="cc14d-1175">A soma de verificação passa.</span><span class="sxs-lookup"><span data-stu-id="cc14d-1175">The checksum passes.</span></span>

<span data-ttu-id="cc14d-1176">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="cc14d-1176">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="cc14d-1177">A função Func_unformatted_canadian_sin localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="cc14d-1177">The function Func_unformatted_canadian_sin finds content that matches the pattern.</span></span>
- <span data-ttu-id="cc14d-1178">Uma palavra-chave de Keyword_sin for encontrada.</span><span class="sxs-lookup"><span data-stu-id="cc14d-1178">A keyword from Keyword_sin is found.</span></span>
- <span data-ttu-id="cc14d-1179">A soma de verificação passa.</span><span class="sxs-lookup"><span data-stu-id="cc14d-1179">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="cc14d-1180">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="cc14d-1180">Keywords</span></span>

#### <a name="keywordsin"></a><span data-ttu-id="cc14d-1181">Keyword_sin</span><span class="sxs-lookup"><span data-stu-id="cc14d-1181">Keyword_sin</span></span>

- <span data-ttu-id="cc14d-1182">sin</span><span class="sxs-lookup"><span data-stu-id="cc14d-1182">sin</span></span> 
- <span data-ttu-id="cc14d-1183">social insurance</span><span class="sxs-lookup"><span data-stu-id="cc14d-1183">social insurance</span></span> 
- <span data-ttu-id="cc14d-1184">numero d'assurance sociale</span><span class="sxs-lookup"><span data-stu-id="cc14d-1184">numero d'assurance sociale</span></span> 
- <span data-ttu-id="cc14d-1185">capitais</span><span class="sxs-lookup"><span data-stu-id="cc14d-1185">sins</span></span> 
- <span data-ttu-id="cc14d-1186">es</span><span class="sxs-lookup"><span data-stu-id="cc14d-1186">ssn</span></span> 
- <span data-ttu-id="cc14d-1187">CPFs</span><span class="sxs-lookup"><span data-stu-id="cc14d-1187">ssns</span></span> 
- <span data-ttu-id="cc14d-1188">social security</span><span class="sxs-lookup"><span data-stu-id="cc14d-1188">social security</span></span> 
- <span data-ttu-id="cc14d-1189">numero d'assurance social</span><span class="sxs-lookup"><span data-stu-id="cc14d-1189">numero d'assurance social</span></span> 
- <span data-ttu-id="cc14d-1190">national identification number</span><span class="sxs-lookup"><span data-stu-id="cc14d-1190">national identification number</span></span> 
- <span data-ttu-id="cc14d-1191">national id</span><span class="sxs-lookup"><span data-stu-id="cc14d-1191">national id</span></span> 
- <span data-ttu-id="cc14d-1192">Sin</span><span class="sxs-lookup"><span data-stu-id="cc14d-1192">sin#</span></span> 
- <span data-ttu-id="cc14d-1193">soc ins</span><span class="sxs-lookup"><span data-stu-id="cc14d-1193">soc ins</span></span> 
- <span data-ttu-id="cc14d-1194">social ins</span><span class="sxs-lookup"><span data-stu-id="cc14d-1194">social ins</span></span> 

#### <a name="keywordsincollaborative"></a><span data-ttu-id="cc14d-1195">Keyword_sin_collaborative</span><span class="sxs-lookup"><span data-stu-id="cc14d-1195">Keyword_sin_collaborative</span></span>

- <span data-ttu-id="cc14d-1196">driver's license</span><span class="sxs-lookup"><span data-stu-id="cc14d-1196">driver's license</span></span> 
- <span data-ttu-id="cc14d-1197">drivers license</span><span class="sxs-lookup"><span data-stu-id="cc14d-1197">drivers license</span></span> 
- <span data-ttu-id="cc14d-1198">driver's licence</span><span class="sxs-lookup"><span data-stu-id="cc14d-1198">driver's licence</span></span> 
- <span data-ttu-id="cc14d-1199">drivers licence</span><span class="sxs-lookup"><span data-stu-id="cc14d-1199">drivers licence</span></span> 
- <span data-ttu-id="cc14d-1200">DOB</span><span class="sxs-lookup"><span data-stu-id="cc14d-1200">DOB</span></span> 
- <span data-ttu-id="cc14d-1201">Data de Nascimento</span><span class="sxs-lookup"><span data-stu-id="cc14d-1201">Birthdate</span></span> 
- <span data-ttu-id="cc14d-1202">Aniversário</span><span class="sxs-lookup"><span data-stu-id="cc14d-1202">Birthday</span></span> 
- <span data-ttu-id="cc14d-1203">Date of Birth</span><span class="sxs-lookup"><span data-stu-id="cc14d-1203">Date of Birth</span></span> 
   
## <a name="chile-identity-card-number"></a><span data-ttu-id="cc14d-1204">	Número do Cartão de Identidade do Chile</span><span class="sxs-lookup"><span data-stu-id="cc14d-1204">Chile Identity Card Number</span></span>

### <a name="format"></a><span data-ttu-id="cc14d-1205">Format</span><span class="sxs-lookup"><span data-stu-id="cc14d-1205">Format</span></span>

<span data-ttu-id="cc14d-1206">7-8 dígitos mais delimitadores um dígito ou letra de verificação</span><span class="sxs-lookup"><span data-stu-id="cc14d-1206">7-8 digits plus delimiters a check digit or letter</span></span>

### <a name="pattern"></a><span data-ttu-id="cc14d-1207">Padrão</span><span class="sxs-lookup"><span data-stu-id="cc14d-1207">Pattern</span></span>

<span data-ttu-id="cc14d-1208">7 a 8 dígitos mais delimitadores:</span><span class="sxs-lookup"><span data-stu-id="cc14d-1208">7-8 digits plus delimiters:</span></span>
- <span data-ttu-id="cc14d-1209">1 a 2 dígitos</span><span class="sxs-lookup"><span data-stu-id="cc14d-1209">1-2 digits</span></span> 
- <span data-ttu-id="cc14d-1210">Um ponto </span><span class="sxs-lookup"><span data-stu-id="cc14d-1210">A period</span></span> 
- <span data-ttu-id="cc14d-1211">Três dígitos</span><span class="sxs-lookup"><span data-stu-id="cc14d-1211">Three digits</span></span> 
- <span data-ttu-id="cc14d-1212">Um ponto </span><span class="sxs-lookup"><span data-stu-id="cc14d-1212">A period</span></span> 
- <span data-ttu-id="cc14d-1213">Três dígitos</span><span class="sxs-lookup"><span data-stu-id="cc14d-1213">Three digits</span></span> 
- <span data-ttu-id="cc14d-1214">Um traço</span><span class="sxs-lookup"><span data-stu-id="cc14d-1214">A dash</span></span> 
- <span data-ttu-id="cc14d-1215">Um dígito ou letra (não diferencia maiúscula de minúscula) que é um dígito de verificação</span><span class="sxs-lookup"><span data-stu-id="cc14d-1215">One digit or letter (not case sensitive) which is a check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="cc14d-1216">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="cc14d-1216">Checksum</span></span>

<span data-ttu-id="cc14d-1217">Sim</span><span class="sxs-lookup"><span data-stu-id="cc14d-1217">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="cc14d-1218">Definição</span><span class="sxs-lookup"><span data-stu-id="cc14d-1218">Definition</span></span>

<span data-ttu-id="cc14d-1219">Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="cc14d-1219">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="cc14d-1220">A função Func_chile_id_card localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="cc14d-1220">The function Func_chile_id_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="cc14d-1221">Uma palavra-chave de Keyword_chile_id_card for encontrada.</span><span class="sxs-lookup"><span data-stu-id="cc14d-1221">A keyword from Keyword_chile_id_card is found.</span></span>
- <span data-ttu-id="cc14d-1222">A soma de verificação passa.</span><span class="sxs-lookup"><span data-stu-id="cc14d-1222">The checksum passes.</span></span>

<span data-ttu-id="cc14d-1223">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="cc14d-1223">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="cc14d-1224">A função Func_chile_id_card localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="cc14d-1224">The function Func_chile_id_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="cc14d-1225">A soma de verificação passa.</span><span class="sxs-lookup"><span data-stu-id="cc14d-1225">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="cc14d-1226">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="cc14d-1226">Keywords</span></span>

#### <a name="keywordchileidcard"></a><span data-ttu-id="cc14d-1227">Keyword_chile_id_card</span><span class="sxs-lookup"><span data-stu-id="cc14d-1227">Keyword_chile_id_card</span></span>

- <span data-ttu-id="cc14d-1228">Número de Identificação Nacional</span><span class="sxs-lookup"><span data-stu-id="cc14d-1228">National Identification Number</span></span> 
- <span data-ttu-id="cc14d-1229">Cartão de identidade</span><span class="sxs-lookup"><span data-stu-id="cc14d-1229">Identity card</span></span> 
- <span data-ttu-id="cc14d-1230">ID</span><span class="sxs-lookup"><span data-stu-id="cc14d-1230">ID</span></span> 
- <span data-ttu-id="cc14d-1231">Identificador</span><span class="sxs-lookup"><span data-stu-id="cc14d-1231">Identification</span></span> 
- <span data-ttu-id="cc14d-1232">Rol Único Nacional</span><span class="sxs-lookup"><span data-stu-id="cc14d-1232">Rol Único Nacional</span></span> 
- <span data-ttu-id="cc14d-1233">SEJAM</span><span class="sxs-lookup"><span data-stu-id="cc14d-1233">RUN</span></span> 
- <span data-ttu-id="cc14d-1234">Rol Único Tributario</span><span class="sxs-lookup"><span data-stu-id="cc14d-1234">Rol Único Tributario</span></span> 
- <span data-ttu-id="cc14d-1235">ROTINA</span><span class="sxs-lookup"><span data-stu-id="cc14d-1235">RUT</span></span> 
- <span data-ttu-id="cc14d-1236">Cédula de Identidad</span><span class="sxs-lookup"><span data-stu-id="cc14d-1236">Cédula de Identidad</span></span> 
- <span data-ttu-id="cc14d-1237">Número De Identificación Nacional</span><span class="sxs-lookup"><span data-stu-id="cc14d-1237">Número De Identificación Nacional</span></span> 
- <span data-ttu-id="cc14d-1238">Tarjeta de identificación</span><span class="sxs-lookup"><span data-stu-id="cc14d-1238">Tarjeta de identificación</span></span> 
- <span data-ttu-id="cc14d-1239">Identificación</span><span class="sxs-lookup"><span data-stu-id="cc14d-1239">Identificación</span></span> 
   
## <a name="china-resident-identity-card-prc-number"></a><span data-ttu-id="cc14d-1240">	Número do Cartão de Identidade de Residentes (PRC) da China</span><span class="sxs-lookup"><span data-stu-id="cc14d-1240">China Resident Identity Card (PRC) Number</span></span>

### <a name="format"></a><span data-ttu-id="cc14d-1241">Format</span><span class="sxs-lookup"><span data-stu-id="cc14d-1241">Format</span></span>

<span data-ttu-id="cc14d-1242">18 dígitos</span><span class="sxs-lookup"><span data-stu-id="cc14d-1242">18 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="cc14d-1243">Padrão</span><span class="sxs-lookup"><span data-stu-id="cc14d-1243">Pattern</span></span>

<span data-ttu-id="cc14d-1244">18 dígitos:</span><span class="sxs-lookup"><span data-stu-id="cc14d-1244">18 digits:</span></span>
- <span data-ttu-id="cc14d-1245">Seis dígitos que são um código de endereço </span><span class="sxs-lookup"><span data-stu-id="cc14d-1245">Six digits which are an address code</span></span> 
- <span data-ttu-id="cc14d-1246">Oito dígitos no formato AAAAMMDD que são a data de nascimento </span><span class="sxs-lookup"><span data-stu-id="cc14d-1246">Eight digits in the form YYYYMMDD which are the date of birth</span></span> 
- <span data-ttu-id="cc14d-1247">Três dígitos que são um código de pedido </span><span class="sxs-lookup"><span data-stu-id="cc14d-1247">Three digits which are an order code</span></span> 
- <span data-ttu-id="cc14d-1248">Um dígito que é um dígito de verificação</span><span class="sxs-lookup"><span data-stu-id="cc14d-1248">One digit which is a check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="cc14d-1249">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="cc14d-1249">Checksum</span></span>

<span data-ttu-id="cc14d-1250">Sim</span><span class="sxs-lookup"><span data-stu-id="cc14d-1250">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="cc14d-1251">Definição</span><span class="sxs-lookup"><span data-stu-id="cc14d-1251">Definition</span></span>

<span data-ttu-id="cc14d-1252">Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="cc14d-1252">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="cc14d-1253">A função Func_china_resident_id localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="cc14d-1253">The function Func_china_resident_id finds content that matches the pattern.</span></span>
- <span data-ttu-id="cc14d-1254">Uma palavra-chave de Keyword_china_resident_id for encontrada.</span><span class="sxs-lookup"><span data-stu-id="cc14d-1254">A keyword from Keyword_china_resident_id is found.</span></span>
- <span data-ttu-id="cc14d-1255">A soma de verificação passa.</span><span class="sxs-lookup"><span data-stu-id="cc14d-1255">The checksum passes.</span></span>

<span data-ttu-id="cc14d-1256">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="cc14d-1256">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="cc14d-1257">A função Func_china_resident_id localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="cc14d-1257">The function Func_china_resident_id finds content that matches the pattern.</span></span>
- <span data-ttu-id="cc14d-1258">A soma de verificação passa.</span><span class="sxs-lookup"><span data-stu-id="cc14d-1258">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="cc14d-1259">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="cc14d-1259">Keywords</span></span>

### <a name="keywordchinaresidentid"></a><span data-ttu-id="cc14d-1260">Keyword_china_resident_id</span><span class="sxs-lookup"><span data-stu-id="cc14d-1260">Keyword_china_resident_id</span></span>

- <span data-ttu-id="cc14d-1261">Cartão de Identidade da Polônia</span><span class="sxs-lookup"><span data-stu-id="cc14d-1261">Resident Identity Card</span></span> 
- <span data-ttu-id="cc14d-1262">POPULAR</span><span class="sxs-lookup"><span data-stu-id="cc14d-1262">PRC</span></span> 
- <span data-ttu-id="cc14d-1263">Cartão de Identificação Nacional</span><span class="sxs-lookup"><span data-stu-id="cc14d-1263">National Identification Card</span></span> 
- <span data-ttu-id="cc14d-1264">身份证</span><span class="sxs-lookup"><span data-stu-id="cc14d-1264">身份证</span></span> 
- <span data-ttu-id="cc14d-1265">居民 身份证</span><span class="sxs-lookup"><span data-stu-id="cc14d-1265">居民 身份证</span></span> 
- <span data-ttu-id="cc14d-1266">居民身份证</span><span class="sxs-lookup"><span data-stu-id="cc14d-1266">居民身份证</span></span> 
- <span data-ttu-id="cc14d-1267">鉴定</span><span class="sxs-lookup"><span data-stu-id="cc14d-1267">鉴定</span></span> 
- <span data-ttu-id="cc14d-1268">身分證</span><span class="sxs-lookup"><span data-stu-id="cc14d-1268">身分證</span></span> 
- <span data-ttu-id="cc14d-1269">居民 身份證</span><span class="sxs-lookup"><span data-stu-id="cc14d-1269">居民 身份證</span></span>
- <span data-ttu-id="cc14d-1270">鑑定</span><span class="sxs-lookup"><span data-stu-id="cc14d-1270">鑑定</span></span> 
   
## <a name="credit-card-number"></a><span data-ttu-id="cc14d-1271">Credit Card Number</span><span class="sxs-lookup"><span data-stu-id="cc14d-1271">Credit Card Number</span></span>

### <a name="format"></a><span data-ttu-id="cc14d-1272">Format</span><span class="sxs-lookup"><span data-stu-id="cc14d-1272">Format</span></span>

<span data-ttu-id="cc14d-1273">16 dígitos que podem ser formatados ou não formatados (dddddddddddddddd) e devem passar no teste Luhn.</span><span class="sxs-lookup"><span data-stu-id="cc14d-1273">16 digits which can be formatted or unformatted (dddddddddddddddd) and must pass the Luhn test.</span></span>

### <a name="pattern"></a><span data-ttu-id="cc14d-1274">Padrão</span><span class="sxs-lookup"><span data-stu-id="cc14d-1274">Pattern</span></span>

<span data-ttu-id="cc14d-1275">Padrão muito complexo e robusto que detecta cartões de todas as principais marcas em todo o mundo, incluindo Visa, MasterCard, Discover Card, JCB, American Express, vales-presentes e cartões diner.</span><span class="sxs-lookup"><span data-stu-id="cc14d-1275">Very complex and robust pattern that detects cards from all major brands worldwide, including Visa, MasterCard, Discover Card, JCB, American Express, gift cards, and diner cards.</span></span>

### <a name="checksum"></a><span data-ttu-id="cc14d-1276">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="cc14d-1276">Checksum</span></span>

<span data-ttu-id="cc14d-1277">Sim, a soma de verificação Luhn</span><span class="sxs-lookup"><span data-stu-id="cc14d-1277">Yes, the Luhn checksum</span></span>

### <a name="definition"></a><span data-ttu-id="cc14d-1278">Definição</span><span class="sxs-lookup"><span data-stu-id="cc14d-1278">Definition</span></span>

<span data-ttu-id="cc14d-1279">Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="cc14d-1279">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="cc14d-1280">A função Func_credit_card localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="cc14d-1280">The function Func_credit_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="cc14d-1281">Uma das seguintes opções for verdadeira:</span><span class="sxs-lookup"><span data-stu-id="cc14d-1281">One of the following is true:</span></span>
    - <span data-ttu-id="cc14d-1282">Uma palavra-chave de Keyword_cc_verification for encontrada.</span><span class="sxs-lookup"><span data-stu-id="cc14d-1282">A keyword from Keyword_cc_verification is found.</span></span>
    - <span data-ttu-id="cc14d-1283">Uma palavra-chave de Keyword_cc_name for encontrada.</span><span class="sxs-lookup"><span data-stu-id="cc14d-1283">A keyword from Keyword_cc_name is found.</span></span>
    - <span data-ttu-id="cc14d-1284">A função Func_expiration_date encontra uma data no formato de data à direita.</span><span class="sxs-lookup"><span data-stu-id="cc14d-1284">The function Func_expiration_date finds a date in the right date format.</span></span>
- <span data-ttu-id="cc14d-1285">A soma de verificação passa.</span><span class="sxs-lookup"><span data-stu-id="cc14d-1285">The checksum passes.</span></span>

<span data-ttu-id="cc14d-1286">Uma política de DLP tem 65% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="cc14d-1286">A DLP policy is 65% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="cc14d-1287">A função Func_credit_card localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="cc14d-1287">The function Func_credit_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="cc14d-1288">A soma de verificação passa.</span><span class="sxs-lookup"><span data-stu-id="cc14d-1288">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="cc14d-1289">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="cc14d-1289">Keywords</span></span>

#### <a name="keywordccverification"></a><span data-ttu-id="cc14d-1290">Keyword_cc_verification</span><span class="sxs-lookup"><span data-stu-id="cc14d-1290">Keyword_cc_verification</span></span>

- <span data-ttu-id="cc14d-1291">card verification</span><span class="sxs-lookup"><span data-stu-id="cc14d-1291">card verification</span></span>
- <span data-ttu-id="cc14d-1292">card identification number</span><span class="sxs-lookup"><span data-stu-id="cc14d-1292">card identification number</span></span>
- <span data-ttu-id="cc14d-1293">CVN</span><span class="sxs-lookup"><span data-stu-id="cc14d-1293">cvn</span></span>
- <span data-ttu-id="cc14d-1294">CID</span><span class="sxs-lookup"><span data-stu-id="cc14d-1294">cid</span></span>
- <span data-ttu-id="cc14d-1295">CVC2</span><span class="sxs-lookup"><span data-stu-id="cc14d-1295">cvc2</span></span>
- <span data-ttu-id="cc14d-1296">CVV2</span><span class="sxs-lookup"><span data-stu-id="cc14d-1296">cvv2</span></span>
- <span data-ttu-id="cc14d-1297">pin block</span><span class="sxs-lookup"><span data-stu-id="cc14d-1297">pin block</span></span>
- <span data-ttu-id="cc14d-1298">security code</span><span class="sxs-lookup"><span data-stu-id="cc14d-1298">security code</span></span>
- <span data-ttu-id="cc14d-1299">security number</span><span class="sxs-lookup"><span data-stu-id="cc14d-1299">security number</span></span>
- <span data-ttu-id="cc14d-1300">security no</span><span class="sxs-lookup"><span data-stu-id="cc14d-1300">security no</span></span>
- <span data-ttu-id="cc14d-1301">issue number</span><span class="sxs-lookup"><span data-stu-id="cc14d-1301">issue number</span></span>
- <span data-ttu-id="cc14d-1302">issue no</span><span class="sxs-lookup"><span data-stu-id="cc14d-1302">issue no</span></span>
- <span data-ttu-id="cc14d-1303">cryptogramme</span><span class="sxs-lookup"><span data-stu-id="cc14d-1303">cryptogramme</span></span>
- <span data-ttu-id="cc14d-1304">numéro de sécurité</span><span class="sxs-lookup"><span data-stu-id="cc14d-1304">numéro de sécurité</span></span>
- <span data-ttu-id="cc14d-1305">numero de securite</span><span class="sxs-lookup"><span data-stu-id="cc14d-1305">numero de securite</span></span>
- <span data-ttu-id="cc14d-1306">kreditkartenprüfnummer</span><span class="sxs-lookup"><span data-stu-id="cc14d-1306">kreditkartenprüfnummer</span></span>
- <span data-ttu-id="cc14d-1307">kreditkartenprufnummer</span><span class="sxs-lookup"><span data-stu-id="cc14d-1307">kreditkartenprufnummer</span></span>
- <span data-ttu-id="cc14d-1308">prüfziffer</span><span class="sxs-lookup"><span data-stu-id="cc14d-1308">prüfziffer</span></span>
- <span data-ttu-id="cc14d-1309">prufziffer</span><span class="sxs-lookup"><span data-stu-id="cc14d-1309">prufziffer</span></span>
- <span data-ttu-id="cc14d-1310">sicherheits Kode</span><span class="sxs-lookup"><span data-stu-id="cc14d-1310">sicherheits Kode</span></span>
- <span data-ttu-id="cc14d-1311">sicherheitscode</span><span class="sxs-lookup"><span data-stu-id="cc14d-1311">sicherheitscode</span></span>
- <span data-ttu-id="cc14d-1312">sicherheitsnummer</span><span class="sxs-lookup"><span data-stu-id="cc14d-1312">sicherheitsnummer</span></span>
- <span data-ttu-id="cc14d-1313">verfalldatum</span><span class="sxs-lookup"><span data-stu-id="cc14d-1313">verfalldatum</span></span>
- <span data-ttu-id="cc14d-1314">codice di verifica</span><span class="sxs-lookup"><span data-stu-id="cc14d-1314">codice di verifica</span></span>
- <span data-ttu-id="cc14d-1315">COD.</span><span class="sxs-lookup"><span data-stu-id="cc14d-1315">cod.</span></span> <span data-ttu-id="cc14d-1316">sicurezza</span><span class="sxs-lookup"><span data-stu-id="cc14d-1316">sicurezza</span></span>
- <span data-ttu-id="cc14d-1317">cod sicurezza</span><span class="sxs-lookup"><span data-stu-id="cc14d-1317">cod sicurezza</span></span>
- <span data-ttu-id="cc14d-1318">n autorizzazione</span><span class="sxs-lookup"><span data-stu-id="cc14d-1318">n autorizzazione</span></span>
- <span data-ttu-id="cc14d-1319">CFOP</span><span class="sxs-lookup"><span data-stu-id="cc14d-1319">código</span></span>
- <span data-ttu-id="cc14d-1320">codigo</span><span class="sxs-lookup"><span data-stu-id="cc14d-1320">codigo</span></span>
- <span data-ttu-id="cc14d-1321">COD.</span><span class="sxs-lookup"><span data-stu-id="cc14d-1321">cod.</span></span> <span data-ttu-id="cc14d-1322">seg</span><span class="sxs-lookup"><span data-stu-id="cc14d-1322">seg</span></span>
- <span data-ttu-id="cc14d-1323">cod seg</span><span class="sxs-lookup"><span data-stu-id="cc14d-1323">cod seg</span></span>
- <span data-ttu-id="cc14d-1324">código de segurança</span><span class="sxs-lookup"><span data-stu-id="cc14d-1324">código de segurança</span></span>
- <span data-ttu-id="cc14d-1325">codigo de seguranca</span><span class="sxs-lookup"><span data-stu-id="cc14d-1325">codigo de seguranca</span></span>
- <span data-ttu-id="cc14d-1326">codigo de segurança</span><span class="sxs-lookup"><span data-stu-id="cc14d-1326">codigo de segurança</span></span>
- <span data-ttu-id="cc14d-1327">código de seguranca</span><span class="sxs-lookup"><span data-stu-id="cc14d-1327">código de seguranca</span></span>
- <span data-ttu-id="cc14d-1328">Cód.</span><span class="sxs-lookup"><span data-stu-id="cc14d-1328">cód.</span></span> <span data-ttu-id="cc14d-1329">segurança</span><span class="sxs-lookup"><span data-stu-id="cc14d-1329">segurança</span></span>
- <span data-ttu-id="cc14d-1330">COD.</span><span class="sxs-lookup"><span data-stu-id="cc14d-1330">cod.</span></span> <span data-ttu-id="cc14d-1331">seguranca Cod.</span><span class="sxs-lookup"><span data-stu-id="cc14d-1331">seguranca cod.</span></span> <span data-ttu-id="cc14d-1332">segurança</span><span class="sxs-lookup"><span data-stu-id="cc14d-1332">segurança</span></span>
- <span data-ttu-id="cc14d-1333">Cód.</span><span class="sxs-lookup"><span data-stu-id="cc14d-1333">cód.</span></span> <span data-ttu-id="cc14d-1334">seguranca</span><span class="sxs-lookup"><span data-stu-id="cc14d-1334">seguranca</span></span>
- <span data-ttu-id="cc14d-1335">cód segurança</span><span class="sxs-lookup"><span data-stu-id="cc14d-1335">cód segurança</span></span>
- <span data-ttu-id="cc14d-1336">COD seguranca COD segurança</span><span class="sxs-lookup"><span data-stu-id="cc14d-1336">cod seguranca cod segurança</span></span>
- <span data-ttu-id="cc14d-1337">cód seguranca</span><span class="sxs-lookup"><span data-stu-id="cc14d-1337">cód seguranca</span></span>
- <span data-ttu-id="cc14d-1338">número de verificação</span><span class="sxs-lookup"><span data-stu-id="cc14d-1338">número de verificação</span></span>
- <span data-ttu-id="cc14d-1339">numero de verificacao</span><span class="sxs-lookup"><span data-stu-id="cc14d-1339">numero de verificacao</span></span>
- <span data-ttu-id="cc14d-1340">ablauf</span><span class="sxs-lookup"><span data-stu-id="cc14d-1340">ablauf</span></span>
- <span data-ttu-id="cc14d-1341">gültig bis</span><span class="sxs-lookup"><span data-stu-id="cc14d-1341">gültig bis</span></span>
- <span data-ttu-id="cc14d-1342">gültigkeitsdatum</span><span class="sxs-lookup"><span data-stu-id="cc14d-1342">gültigkeitsdatum</span></span>
- <span data-ttu-id="cc14d-1343">gultig bis</span><span class="sxs-lookup"><span data-stu-id="cc14d-1343">gultig bis</span></span>
- <span data-ttu-id="cc14d-1344">gultigkeitsdatum</span><span class="sxs-lookup"><span data-stu-id="cc14d-1344">gultigkeitsdatum</span></span>
- <span data-ttu-id="cc14d-1345">scadenza</span><span class="sxs-lookup"><span data-stu-id="cc14d-1345">scadenza</span></span>
- <span data-ttu-id="cc14d-1346">data scad</span><span class="sxs-lookup"><span data-stu-id="cc14d-1346">data scad</span></span>
- <span data-ttu-id="cc14d-1347">fecha de expiracion</span><span class="sxs-lookup"><span data-stu-id="cc14d-1347">fecha de expiracion</span></span>
- <span data-ttu-id="cc14d-1348">fecha de venc</span><span class="sxs-lookup"><span data-stu-id="cc14d-1348">fecha de venc</span></span>
- <span data-ttu-id="cc14d-1349">vencimiento</span><span class="sxs-lookup"><span data-stu-id="cc14d-1349">vencimiento</span></span>
- <span data-ttu-id="cc14d-1350">válido hasta</span><span class="sxs-lookup"><span data-stu-id="cc14d-1350">válido hasta</span></span>
- <span data-ttu-id="cc14d-1351">valido hasta</span><span class="sxs-lookup"><span data-stu-id="cc14d-1351">valido hasta</span></span>
- <span data-ttu-id="cc14d-1352">vto</span><span class="sxs-lookup"><span data-stu-id="cc14d-1352">vto</span></span>
- <span data-ttu-id="cc14d-1353">data de expiração</span><span class="sxs-lookup"><span data-stu-id="cc14d-1353">data de expiração</span></span>
- <span data-ttu-id="cc14d-1354">data de expiracao</span><span class="sxs-lookup"><span data-stu-id="cc14d-1354">data de expiracao</span></span>
- <span data-ttu-id="cc14d-1355">data em que expira</span><span class="sxs-lookup"><span data-stu-id="cc14d-1355">data em que expira</span></span>
- <span data-ttu-id="cc14d-1356">validade</span><span class="sxs-lookup"><span data-stu-id="cc14d-1356">validade</span></span>
- <span data-ttu-id="cc14d-1357">coragem</span><span class="sxs-lookup"><span data-stu-id="cc14d-1357">valor</span></span>
- <span data-ttu-id="cc14d-1358">vencimento</span><span class="sxs-lookup"><span data-stu-id="cc14d-1358">vencimento</span></span>
- <span data-ttu-id="cc14d-1359">Venc</span><span class="sxs-lookup"><span data-stu-id="cc14d-1359">Venc</span></span> 

#### <a name="keywordccname"></a><span data-ttu-id="cc14d-1360">Keyword_cc_name</span><span class="sxs-lookup"><span data-stu-id="cc14d-1360">Keyword_cc_name</span></span>

- <span data-ttu-id="cc14d-1361">Amex</span><span class="sxs-lookup"><span data-stu-id="cc14d-1361">amex</span></span>
- <span data-ttu-id="cc14d-1362">american express</span><span class="sxs-lookup"><span data-stu-id="cc14d-1362">american express</span></span>
- <span data-ttu-id="cc14d-1363">americanexpress</span><span class="sxs-lookup"><span data-stu-id="cc14d-1363">americanexpress</span></span>
- <span data-ttu-id="cc14d-1364">Cartões</span><span class="sxs-lookup"><span data-stu-id="cc14d-1364">Visa</span></span>
- <span data-ttu-id="cc14d-1365">MasterCard</span><span class="sxs-lookup"><span data-stu-id="cc14d-1365">mastercard</span></span>
- <span data-ttu-id="cc14d-1366">master card</span><span class="sxs-lookup"><span data-stu-id="cc14d-1366">master card</span></span>
- <span data-ttu-id="cc14d-1367">MC</span><span class="sxs-lookup"><span data-stu-id="cc14d-1367">mc</span></span> 
- <span data-ttu-id="cc14d-1368">MasterCards</span><span class="sxs-lookup"><span data-stu-id="cc14d-1368">mastercards</span></span>
- <span data-ttu-id="cc14d-1369">master cards</span><span class="sxs-lookup"><span data-stu-id="cc14d-1369">master cards</span></span>
- <span data-ttu-id="cc14d-1370">diner's Club</span><span class="sxs-lookup"><span data-stu-id="cc14d-1370">diner's Club</span></span>
- <span data-ttu-id="cc14d-1371">diners club</span><span class="sxs-lookup"><span data-stu-id="cc14d-1371">diners club</span></span>
- <span data-ttu-id="cc14d-1372">Dinersclub</span><span class="sxs-lookup"><span data-stu-id="cc14d-1372">dinersclub</span></span>
- <span data-ttu-id="cc14d-1373">discover card</span><span class="sxs-lookup"><span data-stu-id="cc14d-1373">discover card</span></span>
- <span data-ttu-id="cc14d-1374">DiscoverCard</span><span class="sxs-lookup"><span data-stu-id="cc14d-1374">discovercard</span></span>
- <span data-ttu-id="cc14d-1375">discover cards</span><span class="sxs-lookup"><span data-stu-id="cc14d-1375">discover cards</span></span>
- <span data-ttu-id="cc14d-1376">JCB</span><span class="sxs-lookup"><span data-stu-id="cc14d-1376">JCB</span></span>
- <span data-ttu-id="cc14d-1377">japanese card bureau</span><span class="sxs-lookup"><span data-stu-id="cc14d-1377">japanese card bureau</span></span>
- <span data-ttu-id="cc14d-1378">carte blanche</span><span class="sxs-lookup"><span data-stu-id="cc14d-1378">carte blanche</span></span>
- <span data-ttu-id="cc14d-1379">carteblanche</span><span class="sxs-lookup"><span data-stu-id="cc14d-1379">carteblanche</span></span>
- <span data-ttu-id="cc14d-1380">credit card</span><span class="sxs-lookup"><span data-stu-id="cc14d-1380">credit card</span></span>
- <span data-ttu-id="cc14d-1381">colocado</span><span class="sxs-lookup"><span data-stu-id="cc14d-1381">cc#</span></span>
- <span data-ttu-id="cc14d-1382">CC #:</span><span class="sxs-lookup"><span data-stu-id="cc14d-1382">cc#:</span></span>
- <span data-ttu-id="cc14d-1383">expiration date</span><span class="sxs-lookup"><span data-stu-id="cc14d-1383">expiration date</span></span>
- <span data-ttu-id="cc14d-1384">exp date</span><span class="sxs-lookup"><span data-stu-id="cc14d-1384">exp date</span></span>
- <span data-ttu-id="cc14d-1385">expiry date</span><span class="sxs-lookup"><span data-stu-id="cc14d-1385">expiry date</span></span>
- <span data-ttu-id="cc14d-1386">date d’expiration</span><span class="sxs-lookup"><span data-stu-id="cc14d-1386">date d’expiration</span></span>
- <span data-ttu-id="cc14d-1387">date d'exp</span><span class="sxs-lookup"><span data-stu-id="cc14d-1387">date d'exp</span></span>
- <span data-ttu-id="cc14d-1388">date expiration</span><span class="sxs-lookup"><span data-stu-id="cc14d-1388">date expiration</span></span>
- <span data-ttu-id="cc14d-1389">bank card</span><span class="sxs-lookup"><span data-stu-id="cc14d-1389">bank card</span></span>
- <span data-ttu-id="cc14d-1390">BankCard</span><span class="sxs-lookup"><span data-stu-id="cc14d-1390">bankcard</span></span>
- <span data-ttu-id="cc14d-1391">card number</span><span class="sxs-lookup"><span data-stu-id="cc14d-1391">card number</span></span>
- <span data-ttu-id="cc14d-1392">card num</span><span class="sxs-lookup"><span data-stu-id="cc14d-1392">card num</span></span>
- <span data-ttu-id="cc14d-1393">cardNumber</span><span class="sxs-lookup"><span data-stu-id="cc14d-1393">cardnumber</span></span>
- <span data-ttu-id="cc14d-1394">cardnumbers</span><span class="sxs-lookup"><span data-stu-id="cc14d-1394">cardnumbers</span></span>
- <span data-ttu-id="cc14d-1395">card numbers</span><span class="sxs-lookup"><span data-stu-id="cc14d-1395">card numbers</span></span>
- <span data-ttu-id="cc14d-1396">CreditCard</span><span class="sxs-lookup"><span data-stu-id="cc14d-1396">creditcard</span></span>
- <span data-ttu-id="cc14d-1397">credit cards</span><span class="sxs-lookup"><span data-stu-id="cc14d-1397">credit cards</span></span>
- <span data-ttu-id="cc14d-1398">CreditCards</span><span class="sxs-lookup"><span data-stu-id="cc14d-1398">creditcards</span></span>
- <span data-ttu-id="cc14d-1399">CCN</span><span class="sxs-lookup"><span data-stu-id="cc14d-1399">ccn</span></span>
- <span data-ttu-id="cc14d-1400">card holder</span><span class="sxs-lookup"><span data-stu-id="cc14d-1400">card holder</span></span>
- <span data-ttu-id="cc14d-1401">aos</span><span class="sxs-lookup"><span data-stu-id="cc14d-1401">cardholder</span></span>
- <span data-ttu-id="cc14d-1402">card holders</span><span class="sxs-lookup"><span data-stu-id="cc14d-1402">card holders</span></span>
- <span data-ttu-id="cc14d-1403">titulares de cartões</span><span class="sxs-lookup"><span data-stu-id="cc14d-1403">cardholders</span></span>
- <span data-ttu-id="cc14d-1404">check card</span><span class="sxs-lookup"><span data-stu-id="cc14d-1404">check card</span></span>
- <span data-ttu-id="cc14d-1405">checkcard</span><span class="sxs-lookup"><span data-stu-id="cc14d-1405">checkcard</span></span>
- <span data-ttu-id="cc14d-1406">check cards</span><span class="sxs-lookup"><span data-stu-id="cc14d-1406">check cards</span></span>
- <span data-ttu-id="cc14d-1407">checkcards</span><span class="sxs-lookup"><span data-stu-id="cc14d-1407">checkcards</span></span>
- <span data-ttu-id="cc14d-1408">debit card</span><span class="sxs-lookup"><span data-stu-id="cc14d-1408">debit card</span></span>
- <span data-ttu-id="cc14d-1409">Debitcard</span><span class="sxs-lookup"><span data-stu-id="cc14d-1409">debitcard</span></span>
- <span data-ttu-id="cc14d-1410">debit cards</span><span class="sxs-lookup"><span data-stu-id="cc14d-1410">debit cards</span></span>
- <span data-ttu-id="cc14d-1411">debitcards</span><span class="sxs-lookup"><span data-stu-id="cc14d-1411">debitcards</span></span>
- <span data-ttu-id="cc14d-1412">atm card</span><span class="sxs-lookup"><span data-stu-id="cc14d-1412">atm card</span></span>
- <span data-ttu-id="cc14d-1413">atmcard</span><span class="sxs-lookup"><span data-stu-id="cc14d-1413">atmcard</span></span>
- <span data-ttu-id="cc14d-1414">atm cards</span><span class="sxs-lookup"><span data-stu-id="cc14d-1414">atm cards</span></span>
- <span data-ttu-id="cc14d-1415">atmcards</span><span class="sxs-lookup"><span data-stu-id="cc14d-1415">atmcards</span></span>
- <span data-ttu-id="cc14d-1416">encaminhar</span><span class="sxs-lookup"><span data-stu-id="cc14d-1416">enroute</span></span>
- <span data-ttu-id="cc14d-1417">en route</span><span class="sxs-lookup"><span data-stu-id="cc14d-1417">en route</span></span>
- <span data-ttu-id="cc14d-1418">card type</span><span class="sxs-lookup"><span data-stu-id="cc14d-1418">card type</span></span>
- <span data-ttu-id="cc14d-1419">carte bancaire</span><span class="sxs-lookup"><span data-stu-id="cc14d-1419">carte bancaire</span></span>
- <span data-ttu-id="cc14d-1420">carte de crédit</span><span class="sxs-lookup"><span data-stu-id="cc14d-1420">carte de crédit</span></span>
- <span data-ttu-id="cc14d-1421">carte de credit</span><span class="sxs-lookup"><span data-stu-id="cc14d-1421">carte de credit</span></span>
- <span data-ttu-id="cc14d-1422">numéro de carte</span><span class="sxs-lookup"><span data-stu-id="cc14d-1422">numéro de carte</span></span>
- <span data-ttu-id="cc14d-1423">numero de carte</span><span class="sxs-lookup"><span data-stu-id="cc14d-1423">numero de carte</span></span>
- <span data-ttu-id="cc14d-1424">nº de la carte</span><span class="sxs-lookup"><span data-stu-id="cc14d-1424">nº de la carte</span></span>
- <span data-ttu-id="cc14d-1425">nº de carte</span><span class="sxs-lookup"><span data-stu-id="cc14d-1425">nº de carte</span></span>
- <span data-ttu-id="cc14d-1426">kreditkarte</span><span class="sxs-lookup"><span data-stu-id="cc14d-1426">kreditkarte</span></span>
- <span data-ttu-id="cc14d-1427">Karte</span><span class="sxs-lookup"><span data-stu-id="cc14d-1427">karte</span></span>
- <span data-ttu-id="cc14d-1428">karteninhaber</span><span class="sxs-lookup"><span data-stu-id="cc14d-1428">karteninhaber</span></span>
- <span data-ttu-id="cc14d-1429">karteninhabers</span><span class="sxs-lookup"><span data-stu-id="cc14d-1429">karteninhabers</span></span>
- <span data-ttu-id="cc14d-1430">kreditkarteninhaber</span><span class="sxs-lookup"><span data-stu-id="cc14d-1430">kreditkarteninhaber</span></span>
- <span data-ttu-id="cc14d-1431">kreditkarteninstitut</span><span class="sxs-lookup"><span data-stu-id="cc14d-1431">kreditkarteninstitut</span></span>
- <span data-ttu-id="cc14d-1432">kreditkartentyp</span><span class="sxs-lookup"><span data-stu-id="cc14d-1432">kreditkartentyp</span></span>
- <span data-ttu-id="cc14d-1433">eigentümername</span><span class="sxs-lookup"><span data-stu-id="cc14d-1433">eigentümername</span></span>
- <span data-ttu-id="cc14d-1434">kartennr</span><span class="sxs-lookup"><span data-stu-id="cc14d-1434">kartennr</span></span> 
- <span data-ttu-id="cc14d-1435">kartennummer</span><span class="sxs-lookup"><span data-stu-id="cc14d-1435">kartennummer</span></span>
- <span data-ttu-id="cc14d-1436">kreditkartennummer</span><span class="sxs-lookup"><span data-stu-id="cc14d-1436">kreditkartennummer</span></span>
- <span data-ttu-id="cc14d-1437">kreditkarten-Nummer</span><span class="sxs-lookup"><span data-stu-id="cc14d-1437">kreditkarten-nummer</span></span>
- <span data-ttu-id="cc14d-1438">carta di credito</span><span class="sxs-lookup"><span data-stu-id="cc14d-1438">carta di credito</span></span>
- <span data-ttu-id="cc14d-1439">carta credito</span><span class="sxs-lookup"><span data-stu-id="cc14d-1439">carta credito</span></span>
- <span data-ttu-id="cc14d-1440">carta</span><span class="sxs-lookup"><span data-stu-id="cc14d-1440">carta</span></span>
- <span data-ttu-id="cc14d-1441">n carta</span><span class="sxs-lookup"><span data-stu-id="cc14d-1441">n carta</span></span>
- <span data-ttu-id="cc14d-1442">Nr.</span><span class="sxs-lookup"><span data-stu-id="cc14d-1442">nr.</span></span> <span data-ttu-id="cc14d-1443">carta</span><span class="sxs-lookup"><span data-stu-id="cc14d-1443">carta</span></span>
- <span data-ttu-id="cc14d-1444">nr carta</span><span class="sxs-lookup"><span data-stu-id="cc14d-1444">nr carta</span></span>
- <span data-ttu-id="cc14d-1445">numero carta</span><span class="sxs-lookup"><span data-stu-id="cc14d-1445">numero carta</span></span>
- <span data-ttu-id="cc14d-1446">numero della carta</span><span class="sxs-lookup"><span data-stu-id="cc14d-1446">numero della carta</span></span>
- <span data-ttu-id="cc14d-1447">numero di carta</span><span class="sxs-lookup"><span data-stu-id="cc14d-1447">numero di carta</span></span>
- <span data-ttu-id="cc14d-1448">tarjeta credito</span><span class="sxs-lookup"><span data-stu-id="cc14d-1448">tarjeta credito</span></span>
- <span data-ttu-id="cc14d-1449">tarjeta de credito</span><span class="sxs-lookup"><span data-stu-id="cc14d-1449">tarjeta de credito</span></span>
- <span data-ttu-id="cc14d-1450">tarjeta crédito</span><span class="sxs-lookup"><span data-stu-id="cc14d-1450">tarjeta crédito</span></span>
- <span data-ttu-id="cc14d-1451">tarjeta de crédito</span><span class="sxs-lookup"><span data-stu-id="cc14d-1451">tarjeta de crédito</span></span>
- <span data-ttu-id="cc14d-1452">tarjeta de atm</span><span class="sxs-lookup"><span data-stu-id="cc14d-1452">tarjeta de atm</span></span>
- <span data-ttu-id="cc14d-1453">tarjeta atm</span><span class="sxs-lookup"><span data-stu-id="cc14d-1453">tarjeta atm</span></span>
- <span data-ttu-id="cc14d-1454">tarjeta debito</span><span class="sxs-lookup"><span data-stu-id="cc14d-1454">tarjeta debito</span></span>
- <span data-ttu-id="cc14d-1455">tarjeta de debito</span><span class="sxs-lookup"><span data-stu-id="cc14d-1455">tarjeta de debito</span></span>
- <span data-ttu-id="cc14d-1456">tarjeta débito</span><span class="sxs-lookup"><span data-stu-id="cc14d-1456">tarjeta débito</span></span>
- <span data-ttu-id="cc14d-1457">tarjeta de débito</span><span class="sxs-lookup"><span data-stu-id="cc14d-1457">tarjeta de débito</span></span>
- <span data-ttu-id="cc14d-1458">nº de tarjeta</span><span class="sxs-lookup"><span data-stu-id="cc14d-1458">nº de tarjeta</span></span>
- <span data-ttu-id="cc14d-1459">Não.</span><span class="sxs-lookup"><span data-stu-id="cc14d-1459">no.</span></span> <span data-ttu-id="cc14d-1460">de tarjeta</span><span class="sxs-lookup"><span data-stu-id="cc14d-1460">de tarjeta</span></span>
- <span data-ttu-id="cc14d-1461">no de tarjeta</span><span class="sxs-lookup"><span data-stu-id="cc14d-1461">no de tarjeta</span></span>
- <span data-ttu-id="cc14d-1462">numero de tarjeta</span><span class="sxs-lookup"><span data-stu-id="cc14d-1462">numero de tarjeta</span></span>
- <span data-ttu-id="cc14d-1463">número de tarjeta</span><span class="sxs-lookup"><span data-stu-id="cc14d-1463">número de tarjeta</span></span>
- <span data-ttu-id="cc14d-1464">tarjeta no</span><span class="sxs-lookup"><span data-stu-id="cc14d-1464">tarjeta no</span></span>
- <span data-ttu-id="cc14d-1465">tarjetahabiente</span><span class="sxs-lookup"><span data-stu-id="cc14d-1465">tarjetahabiente</span></span>
- <span data-ttu-id="cc14d-1466">cartão de crédito</span><span class="sxs-lookup"><span data-stu-id="cc14d-1466">cartão de crédito</span></span>
- <span data-ttu-id="cc14d-1467">cartão de credito</span><span class="sxs-lookup"><span data-stu-id="cc14d-1467">cartão de credito</span></span>
- <span data-ttu-id="cc14d-1468">cartao de crédito</span><span class="sxs-lookup"><span data-stu-id="cc14d-1468">cartao de crédito</span></span>
- <span data-ttu-id="cc14d-1469">cartao de credito</span><span class="sxs-lookup"><span data-stu-id="cc14d-1469">cartao de credito</span></span>
- <span data-ttu-id="cc14d-1470">cartão de débito</span><span class="sxs-lookup"><span data-stu-id="cc14d-1470">cartão de débito</span></span>
- <span data-ttu-id="cc14d-1471">cartao de débito</span><span class="sxs-lookup"><span data-stu-id="cc14d-1471">cartao de débito</span></span>
- <span data-ttu-id="cc14d-1472">cartão de debito</span><span class="sxs-lookup"><span data-stu-id="cc14d-1472">cartão de debito</span></span>
- <span data-ttu-id="cc14d-1473">cartao de debito</span><span class="sxs-lookup"><span data-stu-id="cc14d-1473">cartao de debito</span></span>
- <span data-ttu-id="cc14d-1474">débito automático</span><span class="sxs-lookup"><span data-stu-id="cc14d-1474">débito automático</span></span>
- <span data-ttu-id="cc14d-1475">debito automatico</span><span class="sxs-lookup"><span data-stu-id="cc14d-1475">debito automatico</span></span>
- <span data-ttu-id="cc14d-1476">número do cartão</span><span class="sxs-lookup"><span data-stu-id="cc14d-1476">número do cartão</span></span>
- <span data-ttu-id="cc14d-1477">numero do cartão</span><span class="sxs-lookup"><span data-stu-id="cc14d-1477">numero do cartão</span></span> 
- <span data-ttu-id="cc14d-1478">número do cartao</span><span class="sxs-lookup"><span data-stu-id="cc14d-1478">número do cartao</span></span>
- <span data-ttu-id="cc14d-1479">numero do cartao</span><span class="sxs-lookup"><span data-stu-id="cc14d-1479">numero do cartao</span></span>
- <span data-ttu-id="cc14d-1480">número de cartão</span><span class="sxs-lookup"><span data-stu-id="cc14d-1480">número de cartão</span></span>
- <span data-ttu-id="cc14d-1481">numero de cartão</span><span class="sxs-lookup"><span data-stu-id="cc14d-1481">numero de cartão</span></span>
- <span data-ttu-id="cc14d-1482">número de cartao</span><span class="sxs-lookup"><span data-stu-id="cc14d-1482">número de cartao</span></span>
- <span data-ttu-id="cc14d-1483">numero de cartao</span><span class="sxs-lookup"><span data-stu-id="cc14d-1483">numero de cartao</span></span>
- <span data-ttu-id="cc14d-1484">nº do cartão</span><span class="sxs-lookup"><span data-stu-id="cc14d-1484">nº do cartão</span></span>
- <span data-ttu-id="cc14d-1485">nº do cartao</span><span class="sxs-lookup"><span data-stu-id="cc14d-1485">nº do cartao</span></span>
- <span data-ttu-id="cc14d-1486">n º.</span><span class="sxs-lookup"><span data-stu-id="cc14d-1486">nº.</span></span> <span data-ttu-id="cc14d-1487">do cartão</span><span class="sxs-lookup"><span data-stu-id="cc14d-1487">do cartão</span></span>
- <span data-ttu-id="cc14d-1488">no do cartão</span><span class="sxs-lookup"><span data-stu-id="cc14d-1488">no do cartão</span></span>
- <span data-ttu-id="cc14d-1489">no do cartao</span><span class="sxs-lookup"><span data-stu-id="cc14d-1489">no do cartao</span></span>
- <span data-ttu-id="cc14d-1490">Não.</span><span class="sxs-lookup"><span data-stu-id="cc14d-1490">no.</span></span> <span data-ttu-id="cc14d-1491">do cartão</span><span class="sxs-lookup"><span data-stu-id="cc14d-1491">do cartão</span></span>
- <span data-ttu-id="cc14d-1492">Não.</span><span class="sxs-lookup"><span data-stu-id="cc14d-1492">no.</span></span> <span data-ttu-id="cc14d-1493">do cartao</span><span class="sxs-lookup"><span data-stu-id="cc14d-1493">do cartao</span></span> 
   
## <a name="croatia-identity-card-number"></a><span data-ttu-id="cc14d-1494">	Número do Cartão de Identidade da Croácia</span><span class="sxs-lookup"><span data-stu-id="cc14d-1494">Croatia Identity Card Number</span></span>

### <a name="format"></a><span data-ttu-id="cc14d-1495">Format</span><span class="sxs-lookup"><span data-stu-id="cc14d-1495">Format</span></span>

<span data-ttu-id="cc14d-1496">Nove dígitos</span><span class="sxs-lookup"><span data-stu-id="cc14d-1496">Nine digits</span></span>

### <a name="pattern"></a><span data-ttu-id="cc14d-1497">Padrão</span><span class="sxs-lookup"><span data-stu-id="cc14d-1497">Pattern</span></span>

<span data-ttu-id="cc14d-1498">Nove dígitos consecutivos</span><span class="sxs-lookup"><span data-stu-id="cc14d-1498">Nine consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="cc14d-1499">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="cc14d-1499">Checksum</span></span>

<span data-ttu-id="cc14d-1500">Não</span><span class="sxs-lookup"><span data-stu-id="cc14d-1500">No</span></span>

### <a name="definition"></a><span data-ttu-id="cc14d-1501">Definição</span><span class="sxs-lookup"><span data-stu-id="cc14d-1501">Definition</span></span>

<span data-ttu-id="cc14d-1502">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="cc14d-1502">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="cc14d-1503">A função Func_croatia_id_card localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="cc14d-1503">The function Func_croatia_id_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="cc14d-1504">Uma palavra-chave de Keyword_croatia_id_card for encontrada.</span><span class="sxs-lookup"><span data-stu-id="cc14d-1504">A keyword from Keyword_croatia_id_card is found.</span></span>

```
<!--Croatia Identity Card Number-->
<Entity id="ff12f884-c20a-4189-b185-34c8e7258d47" recommendedConfidence="75" patternsProximity="300">
  <Pattern confidenceLevel="75">
     <IdMatch idRef="Func_croatia_id_card"/>
     <Match idRef="Keyword_croatia_id_card"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="cc14d-1505">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="cc14d-1505">Keywords</span></span>

#### <a name="keywordcroatiaidcard"></a><span data-ttu-id="cc14d-1506">Keyword_croatia_id_card</span><span class="sxs-lookup"><span data-stu-id="cc14d-1506">Keyword_croatia_id_card</span></span>

- <span data-ttu-id="cc14d-1507">Cartão de identidade croata</span><span class="sxs-lookup"><span data-stu-id="cc14d-1507">Croatian identity card</span></span>
- <span data-ttu-id="cc14d-1508">Osobna iskaznica</span><span class="sxs-lookup"><span data-stu-id="cc14d-1508">Osobna iskaznica</span></span>

   
## <a name="croatia-personal-identification-oib-number"></a><span data-ttu-id="cc14d-1509">	Número de Identificação Pessoal (OIB) da Croácia</span><span class="sxs-lookup"><span data-stu-id="cc14d-1509">Croatia Personal Identification (OIB) Number</span></span>

### <a name="format"></a><span data-ttu-id="cc14d-1510">Format</span><span class="sxs-lookup"><span data-stu-id="cc14d-1510">Format</span></span>

<span data-ttu-id="cc14d-1511">11 dígitos</span><span class="sxs-lookup"><span data-stu-id="cc14d-1511">11 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="cc14d-1512">Padrão</span><span class="sxs-lookup"><span data-stu-id="cc14d-1512">Pattern</span></span>

<span data-ttu-id="cc14d-1513">11 dígitos:</span><span class="sxs-lookup"><span data-stu-id="cc14d-1513">11 digits:</span></span>
- <span data-ttu-id="cc14d-1514">10 dígitos</span><span class="sxs-lookup"><span data-stu-id="cc14d-1514">10 digits</span></span> 
- <span data-ttu-id="cc14d-1515">O dígito final é um dígito de verificação para os fins de troca de dados internacionais, as letras de RH são adicionadas antes dos onze dígitos.</span><span class="sxs-lookup"><span data-stu-id="cc14d-1515">Final digit is a check digit For the purposes of international data exchange, the letters HR are added preceding the eleven digits.</span></span>

### <a name="checksum"></a><span data-ttu-id="cc14d-1516">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="cc14d-1516">Checksum</span></span>

<span data-ttu-id="cc14d-1517">Sim</span><span class="sxs-lookup"><span data-stu-id="cc14d-1517">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="cc14d-1518">Definição</span><span class="sxs-lookup"><span data-stu-id="cc14d-1518">Definition</span></span>

<span data-ttu-id="cc14d-1519">Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="cc14d-1519">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="cc14d-1520">A função Func_croatia_oib_number localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="cc14d-1520">The function Func_croatia_oib_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="cc14d-1521">Uma palavra-chave de Keyword_croatia_oib_number for encontrada.</span><span class="sxs-lookup"><span data-stu-id="cc14d-1521">A keyword from Keyword_croatia_oib_number is found.</span></span>
- <span data-ttu-id="cc14d-1522">A soma de verificação passa.</span><span class="sxs-lookup"><span data-stu-id="cc14d-1522">The checksum passes.</span></span>

<span data-ttu-id="cc14d-1523">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="cc14d-1523">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="cc14d-1524">A função Func_croatia_oib_number localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="cc14d-1524">The function Func_croatia_oib_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="cc14d-1525">A soma de verificação passa.</span><span class="sxs-lookup"><span data-stu-id="cc14d-1525">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="cc14d-1526">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="cc14d-1526">Keywords</span></span>

#### <a name="keywordcroatiaoibnumber"></a><span data-ttu-id="cc14d-1527">Keyword_croatia_oib_number</span><span class="sxs-lookup"><span data-stu-id="cc14d-1527">Keyword_croatia_oib_number</span></span>

- <span data-ttu-id="cc14d-1528">Número de Identificação Pessoal</span><span class="sxs-lookup"><span data-stu-id="cc14d-1528">Personal Identification Number</span></span>
- <span data-ttu-id="cc14d-1529">Osobni identifikacijski broj</span><span class="sxs-lookup"><span data-stu-id="cc14d-1529">Osobni identifikacijski broj</span></span> 
- <span data-ttu-id="cc14d-1530">NIB</span><span class="sxs-lookup"><span data-stu-id="cc14d-1530">OIB</span></span> 

   
## <a name="czech-personal-identity-number"></a><span data-ttu-id="cc14d-1531">Número de identidade pessoal tcheco</span><span class="sxs-lookup"><span data-stu-id="cc14d-1531">Czech Personal Identity Number</span></span>

### <a name="format"></a><span data-ttu-id="cc14d-1532">Format</span><span class="sxs-lookup"><span data-stu-id="cc14d-1532">Format</span></span>

<span data-ttu-id="cc14d-1533">Nove dígitos com barra de avanço opcional (formato antigo) 10 dígitos com barra de avanço opcional (novo formato)</span><span class="sxs-lookup"><span data-stu-id="cc14d-1533">Nine digits with optional forward slash (old format) 10 digits with optional forward slash (new format)</span></span>

### <a name="pattern"></a><span data-ttu-id="cc14d-1534">Padrão</span><span class="sxs-lookup"><span data-stu-id="cc14d-1534">Pattern</span></span>

<span data-ttu-id="cc14d-1535">Nove dígitos (formato antigo):</span><span class="sxs-lookup"><span data-stu-id="cc14d-1535">Nine digits (old format):</span></span>
- <span data-ttu-id="cc14d-1536">Nove dígitos</span><span class="sxs-lookup"><span data-stu-id="cc14d-1536">Nine digits</span></span>

<span data-ttu-id="cc14d-1537">OU</span><span class="sxs-lookup"><span data-stu-id="cc14d-1537">OR</span></span>

- <span data-ttu-id="cc14d-1538">Seis dígitos que representam a data de nascimento</span><span class="sxs-lookup"><span data-stu-id="cc14d-1538">Six digits that represent date of birth</span></span>
- <span data-ttu-id="cc14d-1539">Uma barra</span><span class="sxs-lookup"><span data-stu-id="cc14d-1539">A forward slash</span></span>
- <span data-ttu-id="cc14d-1540">Três dígitos</span><span class="sxs-lookup"><span data-stu-id="cc14d-1540">Three digits</span></span>

<span data-ttu-id="cc14d-1541">10 dígitos (novo formato):</span><span class="sxs-lookup"><span data-stu-id="cc14d-1541">10 digits (new format):</span></span>
- <span data-ttu-id="cc14d-1542">10 dígitos</span><span class="sxs-lookup"><span data-stu-id="cc14d-1542">10 digits</span></span>

<span data-ttu-id="cc14d-1543">OU</span><span class="sxs-lookup"><span data-stu-id="cc14d-1543">OR</span></span>

- <span data-ttu-id="cc14d-1544">Seis dígitos que representam a data de nascimento</span><span class="sxs-lookup"><span data-stu-id="cc14d-1544">Six digits that represent date of birth</span></span>
- <span data-ttu-id="cc14d-1545">Uma barra</span><span class="sxs-lookup"><span data-stu-id="cc14d-1545">A forward slash</span></span> 
- <span data-ttu-id="cc14d-1546">Quatro dígitos onde o último dígito é um dígito de verificação</span><span class="sxs-lookup"><span data-stu-id="cc14d-1546">Four digits where last digit is a check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="cc14d-1547">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="cc14d-1547">Checksum</span></span>

<span data-ttu-id="cc14d-1548">Sim</span><span class="sxs-lookup"><span data-stu-id="cc14d-1548">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="cc14d-1549">Definição</span><span class="sxs-lookup"><span data-stu-id="cc14d-1549">Definition</span></span>

<span data-ttu-id="cc14d-1550">Uma política de DLP é de 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres: a função Func_czech_id_card localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="cc14d-1550">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters: The function Func_czech_id_card finds content that matches the pattern.</span></span>
<span data-ttu-id="cc14d-1551">Uma palavra-chave de Keyword_czech_id_card for encontrada.</span><span class="sxs-lookup"><span data-stu-id="cc14d-1551">A keyword from Keyword_czech_id_card is found.</span></span>
<span data-ttu-id="cc14d-1552">A soma de verificação passa.</span><span class="sxs-lookup"><span data-stu-id="cc14d-1552">The checksum passes.</span></span>

```
<!-- Czech Personal Identity Number -->
<Entity id="60c0725a-4eb6-455b-9dda-05d8a7396497"      patternsProximity="300" recommendedConfidence="85">
   <Pattern confidenceLevel="85">
      <IdMatch idRef="Func_czech_id_card" />
      <Match idRef="Keyword_czech_id_card" />
   </Pattern>
</Entity>
```
### <a name="keywords"></a><span data-ttu-id="cc14d-1553">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="cc14d-1553">Keywords</span></span>

- <span data-ttu-id="cc14d-1554">número de identidade pessoal tcheco</span><span class="sxs-lookup"><span data-stu-id="cc14d-1554">czech personal identity number</span></span>
- <span data-ttu-id="cc14d-1555">Rodné číslo</span><span class="sxs-lookup"><span data-stu-id="cc14d-1555">Rodné číslo</span></span>
   
## <a name="denmark-personal-identification-number"></a><span data-ttu-id="cc14d-1556">	Número de Identificação Pessoal da Dinamarca</span><span class="sxs-lookup"><span data-stu-id="cc14d-1556">Denmark Personal Identification Number</span></span>

### <a name="format"></a><span data-ttu-id="cc14d-1557">Format</span><span class="sxs-lookup"><span data-stu-id="cc14d-1557">Format</span></span>

<span data-ttu-id="cc14d-1558">10 dígitos que contêm um hífen</span><span class="sxs-lookup"><span data-stu-id="cc14d-1558">10 digits containing a hyphen</span></span>

### <a name="pattern"></a><span data-ttu-id="cc14d-1559">Padrão</span><span class="sxs-lookup"><span data-stu-id="cc14d-1559">Pattern</span></span>

<span data-ttu-id="cc14d-1560">10 dígitos:</span><span class="sxs-lookup"><span data-stu-id="cc14d-1560">10 digits:</span></span>
- <span data-ttu-id="cc14d-1561">Seis dígitos no formato DDMMAA que são a data de nascimento</span><span class="sxs-lookup"><span data-stu-id="cc14d-1561">Six digits in the format DDMMYY which are the date of birth</span></span> 
- <span data-ttu-id="cc14d-1562">Um hífen</span><span class="sxs-lookup"><span data-stu-id="cc14d-1562">A hyphen</span></span> 
- <span data-ttu-id="cc14d-1563">Quatro dígitos em que o último é um dígito de verificação</span><span class="sxs-lookup"><span data-stu-id="cc14d-1563">Four digits where the final digit is a check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="cc14d-1564">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="cc14d-1564">Checksum</span></span>

<span data-ttu-id="cc14d-1565">Sim</span><span class="sxs-lookup"><span data-stu-id="cc14d-1565">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="cc14d-1566">Definição</span><span class="sxs-lookup"><span data-stu-id="cc14d-1566">Definition</span></span>

<span data-ttu-id="cc14d-1567">Uma política de DLP é de 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres: a expressão regular Regex_denmark_id localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="cc14d-1567">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters: The regular expression Regex_denmark_id finds content that matches the pattern.</span></span>
<span data-ttu-id="cc14d-1568">Uma palavra-chave de Keyword_denmark_id for encontrada.</span><span class="sxs-lookup"><span data-stu-id="cc14d-1568">A keyword from Keyword_denmark_id is found.</span></span>
<span data-ttu-id="cc14d-1569">A soma de verificação passa.</span><span class="sxs-lookup"><span data-stu-id="cc14d-1569">The checksum passes.</span></span>

```
<!-- Denmark Personal Identification Number -->
<Entity id="6c4f2fef-56e1-4c00-8093-88d7a01cf460" recommendedConfidence="75" patternsProximity="300">
  <Pattern confidenceLevel="75">
     <IdMatch idRef="Regex_denmark_id"/>
     <Match idRef="Keyword_denmark_id"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="cc14d-1570">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="cc14d-1570">Keywords</span></span>

#### <a name="keyworddenmarkid"></a><span data-ttu-id="cc14d-1571">Keyword_denmark_id</span><span class="sxs-lookup"><span data-stu-id="cc14d-1571">Keyword_denmark_id</span></span>

- <span data-ttu-id="cc14d-1572">Número de Identificação Pessoal</span><span class="sxs-lookup"><span data-stu-id="cc14d-1572">Personal Identification Number</span></span>
- <span data-ttu-id="cc14d-1573">PEDIR</span><span class="sxs-lookup"><span data-stu-id="cc14d-1573">CPR</span></span>
- <span data-ttu-id="cc14d-1574">Det Centrale Personregister</span><span class="sxs-lookup"><span data-stu-id="cc14d-1574">Det Centrale Personregister</span></span>
- <span data-ttu-id="cc14d-1575">Personnummer</span><span class="sxs-lookup"><span data-stu-id="cc14d-1575">Personnummer</span></span>
   
## <a name="drug-enforcement-agency-dea-number"></a><span data-ttu-id="cc14d-1576">Número da Drug Enforcement Agency (DEA)</span><span class="sxs-lookup"><span data-stu-id="cc14d-1576">Drug Enforcement Agency (DEA) Number</span></span>

### <a name="format"></a><span data-ttu-id="cc14d-1577">Format</span><span class="sxs-lookup"><span data-stu-id="cc14d-1577">Format</span></span>

<span data-ttu-id="cc14d-1578">Duas letras seguidas por sete dígitos</span><span class="sxs-lookup"><span data-stu-id="cc14d-1578">Two letters followed by seven digits</span></span>

### <a name="pattern"></a><span data-ttu-id="cc14d-1579">Padrão</span><span class="sxs-lookup"><span data-stu-id="cc14d-1579">Pattern</span></span>

<span data-ttu-id="cc14d-1580">O padrão deve incluir todos os seguintes itens:</span><span class="sxs-lookup"><span data-stu-id="cc14d-1580">Pattern must include all of the following:</span></span>
- <span data-ttu-id="cc14d-1581">Uma letra (não diferencia maiúscula de minúscula) deste conjunto de letras possíveis: abcdefghjklmnprstux, que é um código de inscrito</span><span class="sxs-lookup"><span data-stu-id="cc14d-1581">One letter (not case sensitive) from this set of possible letters: abcdefghjklmnprstux, which is a registrant code</span></span> 
- <span data-ttu-id="cc14d-1582">Uma letra (não diferencia maiúscula de minúscula), que é a primeira letra do sobrenome do inscrito</span><span class="sxs-lookup"><span data-stu-id="cc14d-1582">One letter (not case sensitive), which is the first letter of the registrant's last name</span></span> 
- <span data-ttu-id="cc14d-1583">Sete dígitos, dos quais o último é o dígito de verificação</span><span class="sxs-lookup"><span data-stu-id="cc14d-1583">Seven digits, the last of which is the check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="cc14d-1584">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="cc14d-1584">Checksum</span></span>

<span data-ttu-id="cc14d-1585">Sim</span><span class="sxs-lookup"><span data-stu-id="cc14d-1585">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="cc14d-1586">Definição</span><span class="sxs-lookup"><span data-stu-id="cc14d-1586">Definition</span></span>

<span data-ttu-id="cc14d-1587">Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="cc14d-1587">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="cc14d-1588">A função Func_dea_number localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="cc14d-1588">The function Func_dea_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="cc14d-1589">A soma de verificação passa.</span><span class="sxs-lookup"><span data-stu-id="cc14d-1589">The checksum passes.</span></span>

```
<!-- DEA Number -->
<Entity id="9a5445ad-406e-43eb-8bd7-cac17ab6d0e4" recommendedConfidence="85" patternsProximity="300">
  <Pattern confidenceLevel="85">
     <IdMatch idRef="Func_dea_number"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="cc14d-1590">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="cc14d-1590">Keywords</span></span>

<span data-ttu-id="cc14d-1591">Nenhum</span><span class="sxs-lookup"><span data-stu-id="cc14d-1591">None</span></span>

   
## <a name="eu-debit-card-number"></a><span data-ttu-id="cc14d-1592">Número de cartão de débito da UE</span><span class="sxs-lookup"><span data-stu-id="cc14d-1592">EU Debit Card Number</span></span>

### <a name="format"></a><span data-ttu-id="cc14d-1593">Format</span><span class="sxs-lookup"><span data-stu-id="cc14d-1593">Format</span></span>

<span data-ttu-id="cc14d-1594">16 dígitos</span><span class="sxs-lookup"><span data-stu-id="cc14d-1594">16 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="cc14d-1595">Padrão</span><span class="sxs-lookup"><span data-stu-id="cc14d-1595">Pattern</span></span>

<span data-ttu-id="cc14d-1596">Padrão muito complexo e robusto</span><span class="sxs-lookup"><span data-stu-id="cc14d-1596">Very complex and robust pattern</span></span>

### <a name="checksum"></a><span data-ttu-id="cc14d-1597">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="cc14d-1597">Checksum</span></span>

<span data-ttu-id="cc14d-1598">Sim</span><span class="sxs-lookup"><span data-stu-id="cc14d-1598">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="cc14d-1599">Definição</span><span class="sxs-lookup"><span data-stu-id="cc14d-1599">Definition</span></span>

<span data-ttu-id="cc14d-1600">Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="cc14d-1600">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="cc14d-1601">A função Func_eu_debit_card localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="cc14d-1601">The function Func_eu_debit_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="cc14d-1602">Pelo menos uma das seguintes opções for verdadeira:</span><span class="sxs-lookup"><span data-stu-id="cc14d-1602">At least one of the following is true:</span></span>
    - <span data-ttu-id="cc14d-1603">Uma palavra-chave de Keyword_eu_debit_card for encontrada.</span><span class="sxs-lookup"><span data-stu-id="cc14d-1603">A keyword from Keyword_eu_debit_card is found.</span></span>
    - <span data-ttu-id="cc14d-1604">Uma palavra-chave de Keyword_card_terms_dict for encontrada.</span><span class="sxs-lookup"><span data-stu-id="cc14d-1604">A keyword from Keyword_card_terms_dict is found.</span></span>
    - <span data-ttu-id="cc14d-1605">Uma palavra-chave de Keyword_card_security_terms_dict for encontrada.</span><span class="sxs-lookup"><span data-stu-id="cc14d-1605">A keyword from Keyword_card_security_terms_dict is found.</span></span>
    - <span data-ttu-id="cc14d-1606">Uma palavra-chave de Keyword_card_expiration_terms_dict for encontrada.</span><span class="sxs-lookup"><span data-stu-id="cc14d-1606">A keyword from Keyword_card_expiration_terms_dict is found.</span></span>
    - <span data-ttu-id="cc14d-1607">A função Func_expiration_date encontra uma data no formato de data à direita.</span><span class="sxs-lookup"><span data-stu-id="cc14d-1607">The function Func_expiration_date finds a date in the right date format.</span></span>
- <span data-ttu-id="cc14d-1608">A soma de verificação passa.</span><span class="sxs-lookup"><span data-stu-id="cc14d-1608">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="cc14d-1609">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="cc14d-1609">Keywords</span></span>

#### <a name="keywordeudebitcard"></a><span data-ttu-id="cc14d-1610">Keyword_eu_debit_card</span><span class="sxs-lookup"><span data-stu-id="cc14d-1610">Keyword_eu_debit_card</span></span>

- <span data-ttu-id="cc14d-1611">account number</span><span class="sxs-lookup"><span data-stu-id="cc14d-1611">account number</span></span> 
- <span data-ttu-id="cc14d-1612">card number</span><span class="sxs-lookup"><span data-stu-id="cc14d-1612">card number</span></span> 
- <span data-ttu-id="cc14d-1613">card no.</span><span class="sxs-lookup"><span data-stu-id="cc14d-1613">card no.</span></span> 
- <span data-ttu-id="cc14d-1614">security number</span><span class="sxs-lookup"><span data-stu-id="cc14d-1614">security number</span></span> 
- <span data-ttu-id="cc14d-1615">colocado</span><span class="sxs-lookup"><span data-stu-id="cc14d-1615">cc#</span></span> 

#### <a name="keywordcardtermsdict"></a><span data-ttu-id="cc14d-1616">Keyword_card_terms_dict</span><span class="sxs-lookup"><span data-stu-id="cc14d-1616">Keyword_card_terms_dict</span></span>

- <span data-ttu-id="cc14d-1617">acct nbr</span><span class="sxs-lookup"><span data-stu-id="cc14d-1617">acct nbr</span></span> 
- <span data-ttu-id="cc14d-1618">acct num</span><span class="sxs-lookup"><span data-stu-id="cc14d-1618">acct num</span></span> 
- <span data-ttu-id="cc14d-1619">acct no</span><span class="sxs-lookup"><span data-stu-id="cc14d-1619">acct no</span></span> 
- <span data-ttu-id="cc14d-1620">american express</span><span class="sxs-lookup"><span data-stu-id="cc14d-1620">american express</span></span> 
- <span data-ttu-id="cc14d-1621">americanexpress</span><span class="sxs-lookup"><span data-stu-id="cc14d-1621">americanexpress</span></span> 
- <span data-ttu-id="cc14d-1622">americano espresso</span><span class="sxs-lookup"><span data-stu-id="cc14d-1622">americano espresso</span></span> 
- <span data-ttu-id="cc14d-1623">Amex</span><span class="sxs-lookup"><span data-stu-id="cc14d-1623">amex</span></span> 
- <span data-ttu-id="cc14d-1624">atm card</span><span class="sxs-lookup"><span data-stu-id="cc14d-1624">atm card</span></span> 
- <span data-ttu-id="cc14d-1625">atm cards</span><span class="sxs-lookup"><span data-stu-id="cc14d-1625">atm cards</span></span> 
- <span data-ttu-id="cc14d-1626">atm kaart</span><span class="sxs-lookup"><span data-stu-id="cc14d-1626">atm kaart</span></span> 
- <span data-ttu-id="cc14d-1627">atmcard</span><span class="sxs-lookup"><span data-stu-id="cc14d-1627">atmcard</span></span> 
- <span data-ttu-id="cc14d-1628">atmcards</span><span class="sxs-lookup"><span data-stu-id="cc14d-1628">atmcards</span></span> 
- <span data-ttu-id="cc14d-1629">atmkaart</span><span class="sxs-lookup"><span data-stu-id="cc14d-1629">atmkaart</span></span> 
- <span data-ttu-id="cc14d-1630">atmkaarten</span><span class="sxs-lookup"><span data-stu-id="cc14d-1630">atmkaarten</span></span> 
- <span data-ttu-id="cc14d-1631">Bancontact</span><span class="sxs-lookup"><span data-stu-id="cc14d-1631">bancontact</span></span> 
- <span data-ttu-id="cc14d-1632">bank card</span><span class="sxs-lookup"><span data-stu-id="cc14d-1632">bank card</span></span> 
- <span data-ttu-id="cc14d-1633">bankkaart</span><span class="sxs-lookup"><span data-stu-id="cc14d-1633">bankkaart</span></span> 
- <span data-ttu-id="cc14d-1634">card holder</span><span class="sxs-lookup"><span data-stu-id="cc14d-1634">card holder</span></span> 
- <span data-ttu-id="cc14d-1635">card holders</span><span class="sxs-lookup"><span data-stu-id="cc14d-1635">card holders</span></span> 
- <span data-ttu-id="cc14d-1636">card num</span><span class="sxs-lookup"><span data-stu-id="cc14d-1636">card num</span></span> 
- <span data-ttu-id="cc14d-1637">card number</span><span class="sxs-lookup"><span data-stu-id="cc14d-1637">card number</span></span> 
- <span data-ttu-id="cc14d-1638">card numbers</span><span class="sxs-lookup"><span data-stu-id="cc14d-1638">card numbers</span></span> 
- <span data-ttu-id="cc14d-1639">card type</span><span class="sxs-lookup"><span data-stu-id="cc14d-1639">card type</span></span> 
- <span data-ttu-id="cc14d-1640">cardano numerico</span><span class="sxs-lookup"><span data-stu-id="cc14d-1640">cardano numerico</span></span> 
- <span data-ttu-id="cc14d-1641">aos</span><span class="sxs-lookup"><span data-stu-id="cc14d-1641">cardholder</span></span> 
- <span data-ttu-id="cc14d-1642">titulares de cartões</span><span class="sxs-lookup"><span data-stu-id="cc14d-1642">cardholders</span></span> 
- <span data-ttu-id="cc14d-1643">cardNumber</span><span class="sxs-lookup"><span data-stu-id="cc14d-1643">cardnumber</span></span> 
- <span data-ttu-id="cc14d-1644">cardnumbers</span><span class="sxs-lookup"><span data-stu-id="cc14d-1644">cardnumbers</span></span> 
- <span data-ttu-id="cc14d-1645">carta bianca</span><span class="sxs-lookup"><span data-stu-id="cc14d-1645">carta bianca</span></span> 
- <span data-ttu-id="cc14d-1646">carta credito</span><span class="sxs-lookup"><span data-stu-id="cc14d-1646">carta credito</span></span> 
- <span data-ttu-id="cc14d-1647">carta di credito</span><span class="sxs-lookup"><span data-stu-id="cc14d-1647">carta di credito</span></span> 
- <span data-ttu-id="cc14d-1648">cartao de credito</span><span class="sxs-lookup"><span data-stu-id="cc14d-1648">cartao de credito</span></span> 
- <span data-ttu-id="cc14d-1649">cartao de crédito</span><span class="sxs-lookup"><span data-stu-id="cc14d-1649">cartao de crédito</span></span> 
- <span data-ttu-id="cc14d-1650">cartao de debito</span><span class="sxs-lookup"><span data-stu-id="cc14d-1650">cartao de debito</span></span> 
- <span data-ttu-id="cc14d-1651">cartao de débito</span><span class="sxs-lookup"><span data-stu-id="cc14d-1651">cartao de débito</span></span> 
- <span data-ttu-id="cc14d-1652">carte bancaire</span><span class="sxs-lookup"><span data-stu-id="cc14d-1652">carte bancaire</span></span> 
- <span data-ttu-id="cc14d-1653">carte blanche</span><span class="sxs-lookup"><span data-stu-id="cc14d-1653">carte blanche</span></span> 
- <span data-ttu-id="cc14d-1654">carte bleue</span><span class="sxs-lookup"><span data-stu-id="cc14d-1654">carte bleue</span></span> 
- <span data-ttu-id="cc14d-1655">carte de credit</span><span class="sxs-lookup"><span data-stu-id="cc14d-1655">carte de credit</span></span> 
- <span data-ttu-id="cc14d-1656">carte de crédit</span><span class="sxs-lookup"><span data-stu-id="cc14d-1656">carte de crédit</span></span> 
- <span data-ttu-id="cc14d-1657">carte di credito</span><span class="sxs-lookup"><span data-stu-id="cc14d-1657">carte di credito</span></span> 
- <span data-ttu-id="cc14d-1658">carteblanche</span><span class="sxs-lookup"><span data-stu-id="cc14d-1658">carteblanche</span></span> 
- <span data-ttu-id="cc14d-1659">cartão de credito</span><span class="sxs-lookup"><span data-stu-id="cc14d-1659">cartão de credito</span></span> 
- <span data-ttu-id="cc14d-1660">cartão de crédito</span><span class="sxs-lookup"><span data-stu-id="cc14d-1660">cartão de crédito</span></span> 
- <span data-ttu-id="cc14d-1661">cartão de debito</span><span class="sxs-lookup"><span data-stu-id="cc14d-1661">cartão de debito</span></span> 
- <span data-ttu-id="cc14d-1662">cartão de débito</span><span class="sxs-lookup"><span data-stu-id="cc14d-1662">cartão de débito</span></span> 
- <span data-ttu-id="cc14d-1663">cb</span><span class="sxs-lookup"><span data-stu-id="cc14d-1663">cb</span></span> 
- <span data-ttu-id="cc14d-1664">CCN</span><span class="sxs-lookup"><span data-stu-id="cc14d-1664">ccn</span></span> 
- <span data-ttu-id="cc14d-1665">check card</span><span class="sxs-lookup"><span data-stu-id="cc14d-1665">check card</span></span> 
- <span data-ttu-id="cc14d-1666">check cards</span><span class="sxs-lookup"><span data-stu-id="cc14d-1666">check cards</span></span> 
- <span data-ttu-id="cc14d-1667">checkcard</span><span class="sxs-lookup"><span data-stu-id="cc14d-1667">checkcard</span></span>
- <span data-ttu-id="cc14d-1668">checkcards</span><span class="sxs-lookup"><span data-stu-id="cc14d-1668">checkcards</span></span> 
- <span data-ttu-id="cc14d-1669">chequekaart</span><span class="sxs-lookup"><span data-stu-id="cc14d-1669">chequekaart</span></span> 
- <span data-ttu-id="cc14d-1670">Cirrus</span><span class="sxs-lookup"><span data-stu-id="cc14d-1670">cirrus</span></span> 
- <span data-ttu-id="cc14d-1671">Cirrus-EDC-maestro</span><span class="sxs-lookup"><span data-stu-id="cc14d-1671">cirrus-edc-maestro</span></span> 
- <span data-ttu-id="cc14d-1672">controlekaart</span><span class="sxs-lookup"><span data-stu-id="cc14d-1672">controlekaart</span></span> 
- <span data-ttu-id="cc14d-1673">controlekaarten</span><span class="sxs-lookup"><span data-stu-id="cc14d-1673">controlekaarten</span></span> 
- <span data-ttu-id="cc14d-1674">credit card</span><span class="sxs-lookup"><span data-stu-id="cc14d-1674">credit card</span></span> 
- <span data-ttu-id="cc14d-1675">credit cards</span><span class="sxs-lookup"><span data-stu-id="cc14d-1675">credit cards</span></span> 
- <span data-ttu-id="cc14d-1676">CreditCard</span><span class="sxs-lookup"><span data-stu-id="cc14d-1676">creditcard</span></span> 
- <span data-ttu-id="cc14d-1677">CreditCards</span><span class="sxs-lookup"><span data-stu-id="cc14d-1677">creditcards</span></span> 
- <span data-ttu-id="cc14d-1678">debetkaart</span><span class="sxs-lookup"><span data-stu-id="cc14d-1678">debetkaart</span></span> 
- <span data-ttu-id="cc14d-1679">debetkaarten</span><span class="sxs-lookup"><span data-stu-id="cc14d-1679">debetkaarten</span></span> 
- <span data-ttu-id="cc14d-1680">debit card</span><span class="sxs-lookup"><span data-stu-id="cc14d-1680">debit card</span></span> 
- <span data-ttu-id="cc14d-1681">debit cards</span><span class="sxs-lookup"><span data-stu-id="cc14d-1681">debit cards</span></span> 
- <span data-ttu-id="cc14d-1682">Debitcard</span><span class="sxs-lookup"><span data-stu-id="cc14d-1682">debitcard</span></span> 
- <span data-ttu-id="cc14d-1683">debitcards</span><span class="sxs-lookup"><span data-stu-id="cc14d-1683">debitcards</span></span> 
- <span data-ttu-id="cc14d-1684">debito automatico</span><span class="sxs-lookup"><span data-stu-id="cc14d-1684">debito automatico</span></span> 
- <span data-ttu-id="cc14d-1685">diners club</span><span class="sxs-lookup"><span data-stu-id="cc14d-1685">diners club</span></span> 
- <span data-ttu-id="cc14d-1686">Dinersclub</span><span class="sxs-lookup"><span data-stu-id="cc14d-1686">dinersclub</span></span> 
- <span data-ttu-id="cc14d-1687">tect</span><span class="sxs-lookup"><span data-stu-id="cc14d-1687">discover</span></span> 
- <span data-ttu-id="cc14d-1688">discover card</span><span class="sxs-lookup"><span data-stu-id="cc14d-1688">discover card</span></span> 
- <span data-ttu-id="cc14d-1689">discover cards</span><span class="sxs-lookup"><span data-stu-id="cc14d-1689">discover cards</span></span> 
- <span data-ttu-id="cc14d-1690">DiscoverCard</span><span class="sxs-lookup"><span data-stu-id="cc14d-1690">discovercard</span></span> 
- <span data-ttu-id="cc14d-1691">discovercards</span><span class="sxs-lookup"><span data-stu-id="cc14d-1691">discovercards</span></span> 
- <span data-ttu-id="cc14d-1692">débito automático</span><span class="sxs-lookup"><span data-stu-id="cc14d-1692">débito automático</span></span>
- <span data-ttu-id="cc14d-1693">EDC</span><span class="sxs-lookup"><span data-stu-id="cc14d-1693">edc</span></span> 
- <span data-ttu-id="cc14d-1694">eigentümername</span><span class="sxs-lookup"><span data-stu-id="cc14d-1694">eigentümername</span></span> 
- <span data-ttu-id="cc14d-1695">european debit card</span><span class="sxs-lookup"><span data-stu-id="cc14d-1695">european debit card</span></span> 
- <span data-ttu-id="cc14d-1696">hoofdkaart</span><span class="sxs-lookup"><span data-stu-id="cc14d-1696">hoofdkaart</span></span> 
- <span data-ttu-id="cc14d-1697">hoofdkaarten</span><span class="sxs-lookup"><span data-stu-id="cc14d-1697">hoofdkaarten</span></span> 
- <span data-ttu-id="cc14d-1698">in viaggio</span><span class="sxs-lookup"><span data-stu-id="cc14d-1698">in viaggio</span></span> 
- <span data-ttu-id="cc14d-1699">japanese card bureau</span><span class="sxs-lookup"><span data-stu-id="cc14d-1699">japanese card bureau</span></span> 
- <span data-ttu-id="cc14d-1700">japanse kaartdienst</span><span class="sxs-lookup"><span data-stu-id="cc14d-1700">japanse kaartdienst</span></span> 
- <span data-ttu-id="cc14d-1701">JCB</span><span class="sxs-lookup"><span data-stu-id="cc14d-1701">jcb</span></span> 
- <span data-ttu-id="cc14d-1702">kaart</span><span class="sxs-lookup"><span data-stu-id="cc14d-1702">kaart</span></span> 
- <span data-ttu-id="cc14d-1703">kaart num</span><span class="sxs-lookup"><span data-stu-id="cc14d-1703">kaart num</span></span> 
- <span data-ttu-id="cc14d-1704">kaartaantal</span><span class="sxs-lookup"><span data-stu-id="cc14d-1704">kaartaantal</span></span> 
- <span data-ttu-id="cc14d-1705">kaartaantallen</span><span class="sxs-lookup"><span data-stu-id="cc14d-1705">kaartaantallen</span></span> 
- <span data-ttu-id="cc14d-1706">kaarthouder</span><span class="sxs-lookup"><span data-stu-id="cc14d-1706">kaarthouder</span></span> 
- <span data-ttu-id="cc14d-1707">kaarthouders</span><span class="sxs-lookup"><span data-stu-id="cc14d-1707">kaarthouders</span></span> 
- <span data-ttu-id="cc14d-1708">Karte</span><span class="sxs-lookup"><span data-stu-id="cc14d-1708">karte</span></span>  
- <span data-ttu-id="cc14d-1709">karteninhaber</span><span class="sxs-lookup"><span data-stu-id="cc14d-1709">karteninhaber</span></span> 
- <span data-ttu-id="cc14d-1710">karteninhabers</span><span class="sxs-lookup"><span data-stu-id="cc14d-1710">karteninhabers</span></span>
- <span data-ttu-id="cc14d-1711">kartennr</span><span class="sxs-lookup"><span data-stu-id="cc14d-1711">kartennr</span></span> 
- <span data-ttu-id="cc14d-1712">kartennummer</span><span class="sxs-lookup"><span data-stu-id="cc14d-1712">kartennummer</span></span> 
- <span data-ttu-id="cc14d-1713">kreditkarte</span><span class="sxs-lookup"><span data-stu-id="cc14d-1713">kreditkarte</span></span> 
- <span data-ttu-id="cc14d-1714">kreditkarten-Nummer</span><span class="sxs-lookup"><span data-stu-id="cc14d-1714">kreditkarten-nummer</span></span> 
- <span data-ttu-id="cc14d-1715">kreditkarteninhaber</span><span class="sxs-lookup"><span data-stu-id="cc14d-1715">kreditkarteninhaber</span></span> 
- <span data-ttu-id="cc14d-1716">kreditkarteninstitut</span><span class="sxs-lookup"><span data-stu-id="cc14d-1716">kreditkarteninstitut</span></span> 
- <span data-ttu-id="cc14d-1717">kreditkartennummer</span><span class="sxs-lookup"><span data-stu-id="cc14d-1717">kreditkartennummer</span></span> 
- <span data-ttu-id="cc14d-1718">kreditkartentyp</span><span class="sxs-lookup"><span data-stu-id="cc14d-1718">kreditkartentyp</span></span> 
- <span data-ttu-id="cc14d-1719">Maestro</span><span class="sxs-lookup"><span data-stu-id="cc14d-1719">maestro</span></span> 
- <span data-ttu-id="cc14d-1720">master card</span><span class="sxs-lookup"><span data-stu-id="cc14d-1720">master card</span></span> 
- <span data-ttu-id="cc14d-1721">master cards</span><span class="sxs-lookup"><span data-stu-id="cc14d-1721">master cards</span></span> 
- <span data-ttu-id="cc14d-1722">MasterCard</span><span class="sxs-lookup"><span data-stu-id="cc14d-1722">mastercard</span></span> 
- <span data-ttu-id="cc14d-1723">MasterCards</span><span class="sxs-lookup"><span data-stu-id="cc14d-1723">mastercards</span></span> 
- <span data-ttu-id="cc14d-1724">MC</span><span class="sxs-lookup"><span data-stu-id="cc14d-1724">mc</span></span> 
- <span data-ttu-id="cc14d-1725">mister cash</span><span class="sxs-lookup"><span data-stu-id="cc14d-1725">mister cash</span></span> 
- <span data-ttu-id="cc14d-1726">n carta</span><span class="sxs-lookup"><span data-stu-id="cc14d-1726">n carta</span></span> 
- <span data-ttu-id="cc14d-1727">carta</span><span class="sxs-lookup"><span data-stu-id="cc14d-1727">carta</span></span> 
- <span data-ttu-id="cc14d-1728">no de tarjeta</span><span class="sxs-lookup"><span data-stu-id="cc14d-1728">no de tarjeta</span></span> 
- <span data-ttu-id="cc14d-1729">no do cartao</span><span class="sxs-lookup"><span data-stu-id="cc14d-1729">no do cartao</span></span> 
- <span data-ttu-id="cc14d-1730">no do cartão</span><span class="sxs-lookup"><span data-stu-id="cc14d-1730">no do cartão</span></span> 
- <span data-ttu-id="cc14d-1731">Não.</span><span class="sxs-lookup"><span data-stu-id="cc14d-1731">no.</span></span> <span data-ttu-id="cc14d-1732">de tarjeta</span><span class="sxs-lookup"><span data-stu-id="cc14d-1732">de tarjeta</span></span> 
- <span data-ttu-id="cc14d-1733">Não.</span><span class="sxs-lookup"><span data-stu-id="cc14d-1733">no.</span></span> <span data-ttu-id="cc14d-1734">do cartao</span><span class="sxs-lookup"><span data-stu-id="cc14d-1734">do cartao</span></span> 
- <span data-ttu-id="cc14d-1735">Não.</span><span class="sxs-lookup"><span data-stu-id="cc14d-1735">no.</span></span> <span data-ttu-id="cc14d-1736">do cartão</span><span class="sxs-lookup"><span data-stu-id="cc14d-1736">do cartão</span></span> 
- <span data-ttu-id="cc14d-1737">nr carta</span><span class="sxs-lookup"><span data-stu-id="cc14d-1737">nr carta</span></span> 
- <span data-ttu-id="cc14d-1738">Nr.</span><span class="sxs-lookup"><span data-stu-id="cc14d-1738">nr.</span></span> <span data-ttu-id="cc14d-1739">carta</span><span class="sxs-lookup"><span data-stu-id="cc14d-1739">carta</span></span> 
- <span data-ttu-id="cc14d-1740">numeri di scheda</span><span class="sxs-lookup"><span data-stu-id="cc14d-1740">numeri di scheda</span></span> 
- <span data-ttu-id="cc14d-1741">numero carta</span><span class="sxs-lookup"><span data-stu-id="cc14d-1741">numero carta</span></span> 
- <span data-ttu-id="cc14d-1742">numero de cartao</span><span class="sxs-lookup"><span data-stu-id="cc14d-1742">numero de cartao</span></span> 
- <span data-ttu-id="cc14d-1743">numero de carte</span><span class="sxs-lookup"><span data-stu-id="cc14d-1743">numero de carte</span></span> 
- <span data-ttu-id="cc14d-1744">numero de cartão</span><span class="sxs-lookup"><span data-stu-id="cc14d-1744">numero de cartão</span></span> 
- <span data-ttu-id="cc14d-1745">numero de tarjeta</span><span class="sxs-lookup"><span data-stu-id="cc14d-1745">numero de tarjeta</span></span>
- <span data-ttu-id="cc14d-1746">numero della carta</span><span class="sxs-lookup"><span data-stu-id="cc14d-1746">numero della carta</span></span> 
- <span data-ttu-id="cc14d-1747">numero di carta</span><span class="sxs-lookup"><span data-stu-id="cc14d-1747">numero di carta</span></span> 
- <span data-ttu-id="cc14d-1748">numero di scheda</span><span class="sxs-lookup"><span data-stu-id="cc14d-1748">numero di scheda</span></span> 
- <span data-ttu-id="cc14d-1749">numero do cartao</span><span class="sxs-lookup"><span data-stu-id="cc14d-1749">numero do cartao</span></span> 
- <span data-ttu-id="cc14d-1750">numero do cartão</span><span class="sxs-lookup"><span data-stu-id="cc14d-1750">numero do cartão</span></span> 
- <span data-ttu-id="cc14d-1751">numéro de carte</span><span class="sxs-lookup"><span data-stu-id="cc14d-1751">numéro de carte</span></span> 
- <span data-ttu-id="cc14d-1752">nº carta</span><span class="sxs-lookup"><span data-stu-id="cc14d-1752">nº carta</span></span> 
- <span data-ttu-id="cc14d-1753">nº de carte</span><span class="sxs-lookup"><span data-stu-id="cc14d-1753">nº de carte</span></span> 
- <span data-ttu-id="cc14d-1754">nº de la carte</span><span class="sxs-lookup"><span data-stu-id="cc14d-1754">nº de la carte</span></span> 
- <span data-ttu-id="cc14d-1755">nº de tarjeta</span><span class="sxs-lookup"><span data-stu-id="cc14d-1755">nº de tarjeta</span></span> 
- <span data-ttu-id="cc14d-1756">nº do cartao</span><span class="sxs-lookup"><span data-stu-id="cc14d-1756">nº do cartao</span></span> 
- <span data-ttu-id="cc14d-1757">nº do cartão</span><span class="sxs-lookup"><span data-stu-id="cc14d-1757">nº do cartão</span></span> 
- <span data-ttu-id="cc14d-1758">n º.</span><span class="sxs-lookup"><span data-stu-id="cc14d-1758">nº.</span></span> <span data-ttu-id="cc14d-1759">do cartão</span><span class="sxs-lookup"><span data-stu-id="cc14d-1759">do cartão</span></span> 
- <span data-ttu-id="cc14d-1760">número de cartao</span><span class="sxs-lookup"><span data-stu-id="cc14d-1760">número de cartao</span></span> 
- <span data-ttu-id="cc14d-1761">número de cartão</span><span class="sxs-lookup"><span data-stu-id="cc14d-1761">número de cartão</span></span> 
- <span data-ttu-id="cc14d-1762">número de tarjeta</span><span class="sxs-lookup"><span data-stu-id="cc14d-1762">número de tarjeta</span></span> 
- <span data-ttu-id="cc14d-1763">número do cartao</span><span class="sxs-lookup"><span data-stu-id="cc14d-1763">número do cartao</span></span> 
- <span data-ttu-id="cc14d-1764">scheda dell'assegno</span><span class="sxs-lookup"><span data-stu-id="cc14d-1764">scheda dell'assegno</span></span> 
- <span data-ttu-id="cc14d-1765">scheda dell'atmosfera</span><span class="sxs-lookup"><span data-stu-id="cc14d-1765">scheda dell'atmosfera</span></span> 
- <span data-ttu-id="cc14d-1766">scheda dell'atmosfera</span><span class="sxs-lookup"><span data-stu-id="cc14d-1766">scheda dell'atmosfera</span></span> 
- <span data-ttu-id="cc14d-1767">scheda della banca</span><span class="sxs-lookup"><span data-stu-id="cc14d-1767">scheda della banca</span></span> 
- <span data-ttu-id="cc14d-1768">scheda di controllo</span><span class="sxs-lookup"><span data-stu-id="cc14d-1768">scheda di controllo</span></span> 
- <span data-ttu-id="cc14d-1769">scheda di debito</span><span class="sxs-lookup"><span data-stu-id="cc14d-1769">scheda di debito</span></span> 
- <span data-ttu-id="cc14d-1770">scheda matrice</span><span class="sxs-lookup"><span data-stu-id="cc14d-1770">scheda matrice</span></span> 
- <span data-ttu-id="cc14d-1771">schede dell'atmosfera</span><span class="sxs-lookup"><span data-stu-id="cc14d-1771">schede dell'atmosfera</span></span> 
- <span data-ttu-id="cc14d-1772">schede di controllo</span><span class="sxs-lookup"><span data-stu-id="cc14d-1772">schede di controllo</span></span> 
- <span data-ttu-id="cc14d-1773">schede di debito</span><span class="sxs-lookup"><span data-stu-id="cc14d-1773">schede di debito</span></span> 
- <span data-ttu-id="cc14d-1774">schede matrici</span><span class="sxs-lookup"><span data-stu-id="cc14d-1774">schede matrici</span></span> 
- <span data-ttu-id="cc14d-1775">scoprono la scheda</span><span class="sxs-lookup"><span data-stu-id="cc14d-1775">scoprono la scheda</span></span> 
- <span data-ttu-id="cc14d-1776">scoprono le schede</span><span class="sxs-lookup"><span data-stu-id="cc14d-1776">scoprono le schede</span></span> 
- <span data-ttu-id="cc14d-1777">individual</span><span class="sxs-lookup"><span data-stu-id="cc14d-1777">solo</span></span> 
- <span data-ttu-id="cc14d-1778">supporti di scheda</span><span class="sxs-lookup"><span data-stu-id="cc14d-1778">supporti di scheda</span></span> 
- <span data-ttu-id="cc14d-1779">supporto di scheda</span><span class="sxs-lookup"><span data-stu-id="cc14d-1779">supporto di scheda</span></span> 
- <span data-ttu-id="cc14d-1780">Vá</span><span class="sxs-lookup"><span data-stu-id="cc14d-1780">switch</span></span> 
- <span data-ttu-id="cc14d-1781">tarjeta atm</span><span class="sxs-lookup"><span data-stu-id="cc14d-1781">tarjeta atm</span></span> 
- <span data-ttu-id="cc14d-1782">tarjeta credito</span><span class="sxs-lookup"><span data-stu-id="cc14d-1782">tarjeta credito</span></span> 
- <span data-ttu-id="cc14d-1783">tarjeta de atm</span><span class="sxs-lookup"><span data-stu-id="cc14d-1783">tarjeta de atm</span></span> 
- <span data-ttu-id="cc14d-1784">tarjeta de credito</span><span class="sxs-lookup"><span data-stu-id="cc14d-1784">tarjeta de credito</span></span> 
- <span data-ttu-id="cc14d-1785">tarjeta de debito</span><span class="sxs-lookup"><span data-stu-id="cc14d-1785">tarjeta de debito</span></span> 
- <span data-ttu-id="cc14d-1786">tarjeta debito</span><span class="sxs-lookup"><span data-stu-id="cc14d-1786">tarjeta debito</span></span> 
- <span data-ttu-id="cc14d-1787">tarjeta no</span><span class="sxs-lookup"><span data-stu-id="cc14d-1787">tarjeta no</span></span>
- <span data-ttu-id="cc14d-1788">tarjetahabiente</span><span class="sxs-lookup"><span data-stu-id="cc14d-1788">tarjetahabiente</span></span> 
- <span data-ttu-id="cc14d-1789">tipo della scheda</span><span class="sxs-lookup"><span data-stu-id="cc14d-1789">tipo della scheda</span></span> 
- <span data-ttu-id="cc14d-1790">ufficio giapponese della</span><span class="sxs-lookup"><span data-stu-id="cc14d-1790">ufficio giapponese della</span></span> 
- <span data-ttu-id="cc14d-1791">scheda</span><span class="sxs-lookup"><span data-stu-id="cc14d-1791">scheda</span></span> 
- <span data-ttu-id="cc14d-1792">v pay</span><span class="sxs-lookup"><span data-stu-id="cc14d-1792">v pay</span></span> 
- <span data-ttu-id="cc14d-1793">v-Pay</span><span class="sxs-lookup"><span data-stu-id="cc14d-1793">v-pay</span></span> 
- <span data-ttu-id="cc14d-1794">cartões</span><span class="sxs-lookup"><span data-stu-id="cc14d-1794">visa</span></span> 
- <span data-ttu-id="cc14d-1795">visa plus</span><span class="sxs-lookup"><span data-stu-id="cc14d-1795">visa plus</span></span> 
- <span data-ttu-id="cc14d-1796">visa electron</span><span class="sxs-lookup"><span data-stu-id="cc14d-1796">visa electron</span></span> 
- <span data-ttu-id="cc14d-1797">previsto</span><span class="sxs-lookup"><span data-stu-id="cc14d-1797">visto</span></span> 
- <span data-ttu-id="cc14d-1798">visum</span><span class="sxs-lookup"><span data-stu-id="cc14d-1798">visum</span></span> 
- <span data-ttu-id="cc14d-1799">vpay</span><span class="sxs-lookup"><span data-stu-id="cc14d-1799">vpay</span></span>   

#### <a name="keywordcardsecuritytermsdict"></a><span data-ttu-id="cc14d-1800">Keyword_card_security_terms_dict</span><span class="sxs-lookup"><span data-stu-id="cc14d-1800">Keyword_card_security_terms_dict</span></span>

- <span data-ttu-id="cc14d-1801">card identification number</span><span class="sxs-lookup"><span data-stu-id="cc14d-1801">card identification number</span></span>
- <span data-ttu-id="cc14d-1802">card verification</span><span class="sxs-lookup"><span data-stu-id="cc14d-1802">card verification</span></span> 
- <span data-ttu-id="cc14d-1803">cardi la verifica</span><span class="sxs-lookup"><span data-stu-id="cc14d-1803">cardi la verifica</span></span> 
- <span data-ttu-id="cc14d-1804">CID</span><span class="sxs-lookup"><span data-stu-id="cc14d-1804">cid</span></span> 
- <span data-ttu-id="cc14d-1805">cod seg</span><span class="sxs-lookup"><span data-stu-id="cc14d-1805">cod seg</span></span> 
- <span data-ttu-id="cc14d-1806">cod seguranca</span><span class="sxs-lookup"><span data-stu-id="cc14d-1806">cod seguranca</span></span> 
- <span data-ttu-id="cc14d-1807">cod segurança</span><span class="sxs-lookup"><span data-stu-id="cc14d-1807">cod segurança</span></span> 
- <span data-ttu-id="cc14d-1808">cod sicurezza</span><span class="sxs-lookup"><span data-stu-id="cc14d-1808">cod sicurezza</span></span> 
- <span data-ttu-id="cc14d-1809">COD.</span><span class="sxs-lookup"><span data-stu-id="cc14d-1809">cod.</span></span> <span data-ttu-id="cc14d-1810">seg</span><span class="sxs-lookup"><span data-stu-id="cc14d-1810">seg</span></span> 
- <span data-ttu-id="cc14d-1811">COD.</span><span class="sxs-lookup"><span data-stu-id="cc14d-1811">cod.</span></span> <span data-ttu-id="cc14d-1812">seguranca</span><span class="sxs-lookup"><span data-stu-id="cc14d-1812">seguranca</span></span> 
- <span data-ttu-id="cc14d-1813">COD.</span><span class="sxs-lookup"><span data-stu-id="cc14d-1813">cod.</span></span> <span data-ttu-id="cc14d-1814">segurança</span><span class="sxs-lookup"><span data-stu-id="cc14d-1814">segurança</span></span> 
- <span data-ttu-id="cc14d-1815">COD.</span><span class="sxs-lookup"><span data-stu-id="cc14d-1815">cod.</span></span> <span data-ttu-id="cc14d-1816">sicurezza</span><span class="sxs-lookup"><span data-stu-id="cc14d-1816">sicurezza</span></span> 
- <span data-ttu-id="cc14d-1817">codice di sicurezza</span><span class="sxs-lookup"><span data-stu-id="cc14d-1817">codice di sicurezza</span></span> 
- <span data-ttu-id="cc14d-1818">codice di verifica</span><span class="sxs-lookup"><span data-stu-id="cc14d-1818">codice di verifica</span></span> 
- <span data-ttu-id="cc14d-1819">codigo</span><span class="sxs-lookup"><span data-stu-id="cc14d-1819">codigo</span></span> 
- <span data-ttu-id="cc14d-1820">codigo de seguranca</span><span class="sxs-lookup"><span data-stu-id="cc14d-1820">codigo de seguranca</span></span> 
- <span data-ttu-id="cc14d-1821">codigo de segurança</span><span class="sxs-lookup"><span data-stu-id="cc14d-1821">codigo de segurança</span></span> 
- <span data-ttu-id="cc14d-1822">crittogramma</span><span class="sxs-lookup"><span data-stu-id="cc14d-1822">crittogramma</span></span> 
- <span data-ttu-id="cc14d-1823">cryptogram</span><span class="sxs-lookup"><span data-stu-id="cc14d-1823">cryptogram</span></span> 
- <span data-ttu-id="cc14d-1824">cryptogramme</span><span class="sxs-lookup"><span data-stu-id="cc14d-1824">cryptogramme</span></span> 
- <span data-ttu-id="cc14d-1825">CV2</span><span class="sxs-lookup"><span data-stu-id="cc14d-1825">cv2</span></span> 
- <span data-ttu-id="cc14d-1826">CVC</span><span class="sxs-lookup"><span data-stu-id="cc14d-1826">cvc</span></span> 
- <span data-ttu-id="cc14d-1827">CVC2</span><span class="sxs-lookup"><span data-stu-id="cc14d-1827">cvc2</span></span> 
- <span data-ttu-id="cc14d-1828">CVN</span><span class="sxs-lookup"><span data-stu-id="cc14d-1828">cvn</span></span> 
- <span data-ttu-id="cc14d-1829">CVV</span><span class="sxs-lookup"><span data-stu-id="cc14d-1829">cvv</span></span> 
- <span data-ttu-id="cc14d-1830">CVV2</span><span class="sxs-lookup"><span data-stu-id="cc14d-1830">cvv2</span></span> 
- <span data-ttu-id="cc14d-1831">cód seguranca</span><span class="sxs-lookup"><span data-stu-id="cc14d-1831">cód seguranca</span></span> 
- <span data-ttu-id="cc14d-1832">cód segurança</span><span class="sxs-lookup"><span data-stu-id="cc14d-1832">cód segurança</span></span> 
- <span data-ttu-id="cc14d-1833">Cód.</span><span class="sxs-lookup"><span data-stu-id="cc14d-1833">cód.</span></span> <span data-ttu-id="cc14d-1834">seguranca</span><span class="sxs-lookup"><span data-stu-id="cc14d-1834">seguranca</span></span> 
- <span data-ttu-id="cc14d-1835">Cód.</span><span class="sxs-lookup"><span data-stu-id="cc14d-1835">cód.</span></span> <span data-ttu-id="cc14d-1836">segurança</span><span class="sxs-lookup"><span data-stu-id="cc14d-1836">segurança</span></span> 
- <span data-ttu-id="cc14d-1837">CFOP</span><span class="sxs-lookup"><span data-stu-id="cc14d-1837">código</span></span> 
- <span data-ttu-id="cc14d-1838">código de seguranca</span><span class="sxs-lookup"><span data-stu-id="cc14d-1838">código de seguranca</span></span> 
- <span data-ttu-id="cc14d-1839">código de segurança</span><span class="sxs-lookup"><span data-stu-id="cc14d-1839">código de segurança</span></span> 
- <span data-ttu-id="cc14d-1840">de kaart controle</span><span class="sxs-lookup"><span data-stu-id="cc14d-1840">de kaart controle</span></span> 
- <span data-ttu-id="cc14d-1841">geeft nr uit</span><span class="sxs-lookup"><span data-stu-id="cc14d-1841">geeft nr uit</span></span> 
- <span data-ttu-id="cc14d-1842">issue no</span><span class="sxs-lookup"><span data-stu-id="cc14d-1842">issue no</span></span> 
- <span data-ttu-id="cc14d-1843">issue number</span><span class="sxs-lookup"><span data-stu-id="cc14d-1843">issue number</span></span> 
- <span data-ttu-id="cc14d-1844">kaartidentificatienummer</span><span class="sxs-lookup"><span data-stu-id="cc14d-1844">kaartidentificatienummer</span></span> 
- <span data-ttu-id="cc14d-1845">kreditkartenprufnummer</span><span class="sxs-lookup"><span data-stu-id="cc14d-1845">kreditkartenprufnummer</span></span> 
- <span data-ttu-id="cc14d-1846">kreditkartenprüfnummer</span><span class="sxs-lookup"><span data-stu-id="cc14d-1846">kreditkartenprüfnummer</span></span> 
- <span data-ttu-id="cc14d-1847">kwestieaantal</span><span class="sxs-lookup"><span data-stu-id="cc14d-1847">kwestieaantal</span></span> 
- <span data-ttu-id="cc14d-1848">Não.</span><span class="sxs-lookup"><span data-stu-id="cc14d-1848">no.</span></span> <span data-ttu-id="cc14d-1849">dell'edizione</span><span class="sxs-lookup"><span data-stu-id="cc14d-1849">dell'edizione</span></span> 
- <span data-ttu-id="cc14d-1850">Não.</span><span class="sxs-lookup"><span data-stu-id="cc14d-1850">no.</span></span> <span data-ttu-id="cc14d-1851">di sicurezza</span><span class="sxs-lookup"><span data-stu-id="cc14d-1851">di sicurezza</span></span> 
- <span data-ttu-id="cc14d-1852">numero de securite</span><span class="sxs-lookup"><span data-stu-id="cc14d-1852">numero de securite</span></span> 
- <span data-ttu-id="cc14d-1853">numero de verificacao</span><span class="sxs-lookup"><span data-stu-id="cc14d-1853">numero de verificacao</span></span> 
- <span data-ttu-id="cc14d-1854">numero dell'edizione</span><span class="sxs-lookup"><span data-stu-id="cc14d-1854">numero dell'edizione</span></span> 
- <span data-ttu-id="cc14d-1855">numero di identificazione della</span><span class="sxs-lookup"><span data-stu-id="cc14d-1855">numero di identificazione della</span></span> 
- <span data-ttu-id="cc14d-1856">scheda</span><span class="sxs-lookup"><span data-stu-id="cc14d-1856">scheda</span></span> 
- <span data-ttu-id="cc14d-1857">numero di sicurezza</span><span class="sxs-lookup"><span data-stu-id="cc14d-1857">numero di sicurezza</span></span> 
- <span data-ttu-id="cc14d-1858">numero van veiligheid</span><span class="sxs-lookup"><span data-stu-id="cc14d-1858">numero van veiligheid</span></span> 
- <span data-ttu-id="cc14d-1859">numéro de sécurité</span><span class="sxs-lookup"><span data-stu-id="cc14d-1859">numéro de sécurité</span></span> 
- <span data-ttu-id="cc14d-1860">nº autorizzazione</span><span class="sxs-lookup"><span data-stu-id="cc14d-1860">nº autorizzazione</span></span> 
- <span data-ttu-id="cc14d-1861">número de verificação</span><span class="sxs-lookup"><span data-stu-id="cc14d-1861">número de verificação</span></span> 
- <span data-ttu-id="cc14d-1862">perno il blocco</span><span class="sxs-lookup"><span data-stu-id="cc14d-1862">perno il blocco</span></span> 
- <span data-ttu-id="cc14d-1863">pin block</span><span class="sxs-lookup"><span data-stu-id="cc14d-1863">pin block</span></span> 
- <span data-ttu-id="cc14d-1864">prufziffer</span><span class="sxs-lookup"><span data-stu-id="cc14d-1864">prufziffer</span></span> 
- <span data-ttu-id="cc14d-1865">prüfziffer</span><span class="sxs-lookup"><span data-stu-id="cc14d-1865">prüfziffer</span></span> 
- <span data-ttu-id="cc14d-1866">security code</span><span class="sxs-lookup"><span data-stu-id="cc14d-1866">security code</span></span> 
- <span data-ttu-id="cc14d-1867">security no</span><span class="sxs-lookup"><span data-stu-id="cc14d-1867">security no</span></span> 
- <span data-ttu-id="cc14d-1868">security number</span><span class="sxs-lookup"><span data-stu-id="cc14d-1868">security number</span></span> 
- <span data-ttu-id="cc14d-1869">sicherheits kode</span><span class="sxs-lookup"><span data-stu-id="cc14d-1869">sicherheits kode</span></span> 
- <span data-ttu-id="cc14d-1870">sicherheitscode</span><span class="sxs-lookup"><span data-stu-id="cc14d-1870">sicherheitscode</span></span> 
- <span data-ttu-id="cc14d-1871">sicherheitsnummer</span><span class="sxs-lookup"><span data-stu-id="cc14d-1871">sicherheitsnummer</span></span> 
- <span data-ttu-id="cc14d-1872">speldblok</span><span class="sxs-lookup"><span data-stu-id="cc14d-1872">speldblok</span></span> 
- <span data-ttu-id="cc14d-1873">veiligheid nr</span><span class="sxs-lookup"><span data-stu-id="cc14d-1873">veiligheid nr</span></span> 
- <span data-ttu-id="cc14d-1874">veiligheidsaantal</span><span class="sxs-lookup"><span data-stu-id="cc14d-1874">veiligheidsaantal</span></span> 
- <span data-ttu-id="cc14d-1875">veiligheidscode</span><span class="sxs-lookup"><span data-stu-id="cc14d-1875">veiligheidscode</span></span> 
- <span data-ttu-id="cc14d-1876">veiligheidsnummer</span><span class="sxs-lookup"><span data-stu-id="cc14d-1876">veiligheidsnummer</span></span> 
- <span data-ttu-id="cc14d-1877">verfalldatum</span><span class="sxs-lookup"><span data-stu-id="cc14d-1877">verfalldatum</span></span> 

#### <a name="keywordcardexpirationtermsdict"></a><span data-ttu-id="cc14d-1878">Keyword_card_expiration_terms_dict</span><span class="sxs-lookup"><span data-stu-id="cc14d-1878">Keyword_card_expiration_terms_dict</span></span>

- <span data-ttu-id="cc14d-1879">ablauf</span><span class="sxs-lookup"><span data-stu-id="cc14d-1879">ablauf</span></span> 
- <span data-ttu-id="cc14d-1880">data de expiracao</span><span class="sxs-lookup"><span data-stu-id="cc14d-1880">data de expiracao</span></span> 
- <span data-ttu-id="cc14d-1881">data de expiração</span><span class="sxs-lookup"><span data-stu-id="cc14d-1881">data de expiração</span></span> 
- <span data-ttu-id="cc14d-1882">data del exp</span><span class="sxs-lookup"><span data-stu-id="cc14d-1882">data del exp</span></span> 
- <span data-ttu-id="cc14d-1883">data di exp</span><span class="sxs-lookup"><span data-stu-id="cc14d-1883">data di exp</span></span> 
- <span data-ttu-id="cc14d-1884">data di scadenza</span><span class="sxs-lookup"><span data-stu-id="cc14d-1884">data di scadenza</span></span> 
- <span data-ttu-id="cc14d-1885">data em que expira</span><span class="sxs-lookup"><span data-stu-id="cc14d-1885">data em que expira</span></span> 
- <span data-ttu-id="cc14d-1886">data scad</span><span class="sxs-lookup"><span data-stu-id="cc14d-1886">data scad</span></span> 
- <span data-ttu-id="cc14d-1887">data scadenza</span><span class="sxs-lookup"><span data-stu-id="cc14d-1887">data scadenza</span></span> 
- <span data-ttu-id="cc14d-1888">date de validité</span><span class="sxs-lookup"><span data-stu-id="cc14d-1888">date de validité</span></span> 
- <span data-ttu-id="cc14d-1889">datum afloop</span><span class="sxs-lookup"><span data-stu-id="cc14d-1889">datum afloop</span></span> 
- <span data-ttu-id="cc14d-1890">datum van exp</span><span class="sxs-lookup"><span data-stu-id="cc14d-1890">datum van exp</span></span> 
- <span data-ttu-id="cc14d-1891">de afloop</span><span class="sxs-lookup"><span data-stu-id="cc14d-1891">de afloop</span></span> 
- <span data-ttu-id="cc14d-1892">espira</span><span class="sxs-lookup"><span data-stu-id="cc14d-1892">espira</span></span> 
- <span data-ttu-id="cc14d-1893">espira</span><span class="sxs-lookup"><span data-stu-id="cc14d-1893">espira</span></span> 
- <span data-ttu-id="cc14d-1894">exp date</span><span class="sxs-lookup"><span data-stu-id="cc14d-1894">exp date</span></span> 
- <span data-ttu-id="cc14d-1895">exp datum</span><span class="sxs-lookup"><span data-stu-id="cc14d-1895">exp datum</span></span> 
- <span data-ttu-id="cc14d-1896">validade</span><span class="sxs-lookup"><span data-stu-id="cc14d-1896">expiration</span></span> 
- <span data-ttu-id="cc14d-1897">expirar</span><span class="sxs-lookup"><span data-stu-id="cc14d-1897">expire</span></span> 
- <span data-ttu-id="cc14d-1898">expira</span><span class="sxs-lookup"><span data-stu-id="cc14d-1898">expires</span></span> 
- <span data-ttu-id="cc14d-1899">expiração</span><span class="sxs-lookup"><span data-stu-id="cc14d-1899">expiry</span></span> 
- <span data-ttu-id="cc14d-1900">fecha de expiracion</span><span class="sxs-lookup"><span data-stu-id="cc14d-1900">fecha de expiracion</span></span> 
- <span data-ttu-id="cc14d-1901">fecha de venc</span><span class="sxs-lookup"><span data-stu-id="cc14d-1901">fecha de venc</span></span> 
- <span data-ttu-id="cc14d-1902">gultig bis</span><span class="sxs-lookup"><span data-stu-id="cc14d-1902">gultig bis</span></span> 
- <span data-ttu-id="cc14d-1903">gultigkeitsdatum</span><span class="sxs-lookup"><span data-stu-id="cc14d-1903">gultigkeitsdatum</span></span> 
- <span data-ttu-id="cc14d-1904">gültig bis</span><span class="sxs-lookup"><span data-stu-id="cc14d-1904">gültig bis</span></span> 
- <span data-ttu-id="cc14d-1905">gültigkeitsdatum</span><span class="sxs-lookup"><span data-stu-id="cc14d-1905">gültigkeitsdatum</span></span> 
- <span data-ttu-id="cc14d-1906">la scadenza</span><span class="sxs-lookup"><span data-stu-id="cc14d-1906">la scadenza</span></span> 
- <span data-ttu-id="cc14d-1907">scadenza</span><span class="sxs-lookup"><span data-stu-id="cc14d-1907">scadenza</span></span> 
- <span data-ttu-id="cc14d-1908">valable</span><span class="sxs-lookup"><span data-stu-id="cc14d-1908">valable</span></span> 
- <span data-ttu-id="cc14d-1909">validade</span><span class="sxs-lookup"><span data-stu-id="cc14d-1909">validade</span></span> 
- <span data-ttu-id="cc14d-1910">valido hasta</span><span class="sxs-lookup"><span data-stu-id="cc14d-1910">valido hasta</span></span> 
- <span data-ttu-id="cc14d-1911">coragem</span><span class="sxs-lookup"><span data-stu-id="cc14d-1911">valor</span></span> 
- <span data-ttu-id="cc14d-1912">venc</span><span class="sxs-lookup"><span data-stu-id="cc14d-1912">venc</span></span> 
- <span data-ttu-id="cc14d-1913">vencimento</span><span class="sxs-lookup"><span data-stu-id="cc14d-1913">vencimento</span></span> 
- <span data-ttu-id="cc14d-1914">vencimiento</span><span class="sxs-lookup"><span data-stu-id="cc14d-1914">vencimiento</span></span> 
- <span data-ttu-id="cc14d-1915">verloopt</span><span class="sxs-lookup"><span data-stu-id="cc14d-1915">verloopt</span></span> 
- <span data-ttu-id="cc14d-1916">vervaldag</span><span class="sxs-lookup"><span data-stu-id="cc14d-1916">vervaldag</span></span> 
- <span data-ttu-id="cc14d-1917">vervaldatum</span><span class="sxs-lookup"><span data-stu-id="cc14d-1917">vervaldatum</span></span> 
- <span data-ttu-id="cc14d-1918">vto</span><span class="sxs-lookup"><span data-stu-id="cc14d-1918">vto</span></span> 
- <span data-ttu-id="cc14d-1919">válido hasta</span><span class="sxs-lookup"><span data-stu-id="cc14d-1919">válido hasta</span></span> 
   
## <a name="eu-drivers-license-number"></a><span data-ttu-id="cc14d-1920">Número da carteira de motorista da UE</span><span class="sxs-lookup"><span data-stu-id="cc14d-1920">EU Driver's License Number</span></span>

<span data-ttu-id="cc14d-1921">Para saber mais, confira o [tipo de informação confidencial do número da carteira de motorista da UE](eu-driver-s-license-number.md).</span><span class="sxs-lookup"><span data-stu-id="cc14d-1921">To learn more, see [EU Driver's License Number sensitive information type](eu-driver-s-license-number.md).</span></span>
  
## <a name="eu-national-identification-number"></a><span data-ttu-id="cc14d-1922">Número de identificação nacional da UE</span><span class="sxs-lookup"><span data-stu-id="cc14d-1922">EU National Identification Number</span></span>

<span data-ttu-id="cc14d-1923">Para saber mais, confira [tipo de informação confidencial do número de identificação nacional da UE](eu-national-identification-number.md).</span><span class="sxs-lookup"><span data-stu-id="cc14d-1923">To learn more, see [EU National Identification Number sensitive information type](eu-national-identification-number.md).</span></span>
  
## <a name="eu-passport-number"></a><span data-ttu-id="cc14d-1924">Número do Passport da UE</span><span class="sxs-lookup"><span data-stu-id="cc14d-1924">EU Passport Number</span></span>

<span data-ttu-id="cc14d-1925">Para saber mais, veja [tipo de informações confidenciais do número do Passport da UE](eu-passport-number.md).</span><span class="sxs-lookup"><span data-stu-id="cc14d-1925">To learn more, see [EU Passport Number sensitive information type](eu-passport-number.md).</span></span>
  
## <a name="eu-social-security-number-or-equivalent-id"></a><span data-ttu-id="cc14d-1926">Número de seguro social da UE ou ID equivalente</span><span class="sxs-lookup"><span data-stu-id="cc14d-1926">EU Social Security Number or Equivalent ID</span></span>

<span data-ttu-id="cc14d-1927">Para saber mais, confira [número de seguridade social da UE ou tipo de informação confidencial de ID equivalente](eu-social-security-number-or-equivalent-id.md).</span><span class="sxs-lookup"><span data-stu-id="cc14d-1927">To learn more, see [EU Social Security Number or Equivalent ID sensitive information type](eu-social-security-number-or-equivalent-id.md).</span></span>
  
## <a name="eu-tax-identification-number"></a><span data-ttu-id="cc14d-1928">Número de identificação do imposto da UE</span><span class="sxs-lookup"><span data-stu-id="cc14d-1928">EU Tax Identification Number</span></span>

<span data-ttu-id="cc14d-1929">Para saber mais, confira [número de identificação de imposto da UE tipo de informação confidencial](eu-tax-identification-number.md).</span><span class="sxs-lookup"><span data-stu-id="cc14d-1929">To learn more, see [EU Tax Identification Number sensitive information type](eu-tax-identification-number.md).</span></span>
  
## <a name="finland-national-id"></a><span data-ttu-id="cc14d-1930">ID nacional da Finlândia</span><span class="sxs-lookup"><span data-stu-id="cc14d-1930">Finland National ID</span></span>

### <a name="format"></a><span data-ttu-id="cc14d-1931">Format</span><span class="sxs-lookup"><span data-stu-id="cc14d-1931">Format</span></span>

<span data-ttu-id="cc14d-1932">Seis dígitos mais um caractere indicando um século mais três dígitos mais um dígito de verificação</span><span class="sxs-lookup"><span data-stu-id="cc14d-1932">Six digits plus a character indicating a century plus three digits plus a check digit</span></span>

### <a name="pattern"></a><span data-ttu-id="cc14d-1933">Padrão</span><span class="sxs-lookup"><span data-stu-id="cc14d-1933">Pattern</span></span>

<span data-ttu-id="cc14d-1934">O padrão deve incluir todos os seguintes itens:</span><span class="sxs-lookup"><span data-stu-id="cc14d-1934">Pattern must include all of the following:</span></span>
- <span data-ttu-id="cc14d-1935">Seis dígitos no formato DDMMAA que é uma data de nascimento</span><span class="sxs-lookup"><span data-stu-id="cc14d-1935">Six digits in the format format DDMMYY which are a date of birth</span></span> 
- <span data-ttu-id="cc14d-1936">Marcador do século (qualquer '-', '+' ou 'a')</span><span class="sxs-lookup"><span data-stu-id="cc14d-1936">Century marker (either '-', '+' or 'a')</span></span> 
- <span data-ttu-id="cc14d-1937">Número de identificação pessoal de três dígitos</span><span class="sxs-lookup"><span data-stu-id="cc14d-1937">Three-digit personal identification number</span></span> 
- <span data-ttu-id="cc14d-1938">Um dígito ou letra (não diferencia maiúscula de minúscula), que é um dígito de verificação</span><span class="sxs-lookup"><span data-stu-id="cc14d-1938">A digit or letter (case insensitive) which is a check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="cc14d-1939">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="cc14d-1939">Checksum</span></span>

<span data-ttu-id="cc14d-1940">Sim</span><span class="sxs-lookup"><span data-stu-id="cc14d-1940">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="cc14d-1941">Definição</span><span class="sxs-lookup"><span data-stu-id="cc14d-1941">Definition</span></span>

<span data-ttu-id="cc14d-1942">Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="cc14d-1942">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="cc14d-1943">A função Func_finnish_national_id localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="cc14d-1943">The function Func_finnish_national_id finds content that matches the pattern.</span></span>
- <span data-ttu-id="cc14d-1944">Uma palavra-chave de Keyword_finnish_national_id for encontrada.</span><span class="sxs-lookup"><span data-stu-id="cc14d-1944">A keyword from Keyword_finnish_national_id is found.</span></span>
- <span data-ttu-id="cc14d-1945">A soma de verificação passa.</span><span class="sxs-lookup"><span data-stu-id="cc14d-1945">The checksum passes.</span></span>

```
<!-- Finnish National ID-->
<Entity id="338FD995-4CB5-4F87-AD35-79BD1DD926C1" patternsProximity="300" recommendedConfidence="85">
  <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_finnish_national_id" />
          <Match idRef="Keyword_finnish_national_id" />
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="cc14d-1946">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="cc14d-1946">Keywords</span></span>

- <span data-ttu-id="cc14d-1947">Keyword_finnish_national_id</span><span class="sxs-lookup"><span data-stu-id="cc14d-1947">Keyword_finnish_national_id</span></span>
- <span data-ttu-id="cc14d-1948">Sosiaaliturvatunnus</span><span class="sxs-lookup"><span data-stu-id="cc14d-1948">Sosiaaliturvatunnus</span></span>
- <span data-ttu-id="cc14d-1949">SOTU Henkilötunnus HETU</span><span class="sxs-lookup"><span data-stu-id="cc14d-1949">SOTU Henkilötunnus HETU</span></span>
- <span data-ttu-id="cc14d-1950">Personbeteckning</span><span class="sxs-lookup"><span data-stu-id="cc14d-1950">Personbeteckning</span></span>
- <span data-ttu-id="cc14d-1951">Personnummer</span><span class="sxs-lookup"><span data-stu-id="cc14d-1951">Personnummer</span></span>
   
## <a name="finland-passport-number"></a><span data-ttu-id="cc14d-1952">Número de Passaporte da Finlândia</span><span class="sxs-lookup"><span data-stu-id="cc14d-1952">Finland Passport Number</span></span>

<span data-ttu-id="cc14d-1953">Combinação de formato de nove letras e dígitos combinação de padrões de nove letras e dígitos: duas letras (não diferencia maiúsculas de minúsculas) sete dígitos soma de verificação sem definição uma política de DLP é de 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de um proximidade de 300 caracteres: a expressão regular Regex_finland_passport_number localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="cc14d-1953">Format Combination of nine letters and digits Pattern Combination of nine letters and digits: Two letters (not case sensitive) Seven digits Checksum No Definition A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters: The regular expression Regex_finland_passport_number finds content that matches the pattern.</span></span>
<span data-ttu-id="cc14d-1954">Uma palavra-chave de Keyword_finland_passport_number for encontrada.</span><span class="sxs-lookup"><span data-stu-id="cc14d-1954">A keyword from Keyword_finland_passport_number is found.</span></span>
<span data-ttu-id="cc14d-1955"><!-- Finland Passport Number -->
<Entity id="d1685ac3-1d3a-40f8-8198-32ef5669c7a5" recommendedConfidence="75" patternsProximity="300"> <Pattern confidenceLevel="75"> <IdMatch idRef="Regex_finland_passport_number"/> <Match idRef="Keyword_finland_passport_number"/> </Pattern>
</Entity></span><span class="sxs-lookup"><span data-stu-id="cc14d-1955"></span></span>
<span data-ttu-id="cc14d-1956">Keyword_finland_passport_number de palavras-chave o Passport Passi</span><span class="sxs-lookup"><span data-stu-id="cc14d-1956">Keywords Keyword_finland_passport_number Passport Passi</span></span>
   
## <a name="france-drivers-license-number"></a><span data-ttu-id="cc14d-1957">Número de carteira de motorista da França</span><span class="sxs-lookup"><span data-stu-id="cc14d-1957">France Driver's License Number</span></span>

### <a name="format"></a><span data-ttu-id="cc14d-1958">Format</span><span class="sxs-lookup"><span data-stu-id="cc14d-1958">Format</span></span>

<span data-ttu-id="cc14d-1959">12 dígitos</span><span class="sxs-lookup"><span data-stu-id="cc14d-1959">12 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="cc14d-1960">Padrão</span><span class="sxs-lookup"><span data-stu-id="cc14d-1960">Pattern</span></span>

<span data-ttu-id="cc14d-1961">12 dígitos com a validação para descontar padrões similares, como números de telefone em francês</span><span class="sxs-lookup"><span data-stu-id="cc14d-1961">12 digits with validation to discount similar patterns such as French telephone numbers</span></span>

### <a name="checksum"></a><span data-ttu-id="cc14d-1962">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="cc14d-1962">Checksum</span></span>

<span data-ttu-id="cc14d-1963">Não</span><span class="sxs-lookup"><span data-stu-id="cc14d-1963">No</span></span>

### <a name="definition"></a><span data-ttu-id="cc14d-1964">Definição</span><span class="sxs-lookup"><span data-stu-id="cc14d-1964">Definition</span></span>

<span data-ttu-id="cc14d-1965">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="cc14d-1965">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="cc14d-1966">A função Func_french_drivers_license localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="cc14d-1966">The function Func_french_drivers_license finds content that matches the pattern.</span></span>
- <span data-ttu-id="cc14d-1967">Pelo menos uma das seguintes opções for verdadeira:</span><span class="sxs-lookup"><span data-stu-id="cc14d-1967">At least one of the following is true:</span></span>
- <span data-ttu-id="cc14d-1968">Uma palavra-chave de Keyword_french_drivers_license for encontrada.</span><span class="sxs-lookup"><span data-stu-id="cc14d-1968">A keyword from Keyword_french_drivers_license is found.</span></span>
- <span data-ttu-id="cc14d-1969">A função Func_eu_date encontra uma data no formato de data à direita.</span><span class="sxs-lookup"><span data-stu-id="cc14d-1969">The function Func_eu_date finds a date in the right date format.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="cc14d-1970">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="cc14d-1970">Keywords</span></span>

#### <a name="keywordfrenchdriverslicense"></a><span data-ttu-id="cc14d-1971">Keyword_french_drivers_license</span><span class="sxs-lookup"><span data-stu-id="cc14d-1971">Keyword_french_drivers_license</span></span>

- <span data-ttu-id="cc14d-1972">drivers licence</span><span class="sxs-lookup"><span data-stu-id="cc14d-1972">drivers licence</span></span>
- <span data-ttu-id="cc14d-1973">drivers license</span><span class="sxs-lookup"><span data-stu-id="cc14d-1973">drivers license</span></span>
- <span data-ttu-id="cc14d-1974">driving licence</span><span class="sxs-lookup"><span data-stu-id="cc14d-1974">driving licence</span></span>
- <span data-ttu-id="cc14d-1975">driving licence</span><span class="sxs-lookup"><span data-stu-id="cc14d-1975">driving license</span></span>
- <span data-ttu-id="cc14d-1976">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="cc14d-1976">permis de conduire</span></span>
- <span data-ttu-id="cc14d-1977">licence number</span><span class="sxs-lookup"><span data-stu-id="cc14d-1977">licence number</span></span>
- <span data-ttu-id="cc14d-1978">license number</span><span class="sxs-lookup"><span data-stu-id="cc14d-1978">license number</span></span>
- <span data-ttu-id="cc14d-1979">licence numbers</span><span class="sxs-lookup"><span data-stu-id="cc14d-1979">licence numbers</span></span>
- <span data-ttu-id="cc14d-1980">license numbers</span><span class="sxs-lookup"><span data-stu-id="cc14d-1980">license numbers</span></span>

## <a name="france-national-id-card-cni"></a><span data-ttu-id="cc14d-1981">Cartão de identificação nacional da França (CNI)</span><span class="sxs-lookup"><span data-stu-id="cc14d-1981">France National ID Card (CNI)</span></span>

### <a name="format"></a><span data-ttu-id="cc14d-1982">Format</span><span class="sxs-lookup"><span data-stu-id="cc14d-1982">Format</span></span>

<span data-ttu-id="cc14d-1983">12 dígitos</span><span class="sxs-lookup"><span data-stu-id="cc14d-1983">12 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="cc14d-1984">Padrão</span><span class="sxs-lookup"><span data-stu-id="cc14d-1984">Pattern</span></span>

<span data-ttu-id="cc14d-1985">12 dígitos</span><span class="sxs-lookup"><span data-stu-id="cc14d-1985">12 digits</span></span>

### <a name="checksum"></a><span data-ttu-id="cc14d-1986">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="cc14d-1986">Checksum</span></span>

<span data-ttu-id="cc14d-1987">Não</span><span class="sxs-lookup"><span data-stu-id="cc14d-1987">No</span></span>

### <a name="definition"></a><span data-ttu-id="cc14d-1988">Definição</span><span class="sxs-lookup"><span data-stu-id="cc14d-1988">Definition</span></span>

<span data-ttu-id="cc14d-1989">Uma política de DLP tem 65% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="cc14d-1989">A DLP policy is 65% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="cc14d-1990">A expressão regular Regex_france_cni localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="cc14d-1990">The regular expression Regex_france_cni finds content that matches the pattern.</span></span>

```
<!-- France CNI -->
<Entity id="f741ac74-1bc0-4665-b69b-f0c7f927c0c4" patternsProximity="300" recommendedConfidence="65">
  <Pattern confidenceLevel="65">
        <IdMatch idRef="Regex_france_cni" />
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="cc14d-1991">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="cc14d-1991">Keywords</span></span>

<span data-ttu-id="cc14d-1992">Nenhum</span><span class="sxs-lookup"><span data-stu-id="cc14d-1992">None</span></span>
   
## <a name="france-passport-number"></a><span data-ttu-id="cc14d-1993">Número de passaporte da França</span><span class="sxs-lookup"><span data-stu-id="cc14d-1993">France Passport Number</span></span>

### <a name="format"></a><span data-ttu-id="cc14d-1994">Format</span><span class="sxs-lookup"><span data-stu-id="cc14d-1994">Format</span></span>

<span data-ttu-id="cc14d-1995">Nove letras e dígitos</span><span class="sxs-lookup"><span data-stu-id="cc14d-1995">Nine digits and letters</span></span>

### <a name="pattern"></a><span data-ttu-id="cc14d-1996">Padrão</span><span class="sxs-lookup"><span data-stu-id="cc14d-1996">Pattern</span></span>

<span data-ttu-id="cc14d-1997">Nove letras e dígitos:</span><span class="sxs-lookup"><span data-stu-id="cc14d-1997">Nine digits and letters:</span></span>
- <span data-ttu-id="cc14d-1998">Dois dígitos</span><span class="sxs-lookup"><span data-stu-id="cc14d-1998">Two digits</span></span> 
- <span data-ttu-id="cc14d-1999">Duas letras (não diferenciam maiúsculas de minúsculas)</span><span class="sxs-lookup"><span data-stu-id="cc14d-1999">Two letters (not case sensitive)</span></span> 
- <span data-ttu-id="cc14d-2000">Cinco dígitos</span><span class="sxs-lookup"><span data-stu-id="cc14d-2000">Five digits</span></span>

### <a name="checksum"></a><span data-ttu-id="cc14d-2001">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="cc14d-2001">Checksum</span></span>

<span data-ttu-id="cc14d-2002">Não</span><span class="sxs-lookup"><span data-stu-id="cc14d-2002">No</span></span>

### <a name="definition"></a><span data-ttu-id="cc14d-2003">Definição</span><span class="sxs-lookup"><span data-stu-id="cc14d-2003">Definition</span></span>

<span data-ttu-id="cc14d-2004">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="cc14d-2004">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="cc14d-2005">A função Func_fr_passport localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="cc14d-2005">The function Func_fr_passport finds content that matches the pattern.</span></span>
- <span data-ttu-id="cc14d-2006">Uma palavra-chave de Keyword_passport for encontrada.</span><span class="sxs-lookup"><span data-stu-id="cc14d-2006">A keyword from Keyword_passport is found.</span></span>

```
<!-- France Passport Number -->
<Entity id="3008b884-8c8c-4cd8-a289-99f34fc7ff5d" patternsProximity="300" recommendedConfidence="75">
  <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_fr_passport" />
        <Match idRef="Keyword_passport" />
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="cc14d-2007">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="cc14d-2007">Keywords</span></span>

#### <a name="keywordpassport"></a><span data-ttu-id="cc14d-2008">Keyword_passport</span><span class="sxs-lookup"><span data-stu-id="cc14d-2008">Keyword_passport</span></span>

- <span data-ttu-id="cc14d-2009">Passport Number</span><span class="sxs-lookup"><span data-stu-id="cc14d-2009">Passport Number</span></span>
- <span data-ttu-id="cc14d-2010">Passport No</span><span class="sxs-lookup"><span data-stu-id="cc14d-2010">Passport No</span></span>
- <span data-ttu-id="cc14d-2011">Passport #</span><span class="sxs-lookup"><span data-stu-id="cc14d-2011">Passport #</span></span>
- <span data-ttu-id="cc14d-2012">Passaport</span><span class="sxs-lookup"><span data-stu-id="cc14d-2012">Passport#</span></span>
- <span data-ttu-id="cc14d-2013">Passportid</span><span class="sxs-lookup"><span data-stu-id="cc14d-2013">PassportID</span></span>
- <span data-ttu-id="cc14d-2014">Passportno</span><span class="sxs-lookup"><span data-stu-id="cc14d-2014">Passportno</span></span>
- <span data-ttu-id="cc14d-2015">passportnumber</span><span class="sxs-lookup"><span data-stu-id="cc14d-2015">passportnumber</span></span>
- <span data-ttu-id="cc14d-2016">パスポート</span><span class="sxs-lookup"><span data-stu-id="cc14d-2016">パスポート</span></span>
- <span data-ttu-id="cc14d-2017">パスポート番号</span><span class="sxs-lookup"><span data-stu-id="cc14d-2017">パスポート番号</span></span>
- <span data-ttu-id="cc14d-2018">パスポートのNum</span><span class="sxs-lookup"><span data-stu-id="cc14d-2018">パスポートのNum</span></span>
- <span data-ttu-id="cc14d-2019">パスポート ＃</span><span class="sxs-lookup"><span data-stu-id="cc14d-2019">パスポート ＃</span></span> 
- <span data-ttu-id="cc14d-2020">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="cc14d-2020">Numéro de passeport</span></span>
- <span data-ttu-id="cc14d-2021">Passeport n °</span><span class="sxs-lookup"><span data-stu-id="cc14d-2021">Passeport n °</span></span>
- <span data-ttu-id="cc14d-2022">Passeport Non</span><span class="sxs-lookup"><span data-stu-id="cc14d-2022">Passeport Non</span></span>
- <span data-ttu-id="cc14d-2023">Passeport #</span><span class="sxs-lookup"><span data-stu-id="cc14d-2023">Passeport #</span></span>
- <span data-ttu-id="cc14d-2024">Passeport #</span><span class="sxs-lookup"><span data-stu-id="cc14d-2024">Passeport#</span></span>
- <span data-ttu-id="cc14d-2025">PasseportNon</span><span class="sxs-lookup"><span data-stu-id="cc14d-2025">PasseportNon</span></span>
- <span data-ttu-id="cc14d-2026">Passeportn °</span><span class="sxs-lookup"><span data-stu-id="cc14d-2026">Passeportn °</span></span>

      
## <a name="france-social-security-number-insee"></a><span data-ttu-id="cc14d-2027">Número de seguridade social da França (INSEE)</span><span class="sxs-lookup"><span data-stu-id="cc14d-2027">France Social Security Number (INSEE)</span></span>

### <a name="format"></a><span data-ttu-id="cc14d-2028">Format</span><span class="sxs-lookup"><span data-stu-id="cc14d-2028">Format</span></span>

<span data-ttu-id="cc14d-2029">15 dígitos</span><span class="sxs-lookup"><span data-stu-id="cc14d-2029">15 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="cc14d-2030">Padrão</span><span class="sxs-lookup"><span data-stu-id="cc14d-2030">Pattern</span></span>

<span data-ttu-id="cc14d-2031">Deve corresponder a um dos dois padrões:</span><span class="sxs-lookup"><span data-stu-id="cc14d-2031">Must match one of two patterns:</span></span>
- <span data-ttu-id="cc14d-2032">13 dígitos seguidos de um espaço seguido de dois dígitos</span><span class="sxs-lookup"><span data-stu-id="cc14d-2032">13 digits followed by a space followed by two digits</span></span><br/>
<span data-ttu-id="cc14d-2033">ou</span><span class="sxs-lookup"><span data-stu-id="cc14d-2033">or</span></span>
- <span data-ttu-id="cc14d-2034">15 dígitos consecutivos</span><span class="sxs-lookup"><span data-stu-id="cc14d-2034">15 consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="cc14d-2035">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="cc14d-2035">Checksum</span></span>

<span data-ttu-id="cc14d-2036">Sim</span><span class="sxs-lookup"><span data-stu-id="cc14d-2036">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="cc14d-2037">Definição</span><span class="sxs-lookup"><span data-stu-id="cc14d-2037">Definition</span></span>

<span data-ttu-id="cc14d-2038">Uma política de DLP tem 95% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="cc14d-2038">A DLP policy is 95% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="cc14d-2039">A função Func_french_insee ou Func_fr_insee localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="cc14d-2039">The function Func_french_insee or Func_fr_insee finds content that matches the pattern.</span></span>
- <span data-ttu-id="cc14d-2040">Uma palavra-chave de Keyword_fr_insee for encontrada.</span><span class="sxs-lookup"><span data-stu-id="cc14d-2040">A keyword from Keyword_fr_insee is found.</span></span>
- <span data-ttu-id="cc14d-2041">A soma de verificação passa.</span><span class="sxs-lookup"><span data-stu-id="cc14d-2041">The checksum passes.</span></span>

<span data-ttu-id="cc14d-2042">Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="cc14d-2042">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="cc14d-2043">A função Func_french_insee ou Func_fr_insee localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="cc14d-2043">The function Func_french_insee or Func_fr_insee finds content that matches the pattern.</span></span>
- <span data-ttu-id="cc14d-2044">Nenhuma palavra-chave de Keyword_fr_insee for encontrada.</span><span class="sxs-lookup"><span data-stu-id="cc14d-2044">No keyword from Keyword_fr_insee is found.</span></span>
- <span data-ttu-id="cc14d-2045">A soma de verificação passa.</span><span class="sxs-lookup"><span data-stu-id="cc14d-2045">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="cc14d-2046">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="cc14d-2046">Keywords</span></span>

#### <a name="keywordfrinsee"></a><span data-ttu-id="cc14d-2047">Keyword_fr_insee</span><span class="sxs-lookup"><span data-stu-id="cc14d-2047">Keyword_fr_insee</span></span>

- <span data-ttu-id="cc14d-2048">INSEE</span><span class="sxs-lookup"><span data-stu-id="cc14d-2048">insee</span></span>
- <span data-ttu-id="cc14d-2049">securité sociale</span><span class="sxs-lookup"><span data-stu-id="cc14d-2049">securité sociale</span></span>
- <span data-ttu-id="cc14d-2050">securite sociale</span><span class="sxs-lookup"><span data-stu-id="cc14d-2050">securite sociale</span></span>
- <span data-ttu-id="cc14d-2051">national id</span><span class="sxs-lookup"><span data-stu-id="cc14d-2051">national id</span></span>
- <span data-ttu-id="cc14d-2052">national identification</span><span class="sxs-lookup"><span data-stu-id="cc14d-2052">national identification</span></span>
- <span data-ttu-id="cc14d-2053">numéro d'identité</span><span class="sxs-lookup"><span data-stu-id="cc14d-2053">numéro d'identité</span></span>
- <span data-ttu-id="cc14d-2054">no d'identité</span><span class="sxs-lookup"><span data-stu-id="cc14d-2054">no d'identité</span></span>
- <span data-ttu-id="cc14d-2055">Não.</span><span class="sxs-lookup"><span data-stu-id="cc14d-2055">no.</span></span> <span data-ttu-id="cc14d-2056">d'identité</span><span class="sxs-lookup"><span data-stu-id="cc14d-2056">d'identité</span></span>
- <span data-ttu-id="cc14d-2057">numero d'identite</span><span class="sxs-lookup"><span data-stu-id="cc14d-2057">numero d'identite</span></span>
- <span data-ttu-id="cc14d-2058">no d'identite</span><span class="sxs-lookup"><span data-stu-id="cc14d-2058">no d'identite</span></span>
- <span data-ttu-id="cc14d-2059">Não.</span><span class="sxs-lookup"><span data-stu-id="cc14d-2059">no.</span></span> <span data-ttu-id="cc14d-2060">d'identite</span><span class="sxs-lookup"><span data-stu-id="cc14d-2060">d'identite</span></span>
- <span data-ttu-id="cc14d-2061">social security number</span><span class="sxs-lookup"><span data-stu-id="cc14d-2061">social security number</span></span>
- <span data-ttu-id="cc14d-2062">social security code</span><span class="sxs-lookup"><span data-stu-id="cc14d-2062">social security code</span></span>
- <span data-ttu-id="cc14d-2063">social insurance number</span><span class="sxs-lookup"><span data-stu-id="cc14d-2063">social insurance number</span></span>
- <span data-ttu-id="cc14d-2064">le numéro d'identification nationale</span><span class="sxs-lookup"><span data-stu-id="cc14d-2064">le numéro d'identification nationale</span></span>
- <span data-ttu-id="cc14d-2065">d'identité nationale</span><span class="sxs-lookup"><span data-stu-id="cc14d-2065">d'identité nationale</span></span>
- <span data-ttu-id="cc14d-2066">numéro de sécurité sociale</span><span class="sxs-lookup"><span data-stu-id="cc14d-2066">numéro de sécurité sociale</span></span>
- <span data-ttu-id="cc14d-2067">le code de la sécurité sociale</span><span class="sxs-lookup"><span data-stu-id="cc14d-2067">le code de la sécurité sociale</span></span>
- <span data-ttu-id="cc14d-2068">numéro d'assurance sociale</span><span class="sxs-lookup"><span data-stu-id="cc14d-2068">numéro d'assurance sociale</span></span>
- <span data-ttu-id="cc14d-2069">numéro de sécu</span><span class="sxs-lookup"><span data-stu-id="cc14d-2069">numéro de sécu</span></span>
- <span data-ttu-id="cc14d-2070">code sécu</span><span class="sxs-lookup"><span data-stu-id="cc14d-2070">code sécu</span></span> 
   
## <a name="german-drivers-license-number"></a><span data-ttu-id="cc14d-2071">Número de carteira de motorista da Alemanha</span><span class="sxs-lookup"><span data-stu-id="cc14d-2071">German Driver's License Number</span></span>

### <a name="format"></a><span data-ttu-id="cc14d-2072">Format</span><span class="sxs-lookup"><span data-stu-id="cc14d-2072">Format</span></span>

<span data-ttu-id="cc14d-2073">Combinação de 11 dígitos e letras</span><span class="sxs-lookup"><span data-stu-id="cc14d-2073">Combination of 11 digits and letters</span></span>

### <a name="pattern"></a><span data-ttu-id="cc14d-2074">Padrão</span><span class="sxs-lookup"><span data-stu-id="cc14d-2074">Pattern</span></span>

<span data-ttu-id="cc14d-2075">11 dígitos e letras (não diferenciam maiúsculas de minúsculas):</span><span class="sxs-lookup"><span data-stu-id="cc14d-2075">11 digits and letters (not case sensitive):</span></span>
- <span data-ttu-id="cc14d-2076">Um dígito ou letra</span><span class="sxs-lookup"><span data-stu-id="cc14d-2076">A digit or letter</span></span> 
- <span data-ttu-id="cc14d-2077">Dois dígitos</span><span class="sxs-lookup"><span data-stu-id="cc14d-2077">Two digits</span></span> 
- <span data-ttu-id="cc14d-2078">Seis dígitos ou letras</span><span class="sxs-lookup"><span data-stu-id="cc14d-2078">Six digits or letters</span></span> 
- <span data-ttu-id="cc14d-2079">Um dígito</span><span class="sxs-lookup"><span data-stu-id="cc14d-2079">A digit</span></span> 
- <span data-ttu-id="cc14d-2080">Um dígito ou letra</span><span class="sxs-lookup"><span data-stu-id="cc14d-2080">A digit or letter</span></span>

### <a name="checksum"></a><span data-ttu-id="cc14d-2081">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="cc14d-2081">Checksum</span></span>

<span data-ttu-id="cc14d-2082">Sim</span><span class="sxs-lookup"><span data-stu-id="cc14d-2082">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="cc14d-2083">Definição</span><span class="sxs-lookup"><span data-stu-id="cc14d-2083">Definition</span></span>

<span data-ttu-id="cc14d-2084">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="cc14d-2084">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="cc14d-2085">A função Func_german_drivers_license localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="cc14d-2085">The function Func_german_drivers_license finds content that matches the pattern.</span></span>
- <span data-ttu-id="cc14d-2086">Pelo menos uma das seguintes opções for verdadeira:</span><span class="sxs-lookup"><span data-stu-id="cc14d-2086">At least one of the following is true:</span></span>
    - <span data-ttu-id="cc14d-2087">Uma palavra-chave de Keyword_german_drivers_license_number for encontrada.</span><span class="sxs-lookup"><span data-stu-id="cc14d-2087">A keyword from Keyword_german_drivers_license_number is found.</span></span>
    - <span data-ttu-id="cc14d-2088">Uma palavra-chave de Keyword_german_drivers_license_collaborative for encontrada.</span><span class="sxs-lookup"><span data-stu-id="cc14d-2088">A keyword from Keyword_german_drivers_license_collaborative is found.</span></span>
    - <span data-ttu-id="cc14d-2089">Uma palavra-chave de Keyword_german_drivers_license for encontrada.</span><span class="sxs-lookup"><span data-stu-id="cc14d-2089">A keyword from Keyword_german_drivers_license is found.</span></span>
- <span data-ttu-id="cc14d-2090">A soma de verificação passa.</span><span class="sxs-lookup"><span data-stu-id="cc14d-2090">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="cc14d-2091">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="cc14d-2091">Keywords</span></span>

#### <a name="keywordgermandriverslicensenumber"></a><span data-ttu-id="cc14d-2092">Keyword_german_drivers_license_number</span><span class="sxs-lookup"><span data-stu-id="cc14d-2092">Keyword_german_drivers_license_number</span></span>

- <span data-ttu-id="cc14d-2093">Führerschein</span><span class="sxs-lookup"><span data-stu-id="cc14d-2093">Führerschein</span></span>
- <span data-ttu-id="cc14d-2094">Fuhrerschein</span><span class="sxs-lookup"><span data-stu-id="cc14d-2094">Fuhrerschein</span></span>
- <span data-ttu-id="cc14d-2095">Fuehrerschein</span><span class="sxs-lookup"><span data-stu-id="cc14d-2095">Fuehrerschein</span></span>
- <span data-ttu-id="cc14d-2096">Führerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="cc14d-2096">Führerscheinnummer</span></span>
- <span data-ttu-id="cc14d-2097">Fuhrerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="cc14d-2097">Fuhrerscheinnummer</span></span>
- <span data-ttu-id="cc14d-2098">Fuehrerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="cc14d-2098">Fuehrerscheinnummer</span></span>
- <span data-ttu-id="cc14d-2099">Führerschein-</span><span class="sxs-lookup"><span data-stu-id="cc14d-2099">Führerschein-</span></span> 
- <span data-ttu-id="cc14d-2100">Fuhrerschein-</span><span class="sxs-lookup"><span data-stu-id="cc14d-2100">Fuhrerschein-</span></span> 
- <span data-ttu-id="cc14d-2101">Fuehrerschein-</span><span class="sxs-lookup"><span data-stu-id="cc14d-2101">Fuehrerschein-</span></span> 
- <span data-ttu-id="cc14d-2102">FührerscheinnummerNr</span><span class="sxs-lookup"><span data-stu-id="cc14d-2102">FührerscheinnummerNr</span></span>
- <span data-ttu-id="cc14d-2103">FuhrerscheinnummerNr</span><span class="sxs-lookup"><span data-stu-id="cc14d-2103">FuhrerscheinnummerNr</span></span>
- <span data-ttu-id="cc14d-2104">FuehrerscheinnummerNr</span><span class="sxs-lookup"><span data-stu-id="cc14d-2104">FuehrerscheinnummerNr</span></span>
- <span data-ttu-id="cc14d-2105">FührerscheinnummerKlasse</span><span class="sxs-lookup"><span data-stu-id="cc14d-2105">FührerscheinnummerKlasse</span></span>
- <span data-ttu-id="cc14d-2106">FuhrerscheinnummerKlasse</span><span class="sxs-lookup"><span data-stu-id="cc14d-2106">FuhrerscheinnummerKlasse</span></span>
- <span data-ttu-id="cc14d-2107">FuehrerscheinnummerKlasse</span><span class="sxs-lookup"><span data-stu-id="cc14d-2107">FuehrerscheinnummerKlasse</span></span>
- <span data-ttu-id="cc14d-2108">Führerschein- Nr</span><span class="sxs-lookup"><span data-stu-id="cc14d-2108">Führerschein- Nr</span></span>
- <span data-ttu-id="cc14d-2109">Fuhrerschein- Nr</span><span class="sxs-lookup"><span data-stu-id="cc14d-2109">Fuhrerschein- Nr</span></span>
- <span data-ttu-id="cc14d-2110">Fuehrerschein- Nr</span><span class="sxs-lookup"><span data-stu-id="cc14d-2110">Fuehrerschein- Nr</span></span> 
- <span data-ttu-id="cc14d-2111">Führerschein- Klasse</span><span class="sxs-lookup"><span data-stu-id="cc14d-2111">Führerschein- Klasse</span></span> 
- <span data-ttu-id="cc14d-2112">Fuhrerschein- Klasse</span><span class="sxs-lookup"><span data-stu-id="cc14d-2112">Fuhrerschein- Klasse</span></span> 
- <span data-ttu-id="cc14d-2113">Fuehrerschein- Klasse</span><span class="sxs-lookup"><span data-stu-id="cc14d-2113">Fuehrerschein- Klasse</span></span>
- <span data-ttu-id="cc14d-2114">FührerscheinnummerNr</span><span class="sxs-lookup"><span data-stu-id="cc14d-2114">FührerscheinnummerNr</span></span> 
- <span data-ttu-id="cc14d-2115">FuhrerscheinnummerNr</span><span class="sxs-lookup"><span data-stu-id="cc14d-2115">FuhrerscheinnummerNr</span></span> 
- <span data-ttu-id="cc14d-2116">FuehrerscheinnummerNr</span><span class="sxs-lookup"><span data-stu-id="cc14d-2116">FuehrerscheinnummerNr</span></span> 
- <span data-ttu-id="cc14d-2117">FührerscheinnummerKlasse</span><span class="sxs-lookup"><span data-stu-id="cc14d-2117">FührerscheinnummerKlasse</span></span> 
- <span data-ttu-id="cc14d-2118">FuhrerscheinnummerKlasse</span><span class="sxs-lookup"><span data-stu-id="cc14d-2118">FuhrerscheinnummerKlasse</span></span> 
- <span data-ttu-id="cc14d-2119">FuehrerscheinnummerKlasse</span><span class="sxs-lookup"><span data-stu-id="cc14d-2119">FuehrerscheinnummerKlasse</span></span> 
- <span data-ttu-id="cc14d-2120">Führerschein- Nr</span><span class="sxs-lookup"><span data-stu-id="cc14d-2120">Führerschein- Nr</span></span> 
- <span data-ttu-id="cc14d-2121">Fuhrerschein- Nr</span><span class="sxs-lookup"><span data-stu-id="cc14d-2121">Fuhrerschein- Nr</span></span> 
- <span data-ttu-id="cc14d-2122">Fuehrerschein- Nr</span><span class="sxs-lookup"><span data-stu-id="cc14d-2122">Fuehrerschein- Nr</span></span> 
- <span data-ttu-id="cc14d-2123">Führerschein- Klasse</span><span class="sxs-lookup"><span data-stu-id="cc14d-2123">Führerschein- Klasse</span></span> 
- <span data-ttu-id="cc14d-2124">Fuhrerschein- Klasse</span><span class="sxs-lookup"><span data-stu-id="cc14d-2124">Fuhrerschein- Klasse</span></span> 
- <span data-ttu-id="cc14d-2125">Fuehrerschein- Klasse</span><span class="sxs-lookup"><span data-stu-id="cc14d-2125">Fuehrerschein- Klasse</span></span> 
- <span data-ttu-id="cc14d-2126">DISTRIBUIÇÃO</span><span class="sxs-lookup"><span data-stu-id="cc14d-2126">DL</span></span> 
- <span data-ttu-id="cc14d-2127">DL</span><span class="sxs-lookup"><span data-stu-id="cc14d-2127">DLS</span></span>
- <span data-ttu-id="cc14d-2128">Driv Lic</span><span class="sxs-lookup"><span data-stu-id="cc14d-2128">Driv Lic</span></span> 
- <span data-ttu-id="cc14d-2129">Driv Licen</span><span class="sxs-lookup"><span data-stu-id="cc14d-2129">Driv Licen</span></span> 
- <span data-ttu-id="cc14d-2130">Driv License</span><span class="sxs-lookup"><span data-stu-id="cc14d-2130">Driv License</span></span>
- <span data-ttu-id="cc14d-2131">Driv Licenses</span><span class="sxs-lookup"><span data-stu-id="cc14d-2131">Driv Licenses</span></span> 
- <span data-ttu-id="cc14d-2132">Driv Licence</span><span class="sxs-lookup"><span data-stu-id="cc14d-2132">Driv Licence</span></span> 
- <span data-ttu-id="cc14d-2133">Driv Licences</span><span class="sxs-lookup"><span data-stu-id="cc14d-2133">Driv Licences</span></span> 
- <span data-ttu-id="cc14d-2134">Driv Lic</span><span class="sxs-lookup"><span data-stu-id="cc14d-2134">Driv Lic</span></span> 
- <span data-ttu-id="cc14d-2135">Driver Licen</span><span class="sxs-lookup"><span data-stu-id="cc14d-2135">Driver Licen</span></span> 
- <span data-ttu-id="cc14d-2136">Driver License</span><span class="sxs-lookup"><span data-stu-id="cc14d-2136">Driver License</span></span> 
- <span data-ttu-id="cc14d-2137">Driver Licenses</span><span class="sxs-lookup"><span data-stu-id="cc14d-2137">Driver Licenses</span></span> 
- <span data-ttu-id="cc14d-2138">Driver Licence</span><span class="sxs-lookup"><span data-stu-id="cc14d-2138">Driver Licence</span></span> 
- <span data-ttu-id="cc14d-2139">Driver Licences</span><span class="sxs-lookup"><span data-stu-id="cc14d-2139">Driver Licences</span></span> 
- <span data-ttu-id="cc14d-2140">Drivers Lic</span><span class="sxs-lookup"><span data-stu-id="cc14d-2140">Drivers Lic</span></span> 
- <span data-ttu-id="cc14d-2141">Drivers Licen</span><span class="sxs-lookup"><span data-stu-id="cc14d-2141">Drivers Licen</span></span> 
- <span data-ttu-id="cc14d-2142">Drivers License</span><span class="sxs-lookup"><span data-stu-id="cc14d-2142">Drivers License</span></span> 
- <span data-ttu-id="cc14d-2143">Drivers Licenses</span><span class="sxs-lookup"><span data-stu-id="cc14d-2143">Drivers Licenses</span></span> 
- <span data-ttu-id="cc14d-2144">Drivers Licence</span><span class="sxs-lookup"><span data-stu-id="cc14d-2144">Drivers Licence</span></span> 
- <span data-ttu-id="cc14d-2145">Drivers Licences</span><span class="sxs-lookup"><span data-stu-id="cc14d-2145">Drivers Licences</span></span> 
- <span data-ttu-id="cc14d-2146">Driver's Lic</span><span class="sxs-lookup"><span data-stu-id="cc14d-2146">Driver's Lic</span></span> 
- <span data-ttu-id="cc14d-2147">Driver's Licen</span><span class="sxs-lookup"><span data-stu-id="cc14d-2147">Driver's Licen</span></span> 
- <span data-ttu-id="cc14d-2148">Driver's License</span><span class="sxs-lookup"><span data-stu-id="cc14d-2148">Driver's License</span></span> 
- <span data-ttu-id="cc14d-2149">Driver's Licenses</span><span class="sxs-lookup"><span data-stu-id="cc14d-2149">Driver's Licenses</span></span> 
- <span data-ttu-id="cc14d-2150">Driver's Licence</span><span class="sxs-lookup"><span data-stu-id="cc14d-2150">Driver's Licence</span></span> 
- <span data-ttu-id="cc14d-2151">Driver's Licences</span><span class="sxs-lookup"><span data-stu-id="cc14d-2151">Driver's Licences</span></span> 
- <span data-ttu-id="cc14d-2152">Driving Lic</span><span class="sxs-lookup"><span data-stu-id="cc14d-2152">Driving Lic</span></span> 
- <span data-ttu-id="cc14d-2153">Driving Licen</span><span class="sxs-lookup"><span data-stu-id="cc14d-2153">Driving Licen</span></span> 
- <span data-ttu-id="cc14d-2154">Driving License</span><span class="sxs-lookup"><span data-stu-id="cc14d-2154">Driving License</span></span> 
- <span data-ttu-id="cc14d-2155">Driving Licenses</span><span class="sxs-lookup"><span data-stu-id="cc14d-2155">Driving Licenses</span></span> 
- <span data-ttu-id="cc14d-2156">Driving Licence</span><span class="sxs-lookup"><span data-stu-id="cc14d-2156">Driving Licence</span></span> 
- <span data-ttu-id="cc14d-2157">Driving Licences</span><span class="sxs-lookup"><span data-stu-id="cc14d-2157">Driving Licences</span></span>

#### <a name="keywordgermandriverslicensecollaborative"></a><span data-ttu-id="cc14d-2158">Keyword_german_drivers_license_collaborative</span><span class="sxs-lookup"><span data-stu-id="cc14d-2158">Keyword_german_drivers_license_collaborative</span></span>

- <span data-ttu-id="cc14d-2159">NR-Führerschein</span><span class="sxs-lookup"><span data-stu-id="cc14d-2159">Nr-Führerschein</span></span> 
- <span data-ttu-id="cc14d-2160">NR-Fuhrerschein</span><span class="sxs-lookup"><span data-stu-id="cc14d-2160">Nr-Fuhrerschein</span></span> 
- <span data-ttu-id="cc14d-2161">NR-Fuehrerschein</span><span class="sxs-lookup"><span data-stu-id="cc14d-2161">Nr-Fuehrerschein</span></span> 
- <span data-ttu-id="cc14d-2162">No-Führerschein</span><span class="sxs-lookup"><span data-stu-id="cc14d-2162">No-Führerschein</span></span> 
- <span data-ttu-id="cc14d-2163">No-Fuhrerschein</span><span class="sxs-lookup"><span data-stu-id="cc14d-2163">No-Fuhrerschein</span></span> 
- <span data-ttu-id="cc14d-2164">No-Fuehrerschein</span><span class="sxs-lookup"><span data-stu-id="cc14d-2164">No-Fuehrerschein</span></span> 
- <span data-ttu-id="cc14d-2165">N-Führerschein</span><span class="sxs-lookup"><span data-stu-id="cc14d-2165">N-Führerschein</span></span> 
- <span data-ttu-id="cc14d-2166">N-Fuhrerschein</span><span class="sxs-lookup"><span data-stu-id="cc14d-2166">N-Fuhrerschein</span></span> 
- <span data-ttu-id="cc14d-2167">N-Fuehrerschein</span><span class="sxs-lookup"><span data-stu-id="cc14d-2167">N-Fuehrerschein</span></span>
- <span data-ttu-id="cc14d-2168">NR-Führerschein</span><span class="sxs-lookup"><span data-stu-id="cc14d-2168">Nr-Führerschein</span></span> 
- <span data-ttu-id="cc14d-2169">NR-Fuhrerschein</span><span class="sxs-lookup"><span data-stu-id="cc14d-2169">Nr-Fuhrerschein</span></span> 
- <span data-ttu-id="cc14d-2170">NR-Fuehrerschein</span><span class="sxs-lookup"><span data-stu-id="cc14d-2170">Nr-Fuehrerschein</span></span> 
- <span data-ttu-id="cc14d-2171">No-Führerschein</span><span class="sxs-lookup"><span data-stu-id="cc14d-2171">No-Führerschein</span></span> 
- <span data-ttu-id="cc14d-2172">No-Fuhrerschein</span><span class="sxs-lookup"><span data-stu-id="cc14d-2172">No-Fuhrerschein</span></span> 
- <span data-ttu-id="cc14d-2173">No-Fuehrerschein</span><span class="sxs-lookup"><span data-stu-id="cc14d-2173">No-Fuehrerschein</span></span> 
- <span data-ttu-id="cc14d-2174">N-Führerschein</span><span class="sxs-lookup"><span data-stu-id="cc14d-2174">N-Führerschein</span></span> 
- <span data-ttu-id="cc14d-2175">N-Fuhrerschein</span><span class="sxs-lookup"><span data-stu-id="cc14d-2175">N-Fuhrerschein</span></span> 
- <span data-ttu-id="cc14d-2176">N-Fuehrerschein</span><span class="sxs-lookup"><span data-stu-id="cc14d-2176">N-Fuehrerschein</span></span> 

#### <a name="keywordgermandriverslicense"></a><span data-ttu-id="cc14d-2177">Keyword_german_drivers_license</span><span class="sxs-lookup"><span data-stu-id="cc14d-2177">Keyword_german_drivers_license</span></span>

- <span data-ttu-id="cc14d-2178">ausstellungsdatum</span><span class="sxs-lookup"><span data-stu-id="cc14d-2178">ausstellungsdatum</span></span>
- <span data-ttu-id="cc14d-2179">ausstellungsort</span><span class="sxs-lookup"><span data-stu-id="cc14d-2179">ausstellungsort</span></span>
- <span data-ttu-id="cc14d-2180">ausstellende behöde</span><span class="sxs-lookup"><span data-stu-id="cc14d-2180">ausstellende behöde</span></span>
- <span data-ttu-id="cc14d-2181">ausstellende behorde</span><span class="sxs-lookup"><span data-stu-id="cc14d-2181">ausstellende behorde</span></span>
- <span data-ttu-id="cc14d-2182">ausstellende behoerde</span><span class="sxs-lookup"><span data-stu-id="cc14d-2182">ausstellende behoerde</span></span>
   
## <a name="german-passport-number"></a><span data-ttu-id="cc14d-2183">Número de passaporte da Alemanha</span><span class="sxs-lookup"><span data-stu-id="cc14d-2183">German Passport Number</span></span>

### <a name="format"></a><span data-ttu-id="cc14d-2184">Format</span><span class="sxs-lookup"><span data-stu-id="cc14d-2184">Format</span></span>

<span data-ttu-id="cc14d-2185">10 dígitos ou letras</span><span class="sxs-lookup"><span data-stu-id="cc14d-2185">10 digits or letters</span></span>

### <a name="pattern"></a><span data-ttu-id="cc14d-2186">Padrão</span><span class="sxs-lookup"><span data-stu-id="cc14d-2186">Pattern</span></span>

<span data-ttu-id="cc14d-2187">O padrão deve incluir todos os seguintes itens:</span><span class="sxs-lookup"><span data-stu-id="cc14d-2187">Pattern must include all of the following:</span></span>
- <span data-ttu-id="cc14d-2188">Primeiro caractere é um dígito ou uma letra desse conjunto (C, F, G, H, J, K)</span><span class="sxs-lookup"><span data-stu-id="cc14d-2188">First character is a digit or a letter from this set (C, F, G, H, J, K)</span></span> 
- <span data-ttu-id="cc14d-2189">Três dígitos</span><span class="sxs-lookup"><span data-stu-id="cc14d-2189">Three digits</span></span> 
- <span data-ttu-id="cc14d-2190">Cinco dígitos ou letras a partir desse conjunto (C, -H, J N, P, R, T, V-Z)</span><span class="sxs-lookup"><span data-stu-id="cc14d-2190">Five digits or letters from this set (C, -H, J-N, P, R, T, V-Z)</span></span> 
- <span data-ttu-id="cc14d-2191">Um dígito</span><span class="sxs-lookup"><span data-stu-id="cc14d-2191">A digit</span></span>

### <a name="checksum"></a><span data-ttu-id="cc14d-2192">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="cc14d-2192">Checksum</span></span>

<span data-ttu-id="cc14d-2193">Sim</span><span class="sxs-lookup"><span data-stu-id="cc14d-2193">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="cc14d-2194">Definição</span><span class="sxs-lookup"><span data-stu-id="cc14d-2194">Definition</span></span>

<span data-ttu-id="cc14d-2195">Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="cc14d-2195">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="cc14d-2196">A função Func_german_passport localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="cc14d-2196">The function Func_german_passport finds content that matches the pattern.</span></span>
- <span data-ttu-id="cc14d-2197">Uma palavra-chave de qualquer uma das cinco listas de palavras-chave for encontrada.</span><span class="sxs-lookup"><span data-stu-id="cc14d-2197">A keyword from any of the five keyword lists is found.</span></span>
- <span data-ttu-id="cc14d-2198">A soma de verificação passa.</span><span class="sxs-lookup"><span data-stu-id="cc14d-2198">The checksum passes.</span></span>

<span data-ttu-id="cc14d-2199">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="cc14d-2199">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="cc14d-2200">A função Func_german_passport_data localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="cc14d-2200">The function Func_german_passport_data finds content that matches the pattern.</span></span>
- <span data-ttu-id="cc14d-2201">Uma palavra-chave de qualquer uma das cinco listas de palavras-chave for encontrada.</span><span class="sxs-lookup"><span data-stu-id="cc14d-2201">A keyword from any of the five keyword lists is found.</span></span>
- <span data-ttu-id="cc14d-2202">A soma de verificação passa.</span><span class="sxs-lookup"><span data-stu-id="cc14d-2202">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="cc14d-2203">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="cc14d-2203">Keywords</span></span>

#### <a name="keywordgermanpassport"></a><span data-ttu-id="cc14d-2204">Keyword_german_passport</span><span class="sxs-lookup"><span data-stu-id="cc14d-2204">Keyword_german_passport</span></span>

- <span data-ttu-id="cc14d-2205">reisepass</span><span class="sxs-lookup"><span data-stu-id="cc14d-2205">reisepass</span></span>
- <span data-ttu-id="cc14d-2206">reisepasse</span><span class="sxs-lookup"><span data-stu-id="cc14d-2206">reisepasse</span></span>
- <span data-ttu-id="cc14d-2207">reisepassnummer</span><span class="sxs-lookup"><span data-stu-id="cc14d-2207">reisepassnummer</span></span>
- <span data-ttu-id="cc14d-2208">Passaport</span><span class="sxs-lookup"><span data-stu-id="cc14d-2208">passport</span></span>
- <span data-ttu-id="cc14d-2209">Passports</span><span class="sxs-lookup"><span data-stu-id="cc14d-2209">passports</span></span>

#### <a name="keywordgermanpassportcollaborative"></a><span data-ttu-id="cc14d-2210">Keyword_german_passport_collaborative</span><span class="sxs-lookup"><span data-stu-id="cc14d-2210">Keyword_german_passport_collaborative</span></span>

- <span data-ttu-id="cc14d-2211">geburtsdatum</span><span class="sxs-lookup"><span data-stu-id="cc14d-2211">geburtsdatum</span></span>
- <span data-ttu-id="cc14d-2212">ausstellungsdatum</span><span class="sxs-lookup"><span data-stu-id="cc14d-2212">ausstellungsdatum</span></span>
- <span data-ttu-id="cc14d-2213">ausstellungsort</span><span class="sxs-lookup"><span data-stu-id="cc14d-2213">ausstellungsort</span></span>

#### <a name="keywordgermanpassportnumber"></a><span data-ttu-id="cc14d-2214">Keyword_german_passport_number</span><span class="sxs-lookup"><span data-stu-id="cc14d-2214">Keyword_german_passport_number</span></span>

<span data-ttu-id="cc14d-2215">No-Reisepass NR-Reisepass</span><span class="sxs-lookup"><span data-stu-id="cc14d-2215">No-Reisepass Nr-Reisepass</span></span>

#### <a name="keywordgermanpassport1"></a><span data-ttu-id="cc14d-2216">Keyword_german_passport1</span><span class="sxs-lookup"><span data-stu-id="cc14d-2216">Keyword_german_passport1</span></span>

<span data-ttu-id="cc14d-2217">Reisepass-NR</span><span class="sxs-lookup"><span data-stu-id="cc14d-2217">Reisepass-Nr</span></span>

#### <a name="keywordgermanpassport2"></a><span data-ttu-id="cc14d-2218">Keyword_german_passport2</span><span class="sxs-lookup"><span data-stu-id="cc14d-2218">Keyword_german_passport2</span></span>

<span data-ttu-id="cc14d-2219">bnationalit. t</span><span class="sxs-lookup"><span data-stu-id="cc14d-2219">bnationalit.t</span></span>
   
## <a name="germany-identity-card-number"></a><span data-ttu-id="cc14d-2220">Número da carteira de identidade alemã</span><span class="sxs-lookup"><span data-stu-id="cc14d-2220">Germany Identity Card Number</span></span>

### <a name="format"></a><span data-ttu-id="cc14d-2221">Format</span><span class="sxs-lookup"><span data-stu-id="cc14d-2221">Format</span></span>

<span data-ttu-id="cc14d-2222">Desde 1 de novembro de 2010: nove letras e dígitos</span><span class="sxs-lookup"><span data-stu-id="cc14d-2222">Since 1 November 2010: Nine letters and digits</span></span>

<span data-ttu-id="cc14d-2223">De 1 de abril de 1987 até 31 de outubro de 2010:10 dígitos</span><span class="sxs-lookup"><span data-stu-id="cc14d-2223">From 1 April 1987 until 31 October 2010: 10 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="cc14d-2224">Padrão</span><span class="sxs-lookup"><span data-stu-id="cc14d-2224">Pattern</span></span>

<span data-ttu-id="cc14d-2225">Desde 1º de novembro de 2010:</span><span class="sxs-lookup"><span data-stu-id="cc14d-2225">Since 1 November 2010:</span></span>
- <span data-ttu-id="cc14d-2226">Uma letra (não diferencia maiúscula de minúscula)</span><span class="sxs-lookup"><span data-stu-id="cc14d-2226">One letter (not case sensitive)</span></span> 
- <span data-ttu-id="cc14d-2227">Oito dígitos</span><span class="sxs-lookup"><span data-stu-id="cc14d-2227">Eight digits</span></span>

<span data-ttu-id="cc14d-2228">De 1 de abril de 1987 até 31 de outubro de 2010:</span><span class="sxs-lookup"><span data-stu-id="cc14d-2228">From 1 April 1987 until 31 October 2010:</span></span>
- <span data-ttu-id="cc14d-2229">10 dígitos</span><span class="sxs-lookup"><span data-stu-id="cc14d-2229">10 digits</span></span>

### <a name="checksum"></a><span data-ttu-id="cc14d-2230">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="cc14d-2230">Checksum</span></span>

<span data-ttu-id="cc14d-2231">Não</span><span class="sxs-lookup"><span data-stu-id="cc14d-2231">No</span></span>

### <a name="definition"></a><span data-ttu-id="cc14d-2232">Definição</span><span class="sxs-lookup"><span data-stu-id="cc14d-2232">Definition</span></span>

<span data-ttu-id="cc14d-2233">Uma política de DLP tem 65% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="cc14d-2233">A DLP policy is 65% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="cc14d-2234">A expressão regular Regex_germany_id_card localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="cc14d-2234">The regular expression Regex_germany_id_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="cc14d-2235">Uma palavra-chave de Keyword_germany_id_card for encontrada.</span><span class="sxs-lookup"><span data-stu-id="cc14d-2235">A keyword from Keyword_germany_id_card is found.</span></span>

```
<!-- Germany Identity Card Number -->
<Entity id="e577372f-c42e-47a0-9d85-bebed1c237d4" recommendedConfidence="65" patternsProximity="300">
  <Pattern confidenceLevel="65">
     <IdMatch idRef="Regex_germany_id_card"/>
     <Match idRef="Keyword_germany_id_card"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="cc14d-2236">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="cc14d-2236">Keywords</span></span>

#### <a name="keywordgermanyidcard"></a><span data-ttu-id="cc14d-2237">Keyword_germany_id_card</span><span class="sxs-lookup"><span data-stu-id="cc14d-2237">Keyword_germany_id_card</span></span>

- <span data-ttu-id="cc14d-2238">Cartão de Identidade</span><span class="sxs-lookup"><span data-stu-id="cc14d-2238">Identity Card</span></span>
- <span data-ttu-id="cc14d-2239">ID</span><span class="sxs-lookup"><span data-stu-id="cc14d-2239">ID</span></span>
- <span data-ttu-id="cc14d-2240">Identificador</span><span class="sxs-lookup"><span data-stu-id="cc14d-2240">Identification</span></span>
- <span data-ttu-id="cc14d-2241">Personalausweis</span><span class="sxs-lookup"><span data-stu-id="cc14d-2241">Personalausweis</span></span>
- <span data-ttu-id="cc14d-2242">Identifizierungsnummer</span><span class="sxs-lookup"><span data-stu-id="cc14d-2242">Identifizierungsnummer</span></span>
- <span data-ttu-id="cc14d-2243">Ausweis</span><span class="sxs-lookup"><span data-stu-id="cc14d-2243">Ausweis</span></span>
- <span data-ttu-id="cc14d-2244">Identifikation</span><span class="sxs-lookup"><span data-stu-id="cc14d-2244">Identifikation</span></span>
   
## <a name="greece-national-id-card"></a><span data-ttu-id="cc14d-2245">Cartão de Identificação Nacional da Grécia</span><span class="sxs-lookup"><span data-stu-id="cc14d-2245">Greece National ID Card</span></span>

### <a name="format"></a><span data-ttu-id="cc14d-2246">Format</span><span class="sxs-lookup"><span data-stu-id="cc14d-2246">Format</span></span>

<span data-ttu-id="cc14d-2247">Combinação de 7 a 8 letras e números mais um traço</span><span class="sxs-lookup"><span data-stu-id="cc14d-2247">Combination of 7-8 letters and numbers plus a dash</span></span>

### <a name="pattern"></a><span data-ttu-id="cc14d-2248">Padrão</span><span class="sxs-lookup"><span data-stu-id="cc14d-2248">Pattern</span></span>

<span data-ttu-id="cc14d-2249">Sete letras e números (formato antigo):</span><span class="sxs-lookup"><span data-stu-id="cc14d-2249">Seven letters and numbers (old format):</span></span>
- <span data-ttu-id="cc14d-2250">Uma letra (qualquer letra do alfabeto grego) </span><span class="sxs-lookup"><span data-stu-id="cc14d-2250">One letter (any letter of the Greek alphabet)</span></span> 
- <span data-ttu-id="cc14d-2251">Um traço</span><span class="sxs-lookup"><span data-stu-id="cc14d-2251">A dash</span></span> 
- <span data-ttu-id="cc14d-2252">Seis dígitos</span><span class="sxs-lookup"><span data-stu-id="cc14d-2252">Six digits</span></span>

<span data-ttu-id="cc14d-2253">Oito letras e números (novo formato):</span><span class="sxs-lookup"><span data-stu-id="cc14d-2253">Eight letters and numbers (new format):</span></span>
- <span data-ttu-id="cc14d-2254">Duas letras cujos caracteres maiúsculos ocorre em alfabetos latino e grego (ABEZHIKMNOPTYX) </span><span class="sxs-lookup"><span data-stu-id="cc14d-2254">Two letters whose uppercase character occurs in both the Greek and Latin alphabets (ABEZHIKMNOPTYX)</span></span> 
- <span data-ttu-id="cc14d-2255">Um traço</span><span class="sxs-lookup"><span data-stu-id="cc14d-2255">A dash</span></span> 
- <span data-ttu-id="cc14d-2256">Seis dígitos</span><span class="sxs-lookup"><span data-stu-id="cc14d-2256">Six digits</span></span>

### <a name="checksum"></a><span data-ttu-id="cc14d-2257">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="cc14d-2257">Checksum</span></span>

<span data-ttu-id="cc14d-2258">Não</span><span class="sxs-lookup"><span data-stu-id="cc14d-2258">No</span></span>

### <a name="definition"></a><span data-ttu-id="cc14d-2259">Definição</span><span class="sxs-lookup"><span data-stu-id="cc14d-2259">Definition</span></span>

<span data-ttu-id="cc14d-2260">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="cc14d-2260">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="cc14d-2261">A expressão regular Regex_greece_id_card localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="cc14d-2261">The regular expression Regex_greece_id_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="cc14d-2262">Uma palavra-chave de Keyword_greece_id_card for encontrada.</span><span class="sxs-lookup"><span data-stu-id="cc14d-2262">A keyword from Keyword_greece_id_card is found.</span></span>

```
<!-- Greece National ID Card -->
<Entity id="82568215-1da1-46d3-874a-d2294d81b5ac" recommendedConfidence="85" patternsProximity="300">
  <Pattern confidenceLevel="85">
     <IdMatch idRef="Regex_greece_id_card"/>
     <Match idRef="Keyword_greece_id_card"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="cc14d-2263">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="cc14d-2263">Keywords</span></span>

#### <a name="keywordgreeceidcard"></a><span data-ttu-id="cc14d-2264">Keyword_greece_id_card</span><span class="sxs-lookup"><span data-stu-id="cc14d-2264">Keyword_greece_id_card</span></span>

- <span data-ttu-id="cc14d-2265">Cartão de identidade grego</span><span class="sxs-lookup"><span data-stu-id="cc14d-2265">Greek identity Card</span></span>
- <span data-ttu-id="cc14d-2266">Tautotita</span><span class="sxs-lookup"><span data-stu-id="cc14d-2266">Tautotita</span></span>
- <span data-ttu-id="cc14d-2267">Δελτίο αστυνομικής ταυτότητας</span><span class="sxs-lookup"><span data-stu-id="cc14d-2267">Δελτίο αστυνομικής ταυτότητας</span></span>
- <span data-ttu-id="cc14d-2268">Ταυτότητα</span><span class="sxs-lookup"><span data-stu-id="cc14d-2268">Ταυτότητα</span></span>
   
## <a name="hong-kong-identity-card-hkid-number"></a><span data-ttu-id="cc14d-2269">Número do Cartão de Identidade de Hong Kong (HKID)</span><span class="sxs-lookup"><span data-stu-id="cc14d-2269">Hong Kong Identity Card (HKID) Number</span></span>

### <a name="format"></a><span data-ttu-id="cc14d-2270">Format</span><span class="sxs-lookup"><span data-stu-id="cc14d-2270">Format</span></span>

<span data-ttu-id="cc14d-2271">Combinação de 8 a 9 letras e números mais parênteses opcionais ao redor do caractere final</span><span class="sxs-lookup"><span data-stu-id="cc14d-2271">Combination of 8-9 letters and numbers plus optional parentheses around the final character</span></span>

### <a name="pattern"></a><span data-ttu-id="cc14d-2272">Padrão</span><span class="sxs-lookup"><span data-stu-id="cc14d-2272">Pattern</span></span>

<span data-ttu-id="cc14d-2273">Combinação de 8 a 9 letras:</span><span class="sxs-lookup"><span data-stu-id="cc14d-2273">Combination of 8-9 letters:</span></span>
- <span data-ttu-id="cc14d-2274">1 a 2 letras (não diferenciam maiúsculas de minúsculas)</span><span class="sxs-lookup"><span data-stu-id="cc14d-2274">1-2 letters (not case sensitive)</span></span> 
- <span data-ttu-id="cc14d-2275">Seis dígitos</span><span class="sxs-lookup"><span data-stu-id="cc14d-2275">Six digits</span></span> 
- <span data-ttu-id="cc14d-2276">O caractere final (qualquer dígito ou a letra A), que é o dígito de verificação e é opcionalmente colocado entre parênteses.</span><span class="sxs-lookup"><span data-stu-id="cc14d-2276">The final character (any digit or the letter A), which is the check digit and is optionally enclosed in parentheses.</span></span>

### <a name="checksum"></a><span data-ttu-id="cc14d-2277">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="cc14d-2277">Checksum</span></span>

<span data-ttu-id="cc14d-2278">Sim</span><span class="sxs-lookup"><span data-stu-id="cc14d-2278">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="cc14d-2279">Definição</span><span class="sxs-lookup"><span data-stu-id="cc14d-2279">Definition</span></span>

<span data-ttu-id="cc14d-2280">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="cc14d-2280">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="cc14d-2281">A função Func_hong_kong_id_card localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="cc14d-2281">The function Func_hong_kong_id_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="cc14d-2282">Uma palavra-chave de Keyword_hong_kong_id_card for encontrada.</span><span class="sxs-lookup"><span data-stu-id="cc14d-2282">A keyword from Keyword_hong_kong_id_card is found.</span></span>
- <span data-ttu-id="cc14d-2283">A soma de verificação passa.</span><span class="sxs-lookup"><span data-stu-id="cc14d-2283">The checksum passes.</span></span>

<span data-ttu-id="cc14d-2284">Uma política de DLP tem 65% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="cc14d-2284">A DLP policy is 65% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="cc14d-2285">A função Func_hong_kong_id_card localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="cc14d-2285">The function Func_hong_kong_id_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="cc14d-2286">A soma de verificação passa.</span><span class="sxs-lookup"><span data-stu-id="cc14d-2286">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="cc14d-2287">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="cc14d-2287">Keywords</span></span>

#### <a name="keywordhongkongidcard"></a><span data-ttu-id="cc14d-2288">Keyword_hong_kong_id_card</span><span class="sxs-lookup"><span data-stu-id="cc14d-2288">Keyword_hong_kong_id_card</span></span>

- <span data-ttu-id="cc14d-2289">cartão de identidade de Hong Kong</span><span class="sxs-lookup"><span data-stu-id="cc14d-2289">hong kong identity card</span></span>
- <span data-ttu-id="cc14d-2290">HKIDC</span><span class="sxs-lookup"><span data-stu-id="cc14d-2290">HKIDC</span></span>
- <span data-ttu-id="cc14d-2291">id card</span><span class="sxs-lookup"><span data-stu-id="cc14d-2291">id card</span></span>
- <span data-ttu-id="cc14d-2292">cartão de identidade</span><span class="sxs-lookup"><span data-stu-id="cc14d-2292">identity card</span></span>
- <span data-ttu-id="cc14d-2293">cartão de identidade HK</span><span class="sxs-lookup"><span data-stu-id="cc14d-2293">hk identity card</span></span>
- <span data-ttu-id="cc14d-2294">ID de Hong Kong</span><span class="sxs-lookup"><span data-stu-id="cc14d-2294">hong kong id</span></span>
- <span data-ttu-id="cc14d-2295">香港身份證</span><span class="sxs-lookup"><span data-stu-id="cc14d-2295">香港身份證</span></span>
- <span data-ttu-id="cc14d-2296">香港永久性居民身份證</span><span class="sxs-lookup"><span data-stu-id="cc14d-2296">香港永久性居民身份證</span></span>
- <span data-ttu-id="cc14d-2297">身份證</span><span class="sxs-lookup"><span data-stu-id="cc14d-2297">身份證</span></span>
- <span data-ttu-id="cc14d-2298">身份証</span><span class="sxs-lookup"><span data-stu-id="cc14d-2298">身份証</span></span>
- <span data-ttu-id="cc14d-2299">身分證</span><span class="sxs-lookup"><span data-stu-id="cc14d-2299">身分證</span></span>
- <span data-ttu-id="cc14d-2300">身分証</span><span class="sxs-lookup"><span data-stu-id="cc14d-2300">身分証</span></span>
- <span data-ttu-id="cc14d-2301">香港身份証</span><span class="sxs-lookup"><span data-stu-id="cc14d-2301">香港身份証</span></span>
- <span data-ttu-id="cc14d-2302">香港身分證</span><span class="sxs-lookup"><span data-stu-id="cc14d-2302">香港身分證</span></span>
- <span data-ttu-id="cc14d-2303">香港身分証</span><span class="sxs-lookup"><span data-stu-id="cc14d-2303">香港身分証</span></span>
- <span data-ttu-id="cc14d-2304">香港身份證</span><span class="sxs-lookup"><span data-stu-id="cc14d-2304">香港身份證</span></span>
- <span data-ttu-id="cc14d-2305">香港居民身份證</span><span class="sxs-lookup"><span data-stu-id="cc14d-2305">香港居民身份證</span></span>
- <span data-ttu-id="cc14d-2306">香港居民身份証</span><span class="sxs-lookup"><span data-stu-id="cc14d-2306">香港居民身份証</span></span>
- <span data-ttu-id="cc14d-2307">香港居民身分證</span><span class="sxs-lookup"><span data-stu-id="cc14d-2307">香港居民身分證</span></span>
- <span data-ttu-id="cc14d-2308">香港居民身分証</span><span class="sxs-lookup"><span data-stu-id="cc14d-2308">香港居民身分証</span></span>
- <span data-ttu-id="cc14d-2309">香港永久性居民身份証</span><span class="sxs-lookup"><span data-stu-id="cc14d-2309">香港永久性居民身份証</span></span>
- <span data-ttu-id="cc14d-2310">香港永久性居民身分證</span><span class="sxs-lookup"><span data-stu-id="cc14d-2310">香港永久性居民身分證</span></span>
- <span data-ttu-id="cc14d-2311">香港永久性居民身分証</span><span class="sxs-lookup"><span data-stu-id="cc14d-2311">香港永久性居民身分証</span></span>
- <span data-ttu-id="cc14d-2312">香港永久性居民身份證</span><span class="sxs-lookup"><span data-stu-id="cc14d-2312">香港永久性居民身份證</span></span>
- <span data-ttu-id="cc14d-2313">香港非永久性居民身份證</span><span class="sxs-lookup"><span data-stu-id="cc14d-2313">香港非永久性居民身份證</span></span>
- <span data-ttu-id="cc14d-2314">香港非永久性居民身份証</span><span class="sxs-lookup"><span data-stu-id="cc14d-2314">香港非永久性居民身份証</span></span>
- <span data-ttu-id="cc14d-2315">香港非永久性居民身分證</span><span class="sxs-lookup"><span data-stu-id="cc14d-2315">香港非永久性居民身分證</span></span>
- <span data-ttu-id="cc14d-2316">香港非永久性居民身分証</span><span class="sxs-lookup"><span data-stu-id="cc14d-2316">香港非永久性居民身分証</span></span>
- <span data-ttu-id="cc14d-2317">香港特別行政區永久性居民身份證</span><span class="sxs-lookup"><span data-stu-id="cc14d-2317">香港特別行政區永久性居民身份證</span></span>
- <span data-ttu-id="cc14d-2318">香港特別行政區永久性居民身份証</span><span class="sxs-lookup"><span data-stu-id="cc14d-2318">香港特別行政區永久性居民身份証</span></span>
- <span data-ttu-id="cc14d-2319">香港特別行政區永久性居民身分證</span><span class="sxs-lookup"><span data-stu-id="cc14d-2319">香港特別行政區永久性居民身分證</span></span>
- <span data-ttu-id="cc14d-2320">香港特別行政區永久性居民身分証</span><span class="sxs-lookup"><span data-stu-id="cc14d-2320">香港特別行政區永久性居民身分証</span></span>
- <span data-ttu-id="cc14d-2321">香港特別行政區非永久性居民身份證</span><span class="sxs-lookup"><span data-stu-id="cc14d-2321">香港特別行政區非永久性居民身份證</span></span>
- <span data-ttu-id="cc14d-2322">香港特別行政區非永久性居民身份証</span><span class="sxs-lookup"><span data-stu-id="cc14d-2322">香港特別行政區非永久性居民身份証</span></span>
- <span data-ttu-id="cc14d-2323">香港特別行政區非永久性居民身分證</span><span class="sxs-lookup"><span data-stu-id="cc14d-2323">香港特別行政區非永久性居民身分證</span></span>
- <span data-ttu-id="cc14d-2324">香港特別行政區非永久性居民身分証</span><span class="sxs-lookup"><span data-stu-id="cc14d-2324">香港特別行政區非永久性居民身分証</span></span>
   
## <a name="india-permanent-account-number-pan"></a><span data-ttu-id="cc14d-2325">Número da Conta Permanente da Índia (PAN)</span><span class="sxs-lookup"><span data-stu-id="cc14d-2325">India Permanent Account Number (PAN)</span></span>

### <a name="format"></a><span data-ttu-id="cc14d-2326">Format</span><span class="sxs-lookup"><span data-stu-id="cc14d-2326">Format</span></span>

<span data-ttu-id="cc14d-2327">10 letras ou dígitos</span><span class="sxs-lookup"><span data-stu-id="cc14d-2327">10 letters or digits</span></span>

### <a name="pattern"></a><span data-ttu-id="cc14d-2328">Padrão</span><span class="sxs-lookup"><span data-stu-id="cc14d-2328">Pattern</span></span>

<span data-ttu-id="cc14d-2329">10 letras ou dígitos.</span><span class="sxs-lookup"><span data-stu-id="cc14d-2329">10 letters or digits:</span></span>
- <span data-ttu-id="cc14d-2330">Cinco letras (não diferenciam maiúsculas de minúsculas)</span><span class="sxs-lookup"><span data-stu-id="cc14d-2330">Five letters (not case sensitive)</span></span> 
- <span data-ttu-id="cc14d-2331">Quatro dígitos</span><span class="sxs-lookup"><span data-stu-id="cc14d-2331">Four digits</span></span> 
- <span data-ttu-id="cc14d-2332">Uma letra que é um dígito de verificação alfabético</span><span class="sxs-lookup"><span data-stu-id="cc14d-2332">A letter which is an alphabetic check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="cc14d-2333">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="cc14d-2333">Checksum</span></span>

<span data-ttu-id="cc14d-2334">Sim</span><span class="sxs-lookup"><span data-stu-id="cc14d-2334">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="cc14d-2335">Definição</span><span class="sxs-lookup"><span data-stu-id="cc14d-2335">Definition</span></span>

<span data-ttu-id="cc14d-2336">Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="cc14d-2336">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="cc14d-2337">A expressão regular Regex_india_permanent_account_number localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="cc14d-2337">The regular expression Regex_india_permanent_account_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="cc14d-2338">Uma palavra-chave de Keyword_india_permanent_account_number for encontrada.</span><span class="sxs-lookup"><span data-stu-id="cc14d-2338">A keyword from Keyword_india_permanent_account_number is found.</span></span>
- <span data-ttu-id="cc14d-2339">A soma de verificação passa.</span><span class="sxs-lookup"><span data-stu-id="cc14d-2339">The checksum passes.</span></span>

```
<!-- India Permanent Account Number -->
<Entity id="2602bfee-9bb0-47a5-a7a6-2bf3053e2804" recommendedConfidence="85" patternsProximity="300">
  <Pattern confidenceLevel="85">
     <IdMatch idRef="Regex_india_permanent_account_number"/>
     <Match idRef="Keyword_india_permanent_account_number"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="cc14d-2340">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="cc14d-2340">Keywords</span></span>

#### <a name="keywordindiapermanentaccountnumber"></a><span data-ttu-id="cc14d-2341">Keyword_india_permanent_account_number</span><span class="sxs-lookup"><span data-stu-id="cc14d-2341">Keyword_india_permanent_account_number</span></span>

- <span data-ttu-id="cc14d-2342">Número da Conta Permanente</span><span class="sxs-lookup"><span data-stu-id="cc14d-2342">Permanent Account Number</span></span> 
- <span data-ttu-id="cc14d-2343">APLICAR</span><span class="sxs-lookup"><span data-stu-id="cc14d-2343">PAN</span></span> 
   
## <a name="india-unique-identification-aadhaar-number"></a><span data-ttu-id="cc14d-2344">Número de Identificação Exclusivo da Índia (Aadhaar)</span><span class="sxs-lookup"><span data-stu-id="cc14d-2344">India Unique Identification (Aadhaar) Number</span></span>

### <a name="format"></a><span data-ttu-id="cc14d-2345">Format</span><span class="sxs-lookup"><span data-stu-id="cc14d-2345">Format</span></span>

<span data-ttu-id="cc14d-2346">12 dígitos contendo espaços opcionais ou traços</span><span class="sxs-lookup"><span data-stu-id="cc14d-2346">12 digits containing optional spaces or dashes</span></span>

### <a name="pattern"></a><span data-ttu-id="cc14d-2347">Padrão</span><span class="sxs-lookup"><span data-stu-id="cc14d-2347">Pattern</span></span>

<span data-ttu-id="cc14d-2348">12 dígitos:</span><span class="sxs-lookup"><span data-stu-id="cc14d-2348">12 digits:</span></span>
- <span data-ttu-id="cc14d-2349">Quatro dígitos</span><span class="sxs-lookup"><span data-stu-id="cc14d-2349">Four digits</span></span> 
- <span data-ttu-id="cc14d-2350">Um espaço ou um traço opcional </span><span class="sxs-lookup"><span data-stu-id="cc14d-2350">An optional space or dash</span></span> 
- <span data-ttu-id="cc14d-2351">Quatro dígitos</span><span class="sxs-lookup"><span data-stu-id="cc14d-2351">Four digits</span></span> 
- <span data-ttu-id="cc14d-2352">Um espaço ou um traço opcional </span><span class="sxs-lookup"><span data-stu-id="cc14d-2352">An optional space or dash</span></span> 
- <span data-ttu-id="cc14d-2353">O dígito final que é o dígito de verificação</span><span class="sxs-lookup"><span data-stu-id="cc14d-2353">The final digit which is the check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="cc14d-2354">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="cc14d-2354">Checksum</span></span>

<span data-ttu-id="cc14d-2355">Sim</span><span class="sxs-lookup"><span data-stu-id="cc14d-2355">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="cc14d-2356">Definição</span><span class="sxs-lookup"><span data-stu-id="cc14d-2356">Definition</span></span>

<span data-ttu-id="cc14d-2357">Uma política de DLP é de 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres: a função Func_india_aadhaar localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="cc14d-2357">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters: The function Func_india_aadhaar finds content that matches the pattern.</span></span>
<span data-ttu-id="cc14d-2358">Uma palavra-chave de Keyword_india_aadhar for encontrada.</span><span class="sxs-lookup"><span data-stu-id="cc14d-2358">A keyword from Keyword_india_aadhar is found.</span></span>
<span data-ttu-id="cc14d-2359">A soma de verificação passa.</span><span class="sxs-lookup"><span data-stu-id="cc14d-2359">The checksum passes.</span></span>
<span data-ttu-id="cc14d-2360">Uma política de DLP é de 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres: a função Func_india_aadhaar localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="cc14d-2360">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters: The function Func_india_aadhaar finds content that matches the pattern.</span></span>
<span data-ttu-id="cc14d-2361">A soma de verificação passa.</span><span class="sxs-lookup"><span data-stu-id="cc14d-2361">The checksum passes.</span></span>
<span data-ttu-id="cc14d-2362"><!-- India Unique Identification (Aadhaar) number -->
<Entity id="1ca46b29-76f5-4f46-9383-cfa15e91048f" recommendedConfidence="85" patternsProximity="300"> <Pattern confidenceLevel="85"> <IdMatch idRef="Func_india_aadhaar"/> <Match idRef="Keyword_india_aadhar"/> </Pattern> <Pattern confidenceLevel="75"> <IdMatch idRef="Func_india_aadhaar"/> </Pattern>
</Entity></span><span class="sxs-lookup"><span data-stu-id="cc14d-2362"></span></span>

### <a name="keywords"></a><span data-ttu-id="cc14d-2363">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="cc14d-2363">Keywords</span></span>
   
#### <a name="keywordindiaaadhar"></a><span data-ttu-id="cc14d-2364">Keyword_india_aadhar</span><span class="sxs-lookup"><span data-stu-id="cc14d-2364">Keyword_india_aadhar</span></span>
- <span data-ttu-id="cc14d-2365">Aadhar</span><span class="sxs-lookup"><span data-stu-id="cc14d-2365">Aadhar</span></span>
- <span data-ttu-id="cc14d-2366">Aadhaar</span><span class="sxs-lookup"><span data-stu-id="cc14d-2366">Aadhaar</span></span>
- <span data-ttu-id="cc14d-2367">UID</span><span class="sxs-lookup"><span data-stu-id="cc14d-2367">UID</span></span>
- <span data-ttu-id="cc14d-2368">आधार</span><span class="sxs-lookup"><span data-stu-id="cc14d-2368">आधार</span></span>
   
## <a name="indonesia-identity-card-ktp-number"></a><span data-ttu-id="cc14d-2369">Número do Cartão de Identidade da Indonésia (KTP)</span><span class="sxs-lookup"><span data-stu-id="cc14d-2369">Indonesia Identity Card (KTP) Number</span></span>

### <a name="format"></a><span data-ttu-id="cc14d-2370">Format</span><span class="sxs-lookup"><span data-stu-id="cc14d-2370">Format</span></span>

<span data-ttu-id="cc14d-2371">16 dígitos contendo pontos opcionais</span><span class="sxs-lookup"><span data-stu-id="cc14d-2371">16 digits containing optional periods</span></span>

### <a name="pattern"></a><span data-ttu-id="cc14d-2372">Padrão</span><span class="sxs-lookup"><span data-stu-id="cc14d-2372">Pattern</span></span>

<span data-ttu-id="cc14d-2373">16 dígitos:</span><span class="sxs-lookup"><span data-stu-id="cc14d-2373">16 digits:</span></span>
- <span data-ttu-id="cc14d-2374">Código de província de dois dígitos </span><span class="sxs-lookup"><span data-stu-id="cc14d-2374">Two-digit province code</span></span> 
- <span data-ttu-id="cc14d-2375">Um ponto (opcional) </span><span class="sxs-lookup"><span data-stu-id="cc14d-2375">A period (optional)</span></span> 
- <span data-ttu-id="cc14d-2376">Código de dois dígitos da regência ou da cidade </span><span class="sxs-lookup"><span data-stu-id="cc14d-2376">Two-digit regency or city code</span></span> 
- <span data-ttu-id="cc14d-2377">Código de dois dígitos do subdistrito </span><span class="sxs-lookup"><span data-stu-id="cc14d-2377">Two-digit subdistrict code</span></span> 
- <span data-ttu-id="cc14d-2378">Um ponto (opcional) </span><span class="sxs-lookup"><span data-stu-id="cc14d-2378">A period (optional)</span></span> 
- <span data-ttu-id="cc14d-2379">Seis dígitos no formato DDMMAA que são a data de nascimento</span><span class="sxs-lookup"><span data-stu-id="cc14d-2379">Six digits in the format DDMMYY which are the date of birth</span></span> 
- <span data-ttu-id="cc14d-2380">Um ponto (opcional) </span><span class="sxs-lookup"><span data-stu-id="cc14d-2380">A period (optional)</span></span> 
- <span data-ttu-id="cc14d-2381">Quatro dígitos</span><span class="sxs-lookup"><span data-stu-id="cc14d-2381">Four digits</span></span>

### <a name="checksum"></a><span data-ttu-id="cc14d-2382">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="cc14d-2382">Checksum</span></span>

<span data-ttu-id="cc14d-2383">Não</span><span class="sxs-lookup"><span data-stu-id="cc14d-2383">No</span></span>

### <a name="definition"></a><span data-ttu-id="cc14d-2384">Definição</span><span class="sxs-lookup"><span data-stu-id="cc14d-2384">Definition</span></span>

<span data-ttu-id="cc14d-2385">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="cc14d-2385">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="cc14d-2386">A expressão regular Regex_indonesia_id_card localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="cc14d-2386">The regular expression Regex_indonesia_id_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="cc14d-2387">Uma palavra-chave de Keyword_indonesia_id_card for encontrada.</span><span class="sxs-lookup"><span data-stu-id="cc14d-2387">A keyword from Keyword_indonesia_id_card is found.</span></span>

<span data-ttu-id="cc14d-2388">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="cc14d-2388">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="cc14d-2389">A expressão regular Regex_indonesia_id_card localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="cc14d-2389">The regular expression Regex_indonesia_id_card finds content that matches the pattern.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="cc14d-2390">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="cc14d-2390">Keywords</span></span>
   
#### <a name="keywordindonesiaidcard"></a><span data-ttu-id="cc14d-2391">Keyword_indonesia_id_card</span><span class="sxs-lookup"><span data-stu-id="cc14d-2391">Keyword_indonesia_id_card</span></span>

- <span data-ttu-id="cc14d-2392">KTP</span><span class="sxs-lookup"><span data-stu-id="cc14d-2392">KTP</span></span>
- <span data-ttu-id="cc14d-2393">Kartu Tanda Penduduk</span><span class="sxs-lookup"><span data-stu-id="cc14d-2393">Kartu Tanda Penduduk</span></span> 
- <span data-ttu-id="cc14d-2394">Nomor Induk Kependudukan</span><span class="sxs-lookup"><span data-stu-id="cc14d-2394">Nomor Induk Kependudukan</span></span> 
   
## <a name="international-banking-account-number-iban"></a><span data-ttu-id="cc14d-2395">Número da Conta Bancária Internacional (IBAN)</span><span class="sxs-lookup"><span data-stu-id="cc14d-2395">International Banking Account Number (IBAN)</span></span>

### <a name="format"></a><span data-ttu-id="cc14d-2396">Format</span><span class="sxs-lookup"><span data-stu-id="cc14d-2396">Format</span></span>

<span data-ttu-id="cc14d-2397">Código do país (duas letras) mais dígitos de verificação (dois dígitos) mais Bban número (até 30 caracteres)</span><span class="sxs-lookup"><span data-stu-id="cc14d-2397">Country code (two letters) plus check digits (two digits) plus bban number (up to 30 characters)</span></span>

### <a name="pattern"></a><span data-ttu-id="cc14d-2398">Padrão</span><span class="sxs-lookup"><span data-stu-id="cc14d-2398">Pattern</span></span>

<span data-ttu-id="cc14d-2399">O padrão deve incluir todos os seguintes itens:</span><span class="sxs-lookup"><span data-stu-id="cc14d-2399">Pattern must include all of the following:</span></span>

- <span data-ttu-id="cc14d-2400">Código de país de duas letras</span><span class="sxs-lookup"><span data-stu-id="cc14d-2400">Two-letter country code</span></span>
- <span data-ttu-id="cc14d-2401">Dois dígitos de verificação (seguidos por um espaço opcional)</span><span class="sxs-lookup"><span data-stu-id="cc14d-2401">Two check digits (followed by an optional space)</span></span> 
- <span data-ttu-id="cc14d-2402">1-7 grupos de quatro letras ou dígitos (podem ser separados por espaços)</span><span class="sxs-lookup"><span data-stu-id="cc14d-2402">1-7 groups of four letters or digits (can be separated by spaces)</span></span>
- <span data-ttu-id="cc14d-2403">1 a 3 letras ou dígitos</span><span class="sxs-lookup"><span data-stu-id="cc14d-2403">1-3 letters or digits</span></span>

<span data-ttu-id="cc14d-2404">O formato de cada país é um pouco diferente.</span><span class="sxs-lookup"><span data-stu-id="cc14d-2404">The format for each country is slightly different.</span></span> <span data-ttu-id="cc14d-2405">O tipo de informação confidencial do IBAN cobre estes 60 países:</span><span class="sxs-lookup"><span data-stu-id="cc14d-2405">The IBAN sensitive information type covers these 60 countries:</span></span>

<span data-ttu-id="cc14d-2406">AD, AE, Al, at, AZ, BA, be, BG, BH, ch, CR, Cy, cz, de, DK, do, EE, es, Fi, fo, FR, GB, GE, GI, GL, GR, HR, Hu, IE, Il, se,-, KZ, lb, li, o (a) e o (a) , NL, no, pl, pt, Ro, RS, SA, se, si, SK, SM, TN, TR, VG</span><span class="sxs-lookup"><span data-stu-id="cc14d-2406">ad, ae, al, at, az, ba, be, bg, bh, ch, cr, cy, cz, de, dk, do, ee, es, fi, fo, fr, gb, ge, gi, gl, gr, hr, hu, ie, il, is, it, kw, kz, lb, li, lt, lu, lv, mc, md, me, mk, mr, mt, mu, nl, no, pl, pt, ro, rs, sa, se, si, sk, sm, tn, tr, vg</span></span>

### <a name="checksum"></a><span data-ttu-id="cc14d-2407">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="cc14d-2407">Checksum</span></span>

<span data-ttu-id="cc14d-2408">Sim</span><span class="sxs-lookup"><span data-stu-id="cc14d-2408">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="cc14d-2409">Definição</span><span class="sxs-lookup"><span data-stu-id="cc14d-2409">Definition</span></span>

<span data-ttu-id="cc14d-2410">Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="cc14d-2410">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="cc14d-2411">A função Func_iban localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="cc14d-2411">The function Func_iban finds content that matches the pattern.</span></span>
- <span data-ttu-id="cc14d-2412">A soma de verificação passa.</span><span class="sxs-lookup"><span data-stu-id="cc14d-2412">The checksum passes.</span></span>

```
<Entity id="e7dc4711-11b7-4cb0-b88b-2c394a771f0e" patternsProximity="300" recommendedConfidence="85">
  <Pattern confidenceLevel="85">
        <IdMatch idRef="Func_iban" />
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="cc14d-2413">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="cc14d-2413">Keywords</span></span>

<span data-ttu-id="cc14d-2414">Nenhum</span><span class="sxs-lookup"><span data-stu-id="cc14d-2414">None</span></span>

   
## <a name="ip-address"></a><span data-ttu-id="cc14d-2415">Endereço IP</span><span class="sxs-lookup"><span data-stu-id="cc14d-2415">IP Address</span></span>

### <a name="format"></a><span data-ttu-id="cc14d-2416">Format</span><span class="sxs-lookup"><span data-stu-id="cc14d-2416">Format</span></span>

#### <a name="ipv4"></a><span data-ttu-id="cc14d-2417">IPv4</span><span class="sxs-lookup"><span data-stu-id="cc14d-2417">IPv4:</span></span>
<span data-ttu-id="cc14d-2418">Padrão complexo que é responsável por versões formatadas (pontos) e não formatadas (sem pontos) dos endereços IPv4</span><span class="sxs-lookup"><span data-stu-id="cc14d-2418">Complex pattern which accounts for formatted (periods) and unformatted (no periods) versions of the IPv4 addresses</span></span>

#### <a name="ipv6"></a><span data-ttu-id="cc14d-2419">IPv6</span><span class="sxs-lookup"><span data-stu-id="cc14d-2419">IPv6:</span></span>
<span data-ttu-id="cc14d-2420">Padrão complexo que é responsável por números IPv6 formatados (que incluem dois pontos)</span><span class="sxs-lookup"><span data-stu-id="cc14d-2420">Complex pattern which accounts for formatted IPv6 numbers (which include colons)</span></span>

### <a name="pattern"></a><span data-ttu-id="cc14d-2421">Padrão</span><span class="sxs-lookup"><span data-stu-id="cc14d-2421">Pattern</span></span>

### <a name="checksum"></a><span data-ttu-id="cc14d-2422">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="cc14d-2422">Checksum</span></span>

<span data-ttu-id="cc14d-2423">Não</span><span class="sxs-lookup"><span data-stu-id="cc14d-2423">No</span></span>

### <a name="definition"></a><span data-ttu-id="cc14d-2424">Definição</span><span class="sxs-lookup"><span data-stu-id="cc14d-2424">Definition</span></span>

<span data-ttu-id="cc14d-2425">Para IPv6, uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="cc14d-2425">For IPv6, a DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="cc14d-2426">A expressão regular Regex_ipv6_address localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="cc14d-2426">The regular expression Regex_ipv6_address finds content that matches the pattern.</span></span>
- <span data-ttu-id="cc14d-2427">Nenhuma palavra-chave de Keyword_ipaddress for encontrada.</span><span class="sxs-lookup"><span data-stu-id="cc14d-2427">No keyword from Keyword_ipaddress is found.</span></span>

<span data-ttu-id="cc14d-2428">Para IPv4, uma política de DLP tem 95% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="cc14d-2428">For IPv4, a DLP policy is 95% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="cc14d-2429">A expressão regular Regex_ipv4_address localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="cc14d-2429">The regular expression Regex_ipv4_address finds content that matches the pattern.</span></span>
- <span data-ttu-id="cc14d-2430">Uma palavra-chave de Keyword_ipaddress for encontrada.</span><span class="sxs-lookup"><span data-stu-id="cc14d-2430">A keyword from Keyword_ipaddress is found.</span></span>

<span data-ttu-id="cc14d-2431">Para IPv6, uma política de DLP tem 95% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="cc14d-2431">For IPv6, a DLP policy is 95% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="cc14d-2432">A expressão regular Regex_ipv6_address localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="cc14d-2432">The regular expression Regex_ipv6_address finds content that matches the pattern.</span></span>
- <span data-ttu-id="cc14d-2433">Nenhuma palavra-chave de Keyword_ipaddress for encontrada.</span><span class="sxs-lookup"><span data-stu-id="cc14d-2433">No keyword from Keyword_ipaddress is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="cc14d-2434">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="cc14d-2434">Keywords</span></span>

#### <a name="keywordipaddress"></a><span data-ttu-id="cc14d-2435">Keyword_ipaddress</span><span class="sxs-lookup"><span data-stu-id="cc14d-2435">Keyword_ipaddress</span></span>

- <span data-ttu-id="cc14d-2436">IP (esta palavra-chave diferencia maiúsculas de minúsculas)</span><span class="sxs-lookup"><span data-stu-id="cc14d-2436">IP (this keyword is case sensitive)</span></span>
- <span data-ttu-id="cc14d-2437">ip address</span><span class="sxs-lookup"><span data-stu-id="cc14d-2437">ip address</span></span> 
- <span data-ttu-id="cc14d-2438">endereços ip</span><span class="sxs-lookup"><span data-stu-id="cc14d-2438">ip addresses</span></span>
- <span data-ttu-id="cc14d-2439">internet protocol</span><span class="sxs-lookup"><span data-stu-id="cc14d-2439">internet protocol</span></span>
- <span data-ttu-id="cc14d-2440">IP כתובת ה</span><span class="sxs-lookup"><span data-stu-id="cc14d-2440">IP-כתובת ה</span></span> 
   
## <a name="international-classification-of-diseases-icd-10-cm"></a><span data-ttu-id="cc14d-2441">Classificação internacional do Diseases (ICD-10-CM)</span><span class="sxs-lookup"><span data-stu-id="cc14d-2441">International Classification of Diseases (ICD-10-CM)</span></span>

### <a name="format"></a><span data-ttu-id="cc14d-2442">Format</span><span class="sxs-lookup"><span data-stu-id="cc14d-2442">Format</span></span>

<span data-ttu-id="cc14d-2443">Dictionary</span><span class="sxs-lookup"><span data-stu-id="cc14d-2443">Dictionary</span></span>

### <a name="pattern"></a><span data-ttu-id="cc14d-2444">Padrão</span><span class="sxs-lookup"><span data-stu-id="cc14d-2444">Pattern</span></span>

<span data-ttu-id="cc14d-2445">Palavra-chave</span><span class="sxs-lookup"><span data-stu-id="cc14d-2445">Keyword</span></span>

### <a name="checksum"></a><span data-ttu-id="cc14d-2446">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="cc14d-2446">Checksum</span></span>

<span data-ttu-id="cc14d-2447">Não</span><span class="sxs-lookup"><span data-stu-id="cc14d-2447">No</span></span>

### <a name="definition"></a><span data-ttu-id="cc14d-2448">Definição</span><span class="sxs-lookup"><span data-stu-id="cc14d-2448">Definition</span></span>

<span data-ttu-id="cc14d-2449">Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="cc14d-2449">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="cc14d-2450">Uma palavra-chave de Dictionary_icd_10_cm for encontrada.</span><span class="sxs-lookup"><span data-stu-id="cc14d-2450">A keyword from Dictionary_icd_10_cm is found.</span></span>

```
      <!-- ICD-10 CM -->
      <Entity id="3356946c-6bb7-449b-b253-6ffa419c0ce7" patternsProximity="300" recommendedConfidence="85">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Dictionary_icd_10_cm" />
        </Pattern>
      </Entity>
```

<span data-ttu-id="cc14d-2451">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="cc14d-2451">Keywords</span></span>

<span data-ttu-id="cc14d-2452">Qualquer termo do dicionário de palavra-chave Dictionary_icd_10_cm, que se baseia na [classificação internacional do Diseases, décimo revisão, modificação clínica (ICD-10-cm)](https://go.microsoft.com/fwlink/?linkid=852604).</span><span class="sxs-lookup"><span data-stu-id="cc14d-2452">Any term from the Dictionary_icd_10_cm keyword dictionary, which is based on the [International Classification of Diseases, Tenth Revision, Clinical Modification (ICD-10-CM)](https://go.microsoft.com/fwlink/?linkid=852604).</span></span> <span data-ttu-id="cc14d-2453">Esse tipo procura apenas o termo, não os códigos de seguro.</span><span class="sxs-lookup"><span data-stu-id="cc14d-2453">This type looks only for the term, not the insurance codes.</span></span>

   
## <a name="international-classification-of-diseases-icd-9-cm"></a><span data-ttu-id="cc14d-2454">Classificação internacional do Diseases (ICD-9-CM)</span><span class="sxs-lookup"><span data-stu-id="cc14d-2454">International Classification of Diseases (ICD-9-CM)</span></span>

### <a name="format"></a><span data-ttu-id="cc14d-2455">Format</span><span class="sxs-lookup"><span data-stu-id="cc14d-2455">Format</span></span>

<span data-ttu-id="cc14d-2456">Dictionary</span><span class="sxs-lookup"><span data-stu-id="cc14d-2456">Dictionary</span></span>

### <a name="pattern"></a><span data-ttu-id="cc14d-2457">Padrão</span><span class="sxs-lookup"><span data-stu-id="cc14d-2457">Pattern</span></span>

<span data-ttu-id="cc14d-2458">Palavra-chave</span><span class="sxs-lookup"><span data-stu-id="cc14d-2458">Keyword</span></span>

### <a name="checksum"></a><span data-ttu-id="cc14d-2459">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="cc14d-2459">Checksum</span></span>

<span data-ttu-id="cc14d-2460">Não</span><span class="sxs-lookup"><span data-stu-id="cc14d-2460">No</span></span>

### <a name="definition"></a><span data-ttu-id="cc14d-2461">Definição</span><span class="sxs-lookup"><span data-stu-id="cc14d-2461">Definition</span></span>

<span data-ttu-id="cc14d-2462">Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="cc14d-2462">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="cc14d-2463">Uma palavra-chave de Dictionary_icd_9_cm for encontrada.</span><span class="sxs-lookup"><span data-stu-id="cc14d-2463">A keyword from Dictionary_icd_9_cm is found.</span></span>

```
      <Entity id="fa3f9c74-ee07-4c52-b5f2-085d6b2c0ec4" patternsProximity="300" recommendedConfidence="85">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Dictionary_icd_9_cm" />
        </Pattern>
      </Entity>
```

### <a name="keywords"></a><span data-ttu-id="cc14d-2464">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="cc14d-2464">Keywords</span></span>

<span data-ttu-id="cc14d-2465">Qualquer termo do dicionário de palavra-chave Dictionary_icd_9_cm, que se baseia na [classificação internacional do Diseases, Nona revisão, modificação clínica (ICD-9-cm)](https://go.microsoft.com/fwlink/?linkid=852605).</span><span class="sxs-lookup"><span data-stu-id="cc14d-2465">Any term from the Dictionary_icd_9_cm keyword dictionary, which is based on the [International Classification of Diseases,Ninth Revision, Clinical Modification (ICD-9-CM)](https://go.microsoft.com/fwlink/?linkid=852605).</span></span> <span data-ttu-id="cc14d-2466">Esse tipo procura apenas o termo, não os códigos de seguro.</span><span class="sxs-lookup"><span data-stu-id="cc14d-2466">This type looks only for the term, not the insurance codes.</span></span>
   
## <a name="ireland-personal-public-service-pps-number"></a><span data-ttu-id="cc14d-2467">Número de Serviço Público Pessoal (PPS) da Irlanda</span><span class="sxs-lookup"><span data-stu-id="cc14d-2467">Ireland Personal Public Service (PPS) Number</span></span>

### <a name="format"></a><span data-ttu-id="cc14d-2468">Format</span><span class="sxs-lookup"><span data-stu-id="cc14d-2468">Format</span></span>

<span data-ttu-id="cc14d-2469">Formato antigo (até 31 de dezembro de 2012):</span><span class="sxs-lookup"><span data-stu-id="cc14d-2469">Old format (until 31 Dec 2012):</span></span>
- <span data-ttu-id="cc14d-2470">Sete dígitos seguidos de 1 a 2 letras </span><span class="sxs-lookup"><span data-stu-id="cc14d-2470">Seven digits followed by 1-2 letters</span></span> 

<span data-ttu-id="cc14d-2471">Novo formato (1 Jan 2013 e posterior):</span><span class="sxs-lookup"><span data-stu-id="cc14d-2471">New format (1 Jan 2013 and after):</span></span>
- <span data-ttu-id="cc14d-2472">Sete dígitos seguidos de duas letras</span><span class="sxs-lookup"><span data-stu-id="cc14d-2472">Seven digits followed by two letters</span></span>

### <a name="pattern"></a><span data-ttu-id="cc14d-2473">Padrão</span><span class="sxs-lookup"><span data-stu-id="cc14d-2473">Pattern</span></span>

<span data-ttu-id="cc14d-2474">Formato antigo (até 31 de dezembro de 2012):</span><span class="sxs-lookup"><span data-stu-id="cc14d-2474">Old format (until 31 Dec 2012):</span></span>
- <span data-ttu-id="cc14d-2475">Sete dígitos </span><span class="sxs-lookup"><span data-stu-id="cc14d-2475">Seven digits</span></span> 
- <span data-ttu-id="cc14d-2476">1 a 2 letras (não diferenciam maiúsculas de minúsculas)</span><span class="sxs-lookup"><span data-stu-id="cc14d-2476">1-2 letters (not case sensitive)</span></span> 

<span data-ttu-id="cc14d-2477">Novo formato (1 Jan 2013 e posterior):</span><span class="sxs-lookup"><span data-stu-id="cc14d-2477">New format (1 Jan 2013 and after):</span></span>
- <span data-ttu-id="cc14d-2478">Sete dígitos </span><span class="sxs-lookup"><span data-stu-id="cc14d-2478">Seven digits</span></span> 
- <span data-ttu-id="cc14d-2479">Uma letra (não diferencia maiúsculas de minúsculas) que é um dígito de verificação alfabético </span><span class="sxs-lookup"><span data-stu-id="cc14d-2479">A letter (not case sensitive) which is an alphabetic check digit</span></span> 
- <span data-ttu-id="cc14d-2480">A letra "A" ou "H" (não diferencia maiúsculas de minúsculas)</span><span class="sxs-lookup"><span data-stu-id="cc14d-2480">The letter "A" or "H" (not case sensitive)</span></span>

### <a name="checksum"></a><span data-ttu-id="cc14d-2481">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="cc14d-2481">Checksum</span></span>

<span data-ttu-id="cc14d-2482">Sim</span><span class="sxs-lookup"><span data-stu-id="cc14d-2482">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="cc14d-2483">Definição</span><span class="sxs-lookup"><span data-stu-id="cc14d-2483">Definition</span></span>

<span data-ttu-id="cc14d-2484">Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="cc14d-2484">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="cc14d-2485">A função Func_ireland_pps localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="cc14d-2485">The function Func_ireland_pps finds content that matches the pattern.</span></span>
- <span data-ttu-id="cc14d-2486">Uma das seguintes opções for verdadeira:</span><span class="sxs-lookup"><span data-stu-id="cc14d-2486">One of the following is true:</span></span>
    - <span data-ttu-id="cc14d-2487">Uma palavra-chave de Keyword_ireland_pps for encontrada.</span><span class="sxs-lookup"><span data-stu-id="cc14d-2487">A keyword from Keyword_ireland_pps is found.</span></span>
    - <span data-ttu-id="cc14d-2488">A função Func_eu_date encontra uma data no formato de data à direita.</span><span class="sxs-lookup"><span data-stu-id="cc14d-2488">The function Func_eu_date finds a date in the right date format.</span></span>
- <span data-ttu-id="cc14d-2489">A soma de verificação passa.</span><span class="sxs-lookup"><span data-stu-id="cc14d-2489">The checksum passes.</span></span>

<span data-ttu-id="cc14d-2490">Uma política de DLP tem 65% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="cc14d-2490">A DLP policy is 65% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="cc14d-2491">A função Func_ireland_pps localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="cc14d-2491">The function Func_ireland_pps finds content that matches the pattern.</span></span>
- <span data-ttu-id="cc14d-2492">A soma de verificação passa.</span><span class="sxs-lookup"><span data-stu-id="cc14d-2492">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="cc14d-2493">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="cc14d-2493">Keywords</span></span>

#### <a name="keywordirelandpps"></a><span data-ttu-id="cc14d-2494">Keyword_ireland_pps</span><span class="sxs-lookup"><span data-stu-id="cc14d-2494">Keyword_ireland_pps</span></span>

- <span data-ttu-id="cc14d-2495">Número do Serviço Público Pessoal</span><span class="sxs-lookup"><span data-stu-id="cc14d-2495">Personal Public Service Number</span></span> 
- <span data-ttu-id="cc14d-2496">Número PPS</span><span class="sxs-lookup"><span data-stu-id="cc14d-2496">PPS Number</span></span> 
- <span data-ttu-id="cc14d-2497">Núm PPS</span><span class="sxs-lookup"><span data-stu-id="cc14d-2497">PPS Num</span></span> 
- <span data-ttu-id="cc14d-2498">Nº PPS</span><span class="sxs-lookup"><span data-stu-id="cc14d-2498">PPS No.</span></span> 
- <span data-ttu-id="cc14d-2499"># PPS</span><span class="sxs-lookup"><span data-stu-id="cc14d-2499">PPS #</span></span> 
- <span data-ttu-id="cc14d-2500">PPS</span><span class="sxs-lookup"><span data-stu-id="cc14d-2500">PPS#</span></span> 
- <span data-ttu-id="cc14d-2501">PPSN</span><span class="sxs-lookup"><span data-stu-id="cc14d-2501">PPSN</span></span> 
- <span data-ttu-id="cc14d-2502">Cartão dos Serviços Públicos</span><span class="sxs-lookup"><span data-stu-id="cc14d-2502">Public Services Card</span></span> 
- <span data-ttu-id="cc14d-2503">Uimhir Phearsanta Seirbhíse Poiblí</span><span class="sxs-lookup"><span data-stu-id="cc14d-2503">Uimhir Phearsanta Seirbhíse Poiblí</span></span> 
- <span data-ttu-id="cc14d-2504">Uimh.</span><span class="sxs-lookup"><span data-stu-id="cc14d-2504">Uimh.</span></span> <span data-ttu-id="cc14d-2505">PSP</span><span class="sxs-lookup"><span data-stu-id="cc14d-2505">PSP</span></span> 
- <span data-ttu-id="cc14d-2506">PSP</span><span class="sxs-lookup"><span data-stu-id="cc14d-2506">PSP</span></span> 
   
## <a name="israel-bank-account-number"></a><span data-ttu-id="cc14d-2507">Número de conta bancária de Israel</span><span class="sxs-lookup"><span data-stu-id="cc14d-2507">Israel Bank Account Number</span></span>

### <a name="format"></a><span data-ttu-id="cc14d-2508">Format</span><span class="sxs-lookup"><span data-stu-id="cc14d-2508">Format</span></span>

<span data-ttu-id="cc14d-2509">13 dígitos</span><span class="sxs-lookup"><span data-stu-id="cc14d-2509">13 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="cc14d-2510">Padrão</span><span class="sxs-lookup"><span data-stu-id="cc14d-2510">Pattern</span></span>

<span data-ttu-id="cc14d-2511">Binário</span><span class="sxs-lookup"><span data-stu-id="cc14d-2511">Formatted:</span></span>
- <span data-ttu-id="cc14d-2512">Dois dígitos</span><span class="sxs-lookup"><span data-stu-id="cc14d-2512">Two digits</span></span> 
- <span data-ttu-id="cc14d-2513">Um traço</span><span class="sxs-lookup"><span data-stu-id="cc14d-2513">A dash</span></span> 
- <span data-ttu-id="cc14d-2514">Três dígitos</span><span class="sxs-lookup"><span data-stu-id="cc14d-2514">Three digits</span></span> 
- <span data-ttu-id="cc14d-2515">Um traço</span><span class="sxs-lookup"><span data-stu-id="cc14d-2515">A dash</span></span> 
- <span data-ttu-id="cc14d-2516">Oito dígitos</span><span class="sxs-lookup"><span data-stu-id="cc14d-2516">Eight digits</span></span>

<span data-ttu-id="cc14d-2517">Não formatado</span><span class="sxs-lookup"><span data-stu-id="cc14d-2517">Unformatted:</span></span>
- <span data-ttu-id="cc14d-2518">13 dígitos consecutivos</span><span class="sxs-lookup"><span data-stu-id="cc14d-2518">13 consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="cc14d-2519">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="cc14d-2519">Checksum</span></span>

<span data-ttu-id="cc14d-2520">Não</span><span class="sxs-lookup"><span data-stu-id="cc14d-2520">No</span></span>

### <a name="definition"></a><span data-ttu-id="cc14d-2521">Definição</span><span class="sxs-lookup"><span data-stu-id="cc14d-2521">Definition</span></span>

<span data-ttu-id="cc14d-2522">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="cc14d-2522">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="cc14d-2523">A expressão regular Regex_israel_bank_account_number localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="cc14d-2523">The regular expression Regex_israel_bank_account_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="cc14d-2524">Uma palavra-chave de Keyword_israel_bank_account_number for encontrada.</span><span class="sxs-lookup"><span data-stu-id="cc14d-2524">A keyword from Keyword_israel_bank_account_number is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="cc14d-2525">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="cc14d-2525">Keywords</span></span>

#### <a name="keywordisraelbankaccountnumber"></a><span data-ttu-id="cc14d-2526">Keyword_israel_bank_account_number</span><span class="sxs-lookup"><span data-stu-id="cc14d-2526">Keyword_israel_bank_account_number</span></span>

- <span data-ttu-id="cc14d-2527">Bank Account Number</span><span class="sxs-lookup"><span data-stu-id="cc14d-2527">Bank Account Number</span></span> 
- <span data-ttu-id="cc14d-2528">Bank Account</span><span class="sxs-lookup"><span data-stu-id="cc14d-2528">Bank Account</span></span> 
- <span data-ttu-id="cc14d-2529">Account Number</span><span class="sxs-lookup"><span data-stu-id="cc14d-2529">Account Number</span></span> 
- <span data-ttu-id="cc14d-2530">מספר חשבון בנק</span><span class="sxs-lookup"><span data-stu-id="cc14d-2530">מספר חשבון בנק</span></span> 
   
## <a name="israel-national-id"></a><span data-ttu-id="cc14d-2531">ID nacional de Israel</span><span class="sxs-lookup"><span data-stu-id="cc14d-2531">Israel National ID</span></span>

### <a name="format"></a><span data-ttu-id="cc14d-2532">Format</span><span class="sxs-lookup"><span data-stu-id="cc14d-2532">Format</span></span>

<span data-ttu-id="cc14d-2533">Nove dígitos</span><span class="sxs-lookup"><span data-stu-id="cc14d-2533">Nine digits</span></span>

### <a name="pattern"></a><span data-ttu-id="cc14d-2534">Padrão</span><span class="sxs-lookup"><span data-stu-id="cc14d-2534">Pattern</span></span>

<span data-ttu-id="cc14d-2535">Nove dígitos consecutivos</span><span class="sxs-lookup"><span data-stu-id="cc14d-2535">Nine consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="cc14d-2536">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="cc14d-2536">Checksum</span></span>

<span data-ttu-id="cc14d-2537">Sim</span><span class="sxs-lookup"><span data-stu-id="cc14d-2537">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="cc14d-2538">Definição</span><span class="sxs-lookup"><span data-stu-id="cc14d-2538">Definition</span></span>

<span data-ttu-id="cc14d-2539">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="cc14d-2539">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="cc14d-2540">A função Func_israeli_national_id_number localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="cc14d-2540">The function Func_israeli_national_id_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="cc14d-2541">Uma palavra-chave de Keyword_Israel_National_ID for encontrada.</span><span class="sxs-lookup"><span data-stu-id="cc14d-2541">A keyword from Keyword_Israel_National_ID is found.</span></span>
- <span data-ttu-id="cc14d-2542">A soma de verificação passa.</span><span class="sxs-lookup"><span data-stu-id="cc14d-2542">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="cc14d-2543">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="cc14d-2543">Keywords</span></span>

#### <a name="keywordisraelnationalid"></a><span data-ttu-id="cc14d-2544">Keyword_Israel_National_ID</span><span class="sxs-lookup"><span data-stu-id="cc14d-2544">Keyword_Israel_National_ID</span></span>

- <span data-ttu-id="cc14d-2545">מספר זהות</span><span class="sxs-lookup"><span data-stu-id="cc14d-2545">מספר זהות</span></span> 
- <span data-ttu-id="cc14d-2546">Número de identificação nacional</span><span class="sxs-lookup"><span data-stu-id="cc14d-2546">National ID Number</span></span>
   
## <a name="italy-drivers-license-number"></a><span data-ttu-id="cc14d-2547">Número de carteira de motorista da Itália</span><span class="sxs-lookup"><span data-stu-id="cc14d-2547">Italy Driver's License Number</span></span>

### <a name="format"></a><span data-ttu-id="cc14d-2548">Format</span><span class="sxs-lookup"><span data-stu-id="cc14d-2548">Format</span></span>

<span data-ttu-id="cc14d-2549">Uma combinação de 10 letras e dígitos</span><span class="sxs-lookup"><span data-stu-id="cc14d-2549">A combination of 10 letters and digits</span></span>

### <a name="pattern"></a><span data-ttu-id="cc14d-2550">Padrão</span><span class="sxs-lookup"><span data-stu-id="cc14d-2550">Pattern</span></span>

- <span data-ttu-id="cc14d-2551">Uma combinação de 10 letras e dígitos:</span><span class="sxs-lookup"><span data-stu-id="cc14d-2551">A combination of 10 letters and digits:</span></span>
- <span data-ttu-id="cc14d-2552">Uma letra (não diferencia maiúscula de minúscula)</span><span class="sxs-lookup"><span data-stu-id="cc14d-2552">One letter (not case sensitive)</span></span> 
- <span data-ttu-id="cc14d-2553">A letra "A" ou "V" (não diferencia maiúscula de minúscula)</span><span class="sxs-lookup"><span data-stu-id="cc14d-2553">The letter "A" or "V" (not case sensitive)</span></span> 
- <span data-ttu-id="cc14d-2554">Sete letras (não diferenciam maiúsculas de minúsculas), dígitos ou o caractere de sublinhado</span><span class="sxs-lookup"><span data-stu-id="cc14d-2554">Seven letters (not case sensitive), digits, or the underscore character</span></span> 
- <span data-ttu-id="cc14d-2555">Uma letra (não diferencia maiúscula de minúscula)</span><span class="sxs-lookup"><span data-stu-id="cc14d-2555">One letter (not case sensitive)</span></span>

### <a name="checksum"></a><span data-ttu-id="cc14d-2556">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="cc14d-2556">Checksum</span></span>

<span data-ttu-id="cc14d-2557">Não</span><span class="sxs-lookup"><span data-stu-id="cc14d-2557">No</span></span>

### <a name="definition"></a><span data-ttu-id="cc14d-2558">Definição</span><span class="sxs-lookup"><span data-stu-id="cc14d-2558">Definition</span></span>

<span data-ttu-id="cc14d-2559">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="cc14d-2559">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="cc14d-2560">A expressão regular Regex_italy_drivers_license_number localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="cc14d-2560">The regular expression Regex_italy_drivers_license_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="cc14d-2561">Uma palavra-chave de Keyword_italy_drivers_license_number for encontrada.</span><span class="sxs-lookup"><span data-stu-id="cc14d-2561">A keyword from Keyword_italy_drivers_license_number is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="cc14d-2562">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="cc14d-2562">Keywords</span></span>

#### <a name="keyworditalydriverslicensenumber"></a><span data-ttu-id="cc14d-2563">Keyword_italy_drivers_license_number</span><span class="sxs-lookup"><span data-stu-id="cc14d-2563">Keyword_italy_drivers_license_number</span></span>

- <span data-ttu-id="cc14d-2564">numero di patente di guida</span><span class="sxs-lookup"><span data-stu-id="cc14d-2564">numero di patente di guida</span></span> 
- <span data-ttu-id="cc14d-2565">patente di guida</span><span class="sxs-lookup"><span data-stu-id="cc14d-2565">patente di guida</span></span> 
   
## <a name="japan-bank-account-number"></a><span data-ttu-id="cc14d-2566">Número de conta bancária do Japão</span><span class="sxs-lookup"><span data-stu-id="cc14d-2566">Japan Bank Account Number</span></span>

### <a name="format"></a><span data-ttu-id="cc14d-2567">Format</span><span class="sxs-lookup"><span data-stu-id="cc14d-2567">Format</span></span>

<span data-ttu-id="cc14d-2568">Sete ou oito dígitos</span><span class="sxs-lookup"><span data-stu-id="cc14d-2568">Seven or eight digits</span></span>

### <a name="pattern"></a><span data-ttu-id="cc14d-2569">Padrão</span><span class="sxs-lookup"><span data-stu-id="cc14d-2569">Pattern</span></span>

<span data-ttu-id="cc14d-2570">Número da Conta Bancária:</span><span class="sxs-lookup"><span data-stu-id="cc14d-2570">Bank account number:</span></span>
- <span data-ttu-id="cc14d-2571">Sete ou oito dígitos</span><span class="sxs-lookup"><span data-stu-id="cc14d-2571">Seven or eight digits</span></span>
- <span data-ttu-id="cc14d-2572">Código da agência de conta bancária:</span><span class="sxs-lookup"><span data-stu-id="cc14d-2572">Bank account branch code:</span></span>
- <span data-ttu-id="cc14d-2573">Quatro dígitos</span><span class="sxs-lookup"><span data-stu-id="cc14d-2573">Four digits</span></span> 
- <span data-ttu-id="cc14d-2574">Um espaço ou um traço (opcional)</span><span class="sxs-lookup"><span data-stu-id="cc14d-2574">A space or dash (optional)</span></span> 
- <span data-ttu-id="cc14d-2575">Três dígitos</span><span class="sxs-lookup"><span data-stu-id="cc14d-2575">Three digits</span></span>

<span data-ttu-id="cc14d-2576">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="cc14d-2576">Checksum</span></span>

<span data-ttu-id="cc14d-2577">Não</span><span class="sxs-lookup"><span data-stu-id="cc14d-2577">No</span></span>

### <a name="definition"></a><span data-ttu-id="cc14d-2578">Definição</span><span class="sxs-lookup"><span data-stu-id="cc14d-2578">Definition</span></span>

<span data-ttu-id="cc14d-2579">Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="cc14d-2579">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="cc14d-2580">A função Func_jp_bank_account localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="cc14d-2580">The function Func_jp_bank_account finds content that matches the pattern.</span></span>
- <span data-ttu-id="cc14d-2581">Uma palavra-chave de Keyword_jp_bank_account for encontrada.</span><span class="sxs-lookup"><span data-stu-id="cc14d-2581">A keyword from Keyword_jp_bank_account is found.</span></span>
- <span data-ttu-id="cc14d-2582">Uma das seguintes opções for verdadeira:</span><span class="sxs-lookup"><span data-stu-id="cc14d-2582">One of the following is true:</span></span>
- <span data-ttu-id="cc14d-2583">A função Func_jp_bank_account_branch_code localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="cc14d-2583">The function Func_jp_bank_account_branch_code finds content that matches the pattern.</span></span>
- <span data-ttu-id="cc14d-2584">Uma palavra-chave de Keyword_jp_bank_branch_code for encontrada.</span><span class="sxs-lookup"><span data-stu-id="cc14d-2584">A keyword from Keyword_jp_bank_branch_code is found.</span></span>

<span data-ttu-id="cc14d-2585">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="cc14d-2585">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="cc14d-2586">A função Func_jp_bank_account localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="cc14d-2586">The function Func_jp_bank_account finds content that matches the pattern.</span></span>
- <span data-ttu-id="cc14d-2587">Uma palavra-chave de Keyword_jp_bank_account for encontrada.</span><span class="sxs-lookup"><span data-stu-id="cc14d-2587">A keyword from Keyword_jp_bank_account is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="cc14d-2588">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="cc14d-2588">Keywords</span></span>

#### <a name="keywordjpbankaccount"></a><span data-ttu-id="cc14d-2589">Keyword_jp_bank_account</span><span class="sxs-lookup"><span data-stu-id="cc14d-2589">Keyword_jp_bank_account</span></span>

- <span data-ttu-id="cc14d-2590">Checking Account Number</span><span class="sxs-lookup"><span data-stu-id="cc14d-2590">Checking Account Number</span></span> 
- <span data-ttu-id="cc14d-2591">Checking Account</span><span class="sxs-lookup"><span data-stu-id="cc14d-2591">Checking Account</span></span> 
- <span data-ttu-id="cc14d-2592">Checking Account #</span><span class="sxs-lookup"><span data-stu-id="cc14d-2592">Checking Account #</span></span> 
- <span data-ttu-id="cc14d-2593">Checking Acct Number</span><span class="sxs-lookup"><span data-stu-id="cc14d-2593">Checking Acct Number</span></span> 
- <span data-ttu-id="cc14d-2594">Checking Acct #</span><span class="sxs-lookup"><span data-stu-id="cc14d-2594">Checking Acct #</span></span> 
- <span data-ttu-id="cc14d-2595">Checking Acct No.</span><span class="sxs-lookup"><span data-stu-id="cc14d-2595">Checking Acct No.</span></span> 
- <span data-ttu-id="cc14d-2596">Checking Account No.</span><span class="sxs-lookup"><span data-stu-id="cc14d-2596">Checking Account No.</span></span> 
- <span data-ttu-id="cc14d-2597">Bank Account Number</span><span class="sxs-lookup"><span data-stu-id="cc14d-2597">Bank Account Number</span></span> 
- <span data-ttu-id="cc14d-2598">Bank Account</span><span class="sxs-lookup"><span data-stu-id="cc14d-2598">Bank Account</span></span> 
- <span data-ttu-id="cc14d-2599">Bank Account #</span><span class="sxs-lookup"><span data-stu-id="cc14d-2599">Bank Account #</span></span> 
- <span data-ttu-id="cc14d-2600">Bank Acct Number</span><span class="sxs-lookup"><span data-stu-id="cc14d-2600">Bank Acct Number</span></span> 
- <span data-ttu-id="cc14d-2601">Bank Acct #</span><span class="sxs-lookup"><span data-stu-id="cc14d-2601">Bank Acct #</span></span> 
- <span data-ttu-id="cc14d-2602">Bank Acct No.</span><span class="sxs-lookup"><span data-stu-id="cc14d-2602">Bank Acct No.</span></span> 
- <span data-ttu-id="cc14d-2603">Bank Account No.</span><span class="sxs-lookup"><span data-stu-id="cc14d-2603">Bank Account No.</span></span> 
- <span data-ttu-id="cc14d-2604">Savings Account Number</span><span class="sxs-lookup"><span data-stu-id="cc14d-2604">Savings Account Number</span></span> 
- <span data-ttu-id="cc14d-2605">Savings Account</span><span class="sxs-lookup"><span data-stu-id="cc14d-2605">Savings Account</span></span> 
- <span data-ttu-id="cc14d-2606">Savings Account #</span><span class="sxs-lookup"><span data-stu-id="cc14d-2606">Savings Account #</span></span> 
- <span data-ttu-id="cc14d-2607">Savings Acct Number</span><span class="sxs-lookup"><span data-stu-id="cc14d-2607">Savings Acct Number</span></span> 
- <span data-ttu-id="cc14d-2608">Savings Acct #</span><span class="sxs-lookup"><span data-stu-id="cc14d-2608">Savings Acct #</span></span> 
- <span data-ttu-id="cc14d-2609">Savings Acct No.</span><span class="sxs-lookup"><span data-stu-id="cc14d-2609">Savings Acct No.</span></span> 
- <span data-ttu-id="cc14d-2610">Savings Account No.</span><span class="sxs-lookup"><span data-stu-id="cc14d-2610">Savings Account No.</span></span> 
- <span data-ttu-id="cc14d-2611">Debit Account Number</span><span class="sxs-lookup"><span data-stu-id="cc14d-2611">Debit Account Number</span></span> 
- <span data-ttu-id="cc14d-2612">Debit Account</span><span class="sxs-lookup"><span data-stu-id="cc14d-2612">Debit Account</span></span> 
- <span data-ttu-id="cc14d-2613">Debit Account #</span><span class="sxs-lookup"><span data-stu-id="cc14d-2613">Debit Account #</span></span> 
- <span data-ttu-id="cc14d-2614">Debit Acct Number</span><span class="sxs-lookup"><span data-stu-id="cc14d-2614">Debit Acct Number</span></span> 
- <span data-ttu-id="cc14d-2615">Debit Acct #</span><span class="sxs-lookup"><span data-stu-id="cc14d-2615">Debit Acct #</span></span> 
- <span data-ttu-id="cc14d-2616">Debit Acct No.</span><span class="sxs-lookup"><span data-stu-id="cc14d-2616">Debit Acct No.</span></span> 
- <span data-ttu-id="cc14d-2617">Debit Account No.</span><span class="sxs-lookup"><span data-stu-id="cc14d-2617">Debit Account No.</span></span> 
- <span data-ttu-id="cc14d-2618">口座番号を当座預金口座の確認</span><span class="sxs-lookup"><span data-stu-id="cc14d-2618">口座番号を当座預金口座の確認</span></span> 
- <span data-ttu-id="cc14d-2619">#アカウントの確認 、 勘定番号の確認</span><span class="sxs-lookup"><span data-stu-id="cc14d-2619">＃アカウントの確認、勘定番号の確認</span></span> 
- <span data-ttu-id="cc14d-2620">#勘定の確認</span><span class="sxs-lookup"><span data-stu-id="cc14d-2620">＃勘定の確認</span></span> 
- <span data-ttu-id="cc14d-2621">勘定番号の確認</span><span class="sxs-lookup"><span data-stu-id="cc14d-2621">勘定番号の確認</span></span> 
- <span data-ttu-id="cc14d-2622">口座番号の確認</span><span class="sxs-lookup"><span data-stu-id="cc14d-2622">口座番号の確認</span></span> 
- <span data-ttu-id="cc14d-2623">銀行口座番号</span><span class="sxs-lookup"><span data-stu-id="cc14d-2623">銀行口座番号</span></span> 
- <span data-ttu-id="cc14d-2624">銀行口座</span><span class="sxs-lookup"><span data-stu-id="cc14d-2624">銀行口座</span></span> 
- <span data-ttu-id="cc14d-2625">銀行口座 #</span><span class="sxs-lookup"><span data-stu-id="cc14d-2625">銀行口座＃</span></span> 
- <span data-ttu-id="cc14d-2626">銀行の勘定番号</span><span class="sxs-lookup"><span data-stu-id="cc14d-2626">銀行の勘定番号</span></span> 
- <span data-ttu-id="cc14d-2627">銀行のacct #</span><span class="sxs-lookup"><span data-stu-id="cc14d-2627">銀行のacct＃</span></span> 
- <span data-ttu-id="cc14d-2628">銀行の勘定いいえ</span><span class="sxs-lookup"><span data-stu-id="cc14d-2628">銀行の勘定いいえ</span></span> 
- <span data-ttu-id="cc14d-2629">銀行口座番号</span><span class="sxs-lookup"><span data-stu-id="cc14d-2629">銀行口座番号</span></span>
- <span data-ttu-id="cc14d-2630">普通預金口座番号</span><span class="sxs-lookup"><span data-stu-id="cc14d-2630">普通預金口座番号</span></span> 
- <span data-ttu-id="cc14d-2631">預金口座</span><span class="sxs-lookup"><span data-stu-id="cc14d-2631">預金口座</span></span> 
- <span data-ttu-id="cc14d-2632">貯蓄口座 #</span><span class="sxs-lookup"><span data-stu-id="cc14d-2632">貯蓄口座＃</span></span> 
- <span data-ttu-id="cc14d-2633">貯蓄勘定の数</span><span class="sxs-lookup"><span data-stu-id="cc14d-2633">貯蓄勘定の数</span></span> 
- <span data-ttu-id="cc14d-2634">貯蓄勘定 #</span><span class="sxs-lookup"><span data-stu-id="cc14d-2634">貯蓄勘定＃</span></span> 
- <span data-ttu-id="cc14d-2635">貯蓄勘定番号</span><span class="sxs-lookup"><span data-stu-id="cc14d-2635">貯蓄勘定番号</span></span> 
- <span data-ttu-id="cc14d-2636">普通預金口座番号</span><span class="sxs-lookup"><span data-stu-id="cc14d-2636">普通預金口座番号</span></span> 
- <span data-ttu-id="cc14d-2637">引き落とし口座番号</span><span class="sxs-lookup"><span data-stu-id="cc14d-2637">引き落とし口座番号</span></span> 
- <span data-ttu-id="cc14d-2638">口座番号</span><span class="sxs-lookup"><span data-stu-id="cc14d-2638">口座番号</span></span> 
- <span data-ttu-id="cc14d-2639">口座番号 #</span><span class="sxs-lookup"><span data-stu-id="cc14d-2639">口座番号＃</span></span> 
- <span data-ttu-id="cc14d-2640">デビットのacct番号</span><span class="sxs-lookup"><span data-stu-id="cc14d-2640">デビットのacct番号</span></span> 
- <span data-ttu-id="cc14d-2641">デビット勘定 #</span><span class="sxs-lookup"><span data-stu-id="cc14d-2641">デビット勘定＃</span></span> 
- <span data-ttu-id="cc14d-2642">デビットACCTの番号</span><span class="sxs-lookup"><span data-stu-id="cc14d-2642">デビットACCTの番号</span></span> 
- <span data-ttu-id="cc14d-2643">デビット口座番号</span><span class="sxs-lookup"><span data-stu-id="cc14d-2643">デビット口座番号</span></span> 

#### <a name="keywordjpbankbranchcode"></a><span data-ttu-id="cc14d-2644">Keyword_jp_bank_branch_code</span><span class="sxs-lookup"><span data-stu-id="cc14d-2644">Keyword_jp_bank_branch_code</span></span>

<span data-ttu-id="cc14d-2645">Otemachi</span><span class="sxs-lookup"><span data-stu-id="cc14d-2645">Otemachi</span></span>

## <a name="japan-drivers-license-number"></a><span data-ttu-id="cc14d-2646">Número de carteira de motorista do Japão</span><span class="sxs-lookup"><span data-stu-id="cc14d-2646">Japan Driver's License Number</span></span>

### <a name="format"></a><span data-ttu-id="cc14d-2647">Format</span><span class="sxs-lookup"><span data-stu-id="cc14d-2647">Format</span></span>

<span data-ttu-id="cc14d-2648">12 dígitos</span><span class="sxs-lookup"><span data-stu-id="cc14d-2648">12 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="cc14d-2649">Padrão</span><span class="sxs-lookup"><span data-stu-id="cc14d-2649">Pattern</span></span>

<span data-ttu-id="cc14d-2650">12 dígitos consecutivos</span><span class="sxs-lookup"><span data-stu-id="cc14d-2650">12 consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="cc14d-2651">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="cc14d-2651">Checksum</span></span>

<span data-ttu-id="cc14d-2652">Não</span><span class="sxs-lookup"><span data-stu-id="cc14d-2652">No</span></span>

### <a name="definition"></a><span data-ttu-id="cc14d-2653">Definição</span><span class="sxs-lookup"><span data-stu-id="cc14d-2653">Definition</span></span>

<span data-ttu-id="cc14d-2654">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="cc14d-2654">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="cc14d-2655">A função Func_jp_drivers_license_number localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="cc14d-2655">The function Func_jp_drivers_license_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="cc14d-2656">Uma palavra-chave de Keyword_jp_drivers_license_number for encontrada.</span><span class="sxs-lookup"><span data-stu-id="cc14d-2656">A keyword from Keyword_jp_drivers_license_number is found.</span></span>

```
<!-- Japan Driver's License Number -->
<Entity id="c6011143-d087-451c-8313-7f6d4aed2270" patternsProximity="300" recommendedConfidence="75">
    <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_jp_drivers_license_number" />
        <Match idRef ="Keyword_jp_drivers_license_number" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="cc14d-2657">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="cc14d-2657">Keywords</span></span>

#### <a name="keywordjpdriverslicensenumber"></a><span data-ttu-id="cc14d-2658">Keyword_jp_drivers_license_number</span><span class="sxs-lookup"><span data-stu-id="cc14d-2658">Keyword_jp_drivers_license_number</span></span>

- <span data-ttu-id="cc14d-2659">distribuição</span><span class="sxs-lookup"><span data-stu-id="cc14d-2659">dl#</span></span> 
- <span data-ttu-id="cc14d-2660">DISTRIBUIÇÃO</span><span class="sxs-lookup"><span data-stu-id="cc14d-2660">DL＃</span></span> 
- <span data-ttu-id="cc14d-2661">DL</span><span class="sxs-lookup"><span data-stu-id="cc14d-2661">dls#</span></span> 
- <span data-ttu-id="cc14d-2662">DL</span><span class="sxs-lookup"><span data-stu-id="cc14d-2662">DLS＃</span></span> 
- <span data-ttu-id="cc14d-2663">driver license</span><span class="sxs-lookup"><span data-stu-id="cc14d-2663">driver license</span></span> 
- <span data-ttu-id="cc14d-2664">driver licenses</span><span class="sxs-lookup"><span data-stu-id="cc14d-2664">driver licenses</span></span> 
- <span data-ttu-id="cc14d-2665">drivers license</span><span class="sxs-lookup"><span data-stu-id="cc14d-2665">drivers license</span></span> 
- <span data-ttu-id="cc14d-2666">driver's license</span><span class="sxs-lookup"><span data-stu-id="cc14d-2666">driver's license</span></span> 
- <span data-ttu-id="cc14d-2667">drivers licenses</span><span class="sxs-lookup"><span data-stu-id="cc14d-2667">drivers licenses</span></span> 
- <span data-ttu-id="cc14d-2668">driver's licenses</span><span class="sxs-lookup"><span data-stu-id="cc14d-2668">driver's licenses</span></span> 
- <span data-ttu-id="cc14d-2669">driving licence</span><span class="sxs-lookup"><span data-stu-id="cc14d-2669">driving licence</span></span> 
- <span data-ttu-id="cc14d-2670">driver'lic</span><span class="sxs-lookup"><span data-stu-id="cc14d-2670">lic#</span></span> 
- <span data-ttu-id="cc14d-2671">DRIVER'LIC</span><span class="sxs-lookup"><span data-stu-id="cc14d-2671">LIC＃</span></span> 
- <span data-ttu-id="cc14d-2672">driver'lics</span><span class="sxs-lookup"><span data-stu-id="cc14d-2672">lics#</span></span> 
- <span data-ttu-id="cc14d-2673">state id</span><span class="sxs-lookup"><span data-stu-id="cc14d-2673">state id</span></span> 
- <span data-ttu-id="cc14d-2674">state identification</span><span class="sxs-lookup"><span data-stu-id="cc14d-2674">state identification</span></span> 
- <span data-ttu-id="cc14d-2675">state identification number</span><span class="sxs-lookup"><span data-stu-id="cc14d-2675">state identification number</span></span> 
- <span data-ttu-id="cc14d-2676">低所得国 #</span><span class="sxs-lookup"><span data-stu-id="cc14d-2676">低所得国＃</span></span> 
- <span data-ttu-id="cc14d-2677">免許証</span><span class="sxs-lookup"><span data-stu-id="cc14d-2677">免許証</span></span> 
- <span data-ttu-id="cc14d-2678">状態ID</span><span class="sxs-lookup"><span data-stu-id="cc14d-2678">状態ID</span></span>
- <span data-ttu-id="cc14d-2679">状態の識別</span><span class="sxs-lookup"><span data-stu-id="cc14d-2679">状態の識別</span></span> 
- <span data-ttu-id="cc14d-2680">状態の識別番号</span><span class="sxs-lookup"><span data-stu-id="cc14d-2680">状態の識別番号</span></span> 
- <span data-ttu-id="cc14d-2681">運転免許</span><span class="sxs-lookup"><span data-stu-id="cc14d-2681">運転免許</span></span> 
- <span data-ttu-id="cc14d-2682">運転免許証</span><span class="sxs-lookup"><span data-stu-id="cc14d-2682">運転免許証</span></span> 
- <span data-ttu-id="cc14d-2683">運転免許証番号</span><span class="sxs-lookup"><span data-stu-id="cc14d-2683">運転免許証番号</span></span> 
   
## <a name="japan-passport-number"></a><span data-ttu-id="cc14d-2684">Número de passaporte do Japão</span><span class="sxs-lookup"><span data-stu-id="cc14d-2684">Japan Passport Number</span></span>

### <a name="format"></a><span data-ttu-id="cc14d-2685">Format</span><span class="sxs-lookup"><span data-stu-id="cc14d-2685">Format</span></span>

<span data-ttu-id="cc14d-2686">Duas letras seguidas por sete dígitos</span><span class="sxs-lookup"><span data-stu-id="cc14d-2686">Two letters followed by seven digits</span></span>

### <a name="pattern"></a><span data-ttu-id="cc14d-2687">Padrão</span><span class="sxs-lookup"><span data-stu-id="cc14d-2687">Pattern</span></span>

<span data-ttu-id="cc14d-2688">Duas letras (não diferencia maiúsculas de minúsculas) seguidas de sete dígitos</span><span class="sxs-lookup"><span data-stu-id="cc14d-2688">Two letters (not case sensitive) followed by seven digits</span></span>

### <a name="checksum"></a><span data-ttu-id="cc14d-2689">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="cc14d-2689">Checksum</span></span>

<span data-ttu-id="cc14d-2690">Não</span><span class="sxs-lookup"><span data-stu-id="cc14d-2690">No</span></span>

### <a name="definition"></a><span data-ttu-id="cc14d-2691">Definição</span><span class="sxs-lookup"><span data-stu-id="cc14d-2691">Definition</span></span>

<span data-ttu-id="cc14d-2692">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="cc14d-2692">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="cc14d-2693">A função Func_jp_passport localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="cc14d-2693">The function Func_jp_passport finds content that matches the pattern.</span></span>
- <span data-ttu-id="cc14d-2694">Uma palavra-chave de Keyword_jp_passport for encontrada.</span><span class="sxs-lookup"><span data-stu-id="cc14d-2694">A keyword from Keyword_jp_passport is found.</span></span>

```
<!-- Japan Passport Number -->
<Entity id="75177310-1a09-4613-bf6d-833aae3743f8" patternsProximity="300" recommendedConfidence="75">
    <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_jp_passport" />
        <Match idRef="Keyword_jp_passport" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="cc14d-2695">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="cc14d-2695">Keywords</span></span>

#### <a name="keywordjppassport"></a><span data-ttu-id="cc14d-2696">Keyword_jp_passport</span><span class="sxs-lookup"><span data-stu-id="cc14d-2696">Keyword_jp_passport</span></span>

- <span data-ttu-id="cc14d-2697">パスポート</span><span class="sxs-lookup"><span data-stu-id="cc14d-2697">パスポート</span></span> 
- <span data-ttu-id="cc14d-2698">パスポート番号</span><span class="sxs-lookup"><span data-stu-id="cc14d-2698">パスポート番号</span></span> 
- <span data-ttu-id="cc14d-2699">パスポートのNum</span><span class="sxs-lookup"><span data-stu-id="cc14d-2699">パスポートのNum</span></span> 
- <span data-ttu-id="cc14d-2700">パスポート #</span><span class="sxs-lookup"><span data-stu-id="cc14d-2700">パスポート＃</span></span> 
   
## <a name="japan-resident-registration-number"></a><span data-ttu-id="cc14d-2701">Número de registro de residente do Japão</span><span class="sxs-lookup"><span data-stu-id="cc14d-2701">Japan Resident Registration Number</span></span>

### <a name="format"></a><span data-ttu-id="cc14d-2702">Format</span><span class="sxs-lookup"><span data-stu-id="cc14d-2702">Format</span></span>

<span data-ttu-id="cc14d-2703">11 dígitos</span><span class="sxs-lookup"><span data-stu-id="cc14d-2703">11 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="cc14d-2704">Padrão</span><span class="sxs-lookup"><span data-stu-id="cc14d-2704">Pattern</span></span>

<span data-ttu-id="cc14d-2705">11 dígitos consecutivos</span><span class="sxs-lookup"><span data-stu-id="cc14d-2705">11 consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="cc14d-2706">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="cc14d-2706">Checksum</span></span>

<span data-ttu-id="cc14d-2707">Não</span><span class="sxs-lookup"><span data-stu-id="cc14d-2707">No</span></span>

### <a name="definition"></a><span data-ttu-id="cc14d-2708">Definição</span><span class="sxs-lookup"><span data-stu-id="cc14d-2708">Definition</span></span>

<span data-ttu-id="cc14d-2709">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="cc14d-2709">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="cc14d-2710">A função Func_jp_resident_registration_number localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="cc14d-2710">The function Func_jp_resident_registration_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="cc14d-2711">Uma palavra-chave de Keyword_jp_resident_registration_number for encontrada.</span><span class="sxs-lookup"><span data-stu-id="cc14d-2711">A keyword from Keyword_jp_resident_registration_number is found.</span></span>

```
<!-- Japan Resident Registration Number -->
<Entity id="01c1209b-6389-4faf-a5f8-3f7e13899652" patternsProximity="300" recommendedConfidence="75">
    <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_jp_resident_registration_number" />
        <Match idRef ="Keyword_jp_resident_registration_number" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="cc14d-2712">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="cc14d-2712">Keywords</span></span>

#### <a name="keywordjpresidentregistrationnumber"></a><span data-ttu-id="cc14d-2713">Keyword_jp_resident_registration_number</span><span class="sxs-lookup"><span data-stu-id="cc14d-2713">Keyword_jp_resident_registration_number</span></span>

- <span data-ttu-id="cc14d-2714">Resident Registration Number</span><span class="sxs-lookup"><span data-stu-id="cc14d-2714">Resident Registration Number</span></span>
- <span data-ttu-id="cc14d-2715">Resident Register Number</span><span class="sxs-lookup"><span data-stu-id="cc14d-2715">Resident Register Number</span></span> 
- <span data-ttu-id="cc14d-2716">Residents Basic Registry Number</span><span class="sxs-lookup"><span data-stu-id="cc14d-2716">Residents Basic Registry Number</span></span> 
- <span data-ttu-id="cc14d-2717">Resident Registration No.</span><span class="sxs-lookup"><span data-stu-id="cc14d-2717">Resident Registration No.</span></span> 
- <span data-ttu-id="cc14d-2718">Resident Register No.</span><span class="sxs-lookup"><span data-stu-id="cc14d-2718">Resident Register No.</span></span> 
- <span data-ttu-id="cc14d-2719">Residents Basic Registry No.</span><span class="sxs-lookup"><span data-stu-id="cc14d-2719">Residents Basic Registry No.</span></span> 
- <span data-ttu-id="cc14d-2720">Basic Resident Register No.</span><span class="sxs-lookup"><span data-stu-id="cc14d-2720">Basic Resident Register No.</span></span> 
- <span data-ttu-id="cc14d-2721">住民登録番号 、 登録番号をレジデント</span><span class="sxs-lookup"><span data-stu-id="cc14d-2721">住民登録番号、登録番号をレジデント</span></span> 
- <span data-ttu-id="cc14d-2722">住民基本登録番号 、 登録番号</span><span class="sxs-lookup"><span data-stu-id="cc14d-2722">住民基本登録番号、登録番号</span></span> 
- <span data-ttu-id="cc14d-2723">住民基本レジストリ番号を常駐</span><span class="sxs-lookup"><span data-stu-id="cc14d-2723">住民基本レジストリ番号を常駐</span></span> 
- <span data-ttu-id="cc14d-2724">登録番号を常駐住民基本台帳登録番号</span><span class="sxs-lookup"><span data-stu-id="cc14d-2724">登録番号を常駐住民基本台帳登録番号</span></span> 

   
## <a name="japan-social-insurance-number-sin"></a><span data-ttu-id="cc14d-2725">Número de seguro social do Japão (SIN)</span><span class="sxs-lookup"><span data-stu-id="cc14d-2725">Japan Social Insurance Number (SIN)</span></span>

### <a name="format"></a><span data-ttu-id="cc14d-2726">Format</span><span class="sxs-lookup"><span data-stu-id="cc14d-2726">Format</span></span>

<span data-ttu-id="cc14d-2727">7 a 12 dígitos</span><span class="sxs-lookup"><span data-stu-id="cc14d-2727">7-12 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="cc14d-2728">Padrão</span><span class="sxs-lookup"><span data-stu-id="cc14d-2728">Pattern</span></span>

<span data-ttu-id="cc14d-2729">7 a 12 dígitos:</span><span class="sxs-lookup"><span data-stu-id="cc14d-2729">7-12 digits:</span></span>
- <span data-ttu-id="cc14d-2730">Quatro dígitos</span><span class="sxs-lookup"><span data-stu-id="cc14d-2730">Four digits</span></span> 
- <span data-ttu-id="cc14d-2731">Um hífen (opcional)</span><span class="sxs-lookup"><span data-stu-id="cc14d-2731">A hyphen (optional)</span></span> 
- <span data-ttu-id="cc14d-2732">Seis dígitos ou</span><span class="sxs-lookup"><span data-stu-id="cc14d-2732">Six digits OR</span></span>
- <span data-ttu-id="cc14d-2733">7 a 12 dígitos consecutivos</span><span class="sxs-lookup"><span data-stu-id="cc14d-2733">7-12 consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="cc14d-2734">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="cc14d-2734">Checksum</span></span>

<span data-ttu-id="cc14d-2735">Não</span><span class="sxs-lookup"><span data-stu-id="cc14d-2735">No</span></span>

### <a name="definition"></a><span data-ttu-id="cc14d-2736">Definição</span><span class="sxs-lookup"><span data-stu-id="cc14d-2736">Definition</span></span>

<span data-ttu-id="cc14d-2737">Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="cc14d-2737">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="cc14d-2738">A função Func_jp_sin localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="cc14d-2738">The function Func_jp_sin finds content that matches the pattern.</span></span>
- <span data-ttu-id="cc14d-2739">Uma palavra-chave de Keyword_jp_sin for encontrada.</span><span class="sxs-lookup"><span data-stu-id="cc14d-2739">A keyword from Keyword_jp_sin is found.</span></span>

<span data-ttu-id="cc14d-2740">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="cc14d-2740">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="cc14d-2741">A função Func_jp_sin_pre_1997 localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="cc14d-2741">The function Func_jp_sin_pre_1997 finds content that matches the pattern.</span></span>
- <span data-ttu-id="cc14d-2742">Uma palavra-chave de Keyword_jp_sin for encontrada.</span><span class="sxs-lookup"><span data-stu-id="cc14d-2742">A keyword from Keyword_jp_sin is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="cc14d-2743">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="cc14d-2743">Keywords</span></span>

#### <a name="keywordjpsin"></a><span data-ttu-id="cc14d-2744">Keyword_jp_sin</span><span class="sxs-lookup"><span data-stu-id="cc14d-2744">Keyword_jp_sin</span></span>

- <span data-ttu-id="cc14d-2745">Social Insurance No.</span><span class="sxs-lookup"><span data-stu-id="cc14d-2745">Social Insurance No.</span></span> 
- <span data-ttu-id="cc14d-2746">Social Insurance Num</span><span class="sxs-lookup"><span data-stu-id="cc14d-2746">Social Insurance Num</span></span> 
- <span data-ttu-id="cc14d-2747">Social Insurance Number</span><span class="sxs-lookup"><span data-stu-id="cc14d-2747">Social Insurance Number</span></span> 
- <span data-ttu-id="cc14d-2748">社会保険のテンキー</span><span class="sxs-lookup"><span data-stu-id="cc14d-2748">社会保険のテンキー</span></span> 
- <span data-ttu-id="cc14d-2749">社会保険番号</span><span class="sxs-lookup"><span data-stu-id="cc14d-2749">社会保険番号</span></span> 

## <a name="japanese-residence-card-number"></a><span data-ttu-id="cc14d-2750">Número do cartão de residência japonês</span><span class="sxs-lookup"><span data-stu-id="cc14d-2750">Japanese Residence Card Number</span></span>

### <a name="format"></a><span data-ttu-id="cc14d-2751">Format</span><span class="sxs-lookup"><span data-stu-id="cc14d-2751">Format</span></span>

<span data-ttu-id="cc14d-2752">12 letras e dígitos</span><span class="sxs-lookup"><span data-stu-id="cc14d-2752">12 letters and digits</span></span>

### <a name="pattern"></a><span data-ttu-id="cc14d-2753">Padrão</span><span class="sxs-lookup"><span data-stu-id="cc14d-2753">Pattern</span></span>

<span data-ttu-id="cc14d-2754">12 letras e dígitos:</span><span class="sxs-lookup"><span data-stu-id="cc14d-2754">12 letters and digits:</span></span>
- <span data-ttu-id="cc14d-2755">Duas letras (não diferenciam maiúsculas de minúsculas)</span><span class="sxs-lookup"><span data-stu-id="cc14d-2755">Two letters (not case sensitive)</span></span>
- <span data-ttu-id="cc14d-2756">Oito dígitos</span><span class="sxs-lookup"><span data-stu-id="cc14d-2756">Eight digits</span></span> 
- <span data-ttu-id="cc14d-2757">Duas letras (não diferenciam maiúsculas de minúsculas)</span><span class="sxs-lookup"><span data-stu-id="cc14d-2757">Two letters (not case sensitive)</span></span>

### <a name="checksum"></a><span data-ttu-id="cc14d-2758">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="cc14d-2758">Checksum</span></span>

<span data-ttu-id="cc14d-2759">Não</span><span class="sxs-lookup"><span data-stu-id="cc14d-2759">No</span></span>

### <a name="definition"></a><span data-ttu-id="cc14d-2760">Definição</span><span class="sxs-lookup"><span data-stu-id="cc14d-2760">Definition</span></span>

<span data-ttu-id="cc14d-2761">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="cc14d-2761">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="cc14d-2762">A expressão regular Regex_jp_residence_card_number localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="cc14d-2762">The regular expression Regex_jp_residence_card_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="cc14d-2763">Uma palavra-chave de Keyword_jp_residence_card_number for encontrada.</span><span class="sxs-lookup"><span data-stu-id="cc14d-2763">A keyword from Keyword_jp_residence_card_number is found.</span></span>

```
<!--Japan Residence Card Number-->
-<Entity id="ac36fef2-a289-4e2c-bb48-b02366e89fc0" recommendedConfidence="75" patternsProximity="300">
   -<Pattern confidenceLevel="75">
      <IdMatch idRef="Regex_jp_residence_card_number"/>
      <Match idRef="Keyword_jp_residence_card_number"/>
   </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="cc14d-2764">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="cc14d-2764">Keywords</span></span>

#### <a name="keywordjpresidencecardnumber"></a><span data-ttu-id="cc14d-2765">Keyword_jp_residence_card_number</span><span class="sxs-lookup"><span data-stu-id="cc14d-2765">Keyword_jp_residence_card_number</span></span>

- <span data-ttu-id="cc14d-2766">Número do cartão de residência</span><span class="sxs-lookup"><span data-stu-id="cc14d-2766">Residence card number</span></span>
- <span data-ttu-id="cc14d-2767">Número do cartão de residência</span><span class="sxs-lookup"><span data-stu-id="cc14d-2767">Residence card no</span></span>
- <span data-ttu-id="cc14d-2768">N º do cartão de residência</span><span class="sxs-lookup"><span data-stu-id="cc14d-2768">Residence card #</span></span>
- <span data-ttu-id="cc14d-2769">在留カード番号</span><span class="sxs-lookup"><span data-stu-id="cc14d-2769">在留カード番号</span></span>
   
## <a name="malaysia-id-card-number"></a><span data-ttu-id="cc14d-2770">Número do Cartão de Identificação da Malásia</span><span class="sxs-lookup"><span data-stu-id="cc14d-2770">Malaysia ID Card Number</span></span>

### <a name="format"></a><span data-ttu-id="cc14d-2771">Format</span><span class="sxs-lookup"><span data-stu-id="cc14d-2771">Format</span></span>

<span data-ttu-id="cc14d-2772">12 dígitos contendo hifens opcionais</span><span class="sxs-lookup"><span data-stu-id="cc14d-2772">12 digits containing optional hyphens</span></span>

### <a name="pattern"></a><span data-ttu-id="cc14d-2773">Padrão</span><span class="sxs-lookup"><span data-stu-id="cc14d-2773">Pattern</span></span>

<span data-ttu-id="cc14d-2774">12 dígitos:</span><span class="sxs-lookup"><span data-stu-id="cc14d-2774">12 digits:</span></span>
- <span data-ttu-id="cc14d-2775">Seis dígitos no formato AAMMDD que são a data de nascimento</span><span class="sxs-lookup"><span data-stu-id="cc14d-2775">Six digits in the format YYMMDD which are the date of birth</span></span> 
- <span data-ttu-id="cc14d-2776">Um traço (opcional)</span><span class="sxs-lookup"><span data-stu-id="cc14d-2776">A dash (optional)</span></span> 
- <span data-ttu-id="cc14d-2777">Código do local de nascimento de duas letras </span><span class="sxs-lookup"><span data-stu-id="cc14d-2777">Two-letter place-of-birth code</span></span> 
- <span data-ttu-id="cc14d-2778">Um traço (opcional)</span><span class="sxs-lookup"><span data-stu-id="cc14d-2778">A dash (optional)</span></span> 
- <span data-ttu-id="cc14d-2779">Três dígitos aleatórios </span><span class="sxs-lookup"><span data-stu-id="cc14d-2779">Three random digits</span></span> 
- <span data-ttu-id="cc14d-2780">Código de sexo de um dígito</span><span class="sxs-lookup"><span data-stu-id="cc14d-2780">One-digit gender code</span></span>

### <a name="checksum"></a><span data-ttu-id="cc14d-2781">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="cc14d-2781">Checksum</span></span>

<span data-ttu-id="cc14d-2782">Não</span><span class="sxs-lookup"><span data-stu-id="cc14d-2782">No</span></span>

### <a name="definition"></a><span data-ttu-id="cc14d-2783">Definição</span><span class="sxs-lookup"><span data-stu-id="cc14d-2783">Definition</span></span>

<span data-ttu-id="cc14d-2784">Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="cc14d-2784">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="cc14d-2785">A expressão regular Regex_malaysia_id_card_number localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="cc14d-2785">The regular expression Regex_malaysia_id_card_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="cc14d-2786">Uma palavra-chave de Keyword_malaysia_id_card_number for encontrada.</span><span class="sxs-lookup"><span data-stu-id="cc14d-2786">A keyword from Keyword_malaysia_id_card_number is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="cc14d-2787">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="cc14d-2787">Keywords</span></span>
   
#### <a name="keywordmalaysiaidcardnumber"></a><span data-ttu-id="cc14d-2788">Keyword_malaysia_id_card_number</span><span class="sxs-lookup"><span data-stu-id="cc14d-2788">Keyword_malaysia_id_card_number</span></span>

- <span data-ttu-id="cc14d-2789">cartão de aplicativo digital</span><span class="sxs-lookup"><span data-stu-id="cc14d-2789">digital application card</span></span>
- <span data-ttu-id="cc14d-2790">e/c</span><span class="sxs-lookup"><span data-stu-id="cc14d-2790">i/c</span></span>
- <span data-ttu-id="cc14d-2791">e/c não</span><span class="sxs-lookup"><span data-stu-id="cc14d-2791">i/c no</span></span>
- <span data-ttu-id="cc14d-2792">Liga</span><span class="sxs-lookup"><span data-stu-id="cc14d-2792">ic</span></span>
- <span data-ttu-id="cc14d-2793">IC não</span><span class="sxs-lookup"><span data-stu-id="cc14d-2793">ic no</span></span>
- <span data-ttu-id="cc14d-2794">id card</span><span class="sxs-lookup"><span data-stu-id="cc14d-2794">id card</span></span>
- <span data-ttu-id="cc14d-2795">Cartão de identificação</span><span class="sxs-lookup"><span data-stu-id="cc14d-2795">identification Card</span></span>
- <span data-ttu-id="cc14d-2796">cartão de identidade</span><span class="sxs-lookup"><span data-stu-id="cc14d-2796">identity card</span></span>
- <span data-ttu-id="cc14d-2797">k/p</span><span class="sxs-lookup"><span data-stu-id="cc14d-2797">k/p</span></span>
- <span data-ttu-id="cc14d-2798">n/p não</span><span class="sxs-lookup"><span data-stu-id="cc14d-2798">k/p no</span></span>
- <span data-ttu-id="cc14d-2799">kad akuan diri</span><span class="sxs-lookup"><span data-stu-id="cc14d-2799">kad akuan diri</span></span>
- <span data-ttu-id="cc14d-2800">kad aplikasi digital</span><span class="sxs-lookup"><span data-stu-id="cc14d-2800">kad aplikasi digital</span></span>
- <span data-ttu-id="cc14d-2801">kad pengenalan Malásia</span><span class="sxs-lookup"><span data-stu-id="cc14d-2801">kad pengenalan malaysia</span></span>
- <span data-ttu-id="cc14d-2802">KP</span><span class="sxs-lookup"><span data-stu-id="cc14d-2802">kp</span></span>
- <span data-ttu-id="cc14d-2803">KP não</span><span class="sxs-lookup"><span data-stu-id="cc14d-2803">kp no</span></span>
- <span data-ttu-id="cc14d-2804">MyKad</span><span class="sxs-lookup"><span data-stu-id="cc14d-2804">mykad</span></span>
- <span data-ttu-id="cc14d-2805">Mykas</span><span class="sxs-lookup"><span data-stu-id="cc14d-2805">mykas</span></span>
- <span data-ttu-id="cc14d-2806">mykid</span><span class="sxs-lookup"><span data-stu-id="cc14d-2806">mykid</span></span>
- <span data-ttu-id="cc14d-2807">mypr</span><span class="sxs-lookup"><span data-stu-id="cc14d-2807">mypr</span></span>
- <span data-ttu-id="cc14d-2808">mytentera</span><span class="sxs-lookup"><span data-stu-id="cc14d-2808">mytentera</span></span>
- <span data-ttu-id="cc14d-2809">cartão de identidade da Malásia</span><span class="sxs-lookup"><span data-stu-id="cc14d-2809">malaysia identity card</span></span>
- <span data-ttu-id="cc14d-2810">cartão de identidade do Malasiano</span><span class="sxs-lookup"><span data-stu-id="cc14d-2810">malaysian identity card</span></span>
- <span data-ttu-id="cc14d-2811">NRIC</span><span class="sxs-lookup"><span data-stu-id="cc14d-2811">nric</span></span>
- <span data-ttu-id="cc14d-2812">cartão de identificação pessoal</span><span class="sxs-lookup"><span data-stu-id="cc14d-2812">personal identification card</span></span>
   
## <a name="netherlands-citizens-service-bsn-number"></a><span data-ttu-id="cc14d-2813">Número do Serviço do Cidadão (BSN) da Holland</span><span class="sxs-lookup"><span data-stu-id="cc14d-2813">Netherlands Citizen's Service (BSN) Number</span></span>

### <a name="format"></a><span data-ttu-id="cc14d-2814">Format</span><span class="sxs-lookup"><span data-stu-id="cc14d-2814">Format</span></span>

<span data-ttu-id="cc14d-2815">8 a 9 dígitos contendo espaços opcionais</span><span class="sxs-lookup"><span data-stu-id="cc14d-2815">8-9 digits containing optional spaces</span></span>

### <a name="pattern"></a><span data-ttu-id="cc14d-2816">Padrão</span><span class="sxs-lookup"><span data-stu-id="cc14d-2816">Pattern</span></span>

<span data-ttu-id="cc14d-2817">8 a 9 dígitos.</span><span class="sxs-lookup"><span data-stu-id="cc14d-2817">8-9 digits:</span></span>
- <span data-ttu-id="cc14d-2818">Três dígitos</span><span class="sxs-lookup"><span data-stu-id="cc14d-2818">Three digits</span></span> 
- <span data-ttu-id="cc14d-2819">Um espaço (opcional)</span><span class="sxs-lookup"><span data-stu-id="cc14d-2819">A space (optional)</span></span> 
- <span data-ttu-id="cc14d-2820">Três dígitos</span><span class="sxs-lookup"><span data-stu-id="cc14d-2820">Three digits</span></span> 
- <span data-ttu-id="cc14d-2821">Um espaço (opcional)</span><span class="sxs-lookup"><span data-stu-id="cc14d-2821">A space (optional)</span></span> 
- <span data-ttu-id="cc14d-2822">2 a 3 dígitos</span><span class="sxs-lookup"><span data-stu-id="cc14d-2822">2-3 digits</span></span>

### <a name="checksum"></a><span data-ttu-id="cc14d-2823">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="cc14d-2823">Checksum</span></span>

<span data-ttu-id="cc14d-2824">Sim</span><span class="sxs-lookup"><span data-stu-id="cc14d-2824">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="cc14d-2825">Definição</span><span class="sxs-lookup"><span data-stu-id="cc14d-2825">Definition</span></span>

<span data-ttu-id="cc14d-2826">Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="cc14d-2826">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="cc14d-2827">A função Func_netherlands_bsn localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="cc14d-2827">The function Func_netherlands_bsn finds content that matches the pattern.</span></span>
- <span data-ttu-id="cc14d-2828">Uma palavra-chave de Keyword_netherlands_bsn for encontrada.</span><span class="sxs-lookup"><span data-stu-id="cc14d-2828">A keyword from Keyword_netherlands_bsn is found.</span></span>
- <span data-ttu-id="cc14d-2829">A função Func_eu_date2 encontra uma data no formato de data à direita.</span><span class="sxs-lookup"><span data-stu-id="cc14d-2829">The function Func_eu_date2 finds a date in the right date format.</span></span>
- <span data-ttu-id="cc14d-2830">A soma de verificação passa.</span><span class="sxs-lookup"><span data-stu-id="cc14d-2830">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="cc14d-2831">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="cc14d-2831">Keywords</span></span>

#### <a name="keywordnetherlandsbsn"></a><span data-ttu-id="cc14d-2832">Keyword_netherlands_bsn</span><span class="sxs-lookup"><span data-stu-id="cc14d-2832">Keyword_netherlands_bsn</span></span>

- <span data-ttu-id="cc14d-2833">Número do serviço do cidadão</span><span class="sxs-lookup"><span data-stu-id="cc14d-2833">Citizen service number</span></span> 
- <span data-ttu-id="cc14d-2834">BSN</span><span class="sxs-lookup"><span data-stu-id="cc14d-2834">BSN</span></span> 
- <span data-ttu-id="cc14d-2835">Burgerservicenummer</span><span class="sxs-lookup"><span data-stu-id="cc14d-2835">Burgerservicenummer</span></span> 
- <span data-ttu-id="cc14d-2836">Sofinummer</span><span class="sxs-lookup"><span data-stu-id="cc14d-2836">Sofinummer</span></span> 
- <span data-ttu-id="cc14d-2837">Persoonsgebonden nummer</span><span class="sxs-lookup"><span data-stu-id="cc14d-2837">Persoonsgebonden nummer</span></span> 
- <span data-ttu-id="cc14d-2838">Persoonsnummer</span><span class="sxs-lookup"><span data-stu-id="cc14d-2838">Persoonsnummer</span></span>    

   
## <a name="new-zealand-ministry-of-health-number"></a><span data-ttu-id="cc14d-2839">Número do Ministério da Saúde da Nova Zelândia</span><span class="sxs-lookup"><span data-stu-id="cc14d-2839">New Zealand Ministry of Health Number</span></span>

### <a name="format"></a><span data-ttu-id="cc14d-2840">Format</span><span class="sxs-lookup"><span data-stu-id="cc14d-2840">Format</span></span>

<span data-ttu-id="cc14d-2841">Três letras, um espaço (opcional) e quatro dígitos</span><span class="sxs-lookup"><span data-stu-id="cc14d-2841">Three letters, a space (optional), and four digits</span></span>

### <a name="pattern"></a><span data-ttu-id="cc14d-2842">Padrão</span><span class="sxs-lookup"><span data-stu-id="cc14d-2842">Pattern</span></span>

<span data-ttu-id="cc14d-2843">Três letras (não diferencia maiúsculas de minúsculas) um espaço (opcional) quatro dígitos</span><span class="sxs-lookup"><span data-stu-id="cc14d-2843">Three letters (not case sensitive) a space (optional) four digits</span></span>

### <a name="checksum"></a><span data-ttu-id="cc14d-2844">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="cc14d-2844">Checksum</span></span>

<span data-ttu-id="cc14d-2845">Sim</span><span class="sxs-lookup"><span data-stu-id="cc14d-2845">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="cc14d-2846">Definição</span><span class="sxs-lookup"><span data-stu-id="cc14d-2846">Definition</span></span>

<span data-ttu-id="cc14d-2847">Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="cc14d-2847">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="cc14d-2848">A função Func_new_zealand_ministry_of_health_number localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="cc14d-2848">The function Func_new_zealand_ministry_of_health_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="cc14d-2849">Uma palavra-chave de Keyword_nz_terms for encontrada.</span><span class="sxs-lookup"><span data-stu-id="cc14d-2849">A keyword from Keyword_nz_terms is found.</span></span>
- <span data-ttu-id="cc14d-2850">A soma de verificação passa.</span><span class="sxs-lookup"><span data-stu-id="cc14d-2850">The checksum passes.</span></span>

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

<span data-ttu-id="cc14d-2851">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="cc14d-2851">Keywords</span></span>

<span data-ttu-id="cc14d-2852">Keyword_nz_terms</span><span class="sxs-lookup"><span data-stu-id="cc14d-2852">Keyword_nz_terms</span></span>

- <span data-ttu-id="cc14d-2853">NHI</span><span class="sxs-lookup"><span data-stu-id="cc14d-2853">NHI</span></span> 
- <span data-ttu-id="cc14d-2854">Nova Zelândia</span><span class="sxs-lookup"><span data-stu-id="cc14d-2854">New Zealand</span></span> 
- <span data-ttu-id="cc14d-2855">Saúde</span><span class="sxs-lookup"><span data-stu-id="cc14d-2855">Health</span></span> 
- <span data-ttu-id="cc14d-2856">tratamento</span><span class="sxs-lookup"><span data-stu-id="cc14d-2856">treatment</span></span> 
   
## <a name="norway-identification-number"></a><span data-ttu-id="cc14d-2857">Número de Identificação da Noruega</span><span class="sxs-lookup"><span data-stu-id="cc14d-2857">Norway Identification Number</span></span>

### <a name="format"></a><span data-ttu-id="cc14d-2858">Format</span><span class="sxs-lookup"><span data-stu-id="cc14d-2858">Format</span></span>

<span data-ttu-id="cc14d-2859">11 dígitos</span><span class="sxs-lookup"><span data-stu-id="cc14d-2859">11 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="cc14d-2860">Padrão</span><span class="sxs-lookup"><span data-stu-id="cc14d-2860">Pattern</span></span>

<span data-ttu-id="cc14d-2861">11 dígitos:</span><span class="sxs-lookup"><span data-stu-id="cc14d-2861">11 digits:</span></span>
- <span data-ttu-id="cc14d-2862">Seis dígitos no formato DDMMAA que são a data de nascimento</span><span class="sxs-lookup"><span data-stu-id="cc14d-2862">Six digits in the format DDMMYY which are the date of birth</span></span> 
- <span data-ttu-id="cc14d-2863">Número individual de três dígitos </span><span class="sxs-lookup"><span data-stu-id="cc14d-2863">Three-digit individual number</span></span> 
- <span data-ttu-id="cc14d-2864">Dois dígitos de verificação</span><span class="sxs-lookup"><span data-stu-id="cc14d-2864">Two check digits</span></span>

### <a name="checksum"></a><span data-ttu-id="cc14d-2865">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="cc14d-2865">Checksum</span></span>

<span data-ttu-id="cc14d-2866">Sim</span><span class="sxs-lookup"><span data-stu-id="cc14d-2866">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="cc14d-2867">Definição</span><span class="sxs-lookup"><span data-stu-id="cc14d-2867">Definition</span></span>

<span data-ttu-id="cc14d-2868">Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="cc14d-2868">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="cc14d-2869">A função Func_norway_id_number localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="cc14d-2869">The function Func_norway_id_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="cc14d-2870">Uma palavra-chave de Keyword_norway_id_number for encontrada.</span><span class="sxs-lookup"><span data-stu-id="cc14d-2870">A keyword from Keyword_norway_id_number is found.</span></span>
- <span data-ttu-id="cc14d-2871">A soma de verificação passa.</span><span class="sxs-lookup"><span data-stu-id="cc14d-2871">The checksum passes.</span></span>
- <span data-ttu-id="cc14d-2872">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="cc14d-2872">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="cc14d-2873">A função Func_norway_id_numbe localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="cc14d-2873">The function Func_norway_id_numbe finds content that matches the pattern.</span></span>
- <span data-ttu-id="cc14d-2874">A soma de verificação passa.</span><span class="sxs-lookup"><span data-stu-id="cc14d-2874">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="cc14d-2875">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="cc14d-2875">Keywords</span></span>

#### <a name="keywordnorwayidnumber"></a><span data-ttu-id="cc14d-2876">Keyword_norway_id_number</span><span class="sxs-lookup"><span data-stu-id="cc14d-2876">Keyword_norway_id_number</span></span>

- <span data-ttu-id="cc14d-2877">Número de identificação pessoal</span><span class="sxs-lookup"><span data-stu-id="cc14d-2877">Personal identification number</span></span>
- <span data-ttu-id="cc14d-2878">Número de Identificação Norueguês</span><span class="sxs-lookup"><span data-stu-id="cc14d-2878">Norwegian ID Number</span></span>
- <span data-ttu-id="cc14d-2879">Número de Identificação</span><span class="sxs-lookup"><span data-stu-id="cc14d-2879">ID Number</span></span>
- <span data-ttu-id="cc14d-2880">Identificador</span><span class="sxs-lookup"><span data-stu-id="cc14d-2880">Identification</span></span>
- <span data-ttu-id="cc14d-2881">Personnummer</span><span class="sxs-lookup"><span data-stu-id="cc14d-2881">Personnummer</span></span>
- <span data-ttu-id="cc14d-2882">Fødselsnummer</span><span class="sxs-lookup"><span data-stu-id="cc14d-2882">Fødselsnummer</span></span>

   
## <a name="philippines-unified-multi-purpose-id-number"></a><span data-ttu-id="cc14d-2883">Número de Identificação Multiuso Unificada das Filipinas</span><span class="sxs-lookup"><span data-stu-id="cc14d-2883">Philippines Unified Multi-Purpose ID Number</span></span>

### <a name="format"></a><span data-ttu-id="cc14d-2884">Format</span><span class="sxs-lookup"><span data-stu-id="cc14d-2884">Format</span></span>

<span data-ttu-id="cc14d-2885">12 dígitos separados por hifens</span><span class="sxs-lookup"><span data-stu-id="cc14d-2885">12 digits separated by hyphens</span></span>

### <a name="pattern"></a><span data-ttu-id="cc14d-2886">Padrão</span><span class="sxs-lookup"><span data-stu-id="cc14d-2886">Pattern</span></span>

<span data-ttu-id="cc14d-2887">12 dígitos:</span><span class="sxs-lookup"><span data-stu-id="cc14d-2887">12 digits:</span></span>
- <span data-ttu-id="cc14d-2888">Quatro dígitos</span><span class="sxs-lookup"><span data-stu-id="cc14d-2888">Four digits</span></span> 
- <span data-ttu-id="cc14d-2889">Um hífen</span><span class="sxs-lookup"><span data-stu-id="cc14d-2889">A hyphen</span></span> 
- <span data-ttu-id="cc14d-2890">Sete dígitos </span><span class="sxs-lookup"><span data-stu-id="cc14d-2890">Seven digits</span></span> 
- <span data-ttu-id="cc14d-2891">Um hífen</span><span class="sxs-lookup"><span data-stu-id="cc14d-2891">A hyphen</span></span> 
- <span data-ttu-id="cc14d-2892">Um dígito</span><span class="sxs-lookup"><span data-stu-id="cc14d-2892">One digit</span></span>

### <a name="checksum"></a><span data-ttu-id="cc14d-2893">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="cc14d-2893">Checksum</span></span>

<span data-ttu-id="cc14d-2894">Não</span><span class="sxs-lookup"><span data-stu-id="cc14d-2894">No</span></span>

### <a name="definition"></a><span data-ttu-id="cc14d-2895">Definição</span><span class="sxs-lookup"><span data-stu-id="cc14d-2895">Definition</span></span>

<span data-ttu-id="cc14d-2896">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="cc14d-2896">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="cc14d-2897">A expressão regular Regex_philippines_unified_id localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="cc14d-2897">The regular expression Regex_philippines_unified_id finds content that matches the pattern.</span></span>
- <span data-ttu-id="cc14d-2898">Uma palavra-chave de Keyword_philippines_id for encontrada.</span><span class="sxs-lookup"><span data-stu-id="cc14d-2898">A keyword from Keyword_philippines_id is found.</span></span>

```
<!-- Philippines Unified Multi-Purpose ID number -->
<Entity id="019b39dd-8c25-4765-91a3-d9c6baf3c3b3" recommendedConfidence="75" patternsProximity="300">
  <Pattern confidenceLevel="75">
     <IdMatch idRef="Regex_philippines_unified_id"/>
     <Match idRef="Keyword_philippines_id"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="cc14d-2899">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="cc14d-2899">Keywords</span></span>
   
#### <a name="keywordphilippinesid"></a><span data-ttu-id="cc14d-2900">Keyword_philippines_id</span><span class="sxs-lookup"><span data-stu-id="cc14d-2900">Keyword_philippines_id</span></span>

- <span data-ttu-id="cc14d-2901">Identificação Multiuso Unificada</span><span class="sxs-lookup"><span data-stu-id="cc14d-2901">Unified Multi-Purpose ID</span></span> 
- <span data-ttu-id="cc14d-2902">UMID</span><span class="sxs-lookup"><span data-stu-id="cc14d-2902">UMID</span></span> 
- <span data-ttu-id="cc14d-2903">Cartão de Identidade</span><span class="sxs-lookup"><span data-stu-id="cc14d-2903">Identity Card</span></span> 
- <span data-ttu-id="cc14d-2904">Pinag-isang Multi-Layunin ID</span><span class="sxs-lookup"><span data-stu-id="cc14d-2904">Pinag-isang Multi-Layunin ID</span></span>
   
## <a name="poland-identity-card"></a><span data-ttu-id="cc14d-2905">Cartão de Identificação da Polônia</span><span class="sxs-lookup"><span data-stu-id="cc14d-2905">Poland Identity Card</span></span>

### <a name="format"></a><span data-ttu-id="cc14d-2906">Format</span><span class="sxs-lookup"><span data-stu-id="cc14d-2906">Format</span></span>

<span data-ttu-id="cc14d-2907">Três letras e seis dígitos</span><span class="sxs-lookup"><span data-stu-id="cc14d-2907">Three letters and six digits</span></span>

### <a name="pattern"></a><span data-ttu-id="cc14d-2908">Padrão</span><span class="sxs-lookup"><span data-stu-id="cc14d-2908">Pattern</span></span>

<span data-ttu-id="cc14d-2909">Três letras (não diferenciam maiúsculas de minúsculas) seguidas de seis dígitos</span><span class="sxs-lookup"><span data-stu-id="cc14d-2909">Three letters (not case sensitive) followed by six digits</span></span>

### <a name="checksum"></a><span data-ttu-id="cc14d-2910">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="cc14d-2910">Checksum</span></span>

<span data-ttu-id="cc14d-2911">Sim</span><span class="sxs-lookup"><span data-stu-id="cc14d-2911">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="cc14d-2912">Definição</span><span class="sxs-lookup"><span data-stu-id="cc14d-2912">Definition</span></span>

<span data-ttu-id="cc14d-2913">Uma política de DLP é de 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres: a função Func_polish_national_id localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="cc14d-2913">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters: The function Func_polish_national_id finds content that matches the pattern.</span></span>
<span data-ttu-id="cc14d-2914">Uma palavra-chave de Keyword_polish_national_id_passport_number for encontrada.</span><span class="sxs-lookup"><span data-stu-id="cc14d-2914">A keyword from Keyword_polish_national_id_passport_number is found.</span></span>
<span data-ttu-id="cc14d-2915">A soma de verificação passa.</span><span class="sxs-lookup"><span data-stu-id="cc14d-2915">The checksum passes.</span></span>

```
<!-- Poland Identity Card-->
<Entity id="25E64989-ED5D-40CA-A939-6C14183BB7BF" patternsProximity="300" recommendedConfidence="85">
      <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_polish_national_id" />
          <Match idRef="Keyword_polish_national_id_passport_number" />
      </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="cc14d-2916">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="cc14d-2916">Keywords</span></span>

#### <a name="keywordpolishnationalidpassportnumber"></a><span data-ttu-id="cc14d-2917">Keyword_polish_national_id_passport_number</span><span class="sxs-lookup"><span data-stu-id="cc14d-2917">Keyword_polish_national_id_passport_number</span></span>

- <span data-ttu-id="cc14d-2918">Dowód osobisty</span><span class="sxs-lookup"><span data-stu-id="cc14d-2918">Dowód osobisty</span></span>
- <span data-ttu-id="cc14d-2919">Numer dowodu osobistego</span><span class="sxs-lookup"><span data-stu-id="cc14d-2919">Numer dowodu osobistego</span></span>
- <span data-ttu-id="cc14d-2920">Nazwa i numer dowodu osobistego</span><span class="sxs-lookup"><span data-stu-id="cc14d-2920">Nazwa i numer dowodu osobistego</span></span>
- <span data-ttu-id="cc14d-2921">Nazwa i NR dowodu osobistego</span><span class="sxs-lookup"><span data-stu-id="cc14d-2921">Nazwa i nr dowodu osobistego</span></span>
- <span data-ttu-id="cc14d-2922">Nazwa i nr dowodu tożsamości</span><span class="sxs-lookup"><span data-stu-id="cc14d-2922">Nazwa i nr dowodu tożsamości</span></span>
- <span data-ttu-id="cc14d-2923">Dowód Tożsamości</span><span class="sxs-lookup"><span data-stu-id="cc14d-2923">Dowód Tożsamości</span></span>
- <span data-ttu-id="cc14d-2924">Dow.</span><span class="sxs-lookup"><span data-stu-id="cc14d-2924">dow.</span></span> <span data-ttu-id="cc14d-2925">Opera.</span><span class="sxs-lookup"><span data-stu-id="cc14d-2925">os.</span></span>

   
## <a name="poland-national-id-pesel"></a><span data-ttu-id="cc14d-2926">ID nacional da Polônia (PESEL)</span><span class="sxs-lookup"><span data-stu-id="cc14d-2926">Poland National ID (PESEL)</span></span>

### <a name="format"></a><span data-ttu-id="cc14d-2927">Format</span><span class="sxs-lookup"><span data-stu-id="cc14d-2927">Format</span></span>

<span data-ttu-id="cc14d-2928">11 dígitos</span><span class="sxs-lookup"><span data-stu-id="cc14d-2928">11 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="cc14d-2929">Padrão</span><span class="sxs-lookup"><span data-stu-id="cc14d-2929">Pattern</span></span>

<span data-ttu-id="cc14d-2930">11 dígitos consecutivos</span><span class="sxs-lookup"><span data-stu-id="cc14d-2930">11 consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="cc14d-2931">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="cc14d-2931">Checksum</span></span>

<span data-ttu-id="cc14d-2932">Sim</span><span class="sxs-lookup"><span data-stu-id="cc14d-2932">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="cc14d-2933">Definição</span><span class="sxs-lookup"><span data-stu-id="cc14d-2933">Definition</span></span>

<span data-ttu-id="cc14d-2934">Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="cc14d-2934">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="cc14d-2935">A função Func_pesel_identification_number localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="cc14d-2935">The function Func_pesel_identification_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="cc14d-2936">Uma palavra-chave de Keyword_pesel_identification_number for encontrada.</span><span class="sxs-lookup"><span data-stu-id="cc14d-2936">A keyword from Keyword_pesel_identification_number is found.</span></span>
- <span data-ttu-id="cc14d-2937">A soma de verificação passa.</span><span class="sxs-lookup"><span data-stu-id="cc14d-2937">The checksum passes.</span></span>

```
<!-- Poland National ID (PESEL) -->      
<Entity id="E3AAF206-4297-412F-9E06-BA8487E22456" patternsProximity="300" recommendedConfidence="85">
      <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_pesel_identification_number" />
          <Match idRef="Keyword_pesel_identification_number" />
      </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="cc14d-2938">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="cc14d-2938">Keywords</span></span>

#### <a name="keywordpeselidentificationnumber"></a><span data-ttu-id="cc14d-2939">Keyword_pesel_identification_number</span><span class="sxs-lookup"><span data-stu-id="cc14d-2939">Keyword_pesel_identification_number</span></span>

- <span data-ttu-id="cc14d-2940">Nr PESEL</span><span class="sxs-lookup"><span data-stu-id="cc14d-2940">Nr PESEL</span></span>
- <span data-ttu-id="cc14d-2941">PESEL</span><span class="sxs-lookup"><span data-stu-id="cc14d-2941">PESEL</span></span>   

   
## <a name="poland-passport"></a><span data-ttu-id="cc14d-2942">Passaporte da Polônia</span><span class="sxs-lookup"><span data-stu-id="cc14d-2942">Poland Passport</span></span>

### <a name="format"></a><span data-ttu-id="cc14d-2943">Format</span><span class="sxs-lookup"><span data-stu-id="cc14d-2943">Format</span></span>

<span data-ttu-id="cc14d-2944">Duas letras e sete dígitos</span><span class="sxs-lookup"><span data-stu-id="cc14d-2944">Two letters and seven digits</span></span>

### <a name="pattern"></a><span data-ttu-id="cc14d-2945">Padrão</span><span class="sxs-lookup"><span data-stu-id="cc14d-2945">Pattern</span></span>

<span data-ttu-id="cc14d-2946">Duas letras (não diferencia maiúsculas de minúsculas) seguidas de sete dígitos</span><span class="sxs-lookup"><span data-stu-id="cc14d-2946">Two letters (not case sensitive) followed by seven digits</span></span>

### <a name="checksum"></a><span data-ttu-id="cc14d-2947">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="cc14d-2947">Checksum</span></span>

<span data-ttu-id="cc14d-2948">Sim</span><span class="sxs-lookup"><span data-stu-id="cc14d-2948">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="cc14d-2949">Definição</span><span class="sxs-lookup"><span data-stu-id="cc14d-2949">Definition</span></span>

<span data-ttu-id="cc14d-2950">Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="cc14d-2950">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="cc14d-2951">A função Func_polish_passport_number localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="cc14d-2951">The function Func_polish_passport_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="cc14d-2952">Uma palavra-chave de Keyword_polish_national_id_passport_number for encontrada.</span><span class="sxs-lookup"><span data-stu-id="cc14d-2952">A keyword from Keyword_polish_national_id_passport_number is found.</span></span>
- <span data-ttu-id="cc14d-2953">A soma de verificação passa.</span><span class="sxs-lookup"><span data-stu-id="cc14d-2953">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="cc14d-2954">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="cc14d-2954">Keywords</span></span>

#### <a name="keywordpolishnationalidpassportnumber"></a><span data-ttu-id="cc14d-2955">Keyword_polish_national_id_passport_number</span><span class="sxs-lookup"><span data-stu-id="cc14d-2955">Keyword_polish_national_id_passport_number</span></span>

- <span data-ttu-id="cc14d-2956">Numer paszportu</span><span class="sxs-lookup"><span data-stu-id="cc14d-2956">Numer paszportu</span></span>
- <span data-ttu-id="cc14d-2957">Nr.</span><span class="sxs-lookup"><span data-stu-id="cc14d-2957">Nr.</span></span> <span data-ttu-id="cc14d-2958">Paszportu</span><span class="sxs-lookup"><span data-stu-id="cc14d-2958">Paszportu</span></span>
- <span data-ttu-id="cc14d-2959">Paszport</span><span class="sxs-lookup"><span data-stu-id="cc14d-2959">Paszport</span></span>

   
## <a name="portugal-citizen-card-number"></a><span data-ttu-id="cc14d-2960">Número do Cartão de Cidadão de Portugal</span><span class="sxs-lookup"><span data-stu-id="cc14d-2960">Portugal Citizen Card Number</span></span>

### <a name="format"></a><span data-ttu-id="cc14d-2961">Format</span><span class="sxs-lookup"><span data-stu-id="cc14d-2961">Format</span></span>

<span data-ttu-id="cc14d-2962">Oito dígitos</span><span class="sxs-lookup"><span data-stu-id="cc14d-2962">Eight digits</span></span>

### <a name="pattern"></a><span data-ttu-id="cc14d-2963">Padrão</span><span class="sxs-lookup"><span data-stu-id="cc14d-2963">Pattern</span></span>

<span data-ttu-id="cc14d-2964">Oito dígitos</span><span class="sxs-lookup"><span data-stu-id="cc14d-2964">Eight digits</span></span>

### <a name="checksum"></a><span data-ttu-id="cc14d-2965">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="cc14d-2965">Checksum</span></span>

<span data-ttu-id="cc14d-2966">Não</span><span class="sxs-lookup"><span data-stu-id="cc14d-2966">No</span></span>

### <a name="definition"></a><span data-ttu-id="cc14d-2967">Definição</span><span class="sxs-lookup"><span data-stu-id="cc14d-2967">Definition</span></span>

<span data-ttu-id="cc14d-2968">Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="cc14d-2968">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="cc14d-2969">A expressão regular Regex_portugal_citizen_card localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="cc14d-2969">The regular expression Regex_portugal_citizen_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="cc14d-2970">Uma palavra-chave de Keyword_portugal_citizen_card for encontrada.</span><span class="sxs-lookup"><span data-stu-id="cc14d-2970">A keyword from Keyword_portugal_citizen_card is found.</span></span>

```
<!-- Portugal Citizen Card Number -->
<Entity id="91a7ece2-add4-4986-9a15-c84544d81ecd" recommendedConfidence="85" patternsProximity="300">
  <Pattern confidenceLevel="85">
     <IdMatch idRef="Regex_portugal_citizen_card"/>
     <Match idRef="Keyword_portugal_citizen_card"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="cc14d-2971">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="cc14d-2971">Keywords</span></span>

#### <a name="keywordportugalcitizencard"></a><span data-ttu-id="cc14d-2972">Keyword_portugal_citizen_card</span><span class="sxs-lookup"><span data-stu-id="cc14d-2972">Keyword_portugal_citizen_card</span></span>

- <span data-ttu-id="cc14d-2973">Cartão de Cidadão</span><span class="sxs-lookup"><span data-stu-id="cc14d-2973">Citizen Card</span></span>
- <span data-ttu-id="cc14d-2974">Cartão de Identidade Nacional</span><span class="sxs-lookup"><span data-stu-id="cc14d-2974">National ID Card</span></span>
- <span data-ttu-id="cc14d-2975">CC</span><span class="sxs-lookup"><span data-stu-id="cc14d-2975">CC</span></span>
- <span data-ttu-id="cc14d-2976">Cartão de Cidadão</span><span class="sxs-lookup"><span data-stu-id="cc14d-2976">Cartão de Cidadão</span></span>
- <span data-ttu-id="cc14d-2977">Bilhete de Identidade</span><span class="sxs-lookup"><span data-stu-id="cc14d-2977">Bilhete de Identidade</span></span>
   
## <a name="saudi-arabia-national-id"></a><span data-ttu-id="cc14d-2978">ID nacional da Arábia Saudita</span><span class="sxs-lookup"><span data-stu-id="cc14d-2978">Saudi Arabia National ID</span></span>

### <a name="format"></a><span data-ttu-id="cc14d-2979">Format</span><span class="sxs-lookup"><span data-stu-id="cc14d-2979">Format</span></span>

<span data-ttu-id="cc14d-2980">10 dígitos</span><span class="sxs-lookup"><span data-stu-id="cc14d-2980">10 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="cc14d-2981">Padrão</span><span class="sxs-lookup"><span data-stu-id="cc14d-2981">Pattern</span></span>

<span data-ttu-id="cc14d-2982">10 dígitos consecutivos</span><span class="sxs-lookup"><span data-stu-id="cc14d-2982">10 consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="cc14d-2983">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="cc14d-2983">Checksum</span></span>

<span data-ttu-id="cc14d-2984">Não</span><span class="sxs-lookup"><span data-stu-id="cc14d-2984">No</span></span>

### <a name="definition"></a><span data-ttu-id="cc14d-2985">Definição</span><span class="sxs-lookup"><span data-stu-id="cc14d-2985">Definition</span></span>

<span data-ttu-id="cc14d-2986">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="cc14d-2986">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="cc14d-2987">A expressão regular Regex_saudi_arabia_national_id localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="cc14d-2987">The regular expression Regex_saudi_arabia_national_id finds content that matches the pattern.</span></span>
- <span data-ttu-id="cc14d-2988">Uma palavra-chave de Keyword_saudi_arabia_national_id for encontrada.</span><span class="sxs-lookup"><span data-stu-id="cc14d-2988">A keyword from Keyword_saudi_arabia_national_id is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="cc14d-2989">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="cc14d-2989">Keywords</span></span>

#### <a name="keywordsaudiarabianationalid"></a><span data-ttu-id="cc14d-2990">Keyword_saudi_arabia_national_id</span><span class="sxs-lookup"><span data-stu-id="cc14d-2990">Keyword_saudi_arabia_national_id</span></span>

- <span data-ttu-id="cc14d-2991">Identification Card</span><span class="sxs-lookup"><span data-stu-id="cc14d-2991">Identification Card</span></span> 
- <span data-ttu-id="cc14d-2992">I card number</span><span class="sxs-lookup"><span data-stu-id="cc14d-2992">I card number</span></span> 
- <span data-ttu-id="cc14d-2993">ID number</span><span class="sxs-lookup"><span data-stu-id="cc14d-2993">ID number</span></span> 
- <span data-ttu-id="cc14d-2994">الوطنية الهوية بطاقة رقم</span><span class="sxs-lookup"><span data-stu-id="cc14d-2994">الوطنية الهوية بطاقة رقم</span></span> 

   
## <a name="singapore-national-registration-identity-card-nric-number"></a><span data-ttu-id="cc14d-2995">Número do Cartão de Identidade do Registro Nacional (NRIC) de Cingapura</span><span class="sxs-lookup"><span data-stu-id="cc14d-2995">Singapore National Registration Identity Card (NRIC) Number</span></span>

### <a name="format"></a><span data-ttu-id="cc14d-2996">Format</span><span class="sxs-lookup"><span data-stu-id="cc14d-2996">Format</span></span>

<span data-ttu-id="cc14d-2997">Nove letras e dígitos</span><span class="sxs-lookup"><span data-stu-id="cc14d-2997">Nine letters and digits</span></span>

### <a name="pattern"></a><span data-ttu-id="cc14d-2998">Padrão</span><span class="sxs-lookup"><span data-stu-id="cc14d-2998">Pattern</span></span>

- <span data-ttu-id="cc14d-2999">Nove letras e dígitos:</span><span class="sxs-lookup"><span data-stu-id="cc14d-2999">Nine letters and digits:</span></span>
- <span data-ttu-id="cc14d-3000">A letra "F", "G", "S" ou "T" (não diferenciam maiúsculas de minúsculas) </span><span class="sxs-lookup"><span data-stu-id="cc14d-3000">The letter "F", "G", "S", or "T" (not case sensitive)</span></span> 
- <span data-ttu-id="cc14d-3001">Sete dígitos </span><span class="sxs-lookup"><span data-stu-id="cc14d-3001">Seven digits</span></span> 
- <span data-ttu-id="cc14d-3002">Um dígito de verificação alfabético</span><span class="sxs-lookup"><span data-stu-id="cc14d-3002">An alphabetic check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="cc14d-3003">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="cc14d-3003">Checksum</span></span>

<span data-ttu-id="cc14d-3004">Sim</span><span class="sxs-lookup"><span data-stu-id="cc14d-3004">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="cc14d-3005">Definição</span><span class="sxs-lookup"><span data-stu-id="cc14d-3005">Definition</span></span>

<span data-ttu-id="cc14d-3006">Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="cc14d-3006">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="cc14d-3007">A expressão regular Regex_singapore_nric localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="cc14d-3007">The regular expression Regex_singapore_nric finds content that matches the pattern.</span></span>
- <span data-ttu-id="cc14d-3008">Uma palavra-chave de Keyword_singapore_nric for encontrada.</span><span class="sxs-lookup"><span data-stu-id="cc14d-3008">A keyword from Keyword_singapore_nric is found.</span></span>
- <span data-ttu-id="cc14d-3009">A soma de verificação passa.</span><span class="sxs-lookup"><span data-stu-id="cc14d-3009">The checksum passes.</span></span>

<span data-ttu-id="cc14d-3010">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="cc14d-3010">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="cc14d-3011">A expressão regular Regex_singapore_nric localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="cc14d-3011">The regular expression Regex_singapore_nric finds content that matches the pattern.</span></span>
- <span data-ttu-id="cc14d-3012">A soma de verificação passa.</span><span class="sxs-lookup"><span data-stu-id="cc14d-3012">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="cc14d-3013">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="cc14d-3013">Keywords</span></span>
   
#### <a name="keywordsingaporenric"></a><span data-ttu-id="cc14d-3014">Keyword_singapore_nric</span><span class="sxs-lookup"><span data-stu-id="cc14d-3014">Keyword_singapore_nric</span></span>

- <span data-ttu-id="cc14d-3015">Número do Cartão de Identidade do Registro Nacional</span><span class="sxs-lookup"><span data-stu-id="cc14d-3015">National Registration Identity Card</span></span> 
- <span data-ttu-id="cc14d-3016">Número do Cartão de Identidade</span><span class="sxs-lookup"><span data-stu-id="cc14d-3016">Identity Card Number</span></span> 
- <span data-ttu-id="cc14d-3017">NRIC</span><span class="sxs-lookup"><span data-stu-id="cc14d-3017">NRIC</span></span> 
- <span data-ttu-id="cc14d-3018">Liga</span><span class="sxs-lookup"><span data-stu-id="cc14d-3018">IC</span></span> 
- <span data-ttu-id="cc14d-3019">Número de Identificação Estrangeira</span><span class="sxs-lookup"><span data-stu-id="cc14d-3019">Foreign Identification Number</span></span> 
- <span data-ttu-id="cc14d-3020">ALETA</span><span class="sxs-lookup"><span data-stu-id="cc14d-3020">FIN</span></span> 
- <span data-ttu-id="cc14d-3021">身份证</span><span class="sxs-lookup"><span data-stu-id="cc14d-3021">身份证</span></span> 
- <span data-ttu-id="cc14d-3022">身份證</span><span class="sxs-lookup"><span data-stu-id="cc14d-3022">身份證</span></span> 
   
## <a name="south-africa-identification-number"></a><span data-ttu-id="cc14d-3023">Número de Identificação da África do Sul</span><span class="sxs-lookup"><span data-stu-id="cc14d-3023">South Africa Identification Number</span></span>

### <a name="format"></a><span data-ttu-id="cc14d-3024">Format</span><span class="sxs-lookup"><span data-stu-id="cc14d-3024">Format</span></span>

<span data-ttu-id="cc14d-3025">13 dígitos que podem conter espaços</span><span class="sxs-lookup"><span data-stu-id="cc14d-3025">13 digits that may contain spaces</span></span>

### <a name="pattern"></a><span data-ttu-id="cc14d-3026">Padrão</span><span class="sxs-lookup"><span data-stu-id="cc14d-3026">Pattern</span></span>

<span data-ttu-id="cc14d-3027">13 dígitos:</span><span class="sxs-lookup"><span data-stu-id="cc14d-3027">13 digits:</span></span>
- <span data-ttu-id="cc14d-3028">Seis dígitos no formato AAMMDD que são a data de nascimento</span><span class="sxs-lookup"><span data-stu-id="cc14d-3028">Six digits in the format YYMMDD which are the date of birth</span></span> 
- <span data-ttu-id="cc14d-3029">Quatro dígitos</span><span class="sxs-lookup"><span data-stu-id="cc14d-3029">Four digits</span></span> 
- <span data-ttu-id="cc14d-3030">Indicador de cidadania de um dígito </span><span class="sxs-lookup"><span data-stu-id="cc14d-3030">A single-digit citizenship indicator</span></span> 
- <span data-ttu-id="cc14d-3031">O dígito "8" ou "9" </span><span class="sxs-lookup"><span data-stu-id="cc14d-3031">The digit "8" or "9"</span></span> 
- <span data-ttu-id="cc14d-3032">Um dígito que é um dígito de soma de verificação</span><span class="sxs-lookup"><span data-stu-id="cc14d-3032">One digit which is a checksum digit</span></span>

### <a name="checksum"></a><span data-ttu-id="cc14d-3033">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="cc14d-3033">Checksum</span></span>

<span data-ttu-id="cc14d-3034">Sim</span><span class="sxs-lookup"><span data-stu-id="cc14d-3034">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="cc14d-3035">Definição</span><span class="sxs-lookup"><span data-stu-id="cc14d-3035">Definition</span></span>

<span data-ttu-id="cc14d-3036">Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="cc14d-3036">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="cc14d-3037">A função Func_south_africa_identification_number localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="cc14d-3037">The function Func_south_africa_identification_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="cc14d-3038">Uma palavra-chave de Keyword_south_africa_identification_number for encontrada.</span><span class="sxs-lookup"><span data-stu-id="cc14d-3038">A keyword from Keyword_south_africa_identification_number is found.</span></span>
- <span data-ttu-id="cc14d-3039">A soma de verificação passa.</span><span class="sxs-lookup"><span data-stu-id="cc14d-3039">The checksum passes.</span></span>

```
<!-- South Africa Identification Number -->
<Entity id="e2adf7cb-8ea6-4048-a2ed-d89eb65f2780" recommendedConfidence="85" patternsProximity="300">
  <Pattern confidenceLevel="85">
     <IdMatch idRef="Func_south_africa_identification_number"/>
     <Match idRef="Keyword_south_africa_identification_number"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="cc14d-3040">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="cc14d-3040">Keywords</span></span>
   
#### <a name="keywordsouthafricaidentificationnumber"></a><span data-ttu-id="cc14d-3041">Keyword_south_africa_identification_number</span><span class="sxs-lookup"><span data-stu-id="cc14d-3041">Keyword_south_africa_identification_number</span></span>

- <span data-ttu-id="cc14d-3042">Cartão de identidade</span><span class="sxs-lookup"><span data-stu-id="cc14d-3042">Identity card</span></span>
- <span data-ttu-id="cc14d-3043">ID</span><span class="sxs-lookup"><span data-stu-id="cc14d-3043">ID</span></span>
- <span data-ttu-id="cc14d-3044">Identificador</span><span class="sxs-lookup"><span data-stu-id="cc14d-3044">Identification</span></span> 
   
## <a name="south-korea-resident-registration-number"></a><span data-ttu-id="cc14d-3045">Número do Registro de Residentes da Coreia do Sul</span><span class="sxs-lookup"><span data-stu-id="cc14d-3045">South Korea Resident Registration Number</span></span>

### <a name="format"></a><span data-ttu-id="cc14d-3046">Format</span><span class="sxs-lookup"><span data-stu-id="cc14d-3046">Format</span></span>

<span data-ttu-id="cc14d-3047">13 dígitos que contém um hifen</span><span class="sxs-lookup"><span data-stu-id="cc14d-3047">13 digits containing a hyphen</span></span>

### <a name="pattern"></a><span data-ttu-id="cc14d-3048">Padrão</span><span class="sxs-lookup"><span data-stu-id="cc14d-3048">Pattern</span></span>

<span data-ttu-id="cc14d-3049">13 dígitos:</span><span class="sxs-lookup"><span data-stu-id="cc14d-3049">13 digits:</span></span>
- <span data-ttu-id="cc14d-3050">Seis dígitos no formato AAMMDD que são a data de nascimento</span><span class="sxs-lookup"><span data-stu-id="cc14d-3050">Six digits in the format YYMMDD which are the date of birth</span></span> 
- <span data-ttu-id="cc14d-3051">Um hífen</span><span class="sxs-lookup"><span data-stu-id="cc14d-3051">A hyphen</span></span> 
- <span data-ttu-id="cc14d-3052">Um dígito determinado pelo século e pelo sexo </span><span class="sxs-lookup"><span data-stu-id="cc14d-3052">One digit determined by the century and gender</span></span> 
- <span data-ttu-id="cc14d-3053">Código da região de nascimento de quatro dígitos </span><span class="sxs-lookup"><span data-stu-id="cc14d-3053">Four-digit region-of-birth code</span></span> 
- <span data-ttu-id="cc14d-3054">Um dígito usado para diferenciar as pessoas para as quais os números anteriores são idênticos </span><span class="sxs-lookup"><span data-stu-id="cc14d-3054">One digit used to differentiate people for whom the preceding numbers are identical</span></span> 
- <span data-ttu-id="cc14d-3055">Um dígito de verificação.</span><span class="sxs-lookup"><span data-stu-id="cc14d-3055">A check digit.</span></span>

### <a name="checksum"></a><span data-ttu-id="cc14d-3056">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="cc14d-3056">Checksum</span></span>

<span data-ttu-id="cc14d-3057">Sim</span><span class="sxs-lookup"><span data-stu-id="cc14d-3057">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="cc14d-3058">Definição</span><span class="sxs-lookup"><span data-stu-id="cc14d-3058">Definition</span></span>

<span data-ttu-id="cc14d-3059">Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="cc14d-3059">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="cc14d-3060">A função Func_south_korea_resident_number localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="cc14d-3060">The function Func_south_korea_resident_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="cc14d-3061">Uma palavra-chave de Keyword_south_korea_resident_number for encontrada.</span><span class="sxs-lookup"><span data-stu-id="cc14d-3061">A keyword from Keyword_south_korea_resident_number is found.</span></span>
- <span data-ttu-id="cc14d-3062">A soma de verificação passa.</span><span class="sxs-lookup"><span data-stu-id="cc14d-3062">The checksum passes.</span></span>

<span data-ttu-id="cc14d-3063">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="cc14d-3063">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="cc14d-3064">A função Func_south_korea_resident_number localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="cc14d-3064">The function Func_south_korea_resident_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="cc14d-3065">A soma de verificação passa.</span><span class="sxs-lookup"><span data-stu-id="cc14d-3065">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="cc14d-3066">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="cc14d-3066">Keywords</span></span>
   
#### <a name="keywordsouthkorearesidentnumber"></a><span data-ttu-id="cc14d-3067">Keyword_south_korea_resident_number</span><span class="sxs-lookup"><span data-stu-id="cc14d-3067">Keyword_south_korea_resident_number</span></span>

- <span data-ttu-id="cc14d-3068">Cartão de identidade nacional</span><span class="sxs-lookup"><span data-stu-id="cc14d-3068">National ID card</span></span> 
- <span data-ttu-id="cc14d-3069">Número de Registro do Cidadão</span><span class="sxs-lookup"><span data-stu-id="cc14d-3069">Citizen's Registration Number</span></span> 
- <span data-ttu-id="cc14d-3070">Jumin deungnok beonho</span><span class="sxs-lookup"><span data-stu-id="cc14d-3070">Jumin deungnok beonho</span></span> 
- <span data-ttu-id="cc14d-3071">RRN</span><span class="sxs-lookup"><span data-stu-id="cc14d-3071">RRN</span></span> 
- <span data-ttu-id="cc14d-3072">주민등록번호</span><span class="sxs-lookup"><span data-stu-id="cc14d-3072">주민등록번호</span></span>
   
## <a name="spain-social-security-number-ssn"></a><span data-ttu-id="cc14d-3073">Número de seguridade social da Espanha (SSN)</span><span class="sxs-lookup"><span data-stu-id="cc14d-3073">Spain Social Security Number (SSN)</span></span>

### <a name="format"></a><span data-ttu-id="cc14d-3074">Format</span><span class="sxs-lookup"><span data-stu-id="cc14d-3074">Format</span></span>

<span data-ttu-id="cc14d-3075">11 a 12 dígitos</span><span class="sxs-lookup"><span data-stu-id="cc14d-3075">11-12 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="cc14d-3076">Padrão</span><span class="sxs-lookup"><span data-stu-id="cc14d-3076">Pattern</span></span>

<span data-ttu-id="cc14d-3077">11-12 dígitos:</span><span class="sxs-lookup"><span data-stu-id="cc14d-3077">11-12 digits:</span></span>
- <span data-ttu-id="cc14d-3078">Dois dígitos</span><span class="sxs-lookup"><span data-stu-id="cc14d-3078">Two digits</span></span> 
- <span data-ttu-id="cc14d-3079">Uma barra (opcional)</span><span class="sxs-lookup"><span data-stu-id="cc14d-3079">A forward slash (optional)</span></span> 
- <span data-ttu-id="cc14d-3080">7 a 8 dígitos</span><span class="sxs-lookup"><span data-stu-id="cc14d-3080">7-8 digits</span></span> 
- <span data-ttu-id="cc14d-3081">Uma barra (opcional)</span><span class="sxs-lookup"><span data-stu-id="cc14d-3081">A forward slash (optional)</span></span> 
- <span data-ttu-id="cc14d-3082">Dois dígitos</span><span class="sxs-lookup"><span data-stu-id="cc14d-3082">Two digits</span></span>

### <a name="checksum"></a><span data-ttu-id="cc14d-3083">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="cc14d-3083">Checksum</span></span>

<span data-ttu-id="cc14d-3084">Sim</span><span class="sxs-lookup"><span data-stu-id="cc14d-3084">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="cc14d-3085">Definição</span><span class="sxs-lookup"><span data-stu-id="cc14d-3085">Definition</span></span>

<span data-ttu-id="cc14d-3086">Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="cc14d-3086">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="cc14d-3087">A função Func_spanish_social_security_number localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="cc14d-3087">The function Func_spanish_social_security_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="cc14d-3088">A soma de verificação passa.</span><span class="sxs-lookup"><span data-stu-id="cc14d-3088">The checksum passes.</span></span>

```
<!-- Spain SSN -->
<Entity id="5df987c0-8eae-4bce-ace7-b316347f3070" patternsProximity="300" recommendedConfidence="85">
    <Pattern confidenceLevel="85">
        <IdMatch idRef="Func_spanish_social_security_number" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="cc14d-3089">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="cc14d-3089">Keywords</span></span>

<span data-ttu-id="cc14d-3090">Nenhum</span><span class="sxs-lookup"><span data-stu-id="cc14d-3090">None</span></span>

## <a name="sql-server-connection-string"></a><span data-ttu-id="cc14d-3091">Cadeia de caracteres de conexão do SQL Server</span><span class="sxs-lookup"><span data-stu-id="cc14d-3091">SQL Server Connection String</span></span>

### <a name="format"></a><span data-ttu-id="cc14d-3092">Format</span><span class="sxs-lookup"><span data-stu-id="cc14d-3092">Format</span></span>

<span data-ttu-id="cc14d-3093">A cadeia de caracteres "User ID", "User ID", "UID" ou "UserId" seguida dos caracteres e cadeias de caracteres descritos no padrão abaixo.</span><span class="sxs-lookup"><span data-stu-id="cc14d-3093">The string "User Id", "User ID", "uid", or "UserId" followed by the characters and strings outlined in the pattern below.</span></span>

### <a name="pattern"></a><span data-ttu-id="cc14d-3094">Padrão</span><span class="sxs-lookup"><span data-stu-id="cc14d-3094">Pattern</span></span>

- <span data-ttu-id="cc14d-3095">A cadeia de caracteres "User ID", "User ID", "UID" ou "UserId"</span><span class="sxs-lookup"><span data-stu-id="cc14d-3095">The string "User Id", "User ID", "uid", or "UserId"</span></span>
- <span data-ttu-id="cc14d-3096">Qualquer combinação entre 1-200 letras minúsculas ou maiúsculas, dígitos, símbolos, caracteres especiais ou espaços</span><span class="sxs-lookup"><span data-stu-id="cc14d-3096">Any combination of between 1-200 lower- or uppercase letters, digits, symbols, special characters, or spaces</span></span>
- <span data-ttu-id="cc14d-3097">A cadeia de caracteres "password" ou "pwd", onde "pwd" não é precedida por uma letra minúscula</span><span class="sxs-lookup"><span data-stu-id="cc14d-3097">The string "Password" or "pwd" where "pwd" is not preceded by a lowercase letter</span></span>
- <span data-ttu-id="cc14d-3098">Um sinal de igual (=)</span><span class="sxs-lookup"><span data-stu-id="cc14d-3098">An equal sign (=)</span></span>
- <span data-ttu-id="cc14d-3099">Qualquer caractere que não seja um cifrão ($), símbolo de porcentagem (%), maior que símbolo (>), em símbolo (@), aspas ("), ponto e vírgula (;), chave esquerda ([) ou colchete esquerdo ({)</span><span class="sxs-lookup"><span data-stu-id="cc14d-3099">Any character that is not a dollar sign ($), percent symbol (%), greater than symbol (>), at symbol (@), quotation mark ("), semicolon (;), left brace ([), or left bracket ({)</span></span>
- <span data-ttu-id="cc14d-3100">Qualquer combinação de 7-128 caracteres que não seja um ponto-e-vírgula (;), barra (/) ou aspas (")</span><span class="sxs-lookup"><span data-stu-id="cc14d-3100">Any combination of 7-128 characters that are not a semicolon (;), forward slash (/), or quotation mark (")</span></span>
- <span data-ttu-id="cc14d-3101">Um ponto e vírgula (;) ou aspas (")</span><span class="sxs-lookup"><span data-stu-id="cc14d-3101">A semicolon (;) or quotation mark (")</span></span>

### <a name="checksum"></a><span data-ttu-id="cc14d-3102">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="cc14d-3102">Checksum</span></span>

<span data-ttu-id="cc14d-3103">Não</span><span class="sxs-lookup"><span data-stu-id="cc14d-3103">No</span></span>

### <a name="definition"></a><span data-ttu-id="cc14d-3104">Definição</span><span class="sxs-lookup"><span data-stu-id="cc14d-3104">Definition</span></span>

<span data-ttu-id="cc14d-3105">Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="cc14d-3105">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="cc14d-3106">A expressão regular CEP_Regex_SQLServerConnectionString localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="cc14d-3106">The regular expression CEP_Regex_SQLServerConnectionString finds content that matches the pattern.</span></span>
- <span data-ttu-id="cc14d-3107">Uma palavra-chave de CEP_GlobalFilter **não** é encontrada.</span><span class="sxs-lookup"><span data-stu-id="cc14d-3107">A keyword from CEP_GlobalFilter is **not** found.</span></span>
- <span data-ttu-id="cc14d-3108">A expressão regular CEP_PasswordPlaceHolder não \*\*\*\* localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="cc14d-3108">The regular expression CEP_PasswordPlaceHolder does **not** find content that matches the pattern.</span></span>
- <span data-ttu-id="cc14d-3109">A expressão regular CEP_CommonExampleKeywords não \*\*\*\* localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="cc14d-3109">The regular expression CEP_CommonExampleKeywords does **not** find content that matches the pattern.</span></span>

```
<!---SQL Server Connection String>
<Entity id="e76b6205-d3cb-46f2-bd63-c90153f2f97d" patternsProximity="300" recommendedConfidence="85">
  <Pattern confidenceLevel="85">
        <IdMatch idRef="CEP_Regex_SQLServerConnectionString" />
        <Any minMatches="0" maxMatches="0">
            <Match idRef="CEP_GlobalFilter" />
            <Match idRef="CEP_PasswordPlaceHolder" />
            <Match idRef="CEP_CommonExampleKeywords" />
        </Any>
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="cc14d-3110">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="cc14d-3110">Keywords</span></span>

#### <a name="cepglobalfilter"></a><span data-ttu-id="cc14d-3111">CEP_GlobalFilter</span><span class="sxs-lookup"><span data-stu-id="cc14d-3111">CEP_GlobalFilter</span></span>

- <span data-ttu-id="cc14d-3112">algumas-senha</span><span class="sxs-lookup"><span data-stu-id="cc14d-3112">some-password</span></span>
- <span data-ttu-id="cc14d-3113">somepassword</span><span class="sxs-lookup"><span data-stu-id="cc14d-3113">somepassword</span></span>
- <span data-ttu-id="cc14d-3114">secretPassword</span><span class="sxs-lookup"><span data-stu-id="cc14d-3114">secretPassword</span></span>
- <span data-ttu-id="cc14d-3115">ISV</span><span class="sxs-lookup"><span data-stu-id="cc14d-3115">sample</span></span>

#### <a name="ceppasswordplaceholder"></a><span data-ttu-id="cc14d-3116">CEP_PasswordPlaceHolder</span><span class="sxs-lookup"><span data-stu-id="cc14d-3116">CEP_PasswordPlaceHolder</span></span>

<span data-ttu-id="cc14d-3117">(Observe que tecnicamente, esse tipo de informação confidencial identifica essas palavras-chave usando uma expressão regular, não uma lista de palavras-chave.)</span><span class="sxs-lookup"><span data-stu-id="cc14d-3117">(Note that technically, this sensitive information type identifies these keywords by using a regular expression, not a keyword list.)</span></span>

- <span data-ttu-id="cc14d-3118">Senha ou pwd seguidos por 0-2 espaços, um sinal de igual (=), 0-2 espaços e um asterisco (\*)--ou--</span><span class="sxs-lookup"><span data-stu-id="cc14d-3118">Password or pwd followed by 0-2 spaces, an equal sign (=), 0-2 spaces, and an asterisk (\*) --OR--</span></span>
- <span data-ttu-id="cc14d-3119">Senha ou pwd seguido por:</span><span class="sxs-lookup"><span data-stu-id="cc14d-3119">Password or pwd followed by:</span></span>
    - <span data-ttu-id="cc14d-3120">Sinal de igual (=)</span><span class="sxs-lookup"><span data-stu-id="cc14d-3120">Equal sign (=)</span></span>
    - <span data-ttu-id="cc14d-3121">Sinal de menor que (<)</span><span class="sxs-lookup"><span data-stu-id="cc14d-3121">Less than symbol (<)</span></span>
    - <span data-ttu-id="cc14d-3122">Qualquer combinação de 1-200 caracteres que sejam letras maiúsculas ou minúsculas, dígitos, um asterisco (\*), hífen (-), sublinhado (_) ou caractere de espaço em branco</span><span class="sxs-lookup"><span data-stu-id="cc14d-3122">Any combination of 1-200 characters that are upper- or lowercase letters, digits, an asterisk (\*), hyphen (-), underline (_), or whitespace character</span></span>
    - <span data-ttu-id="cc14d-3123">Símbolo maior que (>)</span><span class="sxs-lookup"><span data-stu-id="cc14d-3123">Greater than symbol (>)</span></span>

#### <a name="cepcommonexamplekeywords"></a><span data-ttu-id="cc14d-3124">CEP_CommonExampleKeywords</span><span class="sxs-lookup"><span data-stu-id="cc14d-3124">CEP_CommonExampleKeywords</span></span>

<span data-ttu-id="cc14d-3125">(Observe que tecnicamente, esse tipo de informação confidencial identifica essas palavras-chave usando uma expressão regular, não uma lista de palavras-chave.)</span><span class="sxs-lookup"><span data-stu-id="cc14d-3125">(Note that technically, this sensitive information type identifies these keywords by using a regular expression, not a keyword list.)</span></span>

- <span data-ttu-id="cc14d-3126">contoso</span><span class="sxs-lookup"><span data-stu-id="cc14d-3126">contoso</span></span>
- <span data-ttu-id="cc14d-3127">fabrikam</span><span class="sxs-lookup"><span data-stu-id="cc14d-3127">fabrikam</span></span>
- <span data-ttu-id="cc14d-3128">Northwind</span><span class="sxs-lookup"><span data-stu-id="cc14d-3128">northwind</span></span>
- <span data-ttu-id="cc14d-3129">área restrita</span><span class="sxs-lookup"><span data-stu-id="cc14d-3129">sandbox</span></span>
- <span data-ttu-id="cc14d-3130">Onebox</span><span class="sxs-lookup"><span data-stu-id="cc14d-3130">onebox</span></span>
- <span data-ttu-id="cc14d-3131">localhost</span><span class="sxs-lookup"><span data-stu-id="cc14d-3131">localhost</span></span>
- <span data-ttu-id="cc14d-3132">127.0.0.1</span><span class="sxs-lookup"><span data-stu-id="cc14d-3132">127.0.0.1</span></span>
- <span data-ttu-id="cc14d-3133">testacs. <!--no-hyperlink-->com</span><span class="sxs-lookup"><span data-stu-id="cc14d-3133">testacs.<!--no-hyperlink-->com</span></span>
- <span data-ttu-id="cc14d-3134">s-int.<!--no-hyperlink-->net</span><span class="sxs-lookup"><span data-stu-id="cc14d-3134">s-int.<!--no-hyperlink-->net</span></span>

## <a name="sweden-national-id"></a><span data-ttu-id="cc14d-3135">ID nacional da Suécia</span><span class="sxs-lookup"><span data-stu-id="cc14d-3135">Sweden National ID</span></span>

### <a name="format"></a><span data-ttu-id="cc14d-3136">Format</span><span class="sxs-lookup"><span data-stu-id="cc14d-3136">Format</span></span>

<span data-ttu-id="cc14d-3137">10 ou 12 dígitos e um delimitador opcional</span><span class="sxs-lookup"><span data-stu-id="cc14d-3137">10 or 12 digits and an optional delimiter</span></span>

### <a name="pattern"></a><span data-ttu-id="cc14d-3138">Padrão</span><span class="sxs-lookup"><span data-stu-id="cc14d-3138">Pattern</span></span>

<span data-ttu-id="cc14d-3139">10 ou 12 dígitos e um delimitador opcional:</span><span class="sxs-lookup"><span data-stu-id="cc14d-3139">10 or 12 digits and an optional delimiter:</span></span>
- <span data-ttu-id="cc14d-3140">2 a 4 dígitos (opcionais)</span><span class="sxs-lookup"><span data-stu-id="cc14d-3140">2-4 digits (optional)</span></span> 
- <span data-ttu-id="cc14d-3141">Seis dígitos no formato de data AAMMDD</span><span class="sxs-lookup"><span data-stu-id="cc14d-3141">Six digits in date format YYMMDD</span></span> 
- <span data-ttu-id="cc14d-3142">Um delimitador de "-" ou "+" (opcional), mais</span><span class="sxs-lookup"><span data-stu-id="cc14d-3142">Delimiter of "-" or "+" (optional), plus</span></span>
- <span data-ttu-id="cc14d-3143">Quatro dígitos</span><span class="sxs-lookup"><span data-stu-id="cc14d-3143">Four digits</span></span>

### <a name="checksum"></a><span data-ttu-id="cc14d-3144">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="cc14d-3144">Checksum</span></span>

<span data-ttu-id="cc14d-3145">Sim</span><span class="sxs-lookup"><span data-stu-id="cc14d-3145">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="cc14d-3146">Definição</span><span class="sxs-lookup"><span data-stu-id="cc14d-3146">Definition</span></span>

<span data-ttu-id="cc14d-3147">Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="cc14d-3147">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="cc14d-3148">A função Func_swedish_national_identifier localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="cc14d-3148">The function Func_swedish_national_identifier finds content that matches the pattern.</span></span>
- <span data-ttu-id="cc14d-3149">A soma de verificação passa.</span><span class="sxs-lookup"><span data-stu-id="cc14d-3149">The checksum passes.</span></span>

```
<!-- Sweden National ID -->
<Entity id="f69aaf40-79be-4fac-8f05-fd1910d272c8" patternsProximity="300" recommendedConfidence="85">
    <Pattern confidenceLevel="85">
        <IdMatch idRef="Func_swedish_national_identifier" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="cc14d-3150">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="cc14d-3150">Keywords</span></span>

<span data-ttu-id="cc14d-3151">Não</span><span class="sxs-lookup"><span data-stu-id="cc14d-3151">No</span></span>
   
## <a name="sweden-passport-number"></a><span data-ttu-id="cc14d-3152">Número de passaporte da Suécia</span><span class="sxs-lookup"><span data-stu-id="cc14d-3152">Sweden Passport Number</span></span>

### <a name="format"></a><span data-ttu-id="cc14d-3153">Format</span><span class="sxs-lookup"><span data-stu-id="cc14d-3153">Format</span></span>

<span data-ttu-id="cc14d-3154">Oito dígitos</span><span class="sxs-lookup"><span data-stu-id="cc14d-3154">Eight digits</span></span>

### <a name="pattern"></a><span data-ttu-id="cc14d-3155">Padrão</span><span class="sxs-lookup"><span data-stu-id="cc14d-3155">Pattern</span></span>

<span data-ttu-id="cc14d-3156">Oito dígitos consecutivos</span><span class="sxs-lookup"><span data-stu-id="cc14d-3156">Eight consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="cc14d-3157">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="cc14d-3157">Checksum</span></span>

<span data-ttu-id="cc14d-3158">Não</span><span class="sxs-lookup"><span data-stu-id="cc14d-3158">No</span></span>

### <a name="definition"></a><span data-ttu-id="cc14d-3159">Definição</span><span class="sxs-lookup"><span data-stu-id="cc14d-3159">Definition</span></span>

<span data-ttu-id="cc14d-3160">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="cc14d-3160">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="cc14d-3161">A expressão regular Regex_sweden_passport_number localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="cc14d-3161">The regular expression Regex_sweden_passport_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="cc14d-3162">Uma das seguintes opções for verdadeira:</span><span class="sxs-lookup"><span data-stu-id="cc14d-3162">One of the following is true:</span></span>
    - <span data-ttu-id="cc14d-3163">Uma palavra-chave de Keyword_passport for encontrada.</span><span class="sxs-lookup"><span data-stu-id="cc14d-3163">A keyword from Keyword_passport is found.</span></span>
    - <span data-ttu-id="cc14d-3164">Uma palavra-chave de Keyword_sweden_passport for encontrada.</span><span class="sxs-lookup"><span data-stu-id="cc14d-3164">A keyword from Keyword_sweden_passport is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="cc14d-3165">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="cc14d-3165">Keywords</span></span>
   
#### <a name="keywordswedenpassport"></a><span data-ttu-id="cc14d-3166">Keyword_sweden_passport</span><span class="sxs-lookup"><span data-stu-id="cc14d-3166">Keyword_sweden_passport</span></span>

- <span data-ttu-id="cc14d-3167">visa requirements</span><span class="sxs-lookup"><span data-stu-id="cc14d-3167">visa requirements</span></span> 
- <span data-ttu-id="cc14d-3168">Alien Registration Card</span><span class="sxs-lookup"><span data-stu-id="cc14d-3168">Alien Registration Card</span></span> 
- <span data-ttu-id="cc14d-3169">Schengen visas</span><span class="sxs-lookup"><span data-stu-id="cc14d-3169">Schengen visas</span></span> 
- <span data-ttu-id="cc14d-3170">Schengen visa</span><span class="sxs-lookup"><span data-stu-id="cc14d-3170">Schengen visa</span></span> 
- <span data-ttu-id="cc14d-3171">Visa Processing</span><span class="sxs-lookup"><span data-stu-id="cc14d-3171">Visa Processing</span></span> 
- <span data-ttu-id="cc14d-3172">Visa Type</span><span class="sxs-lookup"><span data-stu-id="cc14d-3172">Visa Type</span></span> 
- <span data-ttu-id="cc14d-3173">Single Entry</span><span class="sxs-lookup"><span data-stu-id="cc14d-3173">Single Entry</span></span> 
- <span data-ttu-id="cc14d-3174">Multiple Entry</span><span class="sxs-lookup"><span data-stu-id="cc14d-3174">Multiple Entry</span></span> 
- <span data-ttu-id="cc14d-3175">G3 Processing Fees</span><span class="sxs-lookup"><span data-stu-id="cc14d-3175">G3 Processing Fees</span></span> 

#### <a name="keywordpassport"></a><span data-ttu-id="cc14d-3176">Keyword_passport</span><span class="sxs-lookup"><span data-stu-id="cc14d-3176">Keyword_passport</span></span>

- <span data-ttu-id="cc14d-3177">Passport Number</span><span class="sxs-lookup"><span data-stu-id="cc14d-3177">Passport Number</span></span> 
- <span data-ttu-id="cc14d-3178">Passport No</span><span class="sxs-lookup"><span data-stu-id="cc14d-3178">Passport No</span></span> 
- <span data-ttu-id="cc14d-3179">Passport #</span><span class="sxs-lookup"><span data-stu-id="cc14d-3179">Passport #</span></span> 
- <span data-ttu-id="cc14d-3180">Passaport</span><span class="sxs-lookup"><span data-stu-id="cc14d-3180">Passport#</span></span> 
- <span data-ttu-id="cc14d-3181">Passportid</span><span class="sxs-lookup"><span data-stu-id="cc14d-3181">PassportID</span></span> 
- <span data-ttu-id="cc14d-3182">Passportno</span><span class="sxs-lookup"><span data-stu-id="cc14d-3182">Passportno</span></span> 
- <span data-ttu-id="cc14d-3183">passportnumber</span><span class="sxs-lookup"><span data-stu-id="cc14d-3183">passportnumber</span></span> 
- <span data-ttu-id="cc14d-3184">パスポート</span><span class="sxs-lookup"><span data-stu-id="cc14d-3184">パスポート</span></span> 
- <span data-ttu-id="cc14d-3185">パスポート番号</span><span class="sxs-lookup"><span data-stu-id="cc14d-3185">パスポート番号</span></span> 
- <span data-ttu-id="cc14d-3186">パスポートのNum</span><span class="sxs-lookup"><span data-stu-id="cc14d-3186">パスポートのNum</span></span> 
- <span data-ttu-id="cc14d-3187">パスポート #</span><span class="sxs-lookup"><span data-stu-id="cc14d-3187">パスポート＃</span></span> 
- <span data-ttu-id="cc14d-3188">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="cc14d-3188">Numéro de passeport</span></span> 
- <span data-ttu-id="cc14d-3189">Passeport n °</span><span class="sxs-lookup"><span data-stu-id="cc14d-3189">Passeport n °</span></span> 
- <span data-ttu-id="cc14d-3190">Passeport Non</span><span class="sxs-lookup"><span data-stu-id="cc14d-3190">Passeport Non</span></span> 
- <span data-ttu-id="cc14d-3191">Passeport #</span><span class="sxs-lookup"><span data-stu-id="cc14d-3191">Passeport #</span></span> 
- <span data-ttu-id="cc14d-3192">Passeport #</span><span class="sxs-lookup"><span data-stu-id="cc14d-3192">Passeport#</span></span> 
- <span data-ttu-id="cc14d-3193">PasseportNon</span><span class="sxs-lookup"><span data-stu-id="cc14d-3193">PasseportNon</span></span> 
- <span data-ttu-id="cc14d-3194">Passeportn °</span><span class="sxs-lookup"><span data-stu-id="cc14d-3194">Passeportn °</span></span> 
   
## <a name="swift-code"></a><span data-ttu-id="cc14d-3195">Código SWIFT</span><span class="sxs-lookup"><span data-stu-id="cc14d-3195">SWIFT Code</span></span>

### <a name="format"></a><span data-ttu-id="cc14d-3196">Format</span><span class="sxs-lookup"><span data-stu-id="cc14d-3196">Format</span></span>

<span data-ttu-id="cc14d-3197">Quatro letras seguidas por 5 a 31 letras ou dígitos</span><span class="sxs-lookup"><span data-stu-id="cc14d-3197">Four letters followed by 5-31 letters or digits</span></span>

### <a name="pattern"></a><span data-ttu-id="cc14d-3198">Padrão</span><span class="sxs-lookup"><span data-stu-id="cc14d-3198">Pattern</span></span>

<span data-ttu-id="cc14d-3199">Quatro letras seguidas por 5 a 31 letras ou dígitos:</span><span class="sxs-lookup"><span data-stu-id="cc14d-3199">Four letters followed by 5-31 letters or digits:</span></span>
- <span data-ttu-id="cc14d-3200">Código bancário de quatro letras (não diferencia maiúsculas de minúsculas)</span><span class="sxs-lookup"><span data-stu-id="cc14d-3200">Four-letter bank code (not case sensitive)</span></span> 
- <span data-ttu-id="cc14d-3201">Um espaço opcional</span><span class="sxs-lookup"><span data-stu-id="cc14d-3201">An optional space</span></span> 
- <span data-ttu-id="cc14d-3202">4 a 28 letras ou dígitos (o número de conta bancária básica (BBAN))</span><span class="sxs-lookup"><span data-stu-id="cc14d-3202">4-28 letters or digits (the Basic Bank Account Number (BBAN))</span></span> 
- <span data-ttu-id="cc14d-3203">Um espaço opcional</span><span class="sxs-lookup"><span data-stu-id="cc14d-3203">An optional space</span></span> 
- <span data-ttu-id="cc14d-3204">1 a 3 letras ou dígitos (restante do BBAN)</span><span class="sxs-lookup"><span data-stu-id="cc14d-3204">1-3 letters or digits (remainder of the BBAN)</span></span>

### <a name="checksum"></a><span data-ttu-id="cc14d-3205">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="cc14d-3205">Checksum</span></span>

<span data-ttu-id="cc14d-3206">Não</span><span class="sxs-lookup"><span data-stu-id="cc14d-3206">No</span></span>

### <a name="definition"></a><span data-ttu-id="cc14d-3207">Definição</span><span class="sxs-lookup"><span data-stu-id="cc14d-3207">Definition</span></span>

<span data-ttu-id="cc14d-3208">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="cc14d-3208">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="cc14d-3209">A expressão regular Regex_swift localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="cc14d-3209">The regular expression Regex_swift finds content that matches the pattern.</span></span>
- <span data-ttu-id="cc14d-3210">Uma palavra-chave de Keyword_swift for encontrada.</span><span class="sxs-lookup"><span data-stu-id="cc14d-3210">A keyword from Keyword_swift is found.</span></span>

```
<Entity id="cb2ab58c-9cb8-4c81-baf8-a4e106791df4" patternsProximity="300" recommendedConfidence="75">
<Pattern confidenceLevel="75">
        <IdMatch idRef="Regex_swift" />
        <Match idRef="Keyword_swift" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="cc14d-3211">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="cc14d-3211">Keywords</span></span>
   
#### <a name="keywordswift"></a><span data-ttu-id="cc14d-3212">Keyword_swift</span><span class="sxs-lookup"><span data-stu-id="cc14d-3212">Keyword_swift</span></span>

- <span data-ttu-id="cc14d-3213">international organization for standardization 9362</span><span class="sxs-lookup"><span data-stu-id="cc14d-3213">international organization for standardization 9362</span></span> 
- <span data-ttu-id="cc14d-3214">iso 9362</span><span class="sxs-lookup"><span data-stu-id="cc14d-3214">iso 9362</span></span> 
- <span data-ttu-id="cc14d-3215">iso9362</span><span class="sxs-lookup"><span data-stu-id="cc14d-3215">iso9362</span></span> 
- <span data-ttu-id="cc14d-3216">Swift\#</span><span class="sxs-lookup"><span data-stu-id="cc14d-3216">swift\#</span></span> 
- <span data-ttu-id="cc14d-3217">swiftcode</span><span class="sxs-lookup"><span data-stu-id="cc14d-3217">swiftcode</span></span> 
- <span data-ttu-id="cc14d-3218">swiftnumber</span><span class="sxs-lookup"><span data-stu-id="cc14d-3218">swiftnumber</span></span> 
- <span data-ttu-id="cc14d-3219">swiftroutingnumber</span><span class="sxs-lookup"><span data-stu-id="cc14d-3219">swiftroutingnumber</span></span> 
- <span data-ttu-id="cc14d-3220">swift code</span><span class="sxs-lookup"><span data-stu-id="cc14d-3220">swift code</span></span> 
- <span data-ttu-id="cc14d-3221">swift number #</span><span class="sxs-lookup"><span data-stu-id="cc14d-3221">swift number #</span></span> 
- <span data-ttu-id="cc14d-3222">swift routing number</span><span class="sxs-lookup"><span data-stu-id="cc14d-3222">swift routing number</span></span> 
- <span data-ttu-id="cc14d-3223">bic number</span><span class="sxs-lookup"><span data-stu-id="cc14d-3223">bic number</span></span> 
- <span data-ttu-id="cc14d-3224">bic code</span><span class="sxs-lookup"><span data-stu-id="cc14d-3224">bic code</span></span> 
- <span data-ttu-id="cc14d-3225">BIC\#</span><span class="sxs-lookup"><span data-stu-id="cc14d-3225">bic \#</span></span> 
- <span data-ttu-id="cc14d-3226">BIC\#</span><span class="sxs-lookup"><span data-stu-id="cc14d-3226">bic\#</span></span> 
- <span data-ttu-id="cc14d-3227">bank identifier code</span><span class="sxs-lookup"><span data-stu-id="cc14d-3227">bank identifier code</span></span> 
- <span data-ttu-id="cc14d-3228">標準化 9362</span><span class="sxs-lookup"><span data-stu-id="cc14d-3228">標準化9362</span></span> 
- <span data-ttu-id="cc14d-3229">迅速 #</span><span class="sxs-lookup"><span data-stu-id="cc14d-3229">迅速＃</span></span> 
- <span data-ttu-id="cc14d-3230">SWIFTコード</span><span class="sxs-lookup"><span data-stu-id="cc14d-3230">SWIFTコード</span></span> 
- <span data-ttu-id="cc14d-3231">SWIFT番号</span><span class="sxs-lookup"><span data-stu-id="cc14d-3231">SWIFT番号</span></span> 
- <span data-ttu-id="cc14d-3232">迅速なルーティング番号</span><span class="sxs-lookup"><span data-stu-id="cc14d-3232">迅速なルーティング番号</span></span> 
- <span data-ttu-id="cc14d-3233">BIC番号</span><span class="sxs-lookup"><span data-stu-id="cc14d-3233">BIC番号</span></span> 
- <span data-ttu-id="cc14d-3234">BICコード</span><span class="sxs-lookup"><span data-stu-id="cc14d-3234">BICコード</span></span> 
- <span data-ttu-id="cc14d-3235">銀行識別コードのための国際組織</span><span class="sxs-lookup"><span data-stu-id="cc14d-3235">銀行識別コードのための国際組織</span></span> 
- <span data-ttu-id="cc14d-3236">Organisation internationale de normalisation 9362</span><span class="sxs-lookup"><span data-stu-id="cc14d-3236">Organisation internationale de normalisation 9362</span></span> 
- <span data-ttu-id="cc14d-3237">rápida\#</span><span class="sxs-lookup"><span data-stu-id="cc14d-3237">rapide \#</span></span> 
- <span data-ttu-id="cc14d-3238">code SWIFT</span><span class="sxs-lookup"><span data-stu-id="cc14d-3238">code SWIFT</span></span> 
- <span data-ttu-id="cc14d-3239">le numéro de swift</span><span class="sxs-lookup"><span data-stu-id="cc14d-3239">le numéro de swift</span></span> 
- <span data-ttu-id="cc14d-3240">swift numéro d'acheminement</span><span class="sxs-lookup"><span data-stu-id="cc14d-3240">swift numéro d'acheminement</span></span> 
- <span data-ttu-id="cc14d-3241">le numéro BIC</span><span class="sxs-lookup"><span data-stu-id="cc14d-3241">le numéro BIC</span></span> 
- <span data-ttu-id="cc14d-3242">\#BIC</span><span class="sxs-lookup"><span data-stu-id="cc14d-3242">\# BIC</span></span> 
- <span data-ttu-id="cc14d-3243">code identificateur de banque</span><span class="sxs-lookup"><span data-stu-id="cc14d-3243">code identificateur de banque</span></span> 
   
## <a name="taiwan-national-id"></a><span data-ttu-id="cc14d-3244">ID nacional de Taiwan</span><span class="sxs-lookup"><span data-stu-id="cc14d-3244">Taiwan National ID</span></span>

### <a name="format"></a><span data-ttu-id="cc14d-3245">Format</span><span class="sxs-lookup"><span data-stu-id="cc14d-3245">Format</span></span>

<span data-ttu-id="cc14d-3246">Uma letra (em inglês) seguida de nove dígitos</span><span class="sxs-lookup"><span data-stu-id="cc14d-3246">One letter (in English) followed by nine digits</span></span>

### <a name="pattern"></a><span data-ttu-id="cc14d-3247">Padrão</span><span class="sxs-lookup"><span data-stu-id="cc14d-3247">Pattern</span></span>

<span data-ttu-id="cc14d-3248">Uma letra (em inglês) seguida de nove dígitos:</span><span class="sxs-lookup"><span data-stu-id="cc14d-3248">One letter (in English) followed by nine digits:</span></span>
- <span data-ttu-id="cc14d-3249">Uma letra (em inglês, não diferencia maiúscula de minúscula)</span><span class="sxs-lookup"><span data-stu-id="cc14d-3249">One letter (in English, not case sensitive)</span></span> 
- <span data-ttu-id="cc14d-3250">O dígito "1" ou "2"</span><span class="sxs-lookup"><span data-stu-id="cc14d-3250">The digit "1" or "2"</span></span> 
- <span data-ttu-id="cc14d-3251">Oito dígitos</span><span class="sxs-lookup"><span data-stu-id="cc14d-3251">Eight digits</span></span>

### <a name="checksum"></a><span data-ttu-id="cc14d-3252">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="cc14d-3252">Checksum</span></span>

<span data-ttu-id="cc14d-3253">Sim</span><span class="sxs-lookup"><span data-stu-id="cc14d-3253">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="cc14d-3254">Definição</span><span class="sxs-lookup"><span data-stu-id="cc14d-3254">Definition</span></span>

<span data-ttu-id="cc14d-3255">Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="cc14d-3255">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="cc14d-3256">A função Func_taiwanese_national_id localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="cc14d-3256">The function Func_taiwanese_national_id finds content that matches the pattern.</span></span>
- <span data-ttu-id="cc14d-3257">Uma palavra-chave de Keyword_taiwanese_national_id for encontrada.</span><span class="sxs-lookup"><span data-stu-id="cc14d-3257">A keyword from Keyword_taiwanese_national_id is found.</span></span>
- <span data-ttu-id="cc14d-3258">A soma de verificação passa.</span><span class="sxs-lookup"><span data-stu-id="cc14d-3258">The checksum passes.</span></span>

```
<!-- Taiwanese National ID -->
<Entity id="4C7BFC34-8DD1-421D-8FB7-6C6182C2AF03" patternsProximity="300" recommendedConfidence="85">
      <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_taiwanese_national_id" />
          <Match idRef="Keyword_taiwanese_national_id" />
      </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="cc14d-3259">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="cc14d-3259">Keywords</span></span>

#### <a name="keywordtaiwanesenationalid"></a><span data-ttu-id="cc14d-3260">Keyword_taiwanese_national_id</span><span class="sxs-lookup"><span data-stu-id="cc14d-3260">Keyword_taiwanese_national_id</span></span>

- <span data-ttu-id="cc14d-3261">身份證字號</span><span class="sxs-lookup"><span data-stu-id="cc14d-3261">身份證字號</span></span> 
- <span data-ttu-id="cc14d-3262">身份證</span><span class="sxs-lookup"><span data-stu-id="cc14d-3262">身份證</span></span> 
- <span data-ttu-id="cc14d-3263">身份證號碼</span><span class="sxs-lookup"><span data-stu-id="cc14d-3263">身份證號碼</span></span> 
- <span data-ttu-id="cc14d-3264">身份證號</span><span class="sxs-lookup"><span data-stu-id="cc14d-3264">身份證號</span></span> 
- <span data-ttu-id="cc14d-3265">身分證字號</span><span class="sxs-lookup"><span data-stu-id="cc14d-3265">身分證字號</span></span> 
- <span data-ttu-id="cc14d-3266">身分證</span><span class="sxs-lookup"><span data-stu-id="cc14d-3266">身分證</span></span> 
- <span data-ttu-id="cc14d-3267">身分證號碼</span><span class="sxs-lookup"><span data-stu-id="cc14d-3267">身分證號碼</span></span> 
- <span data-ttu-id="cc14d-3268">身份證號</span><span class="sxs-lookup"><span data-stu-id="cc14d-3268">身份證號</span></span> 
- <span data-ttu-id="cc14d-3269">身分證統一編號</span><span class="sxs-lookup"><span data-stu-id="cc14d-3269">身分證統一編號</span></span> 
- <span data-ttu-id="cc14d-3270">國民身分證統一編號</span><span class="sxs-lookup"><span data-stu-id="cc14d-3270">國民身分證統一編號</span></span> 
- <span data-ttu-id="cc14d-3271">簽名</span><span class="sxs-lookup"><span data-stu-id="cc14d-3271">簽名</span></span> 
- <span data-ttu-id="cc14d-3272">蓋章</span><span class="sxs-lookup"><span data-stu-id="cc14d-3272">蓋章</span></span> 
- <span data-ttu-id="cc14d-3273">簽名或蓋章</span><span class="sxs-lookup"><span data-stu-id="cc14d-3273">簽名或蓋章</span></span> 
- <span data-ttu-id="cc14d-3274">簽章</span><span class="sxs-lookup"><span data-stu-id="cc14d-3274">簽章</span></span>   
   
## <a name="taiwan-passport-number"></a><span data-ttu-id="cc14d-3275">	Número de passaporte de Taiwan</span><span class="sxs-lookup"><span data-stu-id="cc14d-3275">Taiwan Passport Number</span></span>

### <a name="format"></a><span data-ttu-id="cc14d-3276">Format</span><span class="sxs-lookup"><span data-stu-id="cc14d-3276">Format</span></span>

- <span data-ttu-id="cc14d-3277">Número de passaporte biométrico: nove dígitos</span><span class="sxs-lookup"><span data-stu-id="cc14d-3277">Biometric passport number: Nine digits</span></span>
- <span data-ttu-id="cc14d-3278">Número de passaporte não biométrico: nove dígitos</span><span class="sxs-lookup"><span data-stu-id="cc14d-3278">Non-biometric passport number: Nine digits</span></span>

### <a name="pattern"></a><span data-ttu-id="cc14d-3279">Padrão</span><span class="sxs-lookup"><span data-stu-id="cc14d-3279">Pattern</span></span>
<span data-ttu-id="cc14d-3280">Número de passaporte biométrico:</span><span class="sxs-lookup"><span data-stu-id="cc14d-3280">Biometric passport number:</span></span>
- <span data-ttu-id="cc14d-3281">O dígito "3" </span><span class="sxs-lookup"><span data-stu-id="cc14d-3281">The digit "3"</span></span> 
- <span data-ttu-id="cc14d-3282">Oito dígitos</span><span class="sxs-lookup"><span data-stu-id="cc14d-3282">Eight digits</span></span>

<span data-ttu-id="cc14d-3283">Número de passaporte não biométrico:</span><span class="sxs-lookup"><span data-stu-id="cc14d-3283">Non-biometric passport number:</span></span>
- <span data-ttu-id="cc14d-3284">Nove dígitos</span><span class="sxs-lookup"><span data-stu-id="cc14d-3284">Nine digits</span></span>

### <a name="checksum"></a><span data-ttu-id="cc14d-3285">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="cc14d-3285">Checksum</span></span>

<span data-ttu-id="cc14d-3286">Não</span><span class="sxs-lookup"><span data-stu-id="cc14d-3286">No</span></span>

### <a name="definition"></a><span data-ttu-id="cc14d-3287">Definição</span><span class="sxs-lookup"><span data-stu-id="cc14d-3287">Definition</span></span>

<span data-ttu-id="cc14d-3288">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="cc14d-3288">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="cc14d-3289">A expressão regular Regex_taiwan_passport localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="cc14d-3289">The regular expression Regex_taiwan_passport finds content that matches the pattern.</span></span>
- <span data-ttu-id="cc14d-3290">Uma palavra-chave de Keyword_taiwan_passport for encontrada.</span><span class="sxs-lookup"><span data-stu-id="cc14d-3290">A keyword from Keyword_taiwan_passport is found.</span></span>

```
<!-- Taiwan Passport Number -->
<Entity id="e7251cb4-4c2c-41df-963e-924eb3dae04a" recommendedConfidence="75" patternsProximity="300">
  <Pattern confidenceLevel="75">
     <IdMatch idRef="Regex_taiwan_passport"/>
     <Match idRef="Keyword_taiwan_passport"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="cc14d-3291">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="cc14d-3291">Keywords</span></span>

#### <a name="keywordtaiwanpassport"></a><span data-ttu-id="cc14d-3292">Keyword_taiwan_passport</span><span class="sxs-lookup"><span data-stu-id="cc14d-3292">Keyword_taiwan_passport</span></span>

- <span data-ttu-id="cc14d-3293">Número de passaporte ROC</span><span class="sxs-lookup"><span data-stu-id="cc14d-3293">ROC passport number</span></span> 
- <span data-ttu-id="cc14d-3294">Número de passaporte</span><span class="sxs-lookup"><span data-stu-id="cc14d-3294">Passport number</span></span> 
- <span data-ttu-id="cc14d-3295">Nº de passaporte</span><span class="sxs-lookup"><span data-stu-id="cc14d-3295">Passport no</span></span> 
- <span data-ttu-id="cc14d-3296">Núm de Passaporte</span><span class="sxs-lookup"><span data-stu-id="cc14d-3296">Passport Num</span></span> 
- <span data-ttu-id="cc14d-3297">Passport #</span><span class="sxs-lookup"><span data-stu-id="cc14d-3297">Passport #</span></span> 
- <span data-ttu-id="cc14d-3298">护照</span><span class="sxs-lookup"><span data-stu-id="cc14d-3298">护照</span></span> 
- <span data-ttu-id="cc14d-3299">中華民國護照</span><span class="sxs-lookup"><span data-stu-id="cc14d-3299">中華民國護照</span></span> 
- <span data-ttu-id="cc14d-3300">Zhōnghuá Mínguó hùzhào</span><span class="sxs-lookup"><span data-stu-id="cc14d-3300">Zhōnghuá Mínguó hùzhào</span></span>
   
## <a name="taiwan-resident-certificate-arctarc-number"></a><span data-ttu-id="cc14d-3301">Número do Certificado de residente de Taiwan (ARC/TARC)</span><span class="sxs-lookup"><span data-stu-id="cc14d-3301">Taiwan Resident Certificate (ARC/TARC) Number</span></span>

### <a name="format"></a><span data-ttu-id="cc14d-3302">Format</span><span class="sxs-lookup"><span data-stu-id="cc14d-3302">Format</span></span>

<span data-ttu-id="cc14d-3303">10 letras e dígitos</span><span class="sxs-lookup"><span data-stu-id="cc14d-3303">10 letters and digits</span></span>

### <a name="pattern"></a><span data-ttu-id="cc14d-3304">Padrão</span><span class="sxs-lookup"><span data-stu-id="cc14d-3304">Pattern</span></span>

<span data-ttu-id="cc14d-3305">10 letras e dígitos:</span><span class="sxs-lookup"><span data-stu-id="cc14d-3305">10 letters and digits:</span></span>
- <span data-ttu-id="cc14d-3306">Duas letras (não diferenciam maiúsculas de minúsculas)</span><span class="sxs-lookup"><span data-stu-id="cc14d-3306">Two letters (not case sensitive)</span></span> 
- <span data-ttu-id="cc14d-3307">Oito dígitos</span><span class="sxs-lookup"><span data-stu-id="cc14d-3307">Eight digits</span></span>

### <a name="checksum"></a><span data-ttu-id="cc14d-3308">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="cc14d-3308">Checksum</span></span>

<span data-ttu-id="cc14d-3309">Não</span><span class="sxs-lookup"><span data-stu-id="cc14d-3309">No</span></span>

### <a name="definition"></a><span data-ttu-id="cc14d-3310">Definição</span><span class="sxs-lookup"><span data-stu-id="cc14d-3310">Definition</span></span>

<span data-ttu-id="cc14d-3311">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="cc14d-3311">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="cc14d-3312">A expressão regular Regex_taiwan_resident_certificate localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="cc14d-3312">The regular expression Regex_taiwan_resident_certificate finds content that matches the pattern.</span></span>
- <span data-ttu-id="cc14d-3313">Uma palavra-chave de Keyword_taiwan_resident_certificate for encontrada.</span><span class="sxs-lookup"><span data-stu-id="cc14d-3313">A keyword from Keyword_taiwan_resident_certificate is found.</span></span>

```
<!-- Taiwan Resident Certificate (ARC/TARC) -->
<Entity id="48269fec-05ea-46ea-b326-f5623a58c6e9" recommendedConfidence="75" patternsProximity="300">
  <Pattern confidenceLevel="75">
     <IdMatch idRef="Regex_taiwan_resident_certificate"/>
     <Match idRef="Keyword_taiwan_resident_certificate"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="cc14d-3314">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="cc14d-3314">Keywords</span></span>

#### <a name="keywordtaiwanresidentcertificate"></a><span data-ttu-id="cc14d-3315">Keyword_taiwan_resident_certificate</span><span class="sxs-lookup"><span data-stu-id="cc14d-3315">Keyword_taiwan_resident_certificate</span></span>

- <span data-ttu-id="cc14d-3316">Certificado de Residente</span><span class="sxs-lookup"><span data-stu-id="cc14d-3316">Resident Certificate</span></span> 
- <span data-ttu-id="cc14d-3317">Cert de Residente</span><span class="sxs-lookup"><span data-stu-id="cc14d-3317">Resident Cert</span></span> 
- <span data-ttu-id="cc14d-3318">Cert. de Residente
</span><span class="sxs-lookup"><span data-stu-id="cc14d-3318">Resident Cert.</span></span> 
- <span data-ttu-id="cc14d-3319">Cartão de identificação</span><span class="sxs-lookup"><span data-stu-id="cc14d-3319">Identification card</span></span> 
- <span data-ttu-id="cc14d-3320">Certificado de Residente Alien</span><span class="sxs-lookup"><span data-stu-id="cc14d-3320">Alien Resident Certificate</span></span> 
- <span data-ttu-id="cc14d-3321">ARCO</span><span class="sxs-lookup"><span data-stu-id="cc14d-3321">ARC</span></span> 
- <span data-ttu-id="cc14d-3322">Certificado de Residente da Área de Taiwan</span><span class="sxs-lookup"><span data-stu-id="cc14d-3322">Taiwan Area Resident Certificate</span></span> 
- <span data-ttu-id="cc14d-3323">TARC</span><span class="sxs-lookup"><span data-stu-id="cc14d-3323">TARC</span></span> 
- <span data-ttu-id="cc14d-3324">居留證</span><span class="sxs-lookup"><span data-stu-id="cc14d-3324">居留證</span></span> 
- <span data-ttu-id="cc14d-3325">外僑居留證</span><span class="sxs-lookup"><span data-stu-id="cc14d-3325">外僑居留證</span></span> 
- <span data-ttu-id="cc14d-3326">台灣地區居留證</span><span class="sxs-lookup"><span data-stu-id="cc14d-3326">台灣地區居留證</span></span> 

## <a name="thai-population-identification-code"></a><span data-ttu-id="cc14d-3327">Código de identificação de população em tailandês</span><span class="sxs-lookup"><span data-stu-id="cc14d-3327">Thai Population Identification Code</span></span>

### <a name="format"></a><span data-ttu-id="cc14d-3328">Format</span><span class="sxs-lookup"><span data-stu-id="cc14d-3328">Format</span></span>

<span data-ttu-id="cc14d-3329">13 dígitos</span><span class="sxs-lookup"><span data-stu-id="cc14d-3329">13 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="cc14d-3330">Padrão</span><span class="sxs-lookup"><span data-stu-id="cc14d-3330">Pattern</span></span>

<span data-ttu-id="cc14d-3331">13 dígitos:</span><span class="sxs-lookup"><span data-stu-id="cc14d-3331">13 digits:</span></span>
- <span data-ttu-id="cc14d-3332">O primeiro dígito não é 0 ou 9</span><span class="sxs-lookup"><span data-stu-id="cc14d-3332">First digit is not 0 or 9</span></span> 
- <span data-ttu-id="cc14d-3333">12 dígitos</span><span class="sxs-lookup"><span data-stu-id="cc14d-3333">12 digits</span></span>

### <a name="checksum"></a><span data-ttu-id="cc14d-3334">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="cc14d-3334">Checksum</span></span>

<span data-ttu-id="cc14d-3335">Sim</span><span class="sxs-lookup"><span data-stu-id="cc14d-3335">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="cc14d-3336">Definição</span><span class="sxs-lookup"><span data-stu-id="cc14d-3336">Definition</span></span>

<span data-ttu-id="cc14d-3337">Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="cc14d-3337">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="cc14d-3338">A função Func_Thai_Citizen_Id localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="cc14d-3338">The function Func_Thai_Citizen_Id finds content that matches the pattern.</span></span>
- <span data-ttu-id="cc14d-3339">Uma palavra-chave de Keyword_Thai_Citizen_Id for encontrada.</span><span class="sxs-lookup"><span data-stu-id="cc14d-3339">A keyword from Keyword_Thai_Citizen_Id is found.</span></span>

<span data-ttu-id="cc14d-3340">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="cc14d-3340">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="cc14d-3341">A função Func_Thai_Citizen_Id localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="cc14d-3341">The function Func_Thai_Citizen_Id finds content that matches the pattern.</span></span>

```
<!-- Thai Citizen ID -->
-<Entity id="44ca9e86-ead7-4c5d-884a-e2eaa401515e" recommendedConfidence="75" patternsProximity="300">
   -<Pattern confidenceLevel="85">
      <IdMatch idRef="Func_Thai_Citizen_Id"/>
      <Match idRef="Keyword_Thai_Citizen_Id"/>
   </Pattern>
   -<Pattern confidenceLevel="75">
      <IdMatch idRef="Func_Thai_Citizen_Id"/>
   </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="cc14d-3342">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="cc14d-3342">Keywords</span></span>

#### <a name="keywordthaicitizenid"></a><span data-ttu-id="cc14d-3343">Keyword_Thai_Citizen_Id</span><span class="sxs-lookup"><span data-stu-id="cc14d-3343">Keyword_Thai_Citizen_Id</span></span>

- <span data-ttu-id="cc14d-3344">Número de Identificação</span><span class="sxs-lookup"><span data-stu-id="cc14d-3344">ID Number</span></span>
- <span data-ttu-id="cc14d-3345">Número de identificação</span><span class="sxs-lookup"><span data-stu-id="cc14d-3345">Identification Number</span></span>
- <span data-ttu-id="cc14d-3346">บัตรประชาชน</span><span class="sxs-lookup"><span data-stu-id="cc14d-3346">บัตรประชาชน</span></span>
- <span data-ttu-id="cc14d-3347">รหัสบัตรประชาชน</span><span class="sxs-lookup"><span data-stu-id="cc14d-3347">รหัสบัตรประชาชน</span></span>
- <span data-ttu-id="cc14d-3348">บัตรประชาชน</span><span class="sxs-lookup"><span data-stu-id="cc14d-3348">บัตรประชาชน</span></span>
- <span data-ttu-id="cc14d-3349">รหัสบัตรประชาชน</span><span class="sxs-lookup"><span data-stu-id="cc14d-3349">รหัสบัตรประชาชน</span></span>
  
## <a name="turkish-national-identification-number"></a><span data-ttu-id="cc14d-3350">Número de identificação nacional turco</span><span class="sxs-lookup"><span data-stu-id="cc14d-3350">Turkish National Identification Number</span></span>

### <a name="format"></a><span data-ttu-id="cc14d-3351">Format</span><span class="sxs-lookup"><span data-stu-id="cc14d-3351">Format</span></span>

<span data-ttu-id="cc14d-3352">11 dígitos</span><span class="sxs-lookup"><span data-stu-id="cc14d-3352">11 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="cc14d-3353">Padrão</span><span class="sxs-lookup"><span data-stu-id="cc14d-3353">Pattern</span></span>

<span data-ttu-id="cc14d-3354">11 dígitos</span><span class="sxs-lookup"><span data-stu-id="cc14d-3354">11 digits</span></span>

### <a name="checksum"></a><span data-ttu-id="cc14d-3355">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="cc14d-3355">Checksum</span></span>

<span data-ttu-id="cc14d-3356">Sim</span><span class="sxs-lookup"><span data-stu-id="cc14d-3356">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="cc14d-3357">Definição</span><span class="sxs-lookup"><span data-stu-id="cc14d-3357">Definition</span></span>

<span data-ttu-id="cc14d-3358">Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="cc14d-3358">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="cc14d-3359">A função Func_Turkish_National_Id localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="cc14d-3359">The function Func_Turkish_National_Id finds content that matches the pattern.</span></span>
- <span data-ttu-id="cc14d-3360">Uma palavra-chave de Keyword_Turkish_National_Id for encontrada.</span><span class="sxs-lookup"><span data-stu-id="cc14d-3360">A keyword from Keyword_Turkish_National_Id is found.</span></span>

<span data-ttu-id="cc14d-3361">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="cc14d-3361">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="cc14d-3362">A função Func_Turkish_National_Id localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="cc14d-3362">The function Func_Turkish_National_Id finds content that matches the pattern.</span></span>

```
<!-- Turkish National Identity -->
-<Entity id="fb621f20-3876-4cfc-acec-8c8e73ca32c7" recommendedConfidence="75" patternsProximity="300">
   -<Pattern confidenceLevel="85">
      <IdMatch idRef="Func_Turkish_National_Id"/>
      <Match idRef="Keyword_Turkish_National_Id"/>
   </Pattern>
   -<Pattern confidenceLevel="75">
      <IdMatch idRef="Func_Turkish_National_Id"/>
   </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="cc14d-3363">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="cc14d-3363">Keywords</span></span>

#### <a name="keywordturkishnationalid"></a><span data-ttu-id="cc14d-3364">Keyword_Turkish_National_Id</span><span class="sxs-lookup"><span data-stu-id="cc14d-3364">Keyword_Turkish_National_Id</span></span>

- <span data-ttu-id="cc14d-3365">Kimlik TC não</span><span class="sxs-lookup"><span data-stu-id="cc14d-3365">TC Kimlik No</span></span>
- <span data-ttu-id="cc14d-3366">TC Kimlik numarası</span><span class="sxs-lookup"><span data-stu-id="cc14d-3366">TC Kimlik numarası</span></span>
- <span data-ttu-id="cc14d-3367">Vatandaşlık numarası</span><span class="sxs-lookup"><span data-stu-id="cc14d-3367">Vatandaşlık numarası</span></span>
- <span data-ttu-id="cc14d-3368">Vatandaşlık não</span><span class="sxs-lookup"><span data-stu-id="cc14d-3368">Vatandaşlık no</span></span>

## <a name="uk-drivers-license-number"></a><span data-ttu-id="cc14d-p141">Número de carteira de motorista do Reino Unido</span><span class="sxs-lookup"><span data-stu-id="cc14d-p141">U.K. Driver's License Number</span></span>

### <a name="format"></a><span data-ttu-id="cc14d-3371">Format</span><span class="sxs-lookup"><span data-stu-id="cc14d-3371">Format</span></span>

<span data-ttu-id="cc14d-3372">Combinação de 18 letras e dígitos no formato especificado</span><span class="sxs-lookup"><span data-stu-id="cc14d-3372">Combination of 18 letters and digits in the specified format</span></span>

### <a name="pattern"></a><span data-ttu-id="cc14d-3373">Padrão</span><span class="sxs-lookup"><span data-stu-id="cc14d-3373">Pattern</span></span>

<span data-ttu-id="cc14d-3374">18 letras e dígitos:</span><span class="sxs-lookup"><span data-stu-id="cc14d-3374">18 letters and digits:</span></span>
- <span data-ttu-id="cc14d-3375">Cinco letras (não diferenciam maiúsculas de minúsculas) ou o dígito "9" em vez de uma letra</span><span class="sxs-lookup"><span data-stu-id="cc14d-3375">Five letters (not case sensitive) or the digit "9" in place of a letter</span></span> 
- <span data-ttu-id="cc14d-3376">Um dígito</span><span class="sxs-lookup"><span data-stu-id="cc14d-3376">One digit</span></span> 
- <span data-ttu-id="cc14d-3377">Cinco dígitos no formato de data DDMMA para data de nascimento</span><span class="sxs-lookup"><span data-stu-id="cc14d-3377">Five digits in the date format DDMMY for date of birth</span></span> 
- <span data-ttu-id="cc14d-3378">Duas letras (não diferenciam maiúsculas de minúsculas) ou o dígito "9" em vez de uma letra</span><span class="sxs-lookup"><span data-stu-id="cc14d-3378">Two letters (not case sensitive) or the digit "9" in place of a letter</span></span> 
- <span data-ttu-id="cc14d-3379">Cinco dígitos</span><span class="sxs-lookup"><span data-stu-id="cc14d-3379">Five digits</span></span>

### <a name="checksum"></a><span data-ttu-id="cc14d-3380">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="cc14d-3380">Checksum</span></span>

<span data-ttu-id="cc14d-3381">Sim</span><span class="sxs-lookup"><span data-stu-id="cc14d-3381">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="cc14d-3382">Definição</span><span class="sxs-lookup"><span data-stu-id="cc14d-3382">Definition</span></span>

<span data-ttu-id="cc14d-3383">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="cc14d-3383">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="cc14d-3384">A função Func_uk_drivers_license localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="cc14d-3384">The function Func_uk_drivers_license finds content that matches the pattern.</span></span>
- <span data-ttu-id="cc14d-3385">Uma palavra-chave de Keyword_uk_drivers_license for encontrada.</span><span class="sxs-lookup"><span data-stu-id="cc14d-3385">A keyword from Keyword_uk_drivers_license is found.</span></span>
- <span data-ttu-id="cc14d-3386">A soma de verificação passa.</span><span class="sxs-lookup"><span data-stu-id="cc14d-3386">The checksum passes.</span></span>

```
<!-- U.K. Driver's License Number -->
<Entity id="f93de4be-d94c-40df-a8be-461738047551" patternsProximity="300" recommendedConfidence="75">
    <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_uk_drivers_license" />
        <Match idRef="Keyword_uk_drivers_license" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="cc14d-3387">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="cc14d-3387">Keywords</span></span>

#### <a name="keywordukdriverslicense"></a><span data-ttu-id="cc14d-3388">Keyword_uk_drivers_license</span><span class="sxs-lookup"><span data-stu-id="cc14d-3388">Keyword_uk_drivers_license</span></span>

- <span data-ttu-id="cc14d-3389">DVLA</span><span class="sxs-lookup"><span data-stu-id="cc14d-3389">DVLA</span></span> 
- <span data-ttu-id="cc14d-3390">light vans</span><span class="sxs-lookup"><span data-stu-id="cc14d-3390">light vans</span></span> 
- <span data-ttu-id="cc14d-3391">quadbikes</span><span class="sxs-lookup"><span data-stu-id="cc14d-3391">quadbikes</span></span> 
- <span data-ttu-id="cc14d-3392">motor cars</span><span class="sxs-lookup"><span data-stu-id="cc14d-3392">motor cars</span></span> 
- <span data-ttu-id="cc14d-3393">125cc</span><span class="sxs-lookup"><span data-stu-id="cc14d-3393">125cc</span></span> 
- <span data-ttu-id="cc14d-3394">sidecar</span><span class="sxs-lookup"><span data-stu-id="cc14d-3394">sidecar</span></span> 
- <span data-ttu-id="cc14d-3395">tricycles</span><span class="sxs-lookup"><span data-stu-id="cc14d-3395">tricycles</span></span> 
- <span data-ttu-id="cc14d-3396">Motorcycles</span><span class="sxs-lookup"><span data-stu-id="cc14d-3396">motorcycles</span></span> 
- <span data-ttu-id="cc14d-3397">photocard licence</span><span class="sxs-lookup"><span data-stu-id="cc14d-3397">photocard licence</span></span> 
- <span data-ttu-id="cc14d-3398">learner drivers</span><span class="sxs-lookup"><span data-stu-id="cc14d-3398">learner drivers</span></span> 
- <span data-ttu-id="cc14d-3399">licence holder</span><span class="sxs-lookup"><span data-stu-id="cc14d-3399">licence holder</span></span> 
- <span data-ttu-id="cc14d-3400">licence holders</span><span class="sxs-lookup"><span data-stu-id="cc14d-3400">licence holders</span></span> 
- <span data-ttu-id="cc14d-3401">driving licences</span><span class="sxs-lookup"><span data-stu-id="cc14d-3401">driving licences</span></span> 
- <span data-ttu-id="cc14d-3402">driving licence</span><span class="sxs-lookup"><span data-stu-id="cc14d-3402">driving licence</span></span> 
- <span data-ttu-id="cc14d-3403">dual control car</span><span class="sxs-lookup"><span data-stu-id="cc14d-3403">dual control car</span></span> 
   
## <a name="uk-electoral-roll-number"></a><span data-ttu-id="cc14d-p142">Número de Título de Eleitor do Reino Unido</span><span class="sxs-lookup"><span data-stu-id="cc14d-p142">U.K. Electoral Roll Number</span></span>

### <a name="format"></a><span data-ttu-id="cc14d-3406">Format</span><span class="sxs-lookup"><span data-stu-id="cc14d-3406">Format</span></span>

<span data-ttu-id="cc14d-3407">Duas letras seguidas por 1 a 4 dígitos</span><span class="sxs-lookup"><span data-stu-id="cc14d-3407">Two letters followed by 1-4 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="cc14d-3408">Padrão</span><span class="sxs-lookup"><span data-stu-id="cc14d-3408">Pattern</span></span>

<span data-ttu-id="cc14d-3409">Duas letras (não diferencia maiúsculas de minúsculas) seguidas de 1 a 4 anos</span><span class="sxs-lookup"><span data-stu-id="cc14d-3409">Two letters (not case sensitive) followed by 1-4 numbers</span></span>

### <a name="checksum"></a><span data-ttu-id="cc14d-3410">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="cc14d-3410">Checksum</span></span>

<span data-ttu-id="cc14d-3411">Não</span><span class="sxs-lookup"><span data-stu-id="cc14d-3411">No</span></span>

### <a name="definition"></a><span data-ttu-id="cc14d-3412">Definição</span><span class="sxs-lookup"><span data-stu-id="cc14d-3412">Definition</span></span>

<span data-ttu-id="cc14d-3413">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="cc14d-3413">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="cc14d-3414">A expressão regular Regex_uk_electoral localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="cc14d-3414">The regular expression Regex_uk_electoral finds content that matches the pattern.</span></span>
- <span data-ttu-id="cc14d-3415">Uma palavra-chave de Keyword_uk_electoral for encontrada.</span><span class="sxs-lookup"><span data-stu-id="cc14d-3415">A keyword from Keyword_uk_electoral is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="cc14d-3416">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="cc14d-3416">Keywords</span></span>

#### <a name="keywordukelectoral"></a><span data-ttu-id="cc14d-3417">Keyword_uk_electoral</span><span class="sxs-lookup"><span data-stu-id="cc14d-3417">Keyword_uk_electoral</span></span>

- <span data-ttu-id="cc14d-3418">council nomination</span><span class="sxs-lookup"><span data-stu-id="cc14d-3418">council nomination</span></span> 
- <span data-ttu-id="cc14d-3419">nomination form</span><span class="sxs-lookup"><span data-stu-id="cc14d-3419">nomination form</span></span> 
- <span data-ttu-id="cc14d-3420">electoral register</span><span class="sxs-lookup"><span data-stu-id="cc14d-3420">electoral register</span></span> 
- <span data-ttu-id="cc14d-3421">electoral roll</span><span class="sxs-lookup"><span data-stu-id="cc14d-3421">electoral roll</span></span>

   
## <a name="uk-national-health-service-number"></a><span data-ttu-id="cc14d-p143">Número do serviço de saúde nacional do Reino Unido</span><span class="sxs-lookup"><span data-stu-id="cc14d-p143">U.K. National Health Service Number</span></span>

### <a name="format"></a><span data-ttu-id="cc14d-3424">Format</span><span class="sxs-lookup"><span data-stu-id="cc14d-3424">Format</span></span>

<span data-ttu-id="cc14d-3425">10 a 17 dígitos separados por espaços</span><span class="sxs-lookup"><span data-stu-id="cc14d-3425">10-17 digits separated by spaces</span></span>

### <a name="pattern"></a><span data-ttu-id="cc14d-3426">Padrão</span><span class="sxs-lookup"><span data-stu-id="cc14d-3426">Pattern</span></span>

<span data-ttu-id="cc14d-3427">10 a 17 dígitos:</span><span class="sxs-lookup"><span data-stu-id="cc14d-3427">10-17 digits:</span></span>
- <span data-ttu-id="cc14d-3428">3 ou 10 dígitos</span><span class="sxs-lookup"><span data-stu-id="cc14d-3428">Either 3 or 10 digits</span></span> 
- <span data-ttu-id="cc14d-3429">Um espaço</span><span class="sxs-lookup"><span data-stu-id="cc14d-3429">A space</span></span> 
- <span data-ttu-id="cc14d-3430">Três dígitos</span><span class="sxs-lookup"><span data-stu-id="cc14d-3430">Three digits</span></span> 
- <span data-ttu-id="cc14d-3431">Um espaço</span><span class="sxs-lookup"><span data-stu-id="cc14d-3431">A space</span></span> 
- <span data-ttu-id="cc14d-3432">Quatro dígitos</span><span class="sxs-lookup"><span data-stu-id="cc14d-3432">Four digits</span></span>

### <a name="checksum"></a><span data-ttu-id="cc14d-3433">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="cc14d-3433">Checksum</span></span>

<span data-ttu-id="cc14d-3434">Sim</span><span class="sxs-lookup"><span data-stu-id="cc14d-3434">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="cc14d-3435">Definição</span><span class="sxs-lookup"><span data-stu-id="cc14d-3435">Definition</span></span>

<span data-ttu-id="cc14d-3436">Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="cc14d-3436">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="cc14d-3437">A função Func_uk_nhs_number localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="cc14d-3437">The function Func_uk_nhs_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="cc14d-3438">Uma das seguintes opções for verdadeira:</span><span class="sxs-lookup"><span data-stu-id="cc14d-3438">One of the following is true:</span></span>
    - <span data-ttu-id="cc14d-3439">Uma palavra-chave de Keyword_uk_nhs_number for encontrada.</span><span class="sxs-lookup"><span data-stu-id="cc14d-3439">A keyword from Keyword_uk_nhs_number is found.</span></span>
    - <span data-ttu-id="cc14d-3440">Uma palavra-chave de Keyword_uk_nhs_number1 for encontrada.</span><span class="sxs-lookup"><span data-stu-id="cc14d-3440">A keyword from Keyword_uk_nhs_number1 is found.</span></span>
    - <span data-ttu-id="cc14d-3441">Uma palavra-chave de Keyword_uk_nhs_number_dob for encontrada.</span><span class="sxs-lookup"><span data-stu-id="cc14d-3441">A keyword from Keyword_uk_nhs_number_dob is found.</span></span>
- <span data-ttu-id="cc14d-3442">A soma de verificação passa.</span><span class="sxs-lookup"><span data-stu-id="cc14d-3442">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="cc14d-3443">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="cc14d-3443">Keywords</span></span>
   
#### <a name="keyworduknhsnumber"></a><span data-ttu-id="cc14d-3444">Keyword_uk_nhs_number</span><span class="sxs-lookup"><span data-stu-id="cc14d-3444">Keyword_uk_nhs_number</span></span>

- <span data-ttu-id="cc14d-3445">national health service</span><span class="sxs-lookup"><span data-stu-id="cc14d-3445">national health service</span></span> 
- <span data-ttu-id="cc14d-3446">NHS</span><span class="sxs-lookup"><span data-stu-id="cc14d-3446">nhs</span></span> 
- <span data-ttu-id="cc14d-3447">health services authority</span><span class="sxs-lookup"><span data-stu-id="cc14d-3447">health services authority</span></span> 
- <span data-ttu-id="cc14d-3448">health authority</span><span class="sxs-lookup"><span data-stu-id="cc14d-3448">health authority</span></span>

#### <a name="keyworduknhsnumber1"></a><span data-ttu-id="cc14d-3449">Keyword_uk_nhs_number1</span><span class="sxs-lookup"><span data-stu-id="cc14d-3449">Keyword_uk_nhs_number1</span></span>

- <span data-ttu-id="cc14d-3450">patient id</span><span class="sxs-lookup"><span data-stu-id="cc14d-3450">patient id</span></span> 
- <span data-ttu-id="cc14d-3451">patient identification</span><span class="sxs-lookup"><span data-stu-id="cc14d-3451">patient identification</span></span> 
- <span data-ttu-id="cc14d-3452">patient no</span><span class="sxs-lookup"><span data-stu-id="cc14d-3452">patient no</span></span> 
- <span data-ttu-id="cc14d-3453">patient number</span><span class="sxs-lookup"><span data-stu-id="cc14d-3453">patient number</span></span>

#### <a name="keyworduknhsnumberdob"></a><span data-ttu-id="cc14d-3454">Keyword_uk_nhs_number_dob</span><span class="sxs-lookup"><span data-stu-id="cc14d-3454">Keyword_uk_nhs_number_dob</span></span>

- <span data-ttu-id="cc14d-3455">GP</span><span class="sxs-lookup"><span data-stu-id="cc14d-3455">GP</span></span> 
- <span data-ttu-id="cc14d-3456">DOB</span><span class="sxs-lookup"><span data-stu-id="cc14d-3456">DOB</span></span> 
- <span data-ttu-id="cc14d-3457">D. O. B</span><span class="sxs-lookup"><span data-stu-id="cc14d-3457">D.O.B</span></span> 
- <span data-ttu-id="cc14d-3458">Date of Birth</span><span class="sxs-lookup"><span data-stu-id="cc14d-3458">Date of Birth</span></span> 
- <span data-ttu-id="cc14d-3459">Birth Date</span><span class="sxs-lookup"><span data-stu-id="cc14d-3459">Birth Date</span></span> 
   
## <a name="uk-national-insurance-number-nino"></a><span data-ttu-id="cc14d-p144">Número de seguro nacional do Reino Unido (NINO)</span><span class="sxs-lookup"><span data-stu-id="cc14d-p144">U.K. National Insurance Number (NINO)</span></span>

### <a name="format"></a><span data-ttu-id="cc14d-3462">Format</span><span class="sxs-lookup"><span data-stu-id="cc14d-3462">Format</span></span>

<span data-ttu-id="cc14d-3463">7 caracteres ou 9 caracteres separados por espaços ou traços</span><span class="sxs-lookup"><span data-stu-id="cc14d-3463">7 characters or 9 characters separated by spaces or dashes</span></span>

### <a name="pattern"></a><span data-ttu-id="cc14d-3464">Padrão</span><span class="sxs-lookup"><span data-stu-id="cc14d-3464">Pattern</span></span>

<span data-ttu-id="cc14d-3465">Dois padrões possíveis:</span><span class="sxs-lookup"><span data-stu-id="cc14d-3465">Two possible patterns:</span></span>

- <span data-ttu-id="cc14d-3466">Duas letras (NINOs válidas usam apenas determinados caracteres neste prefixo, que esse padrão valida; não diferencia maiúsculas de minúsculas)</span><span class="sxs-lookup"><span data-stu-id="cc14d-3466">Two letters (valid NINOs use only certain characters in this prefix, which this pattern validates; not case sensitive)</span></span>
- <span data-ttu-id="cc14d-3467">Seis dígitos</span><span class="sxs-lookup"><span data-stu-id="cc14d-3467">Six digits</span></span>
- <span data-ttu-id="cc14d-3468">"A", "B", "C" ou "(como o prefixo, apenas determinados caracteres são permitidos no sufixo; não diferencia maiúsculas de minúsculas)</span><span class="sxs-lookup"><span data-stu-id="cc14d-3468">Either 'A', 'B', 'C', or 'D' (like the prefix, only certain characters are allowed in the suffix; not case sensitive)</span></span>

<span data-ttu-id="cc14d-3469">OU</span><span class="sxs-lookup"><span data-stu-id="cc14d-3469">OR</span></span>

- <span data-ttu-id="cc14d-3470">Duas letras</span><span class="sxs-lookup"><span data-stu-id="cc14d-3470">Two letters</span></span>
- <span data-ttu-id="cc14d-3471">Um espaço ou um traço</span><span class="sxs-lookup"><span data-stu-id="cc14d-3471">A space or dash</span></span>
- <span data-ttu-id="cc14d-3472">Dois dígitos</span><span class="sxs-lookup"><span data-stu-id="cc14d-3472">Two digits</span></span>
- <span data-ttu-id="cc14d-3473">Um espaço ou um traço</span><span class="sxs-lookup"><span data-stu-id="cc14d-3473">A space or dash</span></span>
- <span data-ttu-id="cc14d-3474">Dois dígitos</span><span class="sxs-lookup"><span data-stu-id="cc14d-3474">Two digits</span></span>
- <span data-ttu-id="cc14d-3475">Um espaço ou um traço</span><span class="sxs-lookup"><span data-stu-id="cc14d-3475">A space or dash</span></span>
- <span data-ttu-id="cc14d-3476">Dois dígitos</span><span class="sxs-lookup"><span data-stu-id="cc14d-3476">Two digits</span></span>
- <span data-ttu-id="cc14d-3477">Um espaço ou um traço</span><span class="sxs-lookup"><span data-stu-id="cc14d-3477">A space or dash</span></span>
- <span data-ttu-id="cc14d-3478">' A ', ' B ', ' C' ou ' d'</span><span class="sxs-lookup"><span data-stu-id="cc14d-3478">Either 'A', 'B', 'C', or 'D'</span></span>

### <a name="checksum"></a><span data-ttu-id="cc14d-3479">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="cc14d-3479">Checksum</span></span>

<span data-ttu-id="cc14d-3480">Não</span><span class="sxs-lookup"><span data-stu-id="cc14d-3480">No</span></span>

### <a name="definition"></a><span data-ttu-id="cc14d-3481">Definição</span><span class="sxs-lookup"><span data-stu-id="cc14d-3481">Definition</span></span>

<span data-ttu-id="cc14d-3482">Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="cc14d-3482">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="cc14d-3483">A função Func_uk_nino localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="cc14d-3483">The function Func_uk_nino finds content that matches the pattern.</span></span>
- <span data-ttu-id="cc14d-3484">Uma palavra-chave de Keyword_uk_nino for encontrada.</span><span class="sxs-lookup"><span data-stu-id="cc14d-3484">A keyword from Keyword_uk_nino is found.</span></span>

<span data-ttu-id="cc14d-3485">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="cc14d-3485">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="cc14d-3486">A função Func_uk_nino localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="cc14d-3486">The function Func_uk_nino finds content that matches the pattern.</span></span>
- <span data-ttu-id="cc14d-3487">Nenhuma palavra-chave de Keyword_uk_nino for encontrada.</span><span class="sxs-lookup"><span data-stu-id="cc14d-3487">No keyword from Keyword_uk_nino is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="cc14d-3488">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="cc14d-3488">Keywords</span></span>

#### <a name="keyworduknino"></a><span data-ttu-id="cc14d-3489">Keyword_uk_nino</span><span class="sxs-lookup"><span data-stu-id="cc14d-3489">Keyword_uk_nino</span></span>

- <span data-ttu-id="cc14d-3490">national insurance number</span><span class="sxs-lookup"><span data-stu-id="cc14d-3490">national insurance number</span></span> 
- <span data-ttu-id="cc14d-3491">national insurance contributions</span><span class="sxs-lookup"><span data-stu-id="cc14d-3491">national insurance contributions</span></span> 
- <span data-ttu-id="cc14d-3492">protection act</span><span class="sxs-lookup"><span data-stu-id="cc14d-3492">protection act</span></span> 
- <span data-ttu-id="cc14d-3493">seguro</span><span class="sxs-lookup"><span data-stu-id="cc14d-3493">insurance</span></span> 
- <span data-ttu-id="cc14d-3494">social security number</span><span class="sxs-lookup"><span data-stu-id="cc14d-3494">social security number</span></span> 
- <span data-ttu-id="cc14d-3495">insurance application</span><span class="sxs-lookup"><span data-stu-id="cc14d-3495">insurance application</span></span> 
- <span data-ttu-id="cc14d-3496">medical application</span><span class="sxs-lookup"><span data-stu-id="cc14d-3496">medical application</span></span> 
- <span data-ttu-id="cc14d-3497">social insurance</span><span class="sxs-lookup"><span data-stu-id="cc14d-3497">social insurance</span></span> 
- <span data-ttu-id="cc14d-3498">medical attention</span><span class="sxs-lookup"><span data-stu-id="cc14d-3498">medical attention</span></span> 
- <span data-ttu-id="cc14d-3499">social security</span><span class="sxs-lookup"><span data-stu-id="cc14d-3499">social security</span></span> 
- <span data-ttu-id="cc14d-3500">great britain</span><span class="sxs-lookup"><span data-stu-id="cc14d-3500">great britain</span></span> 
- <span data-ttu-id="cc14d-3501">seguro</span><span class="sxs-lookup"><span data-stu-id="cc14d-3501">insurance</span></span>    
   
## <a name="us--uk-passport-number"></a><span data-ttu-id="cc14d-p145">Número de passaporte dos EUA/Reino Unido</span><span class="sxs-lookup"><span data-stu-id="cc14d-p145">U.S. / U.K. Passport Number</span></span>

### <a name="format"></a><span data-ttu-id="cc14d-3504">Format</span><span class="sxs-lookup"><span data-stu-id="cc14d-3504">Format</span></span>

<span data-ttu-id="cc14d-3505">Nove dígitos</span><span class="sxs-lookup"><span data-stu-id="cc14d-3505">Nine digits</span></span>

### <a name="pattern"></a><span data-ttu-id="cc14d-3506">Padrão</span><span class="sxs-lookup"><span data-stu-id="cc14d-3506">Pattern</span></span>

<span data-ttu-id="cc14d-3507">Nove dígitos consecutivos</span><span class="sxs-lookup"><span data-stu-id="cc14d-3507">Nine consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="cc14d-3508">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="cc14d-3508">Checksum</span></span>

<span data-ttu-id="cc14d-3509">Não</span><span class="sxs-lookup"><span data-stu-id="cc14d-3509">No</span></span>

### <a name="definition"></a><span data-ttu-id="cc14d-3510">Definição</span><span class="sxs-lookup"><span data-stu-id="cc14d-3510">Definition</span></span>

<span data-ttu-id="cc14d-3511">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="cc14d-3511">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="cc14d-3512">A função Func_usa_uk_passport localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="cc14d-3512">The function Func_usa_uk_passport finds content that matches the pattern.</span></span>
- <span data-ttu-id="cc14d-3513">Uma palavra-chave de Keyword_passport for encontrada.</span><span class="sxs-lookup"><span data-stu-id="cc14d-3513">A keyword from Keyword_passport is found.</span></span>

```
<Entity id="178ec42a-18b4-47cc-85c7-d62c92fd67f8" patternsProximity="300" recommendedConfidence="75">
    <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_usa_uk_passport" />
        <Match idRef="Keyword_passport" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="cc14d-3514">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="cc14d-3514">Keywords</span></span>

#### <a name="keywordpassport"></a><span data-ttu-id="cc14d-3515">Keyword_passport</span><span class="sxs-lookup"><span data-stu-id="cc14d-3515">Keyword_passport</span></span>

- <span data-ttu-id="cc14d-3516">Passport Number</span><span class="sxs-lookup"><span data-stu-id="cc14d-3516">Passport Number</span></span> 
- <span data-ttu-id="cc14d-3517">Passport No</span><span class="sxs-lookup"><span data-stu-id="cc14d-3517">Passport No</span></span> 
- <span data-ttu-id="cc14d-3518">Passport #</span><span class="sxs-lookup"><span data-stu-id="cc14d-3518">Passport #</span></span> 
- <span data-ttu-id="cc14d-3519">Passaport</span><span class="sxs-lookup"><span data-stu-id="cc14d-3519">Passport#</span></span> 
- <span data-ttu-id="cc14d-3520">Passportid</span><span class="sxs-lookup"><span data-stu-id="cc14d-3520">PassportID</span></span> 
- <span data-ttu-id="cc14d-3521">Passportno</span><span class="sxs-lookup"><span data-stu-id="cc14d-3521">Passportno</span></span> 
- <span data-ttu-id="cc14d-3522">passportnumber</span><span class="sxs-lookup"><span data-stu-id="cc14d-3522">passportnumber</span></span> 
- <span data-ttu-id="cc14d-3523">パスポート</span><span class="sxs-lookup"><span data-stu-id="cc14d-3523">パスポート</span></span> 
- <span data-ttu-id="cc14d-3524">パスポート番号</span><span class="sxs-lookup"><span data-stu-id="cc14d-3524">パスポート番号</span></span> 
- <span data-ttu-id="cc14d-3525">パスポートのNum</span><span class="sxs-lookup"><span data-stu-id="cc14d-3525">パスポートのNum</span></span> 
- <span data-ttu-id="cc14d-3526">パスポート #</span><span class="sxs-lookup"><span data-stu-id="cc14d-3526">パスポート＃</span></span> 
- <span data-ttu-id="cc14d-3527">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="cc14d-3527">Numéro de passeport</span></span> 
- <span data-ttu-id="cc14d-3528">Passeport n °</span><span class="sxs-lookup"><span data-stu-id="cc14d-3528">Passeport n °</span></span> 
- <span data-ttu-id="cc14d-3529">Passeport Non</span><span class="sxs-lookup"><span data-stu-id="cc14d-3529">Passeport Non</span></span> 
- <span data-ttu-id="cc14d-3530">Passeport #</span><span class="sxs-lookup"><span data-stu-id="cc14d-3530">Passeport #</span></span> 
- <span data-ttu-id="cc14d-3531">Passeport #</span><span class="sxs-lookup"><span data-stu-id="cc14d-3531">Passeport#</span></span> 
- <span data-ttu-id="cc14d-3532">PasseportNon</span><span class="sxs-lookup"><span data-stu-id="cc14d-3532">PasseportNon</span></span> 
- <span data-ttu-id="cc14d-3533">Passeportn °</span><span class="sxs-lookup"><span data-stu-id="cc14d-3533">Passeportn °</span></span> 
   
## <a name="us-bank-account-number"></a><span data-ttu-id="cc14d-3534">Número de conta bancária dos EUA</span><span class="sxs-lookup"><span data-stu-id="cc14d-3534">U.S. Bank Account Number</span></span>

### <a name="format"></a><span data-ttu-id="cc14d-3535">Format</span><span class="sxs-lookup"><span data-stu-id="cc14d-3535">Format</span></span>

<span data-ttu-id="cc14d-3536">8 a 17 dígitos</span><span class="sxs-lookup"><span data-stu-id="cc14d-3536">8-17 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="cc14d-3537">Padrão</span><span class="sxs-lookup"><span data-stu-id="cc14d-3537">Pattern</span></span>

<span data-ttu-id="cc14d-3538">8 a 17 dígitos consecutivos</span><span class="sxs-lookup"><span data-stu-id="cc14d-3538">8-17 consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="cc14d-3539">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="cc14d-3539">Checksum</span></span>

<span data-ttu-id="cc14d-3540">Não</span><span class="sxs-lookup"><span data-stu-id="cc14d-3540">No</span></span>

### <a name="definition"></a><span data-ttu-id="cc14d-3541">Definição</span><span class="sxs-lookup"><span data-stu-id="cc14d-3541">Definition</span></span>

<span data-ttu-id="cc14d-3542">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="cc14d-3542">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="cc14d-3543">A expressão regular Regex_usa_bank_account_number localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="cc14d-3543">The regular expression Regex_usa_bank_account_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="cc14d-3544">Uma palavra-chave de Keyword_usa_Bank_Account for encontrada.</span><span class="sxs-lookup"><span data-stu-id="cc14d-3544">A keyword from Keyword_usa_Bank_Account is found.</span></span>

```
<!-- U.S. Bank Account Number -->
<Entity id="a2ce32a8-f935-4bb6-8e96-2a5157672e2c" patternsProximity="300" recommendedConfidence="75">
    <Pattern confidenceLevel="75">
        <IdMatch idRef="Regex_usa_bank_account_number" />
        <Match idRef="Keyword_usa_Bank_Account" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="cc14d-3545">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="cc14d-3545">Keywords</span></span>

#### <a name="keywordusabankaccount"></a><span data-ttu-id="cc14d-3546">Keyword_usa_Bank_Account</span><span class="sxs-lookup"><span data-stu-id="cc14d-3546">Keyword_usa_Bank_Account</span></span>

- <span data-ttu-id="cc14d-3547">Checking Account Number</span><span class="sxs-lookup"><span data-stu-id="cc14d-3547">Checking Account Number</span></span> 
- <span data-ttu-id="cc14d-3548">Checking Account</span><span class="sxs-lookup"><span data-stu-id="cc14d-3548">Checking Account</span></span> 
- <span data-ttu-id="cc14d-3549">Checking Account #</span><span class="sxs-lookup"><span data-stu-id="cc14d-3549">Checking Account #</span></span> 
- <span data-ttu-id="cc14d-3550">Checking Acct Number</span><span class="sxs-lookup"><span data-stu-id="cc14d-3550">Checking Acct Number</span></span> 
- <span data-ttu-id="cc14d-3551">Checking Acct #</span><span class="sxs-lookup"><span data-stu-id="cc14d-3551">Checking Acct #</span></span> 
- <span data-ttu-id="cc14d-3552">Checking Acct No.</span><span class="sxs-lookup"><span data-stu-id="cc14d-3552">Checking Acct No.</span></span> 
- <span data-ttu-id="cc14d-3553">Checking Account No.</span><span class="sxs-lookup"><span data-stu-id="cc14d-3553">Checking Account No.</span></span> 
- <span data-ttu-id="cc14d-3554">Bank Account Number</span><span class="sxs-lookup"><span data-stu-id="cc14d-3554">Bank Account Number</span></span> 
- <span data-ttu-id="cc14d-3555">Bank Account #</span><span class="sxs-lookup"><span data-stu-id="cc14d-3555">Bank Account #</span></span> 
- <span data-ttu-id="cc14d-3556">Bank Acct Number</span><span class="sxs-lookup"><span data-stu-id="cc14d-3556">Bank Acct Number</span></span> 
- <span data-ttu-id="cc14d-3557">Bank Acct #</span><span class="sxs-lookup"><span data-stu-id="cc14d-3557">Bank Acct #</span></span> 
- <span data-ttu-id="cc14d-3558">Bank Acct No.</span><span class="sxs-lookup"><span data-stu-id="cc14d-3558">Bank Acct No.</span></span> 
- <span data-ttu-id="cc14d-3559">Bank Account No.</span><span class="sxs-lookup"><span data-stu-id="cc14d-3559">Bank Account No.</span></span> 
- <span data-ttu-id="cc14d-3560">Savings Account Number</span><span class="sxs-lookup"><span data-stu-id="cc14d-3560">Savings Account Number</span></span> 
- <span data-ttu-id="cc14d-3561">Savings Account.</span><span class="sxs-lookup"><span data-stu-id="cc14d-3561">Savings Account.</span></span> 
- <span data-ttu-id="cc14d-3562">Savings Account #</span><span class="sxs-lookup"><span data-stu-id="cc14d-3562">Savings Account #</span></span> 
- <span data-ttu-id="cc14d-3563">Savings Acct Number</span><span class="sxs-lookup"><span data-stu-id="cc14d-3563">Savings Acct Number</span></span> 
- <span data-ttu-id="cc14d-3564">Savings Acct #</span><span class="sxs-lookup"><span data-stu-id="cc14d-3564">Savings Acct #</span></span> 
- <span data-ttu-id="cc14d-3565">Savings Acct No.</span><span class="sxs-lookup"><span data-stu-id="cc14d-3565">Savings Acct No.</span></span> 
- <span data-ttu-id="cc14d-3566">Savings Account No.</span><span class="sxs-lookup"><span data-stu-id="cc14d-3566">Savings Account No.</span></span> 
- <span data-ttu-id="cc14d-3567">Debit Account Number</span><span class="sxs-lookup"><span data-stu-id="cc14d-3567">Debit Account Number</span></span> 
- <span data-ttu-id="cc14d-3568">Debit Account</span><span class="sxs-lookup"><span data-stu-id="cc14d-3568">Debit Account</span></span> 
- <span data-ttu-id="cc14d-3569">Debit Account #</span><span class="sxs-lookup"><span data-stu-id="cc14d-3569">Debit Account #</span></span> 
- <span data-ttu-id="cc14d-3570">Debit Acct Number</span><span class="sxs-lookup"><span data-stu-id="cc14d-3570">Debit Acct Number</span></span> 
- <span data-ttu-id="cc14d-3571">Debit Acct #</span><span class="sxs-lookup"><span data-stu-id="cc14d-3571">Debit Acct #</span></span> 
- <span data-ttu-id="cc14d-3572">Debit Acct No.</span><span class="sxs-lookup"><span data-stu-id="cc14d-3572">Debit Acct No.</span></span> 
- <span data-ttu-id="cc14d-3573">Debit Account No.</span><span class="sxs-lookup"><span data-stu-id="cc14d-3573">Debit Account No.</span></span> 
   
## <a name="us-drivers-license-number"></a><span data-ttu-id="cc14d-3574">Número de carteira de motorista dos EUA</span><span class="sxs-lookup"><span data-stu-id="cc14d-3574">U.S. Driver's License Number</span></span>

### <a name="format"></a><span data-ttu-id="cc14d-3575">Format</span><span class="sxs-lookup"><span data-stu-id="cc14d-3575">Format</span></span>

<span data-ttu-id="cc14d-3576">Depende do estado</span><span class="sxs-lookup"><span data-stu-id="cc14d-3576">Depends on the state</span></span>

### <a name="pattern"></a><span data-ttu-id="cc14d-3577">Padrão</span><span class="sxs-lookup"><span data-stu-id="cc14d-3577">Pattern</span></span>

<span data-ttu-id="cc14d-3578">Depende do estado – por exemplo, Nova York:</span><span class="sxs-lookup"><span data-stu-id="cc14d-3578">Depends on the state -- for example, New York:</span></span>
- <span data-ttu-id="cc14d-3579">Nove dígitos formatados como DDD DDD DDD corresponderão.</span><span class="sxs-lookup"><span data-stu-id="cc14d-3579">Nine digits formatted like ddd ddd ddd will match.</span></span>
- <span data-ttu-id="cc14d-3580">Nove dígitos como ddddddddd não serão correspondentes.</span><span class="sxs-lookup"><span data-stu-id="cc14d-3580">Nine digits like ddddddddd will not match.</span></span>

### <a name="checksum"></a><span data-ttu-id="cc14d-3581">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="cc14d-3581">Checksum</span></span>

<span data-ttu-id="cc14d-3582">Não</span><span class="sxs-lookup"><span data-stu-id="cc14d-3582">No</span></span>

### <a name="definition"></a><span data-ttu-id="cc14d-3583">Definição</span><span class="sxs-lookup"><span data-stu-id="cc14d-3583">Definition</span></span>

<span data-ttu-id="cc14d-3584">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="cc14d-3584">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="cc14d-3585">A função Func_new_york_drivers_license_number localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="cc14d-3585">The function Func_new_york_drivers_license_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="cc14d-3586">Uma palavra-chave de Keyword_[state_name]_drivers_license_name for encontrada.</span><span class="sxs-lookup"><span data-stu-id="cc14d-3586">A keyword from Keyword_[state_name]_drivers_license_name is found.</span></span>
- <span data-ttu-id="cc14d-3587">Uma palavra-chave de Keyword_us_drivers_license for encontrada.</span><span class="sxs-lookup"><span data-stu-id="cc14d-3587">A keyword from Keyword_us_drivers_license is found.</span></span>

<span data-ttu-id="cc14d-3588">Uma política de DLP tem 65% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="cc14d-3588">A DLP policy is 65% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="cc14d-3589">A função Func_new_york_drivers_license_number localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="cc14d-3589">The function Func_new_york_drivers_license_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="cc14d-3590">Uma palavra-chave de Keyword_[state_name]_drivers_license_name for encontrada.</span><span class="sxs-lookup"><span data-stu-id="cc14d-3590">A keyword from Keyword_[state_name]_drivers_license_name is found.</span></span>
- <span data-ttu-id="cc14d-3591">Uma palavra-chave de Keyword_us_drivers_license_abbreviations for encontrada.</span><span class="sxs-lookup"><span data-stu-id="cc14d-3591">A keyword from Keyword_us_drivers_license_abbreviations is found.</span></span>
- <span data-ttu-id="cc14d-3592">Nenhuma palavra-chave de Keyword_us_drivers_license for encontrada.</span><span class="sxs-lookup"><span data-stu-id="cc14d-3592">No keyword from Keyword_us_drivers_license is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="cc14d-3593">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="cc14d-3593">Keywords</span></span>

#### <a name="keywordusdriverslicenseabbreviations"></a><span data-ttu-id="cc14d-3594">Keyword_us_drivers_license_abbreviations</span><span class="sxs-lookup"><span data-stu-id="cc14d-3594">Keyword_us_drivers_license_abbreviations</span></span>

- <span data-ttu-id="cc14d-3595">DISTRIBUIÇÃO</span><span class="sxs-lookup"><span data-stu-id="cc14d-3595">DL</span></span> 
- <span data-ttu-id="cc14d-3596">DL</span><span class="sxs-lookup"><span data-stu-id="cc14d-3596">DLS</span></span> 
- <span data-ttu-id="cc14d-3597">CDL</span><span class="sxs-lookup"><span data-stu-id="cc14d-3597">CDL</span></span> 
- <span data-ttu-id="cc14d-3598">CDLS</span><span class="sxs-lookup"><span data-stu-id="cc14d-3598">CDLS</span></span> 
- <span data-ttu-id="cc14d-3599">ID</span><span class="sxs-lookup"><span data-stu-id="cc14d-3599">ID</span></span> 
- <span data-ttu-id="cc14d-3600">Código</span><span class="sxs-lookup"><span data-stu-id="cc14d-3600">IDs</span></span> 
- <span data-ttu-id="cc14d-3601">DISTRIBUIÇÃO</span><span class="sxs-lookup"><span data-stu-id="cc14d-3601">DL#</span></span> 
- <span data-ttu-id="cc14d-3602">DL</span><span class="sxs-lookup"><span data-stu-id="cc14d-3602">DLS#</span></span> 
- <span data-ttu-id="cc14d-3603">CDL</span><span class="sxs-lookup"><span data-stu-id="cc14d-3603">CDL#</span></span> 
- <span data-ttu-id="cc14d-3604">CDLS #</span><span class="sxs-lookup"><span data-stu-id="cc14d-3604">CDLS#</span></span> 
- <span data-ttu-id="cc14d-3605">ID</span><span class="sxs-lookup"><span data-stu-id="cc14d-3605">ID#</span></span>
- <span data-ttu-id="cc14d-3606">Código</span><span class="sxs-lookup"><span data-stu-id="cc14d-3606">IDs#</span></span> 
- <span data-ttu-id="cc14d-3607">ID number</span><span class="sxs-lookup"><span data-stu-id="cc14d-3607">ID number</span></span> 
- <span data-ttu-id="cc14d-3608">ID numbers</span><span class="sxs-lookup"><span data-stu-id="cc14d-3608">ID numbers</span></span> 
- <span data-ttu-id="cc14d-3609">DRIVER'LIC</span><span class="sxs-lookup"><span data-stu-id="cc14d-3609">LIC</span></span> 
- <span data-ttu-id="cc14d-3610">DRIVER'LIC</span><span class="sxs-lookup"><span data-stu-id="cc14d-3610">LIC#</span></span> 

#### <a name="keywordusdriverslicense"></a><span data-ttu-id="cc14d-3611">Keyword_us_drivers_license</span><span class="sxs-lookup"><span data-stu-id="cc14d-3611">Keyword_us_drivers_license</span></span>

- <span data-ttu-id="cc14d-3612">DriverLic</span><span class="sxs-lookup"><span data-stu-id="cc14d-3612">DriverLic</span></span> 
- <span data-ttu-id="cc14d-3613">DriverLics</span><span class="sxs-lookup"><span data-stu-id="cc14d-3613">DriverLics</span></span> 
- <span data-ttu-id="cc14d-3614">DriverLicense</span><span class="sxs-lookup"><span data-stu-id="cc14d-3614">DriverLicense</span></span> 
- <span data-ttu-id="cc14d-3615">DriverLicenses</span><span class="sxs-lookup"><span data-stu-id="cc14d-3615">DriverLicenses</span></span> 
- <span data-ttu-id="cc14d-3616">Driver Lic</span><span class="sxs-lookup"><span data-stu-id="cc14d-3616">Driver Lic</span></span> 
- <span data-ttu-id="cc14d-3617">Driver Lics</span><span class="sxs-lookup"><span data-stu-id="cc14d-3617">Driver Lics</span></span> 
- <span data-ttu-id="cc14d-3618">Driver License</span><span class="sxs-lookup"><span data-stu-id="cc14d-3618">Driver License</span></span> 
- <span data-ttu-id="cc14d-3619">Driver Licenses</span><span class="sxs-lookup"><span data-stu-id="cc14d-3619">Driver Licenses</span></span> 
- <span data-ttu-id="cc14d-3620">DriversLic</span><span class="sxs-lookup"><span data-stu-id="cc14d-3620">DriversLic</span></span> 
- <span data-ttu-id="cc14d-3621">DriversLics</span><span class="sxs-lookup"><span data-stu-id="cc14d-3621">DriversLics</span></span> 
- <span data-ttu-id="cc14d-3622">DriversLicense</span><span class="sxs-lookup"><span data-stu-id="cc14d-3622">DriversLicense</span></span> 
- <span data-ttu-id="cc14d-3623">DriversLicenses</span><span class="sxs-lookup"><span data-stu-id="cc14d-3623">DriversLicenses</span></span> 
- <span data-ttu-id="cc14d-3624">Drivers Lic</span><span class="sxs-lookup"><span data-stu-id="cc14d-3624">Drivers Lic</span></span> 
- <span data-ttu-id="cc14d-3625">Drivers Lics</span><span class="sxs-lookup"><span data-stu-id="cc14d-3625">Drivers Lics</span></span> 
- <span data-ttu-id="cc14d-3626">Drivers License</span><span class="sxs-lookup"><span data-stu-id="cc14d-3626">Drivers License</span></span> 
- <span data-ttu-id="cc14d-3627">Drivers Licenses</span><span class="sxs-lookup"><span data-stu-id="cc14d-3627">Drivers Licenses</span></span> 
- <span data-ttu-id="cc14d-3628">Driver'Lic</span><span class="sxs-lookup"><span data-stu-id="cc14d-3628">Driver'Lic</span></span> 
- <span data-ttu-id="cc14d-3629">Driver'Lics</span><span class="sxs-lookup"><span data-stu-id="cc14d-3629">Driver'Lics</span></span> 
- <span data-ttu-id="cc14d-3630">Driver'License</span><span class="sxs-lookup"><span data-stu-id="cc14d-3630">Driver'License</span></span> 
- <span data-ttu-id="cc14d-3631">Driver'Licenses</span><span class="sxs-lookup"><span data-stu-id="cc14d-3631">Driver'Licenses</span></span> 
- <span data-ttu-id="cc14d-3632">Driver' Lic</span><span class="sxs-lookup"><span data-stu-id="cc14d-3632">Driver' Lic</span></span> 
- <span data-ttu-id="cc14d-3633">Driver' Lics</span><span class="sxs-lookup"><span data-stu-id="cc14d-3633">Driver' Lics</span></span> 
- <span data-ttu-id="cc14d-3634">Driver' License</span><span class="sxs-lookup"><span data-stu-id="cc14d-3634">Driver' License</span></span> 
- <span data-ttu-id="cc14d-3635">Driver' Licenses</span><span class="sxs-lookup"><span data-stu-id="cc14d-3635">Driver' Licenses</span></span>
- <span data-ttu-id="cc14d-3636">Driver'sLic</span><span class="sxs-lookup"><span data-stu-id="cc14d-3636">Driver'sLic</span></span> 
- <span data-ttu-id="cc14d-3637">Driver'sLics</span><span class="sxs-lookup"><span data-stu-id="cc14d-3637">Driver'sLics</span></span> 
- <span data-ttu-id="cc14d-3638">Driver'sLicense</span><span class="sxs-lookup"><span data-stu-id="cc14d-3638">Driver'sLicense</span></span> 
- <span data-ttu-id="cc14d-3639">Driver'sLicenses</span><span class="sxs-lookup"><span data-stu-id="cc14d-3639">Driver'sLicenses</span></span> 
- <span data-ttu-id="cc14d-3640">Driver's Lic</span><span class="sxs-lookup"><span data-stu-id="cc14d-3640">Driver's Lic</span></span> 
- <span data-ttu-id="cc14d-3641">Driver's Lics</span><span class="sxs-lookup"><span data-stu-id="cc14d-3641">Driver's Lics</span></span> 
- <span data-ttu-id="cc14d-3642">Driver's License</span><span class="sxs-lookup"><span data-stu-id="cc14d-3642">Driver's License</span></span> 
- <span data-ttu-id="cc14d-3643">Driver's Licenses</span><span class="sxs-lookup"><span data-stu-id="cc14d-3643">Driver's Licenses</span></span> 
- <span data-ttu-id="cc14d-3644">identification number</span><span class="sxs-lookup"><span data-stu-id="cc14d-3644">identification number</span></span> 
- <span data-ttu-id="cc14d-3645">identification numbers</span><span class="sxs-lookup"><span data-stu-id="cc14d-3645">identification numbers</span></span> 
- <span data-ttu-id="cc14d-3646">identification #</span><span class="sxs-lookup"><span data-stu-id="cc14d-3646">identification #</span></span> 
- <span data-ttu-id="cc14d-3647">id card</span><span class="sxs-lookup"><span data-stu-id="cc14d-3647">id card</span></span> 
- <span data-ttu-id="cc14d-3648">id cards</span><span class="sxs-lookup"><span data-stu-id="cc14d-3648">id cards</span></span> 
- <span data-ttu-id="cc14d-3649">identification card</span><span class="sxs-lookup"><span data-stu-id="cc14d-3649">identification card</span></span> 
- <span data-ttu-id="cc14d-3650">identification cards</span><span class="sxs-lookup"><span data-stu-id="cc14d-3650">identification cards</span></span> 
- <span data-ttu-id="cc14d-3651">DriverLic #</span><span class="sxs-lookup"><span data-stu-id="cc14d-3651">DriverLic#</span></span> 
- <span data-ttu-id="cc14d-3652">DriverLics #</span><span class="sxs-lookup"><span data-stu-id="cc14d-3652">DriverLics#</span></span> 
- <span data-ttu-id="cc14d-3653">DriverLicense #</span><span class="sxs-lookup"><span data-stu-id="cc14d-3653">DriverLicense#</span></span> 
- <span data-ttu-id="cc14d-3654">DriverLicenses #</span><span class="sxs-lookup"><span data-stu-id="cc14d-3654">DriverLicenses#</span></span> 
- <span data-ttu-id="cc14d-3655">Driver Lic#</span><span class="sxs-lookup"><span data-stu-id="cc14d-3655">Driver Lic#</span></span> 
- <span data-ttu-id="cc14d-3656">Driver Lics#</span><span class="sxs-lookup"><span data-stu-id="cc14d-3656">Driver Lics#</span></span> 
- <span data-ttu-id="cc14d-3657">Driver License#</span><span class="sxs-lookup"><span data-stu-id="cc14d-3657">Driver License#</span></span> 
- <span data-ttu-id="cc14d-3658">Driver Licenses#</span><span class="sxs-lookup"><span data-stu-id="cc14d-3658">Driver Licenses#</span></span> 
- <span data-ttu-id="cc14d-3659">DriversLic #</span><span class="sxs-lookup"><span data-stu-id="cc14d-3659">DriversLic#</span></span> 
- <span data-ttu-id="cc14d-3660">DriversLics #</span><span class="sxs-lookup"><span data-stu-id="cc14d-3660">DriversLics#</span></span> 
- <span data-ttu-id="cc14d-3661">DriversLicense #</span><span class="sxs-lookup"><span data-stu-id="cc14d-3661">DriversLicense#</span></span> 
- <span data-ttu-id="cc14d-3662">DriversLicenses #</span><span class="sxs-lookup"><span data-stu-id="cc14d-3662">DriversLicenses#</span></span> 
- <span data-ttu-id="cc14d-3663">Drivers Lic#</span><span class="sxs-lookup"><span data-stu-id="cc14d-3663">Drivers Lic#</span></span> 
- <span data-ttu-id="cc14d-3664">Drivers Lics#</span><span class="sxs-lookup"><span data-stu-id="cc14d-3664">Drivers Lics#</span></span> 
- <span data-ttu-id="cc14d-3665">Drivers License#</span><span class="sxs-lookup"><span data-stu-id="cc14d-3665">Drivers License#</span></span> 
- <span data-ttu-id="cc14d-3666">Drivers Licenses#</span><span class="sxs-lookup"><span data-stu-id="cc14d-3666">Drivers Licenses#</span></span> 
- <span data-ttu-id="cc14d-3667">Driver'Lic #</span><span class="sxs-lookup"><span data-stu-id="cc14d-3667">Driver'Lic#</span></span> 
- <span data-ttu-id="cc14d-3668">Driver'Lics #</span><span class="sxs-lookup"><span data-stu-id="cc14d-3668">Driver'Lics#</span></span> 
- <span data-ttu-id="cc14d-3669">Driver'License #</span><span class="sxs-lookup"><span data-stu-id="cc14d-3669">Driver'License#</span></span> 
- <span data-ttu-id="cc14d-3670">Driver'Licenses #</span><span class="sxs-lookup"><span data-stu-id="cc14d-3670">Driver'Licenses#</span></span> 
- <span data-ttu-id="cc14d-3671">Driver' Lic#</span><span class="sxs-lookup"><span data-stu-id="cc14d-3671">Driver' Lic#</span></span> 
- <span data-ttu-id="cc14d-3672">Driver' Lics#</span><span class="sxs-lookup"><span data-stu-id="cc14d-3672">Driver' Lics#</span></span> 
- <span data-ttu-id="cc14d-3673">Driver' License#</span><span class="sxs-lookup"><span data-stu-id="cc14d-3673">Driver' License#</span></span> 
- <span data-ttu-id="cc14d-3674">Driver' Licenses#</span><span class="sxs-lookup"><span data-stu-id="cc14d-3674">Driver' Licenses#</span></span> 
- <span data-ttu-id="cc14d-3675">Driver'sLic #</span><span class="sxs-lookup"><span data-stu-id="cc14d-3675">Driver'sLic#</span></span> 
- <span data-ttu-id="cc14d-3676">Driver'sLics #</span><span class="sxs-lookup"><span data-stu-id="cc14d-3676">Driver'sLics#</span></span> 
- <span data-ttu-id="cc14d-3677">Driver'sLicense #</span><span class="sxs-lookup"><span data-stu-id="cc14d-3677">Driver'sLicense#</span></span> 
- <span data-ttu-id="cc14d-3678">Driver'sLicenses #</span><span class="sxs-lookup"><span data-stu-id="cc14d-3678">Driver'sLicenses#</span></span> 
- <span data-ttu-id="cc14d-3679">Driver's Lic#</span><span class="sxs-lookup"><span data-stu-id="cc14d-3679">Driver's Lic#</span></span> 
- <span data-ttu-id="cc14d-3680">Driver's Lics#</span><span class="sxs-lookup"><span data-stu-id="cc14d-3680">Driver's Lics#</span></span> 
- <span data-ttu-id="cc14d-3681">Driver's License#</span><span class="sxs-lookup"><span data-stu-id="cc14d-3681">Driver's License#</span></span> 
- <span data-ttu-id="cc14d-3682">Driver's Licenses#</span><span class="sxs-lookup"><span data-stu-id="cc14d-3682">Driver's Licenses#</span></span> 
- <span data-ttu-id="cc14d-3683">id card#</span><span class="sxs-lookup"><span data-stu-id="cc14d-3683">id card#</span></span> 
- <span data-ttu-id="cc14d-3684">id cards#</span><span class="sxs-lookup"><span data-stu-id="cc14d-3684">id cards#</span></span> 
- <span data-ttu-id="cc14d-3685">identification card#</span><span class="sxs-lookup"><span data-stu-id="cc14d-3685">identification card#</span></span> 
- <span data-ttu-id="cc14d-3686">identification cards#</span><span class="sxs-lookup"><span data-stu-id="cc14d-3686">identification cards#</span></span> 


#### <a name="keywordstatenamedriverslicensename"></a><span data-ttu-id="cc14d-3687">Keyword_ [state_name] _drivers_license_name</span><span class="sxs-lookup"><span data-stu-id="cc14d-3687">Keyword_[state_name]_drivers_license_name</span></span>

- <span data-ttu-id="cc14d-3688">Abreviação do estado (por exemplo, "NY")</span><span class="sxs-lookup"><span data-stu-id="cc14d-3688">State abbreviation (for example, "NY")</span></span> 
- <span data-ttu-id="cc14d-3689">Nome do estado (por exemplo, "Nova York")</span><span class="sxs-lookup"><span data-stu-id="cc14d-3689">State name (for example, "New York")</span></span>    
   
## <a name="us-individual-taxpayer-identification-number-itin"></a><span data-ttu-id="cc14d-3690">Número de identificação de contribuinte individual (ITIN) dos EUA</span><span class="sxs-lookup"><span data-stu-id="cc14d-3690">U.S. Individual Taxpayer Identification Number (ITIN)</span></span>

### <a name="format"></a><span data-ttu-id="cc14d-3691">Format</span><span class="sxs-lookup"><span data-stu-id="cc14d-3691">Format</span></span>

<span data-ttu-id="cc14d-3692">Nove dígitos que começam com "9" e contêm um "7" ou "8" como o quarto dígito, opcionalmente formatado com espaços ou traços</span><span class="sxs-lookup"><span data-stu-id="cc14d-3692">Nine digits that start with a "9" and contain a "7" or "8" as the fourth digit, optionally formatted with spaces or dashes</span></span>

### <a name="pattern"></a><span data-ttu-id="cc14d-3693">Padrão</span><span class="sxs-lookup"><span data-stu-id="cc14d-3693">Pattern</span></span>

<span data-ttu-id="cc14d-3694">Binário</span><span class="sxs-lookup"><span data-stu-id="cc14d-3694">Formatted:</span></span>
- <span data-ttu-id="cc14d-3695">O dígito "9"</span><span class="sxs-lookup"><span data-stu-id="cc14d-3695">The digit "9"</span></span> 
- <span data-ttu-id="cc14d-3696">Dois dígitos</span><span class="sxs-lookup"><span data-stu-id="cc14d-3696">Two digits</span></span> 
- <span data-ttu-id="cc14d-3697">Um espaço ou um traço</span><span class="sxs-lookup"><span data-stu-id="cc14d-3697">A space or dash</span></span> 
- <span data-ttu-id="cc14d-3698">Um "7" ou "8"</span><span class="sxs-lookup"><span data-stu-id="cc14d-3698">A "7" or "8"</span></span> 
- <span data-ttu-id="cc14d-3699">Um dígito</span><span class="sxs-lookup"><span data-stu-id="cc14d-3699">A digit</span></span> 
- <span data-ttu-id="cc14d-3700">Um espaço ou um traço</span><span class="sxs-lookup"><span data-stu-id="cc14d-3700">A space, or dash</span></span> 
- <span data-ttu-id="cc14d-3701">Quatro dígitos</span><span class="sxs-lookup"><span data-stu-id="cc14d-3701">Four digits</span></span>

<span data-ttu-id="cc14d-3702">Não formatado</span><span class="sxs-lookup"><span data-stu-id="cc14d-3702">Unformatted:</span></span>
- <span data-ttu-id="cc14d-3703">O dígito "9"</span><span class="sxs-lookup"><span data-stu-id="cc14d-3703">The digit "9"</span></span> 
- <span data-ttu-id="cc14d-3704">Dois dígitos</span><span class="sxs-lookup"><span data-stu-id="cc14d-3704">Two digits</span></span> 
- <span data-ttu-id="cc14d-3705">Um "7" ou "8"</span><span class="sxs-lookup"><span data-stu-id="cc14d-3705">A "7" or "8"</span></span> 
- <span data-ttu-id="cc14d-3706">Cinco dígitos</span><span class="sxs-lookup"><span data-stu-id="cc14d-3706">Five digits</span></span>

### <a name="checksum"></a><span data-ttu-id="cc14d-3707">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="cc14d-3707">Checksum</span></span>

<span data-ttu-id="cc14d-3708">Não</span><span class="sxs-lookup"><span data-stu-id="cc14d-3708">No</span></span>

### <a name="definition"></a><span data-ttu-id="cc14d-3709">Definição</span><span class="sxs-lookup"><span data-stu-id="cc14d-3709">Definition</span></span>

<span data-ttu-id="cc14d-3710">Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="cc14d-3710">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="cc14d-3711">A função Func_formatted_itin localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="cc14d-3711">The function Func_formatted_itin finds content that matches the pattern.</span></span>
- <span data-ttu-id="cc14d-3712">Pelo menos uma das seguintes opções for verdadeira:</span><span class="sxs-lookup"><span data-stu-id="cc14d-3712">At least one of the following is true:</span></span>
    - <span data-ttu-id="cc14d-3713">Uma palavra-chave de Keyword_itin for encontrada.</span><span class="sxs-lookup"><span data-stu-id="cc14d-3713">A keyword from Keyword_itin is found.</span></span>
    - <span data-ttu-id="cc14d-3714">A função Func_us_address encontrar um endereço no formato de data à direita.</span><span class="sxs-lookup"><span data-stu-id="cc14d-3714">The function Func_us_address finds an address in the right date format.</span></span>
    - <span data-ttu-id="cc14d-3715">A função Func_us_date encontra uma data no formato de data à direita.</span><span class="sxs-lookup"><span data-stu-id="cc14d-3715">The function Func_us_date finds a date in the right date format.</span></span>
    - <span data-ttu-id="cc14d-3716">Uma palavra-chave de Keyword_itin_collaborative for encontrada.</span><span class="sxs-lookup"><span data-stu-id="cc14d-3716">A keyword from Keyword_itin_collaborative is found.</span></span>

<span data-ttu-id="cc14d-3717">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="cc14d-3717">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="cc14d-3718">A função Func_unformatted_itin localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="cc14d-3718">The function Func_unformatted_itin finds content that matches the pattern.</span></span>
- <span data-ttu-id="cc14d-3719">Pelo menos uma das seguintes opções for verdadeira:</span><span class="sxs-lookup"><span data-stu-id="cc14d-3719">At least one of the following is true:</span></span>
    - <span data-ttu-id="cc14d-3720">Uma palavra-chave de Keyword_itin_collaborative for encontrada.</span><span class="sxs-lookup"><span data-stu-id="cc14d-3720">A keyword from Keyword_itin_collaborative is found.</span></span>
    - <span data-ttu-id="cc14d-3721">A função Func_us_address encontrar um endereço no formato de data à direita.</span><span class="sxs-lookup"><span data-stu-id="cc14d-3721">The function Func_us_address finds an address in the right date format.</span></span>
    - <span data-ttu-id="cc14d-3722">A função Func_us_date encontra uma data no formato de data à direita.</span><span class="sxs-lookup"><span data-stu-id="cc14d-3722">The function Func_us_date finds a date in the right date format.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="cc14d-3723">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="cc14d-3723">Keywords</span></span>

#### <a name="keyworditin"></a><span data-ttu-id="cc14d-3724">Keyword_itin</span><span class="sxs-lookup"><span data-stu-id="cc14d-3724">Keyword_itin</span></span>

- <span data-ttu-id="cc14d-3725">contribui</span><span class="sxs-lookup"><span data-stu-id="cc14d-3725">taxpayer</span></span> 
- <span data-ttu-id="cc14d-3726">tax id</span><span class="sxs-lookup"><span data-stu-id="cc14d-3726">tax id</span></span> 
- <span data-ttu-id="cc14d-3727">tax identification</span><span class="sxs-lookup"><span data-stu-id="cc14d-3727">tax identification</span></span> 
- <span data-ttu-id="cc14d-3728">ITIN</span><span class="sxs-lookup"><span data-stu-id="cc14d-3728">itin</span></span> 
- <span data-ttu-id="cc14d-3729">es</span><span class="sxs-lookup"><span data-stu-id="cc14d-3729">ssn</span></span> 
- <span data-ttu-id="cc14d-3730">Tin</span><span class="sxs-lookup"><span data-stu-id="cc14d-3730">tin</span></span> 
- <span data-ttu-id="cc14d-3731">social security</span><span class="sxs-lookup"><span data-stu-id="cc14d-3731">social security</span></span> 
- <span data-ttu-id="cc14d-3732">tax payer</span><span class="sxs-lookup"><span data-stu-id="cc14d-3732">tax payer</span></span> 
- <span data-ttu-id="cc14d-3733">itins</span><span class="sxs-lookup"><span data-stu-id="cc14d-3733">itins</span></span> 
- <span data-ttu-id="cc14d-3734">táxi</span><span class="sxs-lookup"><span data-stu-id="cc14d-3734">taxid</span></span> 
- <span data-ttu-id="cc14d-3735">individual taxpayer</span><span class="sxs-lookup"><span data-stu-id="cc14d-3735">individual taxpayer</span></span> 

#### <a name="keyworditincollaborative"></a><span data-ttu-id="cc14d-3736">Keyword_itin_collaborative</span><span class="sxs-lookup"><span data-stu-id="cc14d-3736">Keyword_itin_collaborative</span></span>

- <span data-ttu-id="cc14d-3737">License</span><span class="sxs-lookup"><span data-stu-id="cc14d-3737">License</span></span> 
- <span data-ttu-id="cc14d-3738">DISTRIBUIÇÃO</span><span class="sxs-lookup"><span data-stu-id="cc14d-3738">DL</span></span> 
- <span data-ttu-id="cc14d-3739">DOB</span><span class="sxs-lookup"><span data-stu-id="cc14d-3739">DOB</span></span> 
- <span data-ttu-id="cc14d-3740">Data de Nascimento</span><span class="sxs-lookup"><span data-stu-id="cc14d-3740">Birthdate</span></span> 
- <span data-ttu-id="cc14d-3741">Aniversário</span><span class="sxs-lookup"><span data-stu-id="cc14d-3741">Birthday</span></span> 
- <span data-ttu-id="cc14d-3742">Date of Birth</span><span class="sxs-lookup"><span data-stu-id="cc14d-3742">Date of Birth</span></span> 
   
## <a name="us-social-security-number-ssn"></a><span data-ttu-id="cc14d-3743">Número de seguridade social dos EUA (SSN)</span><span class="sxs-lookup"><span data-stu-id="cc14d-3743">U.S. Social Security Number (SSN)</span></span>

### <a name="format"></a><span data-ttu-id="cc14d-3744">Format</span><span class="sxs-lookup"><span data-stu-id="cc14d-3744">Format</span></span>

<span data-ttu-id="cc14d-3745">9 dígitos que podem estar em um padrão formatado ou não formatado</span><span class="sxs-lookup"><span data-stu-id="cc14d-3745">9 digits, which may be in a formatted or unformatted pattern</span></span>

> [!NOTE]
> <span data-ttu-id="cc14d-3746">Se emitido antes de meados de 2011, um SSN tem uma formatação forte, onde determinadas partes do número devem estar dentro de determinados intervalos para serem válidos (mas não há nenhum checksum).</span><span class="sxs-lookup"><span data-stu-id="cc14d-3746">If issued before mid-2011, an SSN has strong formatting where certain parts of the number must fall within certain ranges to be valid (but there's no checksum).</span></span>

### <a name="pattern"></a><span data-ttu-id="cc14d-3747">Padrão</span><span class="sxs-lookup"><span data-stu-id="cc14d-3747">Pattern</span></span>

<span data-ttu-id="cc14d-3748">Quatro funções procuram CPFs em quatro padrões diferentes:</span><span class="sxs-lookup"><span data-stu-id="cc14d-3748">Four functions look for SSNs in four different patterns:</span></span>
- <span data-ttu-id="cc14d-3749">Func_ssn localiza CPFs com uma formatação forte de 2011 formatada com traços ou espaços (DDD-DD-dddd ou DDD DD dddd)</span><span class="sxs-lookup"><span data-stu-id="cc14d-3749">Func_ssn finds SSNs with pre-2011 strong formatting that are formatted with dashes or spaces (ddd-dd-dddd OR ddd dd dddd)</span></span>
- <span data-ttu-id="cc14d-3750">Func_unformatted_ssn localiza o CPFs com uma formatação forte de 2011 que não são formatados como nove dígitos consecutivos (ddddddddd)</span><span class="sxs-lookup"><span data-stu-id="cc14d-3750">Func_unformatted_ssn finds SSNs with pre-2011 strong formatting that are unformatted as nine consecutive digits (ddddddddd)</span></span>
- <span data-ttu-id="cc14d-3751">Func_randomized_formatted_ssn localiza o post-2011 CPFs que são formatados com traços ou espaços (DDD-DD-dddd ou DDD DD dddd)</span><span class="sxs-lookup"><span data-stu-id="cc14d-3751">Func_randomized_formatted_ssn finds post-2011 SSNs that are formatted with dashes or spaces (ddd-dd-dddd OR ddd dd dddd)</span></span>
- <span data-ttu-id="cc14d-3752">Func_randomized_unformatted_ssn localiza o post-2011 CPFs que não estão formatados como nove dígitos consecutivos (ddddddddd)</span><span class="sxs-lookup"><span data-stu-id="cc14d-3752">Func_randomized_unformatted_ssn finds post-2011 SSNs that are unformatted as nine consecutive digits (ddddddddd)</span></span>

### <a name="checksum"></a><span data-ttu-id="cc14d-3753">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="cc14d-3753">Checksum</span></span>

<span data-ttu-id="cc14d-3754">Não</span><span class="sxs-lookup"><span data-stu-id="cc14d-3754">No</span></span>


### <a name="definition"></a><span data-ttu-id="cc14d-3755">Definição</span><span class="sxs-lookup"><span data-stu-id="cc14d-3755">Definition</span></span>

<span data-ttu-id="cc14d-3756">Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="cc14d-3756">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="cc14d-3757">A função Func_ssn localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="cc14d-3757">The function Func_ssn finds content that matches the pattern.</span></span>
- <span data-ttu-id="cc14d-3758">Uma palavra-chave de Keyword_ssn for encontrada.</span><span class="sxs-lookup"><span data-stu-id="cc14d-3758">A keyword from Keyword_ssn is found.</span></span>

<span data-ttu-id="cc14d-3759">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="cc14d-3759">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="cc14d-3760">A função Func_unformatted_ssn localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="cc14d-3760">The function Func_unformatted_ssn finds content that matches the pattern.</span></span>
- <span data-ttu-id="cc14d-3761">Uma palavra-chave de Keyword_ssn for encontrada.</span><span class="sxs-lookup"><span data-stu-id="cc14d-3761">A keyword from Keyword_ssn is found.</span></span>

<span data-ttu-id="cc14d-3762">Uma política de DLP tem 65% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="cc14d-3762">A DLP policy is 65% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="cc14d-3763">A função Func_randomized_formatted_ssn localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="cc14d-3763">The function Func_randomized_formatted_ssn finds content that matches the pattern.</span></span>
- <span data-ttu-id="cc14d-3764">Uma palavra-chave de Keyword_ssn for encontrada.</span><span class="sxs-lookup"><span data-stu-id="cc14d-3764">A keyword from Keyword_ssn is found.</span></span>
- <span data-ttu-id="cc14d-3765">A função Func_ssn não localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="cc14d-3765">The function Func_ssn does not find content that matches the pattern.</span></span>

<span data-ttu-id="cc14d-3766">Uma política de DLP tem 55% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="cc14d-3766">A DLP policy is 55% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="cc14d-3767">A função Func_randomized_unformatted_ssn localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="cc14d-3767">The function Func_randomized_unformatted_ssn finds content that matches the pattern.</span></span>
- <span data-ttu-id="cc14d-3768">Uma palavra-chave de Keyword_ssn for encontrada.</span><span class="sxs-lookup"><span data-stu-id="cc14d-3768">A keyword from Keyword_ssn is found.</span></span>
- <span data-ttu-id="cc14d-3769">A função Func_unformatted_ssn não localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="cc14d-3769">The function Func_unformatted_ssn does not find content that matches the pattern.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="cc14d-3770">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="cc14d-3770">Keywords</span></span>

#### <a name="keywordssn"></a><span data-ttu-id="cc14d-3771">Keyword_ssn</span><span class="sxs-lookup"><span data-stu-id="cc14d-3771">Keyword_ssn</span></span>

- <span data-ttu-id="cc14d-3772">Social Security</span><span class="sxs-lookup"><span data-stu-id="cc14d-3772">Social Security</span></span> 
- <span data-ttu-id="cc14d-3773">Social Security#</span><span class="sxs-lookup"><span data-stu-id="cc14d-3773">Social Security#</span></span> 
- <span data-ttu-id="cc14d-3774">Soc Sec</span><span class="sxs-lookup"><span data-stu-id="cc14d-3774">Soc Sec</span></span> 
- <span data-ttu-id="cc14d-3775">ES</span><span class="sxs-lookup"><span data-stu-id="cc14d-3775">SSN</span></span> 
- <span data-ttu-id="cc14d-3776">CPFs</span><span class="sxs-lookup"><span data-stu-id="cc14d-3776">SSNS</span></span> 
- <span data-ttu-id="cc14d-3777">ES</span><span class="sxs-lookup"><span data-stu-id="cc14d-3777">SSN#</span></span> 
- <span data-ttu-id="cc14d-3778">PLANILHA</span><span class="sxs-lookup"><span data-stu-id="cc14d-3778">SS#</span></span> 
- <span data-ttu-id="cc14d-3779">SSID</span><span class="sxs-lookup"><span data-stu-id="cc14d-3779">SSID</span></span> 
   

