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
ms.openlocfilehash: 55fa8b6855a9a5bf2c84f6555dd8c8227a2ad9cf
ms.sourcegitcommit: 6aa82374eef09d2c1921f93bda3eabeeb28aadeb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/06/2019
ms.locfileid: "30455263"
---
# <a name="what-the-sensitive-information-types-look-for"></a><span data-ttu-id="21a8c-104">O que os tipos de informações confidenciais procuram</span><span class="sxs-lookup"><span data-stu-id="21a8c-104">What the sensitive information types look for</span></span>

<span data-ttu-id="21a8c-105">A prevenção de perda de dados (DLP) no centro &amp; de conformidade de segurança do Office 365 inclui muitos tipos de informações confidenciais que estão prontos para uso nas suas políticas de DLP.</span><span class="sxs-lookup"><span data-stu-id="21a8c-105">Data loss prevention (DLP) in the Office 365 Security &amp; Compliance Center includes many sensitive information types that are ready for you to use in your DLP policies.</span></span> <span data-ttu-id="21a8c-106">Este tópico lista todos os tipos de informações confidenciais e mostra o que uma política de DLP procura ao detectar cada tipo.</span><span class="sxs-lookup"><span data-stu-id="21a8c-106">This topic lists all of these sensitive information types and shows what a DLP policy looks for when it detects each type.</span></span> <span data-ttu-id="21a8c-107">Um tipo de informação confidencial é definido por um padrão que pode ser identificado por uma função ou uma expressão regular.</span><span class="sxs-lookup"><span data-stu-id="21a8c-107">A sensitive information type is defined by a pattern that can be identified by a regular expression or a function.</span></span> <span data-ttu-id="21a8c-108">Além disso, evidências corroborativas, como palavras-chave e somas de verificação, podem ser usadas para identificar um tipo de informação confidencial.</span><span class="sxs-lookup"><span data-stu-id="21a8c-108">In addition, corroborative evidence such as keywords and checksums can be used to identify a sensitive information type.</span></span> <span data-ttu-id="21a8c-109">O nível de confiança e a proximidade também são usados no processo de avaliação.</span><span class="sxs-lookup"><span data-stu-id="21a8c-109">Confidence level and proximity are also used in the evaluation process.</span></span>
  
## <a name="aba-routing-number"></a><span data-ttu-id="21a8c-110">Número de roteamento ABA</span><span class="sxs-lookup"><span data-stu-id="21a8c-110">ABA Routing Number</span></span>

### <a name="format"></a><span data-ttu-id="21a8c-111">Format</span><span class="sxs-lookup"><span data-stu-id="21a8c-111">Format</span></span>

<span data-ttu-id="21a8c-112">9 dígitos que podem estar em um padrão formatado ou não formatado</span><span class="sxs-lookup"><span data-stu-id="21a8c-112">9 digits which may be in a formatted or unformatted pattern</span></span>

### <a name="pattern"></a><span data-ttu-id="21a8c-113">Padrão</span><span class="sxs-lookup"><span data-stu-id="21a8c-113">Pattern</span></span>

<span data-ttu-id="21a8c-114">Binário</span><span class="sxs-lookup"><span data-stu-id="21a8c-114">Formatted:</span></span>
- <span data-ttu-id="21a8c-115">Quatro dígitos, começando com 0, 1, 2, 3, 6, 7 ou 8</span><span class="sxs-lookup"><span data-stu-id="21a8c-115">Four digits beginning with 0, 1, 2, 3, 6, 7, or 8</span></span>
- <span data-ttu-id="21a8c-116">Um hífen</span><span class="sxs-lookup"><span data-stu-id="21a8c-116">A hyphen</span></span>
- <span data-ttu-id="21a8c-117">Quatro dígitos</span><span class="sxs-lookup"><span data-stu-id="21a8c-117">Four digits</span></span>
- <span data-ttu-id="21a8c-118">Um hífen</span><span class="sxs-lookup"><span data-stu-id="21a8c-118">A hyphen</span></span>
- <span data-ttu-id="21a8c-119">Um dígito</span><span class="sxs-lookup"><span data-stu-id="21a8c-119">A digit</span></span>

<span data-ttu-id="21a8c-120">Não formatado: 9 dígitos consecutivos começando com 0, 1, 2, 3, 6, 7 ou 8</span><span class="sxs-lookup"><span data-stu-id="21a8c-120">Unformatted: 9 consecutive digits beginning with 0, 1, 2, 3, 6, 7, or 8</span></span> 

### <a name="checksum"></a><span data-ttu-id="21a8c-121">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="21a8c-121">Checksum</span></span>

<span data-ttu-id="21a8c-122">Não</span><span class="sxs-lookup"><span data-stu-id="21a8c-122">No</span></span>

### <a name="definition"></a><span data-ttu-id="21a8c-123">Definição</span><span class="sxs-lookup"><span data-stu-id="21a8c-123">Definition</span></span>

<span data-ttu-id="21a8c-124">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="21a8c-124">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="21a8c-125">A função Func_aba_routing localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="21a8c-125">The function Func_aba_routing finds content that matches the pattern.</span></span>
- <span data-ttu-id="21a8c-126">Uma palavra-chave de Keyword_ABA_Routing for encontrada.</span><span class="sxs-lookup"><span data-stu-id="21a8c-126">A keyword from Keyword_ABA_Routing is found.</span></span>

```
<!-- ABA Routing Number -->
<Entity id="cb353f78-2b72-4c3c-8827-92ebe4f69fdf" patternsProximity="300" recommendedConfidence="75">
      <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_aba_routing" />
        <Match idRef="Keyword_ABA_Routing" />
      </Pattern>
 </Entity>
```


### <a name="keywords"></a><span data-ttu-id="21a8c-127">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="21a8c-127">Keywords</span></span>

#### <a name="keywordabarouting"></a><span data-ttu-id="21a8c-128">Keyword_ABA_Routing</span><span class="sxs-lookup"><span data-stu-id="21a8c-128">Keyword_ABA_Routing</span></span>

- <span data-ttu-id="21a8c-129">aba</span><span class="sxs-lookup"><span data-stu-id="21a8c-129">aba</span></span>
- <span data-ttu-id="21a8c-130">aba #</span><span class="sxs-lookup"><span data-stu-id="21a8c-130">aba #</span></span>
- <span data-ttu-id="21a8c-131">aba routing #</span><span class="sxs-lookup"><span data-stu-id="21a8c-131">aba routing #</span></span>
- <span data-ttu-id="21a8c-132">aba routing number</span><span class="sxs-lookup"><span data-stu-id="21a8c-132">aba routing number</span></span>
- <span data-ttu-id="21a8c-133">aba #</span><span class="sxs-lookup"><span data-stu-id="21a8c-133">aba#</span></span>
- <span data-ttu-id="21a8c-134">abarouting #</span><span class="sxs-lookup"><span data-stu-id="21a8c-134">abarouting#</span></span>
- <span data-ttu-id="21a8c-135">aba number</span><span class="sxs-lookup"><span data-stu-id="21a8c-135">aba number</span></span>
- <span data-ttu-id="21a8c-136">abaroutingnumber</span><span class="sxs-lookup"><span data-stu-id="21a8c-136">abaroutingnumber</span></span>
- <span data-ttu-id="21a8c-137">american bank association routing #</span><span class="sxs-lookup"><span data-stu-id="21a8c-137">american bank association routing #</span></span>
- <span data-ttu-id="21a8c-138">american bank association routing number</span><span class="sxs-lookup"><span data-stu-id="21a8c-138">american bank association routing number</span></span>
- <span data-ttu-id="21a8c-139">americanbankassociationrouting #</span><span class="sxs-lookup"><span data-stu-id="21a8c-139">americanbankassociationrouting#</span></span>
- <span data-ttu-id="21a8c-140">americanbankassociationroutingnumber</span><span class="sxs-lookup"><span data-stu-id="21a8c-140">americanbankassociationroutingnumber</span></span>
- <span data-ttu-id="21a8c-141">bank routing number</span><span class="sxs-lookup"><span data-stu-id="21a8c-141">bank routing number</span></span>
- <span data-ttu-id="21a8c-142">bankrouting #</span><span class="sxs-lookup"><span data-stu-id="21a8c-142">bankrouting#</span></span>
- <span data-ttu-id="21a8c-143">bankroutingnumber</span><span class="sxs-lookup"><span data-stu-id="21a8c-143">bankroutingnumber</span></span>
- <span data-ttu-id="21a8c-144">routing transit number</span><span class="sxs-lookup"><span data-stu-id="21a8c-144">routing transit number</span></span>
- <span data-ttu-id="21a8c-145">RTN</span><span class="sxs-lookup"><span data-stu-id="21a8c-145">RTN</span></span> 
   
## <a name="argentina-national-identity-dni-number"></a><span data-ttu-id="21a8c-146">Número de Identidade Nacional (DNI) da Argentina</span><span class="sxs-lookup"><span data-stu-id="21a8c-146">Argentina National Identity (DNI) Number</span></span>

### <a name="format"></a><span data-ttu-id="21a8c-147">Format</span><span class="sxs-lookup"><span data-stu-id="21a8c-147">Format</span></span>

<span data-ttu-id="21a8c-148">Oito dígitos separados por pontos</span><span class="sxs-lookup"><span data-stu-id="21a8c-148">Eight digits separated by periods</span></span>

### <a name="pattern"></a><span data-ttu-id="21a8c-149">Padrão</span><span class="sxs-lookup"><span data-stu-id="21a8c-149">Pattern</span></span>

<span data-ttu-id="21a8c-150">Oito dígitos:</span><span class="sxs-lookup"><span data-stu-id="21a8c-150">Eight digits:</span></span>
- <span data-ttu-id="21a8c-151">Dois dígitos</span><span class="sxs-lookup"><span data-stu-id="21a8c-151">Two digits</span></span>
- <span data-ttu-id="21a8c-152">Um ponto </span><span class="sxs-lookup"><span data-stu-id="21a8c-152">A period</span></span>
- <span data-ttu-id="21a8c-153">Três dígitos</span><span class="sxs-lookup"><span data-stu-id="21a8c-153">Three digits</span></span>
- <span data-ttu-id="21a8c-154">Um ponto </span><span class="sxs-lookup"><span data-stu-id="21a8c-154">A period</span></span>
- <span data-ttu-id="21a8c-155">Três dígitos</span><span class="sxs-lookup"><span data-stu-id="21a8c-155">Three digits</span></span>

### <a name="checksum"></a><span data-ttu-id="21a8c-156">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="21a8c-156">Checksum</span></span>

<span data-ttu-id="21a8c-157">Não</span><span class="sxs-lookup"><span data-stu-id="21a8c-157">No</span></span>

### <a name="definition"></a><span data-ttu-id="21a8c-158">Definição</span><span class="sxs-lookup"><span data-stu-id="21a8c-158">Definition</span></span>

<span data-ttu-id="21a8c-159">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="21a8c-159">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="21a8c-160">A expressão regular Regex_argentina_national_id localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="21a8c-160">The regular expression Regex_argentina_national_id finds content that matches the pattern.</span></span>
- <span data-ttu-id="21a8c-161">Uma palavra-chave de Keyword_argentina_national_id for encontrada.</span><span class="sxs-lookup"><span data-stu-id="21a8c-161">A keyword from Keyword_argentina_national_id is found.</span></span>

```
<!-- Argentina National Identity (DNI) Number -->
<Entity id="eefbb00e-8282-433c-8620-8f1da3bffdb2" recommendedConfidence="75" patternsProximity="300">
   <Pattern confidenceLevel="75">
      <IdMatch idRef="Regex_argentina_national_id"/>
      <Match idRef="Keyword_argentina_national_id"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="21a8c-162">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="21a8c-162">Keywords</span></span>

#### <a name="keywordargentinanationalid"></a><span data-ttu-id="21a8c-163">Keyword_argentina_national_id</span><span class="sxs-lookup"><span data-stu-id="21a8c-163">Keyword_argentina_national_id</span></span>

- <span data-ttu-id="21a8c-164">Número de Identidade Nacional da Argentina</span><span class="sxs-lookup"><span data-stu-id="21a8c-164">Argentina National Identity number</span></span> 
- <span data-ttu-id="21a8c-165">Identidade</span><span class="sxs-lookup"><span data-stu-id="21a8c-165">Identity</span></span> 
- <span data-ttu-id="21a8c-166">Identificar cartão de identidade nacional</span><span class="sxs-lookup"><span data-stu-id="21a8c-166">Identification National Identity Card</span></span> 
- <span data-ttu-id="21a8c-167">DNI</span><span class="sxs-lookup"><span data-stu-id="21a8c-167">DNI</span></span> 
- <span data-ttu-id="21a8c-168">Registro Nacional de pessoas da NIC</span><span class="sxs-lookup"><span data-stu-id="21a8c-168">NIC National Registry of Persons</span></span> 
- <span data-ttu-id="21a8c-169">Documento Nacional de Identidad</span><span class="sxs-lookup"><span data-stu-id="21a8c-169">Documento Nacional de Identidad</span></span> 
- <span data-ttu-id="21a8c-170">Registro Nacional de las Personas</span><span class="sxs-lookup"><span data-stu-id="21a8c-170">Registro Nacional de las Personas</span></span> 
- <span data-ttu-id="21a8c-171">Identidad</span><span class="sxs-lookup"><span data-stu-id="21a8c-171">Identidad</span></span> 
- <span data-ttu-id="21a8c-172">Identificación</span><span class="sxs-lookup"><span data-stu-id="21a8c-172">Identificación</span></span> 
   
## <a name="australia-bank-account-number"></a><span data-ttu-id="21a8c-173">Número de conta de banco da Austrália</span><span class="sxs-lookup"><span data-stu-id="21a8c-173">Australia Bank Account Number</span></span>

### <a name="format"></a><span data-ttu-id="21a8c-174">Format</span><span class="sxs-lookup"><span data-stu-id="21a8c-174">Format</span></span>

<span data-ttu-id="21a8c-175">6 a 10 dígitos com ou sem um número BSB</span><span class="sxs-lookup"><span data-stu-id="21a8c-175">6-10 digits with or without a bank state branch number</span></span>

### <a name="pattern"></a><span data-ttu-id="21a8c-176">Padrão</span><span class="sxs-lookup"><span data-stu-id="21a8c-176">Pattern</span></span>

<span data-ttu-id="21a8c-177">Número de conta é 6 de 10 dígitos.</span><span class="sxs-lookup"><span data-stu-id="21a8c-177">Account number is 6-10 digits.</span></span>
<span data-ttu-id="21a8c-178">Número BSB da Austrália:</span><span class="sxs-lookup"><span data-stu-id="21a8c-178">Australia bank state branch number:</span></span>
- <span data-ttu-id="21a8c-179">Três dígitos</span><span class="sxs-lookup"><span data-stu-id="21a8c-179">Three digits</span></span> 
- <span data-ttu-id="21a8c-180">Um hífen</span><span class="sxs-lookup"><span data-stu-id="21a8c-180">A hyphen</span></span> 
- <span data-ttu-id="21a8c-181">Três dígitos</span><span class="sxs-lookup"><span data-stu-id="21a8c-181">Three digits</span></span>

### <a name="checksum"></a><span data-ttu-id="21a8c-182">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="21a8c-182">Checksum</span></span>

<span data-ttu-id="21a8c-183">Não</span><span class="sxs-lookup"><span data-stu-id="21a8c-183">No</span></span>

### <a name="definition"></a><span data-ttu-id="21a8c-184">Definição</span><span class="sxs-lookup"><span data-stu-id="21a8c-184">Definition</span></span>

<span data-ttu-id="21a8c-185">Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="21a8c-185">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="21a8c-186">A expressão regular Regex_australia_bank_account_number localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="21a8c-186">The regular expression Regex_australia_bank_account_number finds content that matches the pattern..</span></span>
- <span data-ttu-id="21a8c-187">Uma palavra-chave de Keyword_australia_bank_account_number for encontrada.</span><span class="sxs-lookup"><span data-stu-id="21a8c-187">A keyword from Keyword_australia_bank_account_number is found.</span></span>
- <span data-ttu-id="21a8c-188">A expressão regular Regex_australia_bank_account_number_bsb localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="21a8c-188">The regular expression Regex_australia_bank_account_number_bsb finds content that matches the pattern.</span></span>

<span data-ttu-id="21a8c-189">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="21a8c-189">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="21a8c-190">A expressão regular Regex_australia_bank_account_number localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="21a8c-190">The regular expression Regex_australia_bank_account_number finds content that matches the pattern..</span></span>
- <span data-ttu-id="21a8c-191">Uma palavra-chave de Keyword_australia_bank_account_number for encontrada.</span><span class="sxs-lookup"><span data-stu-id="21a8c-191">A keyword from Keyword_australia_bank_account_number is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="21a8c-192">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="21a8c-192">Keywords</span></span>

#### <a name="keywordaustraliabankaccountnumber"></a><span data-ttu-id="21a8c-193">Keyword_australia_bank_account_number</span><span class="sxs-lookup"><span data-stu-id="21a8c-193">Keyword_australia_bank_account_number</span></span>

- <span data-ttu-id="21a8c-194">swift bank code</span><span class="sxs-lookup"><span data-stu-id="21a8c-194">swift bank code</span></span>
- <span data-ttu-id="21a8c-195">correspondent bank</span><span class="sxs-lookup"><span data-stu-id="21a8c-195">correspondent bank</span></span>
- <span data-ttu-id="21a8c-196">base currency</span><span class="sxs-lookup"><span data-stu-id="21a8c-196">base currency</span></span>
- <span data-ttu-id="21a8c-197">usa account</span><span class="sxs-lookup"><span data-stu-id="21a8c-197">usa account</span></span>
- <span data-ttu-id="21a8c-198">holder address</span><span class="sxs-lookup"><span data-stu-id="21a8c-198">holder address</span></span>
- <span data-ttu-id="21a8c-199">bank address</span><span class="sxs-lookup"><span data-stu-id="21a8c-199">bank address</span></span>
- <span data-ttu-id="21a8c-200">information account</span><span class="sxs-lookup"><span data-stu-id="21a8c-200">information account</span></span>
- <span data-ttu-id="21a8c-201">fund transfers</span><span class="sxs-lookup"><span data-stu-id="21a8c-201">fund transfers</span></span>
- <span data-ttu-id="21a8c-202">bank charges</span><span class="sxs-lookup"><span data-stu-id="21a8c-202">bank charges</span></span>
- <span data-ttu-id="21a8c-203">bank details</span><span class="sxs-lookup"><span data-stu-id="21a8c-203">bank details</span></span>
- <span data-ttu-id="21a8c-204">banking information</span><span class="sxs-lookup"><span data-stu-id="21a8c-204">banking information</span></span>
- <span data-ttu-id="21a8c-205">full names</span><span class="sxs-lookup"><span data-stu-id="21a8c-205">full names</span></span>
- <span data-ttu-id="21a8c-206">IAEA</span><span class="sxs-lookup"><span data-stu-id="21a8c-206">iaea</span></span>

   
## <a name="australia-drivers-license-number"></a><span data-ttu-id="21a8c-207">Número de carteira de motorista da Austrália</span><span class="sxs-lookup"><span data-stu-id="21a8c-207">Australia Driver's License Number</span></span>

### <a name="format"></a><span data-ttu-id="21a8c-208">Format</span><span class="sxs-lookup"><span data-stu-id="21a8c-208">Format</span></span>

<span data-ttu-id="21a8c-209">Nove letras e dígitos</span><span class="sxs-lookup"><span data-stu-id="21a8c-209">Nine letters and digits</span></span>

### <a name="pattern"></a><span data-ttu-id="21a8c-210">Padrão</span><span class="sxs-lookup"><span data-stu-id="21a8c-210">Pattern</span></span>

<span data-ttu-id="21a8c-211">Nove letras e dígitos:</span><span class="sxs-lookup"><span data-stu-id="21a8c-211">Nine letters and digits:</span></span> 

- <span data-ttu-id="21a8c-212">Dois dígitos ou letras (não diferenciam maiúsculas de minúsculas)</span><span class="sxs-lookup"><span data-stu-id="21a8c-212">Two digits or letters (not case sensitive)</span></span> 
- <span data-ttu-id="21a8c-213">Dois dígitos</span><span class="sxs-lookup"><span data-stu-id="21a8c-213">Two digits</span></span> 
- <span data-ttu-id="21a8c-214">Cinco dígitos ou letras (não diferenciam maiúsculas de minúsculas)</span><span class="sxs-lookup"><span data-stu-id="21a8c-214">Five digits or letters (not case sensitive)</span></span>

<span data-ttu-id="21a8c-215">OU</span><span class="sxs-lookup"><span data-stu-id="21a8c-215">OR</span></span>

- <span data-ttu-id="21a8c-216">1 a 2 letras opcionais (não diferenciam maiúsculas de minúsculas)</span><span class="sxs-lookup"><span data-stu-id="21a8c-216">1-2 optional letters (not case sensitive)</span></span> 
- <span data-ttu-id="21a8c-217">4 a 9 dígitos</span><span class="sxs-lookup"><span data-stu-id="21a8c-217">4-9 digits</span></span>

<span data-ttu-id="21a8c-218">OU</span><span class="sxs-lookup"><span data-stu-id="21a8c-218">OR</span></span>

- <span data-ttu-id="21a8c-219">Nove dígitos ou letras (não diferenciam maiúsculas de minúsculas)</span><span class="sxs-lookup"><span data-stu-id="21a8c-219">Nine digits or letters (not case sensitive)</span></span>

### <a name="checksum"></a><span data-ttu-id="21a8c-220">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="21a8c-220">Checksum</span></span>

<span data-ttu-id="21a8c-221">Não</span><span class="sxs-lookup"><span data-stu-id="21a8c-221">No</span></span>

### <a name="definition"></a><span data-ttu-id="21a8c-222">Definição</span><span class="sxs-lookup"><span data-stu-id="21a8c-222">Definition</span></span>

<span data-ttu-id="21a8c-223">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="21a8c-223">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="21a8c-224">A expressão regular Regex_australia_drivers_license_number localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="21a8c-224">The regular expression Regex_australia_drivers_license_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="21a8c-225">Uma palavra-chave de Keyword_australia_drivers_license_number for encontrada.</span><span class="sxs-lookup"><span data-stu-id="21a8c-225">A keyword from Keyword_australia_drivers_license_number is found.</span></span>
- <span data-ttu-id="21a8c-226">Nenhuma palavra-chave de Keyword_australia_drivers_license_number_exclusions for encontrada.</span><span class="sxs-lookup"><span data-stu-id="21a8c-226">No keyword from Keyword_australia_drivers_license_number_exclusions is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="21a8c-227">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="21a8c-227">Keywords</span></span>

#### <a name="keywordaustraliadriverslicensenumber"></a><span data-ttu-id="21a8c-228">Keyword_australia_drivers_license_number</span><span class="sxs-lookup"><span data-stu-id="21a8c-228">Keyword_australia_drivers_license_number</span></span>

- <span data-ttu-id="21a8c-229">international driving permits</span><span class="sxs-lookup"><span data-stu-id="21a8c-229">international driving permits</span></span>
- <span data-ttu-id="21a8c-230">australian automobile association</span><span class="sxs-lookup"><span data-stu-id="21a8c-230">australian automobile association</span></span>
- <span data-ttu-id="21a8c-231">international driving permit</span><span class="sxs-lookup"><span data-stu-id="21a8c-231">international driving permit</span></span>
- <span data-ttu-id="21a8c-232">DriverLicence</span><span class="sxs-lookup"><span data-stu-id="21a8c-232">DriverLicence</span></span>
- <span data-ttu-id="21a8c-233">DriverLicences</span><span class="sxs-lookup"><span data-stu-id="21a8c-233">DriverLicences</span></span>
- <span data-ttu-id="21a8c-234">Driver Lic</span><span class="sxs-lookup"><span data-stu-id="21a8c-234">Driver Lic</span></span>
- <span data-ttu-id="21a8c-235">Driver Licence</span><span class="sxs-lookup"><span data-stu-id="21a8c-235">Driver Licence</span></span>
- <span data-ttu-id="21a8c-236">Driver Licences</span><span class="sxs-lookup"><span data-stu-id="21a8c-236">Driver Licences</span></span>
- <span data-ttu-id="21a8c-237">DriversLic</span><span class="sxs-lookup"><span data-stu-id="21a8c-237">DriversLic</span></span>
- <span data-ttu-id="21a8c-238">DriversLicence</span><span class="sxs-lookup"><span data-stu-id="21a8c-238">DriversLicence</span></span>
- <span data-ttu-id="21a8c-239">DriversLicences</span><span class="sxs-lookup"><span data-stu-id="21a8c-239">DriversLicences</span></span>
- <span data-ttu-id="21a8c-240">Drivers Lic</span><span class="sxs-lookup"><span data-stu-id="21a8c-240">Drivers Lic</span></span>
- <span data-ttu-id="21a8c-241">Drivers Lics</span><span class="sxs-lookup"><span data-stu-id="21a8c-241">Drivers Lics</span></span>
- <span data-ttu-id="21a8c-242">Drivers Licence</span><span class="sxs-lookup"><span data-stu-id="21a8c-242">Drivers Licence</span></span>
- <span data-ttu-id="21a8c-243">Drivers Licences</span><span class="sxs-lookup"><span data-stu-id="21a8c-243">Drivers Licences</span></span>
- <span data-ttu-id="21a8c-244">Driver'Lic</span><span class="sxs-lookup"><span data-stu-id="21a8c-244">Driver'Lic</span></span>
- <span data-ttu-id="21a8c-245">Driver'Lics</span><span class="sxs-lookup"><span data-stu-id="21a8c-245">Driver'Lics</span></span>
- <span data-ttu-id="21a8c-246">Driver'Licence</span><span class="sxs-lookup"><span data-stu-id="21a8c-246">Driver'Licence</span></span>
- <span data-ttu-id="21a8c-247">Driver'Licences</span><span class="sxs-lookup"><span data-stu-id="21a8c-247">Driver'Licences</span></span>
- <span data-ttu-id="21a8c-248">Driver'Lic</span><span class="sxs-lookup"><span data-stu-id="21a8c-248">Driver' Lic</span></span>
- <span data-ttu-id="21a8c-249">Driver'Lics</span><span class="sxs-lookup"><span data-stu-id="21a8c-249">Driver' Lics</span></span>
- <span data-ttu-id="21a8c-250">Driver'Licence</span><span class="sxs-lookup"><span data-stu-id="21a8c-250">Driver' Licence</span></span>
- <span data-ttu-id="21a8c-251">Driver'Licences</span><span class="sxs-lookup"><span data-stu-id="21a8c-251">Driver' Licences</span></span>
- <span data-ttu-id="21a8c-252">Driver'sLic</span><span class="sxs-lookup"><span data-stu-id="21a8c-252">Driver'sLic</span></span>
- <span data-ttu-id="21a8c-253">Driver'sLics</span><span class="sxs-lookup"><span data-stu-id="21a8c-253">Driver'sLics</span></span>
- <span data-ttu-id="21a8c-254">Driver'sLicence</span><span class="sxs-lookup"><span data-stu-id="21a8c-254">Driver'sLicence</span></span>
- <span data-ttu-id="21a8c-255">Driver'sLicences</span><span class="sxs-lookup"><span data-stu-id="21a8c-255">Driver'sLicences</span></span>
- <span data-ttu-id="21a8c-256">Driver's Lic</span><span class="sxs-lookup"><span data-stu-id="21a8c-256">Driver's Lic</span></span>
- <span data-ttu-id="21a8c-257">Driver's Lics</span><span class="sxs-lookup"><span data-stu-id="21a8c-257">Driver's Lics</span></span>
- <span data-ttu-id="21a8c-258">Driver's Licence</span><span class="sxs-lookup"><span data-stu-id="21a8c-258">Driver's Licence</span></span>
- <span data-ttu-id="21a8c-259">Driver's Licences</span><span class="sxs-lookup"><span data-stu-id="21a8c-259">Driver's Licences</span></span>
- <span data-ttu-id="21a8c-260">DriverLic #</span><span class="sxs-lookup"><span data-stu-id="21a8c-260">DriverLic#</span></span>
- <span data-ttu-id="21a8c-261">DriverLics #</span><span class="sxs-lookup"><span data-stu-id="21a8c-261">DriverLics#</span></span>
- <span data-ttu-id="21a8c-262">DriverLicence #</span><span class="sxs-lookup"><span data-stu-id="21a8c-262">DriverLicence#</span></span>
- <span data-ttu-id="21a8c-263">DriverLicences #</span><span class="sxs-lookup"><span data-stu-id="21a8c-263">DriverLicences#</span></span>
- <span data-ttu-id="21a8c-264">Driver Lic#</span><span class="sxs-lookup"><span data-stu-id="21a8c-264">Driver Lic#</span></span>
- <span data-ttu-id="21a8c-265">Driver Lics#</span><span class="sxs-lookup"><span data-stu-id="21a8c-265">Driver Lics#</span></span>
- <span data-ttu-id="21a8c-266">Driver Licence#</span><span class="sxs-lookup"><span data-stu-id="21a8c-266">Driver Licence#</span></span>
- <span data-ttu-id="21a8c-267">Driver Licences#</span><span class="sxs-lookup"><span data-stu-id="21a8c-267">Driver Licences#</span></span>
- <span data-ttu-id="21a8c-268">DriversLic #</span><span class="sxs-lookup"><span data-stu-id="21a8c-268">DriversLic#</span></span>
- <span data-ttu-id="21a8c-269">DriversLics #</span><span class="sxs-lookup"><span data-stu-id="21a8c-269">DriversLics#</span></span>
- <span data-ttu-id="21a8c-270">DriversLicence #</span><span class="sxs-lookup"><span data-stu-id="21a8c-270">DriversLicence#</span></span>
- <span data-ttu-id="21a8c-271">DriversLicences #</span><span class="sxs-lookup"><span data-stu-id="21a8c-271">DriversLicences#</span></span>
- <span data-ttu-id="21a8c-272">Drivers Lic#</span><span class="sxs-lookup"><span data-stu-id="21a8c-272">Drivers Lic#</span></span>
- <span data-ttu-id="21a8c-273">Drivers Lics#</span><span class="sxs-lookup"><span data-stu-id="21a8c-273">Drivers Lics#</span></span>
- <span data-ttu-id="21a8c-274">Drivers Licence#</span><span class="sxs-lookup"><span data-stu-id="21a8c-274">Drivers Licence#</span></span>
- <span data-ttu-id="21a8c-275">Drivers Licences#</span><span class="sxs-lookup"><span data-stu-id="21a8c-275">Drivers Licences#</span></span>
- <span data-ttu-id="21a8c-276">Driver'Lic #</span><span class="sxs-lookup"><span data-stu-id="21a8c-276">Driver'Lic#</span></span>
- <span data-ttu-id="21a8c-277">Driver'Lics #</span><span class="sxs-lookup"><span data-stu-id="21a8c-277">Driver'Lics#</span></span>
- <span data-ttu-id="21a8c-278">Driver'Licence #</span><span class="sxs-lookup"><span data-stu-id="21a8c-278">Driver'Licence#</span></span>
- <span data-ttu-id="21a8c-279">Driver'Licences #</span><span class="sxs-lookup"><span data-stu-id="21a8c-279">Driver'Licences#</span></span>
- <span data-ttu-id="21a8c-280">Driver'Lic#</span><span class="sxs-lookup"><span data-stu-id="21a8c-280">Driver' Lic#</span></span>
- <span data-ttu-id="21a8c-281">Driver'Lics#</span><span class="sxs-lookup"><span data-stu-id="21a8c-281">Driver' Lics#</span></span>
- <span data-ttu-id="21a8c-282">Driver'Licence#</span><span class="sxs-lookup"><span data-stu-id="21a8c-282">Driver' Licence#</span></span>
- <span data-ttu-id="21a8c-283">Driver'Licences#</span><span class="sxs-lookup"><span data-stu-id="21a8c-283">Driver' Licences#</span></span>
- <span data-ttu-id="21a8c-284">Driver'sLic #</span><span class="sxs-lookup"><span data-stu-id="21a8c-284">Driver'sLic#</span></span>
- <span data-ttu-id="21a8c-285">Driver'sLics #</span><span class="sxs-lookup"><span data-stu-id="21a8c-285">Driver'sLics#</span></span>
- <span data-ttu-id="21a8c-286">Driver'sLicence #</span><span class="sxs-lookup"><span data-stu-id="21a8c-286">Driver'sLicence#</span></span>
- <span data-ttu-id="21a8c-287">Driver'sLicences #</span><span class="sxs-lookup"><span data-stu-id="21a8c-287">Driver'sLicences#</span></span>
- <span data-ttu-id="21a8c-288">Driver's Lic#</span><span class="sxs-lookup"><span data-stu-id="21a8c-288">Driver's Lic#</span></span>
- <span data-ttu-id="21a8c-289">Driver's Lics#</span><span class="sxs-lookup"><span data-stu-id="21a8c-289">Driver's Lics#</span></span>
- <span data-ttu-id="21a8c-290">Driver's Licence#</span><span class="sxs-lookup"><span data-stu-id="21a8c-290">Driver's Licence#</span></span>
- <span data-ttu-id="21a8c-291">Driver's Licences#</span><span class="sxs-lookup"><span data-stu-id="21a8c-291">Driver's Licences#</span></span> 

#### <a name="keywordaustraliadriverslicensenumberexclusions"></a><span data-ttu-id="21a8c-292">Keyword_australia_drivers_license_number_exclusions</span><span class="sxs-lookup"><span data-stu-id="21a8c-292">Keyword_australia_drivers_license_number_exclusions</span></span>

- <span data-ttu-id="21a8c-293">AAA</span><span class="sxs-lookup"><span data-stu-id="21a8c-293">aaa</span></span>
- <span data-ttu-id="21a8c-294">DriverLicense</span><span class="sxs-lookup"><span data-stu-id="21a8c-294">DriverLicense</span></span>
- <span data-ttu-id="21a8c-295">DriverLicenses</span><span class="sxs-lookup"><span data-stu-id="21a8c-295">DriverLicenses</span></span>
- <span data-ttu-id="21a8c-296">Driver License</span><span class="sxs-lookup"><span data-stu-id="21a8c-296">Driver License</span></span>
- <span data-ttu-id="21a8c-297">Driver Licenses</span><span class="sxs-lookup"><span data-stu-id="21a8c-297">Driver Licenses</span></span>
- <span data-ttu-id="21a8c-298">DriversLicense</span><span class="sxs-lookup"><span data-stu-id="21a8c-298">DriversLicense</span></span>
- <span data-ttu-id="21a8c-299">DriversLicenses</span><span class="sxs-lookup"><span data-stu-id="21a8c-299">DriversLicenses</span></span>
- <span data-ttu-id="21a8c-300">Drivers License</span><span class="sxs-lookup"><span data-stu-id="21a8c-300">Drivers License</span></span>
- <span data-ttu-id="21a8c-301">Drivers Licenses</span><span class="sxs-lookup"><span data-stu-id="21a8c-301">Drivers Licenses</span></span>
- <span data-ttu-id="21a8c-302">Driver'License</span><span class="sxs-lookup"><span data-stu-id="21a8c-302">Driver'License</span></span>
- <span data-ttu-id="21a8c-303">Driver'Licenses</span><span class="sxs-lookup"><span data-stu-id="21a8c-303">Driver'Licenses</span></span>
- <span data-ttu-id="21a8c-304">Driver'License</span><span class="sxs-lookup"><span data-stu-id="21a8c-304">Driver' License</span></span>
- <span data-ttu-id="21a8c-305">Driver'Licenses</span><span class="sxs-lookup"><span data-stu-id="21a8c-305">Driver' Licenses</span></span>
- <span data-ttu-id="21a8c-306">Driver'sLicense</span><span class="sxs-lookup"><span data-stu-id="21a8c-306">Driver'sLicense</span></span>
- <span data-ttu-id="21a8c-307">Driver'sLicenses</span><span class="sxs-lookup"><span data-stu-id="21a8c-307">Driver'sLicenses</span></span>
- <span data-ttu-id="21a8c-308">Driver's License</span><span class="sxs-lookup"><span data-stu-id="21a8c-308">Driver's License</span></span>
- <span data-ttu-id="21a8c-309">Driver's Licenses</span><span class="sxs-lookup"><span data-stu-id="21a8c-309">Driver's Licenses</span></span>
- <span data-ttu-id="21a8c-310">DriverLicense #</span><span class="sxs-lookup"><span data-stu-id="21a8c-310">DriverLicense#</span></span>
- <span data-ttu-id="21a8c-311">DriverLicenses #</span><span class="sxs-lookup"><span data-stu-id="21a8c-311">DriverLicenses#</span></span>
- <span data-ttu-id="21a8c-312">Driver License#</span><span class="sxs-lookup"><span data-stu-id="21a8c-312">Driver License#</span></span>
- <span data-ttu-id="21a8c-313">Driver Licenses#</span><span class="sxs-lookup"><span data-stu-id="21a8c-313">Driver Licenses#</span></span>
- <span data-ttu-id="21a8c-314">DriversLicense #</span><span class="sxs-lookup"><span data-stu-id="21a8c-314">DriversLicense#</span></span>
- <span data-ttu-id="21a8c-315">DriversLicenses #</span><span class="sxs-lookup"><span data-stu-id="21a8c-315">DriversLicenses#</span></span>
- <span data-ttu-id="21a8c-316">Drivers License#</span><span class="sxs-lookup"><span data-stu-id="21a8c-316">Drivers License#</span></span>
- <span data-ttu-id="21a8c-317">Drivers Licenses#</span><span class="sxs-lookup"><span data-stu-id="21a8c-317">Drivers Licenses#</span></span>
- <span data-ttu-id="21a8c-318">Driver'License #</span><span class="sxs-lookup"><span data-stu-id="21a8c-318">Driver'License#</span></span>
- <span data-ttu-id="21a8c-319">Driver'Licenses #</span><span class="sxs-lookup"><span data-stu-id="21a8c-319">Driver'Licenses#</span></span>
- <span data-ttu-id="21a8c-320">Driver'License#</span><span class="sxs-lookup"><span data-stu-id="21a8c-320">Driver' License#</span></span>
- <span data-ttu-id="21a8c-321">Driver'Licenses#</span><span class="sxs-lookup"><span data-stu-id="21a8c-321">Driver' Licenses#</span></span>
- <span data-ttu-id="21a8c-322">Driver'sLicense #</span><span class="sxs-lookup"><span data-stu-id="21a8c-322">Driver'sLicense#</span></span>
- <span data-ttu-id="21a8c-323">Driver'sLicenses #</span><span class="sxs-lookup"><span data-stu-id="21a8c-323">Driver'sLicenses#</span></span>
- <span data-ttu-id="21a8c-324">Driver's License#</span><span class="sxs-lookup"><span data-stu-id="21a8c-324">Driver's License#</span></span>
- <span data-ttu-id="21a8c-325">Driver's Licenses#</span><span class="sxs-lookup"><span data-stu-id="21a8c-325">Driver's Licenses#</span></span>
   
## <a name="australia-medical-account-number"></a><span data-ttu-id="21a8c-326">Número de conta médica da Austrália</span><span class="sxs-lookup"><span data-stu-id="21a8c-326">Australia Medical Account Number</span></span>

### <a name="format"></a><span data-ttu-id="21a8c-327">Format</span><span class="sxs-lookup"><span data-stu-id="21a8c-327">Format</span></span>

<span data-ttu-id="21a8c-328">10 a 11 dígitos</span><span class="sxs-lookup"><span data-stu-id="21a8c-328">10-11 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="21a8c-329">Padrão</span><span class="sxs-lookup"><span data-stu-id="21a8c-329">Pattern</span></span>

<span data-ttu-id="21a8c-330">10 a 11 dígitos:</span><span class="sxs-lookup"><span data-stu-id="21a8c-330">10-11 digits:</span></span>
- <span data-ttu-id="21a8c-331">Primeiro dígito está no intervalo de 2 a 6</span><span class="sxs-lookup"><span data-stu-id="21a8c-331">First digit is in the range 2-6</span></span>
- <span data-ttu-id="21a8c-332">O nono dígito é um dígito de verificação</span><span class="sxs-lookup"><span data-stu-id="21a8c-332">Ninth digit is a check digit</span></span>
- <span data-ttu-id="21a8c-333">O décimo dígito é o dígito do problema</span><span class="sxs-lookup"><span data-stu-id="21a8c-333">Tenth digit is the issue digit</span></span>
- <span data-ttu-id="21a8c-334">O décimo primeiro dígito (opcional) é o número individual</span><span class="sxs-lookup"><span data-stu-id="21a8c-334">Eleventh digit (optional) is the individual number</span></span>

### <a name="checksum"></a><span data-ttu-id="21a8c-335">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="21a8c-335">Checksum</span></span>

<span data-ttu-id="21a8c-336">Sim</span><span class="sxs-lookup"><span data-stu-id="21a8c-336">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="21a8c-337">Definição</span><span class="sxs-lookup"><span data-stu-id="21a8c-337">Definition</span></span>

<span data-ttu-id="21a8c-338">Uma política de DLP tem 95% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="21a8c-338">A DLP policy is 95% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="21a8c-339">A função Func_australian_medical_account_number localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="21a8c-339">The function Func_australian_medical_account_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="21a8c-340">Uma palavra-chave de Keyword_Australia_Medical_Account_Number for encontrada.</span><span class="sxs-lookup"><span data-stu-id="21a8c-340">A keyword from Keyword_Australia_Medical_Account_Number is found.</span></span>
- <span data-ttu-id="21a8c-341">A soma de verificação passa.</span><span class="sxs-lookup"><span data-stu-id="21a8c-341">The checksum passes.</span></span>

<span data-ttu-id="21a8c-342">Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="21a8c-342">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="21a8c-343">A função Func_australian_medical_account_number localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="21a8c-343">The function Func_australian_medical_account_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="21a8c-344">A soma de verificação passa.</span><span class="sxs-lookup"><span data-stu-id="21a8c-344">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="21a8c-345">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="21a8c-345">Keywords</span></span>

#### <a name="keywordaustraliamedicalaccountnumber"></a><span data-ttu-id="21a8c-346">Keyword_Australia_Medical_Account_Number</span><span class="sxs-lookup"><span data-stu-id="21a8c-346">Keyword_Australia_Medical_Account_Number</span></span>

- <span data-ttu-id="21a8c-347">bank account details</span><span class="sxs-lookup"><span data-stu-id="21a8c-347">bank account details</span></span>
- <span data-ttu-id="21a8c-348">medicare payments</span><span class="sxs-lookup"><span data-stu-id="21a8c-348">medicare payments</span></span>
- <span data-ttu-id="21a8c-349">mortgage account</span><span class="sxs-lookup"><span data-stu-id="21a8c-349">mortgage account</span></span>
- <span data-ttu-id="21a8c-350">bank payments</span><span class="sxs-lookup"><span data-stu-id="21a8c-350">bank payments</span></span>
- <span data-ttu-id="21a8c-351">information branch</span><span class="sxs-lookup"><span data-stu-id="21a8c-351">information branch</span></span>
- <span data-ttu-id="21a8c-352">credit card loan</span><span class="sxs-lookup"><span data-stu-id="21a8c-352">credit card loan</span></span>
- <span data-ttu-id="21a8c-353">department of human services</span><span class="sxs-lookup"><span data-stu-id="21a8c-353">department of human services</span></span>
- <span data-ttu-id="21a8c-354">local service</span><span class="sxs-lookup"><span data-stu-id="21a8c-354">local service</span></span>
- <span data-ttu-id="21a8c-355">Medicare</span><span class="sxs-lookup"><span data-stu-id="21a8c-355">medicare</span></span>

   
## <a name="australia-passport-number"></a><span data-ttu-id="21a8c-356">Número de passaporte da Austrália</span><span class="sxs-lookup"><span data-stu-id="21a8c-356">Australia Passport Number</span></span>

### <a name="format"></a><span data-ttu-id="21a8c-357">Format</span><span class="sxs-lookup"><span data-stu-id="21a8c-357">Format</span></span>

<span data-ttu-id="21a8c-358">Uma letra seguida por sete dígitos</span><span class="sxs-lookup"><span data-stu-id="21a8c-358">A letter followed by seven digits</span></span>

### <a name="pattern"></a><span data-ttu-id="21a8c-359">Padrão</span><span class="sxs-lookup"><span data-stu-id="21a8c-359">Pattern</span></span>

<span data-ttu-id="21a8c-360">Uma letra (não diferencia maiúsculas de minúsculas) seguida de sete dígitos</span><span class="sxs-lookup"><span data-stu-id="21a8c-360">A letter (not case sensitive) followed by seven digits</span></span>

### <a name="checksum"></a><span data-ttu-id="21a8c-361">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="21a8c-361">Checksum</span></span>

<span data-ttu-id="21a8c-362">Não</span><span class="sxs-lookup"><span data-stu-id="21a8c-362">No</span></span>

### <a name="definition"></a><span data-ttu-id="21a8c-363">Definição</span><span class="sxs-lookup"><span data-stu-id="21a8c-363">Definition</span></span>

<span data-ttu-id="21a8c-364">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="21a8c-364">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="21a8c-365">A expressão regular Regex_australia_passport_number localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="21a8c-365">The regular expression Regex_australia_passport_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="21a8c-366">Uma palavra-chave de Keyword_passport ou Keyword_australia_passport_number for encontrada.</span><span class="sxs-lookup"><span data-stu-id="21a8c-366">A keyword from Keyword_passport or Keyword_australia_passport_number is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="21a8c-367">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="21a8c-367">Keywords</span></span>

#### <a name="keywordpassport"></a><span data-ttu-id="21a8c-368">Keyword_passport</span><span class="sxs-lookup"><span data-stu-id="21a8c-368">Keyword_passport</span></span>

- <span data-ttu-id="21a8c-369">Passport Number</span><span class="sxs-lookup"><span data-stu-id="21a8c-369">Passport Number</span></span>
- <span data-ttu-id="21a8c-370">Passport No</span><span class="sxs-lookup"><span data-stu-id="21a8c-370">Passport No</span></span>
- <span data-ttu-id="21a8c-371">Passport #</span><span class="sxs-lookup"><span data-stu-id="21a8c-371">Passport #</span></span>
- <span data-ttu-id="21a8c-372">Passaport</span><span class="sxs-lookup"><span data-stu-id="21a8c-372">Passport#</span></span>
- <span data-ttu-id="21a8c-373">Passportid</span><span class="sxs-lookup"><span data-stu-id="21a8c-373">PassportID</span></span>
- <span data-ttu-id="21a8c-374">Passportno</span><span class="sxs-lookup"><span data-stu-id="21a8c-374">Passportno</span></span>
- <span data-ttu-id="21a8c-375">passportnumber</span><span class="sxs-lookup"><span data-stu-id="21a8c-375">passportnumber</span></span>
- <span data-ttu-id="21a8c-376">パスポート</span><span class="sxs-lookup"><span data-stu-id="21a8c-376">パスポート</span></span>
- <span data-ttu-id="21a8c-377">パスポート番号</span><span class="sxs-lookup"><span data-stu-id="21a8c-377">パスポート番号</span></span>
- <span data-ttu-id="21a8c-378">パスポートのNum</span><span class="sxs-lookup"><span data-stu-id="21a8c-378">パスポートのNum</span></span>
- <span data-ttu-id="21a8c-379">パスポート ＃</span><span class="sxs-lookup"><span data-stu-id="21a8c-379">パスポート ＃</span></span> 
- <span data-ttu-id="21a8c-380">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="21a8c-380">Numéro de passeport</span></span>
- <span data-ttu-id="21a8c-381">Passeport n °</span><span class="sxs-lookup"><span data-stu-id="21a8c-381">Passeport n °</span></span>
- <span data-ttu-id="21a8c-382">Passeport Non</span><span class="sxs-lookup"><span data-stu-id="21a8c-382">Passeport Non</span></span>
- <span data-ttu-id="21a8c-383">Passeport #</span><span class="sxs-lookup"><span data-stu-id="21a8c-383">Passeport #</span></span>
- <span data-ttu-id="21a8c-384">Passeport #</span><span class="sxs-lookup"><span data-stu-id="21a8c-384">Passeport#</span></span>
- <span data-ttu-id="21a8c-385">PasseportNon</span><span class="sxs-lookup"><span data-stu-id="21a8c-385">PasseportNon</span></span>
- <span data-ttu-id="21a8c-386">Passeportn °</span><span class="sxs-lookup"><span data-stu-id="21a8c-386">Passeportn °</span></span>

#### <a name="keywordaustraliapassportnumber"></a><span data-ttu-id="21a8c-387">Keyword_australia_passport_number</span><span class="sxs-lookup"><span data-stu-id="21a8c-387">Keyword_australia_passport_number</span></span>

- <span data-ttu-id="21a8c-388">Passaport</span><span class="sxs-lookup"><span data-stu-id="21a8c-388">passport</span></span>
- <span data-ttu-id="21a8c-389">passport details</span><span class="sxs-lookup"><span data-stu-id="21a8c-389">passport details</span></span>
- <span data-ttu-id="21a8c-390">immigration and citizenship</span><span class="sxs-lookup"><span data-stu-id="21a8c-390">immigration and citizenship</span></span>
- <span data-ttu-id="21a8c-391">commonwealth of australia</span><span class="sxs-lookup"><span data-stu-id="21a8c-391">commonwealth of australia</span></span>
- <span data-ttu-id="21a8c-392">department of immigration</span><span class="sxs-lookup"><span data-stu-id="21a8c-392">department of immigration</span></span>
- <span data-ttu-id="21a8c-393">residential address</span><span class="sxs-lookup"><span data-stu-id="21a8c-393">residential address</span></span>
- <span data-ttu-id="21a8c-394">department of immigration and citizenship</span><span class="sxs-lookup"><span data-stu-id="21a8c-394">department of immigration and citizenship</span></span>
- <span data-ttu-id="21a8c-395">cartões</span><span class="sxs-lookup"><span data-stu-id="21a8c-395">visa</span></span>
- <span data-ttu-id="21a8c-396">national identity card</span><span class="sxs-lookup"><span data-stu-id="21a8c-396">national identity card</span></span>
- <span data-ttu-id="21a8c-397">passport number</span><span class="sxs-lookup"><span data-stu-id="21a8c-397">passport number</span></span>
- <span data-ttu-id="21a8c-398">travel document</span><span class="sxs-lookup"><span data-stu-id="21a8c-398">travel document</span></span>
- <span data-ttu-id="21a8c-399">issuing authority</span><span class="sxs-lookup"><span data-stu-id="21a8c-399">issuing authority</span></span>
   
## <a name="australia-tax-file-number"></a><span data-ttu-id="21a8c-400">Número de imposto de renda da Austrália</span><span class="sxs-lookup"><span data-stu-id="21a8c-400">Australia Tax File Number</span></span>

### <a name="format"></a><span data-ttu-id="21a8c-401">Format</span><span class="sxs-lookup"><span data-stu-id="21a8c-401">Format</span></span>

<span data-ttu-id="21a8c-402">8 a 9 dígitos</span><span class="sxs-lookup"><span data-stu-id="21a8c-402">8-9 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="21a8c-403">Padrão</span><span class="sxs-lookup"><span data-stu-id="21a8c-403">Pattern</span></span>

<span data-ttu-id="21a8c-404">8 a 9 dígitos normalmente apresentados com espaços, da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="21a8c-404">8-9 digits typically presented with spaces as follows:</span></span>
- <span data-ttu-id="21a8c-405">Três dígitos</span><span class="sxs-lookup"><span data-stu-id="21a8c-405">Three digits</span></span> 
- <span data-ttu-id="21a8c-406">Um espaço opcional</span><span class="sxs-lookup"><span data-stu-id="21a8c-406">An optional space</span></span> 
- <span data-ttu-id="21a8c-407">Três dígitos</span><span class="sxs-lookup"><span data-stu-id="21a8c-407">Three digits</span></span> 
- <span data-ttu-id="21a8c-408">Um espaço opcional</span><span class="sxs-lookup"><span data-stu-id="21a8c-408">An optional space</span></span> 
- <span data-ttu-id="21a8c-409">2 a 3 dígitos em que o último dígito é um dígito de verificação</span><span class="sxs-lookup"><span data-stu-id="21a8c-409">2-3 digits where the last digit is a check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="21a8c-410">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="21a8c-410">Checksum</span></span>

<span data-ttu-id="21a8c-411">Sim</span><span class="sxs-lookup"><span data-stu-id="21a8c-411">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="21a8c-412">Definição</span><span class="sxs-lookup"><span data-stu-id="21a8c-412">Definition</span></span>

<span data-ttu-id="21a8c-413">Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="21a8c-413">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="21a8c-414">A função Func_australian_tax_file_number localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="21a8c-414">The function Func_australian_tax_file_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="21a8c-415">Nenhuma palavra-chave de Keyword_Australia_Tax_File_Number ou Keyword_number_exclusions for encontrada.</span><span class="sxs-lookup"><span data-stu-id="21a8c-415">No keyword from Keyword_Australia_Tax_File_Number or Keyword_number_exclusions is found.</span></span>
- <span data-ttu-id="21a8c-416">A soma de verificação passa.</span><span class="sxs-lookup"><span data-stu-id="21a8c-416">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="21a8c-417">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="21a8c-417">Keywords</span></span>

#### <a name="keywordaustraliataxfilenumber"></a><span data-ttu-id="21a8c-418">Keyword_Australia_Tax_File_Number</span><span class="sxs-lookup"><span data-stu-id="21a8c-418">Keyword_Australia_Tax_File_Number</span></span>

- <span data-ttu-id="21a8c-419">australian business number</span><span class="sxs-lookup"><span data-stu-id="21a8c-419">australian business number</span></span>
- <span data-ttu-id="21a8c-420">marginal tax rate</span><span class="sxs-lookup"><span data-stu-id="21a8c-420">marginal tax rate</span></span>
- <span data-ttu-id="21a8c-421">medicare levy</span><span class="sxs-lookup"><span data-stu-id="21a8c-421">medicare levy</span></span>
- <span data-ttu-id="21a8c-422">portfolio number</span><span class="sxs-lookup"><span data-stu-id="21a8c-422">portfolio number</span></span>
- <span data-ttu-id="21a8c-423">service veterans</span><span class="sxs-lookup"><span data-stu-id="21a8c-423">service veterans</span></span>
- <span data-ttu-id="21a8c-424">withholding tax</span><span class="sxs-lookup"><span data-stu-id="21a8c-424">withholding tax</span></span>
- <span data-ttu-id="21a8c-425">individual tax return</span><span class="sxs-lookup"><span data-stu-id="21a8c-425">individual tax return</span></span>
- <span data-ttu-id="21a8c-426">tax file number</span><span class="sxs-lookup"><span data-stu-id="21a8c-426">tax file number</span></span>

#### <a name="keywordnumberexclusions"></a><span data-ttu-id="21a8c-427">Keyword_number_exclusions</span><span class="sxs-lookup"><span data-stu-id="21a8c-427">Keyword_number_exclusions</span></span>

- <span data-ttu-id="21a8c-428">00000000</span><span class="sxs-lookup"><span data-stu-id="21a8c-428">00000000</span></span>
- <span data-ttu-id="21a8c-429">11111111</span><span class="sxs-lookup"><span data-stu-id="21a8c-429">11111111</span></span>
- <span data-ttu-id="21a8c-430">22222222</span><span class="sxs-lookup"><span data-stu-id="21a8c-430">22222222</span></span>
- <span data-ttu-id="21a8c-431">33333333</span><span class="sxs-lookup"><span data-stu-id="21a8c-431">33333333</span></span>
- <span data-ttu-id="21a8c-432">44444444</span><span class="sxs-lookup"><span data-stu-id="21a8c-432">44444444</span></span>
- <span data-ttu-id="21a8c-433">55555555</span><span class="sxs-lookup"><span data-stu-id="21a8c-433">55555555</span></span>
- <span data-ttu-id="21a8c-434">66666666</span><span class="sxs-lookup"><span data-stu-id="21a8c-434">66666666</span></span>
- <span data-ttu-id="21a8c-435">77777777</span><span class="sxs-lookup"><span data-stu-id="21a8c-435">77777777</span></span>
- <span data-ttu-id="21a8c-436">88888888</span><span class="sxs-lookup"><span data-stu-id="21a8c-436">88888888</span></span>
- <span data-ttu-id="21a8c-437">99999999</span><span class="sxs-lookup"><span data-stu-id="21a8c-437">99999999</span></span>
- <span data-ttu-id="21a8c-438">000000000</span><span class="sxs-lookup"><span data-stu-id="21a8c-438">000000000</span></span>
- <span data-ttu-id="21a8c-439">111111111</span><span class="sxs-lookup"><span data-stu-id="21a8c-439">111111111</span></span>
- <span data-ttu-id="21a8c-440">222222222</span><span class="sxs-lookup"><span data-stu-id="21a8c-440">222222222</span></span>
- <span data-ttu-id="21a8c-441">333333333</span><span class="sxs-lookup"><span data-stu-id="21a8c-441">333333333</span></span>
- <span data-ttu-id="21a8c-442">444444444</span><span class="sxs-lookup"><span data-stu-id="21a8c-442">444444444</span></span>
- <span data-ttu-id="21a8c-443">555555555</span><span class="sxs-lookup"><span data-stu-id="21a8c-443">555555555</span></span>
- <span data-ttu-id="21a8c-444">666666666</span><span class="sxs-lookup"><span data-stu-id="21a8c-444">666666666</span></span>
- <span data-ttu-id="21a8c-445">777777777</span><span class="sxs-lookup"><span data-stu-id="21a8c-445">777777777</span></span>
- <span data-ttu-id="21a8c-446">888888888</span><span class="sxs-lookup"><span data-stu-id="21a8c-446">888888888</span></span>
- <span data-ttu-id="21a8c-447">999999999</span><span class="sxs-lookup"><span data-stu-id="21a8c-447">999999999</span></span>
- <span data-ttu-id="21a8c-448">0000000000</span><span class="sxs-lookup"><span data-stu-id="21a8c-448">0000000000</span></span>
- <span data-ttu-id="21a8c-449">1111111111</span><span class="sxs-lookup"><span data-stu-id="21a8c-449">1111111111</span></span>
- <span data-ttu-id="21a8c-450">2222222222</span><span class="sxs-lookup"><span data-stu-id="21a8c-450">2222222222</span></span>
- <span data-ttu-id="21a8c-451">3333333333</span><span class="sxs-lookup"><span data-stu-id="21a8c-451">3333333333</span></span>
- <span data-ttu-id="21a8c-452">4444444444</span><span class="sxs-lookup"><span data-stu-id="21a8c-452">4444444444</span></span>
- <span data-ttu-id="21a8c-453">5555555555</span><span class="sxs-lookup"><span data-stu-id="21a8c-453">5555555555</span></span>
- <span data-ttu-id="21a8c-454">6666666666</span><span class="sxs-lookup"><span data-stu-id="21a8c-454">6666666666</span></span>
- <span data-ttu-id="21a8c-455">7777777777</span><span class="sxs-lookup"><span data-stu-id="21a8c-455">7777777777</span></span>
- <span data-ttu-id="21a8c-456">8888888888</span><span class="sxs-lookup"><span data-stu-id="21a8c-456">8888888888</span></span>
- <span data-ttu-id="21a8c-457">9999999999</span><span class="sxs-lookup"><span data-stu-id="21a8c-457">9999999999</span></span>
   
## <a name="belgium-national-number"></a><span data-ttu-id="21a8c-458">Número Nacional da Bélgica</span><span class="sxs-lookup"><span data-stu-id="21a8c-458">Belgium National Number</span></span>

### <a name="format"></a><span data-ttu-id="21a8c-459">Format</span><span class="sxs-lookup"><span data-stu-id="21a8c-459">Format</span></span>

<span data-ttu-id="21a8c-460">11 dígitos mais delimitadores</span><span class="sxs-lookup"><span data-stu-id="21a8c-460">11 digits plus delimiters</span></span>

### <a name="pattern"></a><span data-ttu-id="21a8c-461">Padrão</span><span class="sxs-lookup"><span data-stu-id="21a8c-461">Pattern</span></span>

<span data-ttu-id="21a8c-462">11 dígitos mais delimitadores.</span><span class="sxs-lookup"><span data-stu-id="21a8c-462">11 digits plus delimiters:</span></span>
- <span data-ttu-id="21a8c-463">Seis dígitos e dois pontos no formato AA.MM.DD da data de nascimento </span><span class="sxs-lookup"><span data-stu-id="21a8c-463">Six digits and two periods in the format YY.MM.DD for date of birth</span></span> 
- <span data-ttu-id="21a8c-464">Um hífen</span><span class="sxs-lookup"><span data-stu-id="21a8c-464">A hyphen</span></span> 
- <span data-ttu-id="21a8c-465">Três dígitos sequenciais (ímpares para homens, pares para mulheres) </span><span class="sxs-lookup"><span data-stu-id="21a8c-465">Three sequential digits (odd for males, even for females)</span></span> 
- <span data-ttu-id="21a8c-466">Um ponto </span><span class="sxs-lookup"><span data-stu-id="21a8c-466">A period</span></span> 
- <span data-ttu-id="21a8c-467">Dois dígitos que são um dígito de verificação</span><span class="sxs-lookup"><span data-stu-id="21a8c-467">Two digits that are a check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="21a8c-468">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="21a8c-468">Checksum</span></span>

<span data-ttu-id="21a8c-469">Sim</span><span class="sxs-lookup"><span data-stu-id="21a8c-469">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="21a8c-470">Definição</span><span class="sxs-lookup"><span data-stu-id="21a8c-470">Definition</span></span>

<span data-ttu-id="21a8c-471">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="21a8c-471">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="21a8c-472">A função Func_belgium_national_number localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="21a8c-472">The function Func_belgium_national_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="21a8c-473">Uma palavra-chave de Keyword_belgium_national_number for encontrada.</span><span class="sxs-lookup"><span data-stu-id="21a8c-473">A keyword from Keyword_belgium_national_number is found.</span></span>
- <span data-ttu-id="21a8c-474">A soma de verificação passa.</span><span class="sxs-lookup"><span data-stu-id="21a8c-474">The checksum passes.</span></span>

```
<!-- Belgium National Number -->
  <Entity id="fb969c9e-0fd1-4b18-8091-a2123c5e6a54" recommendedConfidence="75" patternsProximity="300">
   <Pattern confidenceLevel="75">
     <IdMatch idRef="Func_belgium_national_number"/>
     <Match idRef="Keyword_belgium_national_number"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="21a8c-475">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="21a8c-475">Keywords</span></span>

#### <a name="keywordbelgiumnationalnumber"></a><span data-ttu-id="21a8c-476">Keyword_belgium_national_number</span><span class="sxs-lookup"><span data-stu-id="21a8c-476">Keyword_belgium_national_number</span></span>

- <span data-ttu-id="21a8c-477">Identidade</span><span class="sxs-lookup"><span data-stu-id="21a8c-477">Identity</span></span>
- <span data-ttu-id="21a8c-478">Registro</span><span class="sxs-lookup"><span data-stu-id="21a8c-478">Registration</span></span>
- <span data-ttu-id="21a8c-479">Identificador</span><span class="sxs-lookup"><span data-stu-id="21a8c-479">Identification</span></span> 
- <span data-ttu-id="21a8c-480">ID</span><span class="sxs-lookup"><span data-stu-id="21a8c-480">ID</span></span> 
- <span data-ttu-id="21a8c-481">Identiteitskaart</span><span class="sxs-lookup"><span data-stu-id="21a8c-481">Identiteitskaart</span></span>
- <span data-ttu-id="21a8c-482">Registratie nummer</span><span class="sxs-lookup"><span data-stu-id="21a8c-482">Registratie nummer</span></span> 
- <span data-ttu-id="21a8c-483">Identificatie nummer</span><span class="sxs-lookup"><span data-stu-id="21a8c-483">Identificatie nummer</span></span> 
- <span data-ttu-id="21a8c-484">Identiteit</span><span class="sxs-lookup"><span data-stu-id="21a8c-484">Identiteit</span></span>
- <span data-ttu-id="21a8c-485">Registratie</span><span class="sxs-lookup"><span data-stu-id="21a8c-485">Registratie</span></span>
- <span data-ttu-id="21a8c-486">Identificatie</span><span class="sxs-lookup"><span data-stu-id="21a8c-486">Identificatie</span></span> 
- <span data-ttu-id="21a8c-487">Carte d’identité</span><span class="sxs-lookup"><span data-stu-id="21a8c-487">Carte d’identité</span></span> 
- <span data-ttu-id="21a8c-488">numéro d'immatriculation</span><span class="sxs-lookup"><span data-stu-id="21a8c-488">numéro d'immatriculation</span></span>
- <span data-ttu-id="21a8c-489">numéro d'identification</span><span class="sxs-lookup"><span data-stu-id="21a8c-489">numéro d'identification</span></span>
- <span data-ttu-id="21a8c-490">identité</span><span class="sxs-lookup"><span data-stu-id="21a8c-490">identité</span></span> 
- <span data-ttu-id="21a8c-491">inscription</span><span class="sxs-lookup"><span data-stu-id="21a8c-491">inscription</span></span> 
- <span data-ttu-id="21a8c-492">Identifikation</span><span class="sxs-lookup"><span data-stu-id="21a8c-492">Identifikation</span></span>
- <span data-ttu-id="21a8c-493">Identifizierung</span><span class="sxs-lookup"><span data-stu-id="21a8c-493">Identifizierung</span></span>
- <span data-ttu-id="21a8c-494">Identifikationsnummer</span><span class="sxs-lookup"><span data-stu-id="21a8c-494">Identifikationsnummer</span></span>
- <span data-ttu-id="21a8c-495">Personalausweis</span><span class="sxs-lookup"><span data-stu-id="21a8c-495">Personalausweis</span></span>
- <span data-ttu-id="21a8c-496">Registrierung</span><span class="sxs-lookup"><span data-stu-id="21a8c-496">Registrierung</span></span>
- <span data-ttu-id="21a8c-497">Registrationsnummer</span><span class="sxs-lookup"><span data-stu-id="21a8c-497">Registrationsnummer</span></span>

   
## <a name="brazil-cpf-number"></a><span data-ttu-id="21a8c-498">Número de CPF do Brasil</span><span class="sxs-lookup"><span data-stu-id="21a8c-498">Brazil CPF Number</span></span>

### <a name="format"></a><span data-ttu-id="21a8c-499">Format</span><span class="sxs-lookup"><span data-stu-id="21a8c-499">Format</span></span>

<span data-ttu-id="21a8c-500">11 dígitos que incluem um dígito de verificação e podem ser formatados ou não formatados</span><span class="sxs-lookup"><span data-stu-id="21a8c-500">11 digits that include a check digit and can be formatted or unformatted</span></span>

### <a name="pattern"></a><span data-ttu-id="21a8c-501">Padrão</span><span class="sxs-lookup"><span data-stu-id="21a8c-501">Pattern</span></span>

<span data-ttu-id="21a8c-502">Binário</span><span class="sxs-lookup"><span data-stu-id="21a8c-502">Formatted:</span></span>
- <span data-ttu-id="21a8c-503">Três dígitos</span><span class="sxs-lookup"><span data-stu-id="21a8c-503">Three digits</span></span> 
- <span data-ttu-id="21a8c-504">Um ponto </span><span class="sxs-lookup"><span data-stu-id="21a8c-504">A period</span></span> 
- <span data-ttu-id="21a8c-505">Três dígitos</span><span class="sxs-lookup"><span data-stu-id="21a8c-505">Three digits</span></span> 
- <span data-ttu-id="21a8c-506">Um ponto </span><span class="sxs-lookup"><span data-stu-id="21a8c-506">A period</span></span> 
- <span data-ttu-id="21a8c-507">Três dígitos</span><span class="sxs-lookup"><span data-stu-id="21a8c-507">Three digits</span></span> 
- <span data-ttu-id="21a8c-508">Um hífen</span><span class="sxs-lookup"><span data-stu-id="21a8c-508">A hyphen</span></span> 
- <span data-ttu-id="21a8c-509">Dois dígitos que são dígitos de verificação</span><span class="sxs-lookup"><span data-stu-id="21a8c-509">Two digits which are check digits</span></span>

<span data-ttu-id="21a8c-510">Não formatado</span><span class="sxs-lookup"><span data-stu-id="21a8c-510">Unformatted:</span></span>
- <span data-ttu-id="21a8c-511">11 dígitos em que os dois últimos dígitos são dígitos de verificação</span><span class="sxs-lookup"><span data-stu-id="21a8c-511">11 digits where the last two digits are check digits</span></span>

### <a name="checksum"></a><span data-ttu-id="21a8c-512">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="21a8c-512">Checksum</span></span>

<span data-ttu-id="21a8c-513">Sim</span><span class="sxs-lookup"><span data-stu-id="21a8c-513">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="21a8c-514">Definição</span><span class="sxs-lookup"><span data-stu-id="21a8c-514">Definition</span></span>

<span data-ttu-id="21a8c-515">Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="21a8c-515">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="21a8c-516">A função Func_brazil_cpf localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="21a8c-516">The function Func_brazil_cpf finds content that matches the pattern.</span></span>
- <span data-ttu-id="21a8c-517">Uma palavra-chave de Keyword_brazil_cpf for encontrada.</span><span class="sxs-lookup"><span data-stu-id="21a8c-517">A keyword from Keyword_brazil_cpf is found.</span></span>
- <span data-ttu-id="21a8c-518">A soma de verificação passa.</span><span class="sxs-lookup"><span data-stu-id="21a8c-518">The checksum passes.</span></span>

<span data-ttu-id="21a8c-519">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="21a8c-519">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="21a8c-520">A função Func_brazil_cpf localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="21a8c-520">The function Func_brazil_cpf finds content that matches the pattern.</span></span>
- <span data-ttu-id="21a8c-521">A soma de verificação passa.</span><span class="sxs-lookup"><span data-stu-id="21a8c-521">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="21a8c-522">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="21a8c-522">Keywords</span></span>

#### <a name="keywordbrazilcpf"></a><span data-ttu-id="21a8c-523">Keyword_brazil_cpf</span><span class="sxs-lookup"><span data-stu-id="21a8c-523">Keyword_brazil_cpf</span></span>

- <span data-ttu-id="21a8c-524">CPF</span><span class="sxs-lookup"><span data-stu-id="21a8c-524">CPF</span></span>
- <span data-ttu-id="21a8c-525">Identificador</span><span class="sxs-lookup"><span data-stu-id="21a8c-525">Identification</span></span>
- <span data-ttu-id="21a8c-526">Registro</span><span class="sxs-lookup"><span data-stu-id="21a8c-526">Registration</span></span>
- <span data-ttu-id="21a8c-527">Participação</span><span class="sxs-lookup"><span data-stu-id="21a8c-527">Revenue</span></span>
- <span data-ttu-id="21a8c-528">Cadastro de Pessoas Físicas</span><span class="sxs-lookup"><span data-stu-id="21a8c-528">Cadastro de Pessoas Físicas</span></span> 
- <span data-ttu-id="21a8c-529">Imposto</span><span class="sxs-lookup"><span data-stu-id="21a8c-529">Imposto</span></span> 
- <span data-ttu-id="21a8c-530">Identificação</span><span class="sxs-lookup"><span data-stu-id="21a8c-530">Identificação</span></span> 
- <span data-ttu-id="21a8c-531">Inscrição</span><span class="sxs-lookup"><span data-stu-id="21a8c-531">Inscrição</span></span> 
- <span data-ttu-id="21a8c-532">Receita</span><span class="sxs-lookup"><span data-stu-id="21a8c-532">Receita</span></span> 
   
## <a name="brazil-legal-entity-number-cnpj"></a><span data-ttu-id="21a8c-533">Número de Pessoa Jurídica (CNPJ) do Brasil</span><span class="sxs-lookup"><span data-stu-id="21a8c-533">Brazil Legal Entity Number (CNPJ)</span></span>

### <a name="format"></a><span data-ttu-id="21a8c-534">Format</span><span class="sxs-lookup"><span data-stu-id="21a8c-534">Format</span></span>

<span data-ttu-id="21a8c-535">14 dígitos que incluem um número de registro, o número da ramificação e dígitos de verificação, além de delimitadores de seleção</span><span class="sxs-lookup"><span data-stu-id="21a8c-535">14 digits that include a registration number, branch number, and check digits, plus delimiters</span></span>

### <a name="pattern"></a><span data-ttu-id="21a8c-536">Padrão</span><span class="sxs-lookup"><span data-stu-id="21a8c-536">Pattern</span></span>
<span data-ttu-id="21a8c-537">14 dígitos mais delimitadores:</span><span class="sxs-lookup"><span data-stu-id="21a8c-537">14 digits, plus delimiters:</span></span>
- <span data-ttu-id="21a8c-538">Dois dígitos</span><span class="sxs-lookup"><span data-stu-id="21a8c-538">Two digits</span></span> 
- <span data-ttu-id="21a8c-539">Um ponto </span><span class="sxs-lookup"><span data-stu-id="21a8c-539">A period</span></span> 
- <span data-ttu-id="21a8c-540">Três dígitos</span><span class="sxs-lookup"><span data-stu-id="21a8c-540">Three digits</span></span> 
- <span data-ttu-id="21a8c-541">Um ponto </span><span class="sxs-lookup"><span data-stu-id="21a8c-541">A period</span></span> 
- <span data-ttu-id="21a8c-542">Três dígitos (esses primeiros oito dígitos são o número de registro) </span><span class="sxs-lookup"><span data-stu-id="21a8c-542">Three digits (these first eight digits are the registration number)</span></span> 
- <span data-ttu-id="21a8c-543">Uma barra</span><span class="sxs-lookup"><span data-stu-id="21a8c-543">A forward slash</span></span> 
- <span data-ttu-id="21a8c-544">Número da ramificação de quatro dígitos </span><span class="sxs-lookup"><span data-stu-id="21a8c-544">Four-digit branch number</span></span> 
- <span data-ttu-id="21a8c-545">Um hífen</span><span class="sxs-lookup"><span data-stu-id="21a8c-545">A hyphen</span></span> 
- <span data-ttu-id="21a8c-546">Dois dígitos que são dígitos de verificação</span><span class="sxs-lookup"><span data-stu-id="21a8c-546">Two digits which are check digits</span></span>

### <a name="checksum"></a><span data-ttu-id="21a8c-547">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="21a8c-547">Checksum</span></span>

<span data-ttu-id="21a8c-548">Sim</span><span class="sxs-lookup"><span data-stu-id="21a8c-548">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="21a8c-549">Definição</span><span class="sxs-lookup"><span data-stu-id="21a8c-549">Definition</span></span>

<span data-ttu-id="21a8c-550">Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="21a8c-550">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="21a8c-551">A função Func_brazil_cnpj localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="21a8c-551">The function Func_brazil_cnpj finds content that matches the pattern.</span></span>
- <span data-ttu-id="21a8c-552">Uma palavra-chave de Keyword_brazil_cnpj for encontrada.</span><span class="sxs-lookup"><span data-stu-id="21a8c-552">A keyword from Keyword_brazil_cnpj is found.</span></span>
- <span data-ttu-id="21a8c-553">A soma de verificação passa.</span><span class="sxs-lookup"><span data-stu-id="21a8c-553">The checksum passes.</span></span>

<span data-ttu-id="21a8c-554">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="21a8c-554">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="21a8c-555">A função Func_brazil_cnpj localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="21a8c-555">The function Func_brazil_cnpj finds content that matches the pattern.</span></span>
- <span data-ttu-id="21a8c-556">A soma de verificação passa.</span><span class="sxs-lookup"><span data-stu-id="21a8c-556">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="21a8c-557">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="21a8c-557">Keywords</span></span>

#### <a name="keywordbrazilcnpj"></a><span data-ttu-id="21a8c-558">Keyword_brazil_cnpj</span><span class="sxs-lookup"><span data-stu-id="21a8c-558">Keyword_brazil_cnpj</span></span>

- <span data-ttu-id="21a8c-559">CNPJ</span><span class="sxs-lookup"><span data-stu-id="21a8c-559">CNPJ</span></span> 
- <span data-ttu-id="21a8c-560">CNPJ/MF</span><span class="sxs-lookup"><span data-stu-id="21a8c-560">CNPJ/MF</span></span> 
- <span data-ttu-id="21a8c-561">CNPJ-MF</span><span class="sxs-lookup"><span data-stu-id="21a8c-561">CNPJ-MF</span></span> 
- <span data-ttu-id="21a8c-562">Registro Nacional de Pessoas Jurídicas</span><span class="sxs-lookup"><span data-stu-id="21a8c-562">National Registry of Legal Entities</span></span> 
- <span data-ttu-id="21a8c-563">Registro de Contribuintes</span><span class="sxs-lookup"><span data-stu-id="21a8c-563">Taxpayers Registry</span></span> 
- <span data-ttu-id="21a8c-564">Pessoa jurídica</span><span class="sxs-lookup"><span data-stu-id="21a8c-564">Legal entity</span></span> 
- <span data-ttu-id="21a8c-565">Pessoas jurídicas</span><span class="sxs-lookup"><span data-stu-id="21a8c-565">Legal entities</span></span> 
- <span data-ttu-id="21a8c-566">Status do Registro</span><span class="sxs-lookup"><span data-stu-id="21a8c-566">Registration Status</span></span> 
- <span data-ttu-id="21a8c-567">Negócios</span><span class="sxs-lookup"><span data-stu-id="21a8c-567">Business</span></span> 
- <span data-ttu-id="21a8c-568">Empresa</span><span class="sxs-lookup"><span data-stu-id="21a8c-568">Company</span></span>
- <span data-ttu-id="21a8c-569">CNPJ</span><span class="sxs-lookup"><span data-stu-id="21a8c-569">CNPJ</span></span> 
- <span data-ttu-id="21a8c-570">Cadastro Nacional da Pessoa Jurídica</span><span class="sxs-lookup"><span data-stu-id="21a8c-570">Cadastro Nacional da Pessoa Jurídica</span></span> 
- <span data-ttu-id="21a8c-571">Cadastro Geral de Contribuintes</span><span class="sxs-lookup"><span data-stu-id="21a8c-571">Cadastro Geral de Contribuintes</span></span> 
- <span data-ttu-id="21a8c-572">CGC</span><span class="sxs-lookup"><span data-stu-id="21a8c-572">CGC</span></span> 
- <span data-ttu-id="21a8c-573">Pessoa jurídica</span><span class="sxs-lookup"><span data-stu-id="21a8c-573">Pessoa jurídica</span></span> 
- <span data-ttu-id="21a8c-574">Pessoas jurídicas</span><span class="sxs-lookup"><span data-stu-id="21a8c-574">Pessoas jurídicas</span></span> 
- <span data-ttu-id="21a8c-575">Situação cadastral</span><span class="sxs-lookup"><span data-stu-id="21a8c-575">Situação cadastral</span></span> 
- <span data-ttu-id="21a8c-576">Inscrição</span><span class="sxs-lookup"><span data-stu-id="21a8c-576">Inscrição</span></span> 
- <span data-ttu-id="21a8c-577">Empresa</span><span class="sxs-lookup"><span data-stu-id="21a8c-577">Empresa</span></span> 
   
## <a name="brazil-national-id-card-rg"></a><span data-ttu-id="21a8c-578">	Cartão de Identidade Nacional (RG) do Brasil</span><span class="sxs-lookup"><span data-stu-id="21a8c-578">Brazil National ID Card (RG)</span></span>

### <a name="format"></a><span data-ttu-id="21a8c-579">Format</span><span class="sxs-lookup"><span data-stu-id="21a8c-579">Format</span></span>

<span data-ttu-id="21a8c-580">Registro geral (formato antigo): nove dígitos</span><span class="sxs-lookup"><span data-stu-id="21a8c-580">Registro Geral (old format): Nine digits</span></span>

<span data-ttu-id="21a8c-581">Registro de identidade (RIC) (novo formato): 11 dígitos</span><span class="sxs-lookup"><span data-stu-id="21a8c-581">Registro de Identidade (RIC) (new format): 11 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="21a8c-582">Padrão</span><span class="sxs-lookup"><span data-stu-id="21a8c-582">Pattern</span></span>

<span data-ttu-id="21a8c-583">Registro Geral (formato antigo):</span><span class="sxs-lookup"><span data-stu-id="21a8c-583">Registro Geral (old format):</span></span>
- <span data-ttu-id="21a8c-584">Dois dígitos</span><span class="sxs-lookup"><span data-stu-id="21a8c-584">Two digits</span></span> 
- <span data-ttu-id="21a8c-585">Um ponto </span><span class="sxs-lookup"><span data-stu-id="21a8c-585">A period</span></span> 
- <span data-ttu-id="21a8c-586">Três dígitos</span><span class="sxs-lookup"><span data-stu-id="21a8c-586">Three digits</span></span> 
- <span data-ttu-id="21a8c-587">Um ponto </span><span class="sxs-lookup"><span data-stu-id="21a8c-587">A period</span></span> 
- <span data-ttu-id="21a8c-588">Três dígitos</span><span class="sxs-lookup"><span data-stu-id="21a8c-588">Three digits</span></span> 
- <span data-ttu-id="21a8c-589">Um hífen</span><span class="sxs-lookup"><span data-stu-id="21a8c-589">A hyphen</span></span> 
- <span data-ttu-id="21a8c-590">Um dígito que é um dígito de verificação</span><span class="sxs-lookup"><span data-stu-id="21a8c-590">One digit which is a check digit</span></span>

<span data-ttu-id="21a8c-591">Registro de identidade (RIC) (novo formato):</span><span class="sxs-lookup"><span data-stu-id="21a8c-591">Registro de Identidade (RIC) (new format):</span></span>
- <span data-ttu-id="21a8c-592">10 dígitos</span><span class="sxs-lookup"><span data-stu-id="21a8c-592">10 digits</span></span> 
- <span data-ttu-id="21a8c-593">Um hífen</span><span class="sxs-lookup"><span data-stu-id="21a8c-593">A hyphen</span></span> 
- <span data-ttu-id="21a8c-594">Um dígito que é um dígito de verificação</span><span class="sxs-lookup"><span data-stu-id="21a8c-594">One digit which is a check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="21a8c-595">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="21a8c-595">Checksum</span></span>

<span data-ttu-id="21a8c-596">Sim</span><span class="sxs-lookup"><span data-stu-id="21a8c-596">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="21a8c-597">Definição</span><span class="sxs-lookup"><span data-stu-id="21a8c-597">Definition</span></span>

<span data-ttu-id="21a8c-598">Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="21a8c-598">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="21a8c-599">A função Func_brazil_rg localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="21a8c-599">The function Func_brazil_rg finds content that matches the pattern.</span></span>
- <span data-ttu-id="21a8c-600">Uma palavra-chave de Keyword_brazil_rg for encontrada.</span><span class="sxs-lookup"><span data-stu-id="21a8c-600">A keyword from Keyword_brazil_rg is found.</span></span>
- <span data-ttu-id="21a8c-601">A soma de verificação passa.</span><span class="sxs-lookup"><span data-stu-id="21a8c-601">The checksum passes.</span></span>

<span data-ttu-id="21a8c-602">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="21a8c-602">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="21a8c-603">A função Func_brazil_rg localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="21a8c-603">The function Func_brazil_rg finds content that matches the pattern.</span></span>
- <span data-ttu-id="21a8c-604">A soma de verificação passa.</span><span class="sxs-lookup"><span data-stu-id="21a8c-604">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="21a8c-605">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="21a8c-605">Keywords</span></span>

#### <a name="keywordbrazilrg"></a><span data-ttu-id="21a8c-606">Keyword_brazil_rg</span><span class="sxs-lookup"><span data-stu-id="21a8c-606">Keyword_brazil_rg</span></span>

<span data-ttu-id="21a8c-607">Cédula de identidade ID nacional número de registro registro de identidade registro de geral RG (esta palavra-chave diferencia maiúsculas de minúsculas) RIC (essa palavra-chave diferencia maiúsculas de minúsculas)</span><span class="sxs-lookup"><span data-stu-id="21a8c-607">Cédula de identidade identity card national id número de rregistro registro de Iidentidade registro geral RG (this keyword is case sensitive) RIC (this keyword is case sensitive)</span></span> 
   
## <a name="canada-bank-account-number"></a><span data-ttu-id="21a8c-608">Número de conta bancária do Canadá</span><span class="sxs-lookup"><span data-stu-id="21a8c-608">Canada Bank Account Number</span></span>

### <a name="format"></a><span data-ttu-id="21a8c-609">Format</span><span class="sxs-lookup"><span data-stu-id="21a8c-609">Format</span></span>

<span data-ttu-id="21a8c-610">Sete ou doze dígitos</span><span class="sxs-lookup"><span data-stu-id="21a8c-610">Seven or twelve digits</span></span>

### <a name="pattern"></a><span data-ttu-id="21a8c-611">Padrão</span><span class="sxs-lookup"><span data-stu-id="21a8c-611">Pattern</span></span>

<span data-ttu-id="21a8c-612">Um número de conta bancária do Canadá tem sete ou doze dígitos.</span><span class="sxs-lookup"><span data-stu-id="21a8c-612">A Canada Bank Account Number is seven or twelve digits.</span></span>

<span data-ttu-id="21a8c-613">Um número de trânsito de conta bancária do Canadá tem:</span><span class="sxs-lookup"><span data-stu-id="21a8c-613">A Canada bank account transit number is:</span></span>
- <span data-ttu-id="21a8c-614">Cinco dígitos</span><span class="sxs-lookup"><span data-stu-id="21a8c-614">Five digits</span></span> 
- <span data-ttu-id="21a8c-615">Um hífen</span><span class="sxs-lookup"><span data-stu-id="21a8c-615">A hyphen</span></span> 
- <span data-ttu-id="21a8c-616">Três dígitos ou</span><span class="sxs-lookup"><span data-stu-id="21a8c-616">Three digits OR</span></span>
- <span data-ttu-id="21a8c-617">Um zero "0"</span><span class="sxs-lookup"><span data-stu-id="21a8c-617">A zero "0"</span></span> 
- <span data-ttu-id="21a8c-618">Oito dígitos</span><span class="sxs-lookup"><span data-stu-id="21a8c-618">Eight digits</span></span>

### <a name="checksum"></a><span data-ttu-id="21a8c-619">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="21a8c-619">Checksum</span></span>

<span data-ttu-id="21a8c-620">Não</span><span class="sxs-lookup"><span data-stu-id="21a8c-620">No</span></span>

### <a name="definition"></a><span data-ttu-id="21a8c-621">Definição</span><span class="sxs-lookup"><span data-stu-id="21a8c-621">Definition</span></span>

<span data-ttu-id="21a8c-622">Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="21a8c-622">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="21a8c-623">A expressão regular Regex_canada_bank_account_number localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="21a8c-623">The regular expression Regex_canada_bank_account_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="21a8c-624">Uma palavra-chave de Keyword_canada_bank_account_number for encontrada.</span><span class="sxs-lookup"><span data-stu-id="21a8c-624">A keyword from Keyword_canada_bank_account_number is found.</span></span>
- <span data-ttu-id="21a8c-625">A expressão regular Regex_canada_bank_account_transit_number localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="21a8c-625">The regular expression Regex_canada_bank_account_transit_number finds content that matches the pattern.</span></span>

<span data-ttu-id="21a8c-626">Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="21a8c-626">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="21a8c-627">A expressão regular Regex_canada_bank_account_number localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="21a8c-627">The regular expression Regex_canada_bank_account_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="21a8c-628">Uma palavra-chave de Keyword_canada_bank_account_number for encontrada.</span><span class="sxs-lookup"><span data-stu-id="21a8c-628">A keyword from Keyword_canada_bank_account_number is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="21a8c-629">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="21a8c-629">Keywords</span></span>

#### <a name="keywordcanadabankaccountnumber"></a><span data-ttu-id="21a8c-630">Keyword_canada_bank_account_number</span><span class="sxs-lookup"><span data-stu-id="21a8c-630">Keyword_canada_bank_account_number</span></span>

- <span data-ttu-id="21a8c-631">canada savings bonds</span><span class="sxs-lookup"><span data-stu-id="21a8c-631">canada savings bonds</span></span>
- <span data-ttu-id="21a8c-632">canada revenue agency</span><span class="sxs-lookup"><span data-stu-id="21a8c-632">canada revenue agency</span></span>
- <span data-ttu-id="21a8c-633">canadian financial institution</span><span class="sxs-lookup"><span data-stu-id="21a8c-633">canadian financial institution</span></span>
- <span data-ttu-id="21a8c-634">direct deposit form</span><span class="sxs-lookup"><span data-stu-id="21a8c-634">direct deposit form</span></span>
- <span data-ttu-id="21a8c-635">canadian citizen</span><span class="sxs-lookup"><span data-stu-id="21a8c-635">canadian citizen</span></span>
- <span data-ttu-id="21a8c-636">legal representative</span><span class="sxs-lookup"><span data-stu-id="21a8c-636">legal representative</span></span>
- <span data-ttu-id="21a8c-637">notary public</span><span class="sxs-lookup"><span data-stu-id="21a8c-637">notary public</span></span>
- <span data-ttu-id="21a8c-638">commissioner for oaths</span><span class="sxs-lookup"><span data-stu-id="21a8c-638">commissioner for oaths</span></span>
- <span data-ttu-id="21a8c-639">child care benefit</span><span class="sxs-lookup"><span data-stu-id="21a8c-639">child care benefit</span></span>
- <span data-ttu-id="21a8c-640">universal child care</span><span class="sxs-lookup"><span data-stu-id="21a8c-640">universal child care</span></span>
- <span data-ttu-id="21a8c-641">canada child tax benefit</span><span class="sxs-lookup"><span data-stu-id="21a8c-641">canada child tax benefit</span></span>
- <span data-ttu-id="21a8c-642">income tax benefit</span><span class="sxs-lookup"><span data-stu-id="21a8c-642">income tax benefit</span></span>
- <span data-ttu-id="21a8c-643">harmonized sales tax</span><span class="sxs-lookup"><span data-stu-id="21a8c-643">harmonized sales tax</span></span>
- <span data-ttu-id="21a8c-644">social insurance number</span><span class="sxs-lookup"><span data-stu-id="21a8c-644">social insurance number</span></span>
- <span data-ttu-id="21a8c-645">income tax refund</span><span class="sxs-lookup"><span data-stu-id="21a8c-645">income tax refund</span></span>
- <span data-ttu-id="21a8c-646">child tax benefit</span><span class="sxs-lookup"><span data-stu-id="21a8c-646">child tax benefit</span></span>
- <span data-ttu-id="21a8c-647">territorial payments</span><span class="sxs-lookup"><span data-stu-id="21a8c-647">territorial payments</span></span>
- <span data-ttu-id="21a8c-648">institution number</span><span class="sxs-lookup"><span data-stu-id="21a8c-648">institution number</span></span>
- <span data-ttu-id="21a8c-649">deposit request</span><span class="sxs-lookup"><span data-stu-id="21a8c-649">deposit request</span></span>
- <span data-ttu-id="21a8c-650">banking information</span><span class="sxs-lookup"><span data-stu-id="21a8c-650">banking information</span></span>
- <span data-ttu-id="21a8c-651">direct deposit</span><span class="sxs-lookup"><span data-stu-id="21a8c-651">direct deposit</span></span>
   
## <a name="canada-drivers-license-number"></a><span data-ttu-id="21a8c-652">Número de carteira de motorista do Canadá</span><span class="sxs-lookup"><span data-stu-id="21a8c-652">Canada Driver's License Number</span></span>

### <a name="format"></a><span data-ttu-id="21a8c-653">Format</span><span class="sxs-lookup"><span data-stu-id="21a8c-653">Format</span></span>

<span data-ttu-id="21a8c-654">Varia por província</span><span class="sxs-lookup"><span data-stu-id="21a8c-654">Varies by province</span></span>

### <a name="pattern"></a><span data-ttu-id="21a8c-655">Padrão</span><span class="sxs-lookup"><span data-stu-id="21a8c-655">Pattern</span></span>

<span data-ttu-id="21a8c-656">Vários padrões que abrangem Alberta, Columbia Britânica, Manitoba, New Brunswick, Newfoundland/Labrador, Nova Escócia, Ontário, Ilha do Príncipe Eduardo, Quebec e Saskatchewan</span><span class="sxs-lookup"><span data-stu-id="21a8c-656">Various patterns covering Alberta, British Columbia, Manitoba, New Brunswick, Newfoundland/Labrador, Nova Scotia, Ontario, Prince Edward Island, Quebec, and Saskatchewan</span></span>

### <a name="checksum"></a><span data-ttu-id="21a8c-657">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="21a8c-657">Checksum</span></span>

<span data-ttu-id="21a8c-658">Não</span><span class="sxs-lookup"><span data-stu-id="21a8c-658">No</span></span>

### <a name="definition"></a><span data-ttu-id="21a8c-659">Definição</span><span class="sxs-lookup"><span data-stu-id="21a8c-659">Definition</span></span>

<span data-ttu-id="21a8c-660">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="21a8c-660">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="21a8c-661">A função Func_[province_name]_drivers_license_number localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="21a8c-661">The function Func_[province_name]_drivers_license_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="21a8c-662">Uma palavra-chave de Keyword_[province_name]_drivers_license_name for encontrada.</span><span class="sxs-lookup"><span data-stu-id="21a8c-662">A keyword from Keyword_[province_name]_drivers_license_name is found.</span></span>
- <span data-ttu-id="21a8c-663">Uma palavra-chave de Keyword_canada_drivers_license for encontrada.</span><span class="sxs-lookup"><span data-stu-id="21a8c-663">A keyword from Keyword_canada_drivers_license is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="21a8c-664">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="21a8c-664">Keywords</span></span>

#### <a name="keywordprovincenamedriverslicensename"></a><span data-ttu-id="21a8c-665">Keyword_ [province_name] _drivers_license_name</span><span class="sxs-lookup"><span data-stu-id="21a8c-665">Keyword_[province_name]_drivers_license_name</span></span>

- <span data-ttu-id="21a8c-666">A abreviação da província, por exemplo AB</span><span class="sxs-lookup"><span data-stu-id="21a8c-666">The province abbreviation, for example AB</span></span>
- <span data-ttu-id="21a8c-667">O nome da província, por exemplo, Alberta</span><span class="sxs-lookup"><span data-stu-id="21a8c-667">The province name, for example Alberta</span></span>

#### <a name="keywordcanadadriverslicense"></a><span data-ttu-id="21a8c-668">Keyword_canada_drivers_license</span><span class="sxs-lookup"><span data-stu-id="21a8c-668">Keyword_canada_drivers_license</span></span>

- <span data-ttu-id="21a8c-669">DISTRIBUIÇÃO</span><span class="sxs-lookup"><span data-stu-id="21a8c-669">DL</span></span>
- <span data-ttu-id="21a8c-670">DL</span><span class="sxs-lookup"><span data-stu-id="21a8c-670">DLS</span></span>
- <span data-ttu-id="21a8c-671">CDL</span><span class="sxs-lookup"><span data-stu-id="21a8c-671">CDL</span></span>
- <span data-ttu-id="21a8c-672">CDLS</span><span class="sxs-lookup"><span data-stu-id="21a8c-672">CDLS</span></span>
- <span data-ttu-id="21a8c-673">DriverLic</span><span class="sxs-lookup"><span data-stu-id="21a8c-673">DriverLic</span></span>
- <span data-ttu-id="21a8c-674">DriverLics</span><span class="sxs-lookup"><span data-stu-id="21a8c-674">DriverLics</span></span>
- <span data-ttu-id="21a8c-675">DriverLicense</span><span class="sxs-lookup"><span data-stu-id="21a8c-675">DriverLicense</span></span>
- <span data-ttu-id="21a8c-676">DriverLicenses</span><span class="sxs-lookup"><span data-stu-id="21a8c-676">DriverLicenses</span></span>
- <span data-ttu-id="21a8c-677">DriverLicence</span><span class="sxs-lookup"><span data-stu-id="21a8c-677">DriverLicence</span></span>
- <span data-ttu-id="21a8c-678">DriverLicences</span><span class="sxs-lookup"><span data-stu-id="21a8c-678">DriverLicences</span></span>
- <span data-ttu-id="21a8c-679">Driver Lic</span><span class="sxs-lookup"><span data-stu-id="21a8c-679">Driver Lic</span></span>
- <span data-ttu-id="21a8c-680">Driver Lics</span><span class="sxs-lookup"><span data-stu-id="21a8c-680">Driver Lics</span></span>
- <span data-ttu-id="21a8c-681">Driver License</span><span class="sxs-lookup"><span data-stu-id="21a8c-681">Driver License</span></span>
- <span data-ttu-id="21a8c-682">Driver Licenses</span><span class="sxs-lookup"><span data-stu-id="21a8c-682">Driver Licenses</span></span>
- <span data-ttu-id="21a8c-683">Driver Licence</span><span class="sxs-lookup"><span data-stu-id="21a8c-683">Driver Licence</span></span>
- <span data-ttu-id="21a8c-684">Driver Licences</span><span class="sxs-lookup"><span data-stu-id="21a8c-684">Driver Licences</span></span>
- <span data-ttu-id="21a8c-685">DriversLic</span><span class="sxs-lookup"><span data-stu-id="21a8c-685">DriversLic</span></span>
- <span data-ttu-id="21a8c-686">DriversLics</span><span class="sxs-lookup"><span data-stu-id="21a8c-686">DriversLics</span></span>
- <span data-ttu-id="21a8c-687">DriversLicence</span><span class="sxs-lookup"><span data-stu-id="21a8c-687">DriversLicence</span></span>
- <span data-ttu-id="21a8c-688">DriversLicences</span><span class="sxs-lookup"><span data-stu-id="21a8c-688">DriversLicences</span></span>
- <span data-ttu-id="21a8c-689">DriversLicense</span><span class="sxs-lookup"><span data-stu-id="21a8c-689">DriversLicense</span></span>
- <span data-ttu-id="21a8c-690">DriversLicenses</span><span class="sxs-lookup"><span data-stu-id="21a8c-690">DriversLicenses</span></span>
- <span data-ttu-id="21a8c-691">Drivers Lic</span><span class="sxs-lookup"><span data-stu-id="21a8c-691">Drivers Lic</span></span>
- <span data-ttu-id="21a8c-692">Drivers Lics</span><span class="sxs-lookup"><span data-stu-id="21a8c-692">Drivers Lics</span></span>
- <span data-ttu-id="21a8c-693">Drivers License</span><span class="sxs-lookup"><span data-stu-id="21a8c-693">Drivers License</span></span>
- <span data-ttu-id="21a8c-694">Drivers Licenses</span><span class="sxs-lookup"><span data-stu-id="21a8c-694">Drivers Licenses</span></span>
- <span data-ttu-id="21a8c-695">Drivers Licence</span><span class="sxs-lookup"><span data-stu-id="21a8c-695">Drivers Licence</span></span>
- <span data-ttu-id="21a8c-696">Drivers Licences</span><span class="sxs-lookup"><span data-stu-id="21a8c-696">Drivers Licences</span></span>
- <span data-ttu-id="21a8c-697">Driver'Lic</span><span class="sxs-lookup"><span data-stu-id="21a8c-697">Driver'Lic</span></span>
- <span data-ttu-id="21a8c-698">Driver'Lics</span><span class="sxs-lookup"><span data-stu-id="21a8c-698">Driver'Lics</span></span>
- <span data-ttu-id="21a8c-699">Driver'License</span><span class="sxs-lookup"><span data-stu-id="21a8c-699">Driver'License</span></span>
- <span data-ttu-id="21a8c-700">Driver'Licenses</span><span class="sxs-lookup"><span data-stu-id="21a8c-700">Driver'Licenses</span></span>
- <span data-ttu-id="21a8c-701">Driver'Licence</span><span class="sxs-lookup"><span data-stu-id="21a8c-701">Driver'Licence</span></span>
- <span data-ttu-id="21a8c-702">Driver'Licences</span><span class="sxs-lookup"><span data-stu-id="21a8c-702">Driver'Licences</span></span>
- <span data-ttu-id="21a8c-703">Driver'Lic</span><span class="sxs-lookup"><span data-stu-id="21a8c-703">Driver' Lic</span></span>
- <span data-ttu-id="21a8c-704">Driver' Lics</span><span class="sxs-lookup"><span data-stu-id="21a8c-704">Driver' Lics</span></span>
- <span data-ttu-id="21a8c-705">Driver' License</span><span class="sxs-lookup"><span data-stu-id="21a8c-705">Driver' License</span></span>
- <span data-ttu-id="21a8c-706">Driver'Licenses</span><span class="sxs-lookup"><span data-stu-id="21a8c-706">Driver' Licenses</span></span>
- <span data-ttu-id="21a8c-707">Driver'Licence</span><span class="sxs-lookup"><span data-stu-id="21a8c-707">Driver' Licence</span></span>
- <span data-ttu-id="21a8c-708">Driver'Licences</span><span class="sxs-lookup"><span data-stu-id="21a8c-708">Driver' Licences</span></span>
- <span data-ttu-id="21a8c-709">Driver'sLic</span><span class="sxs-lookup"><span data-stu-id="21a8c-709">Driver'sLic</span></span>
- <span data-ttu-id="21a8c-710">Driver'sLics</span><span class="sxs-lookup"><span data-stu-id="21a8c-710">Driver'sLics</span></span>
- <span data-ttu-id="21a8c-711">Driver'sLicense</span><span class="sxs-lookup"><span data-stu-id="21a8c-711">Driver'sLicense</span></span>
- <span data-ttu-id="21a8c-712">Driver'sLicenses</span><span class="sxs-lookup"><span data-stu-id="21a8c-712">Driver'sLicenses</span></span>
- <span data-ttu-id="21a8c-713">Driver'sLicence</span><span class="sxs-lookup"><span data-stu-id="21a8c-713">Driver'sLicence</span></span>
- <span data-ttu-id="21a8c-714">Driver'sLicences</span><span class="sxs-lookup"><span data-stu-id="21a8c-714">Driver'sLicences</span></span>
- <span data-ttu-id="21a8c-715">Driver's Lic</span><span class="sxs-lookup"><span data-stu-id="21a8c-715">Driver's Lic</span></span>
- <span data-ttu-id="21a8c-716">Driver's Lics</span><span class="sxs-lookup"><span data-stu-id="21a8c-716">Driver's Lics</span></span>
- <span data-ttu-id="21a8c-717">Driver's License</span><span class="sxs-lookup"><span data-stu-id="21a8c-717">Driver's License</span></span>
- <span data-ttu-id="21a8c-718">Driver's Licenses</span><span class="sxs-lookup"><span data-stu-id="21a8c-718">Driver's Licenses</span></span>
- <span data-ttu-id="21a8c-719">Driver's Licence</span><span class="sxs-lookup"><span data-stu-id="21a8c-719">Driver's Licence</span></span>
- <span data-ttu-id="21a8c-720">Driver's Licences</span><span class="sxs-lookup"><span data-stu-id="21a8c-720">Driver's Licences</span></span>
- <span data-ttu-id="21a8c-721">Permis de Conduire</span><span class="sxs-lookup"><span data-stu-id="21a8c-721">Permis de Conduire</span></span>
- <span data-ttu-id="21a8c-722">id</span><span class="sxs-lookup"><span data-stu-id="21a8c-722">id</span></span>
- <span data-ttu-id="21a8c-723">ids</span><span class="sxs-lookup"><span data-stu-id="21a8c-723">ids</span></span>
- <span data-ttu-id="21a8c-724">idcard number</span><span class="sxs-lookup"><span data-stu-id="21a8c-724">idcard number</span></span>
- <span data-ttu-id="21a8c-725">idcard numbers</span><span class="sxs-lookup"><span data-stu-id="21a8c-725">idcard numbers</span></span>
- <span data-ttu-id="21a8c-726">idcard #</span><span class="sxs-lookup"><span data-stu-id="21a8c-726">idcard #</span></span>
- <span data-ttu-id="21a8c-727">idcard #s</span><span class="sxs-lookup"><span data-stu-id="21a8c-727">idcard #s</span></span>
- <span data-ttu-id="21a8c-728">idcard card</span><span class="sxs-lookup"><span data-stu-id="21a8c-728">idcard card</span></span>
- <span data-ttu-id="21a8c-729">idcard cards</span><span class="sxs-lookup"><span data-stu-id="21a8c-729">idcard cards</span></span>
- <span data-ttu-id="21a8c-730">idcard</span><span class="sxs-lookup"><span data-stu-id="21a8c-730">idcard</span></span>
- <span data-ttu-id="21a8c-731">identification number</span><span class="sxs-lookup"><span data-stu-id="21a8c-731">identification number</span></span>
- <span data-ttu-id="21a8c-732">identification numbers</span><span class="sxs-lookup"><span data-stu-id="21a8c-732">identification numbers</span></span>
- <span data-ttu-id="21a8c-733">identification #</span><span class="sxs-lookup"><span data-stu-id="21a8c-733">identification #</span></span>
- <span data-ttu-id="21a8c-734">identification #s</span><span class="sxs-lookup"><span data-stu-id="21a8c-734">identification #s</span></span>
- <span data-ttu-id="21a8c-735">identification card</span><span class="sxs-lookup"><span data-stu-id="21a8c-735">identification card</span></span>
- <span data-ttu-id="21a8c-736">identification cards</span><span class="sxs-lookup"><span data-stu-id="21a8c-736">identification cards</span></span>
- <span data-ttu-id="21a8c-737">identificador</span><span class="sxs-lookup"><span data-stu-id="21a8c-737">identification</span></span> 
- <span data-ttu-id="21a8c-738">DISTRIBUIÇÃO</span><span class="sxs-lookup"><span data-stu-id="21a8c-738">DL#</span></span>
- <span data-ttu-id="21a8c-739">DL</span><span class="sxs-lookup"><span data-stu-id="21a8c-739">DLS#</span></span> 
- <span data-ttu-id="21a8c-740">CDL</span><span class="sxs-lookup"><span data-stu-id="21a8c-740">CDL#</span></span> 
- <span data-ttu-id="21a8c-741">CDLS #</span><span class="sxs-lookup"><span data-stu-id="21a8c-741">CDLS#</span></span> 
- <span data-ttu-id="21a8c-742">DriverLic #</span><span class="sxs-lookup"><span data-stu-id="21a8c-742">DriverLic#</span></span> 
- <span data-ttu-id="21a8c-743">DriverLics #</span><span class="sxs-lookup"><span data-stu-id="21a8c-743">DriverLics#</span></span> 
- <span data-ttu-id="21a8c-744">DriverLicense #</span><span class="sxs-lookup"><span data-stu-id="21a8c-744">DriverLicense#</span></span> 
- <span data-ttu-id="21a8c-745">DriverLicenses #</span><span class="sxs-lookup"><span data-stu-id="21a8c-745">DriverLicenses#</span></span> 
- <span data-ttu-id="21a8c-746">DriverLicence #</span><span class="sxs-lookup"><span data-stu-id="21a8c-746">DriverLicence#</span></span> 
- <span data-ttu-id="21a8c-747">DriverLicences #</span><span class="sxs-lookup"><span data-stu-id="21a8c-747">DriverLicences#</span></span> 
- <span data-ttu-id="21a8c-748">Driver Lic#</span><span class="sxs-lookup"><span data-stu-id="21a8c-748">Driver Lic#</span></span>
- <span data-ttu-id="21a8c-749">Driver Lics#</span><span class="sxs-lookup"><span data-stu-id="21a8c-749">Driver Lics#</span></span> 
- <span data-ttu-id="21a8c-750">Driver License#</span><span class="sxs-lookup"><span data-stu-id="21a8c-750">Driver License#</span></span> 
- <span data-ttu-id="21a8c-751">Driver Licenses#</span><span class="sxs-lookup"><span data-stu-id="21a8c-751">Driver Licenses#</span></span> 
- <span data-ttu-id="21a8c-752">Driver License#</span><span class="sxs-lookup"><span data-stu-id="21a8c-752">Driver License#</span></span> 
- <span data-ttu-id="21a8c-753">Driver Licences#</span><span class="sxs-lookup"><span data-stu-id="21a8c-753">Driver Licences#</span></span> 
- <span data-ttu-id="21a8c-754">DriversLic #</span><span class="sxs-lookup"><span data-stu-id="21a8c-754">DriversLic#</span></span> 
- <span data-ttu-id="21a8c-755">DriversLics #</span><span class="sxs-lookup"><span data-stu-id="21a8c-755">DriversLics#</span></span> 
- <span data-ttu-id="21a8c-756">DriversLicense #</span><span class="sxs-lookup"><span data-stu-id="21a8c-756">DriversLicense#</span></span> 
- <span data-ttu-id="21a8c-757">DriversLicenses #</span><span class="sxs-lookup"><span data-stu-id="21a8c-757">DriversLicenses#</span></span> 
- <span data-ttu-id="21a8c-758">DriversLicence #</span><span class="sxs-lookup"><span data-stu-id="21a8c-758">DriversLicence#</span></span> 
- <span data-ttu-id="21a8c-759">DriversLicences #</span><span class="sxs-lookup"><span data-stu-id="21a8c-759">DriversLicences#</span></span> 
- <span data-ttu-id="21a8c-760">Drivers Lic#</span><span class="sxs-lookup"><span data-stu-id="21a8c-760">Drivers Lic#</span></span> 
- <span data-ttu-id="21a8c-761">Drivers Lics#</span><span class="sxs-lookup"><span data-stu-id="21a8c-761">Drivers Lics#</span></span> 
- <span data-ttu-id="21a8c-762">Drivers License#</span><span class="sxs-lookup"><span data-stu-id="21a8c-762">Drivers License#</span></span> 
- <span data-ttu-id="21a8c-763">Drivers Licenses#</span><span class="sxs-lookup"><span data-stu-id="21a8c-763">Drivers Licenses#</span></span> 
- <span data-ttu-id="21a8c-764">Drivers Licence#</span><span class="sxs-lookup"><span data-stu-id="21a8c-764">Drivers Licence#</span></span> 
- <span data-ttu-id="21a8c-765">Drivers Licences#</span><span class="sxs-lookup"><span data-stu-id="21a8c-765">Drivers Licences#</span></span> 
- <span data-ttu-id="21a8c-766">Driver'Lic #</span><span class="sxs-lookup"><span data-stu-id="21a8c-766">Driver'Lic#</span></span> 
- <span data-ttu-id="21a8c-767">Driver'Lics #</span><span class="sxs-lookup"><span data-stu-id="21a8c-767">Driver'Lics#</span></span> 
- <span data-ttu-id="21a8c-768">Driver'License #</span><span class="sxs-lookup"><span data-stu-id="21a8c-768">Driver'License#</span></span> 
- <span data-ttu-id="21a8c-769">Driver'Licenses #</span><span class="sxs-lookup"><span data-stu-id="21a8c-769">Driver'Licenses#</span></span> 
- <span data-ttu-id="21a8c-770">Driver'Licence #</span><span class="sxs-lookup"><span data-stu-id="21a8c-770">Driver'Licence#</span></span> 
- <span data-ttu-id="21a8c-771">Driver'Licences #</span><span class="sxs-lookup"><span data-stu-id="21a8c-771">Driver'Licences#</span></span> 
- <span data-ttu-id="21a8c-772">Driver'Lic#</span><span class="sxs-lookup"><span data-stu-id="21a8c-772">Driver' Lic#</span></span> 
- <span data-ttu-id="21a8c-773">Driver' Lics#</span><span class="sxs-lookup"><span data-stu-id="21a8c-773">Driver' Lics#</span></span> 
- <span data-ttu-id="21a8c-774">Driver' License#</span><span class="sxs-lookup"><span data-stu-id="21a8c-774">Driver' License#</span></span> 
- <span data-ttu-id="21a8c-775">Driver'Licenses#</span><span class="sxs-lookup"><span data-stu-id="21a8c-775">Driver' Licenses#</span></span> 
- <span data-ttu-id="21a8c-776">Driver'Licence#</span><span class="sxs-lookup"><span data-stu-id="21a8c-776">Driver' Licence#</span></span> 
- <span data-ttu-id="21a8c-777">Driver'Licences#</span><span class="sxs-lookup"><span data-stu-id="21a8c-777">Driver' Licences#</span></span> 
- <span data-ttu-id="21a8c-778">Driver'sLic #</span><span class="sxs-lookup"><span data-stu-id="21a8c-778">Driver'sLic#</span></span> 
- <span data-ttu-id="21a8c-779">Driver'sLics #</span><span class="sxs-lookup"><span data-stu-id="21a8c-779">Driver'sLics#</span></span> 
- <span data-ttu-id="21a8c-780">Driver'sLicense #</span><span class="sxs-lookup"><span data-stu-id="21a8c-780">Driver'sLicense#</span></span> 
- <span data-ttu-id="21a8c-781">Driver'sLicenses #</span><span class="sxs-lookup"><span data-stu-id="21a8c-781">Driver'sLicenses#</span></span> 
- <span data-ttu-id="21a8c-782">Driver'sLicence #</span><span class="sxs-lookup"><span data-stu-id="21a8c-782">Driver'sLicence#</span></span> 
- <span data-ttu-id="21a8c-783">Driver'sLicences #</span><span class="sxs-lookup"><span data-stu-id="21a8c-783">Driver'sLicences#</span></span> 
- <span data-ttu-id="21a8c-784">Driver's Lic#</span><span class="sxs-lookup"><span data-stu-id="21a8c-784">Driver's Lic#</span></span> 
- <span data-ttu-id="21a8c-785">Driver's Lics#</span><span class="sxs-lookup"><span data-stu-id="21a8c-785">Driver's Lics#</span></span> 
- <span data-ttu-id="21a8c-786">Driver's License#</span><span class="sxs-lookup"><span data-stu-id="21a8c-786">Driver's License#</span></span> 
- <span data-ttu-id="21a8c-787">Driver's Licenses#</span><span class="sxs-lookup"><span data-stu-id="21a8c-787">Driver's Licenses#</span></span> 
- <span data-ttu-id="21a8c-788">Driver's Licence#</span><span class="sxs-lookup"><span data-stu-id="21a8c-788">Driver's Licence#</span></span> 
- <span data-ttu-id="21a8c-789">Driver's Licences#</span><span class="sxs-lookup"><span data-stu-id="21a8c-789">Driver's Licences#</span></span> 
- <span data-ttu-id="21a8c-790">Permis de Conduire#</span><span class="sxs-lookup"><span data-stu-id="21a8c-790">Permis de Conduire#</span></span> 
- <span data-ttu-id="21a8c-791">ID</span><span class="sxs-lookup"><span data-stu-id="21a8c-791">id#</span></span> 
- <span data-ttu-id="21a8c-792">código</span><span class="sxs-lookup"><span data-stu-id="21a8c-792">ids#</span></span> 
- <span data-ttu-id="21a8c-793">idcard card#</span><span class="sxs-lookup"><span data-stu-id="21a8c-793">idcard card#</span></span> 
- <span data-ttu-id="21a8c-794">idcard cards#</span><span class="sxs-lookup"><span data-stu-id="21a8c-794">idcard cards#</span></span> 
- <span data-ttu-id="21a8c-795">idcard #</span><span class="sxs-lookup"><span data-stu-id="21a8c-795">idcard#</span></span> 
- <span data-ttu-id="21a8c-796">identification card#</span><span class="sxs-lookup"><span data-stu-id="21a8c-796">identification card#</span></span> 
- <span data-ttu-id="21a8c-797">identification cards#</span><span class="sxs-lookup"><span data-stu-id="21a8c-797">identification cards#</span></span> 
- <span data-ttu-id="21a8c-798">identificador</span><span class="sxs-lookup"><span data-stu-id="21a8c-798">identification#</span></span> 
   
## <a name="canada-health-service-number"></a><span data-ttu-id="21a8c-799">Número de serviço de saúde do Canadá</span><span class="sxs-lookup"><span data-stu-id="21a8c-799">Canada Health Service Number</span></span>

### <a name="format"></a><span data-ttu-id="21a8c-800">Format</span><span class="sxs-lookup"><span data-stu-id="21a8c-800">Format</span></span>

<span data-ttu-id="21a8c-801">10 dígitos</span><span class="sxs-lookup"><span data-stu-id="21a8c-801">10 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="21a8c-802">Padrão</span><span class="sxs-lookup"><span data-stu-id="21a8c-802">Pattern</span></span>

<span data-ttu-id="21a8c-803">10 dígitos</span><span class="sxs-lookup"><span data-stu-id="21a8c-803">10 digits</span></span>

### <a name="checksum"></a><span data-ttu-id="21a8c-804">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="21a8c-804">Checksum</span></span>

<span data-ttu-id="21a8c-805">Não</span><span class="sxs-lookup"><span data-stu-id="21a8c-805">No</span></span>

### <a name="definition"></a><span data-ttu-id="21a8c-806">Definição</span><span class="sxs-lookup"><span data-stu-id="21a8c-806">Definition</span></span>

<span data-ttu-id="21a8c-807">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="21a8c-807">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="21a8c-808">A expressão regular Regex_canada_health_service_number localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="21a8c-808">The regular expression Regex_canada_health_service_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="21a8c-809">Uma palavra-chave de Keyword_canada_health_service_number for encontrada.</span><span class="sxs-lookup"><span data-stu-id="21a8c-809">A keyword from Keyword_canada_health_service_number is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="21a8c-810">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="21a8c-810">Keywords</span></span>

#### <a name="keywordcanadahealthservicenumber"></a><span data-ttu-id="21a8c-811">Keyword_canada_health_service_number</span><span class="sxs-lookup"><span data-stu-id="21a8c-811">Keyword_canada_health_service_number</span></span>

- <span data-ttu-id="21a8c-812">personal health number</span><span class="sxs-lookup"><span data-stu-id="21a8c-812">personal health number</span></span>
- <span data-ttu-id="21a8c-813">patient information</span><span class="sxs-lookup"><span data-stu-id="21a8c-813">patient information</span></span>
- <span data-ttu-id="21a8c-814">health services</span><span class="sxs-lookup"><span data-stu-id="21a8c-814">health services</span></span>
- <span data-ttu-id="21a8c-815">speciality services</span><span class="sxs-lookup"><span data-stu-id="21a8c-815">speciality services</span></span>
- <span data-ttu-id="21a8c-816">automobile accident</span><span class="sxs-lookup"><span data-stu-id="21a8c-816">automobile accident</span></span>
- <span data-ttu-id="21a8c-817">patient hospital</span><span class="sxs-lookup"><span data-stu-id="21a8c-817">patient hospital</span></span>
- <span data-ttu-id="21a8c-818">psychiatrist</span><span class="sxs-lookup"><span data-stu-id="21a8c-818">psychiatrist</span></span>
- <span data-ttu-id="21a8c-819">workers compensation</span><span class="sxs-lookup"><span data-stu-id="21a8c-819">workers compensation</span></span>
- <span data-ttu-id="21a8c-820">Deficiência</span><span class="sxs-lookup"><span data-stu-id="21a8c-820">disability</span></span>
      
## <a name="canada-passport-number"></a><span data-ttu-id="21a8c-821">Número de passaporte do Canadá</span><span class="sxs-lookup"><span data-stu-id="21a8c-821">Canada Passport Number</span></span>

### <a name="format"></a><span data-ttu-id="21a8c-822">Format</span><span class="sxs-lookup"><span data-stu-id="21a8c-822">Format</span></span>

<span data-ttu-id="21a8c-823">Duas letras maiúsculas, seguidas de seis dígitos</span><span class="sxs-lookup"><span data-stu-id="21a8c-823">Two uppercase letters followed by six digits</span></span>

### <a name="pattern"></a><span data-ttu-id="21a8c-824">Padrão</span><span class="sxs-lookup"><span data-stu-id="21a8c-824">Pattern</span></span>

<span data-ttu-id="21a8c-825">Duas letras maiúsculas, seguidas de seis dígitos</span><span class="sxs-lookup"><span data-stu-id="21a8c-825">Two uppercase letters followed by six digits</span></span>

### <a name="checksum"></a><span data-ttu-id="21a8c-826">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="21a8c-826">Checksum</span></span>

<span data-ttu-id="21a8c-827">Não</span><span class="sxs-lookup"><span data-stu-id="21a8c-827">No</span></span>

### <a name="definition"></a><span data-ttu-id="21a8c-828">Definição</span><span class="sxs-lookup"><span data-stu-id="21a8c-828">Definition</span></span>

<span data-ttu-id="21a8c-829">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="21a8c-829">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="21a8c-830">A expressão regular Regex_canada_passport_number localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="21a8c-830">The regular expression Regex_canada_passport_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="21a8c-831">Uma palavra-chave de Keyword_canada_passport_number ou Keyword_passport for encontrada.</span><span class="sxs-lookup"><span data-stu-id="21a8c-831">A keyword from Keyword_canada_passport_number or Keyword_passport is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="21a8c-832">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="21a8c-832">Keywords</span></span>

#### <a name="keywordcanadapassportnumber"></a><span data-ttu-id="21a8c-833">Keyword_canada_passport_number</span><span class="sxs-lookup"><span data-stu-id="21a8c-833">Keyword_canada_passport_number</span></span>

- <span data-ttu-id="21a8c-834">canadian citizenship</span><span class="sxs-lookup"><span data-stu-id="21a8c-834">canadian citizenship</span></span>
- <span data-ttu-id="21a8c-835">canadian passport</span><span class="sxs-lookup"><span data-stu-id="21a8c-835">canadian passport</span></span>
- <span data-ttu-id="21a8c-836">passport application</span><span class="sxs-lookup"><span data-stu-id="21a8c-836">passport application</span></span>
- <span data-ttu-id="21a8c-837">passport photos</span><span class="sxs-lookup"><span data-stu-id="21a8c-837">passport photos</span></span>
- <span data-ttu-id="21a8c-838">certified translator</span><span class="sxs-lookup"><span data-stu-id="21a8c-838">certified translator</span></span>
- <span data-ttu-id="21a8c-839">canadian citizens</span><span class="sxs-lookup"><span data-stu-id="21a8c-839">canadian citizens</span></span>
- <span data-ttu-id="21a8c-840">processing times</span><span class="sxs-lookup"><span data-stu-id="21a8c-840">processing times</span></span>
- <span data-ttu-id="21a8c-841">renewal application</span><span class="sxs-lookup"><span data-stu-id="21a8c-841">renewal application</span></span>

#### <a name="keywordpassport"></a><span data-ttu-id="21a8c-842">Keyword_passport</span><span class="sxs-lookup"><span data-stu-id="21a8c-842">Keyword_passport</span></span>

- <span data-ttu-id="21a8c-843">Passport Number</span><span class="sxs-lookup"><span data-stu-id="21a8c-843">Passport Number</span></span>
- <span data-ttu-id="21a8c-844">Passport No</span><span class="sxs-lookup"><span data-stu-id="21a8c-844">Passport No</span></span>
- <span data-ttu-id="21a8c-845">Passport #</span><span class="sxs-lookup"><span data-stu-id="21a8c-845">Passport #</span></span>
- <span data-ttu-id="21a8c-846">Passaport</span><span class="sxs-lookup"><span data-stu-id="21a8c-846">Passport#</span></span>
- <span data-ttu-id="21a8c-847">Passportid</span><span class="sxs-lookup"><span data-stu-id="21a8c-847">PassportID</span></span>
- <span data-ttu-id="21a8c-848">Passportno</span><span class="sxs-lookup"><span data-stu-id="21a8c-848">Passportno</span></span>
- <span data-ttu-id="21a8c-849">passportnumber</span><span class="sxs-lookup"><span data-stu-id="21a8c-849">passportnumber</span></span>
- <span data-ttu-id="21a8c-850">パスポート</span><span class="sxs-lookup"><span data-stu-id="21a8c-850">パスポート</span></span>
- <span data-ttu-id="21a8c-851">パスポート番号</span><span class="sxs-lookup"><span data-stu-id="21a8c-851">パスポート番号</span></span>
- <span data-ttu-id="21a8c-852">パスポートのNum</span><span class="sxs-lookup"><span data-stu-id="21a8c-852">パスポートのNum</span></span>
- <span data-ttu-id="21a8c-853">パスポート #</span><span class="sxs-lookup"><span data-stu-id="21a8c-853">パスポート＃</span></span>
- <span data-ttu-id="21a8c-854">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="21a8c-854">Numéro de passeport</span></span>
- <span data-ttu-id="21a8c-855">Passeport n °</span><span class="sxs-lookup"><span data-stu-id="21a8c-855">Passeport n °</span></span>
- <span data-ttu-id="21a8c-856">Passeport Non</span><span class="sxs-lookup"><span data-stu-id="21a8c-856">Passeport Non</span></span>
- <span data-ttu-id="21a8c-857">Passeport #</span><span class="sxs-lookup"><span data-stu-id="21a8c-857">Passeport #</span></span>
- <span data-ttu-id="21a8c-858">Passeport #</span><span class="sxs-lookup"><span data-stu-id="21a8c-858">Passeport#</span></span>
- <span data-ttu-id="21a8c-859">PasseportNon</span><span class="sxs-lookup"><span data-stu-id="21a8c-859">PasseportNon</span></span>
- <span data-ttu-id="21a8c-860">Passeportn °</span><span class="sxs-lookup"><span data-stu-id="21a8c-860">Passeportn °</span></span>
   
## <a name="canada-personal-health-identification-number-phin"></a><span data-ttu-id="21a8c-861">Número de identificação pessoal de saúde do Canadá (PHIN)</span><span class="sxs-lookup"><span data-stu-id="21a8c-861">Canada Personal Health Identification Number (PHIN)</span></span>

### <a name="format"></a><span data-ttu-id="21a8c-862">Format</span><span class="sxs-lookup"><span data-stu-id="21a8c-862">Format</span></span>

<span data-ttu-id="21a8c-863">Nove dígitos</span><span class="sxs-lookup"><span data-stu-id="21a8c-863">Nine digits</span></span>

### <a name="pattern"></a><span data-ttu-id="21a8c-864">Padrão</span><span class="sxs-lookup"><span data-stu-id="21a8c-864">Pattern</span></span>

<span data-ttu-id="21a8c-865">Nove dígitos</span><span class="sxs-lookup"><span data-stu-id="21a8c-865">Nine digits</span></span>

### <a name="checksum"></a><span data-ttu-id="21a8c-866">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="21a8c-866">Checksum</span></span>

<span data-ttu-id="21a8c-867">Não</span><span class="sxs-lookup"><span data-stu-id="21a8c-867">No</span></span>

### <a name="definition"></a><span data-ttu-id="21a8c-868">Definição</span><span class="sxs-lookup"><span data-stu-id="21a8c-868">Definition</span></span>

<span data-ttu-id="21a8c-869">Uma política de DLP é de 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres: a expressão regular Regex_canada_phin localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="21a8c-869">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters: The regular expression Regex_canada_phin finds content that matches the pattern.</span></span>
<span data-ttu-id="21a8c-870">São encontradas pelo menos duas palavras-chave do Keyword_canada_phin ou do Keyword_canada_provinces..</span><span class="sxs-lookup"><span data-stu-id="21a8c-870">At least two keywords from Keyword_canada_phin or Keyword_canada_provinces are found..</span></span>

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

### <a name="keywords"></a><span data-ttu-id="21a8c-871">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="21a8c-871">Keywords</span></span>

#### <a name="keywordcanadaphin"></a><span data-ttu-id="21a8c-872">Keyword_canada_phin</span><span class="sxs-lookup"><span data-stu-id="21a8c-872">Keyword_canada_phin</span></span>

- <span data-ttu-id="21a8c-873">social insurance number</span><span class="sxs-lookup"><span data-stu-id="21a8c-873">social insurance number</span></span>
- <span data-ttu-id="21a8c-874">health information act</span><span class="sxs-lookup"><span data-stu-id="21a8c-874">health information act</span></span>
- <span data-ttu-id="21a8c-875">income tax information</span><span class="sxs-lookup"><span data-stu-id="21a8c-875">income tax information</span></span>
- <span data-ttu-id="21a8c-876">manitoba health</span><span class="sxs-lookup"><span data-stu-id="21a8c-876">manitoba health</span></span>
- <span data-ttu-id="21a8c-877">health registration</span><span class="sxs-lookup"><span data-stu-id="21a8c-877">health registration</span></span>
- <span data-ttu-id="21a8c-878">prescription purchases</span><span class="sxs-lookup"><span data-stu-id="21a8c-878">prescription purchases</span></span>
- <span data-ttu-id="21a8c-879">benefit eligibility</span><span class="sxs-lookup"><span data-stu-id="21a8c-879">benefit eligibility</span></span>
- <span data-ttu-id="21a8c-880">personal health</span><span class="sxs-lookup"><span data-stu-id="21a8c-880">personal health</span></span>
- <span data-ttu-id="21a8c-881">power of attorney</span><span class="sxs-lookup"><span data-stu-id="21a8c-881">power of attorney</span></span>
- <span data-ttu-id="21a8c-882">registration number</span><span class="sxs-lookup"><span data-stu-id="21a8c-882">registration number</span></span>
- <span data-ttu-id="21a8c-883">personal health number</span><span class="sxs-lookup"><span data-stu-id="21a8c-883">personal health number</span></span>
- <span data-ttu-id="21a8c-884">practitioner referral</span><span class="sxs-lookup"><span data-stu-id="21a8c-884">practitioner referral</span></span>
- <span data-ttu-id="21a8c-885">wellness professional</span><span class="sxs-lookup"><span data-stu-id="21a8c-885">wellness professional</span></span>
- <span data-ttu-id="21a8c-886">patient referral</span><span class="sxs-lookup"><span data-stu-id="21a8c-886">patient referral</span></span>
- <span data-ttu-id="21a8c-887">health and wellness</span><span class="sxs-lookup"><span data-stu-id="21a8c-887">health and wellness</span></span>

#### <a name="keywordcanadaprovinces"></a><span data-ttu-id="21a8c-888">Keyword_canada_provinces</span><span class="sxs-lookup"><span data-stu-id="21a8c-888">Keyword_canada_provinces</span></span>

- <span data-ttu-id="21a8c-889">Nunavut</span><span class="sxs-lookup"><span data-stu-id="21a8c-889">Nunavut</span></span>
- <span data-ttu-id="21a8c-890">Quebec</span><span class="sxs-lookup"><span data-stu-id="21a8c-890">Quebec</span></span>
- <span data-ttu-id="21a8c-891">Northwest Territories</span><span class="sxs-lookup"><span data-stu-id="21a8c-891">Northwest Territories</span></span>
- <span data-ttu-id="21a8c-892">Ontário</span><span class="sxs-lookup"><span data-stu-id="21a8c-892">Ontario</span></span>
- <span data-ttu-id="21a8c-893">British Columbia</span><span class="sxs-lookup"><span data-stu-id="21a8c-893">British Columbia</span></span>
- <span data-ttu-id="21a8c-894">Alberta</span><span class="sxs-lookup"><span data-stu-id="21a8c-894">Alberta</span></span>
- <span data-ttu-id="21a8c-895">Saskatchewan</span><span class="sxs-lookup"><span data-stu-id="21a8c-895">Saskatchewan</span></span>
- <span data-ttu-id="21a8c-896">Manitoba</span><span class="sxs-lookup"><span data-stu-id="21a8c-896">Manitoba</span></span>
- <span data-ttu-id="21a8c-897">Yukon</span><span class="sxs-lookup"><span data-stu-id="21a8c-897">Yukon</span></span>
- <span data-ttu-id="21a8c-898">Newfoundland and Labrador</span><span class="sxs-lookup"><span data-stu-id="21a8c-898">Newfoundland and Labrador</span></span>
- <span data-ttu-id="21a8c-899">New Brunswick</span><span class="sxs-lookup"><span data-stu-id="21a8c-899">New Brunswick</span></span>
- <span data-ttu-id="21a8c-900">Nova Scotia</span><span class="sxs-lookup"><span data-stu-id="21a8c-900">Nova Scotia</span></span>
- <span data-ttu-id="21a8c-901">Prince Edward Island</span><span class="sxs-lookup"><span data-stu-id="21a8c-901">Prince Edward Island</span></span>
- <span data-ttu-id="21a8c-902">Canadá</span><span class="sxs-lookup"><span data-stu-id="21a8c-902">Canada</span></span>
   
## <a name="canada-social-insurance-number"></a><span data-ttu-id="21a8c-903">Número de seguro social do Canadá</span><span class="sxs-lookup"><span data-stu-id="21a8c-903">Canada Social Insurance Number</span></span>

### <a name="format"></a><span data-ttu-id="21a8c-904">Format</span><span class="sxs-lookup"><span data-stu-id="21a8c-904">Format</span></span>

<span data-ttu-id="21a8c-905">Nove dígitos com espaços ou hífens opcionais</span><span class="sxs-lookup"><span data-stu-id="21a8c-905">Nine digits with optional hyphens or spaces</span></span>

### <a name="pattern"></a><span data-ttu-id="21a8c-906">Padrão</span><span class="sxs-lookup"><span data-stu-id="21a8c-906">Pattern</span></span>

<span data-ttu-id="21a8c-907">Binário</span><span class="sxs-lookup"><span data-stu-id="21a8c-907">Formatted:</span></span>
- <span data-ttu-id="21a8c-908">Três dígitos</span><span class="sxs-lookup"><span data-stu-id="21a8c-908">Three digits</span></span> 
- <span data-ttu-id="21a8c-909">Um hífen ou espaço</span><span class="sxs-lookup"><span data-stu-id="21a8c-909">A hyphen or space</span></span> 
- <span data-ttu-id="21a8c-910">Três dígitos</span><span class="sxs-lookup"><span data-stu-id="21a8c-910">Three digits</span></span> 
- <span data-ttu-id="21a8c-911">Um hífen ou espaço</span><span class="sxs-lookup"><span data-stu-id="21a8c-911">A hyphen or space</span></span> 
- <span data-ttu-id="21a8c-912">Três dígitos</span><span class="sxs-lookup"><span data-stu-id="21a8c-912">Three digits</span></span>

<span data-ttu-id="21a8c-913">Não formatado: nove dígitos</span><span class="sxs-lookup"><span data-stu-id="21a8c-913">Unformatted: Nine digits</span></span>

### <a name="checksum"></a><span data-ttu-id="21a8c-914">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="21a8c-914">Checksum</span></span>

<span data-ttu-id="21a8c-915">Sim</span><span class="sxs-lookup"><span data-stu-id="21a8c-915">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="21a8c-916">Definição</span><span class="sxs-lookup"><span data-stu-id="21a8c-916">Definition</span></span>

<span data-ttu-id="21a8c-917">Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="21a8c-917">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="21a8c-918">A função Func_canadian_sin localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="21a8c-918">The function Func_canadian_sin finds content that matches the pattern.</span></span>
- <span data-ttu-id="21a8c-919">Pelo menos duas de qualquer combinação do seguinte:</span><span class="sxs-lookup"><span data-stu-id="21a8c-919">At least two of any combination of the following:</span></span>
    - <span data-ttu-id="21a8c-920">Uma palavra-chave de Keyword_sin for encontrada.</span><span class="sxs-lookup"><span data-stu-id="21a8c-920">A keyword from Keyword_sin is found.</span></span>
    - <span data-ttu-id="21a8c-921">Uma palavra-chave de Keyword_sin_collaborative for encontrada.</span><span class="sxs-lookup"><span data-stu-id="21a8c-921">A keyword from Keyword_sin_collaborative is found.</span></span>
    - <span data-ttu-id="21a8c-922">A função Func_eu_date encontra uma data no formato de data à direita.</span><span class="sxs-lookup"><span data-stu-id="21a8c-922">The function Func_eu_date finds a date in the right date format.</span></span>
- <span data-ttu-id="21a8c-923">A soma de verificação passa.</span><span class="sxs-lookup"><span data-stu-id="21a8c-923">The checksum passes.</span></span>

<span data-ttu-id="21a8c-924">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="21a8c-924">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="21a8c-925">A função Func_unformatted_canadian_sin localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="21a8c-925">The function Func_unformatted_canadian_sin finds content that matches the pattern.</span></span>
- <span data-ttu-id="21a8c-926">Uma palavra-chave de Keyword_sin for encontrada.</span><span class="sxs-lookup"><span data-stu-id="21a8c-926">A keyword from Keyword_sin is found.</span></span>
- <span data-ttu-id="21a8c-927">A soma de verificação passa.</span><span class="sxs-lookup"><span data-stu-id="21a8c-927">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="21a8c-928">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="21a8c-928">Keywords</span></span>

#### <a name="keywordsin"></a><span data-ttu-id="21a8c-929">Keyword_sin</span><span class="sxs-lookup"><span data-stu-id="21a8c-929">Keyword_sin</span></span>

- <span data-ttu-id="21a8c-930">sin</span><span class="sxs-lookup"><span data-stu-id="21a8c-930">sin</span></span> 
- <span data-ttu-id="21a8c-931">social insurance</span><span class="sxs-lookup"><span data-stu-id="21a8c-931">social insurance</span></span> 
- <span data-ttu-id="21a8c-932">numero d'assurance sociale</span><span class="sxs-lookup"><span data-stu-id="21a8c-932">numero d'assurance sociale</span></span> 
- <span data-ttu-id="21a8c-933">capitais</span><span class="sxs-lookup"><span data-stu-id="21a8c-933">sins</span></span> 
- <span data-ttu-id="21a8c-934">es</span><span class="sxs-lookup"><span data-stu-id="21a8c-934">ssn</span></span> 
- <span data-ttu-id="21a8c-935">CPFs</span><span class="sxs-lookup"><span data-stu-id="21a8c-935">ssns</span></span> 
- <span data-ttu-id="21a8c-936">social security</span><span class="sxs-lookup"><span data-stu-id="21a8c-936">social security</span></span> 
- <span data-ttu-id="21a8c-937">numero d'assurance social</span><span class="sxs-lookup"><span data-stu-id="21a8c-937">numero d'assurance social</span></span> 
- <span data-ttu-id="21a8c-938">national identification number</span><span class="sxs-lookup"><span data-stu-id="21a8c-938">national identification number</span></span> 
- <span data-ttu-id="21a8c-939">national id</span><span class="sxs-lookup"><span data-stu-id="21a8c-939">national id</span></span> 
- <span data-ttu-id="21a8c-940">Sin</span><span class="sxs-lookup"><span data-stu-id="21a8c-940">sin#</span></span> 
- <span data-ttu-id="21a8c-941">soc ins</span><span class="sxs-lookup"><span data-stu-id="21a8c-941">soc ins</span></span> 
- <span data-ttu-id="21a8c-942">social ins</span><span class="sxs-lookup"><span data-stu-id="21a8c-942">social ins</span></span> 

#### <a name="keywordsincollaborative"></a><span data-ttu-id="21a8c-943">Keyword_sin_collaborative</span><span class="sxs-lookup"><span data-stu-id="21a8c-943">Keyword_sin_collaborative</span></span>

- <span data-ttu-id="21a8c-944">driver's license</span><span class="sxs-lookup"><span data-stu-id="21a8c-944">driver's license</span></span> 
- <span data-ttu-id="21a8c-945">drivers license</span><span class="sxs-lookup"><span data-stu-id="21a8c-945">drivers license</span></span> 
- <span data-ttu-id="21a8c-946">driver's licence</span><span class="sxs-lookup"><span data-stu-id="21a8c-946">driver's licence</span></span> 
- <span data-ttu-id="21a8c-947">drivers licence</span><span class="sxs-lookup"><span data-stu-id="21a8c-947">drivers licence</span></span> 
- <span data-ttu-id="21a8c-948">DOB</span><span class="sxs-lookup"><span data-stu-id="21a8c-948">DOB</span></span> 
- <span data-ttu-id="21a8c-949">Data de Nascimento</span><span class="sxs-lookup"><span data-stu-id="21a8c-949">Birthdate</span></span> 
- <span data-ttu-id="21a8c-950">Aniversário</span><span class="sxs-lookup"><span data-stu-id="21a8c-950">Birthday</span></span> 
- <span data-ttu-id="21a8c-951">Date of Birth</span><span class="sxs-lookup"><span data-stu-id="21a8c-951">Date of Birth</span></span> 
   
## <a name="chile-identity-card-number"></a><span data-ttu-id="21a8c-952">	Número do Cartão de Identidade do Chile</span><span class="sxs-lookup"><span data-stu-id="21a8c-952">Chile Identity Card Number</span></span>

### <a name="format"></a><span data-ttu-id="21a8c-953">Format</span><span class="sxs-lookup"><span data-stu-id="21a8c-953">Format</span></span>

<span data-ttu-id="21a8c-954">7-8 dígitos mais delimitadores um dígito ou letra de verificação</span><span class="sxs-lookup"><span data-stu-id="21a8c-954">7-8 digits plus delimiters a check digit or letter</span></span>

### <a name="pattern"></a><span data-ttu-id="21a8c-955">Padrão</span><span class="sxs-lookup"><span data-stu-id="21a8c-955">Pattern</span></span>

<span data-ttu-id="21a8c-956">7 a 8 dígitos mais delimitadores:</span><span class="sxs-lookup"><span data-stu-id="21a8c-956">7-8 digits plus delimiters:</span></span>
- <span data-ttu-id="21a8c-957">1 a 2 dígitos</span><span class="sxs-lookup"><span data-stu-id="21a8c-957">1-2 digits</span></span> 
- <span data-ttu-id="21a8c-958">Um ponto </span><span class="sxs-lookup"><span data-stu-id="21a8c-958">A period</span></span> 
- <span data-ttu-id="21a8c-959">Três dígitos</span><span class="sxs-lookup"><span data-stu-id="21a8c-959">Three digits</span></span> 
- <span data-ttu-id="21a8c-960">Um ponto </span><span class="sxs-lookup"><span data-stu-id="21a8c-960">A period</span></span> 
- <span data-ttu-id="21a8c-961">Três dígitos</span><span class="sxs-lookup"><span data-stu-id="21a8c-961">Three digits</span></span> 
- <span data-ttu-id="21a8c-962">Um traço</span><span class="sxs-lookup"><span data-stu-id="21a8c-962">A dash</span></span> 
- <span data-ttu-id="21a8c-963">Um dígito ou letra (não diferencia maiúscula de minúscula) que é um dígito de verificação</span><span class="sxs-lookup"><span data-stu-id="21a8c-963">One digit or letter (not case sensitive) which is a check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="21a8c-964">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="21a8c-964">Checksum</span></span>

<span data-ttu-id="21a8c-965">Sim</span><span class="sxs-lookup"><span data-stu-id="21a8c-965">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="21a8c-966">Definição</span><span class="sxs-lookup"><span data-stu-id="21a8c-966">Definition</span></span>

<span data-ttu-id="21a8c-967">Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="21a8c-967">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="21a8c-968">A função Func_chile_id_card localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="21a8c-968">The function Func_chile_id_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="21a8c-969">Uma palavra-chave de Keyword_chile_id_card for encontrada.</span><span class="sxs-lookup"><span data-stu-id="21a8c-969">A keyword from Keyword_chile_id_card is found.</span></span>
- <span data-ttu-id="21a8c-970">A soma de verificação passa.</span><span class="sxs-lookup"><span data-stu-id="21a8c-970">The checksum passes.</span></span>

<span data-ttu-id="21a8c-971">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="21a8c-971">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="21a8c-972">A função Func_chile_id_card localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="21a8c-972">The function Func_chile_id_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="21a8c-973">A soma de verificação passa.</span><span class="sxs-lookup"><span data-stu-id="21a8c-973">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="21a8c-974">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="21a8c-974">Keywords</span></span>

#### <a name="keywordchileidcard"></a><span data-ttu-id="21a8c-975">Keyword_chile_id_card</span><span class="sxs-lookup"><span data-stu-id="21a8c-975">Keyword_chile_id_card</span></span>

- <span data-ttu-id="21a8c-976">Número de Identificação Nacional</span><span class="sxs-lookup"><span data-stu-id="21a8c-976">National Identification Number</span></span> 
- <span data-ttu-id="21a8c-977">Cartão de identidade</span><span class="sxs-lookup"><span data-stu-id="21a8c-977">Identity card</span></span> 
- <span data-ttu-id="21a8c-978">ID</span><span class="sxs-lookup"><span data-stu-id="21a8c-978">ID</span></span> 
- <span data-ttu-id="21a8c-979">Identificador</span><span class="sxs-lookup"><span data-stu-id="21a8c-979">Identification</span></span> 
- <span data-ttu-id="21a8c-980">Rol Único Nacional</span><span class="sxs-lookup"><span data-stu-id="21a8c-980">Rol Único Nacional</span></span> 
- <span data-ttu-id="21a8c-981">SEJAM</span><span class="sxs-lookup"><span data-stu-id="21a8c-981">RUN</span></span> 
- <span data-ttu-id="21a8c-982">Rol Único Tributario</span><span class="sxs-lookup"><span data-stu-id="21a8c-982">Rol Único Tributario</span></span> 
- <span data-ttu-id="21a8c-983">ROTINA</span><span class="sxs-lookup"><span data-stu-id="21a8c-983">RUT</span></span> 
- <span data-ttu-id="21a8c-984">Cédula de Identidad</span><span class="sxs-lookup"><span data-stu-id="21a8c-984">Cédula de Identidad</span></span> 
- <span data-ttu-id="21a8c-985">Número De Identificación Nacional</span><span class="sxs-lookup"><span data-stu-id="21a8c-985">Número De Identificación Nacional</span></span> 
- <span data-ttu-id="21a8c-986">Tarjeta de identificación</span><span class="sxs-lookup"><span data-stu-id="21a8c-986">Tarjeta de identificación</span></span> 
- <span data-ttu-id="21a8c-987">Identificación</span><span class="sxs-lookup"><span data-stu-id="21a8c-987">Identificación</span></span> 
   
## <a name="china-resident-identity-card-prc-number"></a><span data-ttu-id="21a8c-988">	Número do Cartão de Identidade de Residentes (PRC) da China</span><span class="sxs-lookup"><span data-stu-id="21a8c-988">China Resident Identity Card (PRC) Number</span></span>

### <a name="format"></a><span data-ttu-id="21a8c-989">Format</span><span class="sxs-lookup"><span data-stu-id="21a8c-989">Format</span></span>

<span data-ttu-id="21a8c-990">18 dígitos</span><span class="sxs-lookup"><span data-stu-id="21a8c-990">18 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="21a8c-991">Padrão</span><span class="sxs-lookup"><span data-stu-id="21a8c-991">Pattern</span></span>

<span data-ttu-id="21a8c-992">18 dígitos:</span><span class="sxs-lookup"><span data-stu-id="21a8c-992">18 digits:</span></span>
- <span data-ttu-id="21a8c-993">Seis dígitos que são um código de endereço </span><span class="sxs-lookup"><span data-stu-id="21a8c-993">Six digits which are an address code</span></span> 
- <span data-ttu-id="21a8c-994">Oito dígitos no formato AAAAMMDD que são a data de nascimento </span><span class="sxs-lookup"><span data-stu-id="21a8c-994">Eight digits in the form YYYYMMDD which are the date of birth</span></span> 
- <span data-ttu-id="21a8c-995">Três dígitos que são um código de pedido </span><span class="sxs-lookup"><span data-stu-id="21a8c-995">Three digits which are an order code</span></span> 
- <span data-ttu-id="21a8c-996">Um dígito que é um dígito de verificação</span><span class="sxs-lookup"><span data-stu-id="21a8c-996">One digit which is a check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="21a8c-997">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="21a8c-997">Checksum</span></span>

<span data-ttu-id="21a8c-998">Sim</span><span class="sxs-lookup"><span data-stu-id="21a8c-998">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="21a8c-999">Definição</span><span class="sxs-lookup"><span data-stu-id="21a8c-999">Definition</span></span>

<span data-ttu-id="21a8c-1000">Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="21a8c-1000">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="21a8c-1001">A função Func_china_resident_id localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="21a8c-1001">The function Func_china_resident_id finds content that matches the pattern.</span></span>
- <span data-ttu-id="21a8c-1002">Uma palavra-chave de Keyword_china_resident_id for encontrada.</span><span class="sxs-lookup"><span data-stu-id="21a8c-1002">A keyword from Keyword_china_resident_id is found.</span></span>
- <span data-ttu-id="21a8c-1003">A soma de verificação passa.</span><span class="sxs-lookup"><span data-stu-id="21a8c-1003">The checksum passes.</span></span>

<span data-ttu-id="21a8c-1004">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="21a8c-1004">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="21a8c-1005">A função Func_china_resident_id localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="21a8c-1005">The function Func_china_resident_id finds content that matches the pattern.</span></span>
- <span data-ttu-id="21a8c-1006">A soma de verificação passa.</span><span class="sxs-lookup"><span data-stu-id="21a8c-1006">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="21a8c-1007">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="21a8c-1007">Keywords</span></span>

### <a name="keywordchinaresidentid"></a><span data-ttu-id="21a8c-1008">Keyword_china_resident_id</span><span class="sxs-lookup"><span data-stu-id="21a8c-1008">Keyword_china_resident_id</span></span>

- <span data-ttu-id="21a8c-1009">Cartão de Identidade da Polônia</span><span class="sxs-lookup"><span data-stu-id="21a8c-1009">Resident Identity Card</span></span> 
- <span data-ttu-id="21a8c-1010">POPULAR</span><span class="sxs-lookup"><span data-stu-id="21a8c-1010">PRC</span></span> 
- <span data-ttu-id="21a8c-1011">Cartão de Identificação Nacional</span><span class="sxs-lookup"><span data-stu-id="21a8c-1011">National Identification Card</span></span> 
- <span data-ttu-id="21a8c-1012">身份证</span><span class="sxs-lookup"><span data-stu-id="21a8c-1012">身份证</span></span> 
- <span data-ttu-id="21a8c-1013">居民 身份证</span><span class="sxs-lookup"><span data-stu-id="21a8c-1013">居民 身份证</span></span> 
- <span data-ttu-id="21a8c-1014">居民身份证</span><span class="sxs-lookup"><span data-stu-id="21a8c-1014">居民身份证</span></span> 
- <span data-ttu-id="21a8c-1015">鉴定</span><span class="sxs-lookup"><span data-stu-id="21a8c-1015">鉴定</span></span> 
- <span data-ttu-id="21a8c-1016">身分證</span><span class="sxs-lookup"><span data-stu-id="21a8c-1016">身分證</span></span> 
- <span data-ttu-id="21a8c-1017">居民 身份證</span><span class="sxs-lookup"><span data-stu-id="21a8c-1017">居民 身份證</span></span>
- <span data-ttu-id="21a8c-1018">鑑定</span><span class="sxs-lookup"><span data-stu-id="21a8c-1018">鑑定</span></span> 
   
## <a name="credit-card-number"></a><span data-ttu-id="21a8c-1019">Credit Card Number</span><span class="sxs-lookup"><span data-stu-id="21a8c-1019">Credit Card Number</span></span>

### <a name="format"></a><span data-ttu-id="21a8c-1020">Format</span><span class="sxs-lookup"><span data-stu-id="21a8c-1020">Format</span></span>

<span data-ttu-id="21a8c-1021">16 dígitos que podem ser formatados ou não formatados (dddddddddddddddd) e devem passar no teste Luhn.</span><span class="sxs-lookup"><span data-stu-id="21a8c-1021">16 digits which can be formatted or unformatted (dddddddddddddddd) and must pass the Luhn test.</span></span>

### <a name="pattern"></a><span data-ttu-id="21a8c-1022">Padrão</span><span class="sxs-lookup"><span data-stu-id="21a8c-1022">Pattern</span></span>

<span data-ttu-id="21a8c-1023">Padrão muito complexo e robusto que detecta cartões de todas as principais marcas em todo o mundo, incluindo Visa, MasterCard, Discover Card, JCB, American Express, vales-presentes e cartões diner.</span><span class="sxs-lookup"><span data-stu-id="21a8c-1023">Very complex and robust pattern that detects cards from all major brands worldwide, including Visa, MasterCard, Discover Card, JCB, American Express, gift cards, and diner cards.</span></span>

### <a name="checksum"></a><span data-ttu-id="21a8c-1024">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="21a8c-1024">Checksum</span></span>

<span data-ttu-id="21a8c-1025">Sim, a soma de verificação Luhn</span><span class="sxs-lookup"><span data-stu-id="21a8c-1025">Yes, the Luhn checksum</span></span>

### <a name="definition"></a><span data-ttu-id="21a8c-1026">Definição</span><span class="sxs-lookup"><span data-stu-id="21a8c-1026">Definition</span></span>

<span data-ttu-id="21a8c-1027">Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="21a8c-1027">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="21a8c-1028">A função Func_credit_card localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="21a8c-1028">The function Func_credit_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="21a8c-1029">Uma das seguintes opções for verdadeira:</span><span class="sxs-lookup"><span data-stu-id="21a8c-1029">One of the following is true:</span></span>
    - <span data-ttu-id="21a8c-1030">Uma palavra-chave de Keyword_cc_verification for encontrada.</span><span class="sxs-lookup"><span data-stu-id="21a8c-1030">A keyword from Keyword_cc_verification is found.</span></span>
    - <span data-ttu-id="21a8c-1031">Uma palavra-chave de Keyword_cc_name for encontrada.</span><span class="sxs-lookup"><span data-stu-id="21a8c-1031">A keyword from Keyword_cc_name is found.</span></span>
    - <span data-ttu-id="21a8c-1032">A função Func_expiration_date encontra uma data no formato de data à direita.</span><span class="sxs-lookup"><span data-stu-id="21a8c-1032">The function Func_expiration_date finds a date in the right date format.</span></span>
- <span data-ttu-id="21a8c-1033">A soma de verificação passa.</span><span class="sxs-lookup"><span data-stu-id="21a8c-1033">The checksum passes.</span></span>

<span data-ttu-id="21a8c-1034">Uma política de DLP tem 65% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="21a8c-1034">A DLP policy is 65% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="21a8c-1035">A função Func_credit_card localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="21a8c-1035">The function Func_credit_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="21a8c-1036">A soma de verificação passa.</span><span class="sxs-lookup"><span data-stu-id="21a8c-1036">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="21a8c-1037">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="21a8c-1037">Keywords</span></span>

#### <a name="keywordccverification"></a><span data-ttu-id="21a8c-1038">Keyword_cc_verification</span><span class="sxs-lookup"><span data-stu-id="21a8c-1038">Keyword_cc_verification</span></span>

- <span data-ttu-id="21a8c-1039">card verification</span><span class="sxs-lookup"><span data-stu-id="21a8c-1039">card verification</span></span>
- <span data-ttu-id="21a8c-1040">card identification number</span><span class="sxs-lookup"><span data-stu-id="21a8c-1040">card identification number</span></span>
- <span data-ttu-id="21a8c-1041">CVN</span><span class="sxs-lookup"><span data-stu-id="21a8c-1041">cvn</span></span>
- <span data-ttu-id="21a8c-1042">CID</span><span class="sxs-lookup"><span data-stu-id="21a8c-1042">cid</span></span>
- <span data-ttu-id="21a8c-1043">CVC2</span><span class="sxs-lookup"><span data-stu-id="21a8c-1043">cvc2</span></span>
- <span data-ttu-id="21a8c-1044">CVV2</span><span class="sxs-lookup"><span data-stu-id="21a8c-1044">cvv2</span></span>
- <span data-ttu-id="21a8c-1045">pin block</span><span class="sxs-lookup"><span data-stu-id="21a8c-1045">pin block</span></span>
- <span data-ttu-id="21a8c-1046">security code</span><span class="sxs-lookup"><span data-stu-id="21a8c-1046">security code</span></span>
- <span data-ttu-id="21a8c-1047">security number</span><span class="sxs-lookup"><span data-stu-id="21a8c-1047">security number</span></span>
- <span data-ttu-id="21a8c-1048">security no</span><span class="sxs-lookup"><span data-stu-id="21a8c-1048">security no</span></span>
- <span data-ttu-id="21a8c-1049">issue number</span><span class="sxs-lookup"><span data-stu-id="21a8c-1049">issue number</span></span>
- <span data-ttu-id="21a8c-1050">issue no</span><span class="sxs-lookup"><span data-stu-id="21a8c-1050">issue no</span></span>
- <span data-ttu-id="21a8c-1051">cryptogramme</span><span class="sxs-lookup"><span data-stu-id="21a8c-1051">cryptogramme</span></span>
- <span data-ttu-id="21a8c-1052">numéro de sécurité</span><span class="sxs-lookup"><span data-stu-id="21a8c-1052">numéro de sécurité</span></span>
- <span data-ttu-id="21a8c-1053">numero de securite</span><span class="sxs-lookup"><span data-stu-id="21a8c-1053">numero de securite</span></span>
- <span data-ttu-id="21a8c-1054">kreditkartenprüfnummer</span><span class="sxs-lookup"><span data-stu-id="21a8c-1054">kreditkartenprüfnummer</span></span>
- <span data-ttu-id="21a8c-1055">kreditkartenprufnummer</span><span class="sxs-lookup"><span data-stu-id="21a8c-1055">kreditkartenprufnummer</span></span>
- <span data-ttu-id="21a8c-1056">prüfziffer</span><span class="sxs-lookup"><span data-stu-id="21a8c-1056">prüfziffer</span></span>
- <span data-ttu-id="21a8c-1057">prufziffer</span><span class="sxs-lookup"><span data-stu-id="21a8c-1057">prufziffer</span></span>
- <span data-ttu-id="21a8c-1058">sicherheits Kode</span><span class="sxs-lookup"><span data-stu-id="21a8c-1058">sicherheits Kode</span></span>
- <span data-ttu-id="21a8c-1059">sicherheitscode</span><span class="sxs-lookup"><span data-stu-id="21a8c-1059">sicherheitscode</span></span>
- <span data-ttu-id="21a8c-1060">sicherheitsnummer</span><span class="sxs-lookup"><span data-stu-id="21a8c-1060">sicherheitsnummer</span></span>
- <span data-ttu-id="21a8c-1061">verfalldatum</span><span class="sxs-lookup"><span data-stu-id="21a8c-1061">verfalldatum</span></span>
- <span data-ttu-id="21a8c-1062">codice di verifica</span><span class="sxs-lookup"><span data-stu-id="21a8c-1062">codice di verifica</span></span>
- <span data-ttu-id="21a8c-1063">COD.</span><span class="sxs-lookup"><span data-stu-id="21a8c-1063">cod.</span></span> <span data-ttu-id="21a8c-1064">sicurezza</span><span class="sxs-lookup"><span data-stu-id="21a8c-1064">sicurezza</span></span>
- <span data-ttu-id="21a8c-1065">cod sicurezza</span><span class="sxs-lookup"><span data-stu-id="21a8c-1065">cod sicurezza</span></span>
- <span data-ttu-id="21a8c-1066">n autorizzazione</span><span class="sxs-lookup"><span data-stu-id="21a8c-1066">n autorizzazione</span></span>
- <span data-ttu-id="21a8c-1067">CFOP</span><span class="sxs-lookup"><span data-stu-id="21a8c-1067">código</span></span>
- <span data-ttu-id="21a8c-1068">codigo</span><span class="sxs-lookup"><span data-stu-id="21a8c-1068">codigo</span></span>
- <span data-ttu-id="21a8c-1069">COD.</span><span class="sxs-lookup"><span data-stu-id="21a8c-1069">cod.</span></span> <span data-ttu-id="21a8c-1070">seg</span><span class="sxs-lookup"><span data-stu-id="21a8c-1070">seg</span></span>
- <span data-ttu-id="21a8c-1071">cod seg</span><span class="sxs-lookup"><span data-stu-id="21a8c-1071">cod seg</span></span>
- <span data-ttu-id="21a8c-1072">código de segurança</span><span class="sxs-lookup"><span data-stu-id="21a8c-1072">código de segurança</span></span>
- <span data-ttu-id="21a8c-1073">codigo de seguranca</span><span class="sxs-lookup"><span data-stu-id="21a8c-1073">codigo de seguranca</span></span>
- <span data-ttu-id="21a8c-1074">codigo de segurança</span><span class="sxs-lookup"><span data-stu-id="21a8c-1074">codigo de segurança</span></span>
- <span data-ttu-id="21a8c-1075">código de seguranca</span><span class="sxs-lookup"><span data-stu-id="21a8c-1075">código de seguranca</span></span>
- <span data-ttu-id="21a8c-1076">Cód.</span><span class="sxs-lookup"><span data-stu-id="21a8c-1076">cód.</span></span> <span data-ttu-id="21a8c-1077">segurança</span><span class="sxs-lookup"><span data-stu-id="21a8c-1077">segurança</span></span>
- <span data-ttu-id="21a8c-1078">COD.</span><span class="sxs-lookup"><span data-stu-id="21a8c-1078">cod.</span></span> <span data-ttu-id="21a8c-1079">seguranca Cod.</span><span class="sxs-lookup"><span data-stu-id="21a8c-1079">seguranca cod.</span></span> <span data-ttu-id="21a8c-1080">segurança</span><span class="sxs-lookup"><span data-stu-id="21a8c-1080">segurança</span></span>
- <span data-ttu-id="21a8c-1081">Cód.</span><span class="sxs-lookup"><span data-stu-id="21a8c-1081">cód.</span></span> <span data-ttu-id="21a8c-1082">seguranca</span><span class="sxs-lookup"><span data-stu-id="21a8c-1082">seguranca</span></span>
- <span data-ttu-id="21a8c-1083">cód segurança</span><span class="sxs-lookup"><span data-stu-id="21a8c-1083">cód segurança</span></span>
- <span data-ttu-id="21a8c-1084">COD seguranca COD segurança</span><span class="sxs-lookup"><span data-stu-id="21a8c-1084">cod seguranca cod segurança</span></span>
- <span data-ttu-id="21a8c-1085">cód seguranca</span><span class="sxs-lookup"><span data-stu-id="21a8c-1085">cód seguranca</span></span>
- <span data-ttu-id="21a8c-1086">número de verificação</span><span class="sxs-lookup"><span data-stu-id="21a8c-1086">número de verificação</span></span>
- <span data-ttu-id="21a8c-1087">numero de verificacao</span><span class="sxs-lookup"><span data-stu-id="21a8c-1087">numero de verificacao</span></span>
- <span data-ttu-id="21a8c-1088">ablauf</span><span class="sxs-lookup"><span data-stu-id="21a8c-1088">ablauf</span></span>
- <span data-ttu-id="21a8c-1089">gültig bis</span><span class="sxs-lookup"><span data-stu-id="21a8c-1089">gültig bis</span></span>
- <span data-ttu-id="21a8c-1090">gültigkeitsdatum</span><span class="sxs-lookup"><span data-stu-id="21a8c-1090">gültigkeitsdatum</span></span>
- <span data-ttu-id="21a8c-1091">gultig bis</span><span class="sxs-lookup"><span data-stu-id="21a8c-1091">gultig bis</span></span>
- <span data-ttu-id="21a8c-1092">gultigkeitsdatum</span><span class="sxs-lookup"><span data-stu-id="21a8c-1092">gultigkeitsdatum</span></span>
- <span data-ttu-id="21a8c-1093">scadenza</span><span class="sxs-lookup"><span data-stu-id="21a8c-1093">scadenza</span></span>
- <span data-ttu-id="21a8c-1094">data scad</span><span class="sxs-lookup"><span data-stu-id="21a8c-1094">data scad</span></span>
- <span data-ttu-id="21a8c-1095">fecha de expiracion</span><span class="sxs-lookup"><span data-stu-id="21a8c-1095">fecha de expiracion</span></span>
- <span data-ttu-id="21a8c-1096">fecha de venc</span><span class="sxs-lookup"><span data-stu-id="21a8c-1096">fecha de venc</span></span>
- <span data-ttu-id="21a8c-1097">vencimiento</span><span class="sxs-lookup"><span data-stu-id="21a8c-1097">vencimiento</span></span>
- <span data-ttu-id="21a8c-1098">válido hasta</span><span class="sxs-lookup"><span data-stu-id="21a8c-1098">válido hasta</span></span>
- <span data-ttu-id="21a8c-1099">valido hasta</span><span class="sxs-lookup"><span data-stu-id="21a8c-1099">valido hasta</span></span>
- <span data-ttu-id="21a8c-1100">vto</span><span class="sxs-lookup"><span data-stu-id="21a8c-1100">vto</span></span>
- <span data-ttu-id="21a8c-1101">data de expiração</span><span class="sxs-lookup"><span data-stu-id="21a8c-1101">data de expiração</span></span>
- <span data-ttu-id="21a8c-1102">data de expiracao</span><span class="sxs-lookup"><span data-stu-id="21a8c-1102">data de expiracao</span></span>
- <span data-ttu-id="21a8c-1103">data em que expira</span><span class="sxs-lookup"><span data-stu-id="21a8c-1103">data em que expira</span></span>
- <span data-ttu-id="21a8c-1104">validade</span><span class="sxs-lookup"><span data-stu-id="21a8c-1104">validade</span></span>
- <span data-ttu-id="21a8c-1105">coragem</span><span class="sxs-lookup"><span data-stu-id="21a8c-1105">valor</span></span>
- <span data-ttu-id="21a8c-1106">vencimento</span><span class="sxs-lookup"><span data-stu-id="21a8c-1106">vencimento</span></span>
- <span data-ttu-id="21a8c-1107">Venc</span><span class="sxs-lookup"><span data-stu-id="21a8c-1107">Venc</span></span> 

#### <a name="keywordccname"></a><span data-ttu-id="21a8c-1108">Keyword_cc_name</span><span class="sxs-lookup"><span data-stu-id="21a8c-1108">Keyword_cc_name</span></span>

- <span data-ttu-id="21a8c-1109">Amex</span><span class="sxs-lookup"><span data-stu-id="21a8c-1109">amex</span></span>
- <span data-ttu-id="21a8c-1110">american express</span><span class="sxs-lookup"><span data-stu-id="21a8c-1110">american express</span></span>
- <span data-ttu-id="21a8c-1111">americanexpress</span><span class="sxs-lookup"><span data-stu-id="21a8c-1111">americanexpress</span></span>
- <span data-ttu-id="21a8c-1112">Cartões</span><span class="sxs-lookup"><span data-stu-id="21a8c-1112">Visa</span></span>
- <span data-ttu-id="21a8c-1113">MasterCard</span><span class="sxs-lookup"><span data-stu-id="21a8c-1113">mastercard</span></span>
- <span data-ttu-id="21a8c-1114">master card</span><span class="sxs-lookup"><span data-stu-id="21a8c-1114">master card</span></span>
- <span data-ttu-id="21a8c-1115">MC</span><span class="sxs-lookup"><span data-stu-id="21a8c-1115">mc</span></span> 
- <span data-ttu-id="21a8c-1116">MasterCards</span><span class="sxs-lookup"><span data-stu-id="21a8c-1116">mastercards</span></span>
- <span data-ttu-id="21a8c-1117">master cards</span><span class="sxs-lookup"><span data-stu-id="21a8c-1117">master cards</span></span>
- <span data-ttu-id="21a8c-1118">diner's Club</span><span class="sxs-lookup"><span data-stu-id="21a8c-1118">diner's Club</span></span>
- <span data-ttu-id="21a8c-1119">diners club</span><span class="sxs-lookup"><span data-stu-id="21a8c-1119">diners club</span></span>
- <span data-ttu-id="21a8c-1120">Dinersclub</span><span class="sxs-lookup"><span data-stu-id="21a8c-1120">dinersclub</span></span>
- <span data-ttu-id="21a8c-1121">discover card</span><span class="sxs-lookup"><span data-stu-id="21a8c-1121">discover card</span></span>
- <span data-ttu-id="21a8c-1122">DiscoverCard</span><span class="sxs-lookup"><span data-stu-id="21a8c-1122">discovercard</span></span>
- <span data-ttu-id="21a8c-1123">discover cards</span><span class="sxs-lookup"><span data-stu-id="21a8c-1123">discover cards</span></span>
- <span data-ttu-id="21a8c-1124">JCB</span><span class="sxs-lookup"><span data-stu-id="21a8c-1124">JCB</span></span>
- <span data-ttu-id="21a8c-1125">japanese card bureau</span><span class="sxs-lookup"><span data-stu-id="21a8c-1125">japanese card bureau</span></span>
- <span data-ttu-id="21a8c-1126">carte blanche</span><span class="sxs-lookup"><span data-stu-id="21a8c-1126">carte blanche</span></span>
- <span data-ttu-id="21a8c-1127">carteblanche</span><span class="sxs-lookup"><span data-stu-id="21a8c-1127">carteblanche</span></span>
- <span data-ttu-id="21a8c-1128">credit card</span><span class="sxs-lookup"><span data-stu-id="21a8c-1128">credit card</span></span>
- <span data-ttu-id="21a8c-1129">colocado</span><span class="sxs-lookup"><span data-stu-id="21a8c-1129">cc#</span></span>
- <span data-ttu-id="21a8c-1130">CC #:</span><span class="sxs-lookup"><span data-stu-id="21a8c-1130">cc#:</span></span>
- <span data-ttu-id="21a8c-1131">expiration date</span><span class="sxs-lookup"><span data-stu-id="21a8c-1131">expiration date</span></span>
- <span data-ttu-id="21a8c-1132">exp date</span><span class="sxs-lookup"><span data-stu-id="21a8c-1132">exp date</span></span>
- <span data-ttu-id="21a8c-1133">expiry date</span><span class="sxs-lookup"><span data-stu-id="21a8c-1133">expiry date</span></span>
- <span data-ttu-id="21a8c-1134">date d’expiration</span><span class="sxs-lookup"><span data-stu-id="21a8c-1134">date d’expiration</span></span>
- <span data-ttu-id="21a8c-1135">date d'exp</span><span class="sxs-lookup"><span data-stu-id="21a8c-1135">date d'exp</span></span>
- <span data-ttu-id="21a8c-1136">date expiration</span><span class="sxs-lookup"><span data-stu-id="21a8c-1136">date expiration</span></span>
- <span data-ttu-id="21a8c-1137">bank card</span><span class="sxs-lookup"><span data-stu-id="21a8c-1137">bank card</span></span>
- <span data-ttu-id="21a8c-1138">BankCard</span><span class="sxs-lookup"><span data-stu-id="21a8c-1138">bankcard</span></span>
- <span data-ttu-id="21a8c-1139">card number</span><span class="sxs-lookup"><span data-stu-id="21a8c-1139">card number</span></span>
- <span data-ttu-id="21a8c-1140">card num</span><span class="sxs-lookup"><span data-stu-id="21a8c-1140">card num</span></span>
- <span data-ttu-id="21a8c-1141">cardNumber</span><span class="sxs-lookup"><span data-stu-id="21a8c-1141">cardnumber</span></span>
- <span data-ttu-id="21a8c-1142">cardnumbers</span><span class="sxs-lookup"><span data-stu-id="21a8c-1142">cardnumbers</span></span>
- <span data-ttu-id="21a8c-1143">card numbers</span><span class="sxs-lookup"><span data-stu-id="21a8c-1143">card numbers</span></span>
- <span data-ttu-id="21a8c-1144">CreditCard</span><span class="sxs-lookup"><span data-stu-id="21a8c-1144">creditcard</span></span>
- <span data-ttu-id="21a8c-1145">credit cards</span><span class="sxs-lookup"><span data-stu-id="21a8c-1145">credit cards</span></span>
- <span data-ttu-id="21a8c-1146">CreditCards</span><span class="sxs-lookup"><span data-stu-id="21a8c-1146">creditcards</span></span>
- <span data-ttu-id="21a8c-1147">CCN</span><span class="sxs-lookup"><span data-stu-id="21a8c-1147">ccn</span></span>
- <span data-ttu-id="21a8c-1148">card holder</span><span class="sxs-lookup"><span data-stu-id="21a8c-1148">card holder</span></span>
- <span data-ttu-id="21a8c-1149">aos</span><span class="sxs-lookup"><span data-stu-id="21a8c-1149">cardholder</span></span>
- <span data-ttu-id="21a8c-1150">card holders</span><span class="sxs-lookup"><span data-stu-id="21a8c-1150">card holders</span></span>
- <span data-ttu-id="21a8c-1151">titulares de cartões</span><span class="sxs-lookup"><span data-stu-id="21a8c-1151">cardholders</span></span>
- <span data-ttu-id="21a8c-1152">check card</span><span class="sxs-lookup"><span data-stu-id="21a8c-1152">check card</span></span>
- <span data-ttu-id="21a8c-1153">checkcard</span><span class="sxs-lookup"><span data-stu-id="21a8c-1153">checkcard</span></span>
- <span data-ttu-id="21a8c-1154">check cards</span><span class="sxs-lookup"><span data-stu-id="21a8c-1154">check cards</span></span>
- <span data-ttu-id="21a8c-1155">checkcards</span><span class="sxs-lookup"><span data-stu-id="21a8c-1155">checkcards</span></span>
- <span data-ttu-id="21a8c-1156">debit card</span><span class="sxs-lookup"><span data-stu-id="21a8c-1156">debit card</span></span>
- <span data-ttu-id="21a8c-1157">Debitcard</span><span class="sxs-lookup"><span data-stu-id="21a8c-1157">debitcard</span></span>
- <span data-ttu-id="21a8c-1158">debit cards</span><span class="sxs-lookup"><span data-stu-id="21a8c-1158">debit cards</span></span>
- <span data-ttu-id="21a8c-1159">debitcards</span><span class="sxs-lookup"><span data-stu-id="21a8c-1159">debitcards</span></span>
- <span data-ttu-id="21a8c-1160">atm card</span><span class="sxs-lookup"><span data-stu-id="21a8c-1160">atm card</span></span>
- <span data-ttu-id="21a8c-1161">atmcard</span><span class="sxs-lookup"><span data-stu-id="21a8c-1161">atmcard</span></span>
- <span data-ttu-id="21a8c-1162">atm cards</span><span class="sxs-lookup"><span data-stu-id="21a8c-1162">atm cards</span></span>
- <span data-ttu-id="21a8c-1163">atmcards</span><span class="sxs-lookup"><span data-stu-id="21a8c-1163">atmcards</span></span>
- <span data-ttu-id="21a8c-1164">encaminhar</span><span class="sxs-lookup"><span data-stu-id="21a8c-1164">enroute</span></span>
- <span data-ttu-id="21a8c-1165">en route</span><span class="sxs-lookup"><span data-stu-id="21a8c-1165">en route</span></span>
- <span data-ttu-id="21a8c-1166">card type</span><span class="sxs-lookup"><span data-stu-id="21a8c-1166">card type</span></span>
- <span data-ttu-id="21a8c-1167">carte bancaire</span><span class="sxs-lookup"><span data-stu-id="21a8c-1167">carte bancaire</span></span>
- <span data-ttu-id="21a8c-1168">carte de crédit</span><span class="sxs-lookup"><span data-stu-id="21a8c-1168">carte de crédit</span></span>
- <span data-ttu-id="21a8c-1169">carte de credit</span><span class="sxs-lookup"><span data-stu-id="21a8c-1169">carte de credit</span></span>
- <span data-ttu-id="21a8c-1170">numéro de carte</span><span class="sxs-lookup"><span data-stu-id="21a8c-1170">numéro de carte</span></span>
- <span data-ttu-id="21a8c-1171">numero de carte</span><span class="sxs-lookup"><span data-stu-id="21a8c-1171">numero de carte</span></span>
- <span data-ttu-id="21a8c-1172">nº de la carte</span><span class="sxs-lookup"><span data-stu-id="21a8c-1172">nº de la carte</span></span>
- <span data-ttu-id="21a8c-1173">nº de carte</span><span class="sxs-lookup"><span data-stu-id="21a8c-1173">nº de carte</span></span>
- <span data-ttu-id="21a8c-1174">kreditkarte</span><span class="sxs-lookup"><span data-stu-id="21a8c-1174">kreditkarte</span></span>
- <span data-ttu-id="21a8c-1175">Karte</span><span class="sxs-lookup"><span data-stu-id="21a8c-1175">karte</span></span>
- <span data-ttu-id="21a8c-1176">karteninhaber</span><span class="sxs-lookup"><span data-stu-id="21a8c-1176">karteninhaber</span></span>
- <span data-ttu-id="21a8c-1177">karteninhabers</span><span class="sxs-lookup"><span data-stu-id="21a8c-1177">karteninhabers</span></span>
- <span data-ttu-id="21a8c-1178">kreditkarteninhaber</span><span class="sxs-lookup"><span data-stu-id="21a8c-1178">kreditkarteninhaber</span></span>
- <span data-ttu-id="21a8c-1179">kreditkarteninstitut</span><span class="sxs-lookup"><span data-stu-id="21a8c-1179">kreditkarteninstitut</span></span>
- <span data-ttu-id="21a8c-1180">kreditkartentyp</span><span class="sxs-lookup"><span data-stu-id="21a8c-1180">kreditkartentyp</span></span>
- <span data-ttu-id="21a8c-1181">eigentümername</span><span class="sxs-lookup"><span data-stu-id="21a8c-1181">eigentümername</span></span>
- <span data-ttu-id="21a8c-1182">kartennr</span><span class="sxs-lookup"><span data-stu-id="21a8c-1182">kartennr</span></span> 
- <span data-ttu-id="21a8c-1183">kartennummer</span><span class="sxs-lookup"><span data-stu-id="21a8c-1183">kartennummer</span></span>
- <span data-ttu-id="21a8c-1184">kreditkartennummer</span><span class="sxs-lookup"><span data-stu-id="21a8c-1184">kreditkartennummer</span></span>
- <span data-ttu-id="21a8c-1185">kreditkarten-Nummer</span><span class="sxs-lookup"><span data-stu-id="21a8c-1185">kreditkarten-nummer</span></span>
- <span data-ttu-id="21a8c-1186">carta di credito</span><span class="sxs-lookup"><span data-stu-id="21a8c-1186">carta di credito</span></span>
- <span data-ttu-id="21a8c-1187">carta credito</span><span class="sxs-lookup"><span data-stu-id="21a8c-1187">carta credito</span></span>
- <span data-ttu-id="21a8c-1188">carta</span><span class="sxs-lookup"><span data-stu-id="21a8c-1188">carta</span></span>
- <span data-ttu-id="21a8c-1189">n carta</span><span class="sxs-lookup"><span data-stu-id="21a8c-1189">n carta</span></span>
- <span data-ttu-id="21a8c-1190">Nr.</span><span class="sxs-lookup"><span data-stu-id="21a8c-1190">nr.</span></span> <span data-ttu-id="21a8c-1191">carta</span><span class="sxs-lookup"><span data-stu-id="21a8c-1191">carta</span></span>
- <span data-ttu-id="21a8c-1192">nr carta</span><span class="sxs-lookup"><span data-stu-id="21a8c-1192">nr carta</span></span>
- <span data-ttu-id="21a8c-1193">numero carta</span><span class="sxs-lookup"><span data-stu-id="21a8c-1193">numero carta</span></span>
- <span data-ttu-id="21a8c-1194">numero della carta</span><span class="sxs-lookup"><span data-stu-id="21a8c-1194">numero della carta</span></span>
- <span data-ttu-id="21a8c-1195">numero di carta</span><span class="sxs-lookup"><span data-stu-id="21a8c-1195">numero di carta</span></span>
- <span data-ttu-id="21a8c-1196">tarjeta credito</span><span class="sxs-lookup"><span data-stu-id="21a8c-1196">tarjeta credito</span></span>
- <span data-ttu-id="21a8c-1197">tarjeta de credito</span><span class="sxs-lookup"><span data-stu-id="21a8c-1197">tarjeta de credito</span></span>
- <span data-ttu-id="21a8c-1198">tarjeta crédito</span><span class="sxs-lookup"><span data-stu-id="21a8c-1198">tarjeta crédito</span></span>
- <span data-ttu-id="21a8c-1199">tarjeta de crédito</span><span class="sxs-lookup"><span data-stu-id="21a8c-1199">tarjeta de crédito</span></span>
- <span data-ttu-id="21a8c-1200">tarjeta de atm</span><span class="sxs-lookup"><span data-stu-id="21a8c-1200">tarjeta de atm</span></span>
- <span data-ttu-id="21a8c-1201">tarjeta atm</span><span class="sxs-lookup"><span data-stu-id="21a8c-1201">tarjeta atm</span></span>
- <span data-ttu-id="21a8c-1202">tarjeta debito</span><span class="sxs-lookup"><span data-stu-id="21a8c-1202">tarjeta debito</span></span>
- <span data-ttu-id="21a8c-1203">tarjeta de debito</span><span class="sxs-lookup"><span data-stu-id="21a8c-1203">tarjeta de debito</span></span>
- <span data-ttu-id="21a8c-1204">tarjeta débito</span><span class="sxs-lookup"><span data-stu-id="21a8c-1204">tarjeta débito</span></span>
- <span data-ttu-id="21a8c-1205">tarjeta de débito</span><span class="sxs-lookup"><span data-stu-id="21a8c-1205">tarjeta de débito</span></span>
- <span data-ttu-id="21a8c-1206">nº de tarjeta</span><span class="sxs-lookup"><span data-stu-id="21a8c-1206">nº de tarjeta</span></span>
- <span data-ttu-id="21a8c-1207">Não.</span><span class="sxs-lookup"><span data-stu-id="21a8c-1207">no.</span></span> <span data-ttu-id="21a8c-1208">de tarjeta</span><span class="sxs-lookup"><span data-stu-id="21a8c-1208">de tarjeta</span></span>
- <span data-ttu-id="21a8c-1209">no de tarjeta</span><span class="sxs-lookup"><span data-stu-id="21a8c-1209">no de tarjeta</span></span>
- <span data-ttu-id="21a8c-1210">numero de tarjeta</span><span class="sxs-lookup"><span data-stu-id="21a8c-1210">numero de tarjeta</span></span>
- <span data-ttu-id="21a8c-1211">número de tarjeta</span><span class="sxs-lookup"><span data-stu-id="21a8c-1211">número de tarjeta</span></span>
- <span data-ttu-id="21a8c-1212">tarjeta no</span><span class="sxs-lookup"><span data-stu-id="21a8c-1212">tarjeta no</span></span>
- <span data-ttu-id="21a8c-1213">tarjetahabiente</span><span class="sxs-lookup"><span data-stu-id="21a8c-1213">tarjetahabiente</span></span>
- <span data-ttu-id="21a8c-1214">cartão de crédito</span><span class="sxs-lookup"><span data-stu-id="21a8c-1214">cartão de crédito</span></span>
- <span data-ttu-id="21a8c-1215">cartão de credito</span><span class="sxs-lookup"><span data-stu-id="21a8c-1215">cartão de credito</span></span>
- <span data-ttu-id="21a8c-1216">cartao de crédito</span><span class="sxs-lookup"><span data-stu-id="21a8c-1216">cartao de crédito</span></span>
- <span data-ttu-id="21a8c-1217">cartao de credito</span><span class="sxs-lookup"><span data-stu-id="21a8c-1217">cartao de credito</span></span>
- <span data-ttu-id="21a8c-1218">cartão de débito</span><span class="sxs-lookup"><span data-stu-id="21a8c-1218">cartão de débito</span></span>
- <span data-ttu-id="21a8c-1219">cartao de débito</span><span class="sxs-lookup"><span data-stu-id="21a8c-1219">cartao de débito</span></span>
- <span data-ttu-id="21a8c-1220">cartão de debito</span><span class="sxs-lookup"><span data-stu-id="21a8c-1220">cartão de debito</span></span>
- <span data-ttu-id="21a8c-1221">cartao de debito</span><span class="sxs-lookup"><span data-stu-id="21a8c-1221">cartao de debito</span></span>
- <span data-ttu-id="21a8c-1222">débito automático</span><span class="sxs-lookup"><span data-stu-id="21a8c-1222">débito automático</span></span>
- <span data-ttu-id="21a8c-1223">debito automatico</span><span class="sxs-lookup"><span data-stu-id="21a8c-1223">debito automatico</span></span>
- <span data-ttu-id="21a8c-1224">número do cartão</span><span class="sxs-lookup"><span data-stu-id="21a8c-1224">número do cartão</span></span>
- <span data-ttu-id="21a8c-1225">numero do cartão</span><span class="sxs-lookup"><span data-stu-id="21a8c-1225">numero do cartão</span></span> 
- <span data-ttu-id="21a8c-1226">número do cartao</span><span class="sxs-lookup"><span data-stu-id="21a8c-1226">número do cartao</span></span>
- <span data-ttu-id="21a8c-1227">numero do cartao</span><span class="sxs-lookup"><span data-stu-id="21a8c-1227">numero do cartao</span></span>
- <span data-ttu-id="21a8c-1228">número de cartão</span><span class="sxs-lookup"><span data-stu-id="21a8c-1228">número de cartão</span></span>
- <span data-ttu-id="21a8c-1229">numero de cartão</span><span class="sxs-lookup"><span data-stu-id="21a8c-1229">numero de cartão</span></span>
- <span data-ttu-id="21a8c-1230">número de cartao</span><span class="sxs-lookup"><span data-stu-id="21a8c-1230">número de cartao</span></span>
- <span data-ttu-id="21a8c-1231">numero de cartao</span><span class="sxs-lookup"><span data-stu-id="21a8c-1231">numero de cartao</span></span>
- <span data-ttu-id="21a8c-1232">nº do cartão</span><span class="sxs-lookup"><span data-stu-id="21a8c-1232">nº do cartão</span></span>
- <span data-ttu-id="21a8c-1233">nº do cartao</span><span class="sxs-lookup"><span data-stu-id="21a8c-1233">nº do cartao</span></span>
- <span data-ttu-id="21a8c-1234">n º.</span><span class="sxs-lookup"><span data-stu-id="21a8c-1234">nº.</span></span> <span data-ttu-id="21a8c-1235">do cartão</span><span class="sxs-lookup"><span data-stu-id="21a8c-1235">do cartão</span></span>
- <span data-ttu-id="21a8c-1236">no do cartão</span><span class="sxs-lookup"><span data-stu-id="21a8c-1236">no do cartão</span></span>
- <span data-ttu-id="21a8c-1237">no do cartao</span><span class="sxs-lookup"><span data-stu-id="21a8c-1237">no do cartao</span></span>
- <span data-ttu-id="21a8c-1238">Não.</span><span class="sxs-lookup"><span data-stu-id="21a8c-1238">no.</span></span> <span data-ttu-id="21a8c-1239">do cartão</span><span class="sxs-lookup"><span data-stu-id="21a8c-1239">do cartão</span></span>
- <span data-ttu-id="21a8c-1240">Não.</span><span class="sxs-lookup"><span data-stu-id="21a8c-1240">no.</span></span> <span data-ttu-id="21a8c-1241">do cartao</span><span class="sxs-lookup"><span data-stu-id="21a8c-1241">do cartao</span></span> 
   
## <a name="croatia-identity-card-number"></a><span data-ttu-id="21a8c-1242">	Número do Cartão de Identidade da Croácia</span><span class="sxs-lookup"><span data-stu-id="21a8c-1242">Croatia Identity Card Number</span></span>

### <a name="format"></a><span data-ttu-id="21a8c-1243">Format</span><span class="sxs-lookup"><span data-stu-id="21a8c-1243">Format</span></span>

<span data-ttu-id="21a8c-1244">Nove dígitos</span><span class="sxs-lookup"><span data-stu-id="21a8c-1244">Nine digits</span></span>

### <a name="pattern"></a><span data-ttu-id="21a8c-1245">Padrão</span><span class="sxs-lookup"><span data-stu-id="21a8c-1245">Pattern</span></span>

<span data-ttu-id="21a8c-1246">Nove dígitos consecutivos</span><span class="sxs-lookup"><span data-stu-id="21a8c-1246">Nine consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="21a8c-1247">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="21a8c-1247">Checksum</span></span>

<span data-ttu-id="21a8c-1248">Não</span><span class="sxs-lookup"><span data-stu-id="21a8c-1248">No</span></span>

### <a name="definition"></a><span data-ttu-id="21a8c-1249">Definição</span><span class="sxs-lookup"><span data-stu-id="21a8c-1249">Definition</span></span>

<span data-ttu-id="21a8c-1250">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="21a8c-1250">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="21a8c-1251">A função Func_croatia_id_card localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="21a8c-1251">The function Func_croatia_id_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="21a8c-1252">Uma palavra-chave de Keyword_croatia_id_card for encontrada.</span><span class="sxs-lookup"><span data-stu-id="21a8c-1252">A keyword from Keyword_croatia_id_card is found.</span></span>

```
<!--Croatia Identity Card Number-->
<Entity id="ff12f884-c20a-4189-b185-34c8e7258d47" recommendedConfidence="75" patternsProximity="300">
  <Pattern confidenceLevel="75">
     <IdMatch idRef="Func_croatia_id_card"/>
     <Match idRef="Keyword_croatia_id_card"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="21a8c-1253">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="21a8c-1253">Keywords</span></span>

#### <a name="keywordcroatiaidcard"></a><span data-ttu-id="21a8c-1254">Keyword_croatia_id_card</span><span class="sxs-lookup"><span data-stu-id="21a8c-1254">Keyword_croatia_id_card</span></span>

- <span data-ttu-id="21a8c-1255">Cartão de identidade croata</span><span class="sxs-lookup"><span data-stu-id="21a8c-1255">Croatian identity card</span></span>
- <span data-ttu-id="21a8c-1256">Osobna iskaznica</span><span class="sxs-lookup"><span data-stu-id="21a8c-1256">Osobna iskaznica</span></span>

   
## <a name="croatia-personal-identification-oib-number"></a><span data-ttu-id="21a8c-1257">	Número de Identificação Pessoal (OIB) da Croácia</span><span class="sxs-lookup"><span data-stu-id="21a8c-1257">Croatia Personal Identification (OIB) Number</span></span>

### <a name="format"></a><span data-ttu-id="21a8c-1258">Format</span><span class="sxs-lookup"><span data-stu-id="21a8c-1258">Format</span></span>

<span data-ttu-id="21a8c-1259">11 dígitos</span><span class="sxs-lookup"><span data-stu-id="21a8c-1259">11 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="21a8c-1260">Padrão</span><span class="sxs-lookup"><span data-stu-id="21a8c-1260">Pattern</span></span>

<span data-ttu-id="21a8c-1261">11 dígitos:</span><span class="sxs-lookup"><span data-stu-id="21a8c-1261">11 digits:</span></span>
- <span data-ttu-id="21a8c-1262">10 dígitos</span><span class="sxs-lookup"><span data-stu-id="21a8c-1262">10 digits</span></span> 
- <span data-ttu-id="21a8c-1263">O dígito final é um dígito de verificação para os fins de troca de dados internacionais, as letras de RH são adicionadas antes dos onze dígitos.</span><span class="sxs-lookup"><span data-stu-id="21a8c-1263">Final digit is a check digit For the purposes of international data exchange, the letters HR are added preceding the eleven digits.</span></span>

### <a name="checksum"></a><span data-ttu-id="21a8c-1264">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="21a8c-1264">Checksum</span></span>

<span data-ttu-id="21a8c-1265">Sim</span><span class="sxs-lookup"><span data-stu-id="21a8c-1265">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="21a8c-1266">Definição</span><span class="sxs-lookup"><span data-stu-id="21a8c-1266">Definition</span></span>

<span data-ttu-id="21a8c-1267">Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="21a8c-1267">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="21a8c-1268">A função Func_croatia_oib_number localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="21a8c-1268">The function Func_croatia_oib_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="21a8c-1269">Uma palavra-chave de Keyword_croatia_oib_number for encontrada.</span><span class="sxs-lookup"><span data-stu-id="21a8c-1269">A keyword from Keyword_croatia_oib_number is found.</span></span>
- <span data-ttu-id="21a8c-1270">A soma de verificação passa.</span><span class="sxs-lookup"><span data-stu-id="21a8c-1270">The checksum passes.</span></span>

<span data-ttu-id="21a8c-1271">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="21a8c-1271">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="21a8c-1272">A função Func_croatia_oib_number localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="21a8c-1272">The function Func_croatia_oib_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="21a8c-1273">A soma de verificação passa.</span><span class="sxs-lookup"><span data-stu-id="21a8c-1273">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="21a8c-1274">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="21a8c-1274">Keywords</span></span>

#### <a name="keywordcroatiaoibnumber"></a><span data-ttu-id="21a8c-1275">Keyword_croatia_oib_number</span><span class="sxs-lookup"><span data-stu-id="21a8c-1275">Keyword_croatia_oib_number</span></span>

- <span data-ttu-id="21a8c-1276">Número de Identificação Pessoal</span><span class="sxs-lookup"><span data-stu-id="21a8c-1276">Personal Identification Number</span></span>
- <span data-ttu-id="21a8c-1277">Osobni identifikacijski broj</span><span class="sxs-lookup"><span data-stu-id="21a8c-1277">Osobni identifikacijski broj</span></span> 
- <span data-ttu-id="21a8c-1278">NIB</span><span class="sxs-lookup"><span data-stu-id="21a8c-1278">OIB</span></span> 

   
## <a name="czech-personal-identity-number"></a><span data-ttu-id="21a8c-1279">Número de identidade pessoal tcheco</span><span class="sxs-lookup"><span data-stu-id="21a8c-1279">Czech Personal Identity Number</span></span>

### <a name="format"></a><span data-ttu-id="21a8c-1280">Format</span><span class="sxs-lookup"><span data-stu-id="21a8c-1280">Format</span></span>

<span data-ttu-id="21a8c-1281">Nove dígitos com barra de avanço opcional (formato antigo) 10 dígitos com barra de avanço opcional (novo formato)</span><span class="sxs-lookup"><span data-stu-id="21a8c-1281">Nine digits with optional forward slash (old format) 10 digits with optional forward slash (new format)</span></span>

### <a name="pattern"></a><span data-ttu-id="21a8c-1282">Padrão</span><span class="sxs-lookup"><span data-stu-id="21a8c-1282">Pattern</span></span>

<span data-ttu-id="21a8c-1283">Nove dígitos (formato antigo):</span><span class="sxs-lookup"><span data-stu-id="21a8c-1283">Nine digits (old format):</span></span>
- <span data-ttu-id="21a8c-1284">Nove dígitos</span><span class="sxs-lookup"><span data-stu-id="21a8c-1284">Nine digits</span></span>

<span data-ttu-id="21a8c-1285">OU</span><span class="sxs-lookup"><span data-stu-id="21a8c-1285">OR</span></span>

- <span data-ttu-id="21a8c-1286">Seis dígitos que representam a data de nascimento</span><span class="sxs-lookup"><span data-stu-id="21a8c-1286">Six digits that represent date of birth</span></span>
- <span data-ttu-id="21a8c-1287">Uma barra</span><span class="sxs-lookup"><span data-stu-id="21a8c-1287">A forward slash</span></span>
- <span data-ttu-id="21a8c-1288">Três dígitos</span><span class="sxs-lookup"><span data-stu-id="21a8c-1288">Three digits</span></span>

<span data-ttu-id="21a8c-1289">10 dígitos (novo formato):</span><span class="sxs-lookup"><span data-stu-id="21a8c-1289">10 digits (new format):</span></span>
- <span data-ttu-id="21a8c-1290">10 dígitos</span><span class="sxs-lookup"><span data-stu-id="21a8c-1290">10 digits</span></span>

<span data-ttu-id="21a8c-1291">OU</span><span class="sxs-lookup"><span data-stu-id="21a8c-1291">OR</span></span>

- <span data-ttu-id="21a8c-1292">Seis dígitos que representam a data de nascimento</span><span class="sxs-lookup"><span data-stu-id="21a8c-1292">Six digits that represent date of birth</span></span>
- <span data-ttu-id="21a8c-1293">Uma barra</span><span class="sxs-lookup"><span data-stu-id="21a8c-1293">A forward slash</span></span> 
- <span data-ttu-id="21a8c-1294">Quatro dígitos onde o último dígito é um dígito de verificação</span><span class="sxs-lookup"><span data-stu-id="21a8c-1294">Four digits where last digit is a check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="21a8c-1295">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="21a8c-1295">Checksum</span></span>

<span data-ttu-id="21a8c-1296">Sim</span><span class="sxs-lookup"><span data-stu-id="21a8c-1296">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="21a8c-1297">Definição</span><span class="sxs-lookup"><span data-stu-id="21a8c-1297">Definition</span></span>

<span data-ttu-id="21a8c-1298">Uma política de DLP é de 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres: a função Func_czech_id_card localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="21a8c-1298">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters: The function Func_czech_id_card finds content that matches the pattern.</span></span>
<span data-ttu-id="21a8c-1299">Uma palavra-chave de Keyword_czech_id_card for encontrada.</span><span class="sxs-lookup"><span data-stu-id="21a8c-1299">A keyword from Keyword_czech_id_card is found.</span></span>
<span data-ttu-id="21a8c-1300">A soma de verificação passa.</span><span class="sxs-lookup"><span data-stu-id="21a8c-1300">The checksum passes.</span></span>

```
<!-- Czech Personal Identity Number -->
<Entity id="60c0725a-4eb6-455b-9dda-05d8a7396497"      patternsProximity="300" recommendedConfidence="85">
   <Pattern confidenceLevel="85">
      <IdMatch idRef="Func_czech_id_card" />
      <Match idRef="Keyword_czech_id_card" />
   </Pattern>
</Entity>
```
### <a name="keywords"></a><span data-ttu-id="21a8c-1301">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="21a8c-1301">Keywords</span></span>

- <span data-ttu-id="21a8c-1302">número de identidade pessoal tcheco</span><span class="sxs-lookup"><span data-stu-id="21a8c-1302">czech personal identity number</span></span>
- <span data-ttu-id="21a8c-1303">Rodné číslo</span><span class="sxs-lookup"><span data-stu-id="21a8c-1303">Rodné číslo</span></span>
   
## <a name="denmark-personal-identification-number"></a><span data-ttu-id="21a8c-1304">	Número de Identificação Pessoal da Dinamarca</span><span class="sxs-lookup"><span data-stu-id="21a8c-1304">Denmark Personal Identification Number</span></span>

### <a name="format"></a><span data-ttu-id="21a8c-1305">Format</span><span class="sxs-lookup"><span data-stu-id="21a8c-1305">Format</span></span>

<span data-ttu-id="21a8c-1306">10 dígitos que contêm um hífen</span><span class="sxs-lookup"><span data-stu-id="21a8c-1306">10 digits containing a hyphen</span></span>

### <a name="pattern"></a><span data-ttu-id="21a8c-1307">Padrão</span><span class="sxs-lookup"><span data-stu-id="21a8c-1307">Pattern</span></span>

<span data-ttu-id="21a8c-1308">10 dígitos:</span><span class="sxs-lookup"><span data-stu-id="21a8c-1308">10 digits:</span></span>
- <span data-ttu-id="21a8c-1309">Seis dígitos no formato DDMMAA que são a data de nascimento</span><span class="sxs-lookup"><span data-stu-id="21a8c-1309">Six digits in the format DDMMYY which are the date of birth</span></span> 
- <span data-ttu-id="21a8c-1310">Um hífen</span><span class="sxs-lookup"><span data-stu-id="21a8c-1310">A hyphen</span></span> 
- <span data-ttu-id="21a8c-1311">Quatro dígitos em que o último é um dígito de verificação</span><span class="sxs-lookup"><span data-stu-id="21a8c-1311">Four digits where the final digit is a check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="21a8c-1312">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="21a8c-1312">Checksum</span></span>

<span data-ttu-id="21a8c-1313">Sim</span><span class="sxs-lookup"><span data-stu-id="21a8c-1313">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="21a8c-1314">Definição</span><span class="sxs-lookup"><span data-stu-id="21a8c-1314">Definition</span></span>

<span data-ttu-id="21a8c-1315">Uma política de DLP é de 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres: a expressão regular Regex_denmark_id localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="21a8c-1315">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters: The regular expression Regex_denmark_id finds content that matches the pattern.</span></span>
<span data-ttu-id="21a8c-1316">Uma palavra-chave de Keyword_denmark_id for encontrada.</span><span class="sxs-lookup"><span data-stu-id="21a8c-1316">A keyword from Keyword_denmark_id is found.</span></span>
<span data-ttu-id="21a8c-1317">A soma de verificação passa.</span><span class="sxs-lookup"><span data-stu-id="21a8c-1317">The checksum passes.</span></span>

```
<!-- Denmark Personal Identification Number -->
<Entity id="6c4f2fef-56e1-4c00-8093-88d7a01cf460" recommendedConfidence="75" patternsProximity="300">
  <Pattern confidenceLevel="75">
     <IdMatch idRef="Regex_denmark_id"/>
     <Match idRef="Keyword_denmark_id"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="21a8c-1318">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="21a8c-1318">Keywords</span></span>

#### <a name="keyworddenmarkid"></a><span data-ttu-id="21a8c-1319">Keyword_denmark_id</span><span class="sxs-lookup"><span data-stu-id="21a8c-1319">Keyword_denmark_id</span></span>

- <span data-ttu-id="21a8c-1320">Número de Identificação Pessoal</span><span class="sxs-lookup"><span data-stu-id="21a8c-1320">Personal Identification Number</span></span>
- <span data-ttu-id="21a8c-1321">PEDIR</span><span class="sxs-lookup"><span data-stu-id="21a8c-1321">CPR</span></span>
- <span data-ttu-id="21a8c-1322">Det Centrale Personregister</span><span class="sxs-lookup"><span data-stu-id="21a8c-1322">Det Centrale Personregister</span></span>
- <span data-ttu-id="21a8c-1323">Personnummer</span><span class="sxs-lookup"><span data-stu-id="21a8c-1323">Personnummer</span></span>
   
## <a name="drug-enforcement-agency-dea-number"></a><span data-ttu-id="21a8c-1324">Número da Drug Enforcement Agency (DEA)</span><span class="sxs-lookup"><span data-stu-id="21a8c-1324">Drug Enforcement Agency (DEA) Number</span></span>

### <a name="format"></a><span data-ttu-id="21a8c-1325">Format</span><span class="sxs-lookup"><span data-stu-id="21a8c-1325">Format</span></span>

<span data-ttu-id="21a8c-1326">Duas letras seguidas por sete dígitos</span><span class="sxs-lookup"><span data-stu-id="21a8c-1326">Two letters followed by seven digits</span></span>

### <a name="pattern"></a><span data-ttu-id="21a8c-1327">Padrão</span><span class="sxs-lookup"><span data-stu-id="21a8c-1327">Pattern</span></span>

<span data-ttu-id="21a8c-1328">O padrão deve incluir todos os seguintes itens:</span><span class="sxs-lookup"><span data-stu-id="21a8c-1328">Pattern must include all of the following:</span></span>
- <span data-ttu-id="21a8c-1329">Uma letra (não diferencia maiúscula de minúscula) deste conjunto de letras possíveis: abcdefghjklmnprstux, que é um código de inscrito</span><span class="sxs-lookup"><span data-stu-id="21a8c-1329">One letter (not case sensitive) from this set of possible letters: abcdefghjklmnprstux, which is a registrant code</span></span> 
- <span data-ttu-id="21a8c-1330">Uma letra (não diferencia maiúscula de minúscula), que é a primeira letra do sobrenome do inscrito</span><span class="sxs-lookup"><span data-stu-id="21a8c-1330">One letter (not case sensitive), which is the first letter of the registrant's last name</span></span> 
- <span data-ttu-id="21a8c-1331">Sete dígitos, dos quais o último é o dígito de verificação</span><span class="sxs-lookup"><span data-stu-id="21a8c-1331">Seven digits, the last of which is the check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="21a8c-1332">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="21a8c-1332">Checksum</span></span>

<span data-ttu-id="21a8c-1333">Sim</span><span class="sxs-lookup"><span data-stu-id="21a8c-1333">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="21a8c-1334">Definição</span><span class="sxs-lookup"><span data-stu-id="21a8c-1334">Definition</span></span>

<span data-ttu-id="21a8c-1335">Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="21a8c-1335">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="21a8c-1336">A função Func_dea_number localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="21a8c-1336">The function Func_dea_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="21a8c-1337">A soma de verificação passa.</span><span class="sxs-lookup"><span data-stu-id="21a8c-1337">The checksum passes.</span></span>

```
<!-- DEA Number -->
<Entity id="9a5445ad-406e-43eb-8bd7-cac17ab6d0e4" recommendedConfidence="85" patternsProximity="300">
  <Pattern confidenceLevel="85">
     <IdMatch idRef="Func_dea_number"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="21a8c-1338">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="21a8c-1338">Keywords</span></span>

<span data-ttu-id="21a8c-1339">Nenhum</span><span class="sxs-lookup"><span data-stu-id="21a8c-1339">None</span></span>

   
## <a name="eu-debit-card-number"></a><span data-ttu-id="21a8c-1340">Número de cartão de débito da UE</span><span class="sxs-lookup"><span data-stu-id="21a8c-1340">EU Debit Card Number</span></span>

### <a name="format"></a><span data-ttu-id="21a8c-1341">Format</span><span class="sxs-lookup"><span data-stu-id="21a8c-1341">Format</span></span>

<span data-ttu-id="21a8c-1342">16 dígitos</span><span class="sxs-lookup"><span data-stu-id="21a8c-1342">16 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="21a8c-1343">Padrão</span><span class="sxs-lookup"><span data-stu-id="21a8c-1343">Pattern</span></span>

<span data-ttu-id="21a8c-1344">Padrão muito complexo e robusto</span><span class="sxs-lookup"><span data-stu-id="21a8c-1344">Very complex and robust pattern</span></span>

### <a name="checksum"></a><span data-ttu-id="21a8c-1345">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="21a8c-1345">Checksum</span></span>

<span data-ttu-id="21a8c-1346">Sim</span><span class="sxs-lookup"><span data-stu-id="21a8c-1346">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="21a8c-1347">Definição</span><span class="sxs-lookup"><span data-stu-id="21a8c-1347">Definition</span></span>

<span data-ttu-id="21a8c-1348">Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="21a8c-1348">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="21a8c-1349">A função Func_eu_debit_card localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="21a8c-1349">The function Func_eu_debit_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="21a8c-1350">Pelo menos uma das seguintes opções for verdadeira:</span><span class="sxs-lookup"><span data-stu-id="21a8c-1350">At least one of the following is true:</span></span>
    - <span data-ttu-id="21a8c-1351">Uma palavra-chave de Keyword_eu_debit_card for encontrada.</span><span class="sxs-lookup"><span data-stu-id="21a8c-1351">A keyword from Keyword_eu_debit_card is found.</span></span>
    - <span data-ttu-id="21a8c-1352">Uma palavra-chave de Keyword_card_terms_dict for encontrada.</span><span class="sxs-lookup"><span data-stu-id="21a8c-1352">A keyword from Keyword_card_terms_dict is found.</span></span>
    - <span data-ttu-id="21a8c-1353">Uma palavra-chave de Keyword_card_security_terms_dict for encontrada.</span><span class="sxs-lookup"><span data-stu-id="21a8c-1353">A keyword from Keyword_card_security_terms_dict is found.</span></span>
    - <span data-ttu-id="21a8c-1354">Uma palavra-chave de Keyword_card_expiration_terms_dict for encontrada.</span><span class="sxs-lookup"><span data-stu-id="21a8c-1354">A keyword from Keyword_card_expiration_terms_dict is found.</span></span>
    - <span data-ttu-id="21a8c-1355">A função Func_expiration_date encontra uma data no formato de data à direita.</span><span class="sxs-lookup"><span data-stu-id="21a8c-1355">The function Func_expiration_date finds a date in the right date format.</span></span>
- <span data-ttu-id="21a8c-1356">A soma de verificação passa.</span><span class="sxs-lookup"><span data-stu-id="21a8c-1356">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="21a8c-1357">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="21a8c-1357">Keywords</span></span>

#### <a name="keywordeudebitcard"></a><span data-ttu-id="21a8c-1358">Keyword_eu_debit_card</span><span class="sxs-lookup"><span data-stu-id="21a8c-1358">Keyword_eu_debit_card</span></span>

- <span data-ttu-id="21a8c-1359">account number</span><span class="sxs-lookup"><span data-stu-id="21a8c-1359">account number</span></span> 
- <span data-ttu-id="21a8c-1360">card number</span><span class="sxs-lookup"><span data-stu-id="21a8c-1360">card number</span></span> 
- <span data-ttu-id="21a8c-1361">card no.</span><span class="sxs-lookup"><span data-stu-id="21a8c-1361">card no.</span></span> 
- <span data-ttu-id="21a8c-1362">security number</span><span class="sxs-lookup"><span data-stu-id="21a8c-1362">security number</span></span> 
- <span data-ttu-id="21a8c-1363">colocado</span><span class="sxs-lookup"><span data-stu-id="21a8c-1363">cc#</span></span> 

#### <a name="keywordcardtermsdict"></a><span data-ttu-id="21a8c-1364">Keyword_card_terms_dict</span><span class="sxs-lookup"><span data-stu-id="21a8c-1364">Keyword_card_terms_dict</span></span>

- <span data-ttu-id="21a8c-1365">acct nbr</span><span class="sxs-lookup"><span data-stu-id="21a8c-1365">acct nbr</span></span> 
- <span data-ttu-id="21a8c-1366">acct num</span><span class="sxs-lookup"><span data-stu-id="21a8c-1366">acct num</span></span> 
- <span data-ttu-id="21a8c-1367">acct no</span><span class="sxs-lookup"><span data-stu-id="21a8c-1367">acct no</span></span> 
- <span data-ttu-id="21a8c-1368">american express</span><span class="sxs-lookup"><span data-stu-id="21a8c-1368">american express</span></span> 
- <span data-ttu-id="21a8c-1369">americanexpress</span><span class="sxs-lookup"><span data-stu-id="21a8c-1369">americanexpress</span></span> 
- <span data-ttu-id="21a8c-1370">americano espresso</span><span class="sxs-lookup"><span data-stu-id="21a8c-1370">americano espresso</span></span> 
- <span data-ttu-id="21a8c-1371">Amex</span><span class="sxs-lookup"><span data-stu-id="21a8c-1371">amex</span></span> 
- <span data-ttu-id="21a8c-1372">atm card</span><span class="sxs-lookup"><span data-stu-id="21a8c-1372">atm card</span></span> 
- <span data-ttu-id="21a8c-1373">atm cards</span><span class="sxs-lookup"><span data-stu-id="21a8c-1373">atm cards</span></span> 
- <span data-ttu-id="21a8c-1374">atm kaart</span><span class="sxs-lookup"><span data-stu-id="21a8c-1374">atm kaart</span></span> 
- <span data-ttu-id="21a8c-1375">atmcard</span><span class="sxs-lookup"><span data-stu-id="21a8c-1375">atmcard</span></span> 
- <span data-ttu-id="21a8c-1376">atmcards</span><span class="sxs-lookup"><span data-stu-id="21a8c-1376">atmcards</span></span> 
- <span data-ttu-id="21a8c-1377">atmkaart</span><span class="sxs-lookup"><span data-stu-id="21a8c-1377">atmkaart</span></span> 
- <span data-ttu-id="21a8c-1378">atmkaarten</span><span class="sxs-lookup"><span data-stu-id="21a8c-1378">atmkaarten</span></span> 
- <span data-ttu-id="21a8c-1379">Bancontact</span><span class="sxs-lookup"><span data-stu-id="21a8c-1379">bancontact</span></span> 
- <span data-ttu-id="21a8c-1380">bank card</span><span class="sxs-lookup"><span data-stu-id="21a8c-1380">bank card</span></span> 
- <span data-ttu-id="21a8c-1381">bankkaart</span><span class="sxs-lookup"><span data-stu-id="21a8c-1381">bankkaart</span></span> 
- <span data-ttu-id="21a8c-1382">card holder</span><span class="sxs-lookup"><span data-stu-id="21a8c-1382">card holder</span></span> 
- <span data-ttu-id="21a8c-1383">card holders</span><span class="sxs-lookup"><span data-stu-id="21a8c-1383">card holders</span></span> 
- <span data-ttu-id="21a8c-1384">card num</span><span class="sxs-lookup"><span data-stu-id="21a8c-1384">card num</span></span> 
- <span data-ttu-id="21a8c-1385">card number</span><span class="sxs-lookup"><span data-stu-id="21a8c-1385">card number</span></span> 
- <span data-ttu-id="21a8c-1386">card numbers</span><span class="sxs-lookup"><span data-stu-id="21a8c-1386">card numbers</span></span> 
- <span data-ttu-id="21a8c-1387">card type</span><span class="sxs-lookup"><span data-stu-id="21a8c-1387">card type</span></span> 
- <span data-ttu-id="21a8c-1388">cardano numerico</span><span class="sxs-lookup"><span data-stu-id="21a8c-1388">cardano numerico</span></span> 
- <span data-ttu-id="21a8c-1389">aos</span><span class="sxs-lookup"><span data-stu-id="21a8c-1389">cardholder</span></span> 
- <span data-ttu-id="21a8c-1390">titulares de cartões</span><span class="sxs-lookup"><span data-stu-id="21a8c-1390">cardholders</span></span> 
- <span data-ttu-id="21a8c-1391">cardNumber</span><span class="sxs-lookup"><span data-stu-id="21a8c-1391">cardnumber</span></span> 
- <span data-ttu-id="21a8c-1392">cardnumbers</span><span class="sxs-lookup"><span data-stu-id="21a8c-1392">cardnumbers</span></span> 
- <span data-ttu-id="21a8c-1393">carta bianca</span><span class="sxs-lookup"><span data-stu-id="21a8c-1393">carta bianca</span></span> 
- <span data-ttu-id="21a8c-1394">carta credito</span><span class="sxs-lookup"><span data-stu-id="21a8c-1394">carta credito</span></span> 
- <span data-ttu-id="21a8c-1395">carta di credito</span><span class="sxs-lookup"><span data-stu-id="21a8c-1395">carta di credito</span></span> 
- <span data-ttu-id="21a8c-1396">cartao de credito</span><span class="sxs-lookup"><span data-stu-id="21a8c-1396">cartao de credito</span></span> 
- <span data-ttu-id="21a8c-1397">cartao de crédito</span><span class="sxs-lookup"><span data-stu-id="21a8c-1397">cartao de crédito</span></span> 
- <span data-ttu-id="21a8c-1398">cartao de debito</span><span class="sxs-lookup"><span data-stu-id="21a8c-1398">cartao de debito</span></span> 
- <span data-ttu-id="21a8c-1399">cartao de débito</span><span class="sxs-lookup"><span data-stu-id="21a8c-1399">cartao de débito</span></span> 
- <span data-ttu-id="21a8c-1400">carte bancaire</span><span class="sxs-lookup"><span data-stu-id="21a8c-1400">carte bancaire</span></span> 
- <span data-ttu-id="21a8c-1401">carte blanche</span><span class="sxs-lookup"><span data-stu-id="21a8c-1401">carte blanche</span></span> 
- <span data-ttu-id="21a8c-1402">carte bleue</span><span class="sxs-lookup"><span data-stu-id="21a8c-1402">carte bleue</span></span> 
- <span data-ttu-id="21a8c-1403">carte de credit</span><span class="sxs-lookup"><span data-stu-id="21a8c-1403">carte de credit</span></span> 
- <span data-ttu-id="21a8c-1404">carte de crédit</span><span class="sxs-lookup"><span data-stu-id="21a8c-1404">carte de crédit</span></span> 
- <span data-ttu-id="21a8c-1405">carte di credito</span><span class="sxs-lookup"><span data-stu-id="21a8c-1405">carte di credito</span></span> 
- <span data-ttu-id="21a8c-1406">carteblanche</span><span class="sxs-lookup"><span data-stu-id="21a8c-1406">carteblanche</span></span> 
- <span data-ttu-id="21a8c-1407">cartão de credito</span><span class="sxs-lookup"><span data-stu-id="21a8c-1407">cartão de credito</span></span> 
- <span data-ttu-id="21a8c-1408">cartão de crédito</span><span class="sxs-lookup"><span data-stu-id="21a8c-1408">cartão de crédito</span></span> 
- <span data-ttu-id="21a8c-1409">cartão de debito</span><span class="sxs-lookup"><span data-stu-id="21a8c-1409">cartão de debito</span></span> 
- <span data-ttu-id="21a8c-1410">cartão de débito</span><span class="sxs-lookup"><span data-stu-id="21a8c-1410">cartão de débito</span></span> 
- <span data-ttu-id="21a8c-1411">cb</span><span class="sxs-lookup"><span data-stu-id="21a8c-1411">cb</span></span> 
- <span data-ttu-id="21a8c-1412">CCN</span><span class="sxs-lookup"><span data-stu-id="21a8c-1412">ccn</span></span> 
- <span data-ttu-id="21a8c-1413">check card</span><span class="sxs-lookup"><span data-stu-id="21a8c-1413">check card</span></span> 
- <span data-ttu-id="21a8c-1414">check cards</span><span class="sxs-lookup"><span data-stu-id="21a8c-1414">check cards</span></span> 
- <span data-ttu-id="21a8c-1415">checkcard</span><span class="sxs-lookup"><span data-stu-id="21a8c-1415">checkcard</span></span>
- <span data-ttu-id="21a8c-1416">checkcards</span><span class="sxs-lookup"><span data-stu-id="21a8c-1416">checkcards</span></span> 
- <span data-ttu-id="21a8c-1417">chequekaart</span><span class="sxs-lookup"><span data-stu-id="21a8c-1417">chequekaart</span></span> 
- <span data-ttu-id="21a8c-1418">Cirrus</span><span class="sxs-lookup"><span data-stu-id="21a8c-1418">cirrus</span></span> 
- <span data-ttu-id="21a8c-1419">Cirrus-EDC-maestro</span><span class="sxs-lookup"><span data-stu-id="21a8c-1419">cirrus-edc-maestro</span></span> 
- <span data-ttu-id="21a8c-1420">controlekaart</span><span class="sxs-lookup"><span data-stu-id="21a8c-1420">controlekaart</span></span> 
- <span data-ttu-id="21a8c-1421">controlekaarten</span><span class="sxs-lookup"><span data-stu-id="21a8c-1421">controlekaarten</span></span> 
- <span data-ttu-id="21a8c-1422">credit card</span><span class="sxs-lookup"><span data-stu-id="21a8c-1422">credit card</span></span> 
- <span data-ttu-id="21a8c-1423">credit cards</span><span class="sxs-lookup"><span data-stu-id="21a8c-1423">credit cards</span></span> 
- <span data-ttu-id="21a8c-1424">CreditCard</span><span class="sxs-lookup"><span data-stu-id="21a8c-1424">creditcard</span></span> 
- <span data-ttu-id="21a8c-1425">CreditCards</span><span class="sxs-lookup"><span data-stu-id="21a8c-1425">creditcards</span></span> 
- <span data-ttu-id="21a8c-1426">debetkaart</span><span class="sxs-lookup"><span data-stu-id="21a8c-1426">debetkaart</span></span> 
- <span data-ttu-id="21a8c-1427">debetkaarten</span><span class="sxs-lookup"><span data-stu-id="21a8c-1427">debetkaarten</span></span> 
- <span data-ttu-id="21a8c-1428">debit card</span><span class="sxs-lookup"><span data-stu-id="21a8c-1428">debit card</span></span> 
- <span data-ttu-id="21a8c-1429">debit cards</span><span class="sxs-lookup"><span data-stu-id="21a8c-1429">debit cards</span></span> 
- <span data-ttu-id="21a8c-1430">Debitcard</span><span class="sxs-lookup"><span data-stu-id="21a8c-1430">debitcard</span></span> 
- <span data-ttu-id="21a8c-1431">debitcards</span><span class="sxs-lookup"><span data-stu-id="21a8c-1431">debitcards</span></span> 
- <span data-ttu-id="21a8c-1432">debito automatico</span><span class="sxs-lookup"><span data-stu-id="21a8c-1432">debito automatico</span></span> 
- <span data-ttu-id="21a8c-1433">diners club</span><span class="sxs-lookup"><span data-stu-id="21a8c-1433">diners club</span></span> 
- <span data-ttu-id="21a8c-1434">Dinersclub</span><span class="sxs-lookup"><span data-stu-id="21a8c-1434">dinersclub</span></span> 
- <span data-ttu-id="21a8c-1435">tect</span><span class="sxs-lookup"><span data-stu-id="21a8c-1435">discover</span></span> 
- <span data-ttu-id="21a8c-1436">discover card</span><span class="sxs-lookup"><span data-stu-id="21a8c-1436">discover card</span></span> 
- <span data-ttu-id="21a8c-1437">discover cards</span><span class="sxs-lookup"><span data-stu-id="21a8c-1437">discover cards</span></span> 
- <span data-ttu-id="21a8c-1438">DiscoverCard</span><span class="sxs-lookup"><span data-stu-id="21a8c-1438">discovercard</span></span> 
- <span data-ttu-id="21a8c-1439">discovercards</span><span class="sxs-lookup"><span data-stu-id="21a8c-1439">discovercards</span></span> 
- <span data-ttu-id="21a8c-1440">débito automático</span><span class="sxs-lookup"><span data-stu-id="21a8c-1440">débito automático</span></span>
- <span data-ttu-id="21a8c-1441">EDC</span><span class="sxs-lookup"><span data-stu-id="21a8c-1441">edc</span></span> 
- <span data-ttu-id="21a8c-1442">eigentümername</span><span class="sxs-lookup"><span data-stu-id="21a8c-1442">eigentümername</span></span> 
- <span data-ttu-id="21a8c-1443">european debit card</span><span class="sxs-lookup"><span data-stu-id="21a8c-1443">european debit card</span></span> 
- <span data-ttu-id="21a8c-1444">hoofdkaart</span><span class="sxs-lookup"><span data-stu-id="21a8c-1444">hoofdkaart</span></span> 
- <span data-ttu-id="21a8c-1445">hoofdkaarten</span><span class="sxs-lookup"><span data-stu-id="21a8c-1445">hoofdkaarten</span></span> 
- <span data-ttu-id="21a8c-1446">in viaggio</span><span class="sxs-lookup"><span data-stu-id="21a8c-1446">in viaggio</span></span> 
- <span data-ttu-id="21a8c-1447">japanese card bureau</span><span class="sxs-lookup"><span data-stu-id="21a8c-1447">japanese card bureau</span></span> 
- <span data-ttu-id="21a8c-1448">japanse kaartdienst</span><span class="sxs-lookup"><span data-stu-id="21a8c-1448">japanse kaartdienst</span></span> 
- <span data-ttu-id="21a8c-1449">JCB</span><span class="sxs-lookup"><span data-stu-id="21a8c-1449">jcb</span></span> 
- <span data-ttu-id="21a8c-1450">kaart</span><span class="sxs-lookup"><span data-stu-id="21a8c-1450">kaart</span></span> 
- <span data-ttu-id="21a8c-1451">kaart num</span><span class="sxs-lookup"><span data-stu-id="21a8c-1451">kaart num</span></span> 
- <span data-ttu-id="21a8c-1452">kaartaantal</span><span class="sxs-lookup"><span data-stu-id="21a8c-1452">kaartaantal</span></span> 
- <span data-ttu-id="21a8c-1453">kaartaantallen</span><span class="sxs-lookup"><span data-stu-id="21a8c-1453">kaartaantallen</span></span> 
- <span data-ttu-id="21a8c-1454">kaarthouder</span><span class="sxs-lookup"><span data-stu-id="21a8c-1454">kaarthouder</span></span> 
- <span data-ttu-id="21a8c-1455">kaarthouders</span><span class="sxs-lookup"><span data-stu-id="21a8c-1455">kaarthouders</span></span> 
- <span data-ttu-id="21a8c-1456">Karte</span><span class="sxs-lookup"><span data-stu-id="21a8c-1456">karte</span></span>  
- <span data-ttu-id="21a8c-1457">karteninhaber</span><span class="sxs-lookup"><span data-stu-id="21a8c-1457">karteninhaber</span></span> 
- <span data-ttu-id="21a8c-1458">karteninhabers</span><span class="sxs-lookup"><span data-stu-id="21a8c-1458">karteninhabers</span></span>
- <span data-ttu-id="21a8c-1459">kartennr</span><span class="sxs-lookup"><span data-stu-id="21a8c-1459">kartennr</span></span> 
- <span data-ttu-id="21a8c-1460">kartennummer</span><span class="sxs-lookup"><span data-stu-id="21a8c-1460">kartennummer</span></span> 
- <span data-ttu-id="21a8c-1461">kreditkarte</span><span class="sxs-lookup"><span data-stu-id="21a8c-1461">kreditkarte</span></span> 
- <span data-ttu-id="21a8c-1462">kreditkarten-Nummer</span><span class="sxs-lookup"><span data-stu-id="21a8c-1462">kreditkarten-nummer</span></span> 
- <span data-ttu-id="21a8c-1463">kreditkarteninhaber</span><span class="sxs-lookup"><span data-stu-id="21a8c-1463">kreditkarteninhaber</span></span> 
- <span data-ttu-id="21a8c-1464">kreditkarteninstitut</span><span class="sxs-lookup"><span data-stu-id="21a8c-1464">kreditkarteninstitut</span></span> 
- <span data-ttu-id="21a8c-1465">kreditkartennummer</span><span class="sxs-lookup"><span data-stu-id="21a8c-1465">kreditkartennummer</span></span> 
- <span data-ttu-id="21a8c-1466">kreditkartentyp</span><span class="sxs-lookup"><span data-stu-id="21a8c-1466">kreditkartentyp</span></span> 
- <span data-ttu-id="21a8c-1467">Maestro</span><span class="sxs-lookup"><span data-stu-id="21a8c-1467">maestro</span></span> 
- <span data-ttu-id="21a8c-1468">master card</span><span class="sxs-lookup"><span data-stu-id="21a8c-1468">master card</span></span> 
- <span data-ttu-id="21a8c-1469">master cards</span><span class="sxs-lookup"><span data-stu-id="21a8c-1469">master cards</span></span> 
- <span data-ttu-id="21a8c-1470">MasterCard</span><span class="sxs-lookup"><span data-stu-id="21a8c-1470">mastercard</span></span> 
- <span data-ttu-id="21a8c-1471">MasterCards</span><span class="sxs-lookup"><span data-stu-id="21a8c-1471">mastercards</span></span> 
- <span data-ttu-id="21a8c-1472">MC</span><span class="sxs-lookup"><span data-stu-id="21a8c-1472">mc</span></span> 
- <span data-ttu-id="21a8c-1473">mister cash</span><span class="sxs-lookup"><span data-stu-id="21a8c-1473">mister cash</span></span> 
- <span data-ttu-id="21a8c-1474">n carta</span><span class="sxs-lookup"><span data-stu-id="21a8c-1474">n carta</span></span> 
- <span data-ttu-id="21a8c-1475">carta</span><span class="sxs-lookup"><span data-stu-id="21a8c-1475">carta</span></span> 
- <span data-ttu-id="21a8c-1476">no de tarjeta</span><span class="sxs-lookup"><span data-stu-id="21a8c-1476">no de tarjeta</span></span> 
- <span data-ttu-id="21a8c-1477">no do cartao</span><span class="sxs-lookup"><span data-stu-id="21a8c-1477">no do cartao</span></span> 
- <span data-ttu-id="21a8c-1478">no do cartão</span><span class="sxs-lookup"><span data-stu-id="21a8c-1478">no do cartão</span></span> 
- <span data-ttu-id="21a8c-1479">Não.</span><span class="sxs-lookup"><span data-stu-id="21a8c-1479">no.</span></span> <span data-ttu-id="21a8c-1480">de tarjeta</span><span class="sxs-lookup"><span data-stu-id="21a8c-1480">de tarjeta</span></span> 
- <span data-ttu-id="21a8c-1481">Não.</span><span class="sxs-lookup"><span data-stu-id="21a8c-1481">no.</span></span> <span data-ttu-id="21a8c-1482">do cartao</span><span class="sxs-lookup"><span data-stu-id="21a8c-1482">do cartao</span></span> 
- <span data-ttu-id="21a8c-1483">Não.</span><span class="sxs-lookup"><span data-stu-id="21a8c-1483">no.</span></span> <span data-ttu-id="21a8c-1484">do cartão</span><span class="sxs-lookup"><span data-stu-id="21a8c-1484">do cartão</span></span> 
- <span data-ttu-id="21a8c-1485">nr carta</span><span class="sxs-lookup"><span data-stu-id="21a8c-1485">nr carta</span></span> 
- <span data-ttu-id="21a8c-1486">Nr.</span><span class="sxs-lookup"><span data-stu-id="21a8c-1486">nr.</span></span> <span data-ttu-id="21a8c-1487">carta</span><span class="sxs-lookup"><span data-stu-id="21a8c-1487">carta</span></span> 
- <span data-ttu-id="21a8c-1488">numeri di scheda</span><span class="sxs-lookup"><span data-stu-id="21a8c-1488">numeri di scheda</span></span> 
- <span data-ttu-id="21a8c-1489">numero carta</span><span class="sxs-lookup"><span data-stu-id="21a8c-1489">numero carta</span></span> 
- <span data-ttu-id="21a8c-1490">numero de cartao</span><span class="sxs-lookup"><span data-stu-id="21a8c-1490">numero de cartao</span></span> 
- <span data-ttu-id="21a8c-1491">numero de carte</span><span class="sxs-lookup"><span data-stu-id="21a8c-1491">numero de carte</span></span> 
- <span data-ttu-id="21a8c-1492">numero de cartão</span><span class="sxs-lookup"><span data-stu-id="21a8c-1492">numero de cartão</span></span> 
- <span data-ttu-id="21a8c-1493">numero de tarjeta</span><span class="sxs-lookup"><span data-stu-id="21a8c-1493">numero de tarjeta</span></span>
- <span data-ttu-id="21a8c-1494">numero della carta</span><span class="sxs-lookup"><span data-stu-id="21a8c-1494">numero della carta</span></span> 
- <span data-ttu-id="21a8c-1495">numero di carta</span><span class="sxs-lookup"><span data-stu-id="21a8c-1495">numero di carta</span></span> 
- <span data-ttu-id="21a8c-1496">numero di scheda</span><span class="sxs-lookup"><span data-stu-id="21a8c-1496">numero di scheda</span></span> 
- <span data-ttu-id="21a8c-1497">numero do cartao</span><span class="sxs-lookup"><span data-stu-id="21a8c-1497">numero do cartao</span></span> 
- <span data-ttu-id="21a8c-1498">numero do cartão</span><span class="sxs-lookup"><span data-stu-id="21a8c-1498">numero do cartão</span></span> 
- <span data-ttu-id="21a8c-1499">numéro de carte</span><span class="sxs-lookup"><span data-stu-id="21a8c-1499">numéro de carte</span></span> 
- <span data-ttu-id="21a8c-1500">nº carta</span><span class="sxs-lookup"><span data-stu-id="21a8c-1500">nº carta</span></span> 
- <span data-ttu-id="21a8c-1501">nº de carte</span><span class="sxs-lookup"><span data-stu-id="21a8c-1501">nº de carte</span></span> 
- <span data-ttu-id="21a8c-1502">nº de la carte</span><span class="sxs-lookup"><span data-stu-id="21a8c-1502">nº de la carte</span></span> 
- <span data-ttu-id="21a8c-1503">nº de tarjeta</span><span class="sxs-lookup"><span data-stu-id="21a8c-1503">nº de tarjeta</span></span> 
- <span data-ttu-id="21a8c-1504">nº do cartao</span><span class="sxs-lookup"><span data-stu-id="21a8c-1504">nº do cartao</span></span> 
- <span data-ttu-id="21a8c-1505">nº do cartão</span><span class="sxs-lookup"><span data-stu-id="21a8c-1505">nº do cartão</span></span> 
- <span data-ttu-id="21a8c-1506">n º.</span><span class="sxs-lookup"><span data-stu-id="21a8c-1506">nº.</span></span> <span data-ttu-id="21a8c-1507">do cartão</span><span class="sxs-lookup"><span data-stu-id="21a8c-1507">do cartão</span></span> 
- <span data-ttu-id="21a8c-1508">número de cartao</span><span class="sxs-lookup"><span data-stu-id="21a8c-1508">número de cartao</span></span> 
- <span data-ttu-id="21a8c-1509">número de cartão</span><span class="sxs-lookup"><span data-stu-id="21a8c-1509">número de cartão</span></span> 
- <span data-ttu-id="21a8c-1510">número de tarjeta</span><span class="sxs-lookup"><span data-stu-id="21a8c-1510">número de tarjeta</span></span> 
- <span data-ttu-id="21a8c-1511">número do cartao</span><span class="sxs-lookup"><span data-stu-id="21a8c-1511">número do cartao</span></span> 
- <span data-ttu-id="21a8c-1512">scheda dell'assegno</span><span class="sxs-lookup"><span data-stu-id="21a8c-1512">scheda dell'assegno</span></span> 
- <span data-ttu-id="21a8c-1513">scheda dell'atmosfera</span><span class="sxs-lookup"><span data-stu-id="21a8c-1513">scheda dell'atmosfera</span></span> 
- <span data-ttu-id="21a8c-1514">scheda dell'atmosfera</span><span class="sxs-lookup"><span data-stu-id="21a8c-1514">scheda dell'atmosfera</span></span> 
- <span data-ttu-id="21a8c-1515">scheda della banca</span><span class="sxs-lookup"><span data-stu-id="21a8c-1515">scheda della banca</span></span> 
- <span data-ttu-id="21a8c-1516">scheda di controllo</span><span class="sxs-lookup"><span data-stu-id="21a8c-1516">scheda di controllo</span></span> 
- <span data-ttu-id="21a8c-1517">scheda di debito</span><span class="sxs-lookup"><span data-stu-id="21a8c-1517">scheda di debito</span></span> 
- <span data-ttu-id="21a8c-1518">scheda matrice</span><span class="sxs-lookup"><span data-stu-id="21a8c-1518">scheda matrice</span></span> 
- <span data-ttu-id="21a8c-1519">schede dell'atmosfera</span><span class="sxs-lookup"><span data-stu-id="21a8c-1519">schede dell'atmosfera</span></span> 
- <span data-ttu-id="21a8c-1520">schede di controllo</span><span class="sxs-lookup"><span data-stu-id="21a8c-1520">schede di controllo</span></span> 
- <span data-ttu-id="21a8c-1521">schede di debito</span><span class="sxs-lookup"><span data-stu-id="21a8c-1521">schede di debito</span></span> 
- <span data-ttu-id="21a8c-1522">schede matrici</span><span class="sxs-lookup"><span data-stu-id="21a8c-1522">schede matrici</span></span> 
- <span data-ttu-id="21a8c-1523">scoprono la scheda</span><span class="sxs-lookup"><span data-stu-id="21a8c-1523">scoprono la scheda</span></span> 
- <span data-ttu-id="21a8c-1524">scoprono le schede</span><span class="sxs-lookup"><span data-stu-id="21a8c-1524">scoprono le schede</span></span> 
- <span data-ttu-id="21a8c-1525">individual</span><span class="sxs-lookup"><span data-stu-id="21a8c-1525">solo</span></span> 
- <span data-ttu-id="21a8c-1526">supporti di scheda</span><span class="sxs-lookup"><span data-stu-id="21a8c-1526">supporti di scheda</span></span> 
- <span data-ttu-id="21a8c-1527">supporto di scheda</span><span class="sxs-lookup"><span data-stu-id="21a8c-1527">supporto di scheda</span></span> 
- <span data-ttu-id="21a8c-1528">Vá</span><span class="sxs-lookup"><span data-stu-id="21a8c-1528">switch</span></span> 
- <span data-ttu-id="21a8c-1529">tarjeta atm</span><span class="sxs-lookup"><span data-stu-id="21a8c-1529">tarjeta atm</span></span> 
- <span data-ttu-id="21a8c-1530">tarjeta credito</span><span class="sxs-lookup"><span data-stu-id="21a8c-1530">tarjeta credito</span></span> 
- <span data-ttu-id="21a8c-1531">tarjeta de atm</span><span class="sxs-lookup"><span data-stu-id="21a8c-1531">tarjeta de atm</span></span> 
- <span data-ttu-id="21a8c-1532">tarjeta de credito</span><span class="sxs-lookup"><span data-stu-id="21a8c-1532">tarjeta de credito</span></span> 
- <span data-ttu-id="21a8c-1533">tarjeta de debito</span><span class="sxs-lookup"><span data-stu-id="21a8c-1533">tarjeta de debito</span></span> 
- <span data-ttu-id="21a8c-1534">tarjeta debito</span><span class="sxs-lookup"><span data-stu-id="21a8c-1534">tarjeta debito</span></span> 
- <span data-ttu-id="21a8c-1535">tarjeta no</span><span class="sxs-lookup"><span data-stu-id="21a8c-1535">tarjeta no</span></span>
- <span data-ttu-id="21a8c-1536">tarjetahabiente</span><span class="sxs-lookup"><span data-stu-id="21a8c-1536">tarjetahabiente</span></span> 
- <span data-ttu-id="21a8c-1537">tipo della scheda</span><span class="sxs-lookup"><span data-stu-id="21a8c-1537">tipo della scheda</span></span> 
- <span data-ttu-id="21a8c-1538">ufficio giapponese della</span><span class="sxs-lookup"><span data-stu-id="21a8c-1538">ufficio giapponese della</span></span> 
- <span data-ttu-id="21a8c-1539">scheda</span><span class="sxs-lookup"><span data-stu-id="21a8c-1539">scheda</span></span> 
- <span data-ttu-id="21a8c-1540">v pay</span><span class="sxs-lookup"><span data-stu-id="21a8c-1540">v pay</span></span> 
- <span data-ttu-id="21a8c-1541">v-Pay</span><span class="sxs-lookup"><span data-stu-id="21a8c-1541">v-pay</span></span> 
- <span data-ttu-id="21a8c-1542">cartões</span><span class="sxs-lookup"><span data-stu-id="21a8c-1542">visa</span></span> 
- <span data-ttu-id="21a8c-1543">visa plus</span><span class="sxs-lookup"><span data-stu-id="21a8c-1543">visa plus</span></span> 
- <span data-ttu-id="21a8c-1544">visa electron</span><span class="sxs-lookup"><span data-stu-id="21a8c-1544">visa electron</span></span> 
- <span data-ttu-id="21a8c-1545">previsto</span><span class="sxs-lookup"><span data-stu-id="21a8c-1545">visto</span></span> 
- <span data-ttu-id="21a8c-1546">visum</span><span class="sxs-lookup"><span data-stu-id="21a8c-1546">visum</span></span> 
- <span data-ttu-id="21a8c-1547">vpay</span><span class="sxs-lookup"><span data-stu-id="21a8c-1547">vpay</span></span>   

#### <a name="keywordcardsecuritytermsdict"></a><span data-ttu-id="21a8c-1548">Keyword_card_security_terms_dict</span><span class="sxs-lookup"><span data-stu-id="21a8c-1548">Keyword_card_security_terms_dict</span></span>

- <span data-ttu-id="21a8c-1549">card identification number</span><span class="sxs-lookup"><span data-stu-id="21a8c-1549">card identification number</span></span>
- <span data-ttu-id="21a8c-1550">card verification</span><span class="sxs-lookup"><span data-stu-id="21a8c-1550">card verification</span></span> 
- <span data-ttu-id="21a8c-1551">cardi la verifica</span><span class="sxs-lookup"><span data-stu-id="21a8c-1551">cardi la verifica</span></span> 
- <span data-ttu-id="21a8c-1552">CID</span><span class="sxs-lookup"><span data-stu-id="21a8c-1552">cid</span></span> 
- <span data-ttu-id="21a8c-1553">cod seg</span><span class="sxs-lookup"><span data-stu-id="21a8c-1553">cod seg</span></span> 
- <span data-ttu-id="21a8c-1554">cod seguranca</span><span class="sxs-lookup"><span data-stu-id="21a8c-1554">cod seguranca</span></span> 
- <span data-ttu-id="21a8c-1555">cod segurança</span><span class="sxs-lookup"><span data-stu-id="21a8c-1555">cod segurança</span></span> 
- <span data-ttu-id="21a8c-1556">cod sicurezza</span><span class="sxs-lookup"><span data-stu-id="21a8c-1556">cod sicurezza</span></span> 
- <span data-ttu-id="21a8c-1557">COD.</span><span class="sxs-lookup"><span data-stu-id="21a8c-1557">cod.</span></span> <span data-ttu-id="21a8c-1558">seg</span><span class="sxs-lookup"><span data-stu-id="21a8c-1558">seg</span></span> 
- <span data-ttu-id="21a8c-1559">COD.</span><span class="sxs-lookup"><span data-stu-id="21a8c-1559">cod.</span></span> <span data-ttu-id="21a8c-1560">seguranca</span><span class="sxs-lookup"><span data-stu-id="21a8c-1560">seguranca</span></span> 
- <span data-ttu-id="21a8c-1561">COD.</span><span class="sxs-lookup"><span data-stu-id="21a8c-1561">cod.</span></span> <span data-ttu-id="21a8c-1562">segurança</span><span class="sxs-lookup"><span data-stu-id="21a8c-1562">segurança</span></span> 
- <span data-ttu-id="21a8c-1563">COD.</span><span class="sxs-lookup"><span data-stu-id="21a8c-1563">cod.</span></span> <span data-ttu-id="21a8c-1564">sicurezza</span><span class="sxs-lookup"><span data-stu-id="21a8c-1564">sicurezza</span></span> 
- <span data-ttu-id="21a8c-1565">codice di sicurezza</span><span class="sxs-lookup"><span data-stu-id="21a8c-1565">codice di sicurezza</span></span> 
- <span data-ttu-id="21a8c-1566">codice di verifica</span><span class="sxs-lookup"><span data-stu-id="21a8c-1566">codice di verifica</span></span> 
- <span data-ttu-id="21a8c-1567">codigo</span><span class="sxs-lookup"><span data-stu-id="21a8c-1567">codigo</span></span> 
- <span data-ttu-id="21a8c-1568">codigo de seguranca</span><span class="sxs-lookup"><span data-stu-id="21a8c-1568">codigo de seguranca</span></span> 
- <span data-ttu-id="21a8c-1569">codigo de segurança</span><span class="sxs-lookup"><span data-stu-id="21a8c-1569">codigo de segurança</span></span> 
- <span data-ttu-id="21a8c-1570">crittogramma</span><span class="sxs-lookup"><span data-stu-id="21a8c-1570">crittogramma</span></span> 
- <span data-ttu-id="21a8c-1571">cryptogram</span><span class="sxs-lookup"><span data-stu-id="21a8c-1571">cryptogram</span></span> 
- <span data-ttu-id="21a8c-1572">cryptogramme</span><span class="sxs-lookup"><span data-stu-id="21a8c-1572">cryptogramme</span></span> 
- <span data-ttu-id="21a8c-1573">CV2</span><span class="sxs-lookup"><span data-stu-id="21a8c-1573">cv2</span></span> 
- <span data-ttu-id="21a8c-1574">CVC</span><span class="sxs-lookup"><span data-stu-id="21a8c-1574">cvc</span></span> 
- <span data-ttu-id="21a8c-1575">CVC2</span><span class="sxs-lookup"><span data-stu-id="21a8c-1575">cvc2</span></span> 
- <span data-ttu-id="21a8c-1576">CVN</span><span class="sxs-lookup"><span data-stu-id="21a8c-1576">cvn</span></span> 
- <span data-ttu-id="21a8c-1577">CVV</span><span class="sxs-lookup"><span data-stu-id="21a8c-1577">cvv</span></span> 
- <span data-ttu-id="21a8c-1578">CVV2</span><span class="sxs-lookup"><span data-stu-id="21a8c-1578">cvv2</span></span> 
- <span data-ttu-id="21a8c-1579">cód seguranca</span><span class="sxs-lookup"><span data-stu-id="21a8c-1579">cód seguranca</span></span> 
- <span data-ttu-id="21a8c-1580">cód segurança</span><span class="sxs-lookup"><span data-stu-id="21a8c-1580">cód segurança</span></span> 
- <span data-ttu-id="21a8c-1581">Cód.</span><span class="sxs-lookup"><span data-stu-id="21a8c-1581">cód.</span></span> <span data-ttu-id="21a8c-1582">seguranca</span><span class="sxs-lookup"><span data-stu-id="21a8c-1582">seguranca</span></span> 
- <span data-ttu-id="21a8c-1583">Cód.</span><span class="sxs-lookup"><span data-stu-id="21a8c-1583">cód.</span></span> <span data-ttu-id="21a8c-1584">segurança</span><span class="sxs-lookup"><span data-stu-id="21a8c-1584">segurança</span></span> 
- <span data-ttu-id="21a8c-1585">CFOP</span><span class="sxs-lookup"><span data-stu-id="21a8c-1585">código</span></span> 
- <span data-ttu-id="21a8c-1586">código de seguranca</span><span class="sxs-lookup"><span data-stu-id="21a8c-1586">código de seguranca</span></span> 
- <span data-ttu-id="21a8c-1587">código de segurança</span><span class="sxs-lookup"><span data-stu-id="21a8c-1587">código de segurança</span></span> 
- <span data-ttu-id="21a8c-1588">de kaart controle</span><span class="sxs-lookup"><span data-stu-id="21a8c-1588">de kaart controle</span></span> 
- <span data-ttu-id="21a8c-1589">geeft nr uit</span><span class="sxs-lookup"><span data-stu-id="21a8c-1589">geeft nr uit</span></span> 
- <span data-ttu-id="21a8c-1590">issue no</span><span class="sxs-lookup"><span data-stu-id="21a8c-1590">issue no</span></span> 
- <span data-ttu-id="21a8c-1591">issue number</span><span class="sxs-lookup"><span data-stu-id="21a8c-1591">issue number</span></span> 
- <span data-ttu-id="21a8c-1592">kaartidentificatienummer</span><span class="sxs-lookup"><span data-stu-id="21a8c-1592">kaartidentificatienummer</span></span> 
- <span data-ttu-id="21a8c-1593">kreditkartenprufnummer</span><span class="sxs-lookup"><span data-stu-id="21a8c-1593">kreditkartenprufnummer</span></span> 
- <span data-ttu-id="21a8c-1594">kreditkartenprüfnummer</span><span class="sxs-lookup"><span data-stu-id="21a8c-1594">kreditkartenprüfnummer</span></span> 
- <span data-ttu-id="21a8c-1595">kwestieaantal</span><span class="sxs-lookup"><span data-stu-id="21a8c-1595">kwestieaantal</span></span> 
- <span data-ttu-id="21a8c-1596">Não.</span><span class="sxs-lookup"><span data-stu-id="21a8c-1596">no.</span></span> <span data-ttu-id="21a8c-1597">dell'edizione</span><span class="sxs-lookup"><span data-stu-id="21a8c-1597">dell'edizione</span></span> 
- <span data-ttu-id="21a8c-1598">Não.</span><span class="sxs-lookup"><span data-stu-id="21a8c-1598">no.</span></span> <span data-ttu-id="21a8c-1599">di sicurezza</span><span class="sxs-lookup"><span data-stu-id="21a8c-1599">di sicurezza</span></span> 
- <span data-ttu-id="21a8c-1600">numero de securite</span><span class="sxs-lookup"><span data-stu-id="21a8c-1600">numero de securite</span></span> 
- <span data-ttu-id="21a8c-1601">numero de verificacao</span><span class="sxs-lookup"><span data-stu-id="21a8c-1601">numero de verificacao</span></span> 
- <span data-ttu-id="21a8c-1602">numero dell'edizione</span><span class="sxs-lookup"><span data-stu-id="21a8c-1602">numero dell'edizione</span></span> 
- <span data-ttu-id="21a8c-1603">numero di identificazione della</span><span class="sxs-lookup"><span data-stu-id="21a8c-1603">numero di identificazione della</span></span> 
- <span data-ttu-id="21a8c-1604">scheda</span><span class="sxs-lookup"><span data-stu-id="21a8c-1604">scheda</span></span> 
- <span data-ttu-id="21a8c-1605">numero di sicurezza</span><span class="sxs-lookup"><span data-stu-id="21a8c-1605">numero di sicurezza</span></span> 
- <span data-ttu-id="21a8c-1606">numero van veiligheid</span><span class="sxs-lookup"><span data-stu-id="21a8c-1606">numero van veiligheid</span></span> 
- <span data-ttu-id="21a8c-1607">numéro de sécurité</span><span class="sxs-lookup"><span data-stu-id="21a8c-1607">numéro de sécurité</span></span> 
- <span data-ttu-id="21a8c-1608">nº autorizzazione</span><span class="sxs-lookup"><span data-stu-id="21a8c-1608">nº autorizzazione</span></span> 
- <span data-ttu-id="21a8c-1609">número de verificação</span><span class="sxs-lookup"><span data-stu-id="21a8c-1609">número de verificação</span></span> 
- <span data-ttu-id="21a8c-1610">perno il blocco</span><span class="sxs-lookup"><span data-stu-id="21a8c-1610">perno il blocco</span></span> 
- <span data-ttu-id="21a8c-1611">pin block</span><span class="sxs-lookup"><span data-stu-id="21a8c-1611">pin block</span></span> 
- <span data-ttu-id="21a8c-1612">prufziffer</span><span class="sxs-lookup"><span data-stu-id="21a8c-1612">prufziffer</span></span> 
- <span data-ttu-id="21a8c-1613">prüfziffer</span><span class="sxs-lookup"><span data-stu-id="21a8c-1613">prüfziffer</span></span> 
- <span data-ttu-id="21a8c-1614">security code</span><span class="sxs-lookup"><span data-stu-id="21a8c-1614">security code</span></span> 
- <span data-ttu-id="21a8c-1615">security no</span><span class="sxs-lookup"><span data-stu-id="21a8c-1615">security no</span></span> 
- <span data-ttu-id="21a8c-1616">security number</span><span class="sxs-lookup"><span data-stu-id="21a8c-1616">security number</span></span> 
- <span data-ttu-id="21a8c-1617">sicherheits kode</span><span class="sxs-lookup"><span data-stu-id="21a8c-1617">sicherheits kode</span></span> 
- <span data-ttu-id="21a8c-1618">sicherheitscode</span><span class="sxs-lookup"><span data-stu-id="21a8c-1618">sicherheitscode</span></span> 
- <span data-ttu-id="21a8c-1619">sicherheitsnummer</span><span class="sxs-lookup"><span data-stu-id="21a8c-1619">sicherheitsnummer</span></span> 
- <span data-ttu-id="21a8c-1620">speldblok</span><span class="sxs-lookup"><span data-stu-id="21a8c-1620">speldblok</span></span> 
- <span data-ttu-id="21a8c-1621">veiligheid nr</span><span class="sxs-lookup"><span data-stu-id="21a8c-1621">veiligheid nr</span></span> 
- <span data-ttu-id="21a8c-1622">veiligheidsaantal</span><span class="sxs-lookup"><span data-stu-id="21a8c-1622">veiligheidsaantal</span></span> 
- <span data-ttu-id="21a8c-1623">veiligheidscode</span><span class="sxs-lookup"><span data-stu-id="21a8c-1623">veiligheidscode</span></span> 
- <span data-ttu-id="21a8c-1624">veiligheidsnummer</span><span class="sxs-lookup"><span data-stu-id="21a8c-1624">veiligheidsnummer</span></span> 
- <span data-ttu-id="21a8c-1625">verfalldatum</span><span class="sxs-lookup"><span data-stu-id="21a8c-1625">verfalldatum</span></span> 

#### <a name="keywordcardexpirationtermsdict"></a><span data-ttu-id="21a8c-1626">Keyword_card_expiration_terms_dict</span><span class="sxs-lookup"><span data-stu-id="21a8c-1626">Keyword_card_expiration_terms_dict</span></span>

- <span data-ttu-id="21a8c-1627">ablauf</span><span class="sxs-lookup"><span data-stu-id="21a8c-1627">ablauf</span></span> 
- <span data-ttu-id="21a8c-1628">data de expiracao</span><span class="sxs-lookup"><span data-stu-id="21a8c-1628">data de expiracao</span></span> 
- <span data-ttu-id="21a8c-1629">data de expiração</span><span class="sxs-lookup"><span data-stu-id="21a8c-1629">data de expiração</span></span> 
- <span data-ttu-id="21a8c-1630">data del exp</span><span class="sxs-lookup"><span data-stu-id="21a8c-1630">data del exp</span></span> 
- <span data-ttu-id="21a8c-1631">data di exp</span><span class="sxs-lookup"><span data-stu-id="21a8c-1631">data di exp</span></span> 
- <span data-ttu-id="21a8c-1632">data di scadenza</span><span class="sxs-lookup"><span data-stu-id="21a8c-1632">data di scadenza</span></span> 
- <span data-ttu-id="21a8c-1633">data em que expira</span><span class="sxs-lookup"><span data-stu-id="21a8c-1633">data em que expira</span></span> 
- <span data-ttu-id="21a8c-1634">data scad</span><span class="sxs-lookup"><span data-stu-id="21a8c-1634">data scad</span></span> 
- <span data-ttu-id="21a8c-1635">data scadenza</span><span class="sxs-lookup"><span data-stu-id="21a8c-1635">data scadenza</span></span> 
- <span data-ttu-id="21a8c-1636">date de validité</span><span class="sxs-lookup"><span data-stu-id="21a8c-1636">date de validité</span></span> 
- <span data-ttu-id="21a8c-1637">datum afloop</span><span class="sxs-lookup"><span data-stu-id="21a8c-1637">datum afloop</span></span> 
- <span data-ttu-id="21a8c-1638">datum van exp</span><span class="sxs-lookup"><span data-stu-id="21a8c-1638">datum van exp</span></span> 
- <span data-ttu-id="21a8c-1639">de afloop</span><span class="sxs-lookup"><span data-stu-id="21a8c-1639">de afloop</span></span> 
- <span data-ttu-id="21a8c-1640">espira</span><span class="sxs-lookup"><span data-stu-id="21a8c-1640">espira</span></span> 
- <span data-ttu-id="21a8c-1641">espira</span><span class="sxs-lookup"><span data-stu-id="21a8c-1641">espira</span></span> 
- <span data-ttu-id="21a8c-1642">exp date</span><span class="sxs-lookup"><span data-stu-id="21a8c-1642">exp date</span></span> 
- <span data-ttu-id="21a8c-1643">exp datum</span><span class="sxs-lookup"><span data-stu-id="21a8c-1643">exp datum</span></span> 
- <span data-ttu-id="21a8c-1644">validade</span><span class="sxs-lookup"><span data-stu-id="21a8c-1644">expiration</span></span> 
- <span data-ttu-id="21a8c-1645">expirar</span><span class="sxs-lookup"><span data-stu-id="21a8c-1645">expire</span></span> 
- <span data-ttu-id="21a8c-1646">expira</span><span class="sxs-lookup"><span data-stu-id="21a8c-1646">expires</span></span> 
- <span data-ttu-id="21a8c-1647">expiração</span><span class="sxs-lookup"><span data-stu-id="21a8c-1647">expiry</span></span> 
- <span data-ttu-id="21a8c-1648">fecha de expiracion</span><span class="sxs-lookup"><span data-stu-id="21a8c-1648">fecha de expiracion</span></span> 
- <span data-ttu-id="21a8c-1649">fecha de venc</span><span class="sxs-lookup"><span data-stu-id="21a8c-1649">fecha de venc</span></span> 
- <span data-ttu-id="21a8c-1650">gultig bis</span><span class="sxs-lookup"><span data-stu-id="21a8c-1650">gultig bis</span></span> 
- <span data-ttu-id="21a8c-1651">gultigkeitsdatum</span><span class="sxs-lookup"><span data-stu-id="21a8c-1651">gultigkeitsdatum</span></span> 
- <span data-ttu-id="21a8c-1652">gültig bis</span><span class="sxs-lookup"><span data-stu-id="21a8c-1652">gültig bis</span></span> 
- <span data-ttu-id="21a8c-1653">gültigkeitsdatum</span><span class="sxs-lookup"><span data-stu-id="21a8c-1653">gültigkeitsdatum</span></span> 
- <span data-ttu-id="21a8c-1654">la scadenza</span><span class="sxs-lookup"><span data-stu-id="21a8c-1654">la scadenza</span></span> 
- <span data-ttu-id="21a8c-1655">scadenza</span><span class="sxs-lookup"><span data-stu-id="21a8c-1655">scadenza</span></span> 
- <span data-ttu-id="21a8c-1656">valable</span><span class="sxs-lookup"><span data-stu-id="21a8c-1656">valable</span></span> 
- <span data-ttu-id="21a8c-1657">validade</span><span class="sxs-lookup"><span data-stu-id="21a8c-1657">validade</span></span> 
- <span data-ttu-id="21a8c-1658">valido hasta</span><span class="sxs-lookup"><span data-stu-id="21a8c-1658">valido hasta</span></span> 
- <span data-ttu-id="21a8c-1659">coragem</span><span class="sxs-lookup"><span data-stu-id="21a8c-1659">valor</span></span> 
- <span data-ttu-id="21a8c-1660">venc</span><span class="sxs-lookup"><span data-stu-id="21a8c-1660">venc</span></span> 
- <span data-ttu-id="21a8c-1661">vencimento</span><span class="sxs-lookup"><span data-stu-id="21a8c-1661">vencimento</span></span> 
- <span data-ttu-id="21a8c-1662">vencimiento</span><span class="sxs-lookup"><span data-stu-id="21a8c-1662">vencimiento</span></span> 
- <span data-ttu-id="21a8c-1663">verloopt</span><span class="sxs-lookup"><span data-stu-id="21a8c-1663">verloopt</span></span> 
- <span data-ttu-id="21a8c-1664">vervaldag</span><span class="sxs-lookup"><span data-stu-id="21a8c-1664">vervaldag</span></span> 
- <span data-ttu-id="21a8c-1665">vervaldatum</span><span class="sxs-lookup"><span data-stu-id="21a8c-1665">vervaldatum</span></span> 
- <span data-ttu-id="21a8c-1666">vto</span><span class="sxs-lookup"><span data-stu-id="21a8c-1666">vto</span></span> 
- <span data-ttu-id="21a8c-1667">válido hasta</span><span class="sxs-lookup"><span data-stu-id="21a8c-1667">válido hasta</span></span> 
   
## <a name="eu-drivers-license-number"></a><span data-ttu-id="21a8c-1668">Número da carteira de motorista da UE</span><span class="sxs-lookup"><span data-stu-id="21a8c-1668">EU Driver's License Number</span></span>

<span data-ttu-id="21a8c-1669">Para saber mais, confira o [tipo de informação confidencial do número da carteira de motorista da UE](eu-driver-s-license-number.md).</span><span class="sxs-lookup"><span data-stu-id="21a8c-1669">To learn more, see [EU Driver's License Number sensitive information type](eu-driver-s-license-number.md).</span></span>
  
## <a name="eu-national-identification-number"></a><span data-ttu-id="21a8c-1670">Número de identificação nacional da UE</span><span class="sxs-lookup"><span data-stu-id="21a8c-1670">EU National Identification Number</span></span>

<span data-ttu-id="21a8c-1671">Para saber mais, confira [tipo de informação confidencial do número de identificação nacional da UE](eu-national-identification-number.md).</span><span class="sxs-lookup"><span data-stu-id="21a8c-1671">To learn more, see [EU National Identification Number sensitive information type](eu-national-identification-number.md).</span></span>
  
## <a name="eu-passport-number"></a><span data-ttu-id="21a8c-1672">Número do Passport da UE</span><span class="sxs-lookup"><span data-stu-id="21a8c-1672">EU Passport Number</span></span>

<span data-ttu-id="21a8c-1673">Para saber mais, veja [tipo de informações confidenciais do número do Passport da UE](eu-passport-number.md).</span><span class="sxs-lookup"><span data-stu-id="21a8c-1673">To learn more, see [EU Passport Number sensitive information type](eu-passport-number.md).</span></span>
  
## <a name="eu-social-security-number-or-equivalent-id"></a><span data-ttu-id="21a8c-1674">Número de seguro social da UE ou ID equivalente</span><span class="sxs-lookup"><span data-stu-id="21a8c-1674">EU Social Security Number or Equivalent ID</span></span>

<span data-ttu-id="21a8c-1675">Para saber mais, confira [número de seguridade social da UE ou tipo de informação confidencial de ID equivalente](eu-social-security-number-or-equivalent-id.md).</span><span class="sxs-lookup"><span data-stu-id="21a8c-1675">To learn more, see [EU Social Security Number or Equivalent ID sensitive information type](eu-social-security-number-or-equivalent-id.md).</span></span>
  
## <a name="eu-tax-identification-number"></a><span data-ttu-id="21a8c-1676">Número de identificação do imposto da UE</span><span class="sxs-lookup"><span data-stu-id="21a8c-1676">EU Tax Identification Number</span></span>

<span data-ttu-id="21a8c-1677">Para saber mais, confira [número de identificação de imposto da UE tipo de informação confidencial](eu-tax-identification-number.md).</span><span class="sxs-lookup"><span data-stu-id="21a8c-1677">To learn more, see [EU Tax Identification Number sensitive information type](eu-tax-identification-number.md).</span></span>
  
## <a name="finland-national-id"></a><span data-ttu-id="21a8c-1678">ID nacional da Finlândia</span><span class="sxs-lookup"><span data-stu-id="21a8c-1678">Finland National ID</span></span>

### <a name="format"></a><span data-ttu-id="21a8c-1679">Format</span><span class="sxs-lookup"><span data-stu-id="21a8c-1679">Format</span></span>

<span data-ttu-id="21a8c-1680">Seis dígitos mais um caractere indicando um século mais três dígitos mais um dígito de verificação</span><span class="sxs-lookup"><span data-stu-id="21a8c-1680">Six digits plus a character indicating a century plus three digits plus a check digit</span></span>

### <a name="pattern"></a><span data-ttu-id="21a8c-1681">Padrão</span><span class="sxs-lookup"><span data-stu-id="21a8c-1681">Pattern</span></span>

<span data-ttu-id="21a8c-1682">O padrão deve incluir todos os seguintes itens:</span><span class="sxs-lookup"><span data-stu-id="21a8c-1682">Pattern must include all of the following:</span></span>
- <span data-ttu-id="21a8c-1683">Seis dígitos no formato DDMMAA que é uma data de nascimento</span><span class="sxs-lookup"><span data-stu-id="21a8c-1683">Six digits in the format format DDMMYY which are a date of birth</span></span> 
- <span data-ttu-id="21a8c-1684">Marcador do século (qualquer '-', '+' ou 'a')</span><span class="sxs-lookup"><span data-stu-id="21a8c-1684">Century marker (either '-', '+' or 'a')</span></span> 
- <span data-ttu-id="21a8c-1685">Número de identificação pessoal de três dígitos</span><span class="sxs-lookup"><span data-stu-id="21a8c-1685">Three-digit personal identification number</span></span> 
- <span data-ttu-id="21a8c-1686">Um dígito ou letra (não diferencia maiúscula de minúscula), que é um dígito de verificação</span><span class="sxs-lookup"><span data-stu-id="21a8c-1686">A digit or letter (case insensitive) which is a check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="21a8c-1687">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="21a8c-1687">Checksum</span></span>

<span data-ttu-id="21a8c-1688">Sim</span><span class="sxs-lookup"><span data-stu-id="21a8c-1688">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="21a8c-1689">Definição</span><span class="sxs-lookup"><span data-stu-id="21a8c-1689">Definition</span></span>

<span data-ttu-id="21a8c-1690">Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="21a8c-1690">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="21a8c-1691">A função Func_finnish_national_id localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="21a8c-1691">The function Func_finnish_national_id finds content that matches the pattern.</span></span>
- <span data-ttu-id="21a8c-1692">Uma palavra-chave de Keyword_finnish_national_id for encontrada.</span><span class="sxs-lookup"><span data-stu-id="21a8c-1692">A keyword from Keyword_finnish_national_id is found.</span></span>
- <span data-ttu-id="21a8c-1693">A soma de verificação passa.</span><span class="sxs-lookup"><span data-stu-id="21a8c-1693">The checksum passes.</span></span>

```
<!-- Finnish National ID-->
<Entity id="338FD995-4CB5-4F87-AD35-79BD1DD926C1" patternsProximity="300" recommendedConfidence="85">
  <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_finnish_national_id" />
          <Match idRef="Keyword_finnish_national_id" />
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="21a8c-1694">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="21a8c-1694">Keywords</span></span>

- <span data-ttu-id="21a8c-1695">Keyword_finnish_national_id</span><span class="sxs-lookup"><span data-stu-id="21a8c-1695">Keyword_finnish_national_id</span></span>
- <span data-ttu-id="21a8c-1696">Sosiaaliturvatunnus</span><span class="sxs-lookup"><span data-stu-id="21a8c-1696">Sosiaaliturvatunnus</span></span>
- <span data-ttu-id="21a8c-1697">SOTU Henkilötunnus HETU</span><span class="sxs-lookup"><span data-stu-id="21a8c-1697">SOTU Henkilötunnus HETU</span></span>
- <span data-ttu-id="21a8c-1698">Personbeteckning</span><span class="sxs-lookup"><span data-stu-id="21a8c-1698">Personbeteckning</span></span>
- <span data-ttu-id="21a8c-1699">Personnummer</span><span class="sxs-lookup"><span data-stu-id="21a8c-1699">Personnummer</span></span>
   
## <a name="finland-passport-number"></a><span data-ttu-id="21a8c-1700">Número de Passaporte da Finlândia</span><span class="sxs-lookup"><span data-stu-id="21a8c-1700">Finland Passport Number</span></span>

<span data-ttu-id="21a8c-1701">Combinação de formato de nove letras e dígitos combinação de padrões de nove letras e dígitos: duas letras (não diferencia maiúsculas de minúsculas) sete dígitos soma de verificação sem definição uma política de DLP é de 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de um proximidade de 300 caracteres: a expressão regular Regex_finland_passport_number localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="21a8c-1701">Format Combination of nine letters and digits Pattern Combination of nine letters and digits: Two letters (not case sensitive) Seven digits Checksum No Definition A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters: The regular expression Regex_finland_passport_number finds content that matches the pattern.</span></span>
<span data-ttu-id="21a8c-1702">Uma palavra-chave de Keyword_finland_passport_number for encontrada.</span><span class="sxs-lookup"><span data-stu-id="21a8c-1702">A keyword from Keyword_finland_passport_number is found.</span></span>
<span data-ttu-id="21a8c-1703"><!-- Finland Passport Number -->
<Entity id="d1685ac3-1d3a-40f8-8198-32ef5669c7a5" recommendedConfidence="75" patternsProximity="300"> <Pattern confidenceLevel="75"> <IdMatch idRef="Regex_finland_passport_number"/> <Match idRef="Keyword_finland_passport_number"/> </Pattern>
</Entity></span><span class="sxs-lookup"><span data-stu-id="21a8c-1703"></span></span>
<span data-ttu-id="21a8c-1704">Keyword_finland_passport_number de palavras-chave o Passport Passi</span><span class="sxs-lookup"><span data-stu-id="21a8c-1704">Keywords Keyword_finland_passport_number Passport Passi</span></span>
   
## <a name="france-drivers-license-number"></a><span data-ttu-id="21a8c-1705">Número de carteira de motorista da França</span><span class="sxs-lookup"><span data-stu-id="21a8c-1705">France Driver's License Number</span></span>

### <a name="format"></a><span data-ttu-id="21a8c-1706">Format</span><span class="sxs-lookup"><span data-stu-id="21a8c-1706">Format</span></span>

<span data-ttu-id="21a8c-1707">12 dígitos</span><span class="sxs-lookup"><span data-stu-id="21a8c-1707">12 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="21a8c-1708">Padrão</span><span class="sxs-lookup"><span data-stu-id="21a8c-1708">Pattern</span></span>

<span data-ttu-id="21a8c-1709">12 dígitos com a validação para descontar padrões similares, como números de telefone em francês</span><span class="sxs-lookup"><span data-stu-id="21a8c-1709">12 digits with validation to discount similar patterns such as French telephone numbers</span></span>

### <a name="checksum"></a><span data-ttu-id="21a8c-1710">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="21a8c-1710">Checksum</span></span>

<span data-ttu-id="21a8c-1711">Não</span><span class="sxs-lookup"><span data-stu-id="21a8c-1711">No</span></span>

### <a name="definition"></a><span data-ttu-id="21a8c-1712">Definição</span><span class="sxs-lookup"><span data-stu-id="21a8c-1712">Definition</span></span>

<span data-ttu-id="21a8c-1713">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="21a8c-1713">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="21a8c-1714">A função Func_french_drivers_license localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="21a8c-1714">The function Func_french_drivers_license finds content that matches the pattern.</span></span>
- <span data-ttu-id="21a8c-1715">Pelo menos uma das seguintes opções for verdadeira:</span><span class="sxs-lookup"><span data-stu-id="21a8c-1715">At least one of the following is true:</span></span>
- <span data-ttu-id="21a8c-1716">Uma palavra-chave de Keyword_french_drivers_license for encontrada.</span><span class="sxs-lookup"><span data-stu-id="21a8c-1716">A keyword from Keyword_french_drivers_license is found.</span></span>
- <span data-ttu-id="21a8c-1717">A função Func_eu_date encontra uma data no formato de data à direita.</span><span class="sxs-lookup"><span data-stu-id="21a8c-1717">The function Func_eu_date finds a date in the right date format.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="21a8c-1718">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="21a8c-1718">Keywords</span></span>

#### <a name="keywordfrenchdriverslicense"></a><span data-ttu-id="21a8c-1719">Keyword_french_drivers_license</span><span class="sxs-lookup"><span data-stu-id="21a8c-1719">Keyword_french_drivers_license</span></span>

- <span data-ttu-id="21a8c-1720">drivers licence</span><span class="sxs-lookup"><span data-stu-id="21a8c-1720">drivers licence</span></span>
- <span data-ttu-id="21a8c-1721">drivers license</span><span class="sxs-lookup"><span data-stu-id="21a8c-1721">drivers license</span></span>
- <span data-ttu-id="21a8c-1722">driving licence</span><span class="sxs-lookup"><span data-stu-id="21a8c-1722">driving licence</span></span>
- <span data-ttu-id="21a8c-1723">driving licence</span><span class="sxs-lookup"><span data-stu-id="21a8c-1723">driving license</span></span>
- <span data-ttu-id="21a8c-1724">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="21a8c-1724">permis de conduire</span></span>
- <span data-ttu-id="21a8c-1725">licence number</span><span class="sxs-lookup"><span data-stu-id="21a8c-1725">licence number</span></span>
- <span data-ttu-id="21a8c-1726">license number</span><span class="sxs-lookup"><span data-stu-id="21a8c-1726">license number</span></span>
- <span data-ttu-id="21a8c-1727">licence numbers</span><span class="sxs-lookup"><span data-stu-id="21a8c-1727">licence numbers</span></span>
- <span data-ttu-id="21a8c-1728">license numbers</span><span class="sxs-lookup"><span data-stu-id="21a8c-1728">license numbers</span></span>

## <a name="france-national-id-card-cni"></a><span data-ttu-id="21a8c-1729">Cartão de identificação nacional da França (CNI)</span><span class="sxs-lookup"><span data-stu-id="21a8c-1729">France National ID Card (CNI)</span></span>

### <a name="format"></a><span data-ttu-id="21a8c-1730">Format</span><span class="sxs-lookup"><span data-stu-id="21a8c-1730">Format</span></span>

<span data-ttu-id="21a8c-1731">12 dígitos</span><span class="sxs-lookup"><span data-stu-id="21a8c-1731">12 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="21a8c-1732">Padrão</span><span class="sxs-lookup"><span data-stu-id="21a8c-1732">Pattern</span></span>

<span data-ttu-id="21a8c-1733">12 dígitos</span><span class="sxs-lookup"><span data-stu-id="21a8c-1733">12 digits</span></span>

### <a name="checksum"></a><span data-ttu-id="21a8c-1734">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="21a8c-1734">Checksum</span></span>

<span data-ttu-id="21a8c-1735">Não</span><span class="sxs-lookup"><span data-stu-id="21a8c-1735">No</span></span>

### <a name="definition"></a><span data-ttu-id="21a8c-1736">Definição</span><span class="sxs-lookup"><span data-stu-id="21a8c-1736">Definition</span></span>

<span data-ttu-id="21a8c-1737">Uma política de DLP tem 65% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="21a8c-1737">A DLP policy is 65% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="21a8c-1738">A expressão regular Regex_france_cni localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="21a8c-1738">The regular expression Regex_france_cni finds content that matches the pattern.</span></span>

```
<!-- France CNI -->
<Entity id="f741ac74-1bc0-4665-b69b-f0c7f927c0c4" patternsProximity="300" recommendedConfidence="65">
  <Pattern confidenceLevel="65">
        <IdMatch idRef="Regex_france_cni" />
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="21a8c-1739">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="21a8c-1739">Keywords</span></span>

<span data-ttu-id="21a8c-1740">Nenhum</span><span class="sxs-lookup"><span data-stu-id="21a8c-1740">None</span></span>
   
## <a name="france-passport-number"></a><span data-ttu-id="21a8c-1741">Número de passaporte da França</span><span class="sxs-lookup"><span data-stu-id="21a8c-1741">France Passport Number</span></span>

### <a name="format"></a><span data-ttu-id="21a8c-1742">Format</span><span class="sxs-lookup"><span data-stu-id="21a8c-1742">Format</span></span>

<span data-ttu-id="21a8c-1743">Nove letras e dígitos</span><span class="sxs-lookup"><span data-stu-id="21a8c-1743">Nine digits and letters</span></span>

### <a name="pattern"></a><span data-ttu-id="21a8c-1744">Padrão</span><span class="sxs-lookup"><span data-stu-id="21a8c-1744">Pattern</span></span>

<span data-ttu-id="21a8c-1745">Nove letras e dígitos:</span><span class="sxs-lookup"><span data-stu-id="21a8c-1745">Nine digits and letters:</span></span>
- <span data-ttu-id="21a8c-1746">Dois dígitos</span><span class="sxs-lookup"><span data-stu-id="21a8c-1746">Two digits</span></span> 
- <span data-ttu-id="21a8c-1747">Duas letras (não diferenciam maiúsculas de minúsculas)</span><span class="sxs-lookup"><span data-stu-id="21a8c-1747">Two letters (not case sensitive)</span></span> 
- <span data-ttu-id="21a8c-1748">Cinco dígitos</span><span class="sxs-lookup"><span data-stu-id="21a8c-1748">Five digits</span></span>

### <a name="checksum"></a><span data-ttu-id="21a8c-1749">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="21a8c-1749">Checksum</span></span>

<span data-ttu-id="21a8c-1750">Não</span><span class="sxs-lookup"><span data-stu-id="21a8c-1750">No</span></span>

### <a name="definition"></a><span data-ttu-id="21a8c-1751">Definição</span><span class="sxs-lookup"><span data-stu-id="21a8c-1751">Definition</span></span>

<span data-ttu-id="21a8c-1752">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="21a8c-1752">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="21a8c-1753">A função Func_fr_passport localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="21a8c-1753">The function Func_fr_passport finds content that matches the pattern.</span></span>
- <span data-ttu-id="21a8c-1754">Uma palavra-chave de Keyword_passport for encontrada.</span><span class="sxs-lookup"><span data-stu-id="21a8c-1754">A keyword from Keyword_passport is found.</span></span>

```
<!-- France Passport Number -->
<Entity id="3008b884-8c8c-4cd8-a289-99f34fc7ff5d" patternsProximity="300" recommendedConfidence="75">
  <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_fr_passport" />
        <Match idRef="Keyword_passport" />
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="21a8c-1755">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="21a8c-1755">Keywords</span></span>

#### <a name="keywordpassport"></a><span data-ttu-id="21a8c-1756">Keyword_passport</span><span class="sxs-lookup"><span data-stu-id="21a8c-1756">Keyword_passport</span></span>

- <span data-ttu-id="21a8c-1757">Passport Number</span><span class="sxs-lookup"><span data-stu-id="21a8c-1757">Passport Number</span></span>
- <span data-ttu-id="21a8c-1758">Passport No</span><span class="sxs-lookup"><span data-stu-id="21a8c-1758">Passport No</span></span>
- <span data-ttu-id="21a8c-1759">Passport #</span><span class="sxs-lookup"><span data-stu-id="21a8c-1759">Passport #</span></span>
- <span data-ttu-id="21a8c-1760">Passaport</span><span class="sxs-lookup"><span data-stu-id="21a8c-1760">Passport#</span></span>
- <span data-ttu-id="21a8c-1761">Passportid</span><span class="sxs-lookup"><span data-stu-id="21a8c-1761">PassportID</span></span>
- <span data-ttu-id="21a8c-1762">Passportno</span><span class="sxs-lookup"><span data-stu-id="21a8c-1762">Passportno</span></span>
- <span data-ttu-id="21a8c-1763">passportnumber</span><span class="sxs-lookup"><span data-stu-id="21a8c-1763">passportnumber</span></span>
- <span data-ttu-id="21a8c-1764">パスポート</span><span class="sxs-lookup"><span data-stu-id="21a8c-1764">パスポート</span></span>
- <span data-ttu-id="21a8c-1765">パスポート番号</span><span class="sxs-lookup"><span data-stu-id="21a8c-1765">パスポート番号</span></span>
- <span data-ttu-id="21a8c-1766">パスポートのNum</span><span class="sxs-lookup"><span data-stu-id="21a8c-1766">パスポートのNum</span></span>
- <span data-ttu-id="21a8c-1767">パスポート ＃</span><span class="sxs-lookup"><span data-stu-id="21a8c-1767">パスポート ＃</span></span> 
- <span data-ttu-id="21a8c-1768">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="21a8c-1768">Numéro de passeport</span></span>
- <span data-ttu-id="21a8c-1769">Passeport n °</span><span class="sxs-lookup"><span data-stu-id="21a8c-1769">Passeport n °</span></span>
- <span data-ttu-id="21a8c-1770">Passeport Non</span><span class="sxs-lookup"><span data-stu-id="21a8c-1770">Passeport Non</span></span>
- <span data-ttu-id="21a8c-1771">Passeport #</span><span class="sxs-lookup"><span data-stu-id="21a8c-1771">Passeport #</span></span>
- <span data-ttu-id="21a8c-1772">Passeport #</span><span class="sxs-lookup"><span data-stu-id="21a8c-1772">Passeport#</span></span>
- <span data-ttu-id="21a8c-1773">PasseportNon</span><span class="sxs-lookup"><span data-stu-id="21a8c-1773">PasseportNon</span></span>
- <span data-ttu-id="21a8c-1774">Passeportn °</span><span class="sxs-lookup"><span data-stu-id="21a8c-1774">Passeportn °</span></span>

      
## <a name="france-social-security-number-insee"></a><span data-ttu-id="21a8c-1775">Número de seguridade social da França (INSEE)</span><span class="sxs-lookup"><span data-stu-id="21a8c-1775">France Social Security Number (INSEE)</span></span>

### <a name="format"></a><span data-ttu-id="21a8c-1776">Format</span><span class="sxs-lookup"><span data-stu-id="21a8c-1776">Format</span></span>

<span data-ttu-id="21a8c-1777">15 dígitos</span><span class="sxs-lookup"><span data-stu-id="21a8c-1777">15 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="21a8c-1778">Padrão</span><span class="sxs-lookup"><span data-stu-id="21a8c-1778">Pattern</span></span>

<span data-ttu-id="21a8c-1779">Deve corresponder a um dos dois padrões:</span><span class="sxs-lookup"><span data-stu-id="21a8c-1779">Must match one of two patterns:</span></span>
- <span data-ttu-id="21a8c-1780">13 dígitos seguidos de um espaço seguido de dois dígitos</span><span class="sxs-lookup"><span data-stu-id="21a8c-1780">13 digits followed by a space followed by two digits</span></span><br/>
<span data-ttu-id="21a8c-1781">ou</span><span class="sxs-lookup"><span data-stu-id="21a8c-1781">or</span></span>
- <span data-ttu-id="21a8c-1782">15 dígitos consecutivos</span><span class="sxs-lookup"><span data-stu-id="21a8c-1782">15 consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="21a8c-1783">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="21a8c-1783">Checksum</span></span>

<span data-ttu-id="21a8c-1784">Sim</span><span class="sxs-lookup"><span data-stu-id="21a8c-1784">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="21a8c-1785">Definição</span><span class="sxs-lookup"><span data-stu-id="21a8c-1785">Definition</span></span>

<span data-ttu-id="21a8c-1786">Uma política de DLP tem 95% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="21a8c-1786">A DLP policy is 95% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="21a8c-1787">A função Func_french_insee ou Func_fr_insee localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="21a8c-1787">The function Func_french_insee or Func_fr_insee finds content that matches the pattern.</span></span>
- <span data-ttu-id="21a8c-1788">Uma palavra-chave de Keyword_fr_insee for encontrada.</span><span class="sxs-lookup"><span data-stu-id="21a8c-1788">A keyword from Keyword_fr_insee is found.</span></span>
- <span data-ttu-id="21a8c-1789">A soma de verificação passa.</span><span class="sxs-lookup"><span data-stu-id="21a8c-1789">The checksum passes.</span></span>

<span data-ttu-id="21a8c-1790">Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="21a8c-1790">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="21a8c-1791">A função Func_french_insee ou Func_fr_insee localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="21a8c-1791">The function Func_french_insee or Func_fr_insee finds content that matches the pattern.</span></span>
- <span data-ttu-id="21a8c-1792">Nenhuma palavra-chave de Keyword_fr_insee for encontrada.</span><span class="sxs-lookup"><span data-stu-id="21a8c-1792">No keyword from Keyword_fr_insee is found.</span></span>
- <span data-ttu-id="21a8c-1793">A soma de verificação passa.</span><span class="sxs-lookup"><span data-stu-id="21a8c-1793">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="21a8c-1794">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="21a8c-1794">Keywords</span></span>

#### <a name="keywordfrinsee"></a><span data-ttu-id="21a8c-1795">Keyword_fr_insee</span><span class="sxs-lookup"><span data-stu-id="21a8c-1795">Keyword_fr_insee</span></span>

- <span data-ttu-id="21a8c-1796">INSEE</span><span class="sxs-lookup"><span data-stu-id="21a8c-1796">insee</span></span>
- <span data-ttu-id="21a8c-1797">securité sociale</span><span class="sxs-lookup"><span data-stu-id="21a8c-1797">securité sociale</span></span>
- <span data-ttu-id="21a8c-1798">securite sociale</span><span class="sxs-lookup"><span data-stu-id="21a8c-1798">securite sociale</span></span>
- <span data-ttu-id="21a8c-1799">national id</span><span class="sxs-lookup"><span data-stu-id="21a8c-1799">national id</span></span>
- <span data-ttu-id="21a8c-1800">national identification</span><span class="sxs-lookup"><span data-stu-id="21a8c-1800">national identification</span></span>
- <span data-ttu-id="21a8c-1801">numéro d'identité</span><span class="sxs-lookup"><span data-stu-id="21a8c-1801">numéro d'identité</span></span>
- <span data-ttu-id="21a8c-1802">no d'identité</span><span class="sxs-lookup"><span data-stu-id="21a8c-1802">no d'identité</span></span>
- <span data-ttu-id="21a8c-1803">Não.</span><span class="sxs-lookup"><span data-stu-id="21a8c-1803">no.</span></span> <span data-ttu-id="21a8c-1804">d'identité</span><span class="sxs-lookup"><span data-stu-id="21a8c-1804">d'identité</span></span>
- <span data-ttu-id="21a8c-1805">numero d'identite</span><span class="sxs-lookup"><span data-stu-id="21a8c-1805">numero d'identite</span></span>
- <span data-ttu-id="21a8c-1806">no d'identite</span><span class="sxs-lookup"><span data-stu-id="21a8c-1806">no d'identite</span></span>
- <span data-ttu-id="21a8c-1807">Não.</span><span class="sxs-lookup"><span data-stu-id="21a8c-1807">no.</span></span> <span data-ttu-id="21a8c-1808">d'identite</span><span class="sxs-lookup"><span data-stu-id="21a8c-1808">d'identite</span></span>
- <span data-ttu-id="21a8c-1809">social security number</span><span class="sxs-lookup"><span data-stu-id="21a8c-1809">social security number</span></span>
- <span data-ttu-id="21a8c-1810">social security code</span><span class="sxs-lookup"><span data-stu-id="21a8c-1810">social security code</span></span>
- <span data-ttu-id="21a8c-1811">social insurance number</span><span class="sxs-lookup"><span data-stu-id="21a8c-1811">social insurance number</span></span>
- <span data-ttu-id="21a8c-1812">le numéro d'identification nationale</span><span class="sxs-lookup"><span data-stu-id="21a8c-1812">le numéro d'identification nationale</span></span>
- <span data-ttu-id="21a8c-1813">d'identité nationale</span><span class="sxs-lookup"><span data-stu-id="21a8c-1813">d'identité nationale</span></span>
- <span data-ttu-id="21a8c-1814">numéro de sécurité sociale</span><span class="sxs-lookup"><span data-stu-id="21a8c-1814">numéro de sécurité sociale</span></span>
- <span data-ttu-id="21a8c-1815">le code de la sécurité sociale</span><span class="sxs-lookup"><span data-stu-id="21a8c-1815">le code de la sécurité sociale</span></span>
- <span data-ttu-id="21a8c-1816">numéro d'assurance sociale</span><span class="sxs-lookup"><span data-stu-id="21a8c-1816">numéro d'assurance sociale</span></span>
- <span data-ttu-id="21a8c-1817">numéro de sécu</span><span class="sxs-lookup"><span data-stu-id="21a8c-1817">numéro de sécu</span></span>
- <span data-ttu-id="21a8c-1818">code sécu</span><span class="sxs-lookup"><span data-stu-id="21a8c-1818">code sécu</span></span> 
   
## <a name="german-drivers-license-number"></a><span data-ttu-id="21a8c-1819">Número de carteira de motorista da Alemanha</span><span class="sxs-lookup"><span data-stu-id="21a8c-1819">German Driver's License Number</span></span>

### <a name="format"></a><span data-ttu-id="21a8c-1820">Format</span><span class="sxs-lookup"><span data-stu-id="21a8c-1820">Format</span></span>

<span data-ttu-id="21a8c-1821">Combinação de 11 dígitos e letras</span><span class="sxs-lookup"><span data-stu-id="21a8c-1821">Combination of 11 digits and letters</span></span>

### <a name="pattern"></a><span data-ttu-id="21a8c-1822">Padrão</span><span class="sxs-lookup"><span data-stu-id="21a8c-1822">Pattern</span></span>

<span data-ttu-id="21a8c-1823">11 dígitos e letras (não diferenciam maiúsculas de minúsculas):</span><span class="sxs-lookup"><span data-stu-id="21a8c-1823">11 digits and letters (not case sensitive):</span></span>
- <span data-ttu-id="21a8c-1824">Um dígito ou letra</span><span class="sxs-lookup"><span data-stu-id="21a8c-1824">A digit or letter</span></span> 
- <span data-ttu-id="21a8c-1825">Dois dígitos</span><span class="sxs-lookup"><span data-stu-id="21a8c-1825">Two digits</span></span> 
- <span data-ttu-id="21a8c-1826">Seis dígitos ou letras</span><span class="sxs-lookup"><span data-stu-id="21a8c-1826">Six digits or letters</span></span> 
- <span data-ttu-id="21a8c-1827">Um dígito</span><span class="sxs-lookup"><span data-stu-id="21a8c-1827">A digit</span></span> 
- <span data-ttu-id="21a8c-1828">Um dígito ou letra</span><span class="sxs-lookup"><span data-stu-id="21a8c-1828">A digit or letter</span></span>

### <a name="checksum"></a><span data-ttu-id="21a8c-1829">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="21a8c-1829">Checksum</span></span>

<span data-ttu-id="21a8c-1830">Sim</span><span class="sxs-lookup"><span data-stu-id="21a8c-1830">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="21a8c-1831">Definição</span><span class="sxs-lookup"><span data-stu-id="21a8c-1831">Definition</span></span>

<span data-ttu-id="21a8c-1832">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="21a8c-1832">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="21a8c-1833">A função Func_german_drivers_license localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="21a8c-1833">The function Func_german_drivers_license finds content that matches the pattern.</span></span>
- <span data-ttu-id="21a8c-1834">Pelo menos uma das seguintes opções for verdadeira:</span><span class="sxs-lookup"><span data-stu-id="21a8c-1834">At least one of the following is true:</span></span>
    - <span data-ttu-id="21a8c-1835">Uma palavra-chave de Keyword_german_drivers_license_number for encontrada.</span><span class="sxs-lookup"><span data-stu-id="21a8c-1835">A keyword from Keyword_german_drivers_license_number is found.</span></span>
    - <span data-ttu-id="21a8c-1836">Uma palavra-chave de Keyword_german_drivers_license_collaborative for encontrada.</span><span class="sxs-lookup"><span data-stu-id="21a8c-1836">A keyword from Keyword_german_drivers_license_collaborative is found.</span></span>
    - <span data-ttu-id="21a8c-1837">Uma palavra-chave de Keyword_german_drivers_license for encontrada.</span><span class="sxs-lookup"><span data-stu-id="21a8c-1837">A keyword from Keyword_german_drivers_license is found.</span></span>
- <span data-ttu-id="21a8c-1838">A soma de verificação passa.</span><span class="sxs-lookup"><span data-stu-id="21a8c-1838">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="21a8c-1839">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="21a8c-1839">Keywords</span></span>

#### <a name="keywordgermandriverslicensenumber"></a><span data-ttu-id="21a8c-1840">Keyword_german_drivers_license_number</span><span class="sxs-lookup"><span data-stu-id="21a8c-1840">Keyword_german_drivers_license_number</span></span>

- <span data-ttu-id="21a8c-1841">Führerschein</span><span class="sxs-lookup"><span data-stu-id="21a8c-1841">Führerschein</span></span>
- <span data-ttu-id="21a8c-1842">Fuhrerschein</span><span class="sxs-lookup"><span data-stu-id="21a8c-1842">Fuhrerschein</span></span>
- <span data-ttu-id="21a8c-1843">Fuehrerschein</span><span class="sxs-lookup"><span data-stu-id="21a8c-1843">Fuehrerschein</span></span>
- <span data-ttu-id="21a8c-1844">Führerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="21a8c-1844">Führerscheinnummer</span></span>
- <span data-ttu-id="21a8c-1845">Fuhrerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="21a8c-1845">Fuhrerscheinnummer</span></span>
- <span data-ttu-id="21a8c-1846">Fuehrerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="21a8c-1846">Fuehrerscheinnummer</span></span>
- <span data-ttu-id="21a8c-1847">Führerschein-</span><span class="sxs-lookup"><span data-stu-id="21a8c-1847">Führerschein-</span></span> 
- <span data-ttu-id="21a8c-1848">Fuhrerschein-</span><span class="sxs-lookup"><span data-stu-id="21a8c-1848">Fuhrerschein-</span></span> 
- <span data-ttu-id="21a8c-1849">Fuehrerschein-</span><span class="sxs-lookup"><span data-stu-id="21a8c-1849">Fuehrerschein-</span></span> 
- <span data-ttu-id="21a8c-1850">FührerscheinnummerNr</span><span class="sxs-lookup"><span data-stu-id="21a8c-1850">FührerscheinnummerNr</span></span>
- <span data-ttu-id="21a8c-1851">FuhrerscheinnummerNr</span><span class="sxs-lookup"><span data-stu-id="21a8c-1851">FuhrerscheinnummerNr</span></span>
- <span data-ttu-id="21a8c-1852">FuehrerscheinnummerNr</span><span class="sxs-lookup"><span data-stu-id="21a8c-1852">FuehrerscheinnummerNr</span></span>
- <span data-ttu-id="21a8c-1853">FührerscheinnummerKlasse</span><span class="sxs-lookup"><span data-stu-id="21a8c-1853">FührerscheinnummerKlasse</span></span>
- <span data-ttu-id="21a8c-1854">FuhrerscheinnummerKlasse</span><span class="sxs-lookup"><span data-stu-id="21a8c-1854">FuhrerscheinnummerKlasse</span></span>
- <span data-ttu-id="21a8c-1855">FuehrerscheinnummerKlasse</span><span class="sxs-lookup"><span data-stu-id="21a8c-1855">FuehrerscheinnummerKlasse</span></span>
- <span data-ttu-id="21a8c-1856">Führerschein- Nr</span><span class="sxs-lookup"><span data-stu-id="21a8c-1856">Führerschein- Nr</span></span>
- <span data-ttu-id="21a8c-1857">Fuhrerschein- Nr</span><span class="sxs-lookup"><span data-stu-id="21a8c-1857">Fuhrerschein- Nr</span></span>
- <span data-ttu-id="21a8c-1858">Fuehrerschein- Nr</span><span class="sxs-lookup"><span data-stu-id="21a8c-1858">Fuehrerschein- Nr</span></span> 
- <span data-ttu-id="21a8c-1859">Führerschein- Klasse</span><span class="sxs-lookup"><span data-stu-id="21a8c-1859">Führerschein- Klasse</span></span> 
- <span data-ttu-id="21a8c-1860">Fuhrerschein- Klasse</span><span class="sxs-lookup"><span data-stu-id="21a8c-1860">Fuhrerschein- Klasse</span></span> 
- <span data-ttu-id="21a8c-1861">Fuehrerschein- Klasse</span><span class="sxs-lookup"><span data-stu-id="21a8c-1861">Fuehrerschein- Klasse</span></span>
- <span data-ttu-id="21a8c-1862">FührerscheinnummerNr</span><span class="sxs-lookup"><span data-stu-id="21a8c-1862">FührerscheinnummerNr</span></span> 
- <span data-ttu-id="21a8c-1863">FuhrerscheinnummerNr</span><span class="sxs-lookup"><span data-stu-id="21a8c-1863">FuhrerscheinnummerNr</span></span> 
- <span data-ttu-id="21a8c-1864">FuehrerscheinnummerNr</span><span class="sxs-lookup"><span data-stu-id="21a8c-1864">FuehrerscheinnummerNr</span></span> 
- <span data-ttu-id="21a8c-1865">FührerscheinnummerKlasse</span><span class="sxs-lookup"><span data-stu-id="21a8c-1865">FührerscheinnummerKlasse</span></span> 
- <span data-ttu-id="21a8c-1866">FuhrerscheinnummerKlasse</span><span class="sxs-lookup"><span data-stu-id="21a8c-1866">FuhrerscheinnummerKlasse</span></span> 
- <span data-ttu-id="21a8c-1867">FuehrerscheinnummerKlasse</span><span class="sxs-lookup"><span data-stu-id="21a8c-1867">FuehrerscheinnummerKlasse</span></span> 
- <span data-ttu-id="21a8c-1868">Führerschein- Nr</span><span class="sxs-lookup"><span data-stu-id="21a8c-1868">Führerschein- Nr</span></span> 
- <span data-ttu-id="21a8c-1869">Fuhrerschein- Nr</span><span class="sxs-lookup"><span data-stu-id="21a8c-1869">Fuhrerschein- Nr</span></span> 
- <span data-ttu-id="21a8c-1870">Fuehrerschein- Nr</span><span class="sxs-lookup"><span data-stu-id="21a8c-1870">Fuehrerschein- Nr</span></span> 
- <span data-ttu-id="21a8c-1871">Führerschein- Klasse</span><span class="sxs-lookup"><span data-stu-id="21a8c-1871">Führerschein- Klasse</span></span> 
- <span data-ttu-id="21a8c-1872">Fuhrerschein- Klasse</span><span class="sxs-lookup"><span data-stu-id="21a8c-1872">Fuhrerschein- Klasse</span></span> 
- <span data-ttu-id="21a8c-1873">Fuehrerschein- Klasse</span><span class="sxs-lookup"><span data-stu-id="21a8c-1873">Fuehrerschein- Klasse</span></span> 
- <span data-ttu-id="21a8c-1874">DISTRIBUIÇÃO</span><span class="sxs-lookup"><span data-stu-id="21a8c-1874">DL</span></span> 
- <span data-ttu-id="21a8c-1875">DL</span><span class="sxs-lookup"><span data-stu-id="21a8c-1875">DLS</span></span>
- <span data-ttu-id="21a8c-1876">Driv Lic</span><span class="sxs-lookup"><span data-stu-id="21a8c-1876">Driv Lic</span></span> 
- <span data-ttu-id="21a8c-1877">Driv Licen</span><span class="sxs-lookup"><span data-stu-id="21a8c-1877">Driv Licen</span></span> 
- <span data-ttu-id="21a8c-1878">Driv License</span><span class="sxs-lookup"><span data-stu-id="21a8c-1878">Driv License</span></span>
- <span data-ttu-id="21a8c-1879">Driv Licenses</span><span class="sxs-lookup"><span data-stu-id="21a8c-1879">Driv Licenses</span></span> 
- <span data-ttu-id="21a8c-1880">Driv Licence</span><span class="sxs-lookup"><span data-stu-id="21a8c-1880">Driv Licence</span></span> 
- <span data-ttu-id="21a8c-1881">Driv Licences</span><span class="sxs-lookup"><span data-stu-id="21a8c-1881">Driv Licences</span></span> 
- <span data-ttu-id="21a8c-1882">Driv Lic</span><span class="sxs-lookup"><span data-stu-id="21a8c-1882">Driv Lic</span></span> 
- <span data-ttu-id="21a8c-1883">Driver Licen</span><span class="sxs-lookup"><span data-stu-id="21a8c-1883">Driver Licen</span></span> 
- <span data-ttu-id="21a8c-1884">Driver License</span><span class="sxs-lookup"><span data-stu-id="21a8c-1884">Driver License</span></span> 
- <span data-ttu-id="21a8c-1885">Driver Licenses</span><span class="sxs-lookup"><span data-stu-id="21a8c-1885">Driver Licenses</span></span> 
- <span data-ttu-id="21a8c-1886">Driver Licence</span><span class="sxs-lookup"><span data-stu-id="21a8c-1886">Driver Licence</span></span> 
- <span data-ttu-id="21a8c-1887">Driver Licences</span><span class="sxs-lookup"><span data-stu-id="21a8c-1887">Driver Licences</span></span> 
- <span data-ttu-id="21a8c-1888">Drivers Lic</span><span class="sxs-lookup"><span data-stu-id="21a8c-1888">Drivers Lic</span></span> 
- <span data-ttu-id="21a8c-1889">Drivers Licen</span><span class="sxs-lookup"><span data-stu-id="21a8c-1889">Drivers Licen</span></span> 
- <span data-ttu-id="21a8c-1890">Drivers License</span><span class="sxs-lookup"><span data-stu-id="21a8c-1890">Drivers License</span></span> 
- <span data-ttu-id="21a8c-1891">Drivers Licenses</span><span class="sxs-lookup"><span data-stu-id="21a8c-1891">Drivers Licenses</span></span> 
- <span data-ttu-id="21a8c-1892">Drivers Licence</span><span class="sxs-lookup"><span data-stu-id="21a8c-1892">Drivers Licence</span></span> 
- <span data-ttu-id="21a8c-1893">Drivers Licences</span><span class="sxs-lookup"><span data-stu-id="21a8c-1893">Drivers Licences</span></span> 
- <span data-ttu-id="21a8c-1894">Driver's Lic</span><span class="sxs-lookup"><span data-stu-id="21a8c-1894">Driver's Lic</span></span> 
- <span data-ttu-id="21a8c-1895">Driver's Licen</span><span class="sxs-lookup"><span data-stu-id="21a8c-1895">Driver's Licen</span></span> 
- <span data-ttu-id="21a8c-1896">Driver's License</span><span class="sxs-lookup"><span data-stu-id="21a8c-1896">Driver's License</span></span> 
- <span data-ttu-id="21a8c-1897">Driver's Licenses</span><span class="sxs-lookup"><span data-stu-id="21a8c-1897">Driver's Licenses</span></span> 
- <span data-ttu-id="21a8c-1898">Driver's Licence</span><span class="sxs-lookup"><span data-stu-id="21a8c-1898">Driver's Licence</span></span> 
- <span data-ttu-id="21a8c-1899">Driver's Licences</span><span class="sxs-lookup"><span data-stu-id="21a8c-1899">Driver's Licences</span></span> 
- <span data-ttu-id="21a8c-1900">Driving Lic</span><span class="sxs-lookup"><span data-stu-id="21a8c-1900">Driving Lic</span></span> 
- <span data-ttu-id="21a8c-1901">Driving Licen</span><span class="sxs-lookup"><span data-stu-id="21a8c-1901">Driving Licen</span></span> 
- <span data-ttu-id="21a8c-1902">Driving License</span><span class="sxs-lookup"><span data-stu-id="21a8c-1902">Driving License</span></span> 
- <span data-ttu-id="21a8c-1903">Driving Licenses</span><span class="sxs-lookup"><span data-stu-id="21a8c-1903">Driving Licenses</span></span> 
- <span data-ttu-id="21a8c-1904">Driving Licence</span><span class="sxs-lookup"><span data-stu-id="21a8c-1904">Driving Licence</span></span> 
- <span data-ttu-id="21a8c-1905">Driving Licences</span><span class="sxs-lookup"><span data-stu-id="21a8c-1905">Driving Licences</span></span>

#### <a name="keywordgermandriverslicensecollaborative"></a><span data-ttu-id="21a8c-1906">Keyword_german_drivers_license_collaborative</span><span class="sxs-lookup"><span data-stu-id="21a8c-1906">Keyword_german_drivers_license_collaborative</span></span>

- <span data-ttu-id="21a8c-1907">NR-Führerschein</span><span class="sxs-lookup"><span data-stu-id="21a8c-1907">Nr-Führerschein</span></span> 
- <span data-ttu-id="21a8c-1908">NR-Fuhrerschein</span><span class="sxs-lookup"><span data-stu-id="21a8c-1908">Nr-Fuhrerschein</span></span> 
- <span data-ttu-id="21a8c-1909">NR-Fuehrerschein</span><span class="sxs-lookup"><span data-stu-id="21a8c-1909">Nr-Fuehrerschein</span></span> 
- <span data-ttu-id="21a8c-1910">No-Führerschein</span><span class="sxs-lookup"><span data-stu-id="21a8c-1910">No-Führerschein</span></span> 
- <span data-ttu-id="21a8c-1911">No-Fuhrerschein</span><span class="sxs-lookup"><span data-stu-id="21a8c-1911">No-Fuhrerschein</span></span> 
- <span data-ttu-id="21a8c-1912">No-Fuehrerschein</span><span class="sxs-lookup"><span data-stu-id="21a8c-1912">No-Fuehrerschein</span></span> 
- <span data-ttu-id="21a8c-1913">N-Führerschein</span><span class="sxs-lookup"><span data-stu-id="21a8c-1913">N-Führerschein</span></span> 
- <span data-ttu-id="21a8c-1914">N-Fuhrerschein</span><span class="sxs-lookup"><span data-stu-id="21a8c-1914">N-Fuhrerschein</span></span> 
- <span data-ttu-id="21a8c-1915">N-Fuehrerschein</span><span class="sxs-lookup"><span data-stu-id="21a8c-1915">N-Fuehrerschein</span></span>
- <span data-ttu-id="21a8c-1916">NR-Führerschein</span><span class="sxs-lookup"><span data-stu-id="21a8c-1916">Nr-Führerschein</span></span> 
- <span data-ttu-id="21a8c-1917">NR-Fuhrerschein</span><span class="sxs-lookup"><span data-stu-id="21a8c-1917">Nr-Fuhrerschein</span></span> 
- <span data-ttu-id="21a8c-1918">NR-Fuehrerschein</span><span class="sxs-lookup"><span data-stu-id="21a8c-1918">Nr-Fuehrerschein</span></span> 
- <span data-ttu-id="21a8c-1919">No-Führerschein</span><span class="sxs-lookup"><span data-stu-id="21a8c-1919">No-Führerschein</span></span> 
- <span data-ttu-id="21a8c-1920">No-Fuhrerschein</span><span class="sxs-lookup"><span data-stu-id="21a8c-1920">No-Fuhrerschein</span></span> 
- <span data-ttu-id="21a8c-1921">No-Fuehrerschein</span><span class="sxs-lookup"><span data-stu-id="21a8c-1921">No-Fuehrerschein</span></span> 
- <span data-ttu-id="21a8c-1922">N-Führerschein</span><span class="sxs-lookup"><span data-stu-id="21a8c-1922">N-Führerschein</span></span> 
- <span data-ttu-id="21a8c-1923">N-Fuhrerschein</span><span class="sxs-lookup"><span data-stu-id="21a8c-1923">N-Fuhrerschein</span></span> 
- <span data-ttu-id="21a8c-1924">N-Fuehrerschein</span><span class="sxs-lookup"><span data-stu-id="21a8c-1924">N-Fuehrerschein</span></span> 

#### <a name="keywordgermandriverslicense"></a><span data-ttu-id="21a8c-1925">Keyword_german_drivers_license</span><span class="sxs-lookup"><span data-stu-id="21a8c-1925">Keyword_german_drivers_license</span></span>

- <span data-ttu-id="21a8c-1926">ausstellungsdatum</span><span class="sxs-lookup"><span data-stu-id="21a8c-1926">ausstellungsdatum</span></span>
- <span data-ttu-id="21a8c-1927">ausstellungsort</span><span class="sxs-lookup"><span data-stu-id="21a8c-1927">ausstellungsort</span></span>
- <span data-ttu-id="21a8c-1928">ausstellende behöde</span><span class="sxs-lookup"><span data-stu-id="21a8c-1928">ausstellende behöde</span></span>
- <span data-ttu-id="21a8c-1929">ausstellende behorde</span><span class="sxs-lookup"><span data-stu-id="21a8c-1929">ausstellende behorde</span></span>
- <span data-ttu-id="21a8c-1930">ausstellende behoerde</span><span class="sxs-lookup"><span data-stu-id="21a8c-1930">ausstellende behoerde</span></span>
   
## <a name="german-passport-number"></a><span data-ttu-id="21a8c-1931">Número de passaporte da Alemanha</span><span class="sxs-lookup"><span data-stu-id="21a8c-1931">German Passport Number</span></span>

### <a name="format"></a><span data-ttu-id="21a8c-1932">Format</span><span class="sxs-lookup"><span data-stu-id="21a8c-1932">Format</span></span>

<span data-ttu-id="21a8c-1933">10 dígitos ou letras</span><span class="sxs-lookup"><span data-stu-id="21a8c-1933">10 digits or letters</span></span>

### <a name="pattern"></a><span data-ttu-id="21a8c-1934">Padrão</span><span class="sxs-lookup"><span data-stu-id="21a8c-1934">Pattern</span></span>

<span data-ttu-id="21a8c-1935">O padrão deve incluir todos os seguintes itens:</span><span class="sxs-lookup"><span data-stu-id="21a8c-1935">Pattern must include all of the following:</span></span>
- <span data-ttu-id="21a8c-1936">Primeiro caractere é um dígito ou uma letra desse conjunto (C, F, G, H, J, K)</span><span class="sxs-lookup"><span data-stu-id="21a8c-1936">First character is a digit or a letter from this set (C, F, G, H, J, K)</span></span> 
- <span data-ttu-id="21a8c-1937">Três dígitos</span><span class="sxs-lookup"><span data-stu-id="21a8c-1937">Three digits</span></span> 
- <span data-ttu-id="21a8c-1938">Cinco dígitos ou letras a partir desse conjunto (C, -H, J N, P, R, T, V-Z)</span><span class="sxs-lookup"><span data-stu-id="21a8c-1938">Five digits or letters from this set (C, -H, J-N, P, R, T, V-Z)</span></span> 
- <span data-ttu-id="21a8c-1939">Um dígito</span><span class="sxs-lookup"><span data-stu-id="21a8c-1939">A digit</span></span>

### <a name="checksum"></a><span data-ttu-id="21a8c-1940">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="21a8c-1940">Checksum</span></span>

<span data-ttu-id="21a8c-1941">Sim</span><span class="sxs-lookup"><span data-stu-id="21a8c-1941">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="21a8c-1942">Definição</span><span class="sxs-lookup"><span data-stu-id="21a8c-1942">Definition</span></span>

<span data-ttu-id="21a8c-1943">Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="21a8c-1943">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="21a8c-1944">A função Func_german_passport localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="21a8c-1944">The function Func_german_passport finds content that matches the pattern.</span></span>
- <span data-ttu-id="21a8c-1945">Uma palavra-chave de qualquer uma das cinco listas de palavras-chave for encontrada.</span><span class="sxs-lookup"><span data-stu-id="21a8c-1945">A keyword from any of the five keyword lists is found.</span></span>
- <span data-ttu-id="21a8c-1946">A soma de verificação passa.</span><span class="sxs-lookup"><span data-stu-id="21a8c-1946">The checksum passes.</span></span>

<span data-ttu-id="21a8c-1947">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="21a8c-1947">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="21a8c-1948">A função Func_german_passport_data localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="21a8c-1948">The function Func_german_passport_data finds content that matches the pattern.</span></span>
- <span data-ttu-id="21a8c-1949">Uma palavra-chave de qualquer uma das cinco listas de palavras-chave for encontrada.</span><span class="sxs-lookup"><span data-stu-id="21a8c-1949">A keyword from any of the five keyword lists is found.</span></span>
- <span data-ttu-id="21a8c-1950">A soma de verificação passa.</span><span class="sxs-lookup"><span data-stu-id="21a8c-1950">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="21a8c-1951">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="21a8c-1951">Keywords</span></span>

#### <a name="keywordgermanpassport"></a><span data-ttu-id="21a8c-1952">Keyword_german_passport</span><span class="sxs-lookup"><span data-stu-id="21a8c-1952">Keyword_german_passport</span></span>

- <span data-ttu-id="21a8c-1953">reisepass</span><span class="sxs-lookup"><span data-stu-id="21a8c-1953">reisepass</span></span>
- <span data-ttu-id="21a8c-1954">reisepasse</span><span class="sxs-lookup"><span data-stu-id="21a8c-1954">reisepasse</span></span>
- <span data-ttu-id="21a8c-1955">reisepassnummer</span><span class="sxs-lookup"><span data-stu-id="21a8c-1955">reisepassnummer</span></span>
- <span data-ttu-id="21a8c-1956">Passaport</span><span class="sxs-lookup"><span data-stu-id="21a8c-1956">passport</span></span>
- <span data-ttu-id="21a8c-1957">Passports</span><span class="sxs-lookup"><span data-stu-id="21a8c-1957">passports</span></span>

#### <a name="keywordgermanpassportcollaborative"></a><span data-ttu-id="21a8c-1958">Keyword_german_passport_collaborative</span><span class="sxs-lookup"><span data-stu-id="21a8c-1958">Keyword_german_passport_collaborative</span></span>

- <span data-ttu-id="21a8c-1959">geburtsdatum</span><span class="sxs-lookup"><span data-stu-id="21a8c-1959">geburtsdatum</span></span>
- <span data-ttu-id="21a8c-1960">ausstellungsdatum</span><span class="sxs-lookup"><span data-stu-id="21a8c-1960">ausstellungsdatum</span></span>
- <span data-ttu-id="21a8c-1961">ausstellungsort</span><span class="sxs-lookup"><span data-stu-id="21a8c-1961">ausstellungsort</span></span>

#### <a name="keywordgermanpassportnumber"></a><span data-ttu-id="21a8c-1962">Keyword_german_passport_number</span><span class="sxs-lookup"><span data-stu-id="21a8c-1962">Keyword_german_passport_number</span></span>

<span data-ttu-id="21a8c-1963">No-Reisepass NR-Reisepass</span><span class="sxs-lookup"><span data-stu-id="21a8c-1963">No-Reisepass Nr-Reisepass</span></span>

#### <a name="keywordgermanpassport1"></a><span data-ttu-id="21a8c-1964">Keyword_german_passport1</span><span class="sxs-lookup"><span data-stu-id="21a8c-1964">Keyword_german_passport1</span></span>

<span data-ttu-id="21a8c-1965">Reisepass-NR</span><span class="sxs-lookup"><span data-stu-id="21a8c-1965">Reisepass-Nr</span></span>

#### <a name="keywordgermanpassport2"></a><span data-ttu-id="21a8c-1966">Keyword_german_passport2</span><span class="sxs-lookup"><span data-stu-id="21a8c-1966">Keyword_german_passport2</span></span>

<span data-ttu-id="21a8c-1967">bnationalit. t</span><span class="sxs-lookup"><span data-stu-id="21a8c-1967">bnationalit.t</span></span>
   
## <a name="germany-identity-card-number"></a><span data-ttu-id="21a8c-1968">Número da carteira de identidade alemã</span><span class="sxs-lookup"><span data-stu-id="21a8c-1968">Germany Identity Card Number</span></span>

### <a name="format"></a><span data-ttu-id="21a8c-1969">Format</span><span class="sxs-lookup"><span data-stu-id="21a8c-1969">Format</span></span>

<span data-ttu-id="21a8c-1970">Desde 1 de novembro de 2010: nove letras e dígitos</span><span class="sxs-lookup"><span data-stu-id="21a8c-1970">Since 1 November 2010: Nine letters and digits</span></span>

<span data-ttu-id="21a8c-1971">De 1 de abril de 1987 até 31 de outubro de 2010:10 dígitos</span><span class="sxs-lookup"><span data-stu-id="21a8c-1971">From 1 April 1987 until 31 October 2010: 10 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="21a8c-1972">Padrão</span><span class="sxs-lookup"><span data-stu-id="21a8c-1972">Pattern</span></span>

<span data-ttu-id="21a8c-1973">Desde 1º de novembro de 2010:</span><span class="sxs-lookup"><span data-stu-id="21a8c-1973">Since 1 November 2010:</span></span>
- <span data-ttu-id="21a8c-1974">Uma letra (não diferencia maiúscula de minúscula)</span><span class="sxs-lookup"><span data-stu-id="21a8c-1974">One letter (not case sensitive)</span></span> 
- <span data-ttu-id="21a8c-1975">Oito dígitos</span><span class="sxs-lookup"><span data-stu-id="21a8c-1975">Eight digits</span></span>

<span data-ttu-id="21a8c-1976">De 1 de abril de 1987 até 31 de outubro de 2010:</span><span class="sxs-lookup"><span data-stu-id="21a8c-1976">From 1 April 1987 until 31 October 2010:</span></span>
- <span data-ttu-id="21a8c-1977">10 dígitos</span><span class="sxs-lookup"><span data-stu-id="21a8c-1977">10 digits</span></span>

### <a name="checksum"></a><span data-ttu-id="21a8c-1978">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="21a8c-1978">Checksum</span></span>

<span data-ttu-id="21a8c-1979">Não</span><span class="sxs-lookup"><span data-stu-id="21a8c-1979">No</span></span>

### <a name="definition"></a><span data-ttu-id="21a8c-1980">Definição</span><span class="sxs-lookup"><span data-stu-id="21a8c-1980">Definition</span></span>

<span data-ttu-id="21a8c-1981">Uma política de DLP tem 65% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="21a8c-1981">A DLP policy is 65% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="21a8c-1982">A expressão regular Regex_germany_id_card localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="21a8c-1982">The regular expression Regex_germany_id_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="21a8c-1983">Uma palavra-chave de Keyword_germany_id_card for encontrada.</span><span class="sxs-lookup"><span data-stu-id="21a8c-1983">A keyword from Keyword_germany_id_card is found.</span></span>

```
<!-- Germany Identity Card Number -->
<Entity id="e577372f-c42e-47a0-9d85-bebed1c237d4" recommendedConfidence="65" patternsProximity="300">
  <Pattern confidenceLevel="65">
     <IdMatch idRef="Regex_germany_id_card"/>
     <Match idRef="Keyword_germany_id_card"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="21a8c-1984">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="21a8c-1984">Keywords</span></span>

#### <a name="keywordgermanyidcard"></a><span data-ttu-id="21a8c-1985">Keyword_germany_id_card</span><span class="sxs-lookup"><span data-stu-id="21a8c-1985">Keyword_germany_id_card</span></span>

- <span data-ttu-id="21a8c-1986">Cartão de Identidade</span><span class="sxs-lookup"><span data-stu-id="21a8c-1986">Identity Card</span></span>
- <span data-ttu-id="21a8c-1987">ID</span><span class="sxs-lookup"><span data-stu-id="21a8c-1987">ID</span></span>
- <span data-ttu-id="21a8c-1988">Identificador</span><span class="sxs-lookup"><span data-stu-id="21a8c-1988">Identification</span></span>
- <span data-ttu-id="21a8c-1989">Personalausweis</span><span class="sxs-lookup"><span data-stu-id="21a8c-1989">Personalausweis</span></span>
- <span data-ttu-id="21a8c-1990">Identifizierungsnummer</span><span class="sxs-lookup"><span data-stu-id="21a8c-1990">Identifizierungsnummer</span></span>
- <span data-ttu-id="21a8c-1991">Ausweis</span><span class="sxs-lookup"><span data-stu-id="21a8c-1991">Ausweis</span></span>
- <span data-ttu-id="21a8c-1992">Identifikation</span><span class="sxs-lookup"><span data-stu-id="21a8c-1992">Identifikation</span></span>
   
## <a name="greece-national-id-card"></a><span data-ttu-id="21a8c-1993">Cartão de Identificação Nacional da Grécia</span><span class="sxs-lookup"><span data-stu-id="21a8c-1993">Greece National ID Card</span></span>

### <a name="format"></a><span data-ttu-id="21a8c-1994">Format</span><span class="sxs-lookup"><span data-stu-id="21a8c-1994">Format</span></span>

<span data-ttu-id="21a8c-1995">Combinação de 7 a 8 letras e números mais um traço</span><span class="sxs-lookup"><span data-stu-id="21a8c-1995">Combination of 7-8 letters and numbers plus a dash</span></span>

### <a name="pattern"></a><span data-ttu-id="21a8c-1996">Padrão</span><span class="sxs-lookup"><span data-stu-id="21a8c-1996">Pattern</span></span>

<span data-ttu-id="21a8c-1997">Sete letras e números (formato antigo):</span><span class="sxs-lookup"><span data-stu-id="21a8c-1997">Seven letters and numbers (old format):</span></span>
- <span data-ttu-id="21a8c-1998">Uma letra (qualquer letra do alfabeto grego) </span><span class="sxs-lookup"><span data-stu-id="21a8c-1998">One letter (any letter of the Greek alphabet)</span></span> 
- <span data-ttu-id="21a8c-1999">Um traço</span><span class="sxs-lookup"><span data-stu-id="21a8c-1999">A dash</span></span> 
- <span data-ttu-id="21a8c-2000">Seis dígitos</span><span class="sxs-lookup"><span data-stu-id="21a8c-2000">Six digits</span></span>

<span data-ttu-id="21a8c-2001">Oito letras e números (novo formato):</span><span class="sxs-lookup"><span data-stu-id="21a8c-2001">Eight letters and numbers (new format):</span></span>
- <span data-ttu-id="21a8c-2002">Duas letras cujos caracteres maiúsculos ocorre em alfabetos latino e grego (ABEZHIKMNOPTYX) </span><span class="sxs-lookup"><span data-stu-id="21a8c-2002">Two letters whose uppercase character occurs in both the Greek and Latin alphabets (ABEZHIKMNOPTYX)</span></span> 
- <span data-ttu-id="21a8c-2003">Um traço</span><span class="sxs-lookup"><span data-stu-id="21a8c-2003">A dash</span></span> 
- <span data-ttu-id="21a8c-2004">Seis dígitos</span><span class="sxs-lookup"><span data-stu-id="21a8c-2004">Six digits</span></span>

### <a name="checksum"></a><span data-ttu-id="21a8c-2005">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="21a8c-2005">Checksum</span></span>

<span data-ttu-id="21a8c-2006">Não</span><span class="sxs-lookup"><span data-stu-id="21a8c-2006">No</span></span>

### <a name="definition"></a><span data-ttu-id="21a8c-2007">Definição</span><span class="sxs-lookup"><span data-stu-id="21a8c-2007">Definition</span></span>

<span data-ttu-id="21a8c-2008">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="21a8c-2008">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="21a8c-2009">A expressão regular Regex_greece_id_card localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="21a8c-2009">The regular expression Regex_greece_id_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="21a8c-2010">Uma palavra-chave de Keyword_greece_id_card for encontrada.</span><span class="sxs-lookup"><span data-stu-id="21a8c-2010">A keyword from Keyword_greece_id_card is found.</span></span>

```
<!-- Greece National ID Card -->
<Entity id="82568215-1da1-46d3-874a-d2294d81b5ac" recommendedConfidence="85" patternsProximity="300">
  <Pattern confidenceLevel="85">
     <IdMatch idRef="Regex_greece_id_card"/>
     <Match idRef="Keyword_greece_id_card"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="21a8c-2011">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="21a8c-2011">Keywords</span></span>

#### <a name="keywordgreeceidcard"></a><span data-ttu-id="21a8c-2012">Keyword_greece_id_card</span><span class="sxs-lookup"><span data-stu-id="21a8c-2012">Keyword_greece_id_card</span></span>

- <span data-ttu-id="21a8c-2013">Cartão de identidade grego</span><span class="sxs-lookup"><span data-stu-id="21a8c-2013">Greek identity Card</span></span>
- <span data-ttu-id="21a8c-2014">Tautotita</span><span class="sxs-lookup"><span data-stu-id="21a8c-2014">Tautotita</span></span>
- <span data-ttu-id="21a8c-2015">Δελτίο αστυνομικής ταυτότητας</span><span class="sxs-lookup"><span data-stu-id="21a8c-2015">Δελτίο αστυνομικής ταυτότητας</span></span>
- <span data-ttu-id="21a8c-2016">Ταυτότητα</span><span class="sxs-lookup"><span data-stu-id="21a8c-2016">Ταυτότητα</span></span>
   
## <a name="hong-kong-identity-card-hkid-number"></a><span data-ttu-id="21a8c-2017">Número do Cartão de Identidade de Hong Kong (HKID)</span><span class="sxs-lookup"><span data-stu-id="21a8c-2017">Hong Kong Identity Card (HKID) Number</span></span>

### <a name="format"></a><span data-ttu-id="21a8c-2018">Format</span><span class="sxs-lookup"><span data-stu-id="21a8c-2018">Format</span></span>

<span data-ttu-id="21a8c-2019">Combinação de 8 a 9 letras e números mais parênteses opcionais ao redor do caractere final</span><span class="sxs-lookup"><span data-stu-id="21a8c-2019">Combination of 8-9 letters and numbers plus optional parentheses around the final character</span></span>

### <a name="pattern"></a><span data-ttu-id="21a8c-2020">Padrão</span><span class="sxs-lookup"><span data-stu-id="21a8c-2020">Pattern</span></span>

<span data-ttu-id="21a8c-2021">Combinação de 8 a 9 letras:</span><span class="sxs-lookup"><span data-stu-id="21a8c-2021">Combination of 8-9 letters:</span></span>
- <span data-ttu-id="21a8c-2022">1 a 2 letras (não diferenciam maiúsculas de minúsculas)</span><span class="sxs-lookup"><span data-stu-id="21a8c-2022">1-2 letters (not case sensitive)</span></span> 
- <span data-ttu-id="21a8c-2023">Seis dígitos</span><span class="sxs-lookup"><span data-stu-id="21a8c-2023">Six digits</span></span> 
- <span data-ttu-id="21a8c-2024">O caractere final (qualquer dígito ou a letra A), que é o dígito de verificação e é opcionalmente colocado entre parênteses.</span><span class="sxs-lookup"><span data-stu-id="21a8c-2024">The final character (any digit or the letter A), which is the check digit and is optionally enclosed in parentheses.</span></span>

### <a name="checksum"></a><span data-ttu-id="21a8c-2025">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="21a8c-2025">Checksum</span></span>

<span data-ttu-id="21a8c-2026">Sim</span><span class="sxs-lookup"><span data-stu-id="21a8c-2026">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="21a8c-2027">Definição</span><span class="sxs-lookup"><span data-stu-id="21a8c-2027">Definition</span></span>

<span data-ttu-id="21a8c-2028">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="21a8c-2028">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="21a8c-2029">A função Func_hong_kong_id_card localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="21a8c-2029">The function Func_hong_kong_id_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="21a8c-2030">Uma palavra-chave de Keyword_hong_kong_id_card for encontrada.</span><span class="sxs-lookup"><span data-stu-id="21a8c-2030">A keyword from Keyword_hong_kong_id_card is found.</span></span>
- <span data-ttu-id="21a8c-2031">A soma de verificação passa.</span><span class="sxs-lookup"><span data-stu-id="21a8c-2031">The checksum passes.</span></span>

<span data-ttu-id="21a8c-2032">Uma política de DLP tem 65% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="21a8c-2032">A DLP policy is 65% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="21a8c-2033">A função Func_hong_kong_id_card localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="21a8c-2033">The function Func_hong_kong_id_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="21a8c-2034">A soma de verificação passa.</span><span class="sxs-lookup"><span data-stu-id="21a8c-2034">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="21a8c-2035">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="21a8c-2035">Keywords</span></span>

#### <a name="keywordhongkongidcard"></a><span data-ttu-id="21a8c-2036">Keyword_hong_kong_id_card</span><span class="sxs-lookup"><span data-stu-id="21a8c-2036">Keyword_hong_kong_id_card</span></span>

- <span data-ttu-id="21a8c-2037">cartão de identidade de Hong Kong</span><span class="sxs-lookup"><span data-stu-id="21a8c-2037">hong kong identity card</span></span>
- <span data-ttu-id="21a8c-2038">HKIDC</span><span class="sxs-lookup"><span data-stu-id="21a8c-2038">HKIDC</span></span>
- <span data-ttu-id="21a8c-2039">id card</span><span class="sxs-lookup"><span data-stu-id="21a8c-2039">id card</span></span>
- <span data-ttu-id="21a8c-2040">cartão de identidade</span><span class="sxs-lookup"><span data-stu-id="21a8c-2040">identity card</span></span>
- <span data-ttu-id="21a8c-2041">cartão de identidade HK</span><span class="sxs-lookup"><span data-stu-id="21a8c-2041">hk identity card</span></span>
- <span data-ttu-id="21a8c-2042">ID de Hong Kong</span><span class="sxs-lookup"><span data-stu-id="21a8c-2042">hong kong id</span></span>
- <span data-ttu-id="21a8c-2043">香港身份證</span><span class="sxs-lookup"><span data-stu-id="21a8c-2043">香港身份證</span></span>
- <span data-ttu-id="21a8c-2044">香港永久性居民身份證</span><span class="sxs-lookup"><span data-stu-id="21a8c-2044">香港永久性居民身份證</span></span>
- <span data-ttu-id="21a8c-2045">身份證</span><span class="sxs-lookup"><span data-stu-id="21a8c-2045">身份證</span></span>
- <span data-ttu-id="21a8c-2046">身份証</span><span class="sxs-lookup"><span data-stu-id="21a8c-2046">身份証</span></span>
- <span data-ttu-id="21a8c-2047">身分證</span><span class="sxs-lookup"><span data-stu-id="21a8c-2047">身分證</span></span>
- <span data-ttu-id="21a8c-2048">身分証</span><span class="sxs-lookup"><span data-stu-id="21a8c-2048">身分証</span></span>
- <span data-ttu-id="21a8c-2049">香港身份証</span><span class="sxs-lookup"><span data-stu-id="21a8c-2049">香港身份証</span></span>
- <span data-ttu-id="21a8c-2050">香港身分證</span><span class="sxs-lookup"><span data-stu-id="21a8c-2050">香港身分證</span></span>
- <span data-ttu-id="21a8c-2051">香港身分証</span><span class="sxs-lookup"><span data-stu-id="21a8c-2051">香港身分証</span></span>
- <span data-ttu-id="21a8c-2052">香港身份證</span><span class="sxs-lookup"><span data-stu-id="21a8c-2052">香港身份證</span></span>
- <span data-ttu-id="21a8c-2053">香港居民身份證</span><span class="sxs-lookup"><span data-stu-id="21a8c-2053">香港居民身份證</span></span>
- <span data-ttu-id="21a8c-2054">香港居民身份証</span><span class="sxs-lookup"><span data-stu-id="21a8c-2054">香港居民身份証</span></span>
- <span data-ttu-id="21a8c-2055">香港居民身分證</span><span class="sxs-lookup"><span data-stu-id="21a8c-2055">香港居民身分證</span></span>
- <span data-ttu-id="21a8c-2056">香港居民身分証</span><span class="sxs-lookup"><span data-stu-id="21a8c-2056">香港居民身分証</span></span>
- <span data-ttu-id="21a8c-2057">香港永久性居民身份証</span><span class="sxs-lookup"><span data-stu-id="21a8c-2057">香港永久性居民身份証</span></span>
- <span data-ttu-id="21a8c-2058">香港永久性居民身分證</span><span class="sxs-lookup"><span data-stu-id="21a8c-2058">香港永久性居民身分證</span></span>
- <span data-ttu-id="21a8c-2059">香港永久性居民身分証</span><span class="sxs-lookup"><span data-stu-id="21a8c-2059">香港永久性居民身分証</span></span>
- <span data-ttu-id="21a8c-2060">香港永久性居民身份證</span><span class="sxs-lookup"><span data-stu-id="21a8c-2060">香港永久性居民身份證</span></span>
- <span data-ttu-id="21a8c-2061">香港非永久性居民身份證</span><span class="sxs-lookup"><span data-stu-id="21a8c-2061">香港非永久性居民身份證</span></span>
- <span data-ttu-id="21a8c-2062">香港非永久性居民身份証</span><span class="sxs-lookup"><span data-stu-id="21a8c-2062">香港非永久性居民身份証</span></span>
- <span data-ttu-id="21a8c-2063">香港非永久性居民身分證</span><span class="sxs-lookup"><span data-stu-id="21a8c-2063">香港非永久性居民身分證</span></span>
- <span data-ttu-id="21a8c-2064">香港非永久性居民身分証</span><span class="sxs-lookup"><span data-stu-id="21a8c-2064">香港非永久性居民身分証</span></span>
- <span data-ttu-id="21a8c-2065">香港特別行政區永久性居民身份證</span><span class="sxs-lookup"><span data-stu-id="21a8c-2065">香港特別行政區永久性居民身份證</span></span>
- <span data-ttu-id="21a8c-2066">香港特別行政區永久性居民身份証</span><span class="sxs-lookup"><span data-stu-id="21a8c-2066">香港特別行政區永久性居民身份証</span></span>
- <span data-ttu-id="21a8c-2067">香港特別行政區永久性居民身分證</span><span class="sxs-lookup"><span data-stu-id="21a8c-2067">香港特別行政區永久性居民身分證</span></span>
- <span data-ttu-id="21a8c-2068">香港特別行政區永久性居民身分証</span><span class="sxs-lookup"><span data-stu-id="21a8c-2068">香港特別行政區永久性居民身分証</span></span>
- <span data-ttu-id="21a8c-2069">香港特別行政區非永久性居民身份證</span><span class="sxs-lookup"><span data-stu-id="21a8c-2069">香港特別行政區非永久性居民身份證</span></span>
- <span data-ttu-id="21a8c-2070">香港特別行政區非永久性居民身份証</span><span class="sxs-lookup"><span data-stu-id="21a8c-2070">香港特別行政區非永久性居民身份証</span></span>
- <span data-ttu-id="21a8c-2071">香港特別行政區非永久性居民身分證</span><span class="sxs-lookup"><span data-stu-id="21a8c-2071">香港特別行政區非永久性居民身分證</span></span>
- <span data-ttu-id="21a8c-2072">香港特別行政區非永久性居民身分証</span><span class="sxs-lookup"><span data-stu-id="21a8c-2072">香港特別行政區非永久性居民身分証</span></span>
   
## <a name="india-permanent-account-number-pan"></a><span data-ttu-id="21a8c-2073">Número da Conta Permanente da Índia (PAN)</span><span class="sxs-lookup"><span data-stu-id="21a8c-2073">India Permanent Account Number (PAN)</span></span>

### <a name="format"></a><span data-ttu-id="21a8c-2074">Format</span><span class="sxs-lookup"><span data-stu-id="21a8c-2074">Format</span></span>

<span data-ttu-id="21a8c-2075">10 letras ou dígitos</span><span class="sxs-lookup"><span data-stu-id="21a8c-2075">10 letters or digits</span></span>

### <a name="pattern"></a><span data-ttu-id="21a8c-2076">Padrão</span><span class="sxs-lookup"><span data-stu-id="21a8c-2076">Pattern</span></span>

<span data-ttu-id="21a8c-2077">10 letras ou dígitos.</span><span class="sxs-lookup"><span data-stu-id="21a8c-2077">10 letters or digits:</span></span>
- <span data-ttu-id="21a8c-2078">Cinco letras (não diferenciam maiúsculas de minúsculas)</span><span class="sxs-lookup"><span data-stu-id="21a8c-2078">Five letters (not case sensitive)</span></span> 
- <span data-ttu-id="21a8c-2079">Quatro dígitos</span><span class="sxs-lookup"><span data-stu-id="21a8c-2079">Four digits</span></span> 
- <span data-ttu-id="21a8c-2080">Uma letra que é um dígito de verificação alfabético</span><span class="sxs-lookup"><span data-stu-id="21a8c-2080">A letter which is an alphabetic check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="21a8c-2081">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="21a8c-2081">Checksum</span></span>

<span data-ttu-id="21a8c-2082">Sim</span><span class="sxs-lookup"><span data-stu-id="21a8c-2082">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="21a8c-2083">Definição</span><span class="sxs-lookup"><span data-stu-id="21a8c-2083">Definition</span></span>

<span data-ttu-id="21a8c-2084">Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="21a8c-2084">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="21a8c-2085">A expressão regular Regex_india_permanent_account_number localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="21a8c-2085">The regular expression Regex_india_permanent_account_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="21a8c-2086">Uma palavra-chave de Keyword_india_permanent_account_number for encontrada.</span><span class="sxs-lookup"><span data-stu-id="21a8c-2086">A keyword from Keyword_india_permanent_account_number is found.</span></span>
- <span data-ttu-id="21a8c-2087">A soma de verificação passa.</span><span class="sxs-lookup"><span data-stu-id="21a8c-2087">The checksum passes.</span></span>

```
<!-- India Permanent Account Number -->
<Entity id="2602bfee-9bb0-47a5-a7a6-2bf3053e2804" recommendedConfidence="85" patternsProximity="300">
  <Pattern confidenceLevel="85">
     <IdMatch idRef="Regex_india_permanent_account_number"/>
     <Match idRef="Keyword_india_permanent_account_number"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="21a8c-2088">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="21a8c-2088">Keywords</span></span>

#### <a name="keywordindiapermanentaccountnumber"></a><span data-ttu-id="21a8c-2089">Keyword_india_permanent_account_number</span><span class="sxs-lookup"><span data-stu-id="21a8c-2089">Keyword_india_permanent_account_number</span></span>

- <span data-ttu-id="21a8c-2090">Número da Conta Permanente</span><span class="sxs-lookup"><span data-stu-id="21a8c-2090">Permanent Account Number</span></span> 
- <span data-ttu-id="21a8c-2091">APLICAR</span><span class="sxs-lookup"><span data-stu-id="21a8c-2091">PAN</span></span> 
   
## <a name="india-unique-identification-aadhaar-number"></a><span data-ttu-id="21a8c-2092">Número de Identificação Exclusivo da Índia (Aadhaar)</span><span class="sxs-lookup"><span data-stu-id="21a8c-2092">India Unique Identification (Aadhaar) Number</span></span>

### <a name="format"></a><span data-ttu-id="21a8c-2093">Format</span><span class="sxs-lookup"><span data-stu-id="21a8c-2093">Format</span></span>

<span data-ttu-id="21a8c-2094">12 dígitos contendo espaços opcionais ou traços</span><span class="sxs-lookup"><span data-stu-id="21a8c-2094">12 digits containing optional spaces or dashes</span></span>

### <a name="pattern"></a><span data-ttu-id="21a8c-2095">Padrão</span><span class="sxs-lookup"><span data-stu-id="21a8c-2095">Pattern</span></span>

<span data-ttu-id="21a8c-2096">12 dígitos:</span><span class="sxs-lookup"><span data-stu-id="21a8c-2096">12 digits:</span></span>
- <span data-ttu-id="21a8c-2097">Quatro dígitos</span><span class="sxs-lookup"><span data-stu-id="21a8c-2097">Four digits</span></span> 
- <span data-ttu-id="21a8c-2098">Um espaço ou um traço opcional </span><span class="sxs-lookup"><span data-stu-id="21a8c-2098">An optional space or dash</span></span> 
- <span data-ttu-id="21a8c-2099">Quatro dígitos</span><span class="sxs-lookup"><span data-stu-id="21a8c-2099">Four digits</span></span> 
- <span data-ttu-id="21a8c-2100">Um espaço ou um traço opcional </span><span class="sxs-lookup"><span data-stu-id="21a8c-2100">An optional space or dash</span></span> 
- <span data-ttu-id="21a8c-2101">O dígito final que é o dígito de verificação</span><span class="sxs-lookup"><span data-stu-id="21a8c-2101">The final digit which is the check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="21a8c-2102">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="21a8c-2102">Checksum</span></span>

<span data-ttu-id="21a8c-2103">Sim</span><span class="sxs-lookup"><span data-stu-id="21a8c-2103">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="21a8c-2104">Definição</span><span class="sxs-lookup"><span data-stu-id="21a8c-2104">Definition</span></span>

<span data-ttu-id="21a8c-2105">Uma política de DLP é de 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres: a função Func_india_aadhaar localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="21a8c-2105">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters: The function Func_india_aadhaar finds content that matches the pattern.</span></span>
<span data-ttu-id="21a8c-2106">Uma palavra-chave de Keyword_india_aadhar for encontrada.</span><span class="sxs-lookup"><span data-stu-id="21a8c-2106">A keyword from Keyword_india_aadhar is found.</span></span>
<span data-ttu-id="21a8c-2107">A soma de verificação passa.</span><span class="sxs-lookup"><span data-stu-id="21a8c-2107">The checksum passes.</span></span>
<span data-ttu-id="21a8c-2108">Uma política de DLP é de 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres: a função Func_india_aadhaar localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="21a8c-2108">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters: The function Func_india_aadhaar finds content that matches the pattern.</span></span>
<span data-ttu-id="21a8c-2109">A soma de verificação passa.</span><span class="sxs-lookup"><span data-stu-id="21a8c-2109">The checksum passes.</span></span>
<span data-ttu-id="21a8c-2110"><!-- India Unique Identification (Aadhaar) number -->
<Entity id="1ca46b29-76f5-4f46-9383-cfa15e91048f" recommendedConfidence="85" patternsProximity="300"> <Pattern confidenceLevel="85"> <IdMatch idRef="Func_india_aadhaar"/> <Match idRef="Keyword_india_aadhar"/> </Pattern> <Pattern confidenceLevel="75"> <IdMatch idRef="Func_india_aadhaar"/> </Pattern>
</Entity></span><span class="sxs-lookup"><span data-stu-id="21a8c-2110"></span></span>

### <a name="keywords"></a><span data-ttu-id="21a8c-2111">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="21a8c-2111">Keywords</span></span>
   
#### <a name="keywordindiaaadhar"></a><span data-ttu-id="21a8c-2112">Keyword_india_aadhar</span><span class="sxs-lookup"><span data-stu-id="21a8c-2112">Keyword_india_aadhar</span></span>
- <span data-ttu-id="21a8c-2113">Aadhar</span><span class="sxs-lookup"><span data-stu-id="21a8c-2113">Aadhar</span></span>
- <span data-ttu-id="21a8c-2114">Aadhaar</span><span class="sxs-lookup"><span data-stu-id="21a8c-2114">Aadhaar</span></span>
- <span data-ttu-id="21a8c-2115">UID</span><span class="sxs-lookup"><span data-stu-id="21a8c-2115">UID</span></span>
- <span data-ttu-id="21a8c-2116">आधार</span><span class="sxs-lookup"><span data-stu-id="21a8c-2116">आधार</span></span>
   
## <a name="indonesia-identity-card-ktp-number"></a><span data-ttu-id="21a8c-2117">Número do Cartão de Identidade da Indonésia (KTP)</span><span class="sxs-lookup"><span data-stu-id="21a8c-2117">Indonesia Identity Card (KTP) Number</span></span>

### <a name="format"></a><span data-ttu-id="21a8c-2118">Format</span><span class="sxs-lookup"><span data-stu-id="21a8c-2118">Format</span></span>

<span data-ttu-id="21a8c-2119">16 dígitos contendo pontos opcionais</span><span class="sxs-lookup"><span data-stu-id="21a8c-2119">16 digits containing optional periods</span></span>

### <a name="pattern"></a><span data-ttu-id="21a8c-2120">Padrão</span><span class="sxs-lookup"><span data-stu-id="21a8c-2120">Pattern</span></span>

<span data-ttu-id="21a8c-2121">16 dígitos:</span><span class="sxs-lookup"><span data-stu-id="21a8c-2121">16 digits:</span></span>
- <span data-ttu-id="21a8c-2122">Código de província de dois dígitos </span><span class="sxs-lookup"><span data-stu-id="21a8c-2122">Two-digit province code</span></span> 
- <span data-ttu-id="21a8c-2123">Um ponto (opcional) </span><span class="sxs-lookup"><span data-stu-id="21a8c-2123">A period (optional)</span></span> 
- <span data-ttu-id="21a8c-2124">Código de dois dígitos da regência ou da cidade </span><span class="sxs-lookup"><span data-stu-id="21a8c-2124">Two-digit regency or city code</span></span> 
- <span data-ttu-id="21a8c-2125">Código de dois dígitos do subdistrito </span><span class="sxs-lookup"><span data-stu-id="21a8c-2125">Two-digit subdistrict code</span></span> 
- <span data-ttu-id="21a8c-2126">Um ponto (opcional) </span><span class="sxs-lookup"><span data-stu-id="21a8c-2126">A period (optional)</span></span> 
- <span data-ttu-id="21a8c-2127">Seis dígitos no formato DDMMAA que são a data de nascimento</span><span class="sxs-lookup"><span data-stu-id="21a8c-2127">Six digits in the format DDMMYY which are the date of birth</span></span> 
- <span data-ttu-id="21a8c-2128">Um ponto (opcional) </span><span class="sxs-lookup"><span data-stu-id="21a8c-2128">A period (optional)</span></span> 
- <span data-ttu-id="21a8c-2129">Quatro dígitos</span><span class="sxs-lookup"><span data-stu-id="21a8c-2129">Four digits</span></span>

### <a name="checksum"></a><span data-ttu-id="21a8c-2130">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="21a8c-2130">Checksum</span></span>

<span data-ttu-id="21a8c-2131">Não</span><span class="sxs-lookup"><span data-stu-id="21a8c-2131">No</span></span>

### <a name="definition"></a><span data-ttu-id="21a8c-2132">Definição</span><span class="sxs-lookup"><span data-stu-id="21a8c-2132">Definition</span></span>

<span data-ttu-id="21a8c-2133">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="21a8c-2133">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="21a8c-2134">A expressão regular Regex_indonesia_id_card localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="21a8c-2134">The regular expression Regex_indonesia_id_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="21a8c-2135">Uma palavra-chave de Keyword_indonesia_id_card for encontrada.</span><span class="sxs-lookup"><span data-stu-id="21a8c-2135">A keyword from Keyword_indonesia_id_card is found.</span></span>

<span data-ttu-id="21a8c-2136">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="21a8c-2136">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="21a8c-2137">A expressão regular Regex_indonesia_id_card localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="21a8c-2137">The regular expression Regex_indonesia_id_card finds content that matches the pattern.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="21a8c-2138">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="21a8c-2138">Keywords</span></span>
   
#### <a name="keywordindonesiaidcard"></a><span data-ttu-id="21a8c-2139">Keyword_indonesia_id_card</span><span class="sxs-lookup"><span data-stu-id="21a8c-2139">Keyword_indonesia_id_card</span></span>

- <span data-ttu-id="21a8c-2140">KTP</span><span class="sxs-lookup"><span data-stu-id="21a8c-2140">KTP</span></span>
- <span data-ttu-id="21a8c-2141">Kartu Tanda Penduduk</span><span class="sxs-lookup"><span data-stu-id="21a8c-2141">Kartu Tanda Penduduk</span></span> 
- <span data-ttu-id="21a8c-2142">Nomor Induk Kependudukan</span><span class="sxs-lookup"><span data-stu-id="21a8c-2142">Nomor Induk Kependudukan</span></span> 
   
## <a name="international-banking-account-number-iban"></a><span data-ttu-id="21a8c-2143">Número da Conta Bancária Internacional (IBAN)</span><span class="sxs-lookup"><span data-stu-id="21a8c-2143">International Banking Account Number (IBAN)</span></span>

### <a name="format"></a><span data-ttu-id="21a8c-2144">Format</span><span class="sxs-lookup"><span data-stu-id="21a8c-2144">Format</span></span>

<span data-ttu-id="21a8c-2145">Código do país (duas letras) mais dígitos de verificação (dois dígitos) mais Bban número (até 30 caracteres)</span><span class="sxs-lookup"><span data-stu-id="21a8c-2145">Country code (two letters) plus check digits (two digits) plus bban number (up to 30 characters)</span></span>

### <a name="pattern"></a><span data-ttu-id="21a8c-2146">Padrão</span><span class="sxs-lookup"><span data-stu-id="21a8c-2146">Pattern</span></span>

<span data-ttu-id="21a8c-2147">O padrão deve incluir todos os seguintes itens:</span><span class="sxs-lookup"><span data-stu-id="21a8c-2147">Pattern must include all of the following:</span></span>

- <span data-ttu-id="21a8c-2148">Código de país de duas letras</span><span class="sxs-lookup"><span data-stu-id="21a8c-2148">Two-letter country code</span></span>
- <span data-ttu-id="21a8c-2149">Dois dígitos de verificação (seguidos por um espaço opcional)</span><span class="sxs-lookup"><span data-stu-id="21a8c-2149">Two check digits (followed by an optional space)</span></span> 
- <span data-ttu-id="21a8c-2150">1-7 grupos de quatro letras ou dígitos (podem ser separados por espaços)</span><span class="sxs-lookup"><span data-stu-id="21a8c-2150">1-7 groups of four letters or digits (can be separated by spaces)</span></span>
- <span data-ttu-id="21a8c-2151">1 a 3 letras ou dígitos</span><span class="sxs-lookup"><span data-stu-id="21a8c-2151">1-3 letters or digits</span></span>

<span data-ttu-id="21a8c-2152">O formato de cada país é um pouco diferente.</span><span class="sxs-lookup"><span data-stu-id="21a8c-2152">The format for each country is slightly different.</span></span> <span data-ttu-id="21a8c-2153">O tipo de informação confidencial do IBAN cobre estes 60 países:</span><span class="sxs-lookup"><span data-stu-id="21a8c-2153">The IBAN sensitive information type covers these 60 countries:</span></span>

<span data-ttu-id="21a8c-2154">AD, AE, Al, at, AZ, BA, be, BG, BH, ch, CR, Cy, cz, de, DK, do, EE, es, Fi, fo, FR, GB, GE, GI, GL, GR, HR, Hu, IE, Il, se,-, KZ, lb, li, o (a) e o (a) , NL, no, pl, pt, Ro, RS, SA, se, si, SK, SM, TN, TR, VG</span><span class="sxs-lookup"><span data-stu-id="21a8c-2154">ad, ae, al, at, az, ba, be, bg, bh, ch, cr, cy, cz, de, dk, do, ee, es, fi, fo, fr, gb, ge, gi, gl, gr, hr, hu, ie, il, is, it, kw, kz, lb, li, lt, lu, lv, mc, md, me, mk, mr, mt, mu, nl, no, pl, pt, ro, rs, sa, se, si, sk, sm, tn, tr, vg</span></span>

### <a name="checksum"></a><span data-ttu-id="21a8c-2155">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="21a8c-2155">Checksum</span></span>

<span data-ttu-id="21a8c-2156">Sim</span><span class="sxs-lookup"><span data-stu-id="21a8c-2156">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="21a8c-2157">Definição</span><span class="sxs-lookup"><span data-stu-id="21a8c-2157">Definition</span></span>

<span data-ttu-id="21a8c-2158">Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="21a8c-2158">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="21a8c-2159">A função Func_iban localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="21a8c-2159">The function Func_iban finds content that matches the pattern.</span></span>
- <span data-ttu-id="21a8c-2160">A soma de verificação passa.</span><span class="sxs-lookup"><span data-stu-id="21a8c-2160">The checksum passes.</span></span>

```
<Entity id="e7dc4711-11b7-4cb0-b88b-2c394a771f0e" patternsProximity="300" recommendedConfidence="85">
  <Pattern confidenceLevel="85">
        <IdMatch idRef="Func_iban" />
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="21a8c-2161">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="21a8c-2161">Keywords</span></span>

<span data-ttu-id="21a8c-2162">Nenhum</span><span class="sxs-lookup"><span data-stu-id="21a8c-2162">None</span></span>

   
## <a name="ip-address"></a><span data-ttu-id="21a8c-2163">Endereço IP</span><span class="sxs-lookup"><span data-stu-id="21a8c-2163">IP Address</span></span>

### <a name="format"></a><span data-ttu-id="21a8c-2164">Format</span><span class="sxs-lookup"><span data-stu-id="21a8c-2164">Format</span></span>

#### <a name="ipv4"></a><span data-ttu-id="21a8c-2165">IPv4</span><span class="sxs-lookup"><span data-stu-id="21a8c-2165">IPv4:</span></span>
<span data-ttu-id="21a8c-2166">Padrão complexo que é responsável por versões formatadas (pontos) e não formatadas (sem pontos) dos endereços IPv4</span><span class="sxs-lookup"><span data-stu-id="21a8c-2166">Complex pattern which accounts for formatted (periods) and unformatted (no periods) versions of the IPv4 addresses</span></span>

#### <a name="ipv6"></a><span data-ttu-id="21a8c-2167">IPv6</span><span class="sxs-lookup"><span data-stu-id="21a8c-2167">IPv6:</span></span>
<span data-ttu-id="21a8c-2168">Padrão complexo que é responsável por números IPv6 formatados (que incluem dois pontos)</span><span class="sxs-lookup"><span data-stu-id="21a8c-2168">Complex pattern which accounts for formatted IPv6 numbers (which include colons)</span></span>

### <a name="pattern"></a><span data-ttu-id="21a8c-2169">Padrão</span><span class="sxs-lookup"><span data-stu-id="21a8c-2169">Pattern</span></span>

### <a name="checksum"></a><span data-ttu-id="21a8c-2170">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="21a8c-2170">Checksum</span></span>

<span data-ttu-id="21a8c-2171">Não</span><span class="sxs-lookup"><span data-stu-id="21a8c-2171">No</span></span>

### <a name="definition"></a><span data-ttu-id="21a8c-2172">Definição</span><span class="sxs-lookup"><span data-stu-id="21a8c-2172">Definition</span></span>

<span data-ttu-id="21a8c-2173">Para IPv6, uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="21a8c-2173">For IPv6, a DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="21a8c-2174">A expressão regular Regex_ipv6_address localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="21a8c-2174">The regular expression Regex_ipv6_address finds content that matches the pattern.</span></span>
- <span data-ttu-id="21a8c-2175">Nenhuma palavra-chave de Keyword_ipaddress for encontrada.</span><span class="sxs-lookup"><span data-stu-id="21a8c-2175">No keyword from Keyword_ipaddress is found.</span></span>

<span data-ttu-id="21a8c-2176">Para IPv4, uma política de DLP tem 95% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="21a8c-2176">For IPv4, a DLP policy is 95% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="21a8c-2177">A expressão regular Regex_ipv4_address localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="21a8c-2177">The regular expression Regex_ipv4_address finds content that matches the pattern.</span></span>
- <span data-ttu-id="21a8c-2178">Uma palavra-chave de Keyword_ipaddress for encontrada.</span><span class="sxs-lookup"><span data-stu-id="21a8c-2178">A keyword from Keyword_ipaddress is found.</span></span>

<span data-ttu-id="21a8c-2179">Para IPv6, uma política de DLP tem 95% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="21a8c-2179">For IPv6, a DLP policy is 95% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="21a8c-2180">A expressão regular Regex_ipv6_address localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="21a8c-2180">The regular expression Regex_ipv6_address finds content that matches the pattern.</span></span>
- <span data-ttu-id="21a8c-2181">Nenhuma palavra-chave de Keyword_ipaddress for encontrada.</span><span class="sxs-lookup"><span data-stu-id="21a8c-2181">No keyword from Keyword_ipaddress is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="21a8c-2182">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="21a8c-2182">Keywords</span></span>

#### <a name="keywordipaddress"></a><span data-ttu-id="21a8c-2183">Keyword_ipaddress</span><span class="sxs-lookup"><span data-stu-id="21a8c-2183">Keyword_ipaddress</span></span>

- <span data-ttu-id="21a8c-2184">IP (esta palavra-chave diferencia maiúsculas de minúsculas)</span><span class="sxs-lookup"><span data-stu-id="21a8c-2184">IP (this keyword is case sensitive)</span></span>
- <span data-ttu-id="21a8c-2185">ip address</span><span class="sxs-lookup"><span data-stu-id="21a8c-2185">ip address</span></span> 
- <span data-ttu-id="21a8c-2186">endereços ip</span><span class="sxs-lookup"><span data-stu-id="21a8c-2186">ip addresses</span></span>
- <span data-ttu-id="21a8c-2187">internet protocol</span><span class="sxs-lookup"><span data-stu-id="21a8c-2187">internet protocol</span></span>
- <span data-ttu-id="21a8c-2188">IP כתובת ה</span><span class="sxs-lookup"><span data-stu-id="21a8c-2188">IP-כתובת ה</span></span> 
   
## <a name="international-classification-of-diseases-icd-10-cm"></a><span data-ttu-id="21a8c-2189">Classificação internacional do Diseases (ICD-10-CM)</span><span class="sxs-lookup"><span data-stu-id="21a8c-2189">International Classification of Diseases (ICD-10-CM)</span></span>

### <a name="format"></a><span data-ttu-id="21a8c-2190">Format</span><span class="sxs-lookup"><span data-stu-id="21a8c-2190">Format</span></span>

<span data-ttu-id="21a8c-2191">Dictionary</span><span class="sxs-lookup"><span data-stu-id="21a8c-2191">Dictionary</span></span>

### <a name="pattern"></a><span data-ttu-id="21a8c-2192">Padrão</span><span class="sxs-lookup"><span data-stu-id="21a8c-2192">Pattern</span></span>

<span data-ttu-id="21a8c-2193">Palavra-chave</span><span class="sxs-lookup"><span data-stu-id="21a8c-2193">Keyword</span></span>

### <a name="checksum"></a><span data-ttu-id="21a8c-2194">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="21a8c-2194">Checksum</span></span>

<span data-ttu-id="21a8c-2195">Não</span><span class="sxs-lookup"><span data-stu-id="21a8c-2195">No</span></span>

### <a name="definition"></a><span data-ttu-id="21a8c-2196">Definição</span><span class="sxs-lookup"><span data-stu-id="21a8c-2196">Definition</span></span>

<span data-ttu-id="21a8c-2197">Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="21a8c-2197">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="21a8c-2198">Uma palavra-chave de Dictionary_icd_10_cm for encontrada.</span><span class="sxs-lookup"><span data-stu-id="21a8c-2198">A keyword from Dictionary_icd_10_cm is found.</span></span>

```
      <!-- ICD-10 CM -->
      <Entity id="3356946c-6bb7-449b-b253-6ffa419c0ce7" patternsProximity="300" recommendedConfidence="85">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Dictionary_icd_10_cm" />
        </Pattern>
      </Entity>
```

<span data-ttu-id="21a8c-2199">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="21a8c-2199">Keywords</span></span>

<span data-ttu-id="21a8c-2200">Qualquer termo do dicionário de palavra-chave Dictionary_icd_10_cm, que se baseia na [classificação internacional do Diseases, décimo revisão, modificação clínica (ICD-10-cm)](https://go.microsoft.com/fwlink/?linkid=852604).</span><span class="sxs-lookup"><span data-stu-id="21a8c-2200">Any term from the Dictionary_icd_10_cm keyword dictionary, which is based on the [International Classification of Diseases, Tenth Revision, Clinical Modification (ICD-10-CM)](https://go.microsoft.com/fwlink/?linkid=852604).</span></span> <span data-ttu-id="21a8c-2201">Esse tipo procura apenas o termo, não os códigos de seguro.</span><span class="sxs-lookup"><span data-stu-id="21a8c-2201">This type looks only for the term, not the insurance codes.</span></span>

   
## <a name="international-classification-of-diseases-icd-9-cm"></a><span data-ttu-id="21a8c-2202">Classificação internacional do Diseases (ICD-9-CM)</span><span class="sxs-lookup"><span data-stu-id="21a8c-2202">International Classification of Diseases (ICD-9-CM)</span></span>

### <a name="format"></a><span data-ttu-id="21a8c-2203">Format</span><span class="sxs-lookup"><span data-stu-id="21a8c-2203">Format</span></span>

<span data-ttu-id="21a8c-2204">Dictionary</span><span class="sxs-lookup"><span data-stu-id="21a8c-2204">Dictionary</span></span>

### <a name="pattern"></a><span data-ttu-id="21a8c-2205">Padrão</span><span class="sxs-lookup"><span data-stu-id="21a8c-2205">Pattern</span></span>

<span data-ttu-id="21a8c-2206">Palavra-chave</span><span class="sxs-lookup"><span data-stu-id="21a8c-2206">Keyword</span></span>

### <a name="checksum"></a><span data-ttu-id="21a8c-2207">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="21a8c-2207">Checksum</span></span>

<span data-ttu-id="21a8c-2208">Não</span><span class="sxs-lookup"><span data-stu-id="21a8c-2208">No</span></span>

### <a name="definition"></a><span data-ttu-id="21a8c-2209">Definição</span><span class="sxs-lookup"><span data-stu-id="21a8c-2209">Definition</span></span>

<span data-ttu-id="21a8c-2210">Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="21a8c-2210">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="21a8c-2211">Uma palavra-chave de Dictionary_icd_9_cm for encontrada.</span><span class="sxs-lookup"><span data-stu-id="21a8c-2211">A keyword from Dictionary_icd_9_cm is found.</span></span>

```
      <Entity id="fa3f9c74-ee07-4c52-b5f2-085d6b2c0ec4" patternsProximity="300" recommendedConfidence="85">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Dictionary_icd_9_cm" />
        </Pattern>
      </Entity>
```

### <a name="keywords"></a><span data-ttu-id="21a8c-2212">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="21a8c-2212">Keywords</span></span>

<span data-ttu-id="21a8c-2213">Qualquer termo do dicionário de palavra-chave Dictionary_icd_9_cm, que se baseia na [classificação internacional do Diseases, Nona revisão, modificação clínica (ICD-9-cm)](https://go.microsoft.com/fwlink/?linkid=852605).</span><span class="sxs-lookup"><span data-stu-id="21a8c-2213">Any term from the Dictionary_icd_9_cm keyword dictionary, which is based on the [International Classification of Diseases,Ninth Revision, Clinical Modification (ICD-9-CM)](https://go.microsoft.com/fwlink/?linkid=852605).</span></span> <span data-ttu-id="21a8c-2214">Esse tipo procura apenas o termo, não os códigos de seguro.</span><span class="sxs-lookup"><span data-stu-id="21a8c-2214">This type looks only for the term, not the insurance codes.</span></span>
   
## <a name="ireland-personal-public-service-pps-number"></a><span data-ttu-id="21a8c-2215">Número de Serviço Público Pessoal (PPS) da Irlanda</span><span class="sxs-lookup"><span data-stu-id="21a8c-2215">Ireland Personal Public Service (PPS) Number</span></span>

### <a name="format"></a><span data-ttu-id="21a8c-2216">Format</span><span class="sxs-lookup"><span data-stu-id="21a8c-2216">Format</span></span>

<span data-ttu-id="21a8c-2217">Formato antigo (até 31 de dezembro de 2012):</span><span class="sxs-lookup"><span data-stu-id="21a8c-2217">Old format (until 31 Dec 2012):</span></span>
- <span data-ttu-id="21a8c-2218">Sete dígitos seguidos de 1 a 2 letras </span><span class="sxs-lookup"><span data-stu-id="21a8c-2218">Seven digits followed by 1-2 letters</span></span> 

<span data-ttu-id="21a8c-2219">Novo formato (1 Jan 2013 e posterior):</span><span class="sxs-lookup"><span data-stu-id="21a8c-2219">New format (1 Jan 2013 and after):</span></span>
- <span data-ttu-id="21a8c-2220">Sete dígitos seguidos de duas letras</span><span class="sxs-lookup"><span data-stu-id="21a8c-2220">Seven digits followed by two letters</span></span>

### <a name="pattern"></a><span data-ttu-id="21a8c-2221">Padrão</span><span class="sxs-lookup"><span data-stu-id="21a8c-2221">Pattern</span></span>

<span data-ttu-id="21a8c-2222">Formato antigo (até 31 de dezembro de 2012):</span><span class="sxs-lookup"><span data-stu-id="21a8c-2222">Old format (until 31 Dec 2012):</span></span>
- <span data-ttu-id="21a8c-2223">Sete dígitos </span><span class="sxs-lookup"><span data-stu-id="21a8c-2223">Seven digits</span></span> 
- <span data-ttu-id="21a8c-2224">1 a 2 letras (não diferenciam maiúsculas de minúsculas)</span><span class="sxs-lookup"><span data-stu-id="21a8c-2224">1-2 letters (not case sensitive)</span></span> 

<span data-ttu-id="21a8c-2225">Novo formato (1 Jan 2013 e posterior):</span><span class="sxs-lookup"><span data-stu-id="21a8c-2225">New format (1 Jan 2013 and after):</span></span>
- <span data-ttu-id="21a8c-2226">Sete dígitos </span><span class="sxs-lookup"><span data-stu-id="21a8c-2226">Seven digits</span></span> 
- <span data-ttu-id="21a8c-2227">Uma letra (não diferencia maiúsculas de minúsculas) que é um dígito de verificação alfabético </span><span class="sxs-lookup"><span data-stu-id="21a8c-2227">A letter (not case sensitive) which is an alphabetic check digit</span></span> 
- <span data-ttu-id="21a8c-2228">A letra "A" ou "H" (não diferencia maiúsculas de minúsculas)</span><span class="sxs-lookup"><span data-stu-id="21a8c-2228">The letter "A" or "H" (not case sensitive)</span></span>

### <a name="checksum"></a><span data-ttu-id="21a8c-2229">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="21a8c-2229">Checksum</span></span>

<span data-ttu-id="21a8c-2230">Sim</span><span class="sxs-lookup"><span data-stu-id="21a8c-2230">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="21a8c-2231">Definição</span><span class="sxs-lookup"><span data-stu-id="21a8c-2231">Definition</span></span>

<span data-ttu-id="21a8c-2232">Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="21a8c-2232">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="21a8c-2233">A função Func_ireland_pps localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="21a8c-2233">The function Func_ireland_pps finds content that matches the pattern.</span></span>
- <span data-ttu-id="21a8c-2234">Uma das seguintes opções for verdadeira:</span><span class="sxs-lookup"><span data-stu-id="21a8c-2234">One of the following is true:</span></span>
    - <span data-ttu-id="21a8c-2235">Uma palavra-chave de Keyword_ireland_pps for encontrada.</span><span class="sxs-lookup"><span data-stu-id="21a8c-2235">A keyword from Keyword_ireland_pps is found.</span></span>
    - <span data-ttu-id="21a8c-2236">A função Func_eu_date encontra uma data no formato de data à direita.</span><span class="sxs-lookup"><span data-stu-id="21a8c-2236">The function Func_eu_date finds a date in the right date format.</span></span>
- <span data-ttu-id="21a8c-2237">A soma de verificação passa.</span><span class="sxs-lookup"><span data-stu-id="21a8c-2237">The checksum passes.</span></span>

<span data-ttu-id="21a8c-2238">Uma política de DLP tem 65% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="21a8c-2238">A DLP policy is 65% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="21a8c-2239">A função Func_ireland_pps localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="21a8c-2239">The function Func_ireland_pps finds content that matches the pattern.</span></span>
- <span data-ttu-id="21a8c-2240">A soma de verificação passa.</span><span class="sxs-lookup"><span data-stu-id="21a8c-2240">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="21a8c-2241">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="21a8c-2241">Keywords</span></span>

#### <a name="keywordirelandpps"></a><span data-ttu-id="21a8c-2242">Keyword_ireland_pps</span><span class="sxs-lookup"><span data-stu-id="21a8c-2242">Keyword_ireland_pps</span></span>

- <span data-ttu-id="21a8c-2243">Número do Serviço Público Pessoal</span><span class="sxs-lookup"><span data-stu-id="21a8c-2243">Personal Public Service Number</span></span> 
- <span data-ttu-id="21a8c-2244">Número PPS</span><span class="sxs-lookup"><span data-stu-id="21a8c-2244">PPS Number</span></span> 
- <span data-ttu-id="21a8c-2245">Núm PPS</span><span class="sxs-lookup"><span data-stu-id="21a8c-2245">PPS Num</span></span> 
- <span data-ttu-id="21a8c-2246">Nº PPS</span><span class="sxs-lookup"><span data-stu-id="21a8c-2246">PPS No.</span></span> 
- <span data-ttu-id="21a8c-2247"># PPS</span><span class="sxs-lookup"><span data-stu-id="21a8c-2247">PPS #</span></span> 
- <span data-ttu-id="21a8c-2248">PPS</span><span class="sxs-lookup"><span data-stu-id="21a8c-2248">PPS#</span></span> 
- <span data-ttu-id="21a8c-2249">PPSN</span><span class="sxs-lookup"><span data-stu-id="21a8c-2249">PPSN</span></span> 
- <span data-ttu-id="21a8c-2250">Cartão dos Serviços Públicos</span><span class="sxs-lookup"><span data-stu-id="21a8c-2250">Public Services Card</span></span> 
- <span data-ttu-id="21a8c-2251">Uimhir Phearsanta Seirbhíse Poiblí</span><span class="sxs-lookup"><span data-stu-id="21a8c-2251">Uimhir Phearsanta Seirbhíse Poiblí</span></span> 
- <span data-ttu-id="21a8c-2252">Uimh.</span><span class="sxs-lookup"><span data-stu-id="21a8c-2252">Uimh.</span></span> <span data-ttu-id="21a8c-2253">PSP</span><span class="sxs-lookup"><span data-stu-id="21a8c-2253">PSP</span></span> 
- <span data-ttu-id="21a8c-2254">PSP</span><span class="sxs-lookup"><span data-stu-id="21a8c-2254">PSP</span></span> 
   
## <a name="israel-bank-account-number"></a><span data-ttu-id="21a8c-2255">Número de conta bancária de Israel</span><span class="sxs-lookup"><span data-stu-id="21a8c-2255">Israel Bank Account Number</span></span>

### <a name="format"></a><span data-ttu-id="21a8c-2256">Format</span><span class="sxs-lookup"><span data-stu-id="21a8c-2256">Format</span></span>

<span data-ttu-id="21a8c-2257">13 dígitos</span><span class="sxs-lookup"><span data-stu-id="21a8c-2257">13 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="21a8c-2258">Padrão</span><span class="sxs-lookup"><span data-stu-id="21a8c-2258">Pattern</span></span>

<span data-ttu-id="21a8c-2259">Binário</span><span class="sxs-lookup"><span data-stu-id="21a8c-2259">Formatted:</span></span>
- <span data-ttu-id="21a8c-2260">Dois dígitos</span><span class="sxs-lookup"><span data-stu-id="21a8c-2260">Two digits</span></span> 
- <span data-ttu-id="21a8c-2261">Um traço</span><span class="sxs-lookup"><span data-stu-id="21a8c-2261">A dash</span></span> 
- <span data-ttu-id="21a8c-2262">Três dígitos</span><span class="sxs-lookup"><span data-stu-id="21a8c-2262">Three digits</span></span> 
- <span data-ttu-id="21a8c-2263">Um traço</span><span class="sxs-lookup"><span data-stu-id="21a8c-2263">A dash</span></span> 
- <span data-ttu-id="21a8c-2264">Oito dígitos</span><span class="sxs-lookup"><span data-stu-id="21a8c-2264">Eight digits</span></span>

<span data-ttu-id="21a8c-2265">Não formatado</span><span class="sxs-lookup"><span data-stu-id="21a8c-2265">Unformatted:</span></span>
- <span data-ttu-id="21a8c-2266">13 dígitos consecutivos</span><span class="sxs-lookup"><span data-stu-id="21a8c-2266">13 consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="21a8c-2267">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="21a8c-2267">Checksum</span></span>

<span data-ttu-id="21a8c-2268">Não</span><span class="sxs-lookup"><span data-stu-id="21a8c-2268">No</span></span>

### <a name="definition"></a><span data-ttu-id="21a8c-2269">Definição</span><span class="sxs-lookup"><span data-stu-id="21a8c-2269">Definition</span></span>

<span data-ttu-id="21a8c-2270">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="21a8c-2270">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="21a8c-2271">A expressão regular Regex_israel_bank_account_number localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="21a8c-2271">The regular expression Regex_israel_bank_account_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="21a8c-2272">Uma palavra-chave de Keyword_israel_bank_account_number for encontrada.</span><span class="sxs-lookup"><span data-stu-id="21a8c-2272">A keyword from Keyword_israel_bank_account_number is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="21a8c-2273">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="21a8c-2273">Keywords</span></span>

#### <a name="keywordisraelbankaccountnumber"></a><span data-ttu-id="21a8c-2274">Keyword_israel_bank_account_number</span><span class="sxs-lookup"><span data-stu-id="21a8c-2274">Keyword_israel_bank_account_number</span></span>

- <span data-ttu-id="21a8c-2275">Bank Account Number</span><span class="sxs-lookup"><span data-stu-id="21a8c-2275">Bank Account Number</span></span> 
- <span data-ttu-id="21a8c-2276">Bank Account</span><span class="sxs-lookup"><span data-stu-id="21a8c-2276">Bank Account</span></span> 
- <span data-ttu-id="21a8c-2277">Account Number</span><span class="sxs-lookup"><span data-stu-id="21a8c-2277">Account Number</span></span> 
- <span data-ttu-id="21a8c-2278">מספר חשבון בנק</span><span class="sxs-lookup"><span data-stu-id="21a8c-2278">מספר חשבון בנק</span></span> 
   
## <a name="israel-national-id"></a><span data-ttu-id="21a8c-2279">ID nacional de Israel</span><span class="sxs-lookup"><span data-stu-id="21a8c-2279">Israel National ID</span></span>

### <a name="format"></a><span data-ttu-id="21a8c-2280">Format</span><span class="sxs-lookup"><span data-stu-id="21a8c-2280">Format</span></span>

<span data-ttu-id="21a8c-2281">Nove dígitos</span><span class="sxs-lookup"><span data-stu-id="21a8c-2281">Nine digits</span></span>

### <a name="pattern"></a><span data-ttu-id="21a8c-2282">Padrão</span><span class="sxs-lookup"><span data-stu-id="21a8c-2282">Pattern</span></span>

<span data-ttu-id="21a8c-2283">Nove dígitos consecutivos</span><span class="sxs-lookup"><span data-stu-id="21a8c-2283">Nine consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="21a8c-2284">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="21a8c-2284">Checksum</span></span>

<span data-ttu-id="21a8c-2285">Sim</span><span class="sxs-lookup"><span data-stu-id="21a8c-2285">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="21a8c-2286">Definição</span><span class="sxs-lookup"><span data-stu-id="21a8c-2286">Definition</span></span>

<span data-ttu-id="21a8c-2287">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="21a8c-2287">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="21a8c-2288">A função Func_israeli_national_id_number localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="21a8c-2288">The function Func_israeli_national_id_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="21a8c-2289">Uma palavra-chave de Keyword_Israel_National_ID for encontrada.</span><span class="sxs-lookup"><span data-stu-id="21a8c-2289">A keyword from Keyword_Israel_National_ID is found.</span></span>
- <span data-ttu-id="21a8c-2290">A soma de verificação passa.</span><span class="sxs-lookup"><span data-stu-id="21a8c-2290">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="21a8c-2291">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="21a8c-2291">Keywords</span></span>

#### <a name="keywordisraelnationalid"></a><span data-ttu-id="21a8c-2292">Keyword_Israel_National_ID</span><span class="sxs-lookup"><span data-stu-id="21a8c-2292">Keyword_Israel_National_ID</span></span>

- <span data-ttu-id="21a8c-2293">מספר זהות</span><span class="sxs-lookup"><span data-stu-id="21a8c-2293">מספר זהות</span></span> 
- <span data-ttu-id="21a8c-2294">Número de identificação nacional</span><span class="sxs-lookup"><span data-stu-id="21a8c-2294">National ID Number</span></span>
   
## <a name="italy-drivers-license-number"></a><span data-ttu-id="21a8c-2295">Número de carteira de motorista da Itália</span><span class="sxs-lookup"><span data-stu-id="21a8c-2295">Italy Driver's License Number</span></span>

### <a name="format"></a><span data-ttu-id="21a8c-2296">Format</span><span class="sxs-lookup"><span data-stu-id="21a8c-2296">Format</span></span>

<span data-ttu-id="21a8c-2297">Uma combinação de 10 letras e dígitos</span><span class="sxs-lookup"><span data-stu-id="21a8c-2297">A combination of 10 letters and digits</span></span>

### <a name="pattern"></a><span data-ttu-id="21a8c-2298">Padrão</span><span class="sxs-lookup"><span data-stu-id="21a8c-2298">Pattern</span></span>

- <span data-ttu-id="21a8c-2299">Uma combinação de 10 letras e dígitos:</span><span class="sxs-lookup"><span data-stu-id="21a8c-2299">A combination of 10 letters and digits:</span></span>
- <span data-ttu-id="21a8c-2300">Uma letra (não diferencia maiúscula de minúscula)</span><span class="sxs-lookup"><span data-stu-id="21a8c-2300">One letter (not case sensitive)</span></span> 
- <span data-ttu-id="21a8c-2301">A letra "A" ou "V" (não diferencia maiúscula de minúscula)</span><span class="sxs-lookup"><span data-stu-id="21a8c-2301">The letter "A" or "V" (not case sensitive)</span></span> 
- <span data-ttu-id="21a8c-2302">Sete letras (não diferenciam maiúsculas de minúsculas), dígitos ou o caractere de sublinhado</span><span class="sxs-lookup"><span data-stu-id="21a8c-2302">Seven letters (not case sensitive), digits, or the underscore character</span></span> 
- <span data-ttu-id="21a8c-2303">Uma letra (não diferencia maiúscula de minúscula)</span><span class="sxs-lookup"><span data-stu-id="21a8c-2303">One letter (not case sensitive)</span></span>

### <a name="checksum"></a><span data-ttu-id="21a8c-2304">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="21a8c-2304">Checksum</span></span>

<span data-ttu-id="21a8c-2305">Não</span><span class="sxs-lookup"><span data-stu-id="21a8c-2305">No</span></span>

### <a name="definition"></a><span data-ttu-id="21a8c-2306">Definição</span><span class="sxs-lookup"><span data-stu-id="21a8c-2306">Definition</span></span>

<span data-ttu-id="21a8c-2307">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="21a8c-2307">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="21a8c-2308">A expressão regular Regex_italy_drivers_license_number localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="21a8c-2308">The regular expression Regex_italy_drivers_license_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="21a8c-2309">Uma palavra-chave de Keyword_italy_drivers_license_number for encontrada.</span><span class="sxs-lookup"><span data-stu-id="21a8c-2309">A keyword from Keyword_italy_drivers_license_number is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="21a8c-2310">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="21a8c-2310">Keywords</span></span>

#### <a name="keyworditalydriverslicensenumber"></a><span data-ttu-id="21a8c-2311">Keyword_italy_drivers_license_number</span><span class="sxs-lookup"><span data-stu-id="21a8c-2311">Keyword_italy_drivers_license_number</span></span>

- <span data-ttu-id="21a8c-2312">numero di patente di guida</span><span class="sxs-lookup"><span data-stu-id="21a8c-2312">numero di patente di guida</span></span> 
- <span data-ttu-id="21a8c-2313">patente di guida</span><span class="sxs-lookup"><span data-stu-id="21a8c-2313">patente di guida</span></span> 
   
## <a name="japan-bank-account-number"></a><span data-ttu-id="21a8c-2314">Número de conta bancária do Japão</span><span class="sxs-lookup"><span data-stu-id="21a8c-2314">Japan Bank Account Number</span></span>

### <a name="format"></a><span data-ttu-id="21a8c-2315">Format</span><span class="sxs-lookup"><span data-stu-id="21a8c-2315">Format</span></span>

<span data-ttu-id="21a8c-2316">Sete ou oito dígitos</span><span class="sxs-lookup"><span data-stu-id="21a8c-2316">Seven or eight digits</span></span>

### <a name="pattern"></a><span data-ttu-id="21a8c-2317">Padrão</span><span class="sxs-lookup"><span data-stu-id="21a8c-2317">Pattern</span></span>

<span data-ttu-id="21a8c-2318">Número da Conta Bancária:</span><span class="sxs-lookup"><span data-stu-id="21a8c-2318">Bank account number:</span></span>
- <span data-ttu-id="21a8c-2319">Sete ou oito dígitos</span><span class="sxs-lookup"><span data-stu-id="21a8c-2319">Seven or eight digits</span></span>
- <span data-ttu-id="21a8c-2320">Código da agência de conta bancária:</span><span class="sxs-lookup"><span data-stu-id="21a8c-2320">Bank account branch code:</span></span>
- <span data-ttu-id="21a8c-2321">Quatro dígitos</span><span class="sxs-lookup"><span data-stu-id="21a8c-2321">Four digits</span></span> 
- <span data-ttu-id="21a8c-2322">Um espaço ou um traço (opcional)</span><span class="sxs-lookup"><span data-stu-id="21a8c-2322">A space or dash (optional)</span></span> 
- <span data-ttu-id="21a8c-2323">Três dígitos</span><span class="sxs-lookup"><span data-stu-id="21a8c-2323">Three digits</span></span>

<span data-ttu-id="21a8c-2324">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="21a8c-2324">Checksum</span></span>

<span data-ttu-id="21a8c-2325">Não</span><span class="sxs-lookup"><span data-stu-id="21a8c-2325">No</span></span>

### <a name="definition"></a><span data-ttu-id="21a8c-2326">Definição</span><span class="sxs-lookup"><span data-stu-id="21a8c-2326">Definition</span></span>

<span data-ttu-id="21a8c-2327">Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="21a8c-2327">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="21a8c-2328">A função Func_jp_bank_account localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="21a8c-2328">The function Func_jp_bank_account finds content that matches the pattern.</span></span>
- <span data-ttu-id="21a8c-2329">Uma palavra-chave de Keyword_jp_bank_account for encontrada.</span><span class="sxs-lookup"><span data-stu-id="21a8c-2329">A keyword from Keyword_jp_bank_account is found.</span></span>
- <span data-ttu-id="21a8c-2330">Uma das seguintes opções for verdadeira:</span><span class="sxs-lookup"><span data-stu-id="21a8c-2330">One of the following is true:</span></span>
- <span data-ttu-id="21a8c-2331">A função Func_jp_bank_account_branch_code localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="21a8c-2331">The function Func_jp_bank_account_branch_code finds content that matches the pattern.</span></span>
- <span data-ttu-id="21a8c-2332">Uma palavra-chave de Keyword_jp_bank_branch_code for encontrada.</span><span class="sxs-lookup"><span data-stu-id="21a8c-2332">A keyword from Keyword_jp_bank_branch_code is found.</span></span>

<span data-ttu-id="21a8c-2333">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="21a8c-2333">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="21a8c-2334">A função Func_jp_bank_account localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="21a8c-2334">The function Func_jp_bank_account finds content that matches the pattern.</span></span>
- <span data-ttu-id="21a8c-2335">Uma palavra-chave de Keyword_jp_bank_account for encontrada.</span><span class="sxs-lookup"><span data-stu-id="21a8c-2335">A keyword from Keyword_jp_bank_account is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="21a8c-2336">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="21a8c-2336">Keywords</span></span>

#### <a name="keywordjpbankaccount"></a><span data-ttu-id="21a8c-2337">Keyword_jp_bank_account</span><span class="sxs-lookup"><span data-stu-id="21a8c-2337">Keyword_jp_bank_account</span></span>

- <span data-ttu-id="21a8c-2338">Checking Account Number</span><span class="sxs-lookup"><span data-stu-id="21a8c-2338">Checking Account Number</span></span> 
- <span data-ttu-id="21a8c-2339">Checking Account</span><span class="sxs-lookup"><span data-stu-id="21a8c-2339">Checking Account</span></span> 
- <span data-ttu-id="21a8c-2340">Checking Account #</span><span class="sxs-lookup"><span data-stu-id="21a8c-2340">Checking Account #</span></span> 
- <span data-ttu-id="21a8c-2341">Checking Acct Number</span><span class="sxs-lookup"><span data-stu-id="21a8c-2341">Checking Acct Number</span></span> 
- <span data-ttu-id="21a8c-2342">Checking Acct #</span><span class="sxs-lookup"><span data-stu-id="21a8c-2342">Checking Acct #</span></span> 
- <span data-ttu-id="21a8c-2343">Checking Acct No.</span><span class="sxs-lookup"><span data-stu-id="21a8c-2343">Checking Acct No.</span></span> 
- <span data-ttu-id="21a8c-2344">Checking Account No.</span><span class="sxs-lookup"><span data-stu-id="21a8c-2344">Checking Account No.</span></span> 
- <span data-ttu-id="21a8c-2345">Bank Account Number</span><span class="sxs-lookup"><span data-stu-id="21a8c-2345">Bank Account Number</span></span> 
- <span data-ttu-id="21a8c-2346">Bank Account</span><span class="sxs-lookup"><span data-stu-id="21a8c-2346">Bank Account</span></span> 
- <span data-ttu-id="21a8c-2347">Bank Account #</span><span class="sxs-lookup"><span data-stu-id="21a8c-2347">Bank Account #</span></span> 
- <span data-ttu-id="21a8c-2348">Bank Acct Number</span><span class="sxs-lookup"><span data-stu-id="21a8c-2348">Bank Acct Number</span></span> 
- <span data-ttu-id="21a8c-2349">Bank Acct #</span><span class="sxs-lookup"><span data-stu-id="21a8c-2349">Bank Acct #</span></span> 
- <span data-ttu-id="21a8c-2350">Bank Acct No.</span><span class="sxs-lookup"><span data-stu-id="21a8c-2350">Bank Acct No.</span></span> 
- <span data-ttu-id="21a8c-2351">Bank Account No.</span><span class="sxs-lookup"><span data-stu-id="21a8c-2351">Bank Account No.</span></span> 
- <span data-ttu-id="21a8c-2352">Savings Account Number</span><span class="sxs-lookup"><span data-stu-id="21a8c-2352">Savings Account Number</span></span> 
- <span data-ttu-id="21a8c-2353">Savings Account</span><span class="sxs-lookup"><span data-stu-id="21a8c-2353">Savings Account</span></span> 
- <span data-ttu-id="21a8c-2354">Savings Account #</span><span class="sxs-lookup"><span data-stu-id="21a8c-2354">Savings Account #</span></span> 
- <span data-ttu-id="21a8c-2355">Savings Acct Number</span><span class="sxs-lookup"><span data-stu-id="21a8c-2355">Savings Acct Number</span></span> 
- <span data-ttu-id="21a8c-2356">Savings Acct #</span><span class="sxs-lookup"><span data-stu-id="21a8c-2356">Savings Acct #</span></span> 
- <span data-ttu-id="21a8c-2357">Savings Acct No.</span><span class="sxs-lookup"><span data-stu-id="21a8c-2357">Savings Acct No.</span></span> 
- <span data-ttu-id="21a8c-2358">Savings Account No.</span><span class="sxs-lookup"><span data-stu-id="21a8c-2358">Savings Account No.</span></span> 
- <span data-ttu-id="21a8c-2359">Debit Account Number</span><span class="sxs-lookup"><span data-stu-id="21a8c-2359">Debit Account Number</span></span> 
- <span data-ttu-id="21a8c-2360">Debit Account</span><span class="sxs-lookup"><span data-stu-id="21a8c-2360">Debit Account</span></span> 
- <span data-ttu-id="21a8c-2361">Debit Account #</span><span class="sxs-lookup"><span data-stu-id="21a8c-2361">Debit Account #</span></span> 
- <span data-ttu-id="21a8c-2362">Debit Acct Number</span><span class="sxs-lookup"><span data-stu-id="21a8c-2362">Debit Acct Number</span></span> 
- <span data-ttu-id="21a8c-2363">Debit Acct #</span><span class="sxs-lookup"><span data-stu-id="21a8c-2363">Debit Acct #</span></span> 
- <span data-ttu-id="21a8c-2364">Debit Acct No.</span><span class="sxs-lookup"><span data-stu-id="21a8c-2364">Debit Acct No.</span></span> 
- <span data-ttu-id="21a8c-2365">Debit Account No.</span><span class="sxs-lookup"><span data-stu-id="21a8c-2365">Debit Account No.</span></span> 
- <span data-ttu-id="21a8c-2366">口座番号を当座預金口座の確認</span><span class="sxs-lookup"><span data-stu-id="21a8c-2366">口座番号を当座預金口座の確認</span></span> 
- <span data-ttu-id="21a8c-2367">#アカウントの確認 、 勘定番号の確認</span><span class="sxs-lookup"><span data-stu-id="21a8c-2367">＃アカウントの確認、勘定番号の確認</span></span> 
- <span data-ttu-id="21a8c-2368">#勘定の確認</span><span class="sxs-lookup"><span data-stu-id="21a8c-2368">＃勘定の確認</span></span> 
- <span data-ttu-id="21a8c-2369">勘定番号の確認</span><span class="sxs-lookup"><span data-stu-id="21a8c-2369">勘定番号の確認</span></span> 
- <span data-ttu-id="21a8c-2370">口座番号の確認</span><span class="sxs-lookup"><span data-stu-id="21a8c-2370">口座番号の確認</span></span> 
- <span data-ttu-id="21a8c-2371">銀行口座番号</span><span class="sxs-lookup"><span data-stu-id="21a8c-2371">銀行口座番号</span></span> 
- <span data-ttu-id="21a8c-2372">銀行口座</span><span class="sxs-lookup"><span data-stu-id="21a8c-2372">銀行口座</span></span> 
- <span data-ttu-id="21a8c-2373">銀行口座 #</span><span class="sxs-lookup"><span data-stu-id="21a8c-2373">銀行口座＃</span></span> 
- <span data-ttu-id="21a8c-2374">銀行の勘定番号</span><span class="sxs-lookup"><span data-stu-id="21a8c-2374">銀行の勘定番号</span></span> 
- <span data-ttu-id="21a8c-2375">銀行のacct #</span><span class="sxs-lookup"><span data-stu-id="21a8c-2375">銀行のacct＃</span></span> 
- <span data-ttu-id="21a8c-2376">銀行の勘定いいえ</span><span class="sxs-lookup"><span data-stu-id="21a8c-2376">銀行の勘定いいえ</span></span> 
- <span data-ttu-id="21a8c-2377">銀行口座番号</span><span class="sxs-lookup"><span data-stu-id="21a8c-2377">銀行口座番号</span></span>
- <span data-ttu-id="21a8c-2378">普通預金口座番号</span><span class="sxs-lookup"><span data-stu-id="21a8c-2378">普通預金口座番号</span></span> 
- <span data-ttu-id="21a8c-2379">預金口座</span><span class="sxs-lookup"><span data-stu-id="21a8c-2379">預金口座</span></span> 
- <span data-ttu-id="21a8c-2380">貯蓄口座 #</span><span class="sxs-lookup"><span data-stu-id="21a8c-2380">貯蓄口座＃</span></span> 
- <span data-ttu-id="21a8c-2381">貯蓄勘定の数</span><span class="sxs-lookup"><span data-stu-id="21a8c-2381">貯蓄勘定の数</span></span> 
- <span data-ttu-id="21a8c-2382">貯蓄勘定 #</span><span class="sxs-lookup"><span data-stu-id="21a8c-2382">貯蓄勘定＃</span></span> 
- <span data-ttu-id="21a8c-2383">貯蓄勘定番号</span><span class="sxs-lookup"><span data-stu-id="21a8c-2383">貯蓄勘定番号</span></span> 
- <span data-ttu-id="21a8c-2384">普通預金口座番号</span><span class="sxs-lookup"><span data-stu-id="21a8c-2384">普通預金口座番号</span></span> 
- <span data-ttu-id="21a8c-2385">引き落とし口座番号</span><span class="sxs-lookup"><span data-stu-id="21a8c-2385">引き落とし口座番号</span></span> 
- <span data-ttu-id="21a8c-2386">口座番号</span><span class="sxs-lookup"><span data-stu-id="21a8c-2386">口座番号</span></span> 
- <span data-ttu-id="21a8c-2387">口座番号 #</span><span class="sxs-lookup"><span data-stu-id="21a8c-2387">口座番号＃</span></span> 
- <span data-ttu-id="21a8c-2388">デビットのacct番号</span><span class="sxs-lookup"><span data-stu-id="21a8c-2388">デビットのacct番号</span></span> 
- <span data-ttu-id="21a8c-2389">デビット勘定 #</span><span class="sxs-lookup"><span data-stu-id="21a8c-2389">デビット勘定＃</span></span> 
- <span data-ttu-id="21a8c-2390">デビットACCTの番号</span><span class="sxs-lookup"><span data-stu-id="21a8c-2390">デビットACCTの番号</span></span> 
- <span data-ttu-id="21a8c-2391">デビット口座番号</span><span class="sxs-lookup"><span data-stu-id="21a8c-2391">デビット口座番号</span></span> 

#### <a name="keywordjpbankbranchcode"></a><span data-ttu-id="21a8c-2392">Keyword_jp_bank_branch_code</span><span class="sxs-lookup"><span data-stu-id="21a8c-2392">Keyword_jp_bank_branch_code</span></span>

<span data-ttu-id="21a8c-2393">Otemachi</span><span class="sxs-lookup"><span data-stu-id="21a8c-2393">Otemachi</span></span>

## <a name="japan-drivers-license-number"></a><span data-ttu-id="21a8c-2394">Número de carteira de motorista do Japão</span><span class="sxs-lookup"><span data-stu-id="21a8c-2394">Japan Driver's License Number</span></span>

### <a name="format"></a><span data-ttu-id="21a8c-2395">Format</span><span class="sxs-lookup"><span data-stu-id="21a8c-2395">Format</span></span>

<span data-ttu-id="21a8c-2396">12 dígitos</span><span class="sxs-lookup"><span data-stu-id="21a8c-2396">12 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="21a8c-2397">Padrão</span><span class="sxs-lookup"><span data-stu-id="21a8c-2397">Pattern</span></span>

<span data-ttu-id="21a8c-2398">12 dígitos consecutivos</span><span class="sxs-lookup"><span data-stu-id="21a8c-2398">12 consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="21a8c-2399">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="21a8c-2399">Checksum</span></span>

<span data-ttu-id="21a8c-2400">Não</span><span class="sxs-lookup"><span data-stu-id="21a8c-2400">No</span></span>

### <a name="definition"></a><span data-ttu-id="21a8c-2401">Definição</span><span class="sxs-lookup"><span data-stu-id="21a8c-2401">Definition</span></span>

<span data-ttu-id="21a8c-2402">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="21a8c-2402">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="21a8c-2403">A função Func_jp_drivers_license_number localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="21a8c-2403">The function Func_jp_drivers_license_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="21a8c-2404">Uma palavra-chave de Keyword_jp_drivers_license_number for encontrada.</span><span class="sxs-lookup"><span data-stu-id="21a8c-2404">A keyword from Keyword_jp_drivers_license_number is found.</span></span>

```
<!-- Japan Driver's License Number -->
<Entity id="c6011143-d087-451c-8313-7f6d4aed2270" patternsProximity="300" recommendedConfidence="75">
    <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_jp_drivers_license_number" />
        <Match idRef ="Keyword_jp_drivers_license_number" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="21a8c-2405">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="21a8c-2405">Keywords</span></span>

#### <a name="keywordjpdriverslicensenumber"></a><span data-ttu-id="21a8c-2406">Keyword_jp_drivers_license_number</span><span class="sxs-lookup"><span data-stu-id="21a8c-2406">Keyword_jp_drivers_license_number</span></span>

- <span data-ttu-id="21a8c-2407">distribuição</span><span class="sxs-lookup"><span data-stu-id="21a8c-2407">dl#</span></span> 
- <span data-ttu-id="21a8c-2408">DISTRIBUIÇÃO</span><span class="sxs-lookup"><span data-stu-id="21a8c-2408">DL＃</span></span> 
- <span data-ttu-id="21a8c-2409">DL</span><span class="sxs-lookup"><span data-stu-id="21a8c-2409">dls#</span></span> 
- <span data-ttu-id="21a8c-2410">DL</span><span class="sxs-lookup"><span data-stu-id="21a8c-2410">DLS＃</span></span> 
- <span data-ttu-id="21a8c-2411">driver license</span><span class="sxs-lookup"><span data-stu-id="21a8c-2411">driver license</span></span> 
- <span data-ttu-id="21a8c-2412">driver licenses</span><span class="sxs-lookup"><span data-stu-id="21a8c-2412">driver licenses</span></span> 
- <span data-ttu-id="21a8c-2413">drivers license</span><span class="sxs-lookup"><span data-stu-id="21a8c-2413">drivers license</span></span> 
- <span data-ttu-id="21a8c-2414">driver's license</span><span class="sxs-lookup"><span data-stu-id="21a8c-2414">driver's license</span></span> 
- <span data-ttu-id="21a8c-2415">drivers licenses</span><span class="sxs-lookup"><span data-stu-id="21a8c-2415">drivers licenses</span></span> 
- <span data-ttu-id="21a8c-2416">driver's licenses</span><span class="sxs-lookup"><span data-stu-id="21a8c-2416">driver's licenses</span></span> 
- <span data-ttu-id="21a8c-2417">driving licence</span><span class="sxs-lookup"><span data-stu-id="21a8c-2417">driving licence</span></span> 
- <span data-ttu-id="21a8c-2418">driver'lic</span><span class="sxs-lookup"><span data-stu-id="21a8c-2418">lic#</span></span> 
- <span data-ttu-id="21a8c-2419">DRIVER'LIC</span><span class="sxs-lookup"><span data-stu-id="21a8c-2419">LIC＃</span></span> 
- <span data-ttu-id="21a8c-2420">driver'lics</span><span class="sxs-lookup"><span data-stu-id="21a8c-2420">lics#</span></span> 
- <span data-ttu-id="21a8c-2421">state id</span><span class="sxs-lookup"><span data-stu-id="21a8c-2421">state id</span></span> 
- <span data-ttu-id="21a8c-2422">state identification</span><span class="sxs-lookup"><span data-stu-id="21a8c-2422">state identification</span></span> 
- <span data-ttu-id="21a8c-2423">state identification number</span><span class="sxs-lookup"><span data-stu-id="21a8c-2423">state identification number</span></span> 
- <span data-ttu-id="21a8c-2424">低所得国 #</span><span class="sxs-lookup"><span data-stu-id="21a8c-2424">低所得国＃</span></span> 
- <span data-ttu-id="21a8c-2425">免許証</span><span class="sxs-lookup"><span data-stu-id="21a8c-2425">免許証</span></span> 
- <span data-ttu-id="21a8c-2426">状態ID</span><span class="sxs-lookup"><span data-stu-id="21a8c-2426">状態ID</span></span>
- <span data-ttu-id="21a8c-2427">状態の識別</span><span class="sxs-lookup"><span data-stu-id="21a8c-2427">状態の識別</span></span> 
- <span data-ttu-id="21a8c-2428">状態の識別番号</span><span class="sxs-lookup"><span data-stu-id="21a8c-2428">状態の識別番号</span></span> 
- <span data-ttu-id="21a8c-2429">運転免許</span><span class="sxs-lookup"><span data-stu-id="21a8c-2429">運転免許</span></span> 
- <span data-ttu-id="21a8c-2430">運転免許証</span><span class="sxs-lookup"><span data-stu-id="21a8c-2430">運転免許証</span></span> 
- <span data-ttu-id="21a8c-2431">運転免許証番号</span><span class="sxs-lookup"><span data-stu-id="21a8c-2431">運転免許証番号</span></span> 
   
## <a name="japan-passport-number"></a><span data-ttu-id="21a8c-2432">Número de passaporte do Japão</span><span class="sxs-lookup"><span data-stu-id="21a8c-2432">Japan Passport Number</span></span>

### <a name="format"></a><span data-ttu-id="21a8c-2433">Format</span><span class="sxs-lookup"><span data-stu-id="21a8c-2433">Format</span></span>

<span data-ttu-id="21a8c-2434">Duas letras seguidas por sete dígitos</span><span class="sxs-lookup"><span data-stu-id="21a8c-2434">Two letters followed by seven digits</span></span>

### <a name="pattern"></a><span data-ttu-id="21a8c-2435">Padrão</span><span class="sxs-lookup"><span data-stu-id="21a8c-2435">Pattern</span></span>

<span data-ttu-id="21a8c-2436">Duas letras (não diferencia maiúsculas de minúsculas) seguidas de sete dígitos</span><span class="sxs-lookup"><span data-stu-id="21a8c-2436">Two letters (not case sensitive) followed by seven digits</span></span>

### <a name="checksum"></a><span data-ttu-id="21a8c-2437">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="21a8c-2437">Checksum</span></span>

<span data-ttu-id="21a8c-2438">Não</span><span class="sxs-lookup"><span data-stu-id="21a8c-2438">No</span></span>

### <a name="definition"></a><span data-ttu-id="21a8c-2439">Definição</span><span class="sxs-lookup"><span data-stu-id="21a8c-2439">Definition</span></span>

<span data-ttu-id="21a8c-2440">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="21a8c-2440">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="21a8c-2441">A função Func_jp_passport localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="21a8c-2441">The function Func_jp_passport finds content that matches the pattern.</span></span>
- <span data-ttu-id="21a8c-2442">Uma palavra-chave de Keyword_jp_passport for encontrada.</span><span class="sxs-lookup"><span data-stu-id="21a8c-2442">A keyword from Keyword_jp_passport is found.</span></span>

```
<!-- Japan Passport Number -->
<Entity id="75177310-1a09-4613-bf6d-833aae3743f8" patternsProximity="300" recommendedConfidence="75">
    <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_jp_passport" />
        <Match idRef="Keyword_jp_passport" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="21a8c-2443">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="21a8c-2443">Keywords</span></span>

#### <a name="keywordjppassport"></a><span data-ttu-id="21a8c-2444">Keyword_jp_passport</span><span class="sxs-lookup"><span data-stu-id="21a8c-2444">Keyword_jp_passport</span></span>

- <span data-ttu-id="21a8c-2445">パスポート</span><span class="sxs-lookup"><span data-stu-id="21a8c-2445">パスポート</span></span> 
- <span data-ttu-id="21a8c-2446">パスポート番号</span><span class="sxs-lookup"><span data-stu-id="21a8c-2446">パスポート番号</span></span> 
- <span data-ttu-id="21a8c-2447">パスポートのNum</span><span class="sxs-lookup"><span data-stu-id="21a8c-2447">パスポートのNum</span></span> 
- <span data-ttu-id="21a8c-2448">パスポート #</span><span class="sxs-lookup"><span data-stu-id="21a8c-2448">パスポート＃</span></span> 
   
## <a name="japan-resident-registration-number"></a><span data-ttu-id="21a8c-2449">Número de registro de residente do Japão</span><span class="sxs-lookup"><span data-stu-id="21a8c-2449">Japan Resident Registration Number</span></span>

### <a name="format"></a><span data-ttu-id="21a8c-2450">Format</span><span class="sxs-lookup"><span data-stu-id="21a8c-2450">Format</span></span>

<span data-ttu-id="21a8c-2451">11 dígitos</span><span class="sxs-lookup"><span data-stu-id="21a8c-2451">11 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="21a8c-2452">Padrão</span><span class="sxs-lookup"><span data-stu-id="21a8c-2452">Pattern</span></span>

<span data-ttu-id="21a8c-2453">11 dígitos consecutivos</span><span class="sxs-lookup"><span data-stu-id="21a8c-2453">11 consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="21a8c-2454">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="21a8c-2454">Checksum</span></span>

<span data-ttu-id="21a8c-2455">Não</span><span class="sxs-lookup"><span data-stu-id="21a8c-2455">No</span></span>

### <a name="definition"></a><span data-ttu-id="21a8c-2456">Definição</span><span class="sxs-lookup"><span data-stu-id="21a8c-2456">Definition</span></span>

<span data-ttu-id="21a8c-2457">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="21a8c-2457">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="21a8c-2458">A função Func_jp_resident_registration_number localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="21a8c-2458">The function Func_jp_resident_registration_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="21a8c-2459">Uma palavra-chave de Keyword_jp_resident_registration_number for encontrada.</span><span class="sxs-lookup"><span data-stu-id="21a8c-2459">A keyword from Keyword_jp_resident_registration_number is found.</span></span>

```
<!-- Japan Resident Registration Number -->
<Entity id="01c1209b-6389-4faf-a5f8-3f7e13899652" patternsProximity="300" recommendedConfidence="75">
    <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_jp_resident_registration_number" />
        <Match idRef ="Keyword_jp_resident_registration_number" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="21a8c-2460">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="21a8c-2460">Keywords</span></span>

#### <a name="keywordjpresidentregistrationnumber"></a><span data-ttu-id="21a8c-2461">Keyword_jp_resident_registration_number</span><span class="sxs-lookup"><span data-stu-id="21a8c-2461">Keyword_jp_resident_registration_number</span></span>

- <span data-ttu-id="21a8c-2462">Resident Registration Number</span><span class="sxs-lookup"><span data-stu-id="21a8c-2462">Resident Registration Number</span></span>
- <span data-ttu-id="21a8c-2463">Resident Register Number</span><span class="sxs-lookup"><span data-stu-id="21a8c-2463">Resident Register Number</span></span> 
- <span data-ttu-id="21a8c-2464">Residents Basic Registry Number</span><span class="sxs-lookup"><span data-stu-id="21a8c-2464">Residents Basic Registry Number</span></span> 
- <span data-ttu-id="21a8c-2465">Resident Registration No.</span><span class="sxs-lookup"><span data-stu-id="21a8c-2465">Resident Registration No.</span></span> 
- <span data-ttu-id="21a8c-2466">Resident Register No.</span><span class="sxs-lookup"><span data-stu-id="21a8c-2466">Resident Register No.</span></span> 
- <span data-ttu-id="21a8c-2467">Residents Basic Registry No.</span><span class="sxs-lookup"><span data-stu-id="21a8c-2467">Residents Basic Registry No.</span></span> 
- <span data-ttu-id="21a8c-2468">Basic Resident Register No.</span><span class="sxs-lookup"><span data-stu-id="21a8c-2468">Basic Resident Register No.</span></span> 
- <span data-ttu-id="21a8c-2469">住民登録番号 、 登録番号をレジデント</span><span class="sxs-lookup"><span data-stu-id="21a8c-2469">住民登録番号、登録番号をレジデント</span></span> 
- <span data-ttu-id="21a8c-2470">住民基本登録番号 、 登録番号</span><span class="sxs-lookup"><span data-stu-id="21a8c-2470">住民基本登録番号、登録番号</span></span> 
- <span data-ttu-id="21a8c-2471">住民基本レジストリ番号を常駐</span><span class="sxs-lookup"><span data-stu-id="21a8c-2471">住民基本レジストリ番号を常駐</span></span> 
- <span data-ttu-id="21a8c-2472">登録番号を常駐住民基本台帳登録番号</span><span class="sxs-lookup"><span data-stu-id="21a8c-2472">登録番号を常駐住民基本台帳登録番号</span></span> 

   
## <a name="japan-social-insurance-number-sin"></a><span data-ttu-id="21a8c-2473">Número de seguro social do Japão (SIN)</span><span class="sxs-lookup"><span data-stu-id="21a8c-2473">Japan Social Insurance Number (SIN)</span></span>

### <a name="format"></a><span data-ttu-id="21a8c-2474">Format</span><span class="sxs-lookup"><span data-stu-id="21a8c-2474">Format</span></span>

<span data-ttu-id="21a8c-2475">7 a 12 dígitos</span><span class="sxs-lookup"><span data-stu-id="21a8c-2475">7-12 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="21a8c-2476">Padrão</span><span class="sxs-lookup"><span data-stu-id="21a8c-2476">Pattern</span></span>

<span data-ttu-id="21a8c-2477">7 a 12 dígitos:</span><span class="sxs-lookup"><span data-stu-id="21a8c-2477">7-12 digits:</span></span>
- <span data-ttu-id="21a8c-2478">Quatro dígitos</span><span class="sxs-lookup"><span data-stu-id="21a8c-2478">Four digits</span></span> 
- <span data-ttu-id="21a8c-2479">Um hífen (opcional)</span><span class="sxs-lookup"><span data-stu-id="21a8c-2479">A hyphen (optional)</span></span> 
- <span data-ttu-id="21a8c-2480">Seis dígitos ou</span><span class="sxs-lookup"><span data-stu-id="21a8c-2480">Six digits OR</span></span>
- <span data-ttu-id="21a8c-2481">7 a 12 dígitos consecutivos</span><span class="sxs-lookup"><span data-stu-id="21a8c-2481">7-12 consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="21a8c-2482">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="21a8c-2482">Checksum</span></span>

<span data-ttu-id="21a8c-2483">Não</span><span class="sxs-lookup"><span data-stu-id="21a8c-2483">No</span></span>

### <a name="definition"></a><span data-ttu-id="21a8c-2484">Definição</span><span class="sxs-lookup"><span data-stu-id="21a8c-2484">Definition</span></span>

<span data-ttu-id="21a8c-2485">Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="21a8c-2485">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="21a8c-2486">A função Func_jp_sin localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="21a8c-2486">The function Func_jp_sin finds content that matches the pattern.</span></span>
- <span data-ttu-id="21a8c-2487">Uma palavra-chave de Keyword_jp_sin for encontrada.</span><span class="sxs-lookup"><span data-stu-id="21a8c-2487">A keyword from Keyword_jp_sin is found.</span></span>

<span data-ttu-id="21a8c-2488">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="21a8c-2488">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="21a8c-2489">A função Func_jp_sin_pre_1997 localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="21a8c-2489">The function Func_jp_sin_pre_1997 finds content that matches the pattern.</span></span>
- <span data-ttu-id="21a8c-2490">Uma palavra-chave de Keyword_jp_sin for encontrada.</span><span class="sxs-lookup"><span data-stu-id="21a8c-2490">A keyword from Keyword_jp_sin is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="21a8c-2491">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="21a8c-2491">Keywords</span></span>

#### <a name="keywordjpsin"></a><span data-ttu-id="21a8c-2492">Keyword_jp_sin</span><span class="sxs-lookup"><span data-stu-id="21a8c-2492">Keyword_jp_sin</span></span>

- <span data-ttu-id="21a8c-2493">Social Insurance No.</span><span class="sxs-lookup"><span data-stu-id="21a8c-2493">Social Insurance No.</span></span> 
- <span data-ttu-id="21a8c-2494">Social Insurance Num</span><span class="sxs-lookup"><span data-stu-id="21a8c-2494">Social Insurance Num</span></span> 
- <span data-ttu-id="21a8c-2495">Social Insurance Number</span><span class="sxs-lookup"><span data-stu-id="21a8c-2495">Social Insurance Number</span></span> 
- <span data-ttu-id="21a8c-2496">社会保険のテンキー</span><span class="sxs-lookup"><span data-stu-id="21a8c-2496">社会保険のテンキー</span></span> 
- <span data-ttu-id="21a8c-2497">社会保険番号</span><span class="sxs-lookup"><span data-stu-id="21a8c-2497">社会保険番号</span></span> 

## <a name="japanese-residence-card-number"></a><span data-ttu-id="21a8c-2498">Número do cartão de residência japonês</span><span class="sxs-lookup"><span data-stu-id="21a8c-2498">Japanese Residence Card Number</span></span>

### <a name="format"></a><span data-ttu-id="21a8c-2499">Format</span><span class="sxs-lookup"><span data-stu-id="21a8c-2499">Format</span></span>

<span data-ttu-id="21a8c-2500">12 letras e dígitos</span><span class="sxs-lookup"><span data-stu-id="21a8c-2500">12 letters and digits</span></span>

### <a name="pattern"></a><span data-ttu-id="21a8c-2501">Padrão</span><span class="sxs-lookup"><span data-stu-id="21a8c-2501">Pattern</span></span>

<span data-ttu-id="21a8c-2502">12 letras e dígitos:</span><span class="sxs-lookup"><span data-stu-id="21a8c-2502">12 letters and digits:</span></span>
- <span data-ttu-id="21a8c-2503">Duas letras (não diferenciam maiúsculas de minúsculas)</span><span class="sxs-lookup"><span data-stu-id="21a8c-2503">Two letters (not case sensitive)</span></span>
- <span data-ttu-id="21a8c-2504">Oito dígitos</span><span class="sxs-lookup"><span data-stu-id="21a8c-2504">Eight digits</span></span> 
- <span data-ttu-id="21a8c-2505">Duas letras (não diferenciam maiúsculas de minúsculas)</span><span class="sxs-lookup"><span data-stu-id="21a8c-2505">Two letters (not case sensitive)</span></span>

### <a name="checksum"></a><span data-ttu-id="21a8c-2506">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="21a8c-2506">Checksum</span></span>

<span data-ttu-id="21a8c-2507">Não</span><span class="sxs-lookup"><span data-stu-id="21a8c-2507">No</span></span>

### <a name="definition"></a><span data-ttu-id="21a8c-2508">Definição</span><span class="sxs-lookup"><span data-stu-id="21a8c-2508">Definition</span></span>

<span data-ttu-id="21a8c-2509">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="21a8c-2509">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="21a8c-2510">A expressão regular Regex_jp_residence_card_number localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="21a8c-2510">The regular expression Regex_jp_residence_card_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="21a8c-2511">Uma palavra-chave de Keyword_jp_residence_card_number for encontrada.</span><span class="sxs-lookup"><span data-stu-id="21a8c-2511">A keyword from Keyword_jp_residence_card_number is found.</span></span>

```
<!--Japan Residence Card Number-->
-<Entity id="ac36fef2-a289-4e2c-bb48-b02366e89fc0" recommendedConfidence="75" patternsProximity="300">
   -<Pattern confidenceLevel="75">
      <IdMatch idRef="Regex_jp_residence_card_number"/>
      <Match idRef="Keyword_jp_residence_card_number"/>
   </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="21a8c-2512">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="21a8c-2512">Keywords</span></span>

#### <a name="keywordjpresidencecardnumber"></a><span data-ttu-id="21a8c-2513">Keyword_jp_residence_card_number</span><span class="sxs-lookup"><span data-stu-id="21a8c-2513">Keyword_jp_residence_card_number</span></span>

- <span data-ttu-id="21a8c-2514">Número do cartão de residência</span><span class="sxs-lookup"><span data-stu-id="21a8c-2514">Residence card number</span></span>
- <span data-ttu-id="21a8c-2515">Número do cartão de residência</span><span class="sxs-lookup"><span data-stu-id="21a8c-2515">Residence card no</span></span>
- <span data-ttu-id="21a8c-2516">N º do cartão de residência</span><span class="sxs-lookup"><span data-stu-id="21a8c-2516">Residence card #</span></span>
- <span data-ttu-id="21a8c-2517">在留カード番号</span><span class="sxs-lookup"><span data-stu-id="21a8c-2517">在留カード番号</span></span>
   
## <a name="malaysia-id-card-number"></a><span data-ttu-id="21a8c-2518">Número do Cartão de Identificação da Malásia</span><span class="sxs-lookup"><span data-stu-id="21a8c-2518">Malaysia ID Card Number</span></span>

### <a name="format"></a><span data-ttu-id="21a8c-2519">Format</span><span class="sxs-lookup"><span data-stu-id="21a8c-2519">Format</span></span>

<span data-ttu-id="21a8c-2520">12 dígitos contendo hifens opcionais</span><span class="sxs-lookup"><span data-stu-id="21a8c-2520">12 digits containing optional hyphens</span></span>

### <a name="pattern"></a><span data-ttu-id="21a8c-2521">Padrão</span><span class="sxs-lookup"><span data-stu-id="21a8c-2521">Pattern</span></span>

<span data-ttu-id="21a8c-2522">12 dígitos:</span><span class="sxs-lookup"><span data-stu-id="21a8c-2522">12 digits:</span></span>
- <span data-ttu-id="21a8c-2523">Seis dígitos no formato AAMMDD que são a data de nascimento</span><span class="sxs-lookup"><span data-stu-id="21a8c-2523">Six digits in the format YYMMDD which are the date of birth</span></span> 
- <span data-ttu-id="21a8c-2524">Um traço (opcional)</span><span class="sxs-lookup"><span data-stu-id="21a8c-2524">A dash (optional)</span></span> 
- <span data-ttu-id="21a8c-2525">Código do local de nascimento de duas letras </span><span class="sxs-lookup"><span data-stu-id="21a8c-2525">Two-letter place-of-birth code</span></span> 
- <span data-ttu-id="21a8c-2526">Um traço (opcional)</span><span class="sxs-lookup"><span data-stu-id="21a8c-2526">A dash (optional)</span></span> 
- <span data-ttu-id="21a8c-2527">Três dígitos aleatórios </span><span class="sxs-lookup"><span data-stu-id="21a8c-2527">Three random digits</span></span> 
- <span data-ttu-id="21a8c-2528">Código de sexo de um dígito</span><span class="sxs-lookup"><span data-stu-id="21a8c-2528">One-digit gender code</span></span>

### <a name="checksum"></a><span data-ttu-id="21a8c-2529">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="21a8c-2529">Checksum</span></span>

<span data-ttu-id="21a8c-2530">Não</span><span class="sxs-lookup"><span data-stu-id="21a8c-2530">No</span></span>

### <a name="definition"></a><span data-ttu-id="21a8c-2531">Definição</span><span class="sxs-lookup"><span data-stu-id="21a8c-2531">Definition</span></span>

<span data-ttu-id="21a8c-2532">Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="21a8c-2532">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="21a8c-2533">A expressão regular Regex_malaysia_id_card_number localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="21a8c-2533">The regular expression Regex_malaysia_id_card_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="21a8c-2534">Uma palavra-chave de Keyword_malaysia_id_card_number for encontrada.</span><span class="sxs-lookup"><span data-stu-id="21a8c-2534">A keyword from Keyword_malaysia_id_card_number is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="21a8c-2535">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="21a8c-2535">Keywords</span></span>
   
#### <a name="keywordmalaysiaidcardnumber"></a><span data-ttu-id="21a8c-2536">Keyword_malaysia_id_card_number</span><span class="sxs-lookup"><span data-stu-id="21a8c-2536">Keyword_malaysia_id_card_number</span></span>

- <span data-ttu-id="21a8c-2537">cartão de aplicativo digital</span><span class="sxs-lookup"><span data-stu-id="21a8c-2537">digital application card</span></span>
- <span data-ttu-id="21a8c-2538">e/c</span><span class="sxs-lookup"><span data-stu-id="21a8c-2538">i/c</span></span>
- <span data-ttu-id="21a8c-2539">e/c não</span><span class="sxs-lookup"><span data-stu-id="21a8c-2539">i/c no</span></span>
- <span data-ttu-id="21a8c-2540">Liga</span><span class="sxs-lookup"><span data-stu-id="21a8c-2540">ic</span></span>
- <span data-ttu-id="21a8c-2541">IC não</span><span class="sxs-lookup"><span data-stu-id="21a8c-2541">ic no</span></span>
- <span data-ttu-id="21a8c-2542">id card</span><span class="sxs-lookup"><span data-stu-id="21a8c-2542">id card</span></span>
- <span data-ttu-id="21a8c-2543">Cartão de identificação</span><span class="sxs-lookup"><span data-stu-id="21a8c-2543">identification Card</span></span>
- <span data-ttu-id="21a8c-2544">cartão de identidade</span><span class="sxs-lookup"><span data-stu-id="21a8c-2544">identity card</span></span>
- <span data-ttu-id="21a8c-2545">k/p</span><span class="sxs-lookup"><span data-stu-id="21a8c-2545">k/p</span></span>
- <span data-ttu-id="21a8c-2546">n/p não</span><span class="sxs-lookup"><span data-stu-id="21a8c-2546">k/p no</span></span>
- <span data-ttu-id="21a8c-2547">kad akuan diri</span><span class="sxs-lookup"><span data-stu-id="21a8c-2547">kad akuan diri</span></span>
- <span data-ttu-id="21a8c-2548">kad aplikasi digital</span><span class="sxs-lookup"><span data-stu-id="21a8c-2548">kad aplikasi digital</span></span>
- <span data-ttu-id="21a8c-2549">kad pengenalan Malásia</span><span class="sxs-lookup"><span data-stu-id="21a8c-2549">kad pengenalan malaysia</span></span>
- <span data-ttu-id="21a8c-2550">KP</span><span class="sxs-lookup"><span data-stu-id="21a8c-2550">kp</span></span>
- <span data-ttu-id="21a8c-2551">KP não</span><span class="sxs-lookup"><span data-stu-id="21a8c-2551">kp no</span></span>
- <span data-ttu-id="21a8c-2552">MyKad</span><span class="sxs-lookup"><span data-stu-id="21a8c-2552">mykad</span></span>
- <span data-ttu-id="21a8c-2553">Mykas</span><span class="sxs-lookup"><span data-stu-id="21a8c-2553">mykas</span></span>
- <span data-ttu-id="21a8c-2554">mykid</span><span class="sxs-lookup"><span data-stu-id="21a8c-2554">mykid</span></span>
- <span data-ttu-id="21a8c-2555">mypr</span><span class="sxs-lookup"><span data-stu-id="21a8c-2555">mypr</span></span>
- <span data-ttu-id="21a8c-2556">mytentera</span><span class="sxs-lookup"><span data-stu-id="21a8c-2556">mytentera</span></span>
- <span data-ttu-id="21a8c-2557">cartão de identidade da Malásia</span><span class="sxs-lookup"><span data-stu-id="21a8c-2557">malaysia identity card</span></span>
- <span data-ttu-id="21a8c-2558">cartão de identidade do Malasiano</span><span class="sxs-lookup"><span data-stu-id="21a8c-2558">malaysian identity card</span></span>
- <span data-ttu-id="21a8c-2559">NRIC</span><span class="sxs-lookup"><span data-stu-id="21a8c-2559">nric</span></span>
- <span data-ttu-id="21a8c-2560">cartão de identificação pessoal</span><span class="sxs-lookup"><span data-stu-id="21a8c-2560">personal identification card</span></span>
   
## <a name="netherlands-citizens-service-bsn-number"></a><span data-ttu-id="21a8c-2561">Número do Serviço do Cidadão (BSN) da Holland</span><span class="sxs-lookup"><span data-stu-id="21a8c-2561">Netherlands Citizen's Service (BSN) Number</span></span>

### <a name="format"></a><span data-ttu-id="21a8c-2562">Format</span><span class="sxs-lookup"><span data-stu-id="21a8c-2562">Format</span></span>

<span data-ttu-id="21a8c-2563">8 a 9 dígitos contendo espaços opcionais</span><span class="sxs-lookup"><span data-stu-id="21a8c-2563">8-9 digits containing optional spaces</span></span>

### <a name="pattern"></a><span data-ttu-id="21a8c-2564">Padrão</span><span class="sxs-lookup"><span data-stu-id="21a8c-2564">Pattern</span></span>

<span data-ttu-id="21a8c-2565">8 a 9 dígitos.</span><span class="sxs-lookup"><span data-stu-id="21a8c-2565">8-9 digits:</span></span>
- <span data-ttu-id="21a8c-2566">Três dígitos</span><span class="sxs-lookup"><span data-stu-id="21a8c-2566">Three digits</span></span> 
- <span data-ttu-id="21a8c-2567">Um espaço (opcional)</span><span class="sxs-lookup"><span data-stu-id="21a8c-2567">A space (optional)</span></span> 
- <span data-ttu-id="21a8c-2568">Três dígitos</span><span class="sxs-lookup"><span data-stu-id="21a8c-2568">Three digits</span></span> 
- <span data-ttu-id="21a8c-2569">Um espaço (opcional)</span><span class="sxs-lookup"><span data-stu-id="21a8c-2569">A space (optional)</span></span> 
- <span data-ttu-id="21a8c-2570">2 a 3 dígitos</span><span class="sxs-lookup"><span data-stu-id="21a8c-2570">2-3 digits</span></span>

### <a name="checksum"></a><span data-ttu-id="21a8c-2571">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="21a8c-2571">Checksum</span></span>

<span data-ttu-id="21a8c-2572">Sim</span><span class="sxs-lookup"><span data-stu-id="21a8c-2572">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="21a8c-2573">Definição</span><span class="sxs-lookup"><span data-stu-id="21a8c-2573">Definition</span></span>

<span data-ttu-id="21a8c-2574">Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="21a8c-2574">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="21a8c-2575">A função Func_netherlands_bsn localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="21a8c-2575">The function Func_netherlands_bsn finds content that matches the pattern.</span></span>
- <span data-ttu-id="21a8c-2576">Uma palavra-chave de Keyword_netherlands_bsn for encontrada.</span><span class="sxs-lookup"><span data-stu-id="21a8c-2576">A keyword from Keyword_netherlands_bsn is found.</span></span>
- <span data-ttu-id="21a8c-2577">A função Func_eu_date2 encontra uma data no formato de data à direita.</span><span class="sxs-lookup"><span data-stu-id="21a8c-2577">The function Func_eu_date2 finds a date in the right date format.</span></span>
- <span data-ttu-id="21a8c-2578">A soma de verificação passa.</span><span class="sxs-lookup"><span data-stu-id="21a8c-2578">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="21a8c-2579">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="21a8c-2579">Keywords</span></span>

#### <a name="keywordnetherlandsbsn"></a><span data-ttu-id="21a8c-2580">Keyword_netherlands_bsn</span><span class="sxs-lookup"><span data-stu-id="21a8c-2580">Keyword_netherlands_bsn</span></span>

- <span data-ttu-id="21a8c-2581">Número do serviço do cidadão</span><span class="sxs-lookup"><span data-stu-id="21a8c-2581">Citizen service number</span></span> 
- <span data-ttu-id="21a8c-2582">BSN</span><span class="sxs-lookup"><span data-stu-id="21a8c-2582">BSN</span></span> 
- <span data-ttu-id="21a8c-2583">Burgerservicenummer</span><span class="sxs-lookup"><span data-stu-id="21a8c-2583">Burgerservicenummer</span></span> 
- <span data-ttu-id="21a8c-2584">Sofinummer</span><span class="sxs-lookup"><span data-stu-id="21a8c-2584">Sofinummer</span></span> 
- <span data-ttu-id="21a8c-2585">Persoonsgebonden nummer</span><span class="sxs-lookup"><span data-stu-id="21a8c-2585">Persoonsgebonden nummer</span></span> 
- <span data-ttu-id="21a8c-2586">Persoonsnummer</span><span class="sxs-lookup"><span data-stu-id="21a8c-2586">Persoonsnummer</span></span>    

   
## <a name="new-zealand-ministry-of-health-number"></a><span data-ttu-id="21a8c-2587">Número do Ministério da Saúde da Nova Zelândia</span><span class="sxs-lookup"><span data-stu-id="21a8c-2587">New Zealand Ministry of Health Number</span></span>

### <a name="format"></a><span data-ttu-id="21a8c-2588">Format</span><span class="sxs-lookup"><span data-stu-id="21a8c-2588">Format</span></span>

<span data-ttu-id="21a8c-2589">Três letras, um espaço (opcional) e quatro dígitos</span><span class="sxs-lookup"><span data-stu-id="21a8c-2589">Three letters, a space (optional), and four digits</span></span>

### <a name="pattern"></a><span data-ttu-id="21a8c-2590">Padrão</span><span class="sxs-lookup"><span data-stu-id="21a8c-2590">Pattern</span></span>

<span data-ttu-id="21a8c-2591">Três letras (não diferencia maiúsculas de minúsculas) um espaço (opcional) quatro dígitos</span><span class="sxs-lookup"><span data-stu-id="21a8c-2591">Three letters (not case sensitive) a space (optional) four digits</span></span>

### <a name="checksum"></a><span data-ttu-id="21a8c-2592">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="21a8c-2592">Checksum</span></span>

<span data-ttu-id="21a8c-2593">Sim</span><span class="sxs-lookup"><span data-stu-id="21a8c-2593">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="21a8c-2594">Definição</span><span class="sxs-lookup"><span data-stu-id="21a8c-2594">Definition</span></span>

<span data-ttu-id="21a8c-2595">Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="21a8c-2595">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="21a8c-2596">A função Func_new_zealand_ministry_of_health_number localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="21a8c-2596">The function Func_new_zealand_ministry_of_health_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="21a8c-2597">Uma palavra-chave de Keyword_nz_terms for encontrada.</span><span class="sxs-lookup"><span data-stu-id="21a8c-2597">A keyword from Keyword_nz_terms is found.</span></span>
- <span data-ttu-id="21a8c-2598">A soma de verificação passa.</span><span class="sxs-lookup"><span data-stu-id="21a8c-2598">The checksum passes.</span></span>

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

<span data-ttu-id="21a8c-2599">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="21a8c-2599">Keywords</span></span>

<span data-ttu-id="21a8c-2600">Keyword_nz_terms</span><span class="sxs-lookup"><span data-stu-id="21a8c-2600">Keyword_nz_terms</span></span>

- <span data-ttu-id="21a8c-2601">NHI</span><span class="sxs-lookup"><span data-stu-id="21a8c-2601">NHI</span></span> 
- <span data-ttu-id="21a8c-2602">Nova Zelândia</span><span class="sxs-lookup"><span data-stu-id="21a8c-2602">New Zealand</span></span> 
- <span data-ttu-id="21a8c-2603">Saúde</span><span class="sxs-lookup"><span data-stu-id="21a8c-2603">Health</span></span> 
- <span data-ttu-id="21a8c-2604">tratamento</span><span class="sxs-lookup"><span data-stu-id="21a8c-2604">treatment</span></span> 
   
## <a name="norway-identification-number"></a><span data-ttu-id="21a8c-2605">Número de Identificação da Noruega</span><span class="sxs-lookup"><span data-stu-id="21a8c-2605">Norway Identification Number</span></span>

### <a name="format"></a><span data-ttu-id="21a8c-2606">Format</span><span class="sxs-lookup"><span data-stu-id="21a8c-2606">Format</span></span>

<span data-ttu-id="21a8c-2607">11 dígitos</span><span class="sxs-lookup"><span data-stu-id="21a8c-2607">11 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="21a8c-2608">Padrão</span><span class="sxs-lookup"><span data-stu-id="21a8c-2608">Pattern</span></span>

<span data-ttu-id="21a8c-2609">11 dígitos:</span><span class="sxs-lookup"><span data-stu-id="21a8c-2609">11 digits:</span></span>
- <span data-ttu-id="21a8c-2610">Seis dígitos no formato DDMMAA que são a data de nascimento</span><span class="sxs-lookup"><span data-stu-id="21a8c-2610">Six digits in the format DDMMYY which are the date of birth</span></span> 
- <span data-ttu-id="21a8c-2611">Número individual de três dígitos </span><span class="sxs-lookup"><span data-stu-id="21a8c-2611">Three-digit individual number</span></span> 
- <span data-ttu-id="21a8c-2612">Dois dígitos de verificação</span><span class="sxs-lookup"><span data-stu-id="21a8c-2612">Two check digits</span></span>

### <a name="checksum"></a><span data-ttu-id="21a8c-2613">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="21a8c-2613">Checksum</span></span>

<span data-ttu-id="21a8c-2614">Sim</span><span class="sxs-lookup"><span data-stu-id="21a8c-2614">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="21a8c-2615">Definição</span><span class="sxs-lookup"><span data-stu-id="21a8c-2615">Definition</span></span>

<span data-ttu-id="21a8c-2616">Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="21a8c-2616">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="21a8c-2617">A função Func_norway_id_number localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="21a8c-2617">The function Func_norway_id_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="21a8c-2618">Uma palavra-chave de Keyword_norway_id_number for encontrada.</span><span class="sxs-lookup"><span data-stu-id="21a8c-2618">A keyword from Keyword_norway_id_number is found.</span></span>
- <span data-ttu-id="21a8c-2619">A soma de verificação passa.</span><span class="sxs-lookup"><span data-stu-id="21a8c-2619">The checksum passes.</span></span>
- <span data-ttu-id="21a8c-2620">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="21a8c-2620">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="21a8c-2621">A função Func_norway_id_numbe localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="21a8c-2621">The function Func_norway_id_numbe finds content that matches the pattern.</span></span>
- <span data-ttu-id="21a8c-2622">A soma de verificação passa.</span><span class="sxs-lookup"><span data-stu-id="21a8c-2622">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="21a8c-2623">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="21a8c-2623">Keywords</span></span>

#### <a name="keywordnorwayidnumber"></a><span data-ttu-id="21a8c-2624">Keyword_norway_id_number</span><span class="sxs-lookup"><span data-stu-id="21a8c-2624">Keyword_norway_id_number</span></span>

- <span data-ttu-id="21a8c-2625">Número de identificação pessoal</span><span class="sxs-lookup"><span data-stu-id="21a8c-2625">Personal identification number</span></span>
- <span data-ttu-id="21a8c-2626">Número de Identificação Norueguês</span><span class="sxs-lookup"><span data-stu-id="21a8c-2626">Norwegian ID Number</span></span>
- <span data-ttu-id="21a8c-2627">Número de Identificação</span><span class="sxs-lookup"><span data-stu-id="21a8c-2627">ID Number</span></span>
- <span data-ttu-id="21a8c-2628">Identificador</span><span class="sxs-lookup"><span data-stu-id="21a8c-2628">Identification</span></span>
- <span data-ttu-id="21a8c-2629">Personnummer</span><span class="sxs-lookup"><span data-stu-id="21a8c-2629">Personnummer</span></span>
- <span data-ttu-id="21a8c-2630">Fødselsnummer</span><span class="sxs-lookup"><span data-stu-id="21a8c-2630">Fødselsnummer</span></span>

   
## <a name="philippines-unified-multi-purpose-id-number"></a><span data-ttu-id="21a8c-2631">Número de Identificação Multiuso Unificada das Filipinas</span><span class="sxs-lookup"><span data-stu-id="21a8c-2631">Philippines Unified Multi-Purpose ID Number</span></span>

### <a name="format"></a><span data-ttu-id="21a8c-2632">Format</span><span class="sxs-lookup"><span data-stu-id="21a8c-2632">Format</span></span>

<span data-ttu-id="21a8c-2633">12 dígitos separados por hifens</span><span class="sxs-lookup"><span data-stu-id="21a8c-2633">12 digits separated by hyphens</span></span>

### <a name="pattern"></a><span data-ttu-id="21a8c-2634">Padrão</span><span class="sxs-lookup"><span data-stu-id="21a8c-2634">Pattern</span></span>

<span data-ttu-id="21a8c-2635">12 dígitos:</span><span class="sxs-lookup"><span data-stu-id="21a8c-2635">12 digits:</span></span>
- <span data-ttu-id="21a8c-2636">Quatro dígitos</span><span class="sxs-lookup"><span data-stu-id="21a8c-2636">Four digits</span></span> 
- <span data-ttu-id="21a8c-2637">Um hífen</span><span class="sxs-lookup"><span data-stu-id="21a8c-2637">A hyphen</span></span> 
- <span data-ttu-id="21a8c-2638">Sete dígitos </span><span class="sxs-lookup"><span data-stu-id="21a8c-2638">Seven digits</span></span> 
- <span data-ttu-id="21a8c-2639">Um hífen</span><span class="sxs-lookup"><span data-stu-id="21a8c-2639">A hyphen</span></span> 
- <span data-ttu-id="21a8c-2640">Um dígito</span><span class="sxs-lookup"><span data-stu-id="21a8c-2640">One digit</span></span>

### <a name="checksum"></a><span data-ttu-id="21a8c-2641">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="21a8c-2641">Checksum</span></span>

<span data-ttu-id="21a8c-2642">Não</span><span class="sxs-lookup"><span data-stu-id="21a8c-2642">No</span></span>

### <a name="definition"></a><span data-ttu-id="21a8c-2643">Definição</span><span class="sxs-lookup"><span data-stu-id="21a8c-2643">Definition</span></span>

<span data-ttu-id="21a8c-2644">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="21a8c-2644">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="21a8c-2645">A expressão regular Regex_philippines_unified_id localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="21a8c-2645">The regular expression Regex_philippines_unified_id finds content that matches the pattern.</span></span>
- <span data-ttu-id="21a8c-2646">Uma palavra-chave de Keyword_philippines_id for encontrada.</span><span class="sxs-lookup"><span data-stu-id="21a8c-2646">A keyword from Keyword_philippines_id is found.</span></span>

```
<!-- Philippines Unified Multi-Purpose ID number -->
<Entity id="019b39dd-8c25-4765-91a3-d9c6baf3c3b3" recommendedConfidence="75" patternsProximity="300">
  <Pattern confidenceLevel="75">
     <IdMatch idRef="Regex_philippines_unified_id"/>
     <Match idRef="Keyword_philippines_id"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="21a8c-2647">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="21a8c-2647">Keywords</span></span>
   
#### <a name="keywordphilippinesid"></a><span data-ttu-id="21a8c-2648">Keyword_philippines_id</span><span class="sxs-lookup"><span data-stu-id="21a8c-2648">Keyword_philippines_id</span></span>

- <span data-ttu-id="21a8c-2649">Identificação Multiuso Unificada</span><span class="sxs-lookup"><span data-stu-id="21a8c-2649">Unified Multi-Purpose ID</span></span> 
- <span data-ttu-id="21a8c-2650">UMID</span><span class="sxs-lookup"><span data-stu-id="21a8c-2650">UMID</span></span> 
- <span data-ttu-id="21a8c-2651">Cartão de Identidade</span><span class="sxs-lookup"><span data-stu-id="21a8c-2651">Identity Card</span></span> 
- <span data-ttu-id="21a8c-2652">Pinag-isang Multi-Layunin ID</span><span class="sxs-lookup"><span data-stu-id="21a8c-2652">Pinag-isang Multi-Layunin ID</span></span>
   
## <a name="poland-identity-card"></a><span data-ttu-id="21a8c-2653">Cartão de Identificação da Polônia</span><span class="sxs-lookup"><span data-stu-id="21a8c-2653">Poland Identity Card</span></span>

### <a name="format"></a><span data-ttu-id="21a8c-2654">Format</span><span class="sxs-lookup"><span data-stu-id="21a8c-2654">Format</span></span>

<span data-ttu-id="21a8c-2655">Três letras e seis dígitos</span><span class="sxs-lookup"><span data-stu-id="21a8c-2655">Three letters and six digits</span></span>

### <a name="pattern"></a><span data-ttu-id="21a8c-2656">Padrão</span><span class="sxs-lookup"><span data-stu-id="21a8c-2656">Pattern</span></span>

<span data-ttu-id="21a8c-2657">Três letras (não diferenciam maiúsculas de minúsculas) seguidas de seis dígitos</span><span class="sxs-lookup"><span data-stu-id="21a8c-2657">Three letters (not case sensitive) followed by six digits</span></span>

### <a name="checksum"></a><span data-ttu-id="21a8c-2658">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="21a8c-2658">Checksum</span></span>

<span data-ttu-id="21a8c-2659">Sim</span><span class="sxs-lookup"><span data-stu-id="21a8c-2659">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="21a8c-2660">Definição</span><span class="sxs-lookup"><span data-stu-id="21a8c-2660">Definition</span></span>

<span data-ttu-id="21a8c-2661">Uma política de DLP é de 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres: a função Func_polish_national_id localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="21a8c-2661">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters: The function Func_polish_national_id finds content that matches the pattern.</span></span>
<span data-ttu-id="21a8c-2662">Uma palavra-chave de Keyword_polish_national_id_passport_number for encontrada.</span><span class="sxs-lookup"><span data-stu-id="21a8c-2662">A keyword from Keyword_polish_national_id_passport_number is found.</span></span>
<span data-ttu-id="21a8c-2663">A soma de verificação passa.</span><span class="sxs-lookup"><span data-stu-id="21a8c-2663">The checksum passes.</span></span>

```
<!-- Poland Identity Card-->
<Entity id="25E64989-ED5D-40CA-A939-6C14183BB7BF" patternsProximity="300" recommendedConfidence="85">
      <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_polish_national_id" />
          <Match idRef="Keyword_polish_national_id_passport_number" />
      </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="21a8c-2664">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="21a8c-2664">Keywords</span></span>

#### <a name="keywordpolishnationalidpassportnumber"></a><span data-ttu-id="21a8c-2665">Keyword_polish_national_id_passport_number</span><span class="sxs-lookup"><span data-stu-id="21a8c-2665">Keyword_polish_national_id_passport_number</span></span>

- <span data-ttu-id="21a8c-2666">Dowód osobisty</span><span class="sxs-lookup"><span data-stu-id="21a8c-2666">Dowód osobisty</span></span>
- <span data-ttu-id="21a8c-2667">Numer dowodu osobistego</span><span class="sxs-lookup"><span data-stu-id="21a8c-2667">Numer dowodu osobistego</span></span>
- <span data-ttu-id="21a8c-2668">Nazwa i numer dowodu osobistego</span><span class="sxs-lookup"><span data-stu-id="21a8c-2668">Nazwa i numer dowodu osobistego</span></span>
- <span data-ttu-id="21a8c-2669">Nazwa i NR dowodu osobistego</span><span class="sxs-lookup"><span data-stu-id="21a8c-2669">Nazwa i nr dowodu osobistego</span></span>
- <span data-ttu-id="21a8c-2670">Nazwa i nr dowodu tożsamości</span><span class="sxs-lookup"><span data-stu-id="21a8c-2670">Nazwa i nr dowodu tożsamości</span></span>
- <span data-ttu-id="21a8c-2671">Dowód Tożsamości</span><span class="sxs-lookup"><span data-stu-id="21a8c-2671">Dowód Tożsamości</span></span>
- <span data-ttu-id="21a8c-2672">Dow.</span><span class="sxs-lookup"><span data-stu-id="21a8c-2672">dow.</span></span> <span data-ttu-id="21a8c-2673">Opera.</span><span class="sxs-lookup"><span data-stu-id="21a8c-2673">os.</span></span>

   
## <a name="poland-national-id-pesel"></a><span data-ttu-id="21a8c-2674">ID nacional da Polônia (PESEL)</span><span class="sxs-lookup"><span data-stu-id="21a8c-2674">Poland National ID (PESEL)</span></span>

### <a name="format"></a><span data-ttu-id="21a8c-2675">Format</span><span class="sxs-lookup"><span data-stu-id="21a8c-2675">Format</span></span>

<span data-ttu-id="21a8c-2676">11 dígitos</span><span class="sxs-lookup"><span data-stu-id="21a8c-2676">11 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="21a8c-2677">Padrão</span><span class="sxs-lookup"><span data-stu-id="21a8c-2677">Pattern</span></span>

<span data-ttu-id="21a8c-2678">11 dígitos consecutivos</span><span class="sxs-lookup"><span data-stu-id="21a8c-2678">11 consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="21a8c-2679">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="21a8c-2679">Checksum</span></span>

<span data-ttu-id="21a8c-2680">Sim</span><span class="sxs-lookup"><span data-stu-id="21a8c-2680">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="21a8c-2681">Definição</span><span class="sxs-lookup"><span data-stu-id="21a8c-2681">Definition</span></span>

<span data-ttu-id="21a8c-2682">Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="21a8c-2682">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="21a8c-2683">A função Func_pesel_identification_number localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="21a8c-2683">The function Func_pesel_identification_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="21a8c-2684">Uma palavra-chave de Keyword_pesel_identification_number for encontrada.</span><span class="sxs-lookup"><span data-stu-id="21a8c-2684">A keyword from Keyword_pesel_identification_number is found.</span></span>
- <span data-ttu-id="21a8c-2685">A soma de verificação passa.</span><span class="sxs-lookup"><span data-stu-id="21a8c-2685">The checksum passes.</span></span>

```
<!-- Poland National ID (PESEL) -->      
<Entity id="E3AAF206-4297-412F-9E06-BA8487E22456" patternsProximity="300" recommendedConfidence="85">
      <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_pesel_identification_number" />
          <Match idRef="Keyword_pesel_identification_number" />
      </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="21a8c-2686">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="21a8c-2686">Keywords</span></span>

#### <a name="keywordpeselidentificationnumber"></a><span data-ttu-id="21a8c-2687">Keyword_pesel_identification_number</span><span class="sxs-lookup"><span data-stu-id="21a8c-2687">Keyword_pesel_identification_number</span></span>

- <span data-ttu-id="21a8c-2688">Nr PESEL</span><span class="sxs-lookup"><span data-stu-id="21a8c-2688">Nr PESEL</span></span>
- <span data-ttu-id="21a8c-2689">PESEL</span><span class="sxs-lookup"><span data-stu-id="21a8c-2689">PESEL</span></span>   

   
## <a name="poland-passport"></a><span data-ttu-id="21a8c-2690">Passaporte da Polônia</span><span class="sxs-lookup"><span data-stu-id="21a8c-2690">Poland Passport</span></span>

### <a name="format"></a><span data-ttu-id="21a8c-2691">Format</span><span class="sxs-lookup"><span data-stu-id="21a8c-2691">Format</span></span>

<span data-ttu-id="21a8c-2692">Duas letras e sete dígitos</span><span class="sxs-lookup"><span data-stu-id="21a8c-2692">Two letters and seven digits</span></span>

### <a name="pattern"></a><span data-ttu-id="21a8c-2693">Padrão</span><span class="sxs-lookup"><span data-stu-id="21a8c-2693">Pattern</span></span>

<span data-ttu-id="21a8c-2694">Duas letras (não diferencia maiúsculas de minúsculas) seguidas de sete dígitos</span><span class="sxs-lookup"><span data-stu-id="21a8c-2694">Two letters (not case sensitive) followed by seven digits</span></span>

### <a name="checksum"></a><span data-ttu-id="21a8c-2695">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="21a8c-2695">Checksum</span></span>

<span data-ttu-id="21a8c-2696">Sim</span><span class="sxs-lookup"><span data-stu-id="21a8c-2696">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="21a8c-2697">Definição</span><span class="sxs-lookup"><span data-stu-id="21a8c-2697">Definition</span></span>

<span data-ttu-id="21a8c-2698">Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="21a8c-2698">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="21a8c-2699">A função Func_polish_passport_number localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="21a8c-2699">The function Func_polish_passport_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="21a8c-2700">Uma palavra-chave de Keyword_polish_national_id_passport_number for encontrada.</span><span class="sxs-lookup"><span data-stu-id="21a8c-2700">A keyword from Keyword_polish_national_id_passport_number is found.</span></span>
- <span data-ttu-id="21a8c-2701">A soma de verificação passa.</span><span class="sxs-lookup"><span data-stu-id="21a8c-2701">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="21a8c-2702">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="21a8c-2702">Keywords</span></span>

#### <a name="keywordpolishnationalidpassportnumber"></a><span data-ttu-id="21a8c-2703">Keyword_polish_national_id_passport_number</span><span class="sxs-lookup"><span data-stu-id="21a8c-2703">Keyword_polish_national_id_passport_number</span></span>

- <span data-ttu-id="21a8c-2704">Numer paszportu</span><span class="sxs-lookup"><span data-stu-id="21a8c-2704">Numer paszportu</span></span>
- <span data-ttu-id="21a8c-2705">Nr.</span><span class="sxs-lookup"><span data-stu-id="21a8c-2705">Nr.</span></span> <span data-ttu-id="21a8c-2706">Paszportu</span><span class="sxs-lookup"><span data-stu-id="21a8c-2706">Paszportu</span></span>
- <span data-ttu-id="21a8c-2707">Paszport</span><span class="sxs-lookup"><span data-stu-id="21a8c-2707">Paszport</span></span>

   
## <a name="portugal-citizen-card-number"></a><span data-ttu-id="21a8c-2708">Número do Cartão de Cidadão de Portugal</span><span class="sxs-lookup"><span data-stu-id="21a8c-2708">Portugal Citizen Card Number</span></span>

### <a name="format"></a><span data-ttu-id="21a8c-2709">Format</span><span class="sxs-lookup"><span data-stu-id="21a8c-2709">Format</span></span>

<span data-ttu-id="21a8c-2710">Oito dígitos</span><span class="sxs-lookup"><span data-stu-id="21a8c-2710">Eight digits</span></span>

### <a name="pattern"></a><span data-ttu-id="21a8c-2711">Padrão</span><span class="sxs-lookup"><span data-stu-id="21a8c-2711">Pattern</span></span>

<span data-ttu-id="21a8c-2712">Oito dígitos</span><span class="sxs-lookup"><span data-stu-id="21a8c-2712">Eight digits</span></span>

### <a name="checksum"></a><span data-ttu-id="21a8c-2713">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="21a8c-2713">Checksum</span></span>

<span data-ttu-id="21a8c-2714">Não</span><span class="sxs-lookup"><span data-stu-id="21a8c-2714">No</span></span>

### <a name="definition"></a><span data-ttu-id="21a8c-2715">Definição</span><span class="sxs-lookup"><span data-stu-id="21a8c-2715">Definition</span></span>

<span data-ttu-id="21a8c-2716">Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="21a8c-2716">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="21a8c-2717">A expressão regular Regex_portugal_citizen_card localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="21a8c-2717">The regular expression Regex_portugal_citizen_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="21a8c-2718">Uma palavra-chave de Keyword_portugal_citizen_card for encontrada.</span><span class="sxs-lookup"><span data-stu-id="21a8c-2718">A keyword from Keyword_portugal_citizen_card is found.</span></span>

```
<!-- Portugal Citizen Card Number -->
<Entity id="91a7ece2-add4-4986-9a15-c84544d81ecd" recommendedConfidence="85" patternsProximity="300">
  <Pattern confidenceLevel="85">
     <IdMatch idRef="Regex_portugal_citizen_card"/>
     <Match idRef="Keyword_portugal_citizen_card"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="21a8c-2719">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="21a8c-2719">Keywords</span></span>

#### <a name="keywordportugalcitizencard"></a><span data-ttu-id="21a8c-2720">Keyword_portugal_citizen_card</span><span class="sxs-lookup"><span data-stu-id="21a8c-2720">Keyword_portugal_citizen_card</span></span>

- <span data-ttu-id="21a8c-2721">Cartão de Cidadão</span><span class="sxs-lookup"><span data-stu-id="21a8c-2721">Citizen Card</span></span>
- <span data-ttu-id="21a8c-2722">Cartão de Identidade Nacional</span><span class="sxs-lookup"><span data-stu-id="21a8c-2722">National ID Card</span></span>
- <span data-ttu-id="21a8c-2723">CC</span><span class="sxs-lookup"><span data-stu-id="21a8c-2723">CC</span></span>
- <span data-ttu-id="21a8c-2724">Cartão de Cidadão</span><span class="sxs-lookup"><span data-stu-id="21a8c-2724">Cartão de Cidadão</span></span>
- <span data-ttu-id="21a8c-2725">Bilhete de Identidade</span><span class="sxs-lookup"><span data-stu-id="21a8c-2725">Bilhete de Identidade</span></span>
   
## <a name="saudi-arabia-national-id"></a><span data-ttu-id="21a8c-2726">ID nacional da Arábia Saudita</span><span class="sxs-lookup"><span data-stu-id="21a8c-2726">Saudi Arabia National ID</span></span>

### <a name="format"></a><span data-ttu-id="21a8c-2727">Format</span><span class="sxs-lookup"><span data-stu-id="21a8c-2727">Format</span></span>

<span data-ttu-id="21a8c-2728">10 dígitos</span><span class="sxs-lookup"><span data-stu-id="21a8c-2728">10 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="21a8c-2729">Padrão</span><span class="sxs-lookup"><span data-stu-id="21a8c-2729">Pattern</span></span>

<span data-ttu-id="21a8c-2730">10 dígitos consecutivos</span><span class="sxs-lookup"><span data-stu-id="21a8c-2730">10 consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="21a8c-2731">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="21a8c-2731">Checksum</span></span>

<span data-ttu-id="21a8c-2732">Não</span><span class="sxs-lookup"><span data-stu-id="21a8c-2732">No</span></span>

### <a name="definition"></a><span data-ttu-id="21a8c-2733">Definição</span><span class="sxs-lookup"><span data-stu-id="21a8c-2733">Definition</span></span>

<span data-ttu-id="21a8c-2734">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="21a8c-2734">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="21a8c-2735">A expressão regular Regex_saudi_arabia_national_id localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="21a8c-2735">The regular expression Regex_saudi_arabia_national_id finds content that matches the pattern.</span></span>
- <span data-ttu-id="21a8c-2736">Uma palavra-chave de Keyword_saudi_arabia_national_id for encontrada.</span><span class="sxs-lookup"><span data-stu-id="21a8c-2736">A keyword from Keyword_saudi_arabia_national_id is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="21a8c-2737">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="21a8c-2737">Keywords</span></span>

#### <a name="keywordsaudiarabianationalid"></a><span data-ttu-id="21a8c-2738">Keyword_saudi_arabia_national_id</span><span class="sxs-lookup"><span data-stu-id="21a8c-2738">Keyword_saudi_arabia_national_id</span></span>

- <span data-ttu-id="21a8c-2739">Identification Card</span><span class="sxs-lookup"><span data-stu-id="21a8c-2739">Identification Card</span></span> 
- <span data-ttu-id="21a8c-2740">I card number</span><span class="sxs-lookup"><span data-stu-id="21a8c-2740">I card number</span></span> 
- <span data-ttu-id="21a8c-2741">ID number</span><span class="sxs-lookup"><span data-stu-id="21a8c-2741">ID number</span></span> 
- <span data-ttu-id="21a8c-2742">الوطنية الهوية بطاقة رقم</span><span class="sxs-lookup"><span data-stu-id="21a8c-2742">الوطنية الهوية بطاقة رقم</span></span> 

   
## <a name="singapore-national-registration-identity-card-nric-number"></a><span data-ttu-id="21a8c-2743">Número do Cartão de Identidade do Registro Nacional (NRIC) de Cingapura</span><span class="sxs-lookup"><span data-stu-id="21a8c-2743">Singapore National Registration Identity Card (NRIC) Number</span></span>

### <a name="format"></a><span data-ttu-id="21a8c-2744">Format</span><span class="sxs-lookup"><span data-stu-id="21a8c-2744">Format</span></span>

<span data-ttu-id="21a8c-2745">Nove letras e dígitos</span><span class="sxs-lookup"><span data-stu-id="21a8c-2745">Nine letters and digits</span></span>

### <a name="pattern"></a><span data-ttu-id="21a8c-2746">Padrão</span><span class="sxs-lookup"><span data-stu-id="21a8c-2746">Pattern</span></span>

- <span data-ttu-id="21a8c-2747">Nove letras e dígitos:</span><span class="sxs-lookup"><span data-stu-id="21a8c-2747">Nine letters and digits:</span></span>
- <span data-ttu-id="21a8c-2748">A letra "F", "G", "S" ou "T" (não diferenciam maiúsculas de minúsculas) </span><span class="sxs-lookup"><span data-stu-id="21a8c-2748">The letter "F", "G", "S", or "T" (not case sensitive)</span></span> 
- <span data-ttu-id="21a8c-2749">Sete dígitos </span><span class="sxs-lookup"><span data-stu-id="21a8c-2749">Seven digits</span></span> 
- <span data-ttu-id="21a8c-2750">Um dígito de verificação alfabético</span><span class="sxs-lookup"><span data-stu-id="21a8c-2750">An alphabetic check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="21a8c-2751">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="21a8c-2751">Checksum</span></span>

<span data-ttu-id="21a8c-2752">Sim</span><span class="sxs-lookup"><span data-stu-id="21a8c-2752">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="21a8c-2753">Definição</span><span class="sxs-lookup"><span data-stu-id="21a8c-2753">Definition</span></span>

<span data-ttu-id="21a8c-2754">Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="21a8c-2754">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="21a8c-2755">A expressão regular Regex_singapore_nric localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="21a8c-2755">The regular expression Regex_singapore_nric finds content that matches the pattern.</span></span>
- <span data-ttu-id="21a8c-2756">Uma palavra-chave de Keyword_singapore_nric for encontrada.</span><span class="sxs-lookup"><span data-stu-id="21a8c-2756">A keyword from Keyword_singapore_nric is found.</span></span>
- <span data-ttu-id="21a8c-2757">A soma de verificação passa.</span><span class="sxs-lookup"><span data-stu-id="21a8c-2757">The checksum passes.</span></span>

<span data-ttu-id="21a8c-2758">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="21a8c-2758">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="21a8c-2759">A expressão regular Regex_singapore_nric localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="21a8c-2759">The regular expression Regex_singapore_nric finds content that matches the pattern.</span></span>
- <span data-ttu-id="21a8c-2760">A soma de verificação passa.</span><span class="sxs-lookup"><span data-stu-id="21a8c-2760">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="21a8c-2761">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="21a8c-2761">Keywords</span></span>
   
#### <a name="keywordsingaporenric"></a><span data-ttu-id="21a8c-2762">Keyword_singapore_nric</span><span class="sxs-lookup"><span data-stu-id="21a8c-2762">Keyword_singapore_nric</span></span>

- <span data-ttu-id="21a8c-2763">Número do Cartão de Identidade do Registro Nacional</span><span class="sxs-lookup"><span data-stu-id="21a8c-2763">National Registration Identity Card</span></span> 
- <span data-ttu-id="21a8c-2764">Número do Cartão de Identidade</span><span class="sxs-lookup"><span data-stu-id="21a8c-2764">Identity Card Number</span></span> 
- <span data-ttu-id="21a8c-2765">NRIC</span><span class="sxs-lookup"><span data-stu-id="21a8c-2765">NRIC</span></span> 
- <span data-ttu-id="21a8c-2766">Liga</span><span class="sxs-lookup"><span data-stu-id="21a8c-2766">IC</span></span> 
- <span data-ttu-id="21a8c-2767">Número de Identificação Estrangeira</span><span class="sxs-lookup"><span data-stu-id="21a8c-2767">Foreign Identification Number</span></span> 
- <span data-ttu-id="21a8c-2768">ALETA</span><span class="sxs-lookup"><span data-stu-id="21a8c-2768">FIN</span></span> 
- <span data-ttu-id="21a8c-2769">身份证</span><span class="sxs-lookup"><span data-stu-id="21a8c-2769">身份证</span></span> 
- <span data-ttu-id="21a8c-2770">身份證</span><span class="sxs-lookup"><span data-stu-id="21a8c-2770">身份證</span></span> 
   
## <a name="south-africa-identification-number"></a><span data-ttu-id="21a8c-2771">Número de Identificação da África do Sul</span><span class="sxs-lookup"><span data-stu-id="21a8c-2771">South Africa Identification Number</span></span>

### <a name="format"></a><span data-ttu-id="21a8c-2772">Format</span><span class="sxs-lookup"><span data-stu-id="21a8c-2772">Format</span></span>

<span data-ttu-id="21a8c-2773">13 dígitos que podem conter espaços</span><span class="sxs-lookup"><span data-stu-id="21a8c-2773">13 digits that may contain spaces</span></span>

### <a name="pattern"></a><span data-ttu-id="21a8c-2774">Padrão</span><span class="sxs-lookup"><span data-stu-id="21a8c-2774">Pattern</span></span>

<span data-ttu-id="21a8c-2775">13 dígitos:</span><span class="sxs-lookup"><span data-stu-id="21a8c-2775">13 digits:</span></span>
- <span data-ttu-id="21a8c-2776">Seis dígitos no formato AAMMDD que são a data de nascimento</span><span class="sxs-lookup"><span data-stu-id="21a8c-2776">Six digits in the format YYMMDD which are the date of birth</span></span> 
- <span data-ttu-id="21a8c-2777">Quatro dígitos</span><span class="sxs-lookup"><span data-stu-id="21a8c-2777">Four digits</span></span> 
- <span data-ttu-id="21a8c-2778">Indicador de cidadania de um dígito </span><span class="sxs-lookup"><span data-stu-id="21a8c-2778">A single-digit citizenship indicator</span></span> 
- <span data-ttu-id="21a8c-2779">O dígito "8" ou "9" </span><span class="sxs-lookup"><span data-stu-id="21a8c-2779">The digit "8" or "9"</span></span> 
- <span data-ttu-id="21a8c-2780">Um dígito que é um dígito de soma de verificação</span><span class="sxs-lookup"><span data-stu-id="21a8c-2780">One digit which is a checksum digit</span></span>

### <a name="checksum"></a><span data-ttu-id="21a8c-2781">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="21a8c-2781">Checksum</span></span>

<span data-ttu-id="21a8c-2782">Sim</span><span class="sxs-lookup"><span data-stu-id="21a8c-2782">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="21a8c-2783">Definição</span><span class="sxs-lookup"><span data-stu-id="21a8c-2783">Definition</span></span>

<span data-ttu-id="21a8c-2784">Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="21a8c-2784">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="21a8c-2785">A função Func_south_africa_identification_number localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="21a8c-2785">The function Func_south_africa_identification_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="21a8c-2786">Uma palavra-chave de Keyword_south_africa_identification_number for encontrada.</span><span class="sxs-lookup"><span data-stu-id="21a8c-2786">A keyword from Keyword_south_africa_identification_number is found.</span></span>
- <span data-ttu-id="21a8c-2787">A soma de verificação passa.</span><span class="sxs-lookup"><span data-stu-id="21a8c-2787">The checksum passes.</span></span>

```
<!-- South Africa Identification Number -->
<Entity id="e2adf7cb-8ea6-4048-a2ed-d89eb65f2780" recommendedConfidence="85" patternsProximity="300">
  <Pattern confidenceLevel="85">
     <IdMatch idRef="Func_south_africa_identification_number"/>
     <Match idRef="Keyword_south_africa_identification_number"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="21a8c-2788">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="21a8c-2788">Keywords</span></span>
   
#### <a name="keywordsouthafricaidentificationnumber"></a><span data-ttu-id="21a8c-2789">Keyword_south_africa_identification_number</span><span class="sxs-lookup"><span data-stu-id="21a8c-2789">Keyword_south_africa_identification_number</span></span>

- <span data-ttu-id="21a8c-2790">Cartão de identidade</span><span class="sxs-lookup"><span data-stu-id="21a8c-2790">Identity card</span></span>
- <span data-ttu-id="21a8c-2791">ID</span><span class="sxs-lookup"><span data-stu-id="21a8c-2791">ID</span></span>
- <span data-ttu-id="21a8c-2792">Identificador</span><span class="sxs-lookup"><span data-stu-id="21a8c-2792">Identification</span></span> 
   
## <a name="south-korea-resident-registration-number"></a><span data-ttu-id="21a8c-2793">Número do Registro de Residentes da Coreia do Sul</span><span class="sxs-lookup"><span data-stu-id="21a8c-2793">South Korea Resident Registration Number</span></span>

### <a name="format"></a><span data-ttu-id="21a8c-2794">Format</span><span class="sxs-lookup"><span data-stu-id="21a8c-2794">Format</span></span>

<span data-ttu-id="21a8c-2795">13 dígitos que contém um hifen</span><span class="sxs-lookup"><span data-stu-id="21a8c-2795">13 digits containing a hyphen</span></span>

### <a name="pattern"></a><span data-ttu-id="21a8c-2796">Padrão</span><span class="sxs-lookup"><span data-stu-id="21a8c-2796">Pattern</span></span>

<span data-ttu-id="21a8c-2797">13 dígitos:</span><span class="sxs-lookup"><span data-stu-id="21a8c-2797">13 digits:</span></span>
- <span data-ttu-id="21a8c-2798">Seis dígitos no formato AAMMDD que são a data de nascimento</span><span class="sxs-lookup"><span data-stu-id="21a8c-2798">Six digits in the format YYMMDD which are the date of birth</span></span> 
- <span data-ttu-id="21a8c-2799">Um hífen</span><span class="sxs-lookup"><span data-stu-id="21a8c-2799">A hyphen</span></span> 
- <span data-ttu-id="21a8c-2800">Um dígito determinado pelo século e pelo sexo </span><span class="sxs-lookup"><span data-stu-id="21a8c-2800">One digit determined by the century and gender</span></span> 
- <span data-ttu-id="21a8c-2801">Código da região de nascimento de quatro dígitos </span><span class="sxs-lookup"><span data-stu-id="21a8c-2801">Four-digit region-of-birth code</span></span> 
- <span data-ttu-id="21a8c-2802">Um dígito usado para diferenciar as pessoas para as quais os números anteriores são idênticos </span><span class="sxs-lookup"><span data-stu-id="21a8c-2802">One digit used to differentiate people for whom the preceding numbers are identical</span></span> 
- <span data-ttu-id="21a8c-2803">Um dígito de verificação.</span><span class="sxs-lookup"><span data-stu-id="21a8c-2803">A check digit.</span></span>

### <a name="checksum"></a><span data-ttu-id="21a8c-2804">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="21a8c-2804">Checksum</span></span>

<span data-ttu-id="21a8c-2805">Sim</span><span class="sxs-lookup"><span data-stu-id="21a8c-2805">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="21a8c-2806">Definição</span><span class="sxs-lookup"><span data-stu-id="21a8c-2806">Definition</span></span>

<span data-ttu-id="21a8c-2807">Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="21a8c-2807">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="21a8c-2808">A função Func_south_korea_resident_number localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="21a8c-2808">The function Func_south_korea_resident_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="21a8c-2809">Uma palavra-chave de Keyword_south_korea_resident_number for encontrada.</span><span class="sxs-lookup"><span data-stu-id="21a8c-2809">A keyword from Keyword_south_korea_resident_number is found.</span></span>
- <span data-ttu-id="21a8c-2810">A soma de verificação passa.</span><span class="sxs-lookup"><span data-stu-id="21a8c-2810">The checksum passes.</span></span>

<span data-ttu-id="21a8c-2811">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="21a8c-2811">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="21a8c-2812">A função Func_south_korea_resident_number localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="21a8c-2812">The function Func_south_korea_resident_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="21a8c-2813">A soma de verificação passa.</span><span class="sxs-lookup"><span data-stu-id="21a8c-2813">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="21a8c-2814">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="21a8c-2814">Keywords</span></span>
   
#### <a name="keywordsouthkorearesidentnumber"></a><span data-ttu-id="21a8c-2815">Keyword_south_korea_resident_number</span><span class="sxs-lookup"><span data-stu-id="21a8c-2815">Keyword_south_korea_resident_number</span></span>

- <span data-ttu-id="21a8c-2816">Cartão de identidade nacional</span><span class="sxs-lookup"><span data-stu-id="21a8c-2816">National ID card</span></span> 
- <span data-ttu-id="21a8c-2817">Número de Registro do Cidadão</span><span class="sxs-lookup"><span data-stu-id="21a8c-2817">Citizen's Registration Number</span></span> 
- <span data-ttu-id="21a8c-2818">Jumin deungnok beonho</span><span class="sxs-lookup"><span data-stu-id="21a8c-2818">Jumin deungnok beonho</span></span> 
- <span data-ttu-id="21a8c-2819">RRN</span><span class="sxs-lookup"><span data-stu-id="21a8c-2819">RRN</span></span> 
- <span data-ttu-id="21a8c-2820">주민등록번호</span><span class="sxs-lookup"><span data-stu-id="21a8c-2820">주민등록번호</span></span>
   
## <a name="spain-social-security-number-ssn"></a><span data-ttu-id="21a8c-2821">Número de seguridade social da Espanha (SSN)</span><span class="sxs-lookup"><span data-stu-id="21a8c-2821">Spain Social Security Number (SSN)</span></span>

### <a name="format"></a><span data-ttu-id="21a8c-2822">Format</span><span class="sxs-lookup"><span data-stu-id="21a8c-2822">Format</span></span>

<span data-ttu-id="21a8c-2823">11 a 12 dígitos</span><span class="sxs-lookup"><span data-stu-id="21a8c-2823">11-12 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="21a8c-2824">Padrão</span><span class="sxs-lookup"><span data-stu-id="21a8c-2824">Pattern</span></span>

<span data-ttu-id="21a8c-2825">11-12 dígitos:</span><span class="sxs-lookup"><span data-stu-id="21a8c-2825">11-12 digits:</span></span>
- <span data-ttu-id="21a8c-2826">Dois dígitos</span><span class="sxs-lookup"><span data-stu-id="21a8c-2826">Two digits</span></span> 
- <span data-ttu-id="21a8c-2827">Uma barra (opcional)</span><span class="sxs-lookup"><span data-stu-id="21a8c-2827">A forward slash (optional)</span></span> 
- <span data-ttu-id="21a8c-2828">7 a 8 dígitos</span><span class="sxs-lookup"><span data-stu-id="21a8c-2828">7-8 digits</span></span> 
- <span data-ttu-id="21a8c-2829">Uma barra (opcional)</span><span class="sxs-lookup"><span data-stu-id="21a8c-2829">A forward slash (optional)</span></span> 
- <span data-ttu-id="21a8c-2830">Dois dígitos</span><span class="sxs-lookup"><span data-stu-id="21a8c-2830">Two digits</span></span>

### <a name="checksum"></a><span data-ttu-id="21a8c-2831">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="21a8c-2831">Checksum</span></span>

<span data-ttu-id="21a8c-2832">Sim</span><span class="sxs-lookup"><span data-stu-id="21a8c-2832">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="21a8c-2833">Definição</span><span class="sxs-lookup"><span data-stu-id="21a8c-2833">Definition</span></span>

<span data-ttu-id="21a8c-2834">Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="21a8c-2834">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="21a8c-2835">A função Func_spanish_social_security_number localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="21a8c-2835">The function Func_spanish_social_security_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="21a8c-2836">A soma de verificação passa.</span><span class="sxs-lookup"><span data-stu-id="21a8c-2836">The checksum passes.</span></span>

```
<!-- Spain SSN -->
<Entity id="5df987c0-8eae-4bce-ace7-b316347f3070" patternsProximity="300" recommendedConfidence="85">
    <Pattern confidenceLevel="85">
        <IdMatch idRef="Func_spanish_social_security_number" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="21a8c-2837">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="21a8c-2837">Keywords</span></span>

<span data-ttu-id="21a8c-2838">Nenhum</span><span class="sxs-lookup"><span data-stu-id="21a8c-2838">None</span></span>
   
## <a name="sweden-national-id"></a><span data-ttu-id="21a8c-2839">ID nacional da Suécia</span><span class="sxs-lookup"><span data-stu-id="21a8c-2839">Sweden National ID</span></span>

### <a name="format"></a><span data-ttu-id="21a8c-2840">Format</span><span class="sxs-lookup"><span data-stu-id="21a8c-2840">Format</span></span>

<span data-ttu-id="21a8c-2841">10 ou 12 dígitos e um delimitador opcional</span><span class="sxs-lookup"><span data-stu-id="21a8c-2841">10 or 12 digits and an optional delimiter</span></span>

### <a name="pattern"></a><span data-ttu-id="21a8c-2842">Padrão</span><span class="sxs-lookup"><span data-stu-id="21a8c-2842">Pattern</span></span>

<span data-ttu-id="21a8c-2843">10 ou 12 dígitos e um delimitador opcional:</span><span class="sxs-lookup"><span data-stu-id="21a8c-2843">10 or 12 digits and an optional delimiter:</span></span>
- <span data-ttu-id="21a8c-2844">2 a 4 dígitos (opcionais)</span><span class="sxs-lookup"><span data-stu-id="21a8c-2844">2-4 digits (optional)</span></span> 
- <span data-ttu-id="21a8c-2845">Seis dígitos no formato de data AAMMDD</span><span class="sxs-lookup"><span data-stu-id="21a8c-2845">Six digits in date format YYMMDD</span></span> 
- <span data-ttu-id="21a8c-2846">Um delimitador de "-" ou "+" (opcional), mais</span><span class="sxs-lookup"><span data-stu-id="21a8c-2846">Delimiter of "-" or "+" (optional), plus</span></span>
- <span data-ttu-id="21a8c-2847">Quatro dígitos</span><span class="sxs-lookup"><span data-stu-id="21a8c-2847">Four digits</span></span>

### <a name="checksum"></a><span data-ttu-id="21a8c-2848">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="21a8c-2848">Checksum</span></span>

<span data-ttu-id="21a8c-2849">Sim</span><span class="sxs-lookup"><span data-stu-id="21a8c-2849">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="21a8c-2850">Definição</span><span class="sxs-lookup"><span data-stu-id="21a8c-2850">Definition</span></span>

<span data-ttu-id="21a8c-2851">Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="21a8c-2851">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="21a8c-2852">A função Func_swedish_national_identifier localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="21a8c-2852">The function Func_swedish_national_identifier finds content that matches the pattern.</span></span>
- <span data-ttu-id="21a8c-2853">A soma de verificação passa.</span><span class="sxs-lookup"><span data-stu-id="21a8c-2853">The checksum passes.</span></span>

```
<!-- Sweden National ID -->
<Entity id="f69aaf40-79be-4fac-8f05-fd1910d272c8" patternsProximity="300" recommendedConfidence="85">
    <Pattern confidenceLevel="85">
        <IdMatch idRef="Func_swedish_national_identifier" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="21a8c-2854">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="21a8c-2854">Keywords</span></span>

<span data-ttu-id="21a8c-2855">Não</span><span class="sxs-lookup"><span data-stu-id="21a8c-2855">No</span></span>
   
## <a name="sweden-passport-number"></a><span data-ttu-id="21a8c-2856">Número de passaporte da Suécia</span><span class="sxs-lookup"><span data-stu-id="21a8c-2856">Sweden Passport Number</span></span>

### <a name="format"></a><span data-ttu-id="21a8c-2857">Format</span><span class="sxs-lookup"><span data-stu-id="21a8c-2857">Format</span></span>

<span data-ttu-id="21a8c-2858">Oito dígitos</span><span class="sxs-lookup"><span data-stu-id="21a8c-2858">Eight digits</span></span>

### <a name="pattern"></a><span data-ttu-id="21a8c-2859">Padrão</span><span class="sxs-lookup"><span data-stu-id="21a8c-2859">Pattern</span></span>

<span data-ttu-id="21a8c-2860">Oito dígitos consecutivos</span><span class="sxs-lookup"><span data-stu-id="21a8c-2860">Eight consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="21a8c-2861">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="21a8c-2861">Checksum</span></span>

<span data-ttu-id="21a8c-2862">Não</span><span class="sxs-lookup"><span data-stu-id="21a8c-2862">No</span></span>

### <a name="definition"></a><span data-ttu-id="21a8c-2863">Definição</span><span class="sxs-lookup"><span data-stu-id="21a8c-2863">Definition</span></span>

<span data-ttu-id="21a8c-2864">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="21a8c-2864">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="21a8c-2865">A expressão regular Regex_sweden_passport_number localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="21a8c-2865">The regular expression Regex_sweden_passport_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="21a8c-2866">Uma das seguintes opções for verdadeira:</span><span class="sxs-lookup"><span data-stu-id="21a8c-2866">One of the following is true:</span></span>
    - <span data-ttu-id="21a8c-2867">Uma palavra-chave de Keyword_passport for encontrada.</span><span class="sxs-lookup"><span data-stu-id="21a8c-2867">A keyword from Keyword_passport is found.</span></span>
    - <span data-ttu-id="21a8c-2868">Uma palavra-chave de Keyword_sweden_passport for encontrada.</span><span class="sxs-lookup"><span data-stu-id="21a8c-2868">A keyword from Keyword_sweden_passport is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="21a8c-2869">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="21a8c-2869">Keywords</span></span>
   
#### <a name="keywordswedenpassport"></a><span data-ttu-id="21a8c-2870">Keyword_sweden_passport</span><span class="sxs-lookup"><span data-stu-id="21a8c-2870">Keyword_sweden_passport</span></span>

- <span data-ttu-id="21a8c-2871">visa requirements</span><span class="sxs-lookup"><span data-stu-id="21a8c-2871">visa requirements</span></span> 
- <span data-ttu-id="21a8c-2872">Alien Registration Card</span><span class="sxs-lookup"><span data-stu-id="21a8c-2872">Alien Registration Card</span></span> 
- <span data-ttu-id="21a8c-2873">Schengen visas</span><span class="sxs-lookup"><span data-stu-id="21a8c-2873">Schengen visas</span></span> 
- <span data-ttu-id="21a8c-2874">Schengen visa</span><span class="sxs-lookup"><span data-stu-id="21a8c-2874">Schengen visa</span></span> 
- <span data-ttu-id="21a8c-2875">Visa Processing</span><span class="sxs-lookup"><span data-stu-id="21a8c-2875">Visa Processing</span></span> 
- <span data-ttu-id="21a8c-2876">Visa Type</span><span class="sxs-lookup"><span data-stu-id="21a8c-2876">Visa Type</span></span> 
- <span data-ttu-id="21a8c-2877">Single Entry</span><span class="sxs-lookup"><span data-stu-id="21a8c-2877">Single Entry</span></span> 
- <span data-ttu-id="21a8c-2878">Multiple Entry</span><span class="sxs-lookup"><span data-stu-id="21a8c-2878">Multiple Entry</span></span> 
- <span data-ttu-id="21a8c-2879">G3 Processing Fees</span><span class="sxs-lookup"><span data-stu-id="21a8c-2879">G3 Processing Fees</span></span> 

#### <a name="keywordpassport"></a><span data-ttu-id="21a8c-2880">Keyword_passport</span><span class="sxs-lookup"><span data-stu-id="21a8c-2880">Keyword_passport</span></span>

- <span data-ttu-id="21a8c-2881">Passport Number</span><span class="sxs-lookup"><span data-stu-id="21a8c-2881">Passport Number</span></span> 
- <span data-ttu-id="21a8c-2882">Passport No</span><span class="sxs-lookup"><span data-stu-id="21a8c-2882">Passport No</span></span> 
- <span data-ttu-id="21a8c-2883">Passport #</span><span class="sxs-lookup"><span data-stu-id="21a8c-2883">Passport #</span></span> 
- <span data-ttu-id="21a8c-2884">Passaport</span><span class="sxs-lookup"><span data-stu-id="21a8c-2884">Passport#</span></span> 
- <span data-ttu-id="21a8c-2885">Passportid</span><span class="sxs-lookup"><span data-stu-id="21a8c-2885">PassportID</span></span> 
- <span data-ttu-id="21a8c-2886">Passportno</span><span class="sxs-lookup"><span data-stu-id="21a8c-2886">Passportno</span></span> 
- <span data-ttu-id="21a8c-2887">passportnumber</span><span class="sxs-lookup"><span data-stu-id="21a8c-2887">passportnumber</span></span> 
- <span data-ttu-id="21a8c-2888">パスポート</span><span class="sxs-lookup"><span data-stu-id="21a8c-2888">パスポート</span></span> 
- <span data-ttu-id="21a8c-2889">パスポート番号</span><span class="sxs-lookup"><span data-stu-id="21a8c-2889">パスポート番号</span></span> 
- <span data-ttu-id="21a8c-2890">パスポートのNum</span><span class="sxs-lookup"><span data-stu-id="21a8c-2890">パスポートのNum</span></span> 
- <span data-ttu-id="21a8c-2891">パスポート #</span><span class="sxs-lookup"><span data-stu-id="21a8c-2891">パスポート＃</span></span> 
- <span data-ttu-id="21a8c-2892">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="21a8c-2892">Numéro de passeport</span></span> 
- <span data-ttu-id="21a8c-2893">Passeport n °</span><span class="sxs-lookup"><span data-stu-id="21a8c-2893">Passeport n °</span></span> 
- <span data-ttu-id="21a8c-2894">Passeport Non</span><span class="sxs-lookup"><span data-stu-id="21a8c-2894">Passeport Non</span></span> 
- <span data-ttu-id="21a8c-2895">Passeport #</span><span class="sxs-lookup"><span data-stu-id="21a8c-2895">Passeport #</span></span> 
- <span data-ttu-id="21a8c-2896">Passeport #</span><span class="sxs-lookup"><span data-stu-id="21a8c-2896">Passeport#</span></span> 
- <span data-ttu-id="21a8c-2897">PasseportNon</span><span class="sxs-lookup"><span data-stu-id="21a8c-2897">PasseportNon</span></span> 
- <span data-ttu-id="21a8c-2898">Passeportn °</span><span class="sxs-lookup"><span data-stu-id="21a8c-2898">Passeportn °</span></span> 
   
## <a name="swift-code"></a><span data-ttu-id="21a8c-2899">Código SWIFT</span><span class="sxs-lookup"><span data-stu-id="21a8c-2899">SWIFT Code</span></span>

### <a name="format"></a><span data-ttu-id="21a8c-2900">Format</span><span class="sxs-lookup"><span data-stu-id="21a8c-2900">Format</span></span>

<span data-ttu-id="21a8c-2901">Quatro letras seguidas por 5 a 31 letras ou dígitos</span><span class="sxs-lookup"><span data-stu-id="21a8c-2901">Four letters followed by 5-31 letters or digits</span></span>

### <a name="pattern"></a><span data-ttu-id="21a8c-2902">Padrão</span><span class="sxs-lookup"><span data-stu-id="21a8c-2902">Pattern</span></span>

<span data-ttu-id="21a8c-2903">Quatro letras seguidas por 5 a 31 letras ou dígitos:</span><span class="sxs-lookup"><span data-stu-id="21a8c-2903">Four letters followed by 5-31 letters or digits:</span></span>
- <span data-ttu-id="21a8c-2904">Código bancário de quatro letras (não diferencia maiúsculas de minúsculas)</span><span class="sxs-lookup"><span data-stu-id="21a8c-2904">Four-letter bank code (not case sensitive)</span></span> 
- <span data-ttu-id="21a8c-2905">Um espaço opcional</span><span class="sxs-lookup"><span data-stu-id="21a8c-2905">An optional space</span></span> 
- <span data-ttu-id="21a8c-2906">4 a 28 letras ou dígitos (o número de conta bancária básica (BBAN))</span><span class="sxs-lookup"><span data-stu-id="21a8c-2906">4-28 letters or digits (the Basic Bank Account Number (BBAN))</span></span> 
- <span data-ttu-id="21a8c-2907">Um espaço opcional</span><span class="sxs-lookup"><span data-stu-id="21a8c-2907">An optional space</span></span> 
- <span data-ttu-id="21a8c-2908">1 a 3 letras ou dígitos (restante do BBAN)</span><span class="sxs-lookup"><span data-stu-id="21a8c-2908">1-3 letters or digits (remainder of the BBAN)</span></span>

### <a name="checksum"></a><span data-ttu-id="21a8c-2909">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="21a8c-2909">Checksum</span></span>

<span data-ttu-id="21a8c-2910">Não</span><span class="sxs-lookup"><span data-stu-id="21a8c-2910">No</span></span>

### <a name="definition"></a><span data-ttu-id="21a8c-2911">Definição</span><span class="sxs-lookup"><span data-stu-id="21a8c-2911">Definition</span></span>

<span data-ttu-id="21a8c-2912">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="21a8c-2912">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="21a8c-2913">A expressão regular Regex_swift localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="21a8c-2913">The regular expression Regex_swift finds content that matches the pattern.</span></span>
- <span data-ttu-id="21a8c-2914">Uma palavra-chave de Keyword_swift for encontrada.</span><span class="sxs-lookup"><span data-stu-id="21a8c-2914">A keyword from Keyword_swift is found.</span></span>

```
<Entity id="cb2ab58c-9cb8-4c81-baf8-a4e106791df4" patternsProximity="300" recommendedConfidence="75">
<Pattern confidenceLevel="75">
        <IdMatch idRef="Regex_swift" />
        <Match idRef="Keyword_swift" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="21a8c-2915">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="21a8c-2915">Keywords</span></span>
   
#### <a name="keywordswift"></a><span data-ttu-id="21a8c-2916">Keyword_swift</span><span class="sxs-lookup"><span data-stu-id="21a8c-2916">Keyword_swift</span></span>

- <span data-ttu-id="21a8c-2917">international organization for standardization 9362</span><span class="sxs-lookup"><span data-stu-id="21a8c-2917">international organization for standardization 9362</span></span> 
- <span data-ttu-id="21a8c-2918">iso 9362</span><span class="sxs-lookup"><span data-stu-id="21a8c-2918">iso 9362</span></span> 
- <span data-ttu-id="21a8c-2919">iso9362</span><span class="sxs-lookup"><span data-stu-id="21a8c-2919">iso9362</span></span> 
- <span data-ttu-id="21a8c-2920">Swift\#</span><span class="sxs-lookup"><span data-stu-id="21a8c-2920">swift\#</span></span> 
- <span data-ttu-id="21a8c-2921">swiftcode</span><span class="sxs-lookup"><span data-stu-id="21a8c-2921">swiftcode</span></span> 
- <span data-ttu-id="21a8c-2922">swiftnumber</span><span class="sxs-lookup"><span data-stu-id="21a8c-2922">swiftnumber</span></span> 
- <span data-ttu-id="21a8c-2923">swiftroutingnumber</span><span class="sxs-lookup"><span data-stu-id="21a8c-2923">swiftroutingnumber</span></span> 
- <span data-ttu-id="21a8c-2924">swift code</span><span class="sxs-lookup"><span data-stu-id="21a8c-2924">swift code</span></span> 
- <span data-ttu-id="21a8c-2925">swift number #</span><span class="sxs-lookup"><span data-stu-id="21a8c-2925">swift number #</span></span> 
- <span data-ttu-id="21a8c-2926">swift routing number</span><span class="sxs-lookup"><span data-stu-id="21a8c-2926">swift routing number</span></span> 
- <span data-ttu-id="21a8c-2927">bic number</span><span class="sxs-lookup"><span data-stu-id="21a8c-2927">bic number</span></span> 
- <span data-ttu-id="21a8c-2928">bic code</span><span class="sxs-lookup"><span data-stu-id="21a8c-2928">bic code</span></span> 
- <span data-ttu-id="21a8c-2929">BIC\#</span><span class="sxs-lookup"><span data-stu-id="21a8c-2929">bic \#</span></span> 
- <span data-ttu-id="21a8c-2930">BIC\#</span><span class="sxs-lookup"><span data-stu-id="21a8c-2930">bic\#</span></span> 
- <span data-ttu-id="21a8c-2931">bank identifier code</span><span class="sxs-lookup"><span data-stu-id="21a8c-2931">bank identifier code</span></span> 
- <span data-ttu-id="21a8c-2932">標準化 9362</span><span class="sxs-lookup"><span data-stu-id="21a8c-2932">標準化9362</span></span> 
- <span data-ttu-id="21a8c-2933">迅速 #</span><span class="sxs-lookup"><span data-stu-id="21a8c-2933">迅速＃</span></span> 
- <span data-ttu-id="21a8c-2934">SWIFTコード</span><span class="sxs-lookup"><span data-stu-id="21a8c-2934">SWIFTコード</span></span> 
- <span data-ttu-id="21a8c-2935">SWIFT番号</span><span class="sxs-lookup"><span data-stu-id="21a8c-2935">SWIFT番号</span></span> 
- <span data-ttu-id="21a8c-2936">迅速なルーティング番号</span><span class="sxs-lookup"><span data-stu-id="21a8c-2936">迅速なルーティング番号</span></span> 
- <span data-ttu-id="21a8c-2937">BIC番号</span><span class="sxs-lookup"><span data-stu-id="21a8c-2937">BIC番号</span></span> 
- <span data-ttu-id="21a8c-2938">BICコード</span><span class="sxs-lookup"><span data-stu-id="21a8c-2938">BICコード</span></span> 
- <span data-ttu-id="21a8c-2939">銀行識別コードのための国際組織</span><span class="sxs-lookup"><span data-stu-id="21a8c-2939">銀行識別コードのための国際組織</span></span> 
- <span data-ttu-id="21a8c-2940">Organisation internationale de normalisation 9362</span><span class="sxs-lookup"><span data-stu-id="21a8c-2940">Organisation internationale de normalisation 9362</span></span> 
- <span data-ttu-id="21a8c-2941">rápida\#</span><span class="sxs-lookup"><span data-stu-id="21a8c-2941">rapide \#</span></span> 
- <span data-ttu-id="21a8c-2942">code SWIFT</span><span class="sxs-lookup"><span data-stu-id="21a8c-2942">code SWIFT</span></span> 
- <span data-ttu-id="21a8c-2943">le numéro de swift</span><span class="sxs-lookup"><span data-stu-id="21a8c-2943">le numéro de swift</span></span> 
- <span data-ttu-id="21a8c-2944">swift numéro d'acheminement</span><span class="sxs-lookup"><span data-stu-id="21a8c-2944">swift numéro d'acheminement</span></span> 
- <span data-ttu-id="21a8c-2945">le numéro BIC</span><span class="sxs-lookup"><span data-stu-id="21a8c-2945">le numéro BIC</span></span> 
- <span data-ttu-id="21a8c-2946">\#BIC</span><span class="sxs-lookup"><span data-stu-id="21a8c-2946">\# BIC</span></span> 
- <span data-ttu-id="21a8c-2947">code identificateur de banque</span><span class="sxs-lookup"><span data-stu-id="21a8c-2947">code identificateur de banque</span></span> 
   
## <a name="taiwan-national-id"></a><span data-ttu-id="21a8c-2948">ID nacional de Taiwan</span><span class="sxs-lookup"><span data-stu-id="21a8c-2948">Taiwan National ID</span></span>

### <a name="format"></a><span data-ttu-id="21a8c-2949">Format</span><span class="sxs-lookup"><span data-stu-id="21a8c-2949">Format</span></span>

<span data-ttu-id="21a8c-2950">Uma letra (em inglês) seguida de nove dígitos</span><span class="sxs-lookup"><span data-stu-id="21a8c-2950">One letter (in English) followed by nine digits</span></span>

### <a name="pattern"></a><span data-ttu-id="21a8c-2951">Padrão</span><span class="sxs-lookup"><span data-stu-id="21a8c-2951">Pattern</span></span>

<span data-ttu-id="21a8c-2952">Uma letra (em inglês) seguida de nove dígitos:</span><span class="sxs-lookup"><span data-stu-id="21a8c-2952">One letter (in English) followed by nine digits:</span></span>
- <span data-ttu-id="21a8c-2953">Uma letra (em inglês, não diferencia maiúscula de minúscula)</span><span class="sxs-lookup"><span data-stu-id="21a8c-2953">One letter (in English, not case sensitive)</span></span> 
- <span data-ttu-id="21a8c-2954">O dígito "1" ou "2"</span><span class="sxs-lookup"><span data-stu-id="21a8c-2954">The digit "1" or "2"</span></span> 
- <span data-ttu-id="21a8c-2955">Oito dígitos</span><span class="sxs-lookup"><span data-stu-id="21a8c-2955">Eight digits</span></span>

### <a name="checksum"></a><span data-ttu-id="21a8c-2956">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="21a8c-2956">Checksum</span></span>

<span data-ttu-id="21a8c-2957">Sim</span><span class="sxs-lookup"><span data-stu-id="21a8c-2957">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="21a8c-2958">Definição</span><span class="sxs-lookup"><span data-stu-id="21a8c-2958">Definition</span></span>

<span data-ttu-id="21a8c-2959">Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="21a8c-2959">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="21a8c-2960">A função Func_taiwanese_national_id localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="21a8c-2960">The function Func_taiwanese_national_id finds content that matches the pattern.</span></span>
- <span data-ttu-id="21a8c-2961">Uma palavra-chave de Keyword_taiwanese_national_id for encontrada.</span><span class="sxs-lookup"><span data-stu-id="21a8c-2961">A keyword from Keyword_taiwanese_national_id is found.</span></span>
- <span data-ttu-id="21a8c-2962">A soma de verificação passa.</span><span class="sxs-lookup"><span data-stu-id="21a8c-2962">The checksum passes.</span></span>

```
<!-- Taiwanese National ID -->
<Entity id="4C7BFC34-8DD1-421D-8FB7-6C6182C2AF03" patternsProximity="300" recommendedConfidence="85">
      <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_taiwanese_national_id" />
          <Match idRef="Keyword_taiwanese_national_id" />
      </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="21a8c-2963">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="21a8c-2963">Keywords</span></span>

#### <a name="keywordtaiwanesenationalid"></a><span data-ttu-id="21a8c-2964">Keyword_taiwanese_national_id</span><span class="sxs-lookup"><span data-stu-id="21a8c-2964">Keyword_taiwanese_national_id</span></span>

- <span data-ttu-id="21a8c-2965">身份證字號</span><span class="sxs-lookup"><span data-stu-id="21a8c-2965">身份證字號</span></span> 
- <span data-ttu-id="21a8c-2966">身份證</span><span class="sxs-lookup"><span data-stu-id="21a8c-2966">身份證</span></span> 
- <span data-ttu-id="21a8c-2967">身份證號碼</span><span class="sxs-lookup"><span data-stu-id="21a8c-2967">身份證號碼</span></span> 
- <span data-ttu-id="21a8c-2968">身份證號</span><span class="sxs-lookup"><span data-stu-id="21a8c-2968">身份證號</span></span> 
- <span data-ttu-id="21a8c-2969">身分證字號</span><span class="sxs-lookup"><span data-stu-id="21a8c-2969">身分證字號</span></span> 
- <span data-ttu-id="21a8c-2970">身分證</span><span class="sxs-lookup"><span data-stu-id="21a8c-2970">身分證</span></span> 
- <span data-ttu-id="21a8c-2971">身分證號碼</span><span class="sxs-lookup"><span data-stu-id="21a8c-2971">身分證號碼</span></span> 
- <span data-ttu-id="21a8c-2972">身份證號</span><span class="sxs-lookup"><span data-stu-id="21a8c-2972">身份證號</span></span> 
- <span data-ttu-id="21a8c-2973">身分證統一編號</span><span class="sxs-lookup"><span data-stu-id="21a8c-2973">身分證統一編號</span></span> 
- <span data-ttu-id="21a8c-2974">國民身分證統一編號</span><span class="sxs-lookup"><span data-stu-id="21a8c-2974">國民身分證統一編號</span></span> 
- <span data-ttu-id="21a8c-2975">簽名</span><span class="sxs-lookup"><span data-stu-id="21a8c-2975">簽名</span></span> 
- <span data-ttu-id="21a8c-2976">蓋章</span><span class="sxs-lookup"><span data-stu-id="21a8c-2976">蓋章</span></span> 
- <span data-ttu-id="21a8c-2977">簽名或蓋章</span><span class="sxs-lookup"><span data-stu-id="21a8c-2977">簽名或蓋章</span></span> 
- <span data-ttu-id="21a8c-2978">簽章</span><span class="sxs-lookup"><span data-stu-id="21a8c-2978">簽章</span></span>   
   
## <a name="taiwan-passport-number"></a><span data-ttu-id="21a8c-2979">	Número de passaporte de Taiwan</span><span class="sxs-lookup"><span data-stu-id="21a8c-2979">Taiwan Passport Number</span></span>

### <a name="format"></a><span data-ttu-id="21a8c-2980">Format</span><span class="sxs-lookup"><span data-stu-id="21a8c-2980">Format</span></span>

- <span data-ttu-id="21a8c-2981">Número de passaporte biométrico: nove dígitos</span><span class="sxs-lookup"><span data-stu-id="21a8c-2981">Biometric passport number: Nine digits</span></span>
- <span data-ttu-id="21a8c-2982">Número de passaporte não biométrico: nove dígitos</span><span class="sxs-lookup"><span data-stu-id="21a8c-2982">Non-biometric passport number: Nine digits</span></span>

### <a name="pattern"></a><span data-ttu-id="21a8c-2983">Padrão</span><span class="sxs-lookup"><span data-stu-id="21a8c-2983">Pattern</span></span>
<span data-ttu-id="21a8c-2984">Número de passaporte biométrico:</span><span class="sxs-lookup"><span data-stu-id="21a8c-2984">Biometric passport number:</span></span>
- <span data-ttu-id="21a8c-2985">O dígito "3" </span><span class="sxs-lookup"><span data-stu-id="21a8c-2985">The digit "3"</span></span> 
- <span data-ttu-id="21a8c-2986">Oito dígitos</span><span class="sxs-lookup"><span data-stu-id="21a8c-2986">Eight digits</span></span>

<span data-ttu-id="21a8c-2987">Número de passaporte não biométrico:</span><span class="sxs-lookup"><span data-stu-id="21a8c-2987">Non-biometric passport number:</span></span>
- <span data-ttu-id="21a8c-2988">Nove dígitos</span><span class="sxs-lookup"><span data-stu-id="21a8c-2988">Nine digits</span></span>

### <a name="checksum"></a><span data-ttu-id="21a8c-2989">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="21a8c-2989">Checksum</span></span>

<span data-ttu-id="21a8c-2990">Não</span><span class="sxs-lookup"><span data-stu-id="21a8c-2990">No</span></span>

### <a name="definition"></a><span data-ttu-id="21a8c-2991">Definição</span><span class="sxs-lookup"><span data-stu-id="21a8c-2991">Definition</span></span>

<span data-ttu-id="21a8c-2992">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="21a8c-2992">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="21a8c-2993">A expressão regular Regex_taiwan_passport localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="21a8c-2993">The regular expression Regex_taiwan_passport finds content that matches the pattern.</span></span>
- <span data-ttu-id="21a8c-2994">Uma palavra-chave de Keyword_taiwan_passport for encontrada.</span><span class="sxs-lookup"><span data-stu-id="21a8c-2994">A keyword from Keyword_taiwan_passport is found.</span></span>

```
<!-- Taiwan Passport Number -->
<Entity id="e7251cb4-4c2c-41df-963e-924eb3dae04a" recommendedConfidence="75" patternsProximity="300">
  <Pattern confidenceLevel="75">
     <IdMatch idRef="Regex_taiwan_passport"/>
     <Match idRef="Keyword_taiwan_passport"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="21a8c-2995">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="21a8c-2995">Keywords</span></span>

#### <a name="keywordtaiwanpassport"></a><span data-ttu-id="21a8c-2996">Keyword_taiwan_passport</span><span class="sxs-lookup"><span data-stu-id="21a8c-2996">Keyword_taiwan_passport</span></span>

- <span data-ttu-id="21a8c-2997">Número de passaporte ROC</span><span class="sxs-lookup"><span data-stu-id="21a8c-2997">ROC passport number</span></span> 
- <span data-ttu-id="21a8c-2998">Número de passaporte</span><span class="sxs-lookup"><span data-stu-id="21a8c-2998">Passport number</span></span> 
- <span data-ttu-id="21a8c-2999">Nº de passaporte</span><span class="sxs-lookup"><span data-stu-id="21a8c-2999">Passport no</span></span> 
- <span data-ttu-id="21a8c-3000">Núm de Passaporte</span><span class="sxs-lookup"><span data-stu-id="21a8c-3000">Passport Num</span></span> 
- <span data-ttu-id="21a8c-3001">Passport #</span><span class="sxs-lookup"><span data-stu-id="21a8c-3001">Passport #</span></span> 
- <span data-ttu-id="21a8c-3002">护照</span><span class="sxs-lookup"><span data-stu-id="21a8c-3002">护照</span></span> 
- <span data-ttu-id="21a8c-3003">中華民國護照</span><span class="sxs-lookup"><span data-stu-id="21a8c-3003">中華民國護照</span></span> 
- <span data-ttu-id="21a8c-3004">Zhōnghuá Mínguó hùzhào</span><span class="sxs-lookup"><span data-stu-id="21a8c-3004">Zhōnghuá Mínguó hùzhào</span></span>
   
## <a name="taiwan-resident-certificate-arctarc-number"></a><span data-ttu-id="21a8c-3005">Número do Certificado de residente de Taiwan (ARC/TARC)</span><span class="sxs-lookup"><span data-stu-id="21a8c-3005">Taiwan Resident Certificate (ARC/TARC) Number</span></span>

### <a name="format"></a><span data-ttu-id="21a8c-3006">Format</span><span class="sxs-lookup"><span data-stu-id="21a8c-3006">Format</span></span>

<span data-ttu-id="21a8c-3007">10 letras e dígitos</span><span class="sxs-lookup"><span data-stu-id="21a8c-3007">10 letters and digits</span></span>

### <a name="pattern"></a><span data-ttu-id="21a8c-3008">Padrão</span><span class="sxs-lookup"><span data-stu-id="21a8c-3008">Pattern</span></span>

<span data-ttu-id="21a8c-3009">10 letras e dígitos:</span><span class="sxs-lookup"><span data-stu-id="21a8c-3009">10 letters and digits:</span></span>
- <span data-ttu-id="21a8c-3010">Duas letras (não diferenciam maiúsculas de minúsculas)</span><span class="sxs-lookup"><span data-stu-id="21a8c-3010">Two letters (not case sensitive)</span></span> 
- <span data-ttu-id="21a8c-3011">Oito dígitos</span><span class="sxs-lookup"><span data-stu-id="21a8c-3011">Eight digits</span></span>

### <a name="checksum"></a><span data-ttu-id="21a8c-3012">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="21a8c-3012">Checksum</span></span>

<span data-ttu-id="21a8c-3013">Não</span><span class="sxs-lookup"><span data-stu-id="21a8c-3013">No</span></span>

### <a name="definition"></a><span data-ttu-id="21a8c-3014">Definição</span><span class="sxs-lookup"><span data-stu-id="21a8c-3014">Definition</span></span>

<span data-ttu-id="21a8c-3015">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="21a8c-3015">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="21a8c-3016">A expressão regular Regex_taiwan_resident_certificate localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="21a8c-3016">The regular expression Regex_taiwan_resident_certificate finds content that matches the pattern.</span></span>
- <span data-ttu-id="21a8c-3017">Uma palavra-chave de Keyword_taiwan_resident_certificate for encontrada.</span><span class="sxs-lookup"><span data-stu-id="21a8c-3017">A keyword from Keyword_taiwan_resident_certificate is found.</span></span>

```
<!-- Taiwan Resident Certificate (ARC/TARC) -->
<Entity id="48269fec-05ea-46ea-b326-f5623a58c6e9" recommendedConfidence="75" patternsProximity="300">
  <Pattern confidenceLevel="75">
     <IdMatch idRef="Regex_taiwan_resident_certificate"/>
     <Match idRef="Keyword_taiwan_resident_certificate"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="21a8c-3018">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="21a8c-3018">Keywords</span></span>

#### <a name="keywordtaiwanresidentcertificate"></a><span data-ttu-id="21a8c-3019">Keyword_taiwan_resident_certificate</span><span class="sxs-lookup"><span data-stu-id="21a8c-3019">Keyword_taiwan_resident_certificate</span></span>

- <span data-ttu-id="21a8c-3020">Certificado de Residente</span><span class="sxs-lookup"><span data-stu-id="21a8c-3020">Resident Certificate</span></span> 
- <span data-ttu-id="21a8c-3021">Cert de Residente</span><span class="sxs-lookup"><span data-stu-id="21a8c-3021">Resident Cert</span></span> 
- <span data-ttu-id="21a8c-3022">Cert. de Residente
</span><span class="sxs-lookup"><span data-stu-id="21a8c-3022">Resident Cert.</span></span> 
- <span data-ttu-id="21a8c-3023">Cartão de identificação</span><span class="sxs-lookup"><span data-stu-id="21a8c-3023">Identification card</span></span> 
- <span data-ttu-id="21a8c-3024">Certificado de Residente Alien</span><span class="sxs-lookup"><span data-stu-id="21a8c-3024">Alien Resident Certificate</span></span> 
- <span data-ttu-id="21a8c-3025">ARCO</span><span class="sxs-lookup"><span data-stu-id="21a8c-3025">ARC</span></span> 
- <span data-ttu-id="21a8c-3026">Certificado de Residente da Área de Taiwan</span><span class="sxs-lookup"><span data-stu-id="21a8c-3026">Taiwan Area Resident Certificate</span></span> 
- <span data-ttu-id="21a8c-3027">TARC</span><span class="sxs-lookup"><span data-stu-id="21a8c-3027">TARC</span></span> 
- <span data-ttu-id="21a8c-3028">居留證</span><span class="sxs-lookup"><span data-stu-id="21a8c-3028">居留證</span></span> 
- <span data-ttu-id="21a8c-3029">外僑居留證</span><span class="sxs-lookup"><span data-stu-id="21a8c-3029">外僑居留證</span></span> 
- <span data-ttu-id="21a8c-3030">台灣地區居留證</span><span class="sxs-lookup"><span data-stu-id="21a8c-3030">台灣地區居留證</span></span> 

## <a name="thai-population-identification-code"></a><span data-ttu-id="21a8c-3031">Código de identificação de população em tailandês</span><span class="sxs-lookup"><span data-stu-id="21a8c-3031">Thai Population Identification Code</span></span>

### <a name="format"></a><span data-ttu-id="21a8c-3032">Format</span><span class="sxs-lookup"><span data-stu-id="21a8c-3032">Format</span></span>

<span data-ttu-id="21a8c-3033">13 dígitos</span><span class="sxs-lookup"><span data-stu-id="21a8c-3033">13 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="21a8c-3034">Padrão</span><span class="sxs-lookup"><span data-stu-id="21a8c-3034">Pattern</span></span>

<span data-ttu-id="21a8c-3035">13 dígitos:</span><span class="sxs-lookup"><span data-stu-id="21a8c-3035">13 digits:</span></span>
- <span data-ttu-id="21a8c-3036">O primeiro dígito não é 0 ou 9</span><span class="sxs-lookup"><span data-stu-id="21a8c-3036">First digit is not 0 or 9</span></span> 
- <span data-ttu-id="21a8c-3037">12 dígitos</span><span class="sxs-lookup"><span data-stu-id="21a8c-3037">12 digits</span></span>

### <a name="checksum"></a><span data-ttu-id="21a8c-3038">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="21a8c-3038">Checksum</span></span>

<span data-ttu-id="21a8c-3039">Sim</span><span class="sxs-lookup"><span data-stu-id="21a8c-3039">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="21a8c-3040">Definição</span><span class="sxs-lookup"><span data-stu-id="21a8c-3040">Definition</span></span>

<span data-ttu-id="21a8c-3041">Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="21a8c-3041">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="21a8c-3042">A função Func_Thai_Citizen_Id localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="21a8c-3042">The function Func_Thai_Citizen_Id finds content that matches the pattern.</span></span>
- <span data-ttu-id="21a8c-3043">Uma palavra-chave de Keyword_Thai_Citizen_Id for encontrada.</span><span class="sxs-lookup"><span data-stu-id="21a8c-3043">A keyword from Keyword_Thai_Citizen_Id is found.</span></span>

<span data-ttu-id="21a8c-3044">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="21a8c-3044">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="21a8c-3045">A função Func_Thai_Citizen_Id localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="21a8c-3045">The function Func_Thai_Citizen_Id finds content that matches the pattern.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="21a8c-3046">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="21a8c-3046">Keywords</span></span>

#### <a name="keywordthaicitizenid"></a><span data-ttu-id="21a8c-3047">Keyword_Thai_Citizen_Id</span><span class="sxs-lookup"><span data-stu-id="21a8c-3047">Keyword_Thai_Citizen_Id</span></span>

- <span data-ttu-id="21a8c-3048">Número de Identificação</span><span class="sxs-lookup"><span data-stu-id="21a8c-3048">ID Number</span></span>
- <span data-ttu-id="21a8c-3049">Número de identificação</span><span class="sxs-lookup"><span data-stu-id="21a8c-3049">Identification Number</span></span>
- <span data-ttu-id="21a8c-3050">บัตรประชาชน</span><span class="sxs-lookup"><span data-stu-id="21a8c-3050">บัตรประชาชน</span></span>
- <span data-ttu-id="21a8c-3051">รหัสบัตรประชาชน</span><span class="sxs-lookup"><span data-stu-id="21a8c-3051">รหัสบัตรประชาชน</span></span>
- <span data-ttu-id="21a8c-3052">บัตรประชาชน</span><span class="sxs-lookup"><span data-stu-id="21a8c-3052">บัตรประชาชน</span></span>
- <span data-ttu-id="21a8c-3053">รหัสบัตรประชาชน</span><span class="sxs-lookup"><span data-stu-id="21a8c-3053">รหัสบัตรประชาชน</span></span>
  
## <a name="turkish-national-identification-number"></a><span data-ttu-id="21a8c-3054">Número de identificação nacional turco</span><span class="sxs-lookup"><span data-stu-id="21a8c-3054">Turkish National Identification Number</span></span>

### <a name="format"></a><span data-ttu-id="21a8c-3055">Format</span><span class="sxs-lookup"><span data-stu-id="21a8c-3055">Format</span></span>

<span data-ttu-id="21a8c-3056">11 dígitos</span><span class="sxs-lookup"><span data-stu-id="21a8c-3056">11 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="21a8c-3057">Padrão</span><span class="sxs-lookup"><span data-stu-id="21a8c-3057">Pattern</span></span>

<span data-ttu-id="21a8c-3058">11 dígitos</span><span class="sxs-lookup"><span data-stu-id="21a8c-3058">11 digits</span></span>

### <a name="checksum"></a><span data-ttu-id="21a8c-3059">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="21a8c-3059">Checksum</span></span>

<span data-ttu-id="21a8c-3060">Sim</span><span class="sxs-lookup"><span data-stu-id="21a8c-3060">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="21a8c-3061">Definição</span><span class="sxs-lookup"><span data-stu-id="21a8c-3061">Definition</span></span>

<span data-ttu-id="21a8c-3062">Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="21a8c-3062">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="21a8c-3063">A função Func_Turkish_National_Id localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="21a8c-3063">The function Func_Turkish_National_Id finds content that matches the pattern.</span></span>
- <span data-ttu-id="21a8c-3064">Uma palavra-chave de Keyword_Turkish_National_Id for encontrada.</span><span class="sxs-lookup"><span data-stu-id="21a8c-3064">A keyword from Keyword_Turkish_National_Id is found.</span></span>

<span data-ttu-id="21a8c-3065">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="21a8c-3065">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="21a8c-3066">A função Func_Turkish_National_Id localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="21a8c-3066">The function Func_Turkish_National_Id finds content that matches the pattern.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="21a8c-3067">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="21a8c-3067">Keywords</span></span>

#### <a name="keywordturkishnationalid"></a><span data-ttu-id="21a8c-3068">Keyword_Turkish_National_Id</span><span class="sxs-lookup"><span data-stu-id="21a8c-3068">Keyword_Turkish_National_Id</span></span>

- <span data-ttu-id="21a8c-3069">Kimlik TC não</span><span class="sxs-lookup"><span data-stu-id="21a8c-3069">TC Kimlik No</span></span>
- <span data-ttu-id="21a8c-3070">TC Kimlik numarası</span><span class="sxs-lookup"><span data-stu-id="21a8c-3070">TC Kimlik numarası</span></span>
- <span data-ttu-id="21a8c-3071">Vatandaşlık numarası</span><span class="sxs-lookup"><span data-stu-id="21a8c-3071">Vatandaşlık numarası</span></span>
- <span data-ttu-id="21a8c-3072">Vatandaşlık não</span><span class="sxs-lookup"><span data-stu-id="21a8c-3072">Vatandaşlık no</span></span>

## <a name="uk-drivers-license-number"></a><span data-ttu-id="21a8c-p141">Número de carteira de motorista do Reino Unido</span><span class="sxs-lookup"><span data-stu-id="21a8c-p141">U.K. Driver's License Number</span></span>

### <a name="format"></a><span data-ttu-id="21a8c-3075">Format</span><span class="sxs-lookup"><span data-stu-id="21a8c-3075">Format</span></span>

<span data-ttu-id="21a8c-3076">Combinação de 18 letras e dígitos no formato especificado</span><span class="sxs-lookup"><span data-stu-id="21a8c-3076">Combination of 18 letters and digits in the specified format</span></span>

### <a name="pattern"></a><span data-ttu-id="21a8c-3077">Padrão</span><span class="sxs-lookup"><span data-stu-id="21a8c-3077">Pattern</span></span>

<span data-ttu-id="21a8c-3078">18 letras e dígitos:</span><span class="sxs-lookup"><span data-stu-id="21a8c-3078">18 letters and digits:</span></span>
- <span data-ttu-id="21a8c-3079">Cinco letras (não diferenciam maiúsculas de minúsculas) ou o dígito "9" em vez de uma letra</span><span class="sxs-lookup"><span data-stu-id="21a8c-3079">Five letters (not case sensitive) or the digit "9" in place of a letter</span></span> 
- <span data-ttu-id="21a8c-3080">Um dígito</span><span class="sxs-lookup"><span data-stu-id="21a8c-3080">One digit</span></span> 
- <span data-ttu-id="21a8c-3081">Cinco dígitos no formato de data DDMMA para data de nascimento</span><span class="sxs-lookup"><span data-stu-id="21a8c-3081">Five digits in the date format DDMMY for date of birth</span></span> 
- <span data-ttu-id="21a8c-3082">Duas letras (não diferenciam maiúsculas de minúsculas) ou o dígito "9" em vez de uma letra</span><span class="sxs-lookup"><span data-stu-id="21a8c-3082">Two letters (not case sensitive) or the digit "9" in place of a letter</span></span> 
- <span data-ttu-id="21a8c-3083">Cinco dígitos</span><span class="sxs-lookup"><span data-stu-id="21a8c-3083">Five digits</span></span>

### <a name="checksum"></a><span data-ttu-id="21a8c-3084">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="21a8c-3084">Checksum</span></span>

<span data-ttu-id="21a8c-3085">Sim</span><span class="sxs-lookup"><span data-stu-id="21a8c-3085">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="21a8c-3086">Definição</span><span class="sxs-lookup"><span data-stu-id="21a8c-3086">Definition</span></span>

<span data-ttu-id="21a8c-3087">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="21a8c-3087">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="21a8c-3088">A função Func_uk_drivers_license localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="21a8c-3088">The function Func_uk_drivers_license finds content that matches the pattern.</span></span>
- <span data-ttu-id="21a8c-3089">Uma palavra-chave de Keyword_uk_drivers_license for encontrada.</span><span class="sxs-lookup"><span data-stu-id="21a8c-3089">A keyword from Keyword_uk_drivers_license is found.</span></span>
- <span data-ttu-id="21a8c-3090">A soma de verificação passa.</span><span class="sxs-lookup"><span data-stu-id="21a8c-3090">The checksum passes.</span></span>

```
<!-- U.K. Driver's License Number -->
<Entity id="f93de4be-d94c-40df-a8be-461738047551" patternsProximity="300" recommendedConfidence="75">
    <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_uk_drivers_license" />
        <Match idRef="Keyword_uk_drivers_license" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="21a8c-3091">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="21a8c-3091">Keywords</span></span>

#### <a name="keywordukdriverslicense"></a><span data-ttu-id="21a8c-3092">Keyword_uk_drivers_license</span><span class="sxs-lookup"><span data-stu-id="21a8c-3092">Keyword_uk_drivers_license</span></span>

- <span data-ttu-id="21a8c-3093">DVLA</span><span class="sxs-lookup"><span data-stu-id="21a8c-3093">DVLA</span></span> 
- <span data-ttu-id="21a8c-3094">light vans</span><span class="sxs-lookup"><span data-stu-id="21a8c-3094">light vans</span></span> 
- <span data-ttu-id="21a8c-3095">quadbikes</span><span class="sxs-lookup"><span data-stu-id="21a8c-3095">quadbikes</span></span> 
- <span data-ttu-id="21a8c-3096">motor cars</span><span class="sxs-lookup"><span data-stu-id="21a8c-3096">motor cars</span></span> 
- <span data-ttu-id="21a8c-3097">125cc</span><span class="sxs-lookup"><span data-stu-id="21a8c-3097">125cc</span></span> 
- <span data-ttu-id="21a8c-3098">sidecar</span><span class="sxs-lookup"><span data-stu-id="21a8c-3098">sidecar</span></span> 
- <span data-ttu-id="21a8c-3099">tricycles</span><span class="sxs-lookup"><span data-stu-id="21a8c-3099">tricycles</span></span> 
- <span data-ttu-id="21a8c-3100">Motorcycles</span><span class="sxs-lookup"><span data-stu-id="21a8c-3100">motorcycles</span></span> 
- <span data-ttu-id="21a8c-3101">photocard licence</span><span class="sxs-lookup"><span data-stu-id="21a8c-3101">photocard licence</span></span> 
- <span data-ttu-id="21a8c-3102">learner drivers</span><span class="sxs-lookup"><span data-stu-id="21a8c-3102">learner drivers</span></span> 
- <span data-ttu-id="21a8c-3103">licence holder</span><span class="sxs-lookup"><span data-stu-id="21a8c-3103">licence holder</span></span> 
- <span data-ttu-id="21a8c-3104">licence holders</span><span class="sxs-lookup"><span data-stu-id="21a8c-3104">licence holders</span></span> 
- <span data-ttu-id="21a8c-3105">driving licences</span><span class="sxs-lookup"><span data-stu-id="21a8c-3105">driving licences</span></span> 
- <span data-ttu-id="21a8c-3106">driving licence</span><span class="sxs-lookup"><span data-stu-id="21a8c-3106">driving licence</span></span> 
- <span data-ttu-id="21a8c-3107">dual control car</span><span class="sxs-lookup"><span data-stu-id="21a8c-3107">dual control car</span></span> 
   
## <a name="uk-electoral-roll-number"></a><span data-ttu-id="21a8c-p142">Número de Título de Eleitor do Reino Unido</span><span class="sxs-lookup"><span data-stu-id="21a8c-p142">U.K. Electoral Roll Number</span></span>

### <a name="format"></a><span data-ttu-id="21a8c-3110">Format</span><span class="sxs-lookup"><span data-stu-id="21a8c-3110">Format</span></span>

<span data-ttu-id="21a8c-3111">Duas letras seguidas por 1 a 4 dígitos</span><span class="sxs-lookup"><span data-stu-id="21a8c-3111">Two letters followed by 1-4 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="21a8c-3112">Padrão</span><span class="sxs-lookup"><span data-stu-id="21a8c-3112">Pattern</span></span>

<span data-ttu-id="21a8c-3113">Duas letras (não diferencia maiúsculas de minúsculas) seguidas de 1 a 4 anos</span><span class="sxs-lookup"><span data-stu-id="21a8c-3113">Two letters (not case sensitive) followed by 1-4 numbers</span></span>

### <a name="checksum"></a><span data-ttu-id="21a8c-3114">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="21a8c-3114">Checksum</span></span>

<span data-ttu-id="21a8c-3115">Não</span><span class="sxs-lookup"><span data-stu-id="21a8c-3115">No</span></span>

### <a name="definition"></a><span data-ttu-id="21a8c-3116">Definição</span><span class="sxs-lookup"><span data-stu-id="21a8c-3116">Definition</span></span>

<span data-ttu-id="21a8c-3117">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="21a8c-3117">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="21a8c-3118">A expressão regular Regex_uk_electoral localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="21a8c-3118">The regular expression Regex_uk_electoral finds content that matches the pattern.</span></span>
- <span data-ttu-id="21a8c-3119">Uma palavra-chave de Keyword_uk_electoral for encontrada.</span><span class="sxs-lookup"><span data-stu-id="21a8c-3119">A keyword from Keyword_uk_electoral is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="21a8c-3120">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="21a8c-3120">Keywords</span></span>

#### <a name="keywordukelectoral"></a><span data-ttu-id="21a8c-3121">Keyword_uk_electoral</span><span class="sxs-lookup"><span data-stu-id="21a8c-3121">Keyword_uk_electoral</span></span>

- <span data-ttu-id="21a8c-3122">council nomination</span><span class="sxs-lookup"><span data-stu-id="21a8c-3122">council nomination</span></span> 
- <span data-ttu-id="21a8c-3123">nomination form</span><span class="sxs-lookup"><span data-stu-id="21a8c-3123">nomination form</span></span> 
- <span data-ttu-id="21a8c-3124">electoral register</span><span class="sxs-lookup"><span data-stu-id="21a8c-3124">electoral register</span></span> 
- <span data-ttu-id="21a8c-3125">electoral roll</span><span class="sxs-lookup"><span data-stu-id="21a8c-3125">electoral roll</span></span>

   
## <a name="uk-national-health-service-number"></a><span data-ttu-id="21a8c-p143">Número do serviço de saúde nacional do Reino Unido</span><span class="sxs-lookup"><span data-stu-id="21a8c-p143">U.K. National Health Service Number</span></span>

### <a name="format"></a><span data-ttu-id="21a8c-3128">Format</span><span class="sxs-lookup"><span data-stu-id="21a8c-3128">Format</span></span>

<span data-ttu-id="21a8c-3129">10 a 17 dígitos separados por espaços</span><span class="sxs-lookup"><span data-stu-id="21a8c-3129">10-17 digits separated by spaces</span></span>

### <a name="pattern"></a><span data-ttu-id="21a8c-3130">Padrão</span><span class="sxs-lookup"><span data-stu-id="21a8c-3130">Pattern</span></span>

<span data-ttu-id="21a8c-3131">10 a 17 dígitos:</span><span class="sxs-lookup"><span data-stu-id="21a8c-3131">10-17 digits:</span></span>
- <span data-ttu-id="21a8c-3132">3 ou 10 dígitos</span><span class="sxs-lookup"><span data-stu-id="21a8c-3132">Either 3 or 10 digits</span></span> 
- <span data-ttu-id="21a8c-3133">Um espaço</span><span class="sxs-lookup"><span data-stu-id="21a8c-3133">A space</span></span> 
- <span data-ttu-id="21a8c-3134">Três dígitos</span><span class="sxs-lookup"><span data-stu-id="21a8c-3134">Three digits</span></span> 
- <span data-ttu-id="21a8c-3135">Um espaço</span><span class="sxs-lookup"><span data-stu-id="21a8c-3135">A space</span></span> 
- <span data-ttu-id="21a8c-3136">Quatro dígitos</span><span class="sxs-lookup"><span data-stu-id="21a8c-3136">Four digits</span></span>

### <a name="checksum"></a><span data-ttu-id="21a8c-3137">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="21a8c-3137">Checksum</span></span>

<span data-ttu-id="21a8c-3138">Sim</span><span class="sxs-lookup"><span data-stu-id="21a8c-3138">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="21a8c-3139">Definição</span><span class="sxs-lookup"><span data-stu-id="21a8c-3139">Definition</span></span>

<span data-ttu-id="21a8c-3140">Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="21a8c-3140">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="21a8c-3141">A função Func_uk_nhs_number localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="21a8c-3141">The function Func_uk_nhs_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="21a8c-3142">Uma das seguintes opções for verdadeira:</span><span class="sxs-lookup"><span data-stu-id="21a8c-3142">One of the following is true:</span></span>
    - <span data-ttu-id="21a8c-3143">Uma palavra-chave de Keyword_uk_nhs_number for encontrada.</span><span class="sxs-lookup"><span data-stu-id="21a8c-3143">A keyword from Keyword_uk_nhs_number is found.</span></span>
    - <span data-ttu-id="21a8c-3144">Uma palavra-chave de Keyword_uk_nhs_number1 for encontrada.</span><span class="sxs-lookup"><span data-stu-id="21a8c-3144">A keyword from Keyword_uk_nhs_number1 is found.</span></span>
    - <span data-ttu-id="21a8c-3145">Uma palavra-chave de Keyword_uk_nhs_number_dob for encontrada.</span><span class="sxs-lookup"><span data-stu-id="21a8c-3145">A keyword from Keyword_uk_nhs_number_dob is found.</span></span>
- <span data-ttu-id="21a8c-3146">A soma de verificação passa.</span><span class="sxs-lookup"><span data-stu-id="21a8c-3146">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="21a8c-3147">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="21a8c-3147">Keywords</span></span>
   
#### <a name="keyworduknhsnumber"></a><span data-ttu-id="21a8c-3148">Keyword_uk_nhs_number</span><span class="sxs-lookup"><span data-stu-id="21a8c-3148">Keyword_uk_nhs_number</span></span>

- <span data-ttu-id="21a8c-3149">national health service</span><span class="sxs-lookup"><span data-stu-id="21a8c-3149">national health service</span></span> 
- <span data-ttu-id="21a8c-3150">NHS</span><span class="sxs-lookup"><span data-stu-id="21a8c-3150">nhs</span></span> 
- <span data-ttu-id="21a8c-3151">health services authority</span><span class="sxs-lookup"><span data-stu-id="21a8c-3151">health services authority</span></span> 
- <span data-ttu-id="21a8c-3152">health authority</span><span class="sxs-lookup"><span data-stu-id="21a8c-3152">health authority</span></span>

#### <a name="keyworduknhsnumber1"></a><span data-ttu-id="21a8c-3153">Keyword_uk_nhs_number1</span><span class="sxs-lookup"><span data-stu-id="21a8c-3153">Keyword_uk_nhs_number1</span></span>

- <span data-ttu-id="21a8c-3154">patient id</span><span class="sxs-lookup"><span data-stu-id="21a8c-3154">patient id</span></span> 
- <span data-ttu-id="21a8c-3155">patient identification</span><span class="sxs-lookup"><span data-stu-id="21a8c-3155">patient identification</span></span> 
- <span data-ttu-id="21a8c-3156">patient no</span><span class="sxs-lookup"><span data-stu-id="21a8c-3156">patient no</span></span> 
- <span data-ttu-id="21a8c-3157">patient number</span><span class="sxs-lookup"><span data-stu-id="21a8c-3157">patient number</span></span>

#### <a name="keyworduknhsnumberdob"></a><span data-ttu-id="21a8c-3158">Keyword_uk_nhs_number_dob</span><span class="sxs-lookup"><span data-stu-id="21a8c-3158">Keyword_uk_nhs_number_dob</span></span>

- <span data-ttu-id="21a8c-3159">GP</span><span class="sxs-lookup"><span data-stu-id="21a8c-3159">GP</span></span> 
- <span data-ttu-id="21a8c-3160">DOB</span><span class="sxs-lookup"><span data-stu-id="21a8c-3160">DOB</span></span> 
- <span data-ttu-id="21a8c-3161">D. O. B</span><span class="sxs-lookup"><span data-stu-id="21a8c-3161">D.O.B</span></span> 
- <span data-ttu-id="21a8c-3162">Date of Birth</span><span class="sxs-lookup"><span data-stu-id="21a8c-3162">Date of Birth</span></span> 
- <span data-ttu-id="21a8c-3163">Birth Date</span><span class="sxs-lookup"><span data-stu-id="21a8c-3163">Birth Date</span></span> 
   
## <a name="uk-national-insurance-number-nino"></a><span data-ttu-id="21a8c-p144">Número de seguro nacional do Reino Unido (NINO)</span><span class="sxs-lookup"><span data-stu-id="21a8c-p144">U.K. National Insurance Number (NINO)</span></span>

### <a name="format"></a><span data-ttu-id="21a8c-3166">Format</span><span class="sxs-lookup"><span data-stu-id="21a8c-3166">Format</span></span>

<span data-ttu-id="21a8c-3167">7 caracteres ou 9 caracteres separados por espaços ou traços</span><span class="sxs-lookup"><span data-stu-id="21a8c-3167">7 characters or 9 characters separated by spaces or dashes</span></span>

### <a name="pattern"></a><span data-ttu-id="21a8c-3168">Padrão</span><span class="sxs-lookup"><span data-stu-id="21a8c-3168">Pattern</span></span>

<span data-ttu-id="21a8c-3169">Dois padrões possíveis:</span><span class="sxs-lookup"><span data-stu-id="21a8c-3169">Two possible patterns:</span></span>

- <span data-ttu-id="21a8c-3170">Duas letras (NINOs válidas usam apenas determinados caracteres neste prefixo, que esse padrão valida; não diferencia maiúsculas de minúsculas)</span><span class="sxs-lookup"><span data-stu-id="21a8c-3170">Two letters (valid NINOs use only certain characters in this prefix, which this pattern validates; not case sensitive)</span></span>
- <span data-ttu-id="21a8c-3171">Seis dígitos</span><span class="sxs-lookup"><span data-stu-id="21a8c-3171">Six digits</span></span>
- <span data-ttu-id="21a8c-3172">"A", "B", "C" ou "(como o prefixo, apenas determinados caracteres são permitidos no sufixo; não diferencia maiúsculas de minúsculas)</span><span class="sxs-lookup"><span data-stu-id="21a8c-3172">Either 'A', 'B', 'C', or 'D' (like the prefix, only certain characters are allowed in the suffix; not case sensitive)</span></span>

<span data-ttu-id="21a8c-3173">OU</span><span class="sxs-lookup"><span data-stu-id="21a8c-3173">OR</span></span>

- <span data-ttu-id="21a8c-3174">Duas letras</span><span class="sxs-lookup"><span data-stu-id="21a8c-3174">Two letters</span></span>
- <span data-ttu-id="21a8c-3175">Um espaço ou um traço</span><span class="sxs-lookup"><span data-stu-id="21a8c-3175">A space or dash</span></span>
- <span data-ttu-id="21a8c-3176">Dois dígitos</span><span class="sxs-lookup"><span data-stu-id="21a8c-3176">Two digits</span></span>
- <span data-ttu-id="21a8c-3177">Um espaço ou um traço</span><span class="sxs-lookup"><span data-stu-id="21a8c-3177">A space or dash</span></span>
- <span data-ttu-id="21a8c-3178">Dois dígitos</span><span class="sxs-lookup"><span data-stu-id="21a8c-3178">Two digits</span></span>
- <span data-ttu-id="21a8c-3179">Um espaço ou um traço</span><span class="sxs-lookup"><span data-stu-id="21a8c-3179">A space or dash</span></span>
- <span data-ttu-id="21a8c-3180">Dois dígitos</span><span class="sxs-lookup"><span data-stu-id="21a8c-3180">Two digits</span></span>
- <span data-ttu-id="21a8c-3181">Um espaço ou um traço</span><span class="sxs-lookup"><span data-stu-id="21a8c-3181">A space or dash</span></span>
- <span data-ttu-id="21a8c-3182">' A ', ' B ', ' C' ou ' d'</span><span class="sxs-lookup"><span data-stu-id="21a8c-3182">Either 'A', 'B', 'C', or 'D'</span></span>

### <a name="checksum"></a><span data-ttu-id="21a8c-3183">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="21a8c-3183">Checksum</span></span>

<span data-ttu-id="21a8c-3184">Não</span><span class="sxs-lookup"><span data-stu-id="21a8c-3184">No</span></span>

### <a name="definition"></a><span data-ttu-id="21a8c-3185">Definição</span><span class="sxs-lookup"><span data-stu-id="21a8c-3185">Definition</span></span>

<span data-ttu-id="21a8c-3186">Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="21a8c-3186">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="21a8c-3187">A função Func_uk_nino localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="21a8c-3187">The function Func_uk_nino finds content that matches the pattern.</span></span>
- <span data-ttu-id="21a8c-3188">Uma palavra-chave de Keyword_uk_nino for encontrada.</span><span class="sxs-lookup"><span data-stu-id="21a8c-3188">A keyword from Keyword_uk_nino is found.</span></span>

<span data-ttu-id="21a8c-3189">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="21a8c-3189">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="21a8c-3190">A função Func_uk_nino localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="21a8c-3190">The function Func_uk_nino finds content that matches the pattern.</span></span>
- <span data-ttu-id="21a8c-3191">Nenhuma palavra-chave de Keyword_uk_nino for encontrada.</span><span class="sxs-lookup"><span data-stu-id="21a8c-3191">No keyword from Keyword_uk_nino is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="21a8c-3192">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="21a8c-3192">Keywords</span></span>

#### <a name="keyworduknino"></a><span data-ttu-id="21a8c-3193">Keyword_uk_nino</span><span class="sxs-lookup"><span data-stu-id="21a8c-3193">Keyword_uk_nino</span></span>

- <span data-ttu-id="21a8c-3194">national insurance number</span><span class="sxs-lookup"><span data-stu-id="21a8c-3194">national insurance number</span></span> 
- <span data-ttu-id="21a8c-3195">national insurance contributions</span><span class="sxs-lookup"><span data-stu-id="21a8c-3195">national insurance contributions</span></span> 
- <span data-ttu-id="21a8c-3196">protection act</span><span class="sxs-lookup"><span data-stu-id="21a8c-3196">protection act</span></span> 
- <span data-ttu-id="21a8c-3197">seguro</span><span class="sxs-lookup"><span data-stu-id="21a8c-3197">insurance</span></span> 
- <span data-ttu-id="21a8c-3198">social security number</span><span class="sxs-lookup"><span data-stu-id="21a8c-3198">social security number</span></span> 
- <span data-ttu-id="21a8c-3199">insurance application</span><span class="sxs-lookup"><span data-stu-id="21a8c-3199">insurance application</span></span> 
- <span data-ttu-id="21a8c-3200">medical application</span><span class="sxs-lookup"><span data-stu-id="21a8c-3200">medical application</span></span> 
- <span data-ttu-id="21a8c-3201">social insurance</span><span class="sxs-lookup"><span data-stu-id="21a8c-3201">social insurance</span></span> 
- <span data-ttu-id="21a8c-3202">medical attention</span><span class="sxs-lookup"><span data-stu-id="21a8c-3202">medical attention</span></span> 
- <span data-ttu-id="21a8c-3203">social security</span><span class="sxs-lookup"><span data-stu-id="21a8c-3203">social security</span></span> 
- <span data-ttu-id="21a8c-3204">great britain</span><span class="sxs-lookup"><span data-stu-id="21a8c-3204">great britain</span></span> 
- <span data-ttu-id="21a8c-3205">seguro</span><span class="sxs-lookup"><span data-stu-id="21a8c-3205">insurance</span></span>    
   
## <a name="us--uk-passport-number"></a><span data-ttu-id="21a8c-p145">Número de passaporte dos EUA/Reino Unido</span><span class="sxs-lookup"><span data-stu-id="21a8c-p145">U.S. / U.K. Passport Number</span></span>

### <a name="format"></a><span data-ttu-id="21a8c-3208">Format</span><span class="sxs-lookup"><span data-stu-id="21a8c-3208">Format</span></span>

<span data-ttu-id="21a8c-3209">Nove dígitos</span><span class="sxs-lookup"><span data-stu-id="21a8c-3209">Nine digits</span></span>

### <a name="pattern"></a><span data-ttu-id="21a8c-3210">Padrão</span><span class="sxs-lookup"><span data-stu-id="21a8c-3210">Pattern</span></span>

<span data-ttu-id="21a8c-3211">Nove dígitos consecutivos</span><span class="sxs-lookup"><span data-stu-id="21a8c-3211">Nine consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="21a8c-3212">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="21a8c-3212">Checksum</span></span>

<span data-ttu-id="21a8c-3213">Não</span><span class="sxs-lookup"><span data-stu-id="21a8c-3213">No</span></span>

### <a name="definition"></a><span data-ttu-id="21a8c-3214">Definição</span><span class="sxs-lookup"><span data-stu-id="21a8c-3214">Definition</span></span>

<span data-ttu-id="21a8c-3215">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="21a8c-3215">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="21a8c-3216">A função Func_usa_uk_passport localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="21a8c-3216">The function Func_usa_uk_passport finds content that matches the pattern.</span></span>
- <span data-ttu-id="21a8c-3217">Uma palavra-chave de Keyword_passport for encontrada.</span><span class="sxs-lookup"><span data-stu-id="21a8c-3217">A keyword from Keyword_passport is found.</span></span>

```
<Entity id="178ec42a-18b4-47cc-85c7-d62c92fd67f8" patternsProximity="300" recommendedConfidence="75">
    <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_usa_uk_passport" />
        <Match idRef="Keyword_passport" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="21a8c-3218">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="21a8c-3218">Keywords</span></span>

#### <a name="keywordpassport"></a><span data-ttu-id="21a8c-3219">Keyword_passport</span><span class="sxs-lookup"><span data-stu-id="21a8c-3219">Keyword_passport</span></span>

- <span data-ttu-id="21a8c-3220">Passport Number</span><span class="sxs-lookup"><span data-stu-id="21a8c-3220">Passport Number</span></span> 
- <span data-ttu-id="21a8c-3221">Passport No</span><span class="sxs-lookup"><span data-stu-id="21a8c-3221">Passport No</span></span> 
- <span data-ttu-id="21a8c-3222">Passport #</span><span class="sxs-lookup"><span data-stu-id="21a8c-3222">Passport #</span></span> 
- <span data-ttu-id="21a8c-3223">Passaport</span><span class="sxs-lookup"><span data-stu-id="21a8c-3223">Passport#</span></span> 
- <span data-ttu-id="21a8c-3224">Passportid</span><span class="sxs-lookup"><span data-stu-id="21a8c-3224">PassportID</span></span> 
- <span data-ttu-id="21a8c-3225">Passportno</span><span class="sxs-lookup"><span data-stu-id="21a8c-3225">Passportno</span></span> 
- <span data-ttu-id="21a8c-3226">passportnumber</span><span class="sxs-lookup"><span data-stu-id="21a8c-3226">passportnumber</span></span> 
- <span data-ttu-id="21a8c-3227">パスポート</span><span class="sxs-lookup"><span data-stu-id="21a8c-3227">パスポート</span></span> 
- <span data-ttu-id="21a8c-3228">パスポート番号</span><span class="sxs-lookup"><span data-stu-id="21a8c-3228">パスポート番号</span></span> 
- <span data-ttu-id="21a8c-3229">パスポートのNum</span><span class="sxs-lookup"><span data-stu-id="21a8c-3229">パスポートのNum</span></span> 
- <span data-ttu-id="21a8c-3230">パスポート #</span><span class="sxs-lookup"><span data-stu-id="21a8c-3230">パスポート＃</span></span> 
- <span data-ttu-id="21a8c-3231">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="21a8c-3231">Numéro de passeport</span></span> 
- <span data-ttu-id="21a8c-3232">Passeport n °</span><span class="sxs-lookup"><span data-stu-id="21a8c-3232">Passeport n °</span></span> 
- <span data-ttu-id="21a8c-3233">Passeport Non</span><span class="sxs-lookup"><span data-stu-id="21a8c-3233">Passeport Non</span></span> 
- <span data-ttu-id="21a8c-3234">Passeport #</span><span class="sxs-lookup"><span data-stu-id="21a8c-3234">Passeport #</span></span> 
- <span data-ttu-id="21a8c-3235">Passeport #</span><span class="sxs-lookup"><span data-stu-id="21a8c-3235">Passeport#</span></span> 
- <span data-ttu-id="21a8c-3236">PasseportNon</span><span class="sxs-lookup"><span data-stu-id="21a8c-3236">PasseportNon</span></span> 
- <span data-ttu-id="21a8c-3237">Passeportn °</span><span class="sxs-lookup"><span data-stu-id="21a8c-3237">Passeportn °</span></span> 
   
## <a name="us-bank-account-number"></a><span data-ttu-id="21a8c-3238">Número de conta bancária dos EUA</span><span class="sxs-lookup"><span data-stu-id="21a8c-3238">U.S. Bank Account Number</span></span>

### <a name="format"></a><span data-ttu-id="21a8c-3239">Format</span><span class="sxs-lookup"><span data-stu-id="21a8c-3239">Format</span></span>

<span data-ttu-id="21a8c-3240">8 a 17 dígitos</span><span class="sxs-lookup"><span data-stu-id="21a8c-3240">8-17 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="21a8c-3241">Padrão</span><span class="sxs-lookup"><span data-stu-id="21a8c-3241">Pattern</span></span>

<span data-ttu-id="21a8c-3242">8 a 17 dígitos consecutivos</span><span class="sxs-lookup"><span data-stu-id="21a8c-3242">8-17 consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="21a8c-3243">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="21a8c-3243">Checksum</span></span>

<span data-ttu-id="21a8c-3244">Não</span><span class="sxs-lookup"><span data-stu-id="21a8c-3244">No</span></span>

### <a name="definition"></a><span data-ttu-id="21a8c-3245">Definição</span><span class="sxs-lookup"><span data-stu-id="21a8c-3245">Definition</span></span>

<span data-ttu-id="21a8c-3246">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="21a8c-3246">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="21a8c-3247">A expressão regular Regex_usa_bank_account_number localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="21a8c-3247">The regular expression Regex_usa_bank_account_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="21a8c-3248">Uma palavra-chave de Keyword_usa_Bank_Account for encontrada.</span><span class="sxs-lookup"><span data-stu-id="21a8c-3248">A keyword from Keyword_usa_Bank_Account is found.</span></span>

```
<!-- U.S. Bank Account Number -->
<Entity id="a2ce32a8-f935-4bb6-8e96-2a5157672e2c" patternsProximity="300" recommendedConfidence="75">
    <Pattern confidenceLevel="75">
        <IdMatch idRef="Regex_usa_bank_account_number" />
        <Match idRef="Keyword_usa_Bank_Account" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="21a8c-3249">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="21a8c-3249">Keywords</span></span>

#### <a name="keywordusabankaccount"></a><span data-ttu-id="21a8c-3250">Keyword_usa_Bank_Account</span><span class="sxs-lookup"><span data-stu-id="21a8c-3250">Keyword_usa_Bank_Account</span></span>

- <span data-ttu-id="21a8c-3251">Checking Account Number</span><span class="sxs-lookup"><span data-stu-id="21a8c-3251">Checking Account Number</span></span> 
- <span data-ttu-id="21a8c-3252">Checking Account</span><span class="sxs-lookup"><span data-stu-id="21a8c-3252">Checking Account</span></span> 
- <span data-ttu-id="21a8c-3253">Checking Account #</span><span class="sxs-lookup"><span data-stu-id="21a8c-3253">Checking Account #</span></span> 
- <span data-ttu-id="21a8c-3254">Checking Acct Number</span><span class="sxs-lookup"><span data-stu-id="21a8c-3254">Checking Acct Number</span></span> 
- <span data-ttu-id="21a8c-3255">Checking Acct #</span><span class="sxs-lookup"><span data-stu-id="21a8c-3255">Checking Acct #</span></span> 
- <span data-ttu-id="21a8c-3256">Checking Acct No.</span><span class="sxs-lookup"><span data-stu-id="21a8c-3256">Checking Acct No.</span></span> 
- <span data-ttu-id="21a8c-3257">Checking Account No.</span><span class="sxs-lookup"><span data-stu-id="21a8c-3257">Checking Account No.</span></span> 
- <span data-ttu-id="21a8c-3258">Bank Account Number</span><span class="sxs-lookup"><span data-stu-id="21a8c-3258">Bank Account Number</span></span> 
- <span data-ttu-id="21a8c-3259">Bank Account #</span><span class="sxs-lookup"><span data-stu-id="21a8c-3259">Bank Account #</span></span> 
- <span data-ttu-id="21a8c-3260">Bank Acct Number</span><span class="sxs-lookup"><span data-stu-id="21a8c-3260">Bank Acct Number</span></span> 
- <span data-ttu-id="21a8c-3261">Bank Acct #</span><span class="sxs-lookup"><span data-stu-id="21a8c-3261">Bank Acct #</span></span> 
- <span data-ttu-id="21a8c-3262">Bank Acct No.</span><span class="sxs-lookup"><span data-stu-id="21a8c-3262">Bank Acct No.</span></span> 
- <span data-ttu-id="21a8c-3263">Bank Account No.</span><span class="sxs-lookup"><span data-stu-id="21a8c-3263">Bank Account No.</span></span> 
- <span data-ttu-id="21a8c-3264">Savings Account Number</span><span class="sxs-lookup"><span data-stu-id="21a8c-3264">Savings Account Number</span></span> 
- <span data-ttu-id="21a8c-3265">Savings Account.</span><span class="sxs-lookup"><span data-stu-id="21a8c-3265">Savings Account.</span></span> 
- <span data-ttu-id="21a8c-3266">Savings Account #</span><span class="sxs-lookup"><span data-stu-id="21a8c-3266">Savings Account #</span></span> 
- <span data-ttu-id="21a8c-3267">Savings Acct Number</span><span class="sxs-lookup"><span data-stu-id="21a8c-3267">Savings Acct Number</span></span> 
- <span data-ttu-id="21a8c-3268">Savings Acct #</span><span class="sxs-lookup"><span data-stu-id="21a8c-3268">Savings Acct #</span></span> 
- <span data-ttu-id="21a8c-3269">Savings Acct No.</span><span class="sxs-lookup"><span data-stu-id="21a8c-3269">Savings Acct No.</span></span> 
- <span data-ttu-id="21a8c-3270">Savings Account No.</span><span class="sxs-lookup"><span data-stu-id="21a8c-3270">Savings Account No.</span></span> 
- <span data-ttu-id="21a8c-3271">Debit Account Number</span><span class="sxs-lookup"><span data-stu-id="21a8c-3271">Debit Account Number</span></span> 
- <span data-ttu-id="21a8c-3272">Debit Account</span><span class="sxs-lookup"><span data-stu-id="21a8c-3272">Debit Account</span></span> 
- <span data-ttu-id="21a8c-3273">Debit Account #</span><span class="sxs-lookup"><span data-stu-id="21a8c-3273">Debit Account #</span></span> 
- <span data-ttu-id="21a8c-3274">Debit Acct Number</span><span class="sxs-lookup"><span data-stu-id="21a8c-3274">Debit Acct Number</span></span> 
- <span data-ttu-id="21a8c-3275">Debit Acct #</span><span class="sxs-lookup"><span data-stu-id="21a8c-3275">Debit Acct #</span></span> 
- <span data-ttu-id="21a8c-3276">Debit Acct No.</span><span class="sxs-lookup"><span data-stu-id="21a8c-3276">Debit Acct No.</span></span> 
- <span data-ttu-id="21a8c-3277">Debit Account No.</span><span class="sxs-lookup"><span data-stu-id="21a8c-3277">Debit Account No.</span></span> 
   
## <a name="us-drivers-license-number"></a><span data-ttu-id="21a8c-3278">Número de carteira de motorista dos EUA</span><span class="sxs-lookup"><span data-stu-id="21a8c-3278">U.S. Driver's License Number</span></span>

### <a name="format"></a><span data-ttu-id="21a8c-3279">Format</span><span class="sxs-lookup"><span data-stu-id="21a8c-3279">Format</span></span>

<span data-ttu-id="21a8c-3280">Depende do estado</span><span class="sxs-lookup"><span data-stu-id="21a8c-3280">Depends on the state</span></span>

### <a name="pattern"></a><span data-ttu-id="21a8c-3281">Padrão</span><span class="sxs-lookup"><span data-stu-id="21a8c-3281">Pattern</span></span>

<span data-ttu-id="21a8c-3282">Depende do estado – por exemplo, Nova York:</span><span class="sxs-lookup"><span data-stu-id="21a8c-3282">Depends on the state -- for example, New York:</span></span>
- <span data-ttu-id="21a8c-3283">Nove dígitos formatados como DDD DDD DDD corresponderão.</span><span class="sxs-lookup"><span data-stu-id="21a8c-3283">Nine digits formatted like ddd ddd ddd will match.</span></span>
- <span data-ttu-id="21a8c-3284">Nove dígitos como ddddddddd não serão correspondentes.</span><span class="sxs-lookup"><span data-stu-id="21a8c-3284">Nine digits like ddddddddd will not match.</span></span>

### <a name="checksum"></a><span data-ttu-id="21a8c-3285">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="21a8c-3285">Checksum</span></span>

<span data-ttu-id="21a8c-3286">Não</span><span class="sxs-lookup"><span data-stu-id="21a8c-3286">No</span></span>

### <a name="definition"></a><span data-ttu-id="21a8c-3287">Definição</span><span class="sxs-lookup"><span data-stu-id="21a8c-3287">Definition</span></span>

<span data-ttu-id="21a8c-3288">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="21a8c-3288">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="21a8c-3289">A função Func_new_york_drivers_license_number localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="21a8c-3289">The function Func_new_york_drivers_license_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="21a8c-3290">Uma palavra-chave de Keyword_[state_name]_drivers_license_name for encontrada.</span><span class="sxs-lookup"><span data-stu-id="21a8c-3290">A keyword from Keyword_[state_name]_drivers_license_name is found.</span></span>
- <span data-ttu-id="21a8c-3291">Uma palavra-chave de Keyword_us_drivers_license for encontrada.</span><span class="sxs-lookup"><span data-stu-id="21a8c-3291">A keyword from Keyword_us_drivers_license is found.</span></span>

<span data-ttu-id="21a8c-3292">Uma política de DLP tem 65% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="21a8c-3292">A DLP policy is 65% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="21a8c-3293">A função Func_new_york_drivers_license_number localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="21a8c-3293">The function Func_new_york_drivers_license_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="21a8c-3294">Uma palavra-chave de Keyword_[state_name]_drivers_license_name for encontrada.</span><span class="sxs-lookup"><span data-stu-id="21a8c-3294">A keyword from Keyword_[state_name]_drivers_license_name is found.</span></span>
- <span data-ttu-id="21a8c-3295">Uma palavra-chave de Keyword_us_drivers_license_abbreviations for encontrada.</span><span class="sxs-lookup"><span data-stu-id="21a8c-3295">A keyword from Keyword_us_drivers_license_abbreviations is found.</span></span>
- <span data-ttu-id="21a8c-3296">Nenhuma palavra-chave de Keyword_us_drivers_license for encontrada.</span><span class="sxs-lookup"><span data-stu-id="21a8c-3296">No keyword from Keyword_us_drivers_license is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="21a8c-3297">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="21a8c-3297">Keywords</span></span>

#### <a name="keywordusdriverslicenseabbreviations"></a><span data-ttu-id="21a8c-3298">Keyword_us_drivers_license_abbreviations</span><span class="sxs-lookup"><span data-stu-id="21a8c-3298">Keyword_us_drivers_license_abbreviations</span></span>

- <span data-ttu-id="21a8c-3299">DISTRIBUIÇÃO</span><span class="sxs-lookup"><span data-stu-id="21a8c-3299">DL</span></span> 
- <span data-ttu-id="21a8c-3300">DL</span><span class="sxs-lookup"><span data-stu-id="21a8c-3300">DLS</span></span> 
- <span data-ttu-id="21a8c-3301">CDL</span><span class="sxs-lookup"><span data-stu-id="21a8c-3301">CDL</span></span> 
- <span data-ttu-id="21a8c-3302">CDLS</span><span class="sxs-lookup"><span data-stu-id="21a8c-3302">CDLS</span></span> 
- <span data-ttu-id="21a8c-3303">ID</span><span class="sxs-lookup"><span data-stu-id="21a8c-3303">ID</span></span> 
- <span data-ttu-id="21a8c-3304">Código</span><span class="sxs-lookup"><span data-stu-id="21a8c-3304">IDs</span></span> 
- <span data-ttu-id="21a8c-3305">DISTRIBUIÇÃO</span><span class="sxs-lookup"><span data-stu-id="21a8c-3305">DL#</span></span> 
- <span data-ttu-id="21a8c-3306">DL</span><span class="sxs-lookup"><span data-stu-id="21a8c-3306">DLS#</span></span> 
- <span data-ttu-id="21a8c-3307">CDL</span><span class="sxs-lookup"><span data-stu-id="21a8c-3307">CDL#</span></span> 
- <span data-ttu-id="21a8c-3308">CDLS #</span><span class="sxs-lookup"><span data-stu-id="21a8c-3308">CDLS#</span></span> 
- <span data-ttu-id="21a8c-3309">ID</span><span class="sxs-lookup"><span data-stu-id="21a8c-3309">ID#</span></span>
- <span data-ttu-id="21a8c-3310">Código</span><span class="sxs-lookup"><span data-stu-id="21a8c-3310">IDs#</span></span> 
- <span data-ttu-id="21a8c-3311">ID number</span><span class="sxs-lookup"><span data-stu-id="21a8c-3311">ID number</span></span> 
- <span data-ttu-id="21a8c-3312">ID numbers</span><span class="sxs-lookup"><span data-stu-id="21a8c-3312">ID numbers</span></span> 
- <span data-ttu-id="21a8c-3313">DRIVER'LIC</span><span class="sxs-lookup"><span data-stu-id="21a8c-3313">LIC</span></span> 
- <span data-ttu-id="21a8c-3314">DRIVER'LIC</span><span class="sxs-lookup"><span data-stu-id="21a8c-3314">LIC#</span></span> 

#### <a name="keywordusdriverslicense"></a><span data-ttu-id="21a8c-3315">Keyword_us_drivers_license</span><span class="sxs-lookup"><span data-stu-id="21a8c-3315">Keyword_us_drivers_license</span></span>

- <span data-ttu-id="21a8c-3316">DriverLic</span><span class="sxs-lookup"><span data-stu-id="21a8c-3316">DriverLic</span></span> 
- <span data-ttu-id="21a8c-3317">DriverLics</span><span class="sxs-lookup"><span data-stu-id="21a8c-3317">DriverLics</span></span> 
- <span data-ttu-id="21a8c-3318">DriverLicense</span><span class="sxs-lookup"><span data-stu-id="21a8c-3318">DriverLicense</span></span> 
- <span data-ttu-id="21a8c-3319">DriverLicenses</span><span class="sxs-lookup"><span data-stu-id="21a8c-3319">DriverLicenses</span></span> 
- <span data-ttu-id="21a8c-3320">Driver Lic</span><span class="sxs-lookup"><span data-stu-id="21a8c-3320">Driver Lic</span></span> 
- <span data-ttu-id="21a8c-3321">Driver Lics</span><span class="sxs-lookup"><span data-stu-id="21a8c-3321">Driver Lics</span></span> 
- <span data-ttu-id="21a8c-3322">Driver License</span><span class="sxs-lookup"><span data-stu-id="21a8c-3322">Driver License</span></span> 
- <span data-ttu-id="21a8c-3323">Driver Licenses</span><span class="sxs-lookup"><span data-stu-id="21a8c-3323">Driver Licenses</span></span> 
- <span data-ttu-id="21a8c-3324">DriversLic</span><span class="sxs-lookup"><span data-stu-id="21a8c-3324">DriversLic</span></span> 
- <span data-ttu-id="21a8c-3325">DriversLics</span><span class="sxs-lookup"><span data-stu-id="21a8c-3325">DriversLics</span></span> 
- <span data-ttu-id="21a8c-3326">DriversLicense</span><span class="sxs-lookup"><span data-stu-id="21a8c-3326">DriversLicense</span></span> 
- <span data-ttu-id="21a8c-3327">DriversLicenses</span><span class="sxs-lookup"><span data-stu-id="21a8c-3327">DriversLicenses</span></span> 
- <span data-ttu-id="21a8c-3328">Drivers Lic</span><span class="sxs-lookup"><span data-stu-id="21a8c-3328">Drivers Lic</span></span> 
- <span data-ttu-id="21a8c-3329">Drivers Lics</span><span class="sxs-lookup"><span data-stu-id="21a8c-3329">Drivers Lics</span></span> 
- <span data-ttu-id="21a8c-3330">Drivers License</span><span class="sxs-lookup"><span data-stu-id="21a8c-3330">Drivers License</span></span> 
- <span data-ttu-id="21a8c-3331">Drivers Licenses</span><span class="sxs-lookup"><span data-stu-id="21a8c-3331">Drivers Licenses</span></span> 
- <span data-ttu-id="21a8c-3332">Driver'Lic</span><span class="sxs-lookup"><span data-stu-id="21a8c-3332">Driver'Lic</span></span> 
- <span data-ttu-id="21a8c-3333">Driver'Lics</span><span class="sxs-lookup"><span data-stu-id="21a8c-3333">Driver'Lics</span></span> 
- <span data-ttu-id="21a8c-3334">Driver'License</span><span class="sxs-lookup"><span data-stu-id="21a8c-3334">Driver'License</span></span> 
- <span data-ttu-id="21a8c-3335">Driver'Licenses</span><span class="sxs-lookup"><span data-stu-id="21a8c-3335">Driver'Licenses</span></span> 
- <span data-ttu-id="21a8c-3336">Driver' Lic</span><span class="sxs-lookup"><span data-stu-id="21a8c-3336">Driver' Lic</span></span> 
- <span data-ttu-id="21a8c-3337">Driver' Lics</span><span class="sxs-lookup"><span data-stu-id="21a8c-3337">Driver' Lics</span></span> 
- <span data-ttu-id="21a8c-3338">Driver' License</span><span class="sxs-lookup"><span data-stu-id="21a8c-3338">Driver' License</span></span> 
- <span data-ttu-id="21a8c-3339">Driver' Licenses</span><span class="sxs-lookup"><span data-stu-id="21a8c-3339">Driver' Licenses</span></span>
- <span data-ttu-id="21a8c-3340">Driver'sLic</span><span class="sxs-lookup"><span data-stu-id="21a8c-3340">Driver'sLic</span></span> 
- <span data-ttu-id="21a8c-3341">Driver'sLics</span><span class="sxs-lookup"><span data-stu-id="21a8c-3341">Driver'sLics</span></span> 
- <span data-ttu-id="21a8c-3342">Driver'sLicense</span><span class="sxs-lookup"><span data-stu-id="21a8c-3342">Driver'sLicense</span></span> 
- <span data-ttu-id="21a8c-3343">Driver'sLicenses</span><span class="sxs-lookup"><span data-stu-id="21a8c-3343">Driver'sLicenses</span></span> 
- <span data-ttu-id="21a8c-3344">Driver's Lic</span><span class="sxs-lookup"><span data-stu-id="21a8c-3344">Driver's Lic</span></span> 
- <span data-ttu-id="21a8c-3345">Driver's Lics</span><span class="sxs-lookup"><span data-stu-id="21a8c-3345">Driver's Lics</span></span> 
- <span data-ttu-id="21a8c-3346">Driver's License</span><span class="sxs-lookup"><span data-stu-id="21a8c-3346">Driver's License</span></span> 
- <span data-ttu-id="21a8c-3347">Driver's Licenses</span><span class="sxs-lookup"><span data-stu-id="21a8c-3347">Driver's Licenses</span></span> 
- <span data-ttu-id="21a8c-3348">identification number</span><span class="sxs-lookup"><span data-stu-id="21a8c-3348">identification number</span></span> 
- <span data-ttu-id="21a8c-3349">identification numbers</span><span class="sxs-lookup"><span data-stu-id="21a8c-3349">identification numbers</span></span> 
- <span data-ttu-id="21a8c-3350">identification #</span><span class="sxs-lookup"><span data-stu-id="21a8c-3350">identification #</span></span> 
- <span data-ttu-id="21a8c-3351">id card</span><span class="sxs-lookup"><span data-stu-id="21a8c-3351">id card</span></span> 
- <span data-ttu-id="21a8c-3352">id cards</span><span class="sxs-lookup"><span data-stu-id="21a8c-3352">id cards</span></span> 
- <span data-ttu-id="21a8c-3353">identification card</span><span class="sxs-lookup"><span data-stu-id="21a8c-3353">identification card</span></span> 
- <span data-ttu-id="21a8c-3354">identification cards</span><span class="sxs-lookup"><span data-stu-id="21a8c-3354">identification cards</span></span> 
- <span data-ttu-id="21a8c-3355">DriverLic #</span><span class="sxs-lookup"><span data-stu-id="21a8c-3355">DriverLic#</span></span> 
- <span data-ttu-id="21a8c-3356">DriverLics #</span><span class="sxs-lookup"><span data-stu-id="21a8c-3356">DriverLics#</span></span> 
- <span data-ttu-id="21a8c-3357">DriverLicense #</span><span class="sxs-lookup"><span data-stu-id="21a8c-3357">DriverLicense#</span></span> 
- <span data-ttu-id="21a8c-3358">DriverLicenses #</span><span class="sxs-lookup"><span data-stu-id="21a8c-3358">DriverLicenses#</span></span> 
- <span data-ttu-id="21a8c-3359">Driver Lic#</span><span class="sxs-lookup"><span data-stu-id="21a8c-3359">Driver Lic#</span></span> 
- <span data-ttu-id="21a8c-3360">Driver Lics#</span><span class="sxs-lookup"><span data-stu-id="21a8c-3360">Driver Lics#</span></span> 
- <span data-ttu-id="21a8c-3361">Driver License#</span><span class="sxs-lookup"><span data-stu-id="21a8c-3361">Driver License#</span></span> 
- <span data-ttu-id="21a8c-3362">Driver Licenses#</span><span class="sxs-lookup"><span data-stu-id="21a8c-3362">Driver Licenses#</span></span> 
- <span data-ttu-id="21a8c-3363">DriversLic #</span><span class="sxs-lookup"><span data-stu-id="21a8c-3363">DriversLic#</span></span> 
- <span data-ttu-id="21a8c-3364">DriversLics #</span><span class="sxs-lookup"><span data-stu-id="21a8c-3364">DriversLics#</span></span> 
- <span data-ttu-id="21a8c-3365">DriversLicense #</span><span class="sxs-lookup"><span data-stu-id="21a8c-3365">DriversLicense#</span></span> 
- <span data-ttu-id="21a8c-3366">DriversLicenses #</span><span class="sxs-lookup"><span data-stu-id="21a8c-3366">DriversLicenses#</span></span> 
- <span data-ttu-id="21a8c-3367">Drivers Lic#</span><span class="sxs-lookup"><span data-stu-id="21a8c-3367">Drivers Lic#</span></span> 
- <span data-ttu-id="21a8c-3368">Drivers Lics#</span><span class="sxs-lookup"><span data-stu-id="21a8c-3368">Drivers Lics#</span></span> 
- <span data-ttu-id="21a8c-3369">Drivers License#</span><span class="sxs-lookup"><span data-stu-id="21a8c-3369">Drivers License#</span></span> 
- <span data-ttu-id="21a8c-3370">Drivers Licenses#</span><span class="sxs-lookup"><span data-stu-id="21a8c-3370">Drivers Licenses#</span></span> 
- <span data-ttu-id="21a8c-3371">Driver'Lic #</span><span class="sxs-lookup"><span data-stu-id="21a8c-3371">Driver'Lic#</span></span> 
- <span data-ttu-id="21a8c-3372">Driver'Lics #</span><span class="sxs-lookup"><span data-stu-id="21a8c-3372">Driver'Lics#</span></span> 
- <span data-ttu-id="21a8c-3373">Driver'License #</span><span class="sxs-lookup"><span data-stu-id="21a8c-3373">Driver'License#</span></span> 
- <span data-ttu-id="21a8c-3374">Driver'Licenses #</span><span class="sxs-lookup"><span data-stu-id="21a8c-3374">Driver'Licenses#</span></span> 
- <span data-ttu-id="21a8c-3375">Driver' Lic#</span><span class="sxs-lookup"><span data-stu-id="21a8c-3375">Driver' Lic#</span></span> 
- <span data-ttu-id="21a8c-3376">Driver' Lics#</span><span class="sxs-lookup"><span data-stu-id="21a8c-3376">Driver' Lics#</span></span> 
- <span data-ttu-id="21a8c-3377">Driver' License#</span><span class="sxs-lookup"><span data-stu-id="21a8c-3377">Driver' License#</span></span> 
- <span data-ttu-id="21a8c-3378">Driver' Licenses#</span><span class="sxs-lookup"><span data-stu-id="21a8c-3378">Driver' Licenses#</span></span> 
- <span data-ttu-id="21a8c-3379">Driver'sLic #</span><span class="sxs-lookup"><span data-stu-id="21a8c-3379">Driver'sLic#</span></span> 
- <span data-ttu-id="21a8c-3380">Driver'sLics #</span><span class="sxs-lookup"><span data-stu-id="21a8c-3380">Driver'sLics#</span></span> 
- <span data-ttu-id="21a8c-3381">Driver'sLicense #</span><span class="sxs-lookup"><span data-stu-id="21a8c-3381">Driver'sLicense#</span></span> 
- <span data-ttu-id="21a8c-3382">Driver'sLicenses #</span><span class="sxs-lookup"><span data-stu-id="21a8c-3382">Driver'sLicenses#</span></span> 
- <span data-ttu-id="21a8c-3383">Driver's Lic#</span><span class="sxs-lookup"><span data-stu-id="21a8c-3383">Driver's Lic#</span></span> 
- <span data-ttu-id="21a8c-3384">Driver's Lics#</span><span class="sxs-lookup"><span data-stu-id="21a8c-3384">Driver's Lics#</span></span> 
- <span data-ttu-id="21a8c-3385">Driver's License#</span><span class="sxs-lookup"><span data-stu-id="21a8c-3385">Driver's License#</span></span> 
- <span data-ttu-id="21a8c-3386">Driver's Licenses#</span><span class="sxs-lookup"><span data-stu-id="21a8c-3386">Driver's Licenses#</span></span> 
- <span data-ttu-id="21a8c-3387">id card#</span><span class="sxs-lookup"><span data-stu-id="21a8c-3387">id card#</span></span> 
- <span data-ttu-id="21a8c-3388">id cards#</span><span class="sxs-lookup"><span data-stu-id="21a8c-3388">id cards#</span></span> 
- <span data-ttu-id="21a8c-3389">identification card#</span><span class="sxs-lookup"><span data-stu-id="21a8c-3389">identification card#</span></span> 
- <span data-ttu-id="21a8c-3390">identification cards#</span><span class="sxs-lookup"><span data-stu-id="21a8c-3390">identification cards#</span></span> 


#### <a name="keywordstatenamedriverslicensename"></a><span data-ttu-id="21a8c-3391">Keyword_ [state_name] _drivers_license_name</span><span class="sxs-lookup"><span data-stu-id="21a8c-3391">Keyword_[state_name]_drivers_license_name</span></span>

- <span data-ttu-id="21a8c-3392">Abreviação do estado (por exemplo, "NY")</span><span class="sxs-lookup"><span data-stu-id="21a8c-3392">State abbreviation (for example, "NY")</span></span> 
- <span data-ttu-id="21a8c-3393">Nome do estado (por exemplo, "Nova York")</span><span class="sxs-lookup"><span data-stu-id="21a8c-3393">State name (for example, "New York")</span></span>    
   
## <a name="us-individual-taxpayer-identification-number-itin"></a><span data-ttu-id="21a8c-3394">Número de identificação de contribuinte individual (ITIN) dos EUA</span><span class="sxs-lookup"><span data-stu-id="21a8c-3394">U.S. Individual Taxpayer Identification Number (ITIN)</span></span>

### <a name="format"></a><span data-ttu-id="21a8c-3395">Format</span><span class="sxs-lookup"><span data-stu-id="21a8c-3395">Format</span></span>

<span data-ttu-id="21a8c-3396">Nove dígitos que começam com "9" e contêm um "7" ou "8" como o quarto dígito, opcionalmente formatado com espaços ou traços</span><span class="sxs-lookup"><span data-stu-id="21a8c-3396">Nine digits that start with a "9" and contain a "7" or "8" as the fourth digit, optionally formatted with spaces or dashes</span></span>

### <a name="pattern"></a><span data-ttu-id="21a8c-3397">Padrão</span><span class="sxs-lookup"><span data-stu-id="21a8c-3397">Pattern</span></span>

<span data-ttu-id="21a8c-3398">Binário</span><span class="sxs-lookup"><span data-stu-id="21a8c-3398">Formatted:</span></span>
- <span data-ttu-id="21a8c-3399">O dígito "9"</span><span class="sxs-lookup"><span data-stu-id="21a8c-3399">The digit "9"</span></span> 
- <span data-ttu-id="21a8c-3400">Dois dígitos</span><span class="sxs-lookup"><span data-stu-id="21a8c-3400">Two digits</span></span> 
- <span data-ttu-id="21a8c-3401">Um espaço ou um traço</span><span class="sxs-lookup"><span data-stu-id="21a8c-3401">A space or dash</span></span> 
- <span data-ttu-id="21a8c-3402">Um "7" ou "8"</span><span class="sxs-lookup"><span data-stu-id="21a8c-3402">A "7" or "8"</span></span> 
- <span data-ttu-id="21a8c-3403">Um dígito</span><span class="sxs-lookup"><span data-stu-id="21a8c-3403">A digit</span></span> 
- <span data-ttu-id="21a8c-3404">Um espaço ou um traço</span><span class="sxs-lookup"><span data-stu-id="21a8c-3404">A space, or dash</span></span> 
- <span data-ttu-id="21a8c-3405">Quatro dígitos</span><span class="sxs-lookup"><span data-stu-id="21a8c-3405">Four digits</span></span>

<span data-ttu-id="21a8c-3406">Não formatado</span><span class="sxs-lookup"><span data-stu-id="21a8c-3406">Unformatted:</span></span>
- <span data-ttu-id="21a8c-3407">O dígito "9"</span><span class="sxs-lookup"><span data-stu-id="21a8c-3407">The digit "9"</span></span> 
- <span data-ttu-id="21a8c-3408">Dois dígitos</span><span class="sxs-lookup"><span data-stu-id="21a8c-3408">Two digits</span></span> 
- <span data-ttu-id="21a8c-3409">Um "7" ou "8"</span><span class="sxs-lookup"><span data-stu-id="21a8c-3409">A "7" or "8"</span></span> 
- <span data-ttu-id="21a8c-3410">Cinco dígitos</span><span class="sxs-lookup"><span data-stu-id="21a8c-3410">Five digits</span></span>

### <a name="checksum"></a><span data-ttu-id="21a8c-3411">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="21a8c-3411">Checksum</span></span>

<span data-ttu-id="21a8c-3412">Não</span><span class="sxs-lookup"><span data-stu-id="21a8c-3412">No</span></span>

### <a name="definition"></a><span data-ttu-id="21a8c-3413">Definição</span><span class="sxs-lookup"><span data-stu-id="21a8c-3413">Definition</span></span>

<span data-ttu-id="21a8c-3414">Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="21a8c-3414">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="21a8c-3415">A função Func_formatted_itin localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="21a8c-3415">The function Func_formatted_itin finds content that matches the pattern.</span></span>
- <span data-ttu-id="21a8c-3416">Pelo menos uma das seguintes opções for verdadeira:</span><span class="sxs-lookup"><span data-stu-id="21a8c-3416">At least one of the following is true:</span></span>
    - <span data-ttu-id="21a8c-3417">Uma palavra-chave de Keyword_itin for encontrada.</span><span class="sxs-lookup"><span data-stu-id="21a8c-3417">A keyword from Keyword_itin is found.</span></span>
    - <span data-ttu-id="21a8c-3418">A função Func_us_address encontrar um endereço no formato de data à direita.</span><span class="sxs-lookup"><span data-stu-id="21a8c-3418">The function Func_us_address finds an address in the right date format.</span></span>
    - <span data-ttu-id="21a8c-3419">A função Func_us_date encontra uma data no formato de data à direita.</span><span class="sxs-lookup"><span data-stu-id="21a8c-3419">The function Func_us_date finds a date in the right date format.</span></span>
    - <span data-ttu-id="21a8c-3420">Uma palavra-chave de Keyword_itin_collaborative for encontrada.</span><span class="sxs-lookup"><span data-stu-id="21a8c-3420">A keyword from Keyword_itin_collaborative is found.</span></span>

<span data-ttu-id="21a8c-3421">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="21a8c-3421">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="21a8c-3422">A função Func_unformatted_itin localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="21a8c-3422">The function Func_unformatted_itin finds content that matches the pattern.</span></span>
- <span data-ttu-id="21a8c-3423">Pelo menos uma das seguintes opções for verdadeira:</span><span class="sxs-lookup"><span data-stu-id="21a8c-3423">At least one of the following is true:</span></span>
    - <span data-ttu-id="21a8c-3424">Uma palavra-chave de Keyword_itin_collaborative for encontrada.</span><span class="sxs-lookup"><span data-stu-id="21a8c-3424">A keyword from Keyword_itin_collaborative is found.</span></span>
    - <span data-ttu-id="21a8c-3425">A função Func_us_address encontrar um endereço no formato de data à direita.</span><span class="sxs-lookup"><span data-stu-id="21a8c-3425">The function Func_us_address finds an address in the right date format.</span></span>
    - <span data-ttu-id="21a8c-3426">A função Func_us_date encontra uma data no formato de data à direita.</span><span class="sxs-lookup"><span data-stu-id="21a8c-3426">The function Func_us_date finds a date in the right date format.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="21a8c-3427">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="21a8c-3427">Keywords</span></span>

#### <a name="keyworditin"></a><span data-ttu-id="21a8c-3428">Keyword_itin</span><span class="sxs-lookup"><span data-stu-id="21a8c-3428">Keyword_itin</span></span>

- <span data-ttu-id="21a8c-3429">contribui</span><span class="sxs-lookup"><span data-stu-id="21a8c-3429">taxpayer</span></span> 
- <span data-ttu-id="21a8c-3430">tax id</span><span class="sxs-lookup"><span data-stu-id="21a8c-3430">tax id</span></span> 
- <span data-ttu-id="21a8c-3431">tax identification</span><span class="sxs-lookup"><span data-stu-id="21a8c-3431">tax identification</span></span> 
- <span data-ttu-id="21a8c-3432">ITIN</span><span class="sxs-lookup"><span data-stu-id="21a8c-3432">itin</span></span> 
- <span data-ttu-id="21a8c-3433">es</span><span class="sxs-lookup"><span data-stu-id="21a8c-3433">ssn</span></span> 
- <span data-ttu-id="21a8c-3434">Tin</span><span class="sxs-lookup"><span data-stu-id="21a8c-3434">tin</span></span> 
- <span data-ttu-id="21a8c-3435">social security</span><span class="sxs-lookup"><span data-stu-id="21a8c-3435">social security</span></span> 
- <span data-ttu-id="21a8c-3436">tax payer</span><span class="sxs-lookup"><span data-stu-id="21a8c-3436">tax payer</span></span> 
- <span data-ttu-id="21a8c-3437">itins</span><span class="sxs-lookup"><span data-stu-id="21a8c-3437">itins</span></span> 
- <span data-ttu-id="21a8c-3438">táxi</span><span class="sxs-lookup"><span data-stu-id="21a8c-3438">taxid</span></span> 
- <span data-ttu-id="21a8c-3439">individual taxpayer</span><span class="sxs-lookup"><span data-stu-id="21a8c-3439">individual taxpayer</span></span> 

#### <a name="keyworditincollaborative"></a><span data-ttu-id="21a8c-3440">Keyword_itin_collaborative</span><span class="sxs-lookup"><span data-stu-id="21a8c-3440">Keyword_itin_collaborative</span></span>

- <span data-ttu-id="21a8c-3441">License</span><span class="sxs-lookup"><span data-stu-id="21a8c-3441">License</span></span> 
- <span data-ttu-id="21a8c-3442">DISTRIBUIÇÃO</span><span class="sxs-lookup"><span data-stu-id="21a8c-3442">DL</span></span> 
- <span data-ttu-id="21a8c-3443">DOB</span><span class="sxs-lookup"><span data-stu-id="21a8c-3443">DOB</span></span> 
- <span data-ttu-id="21a8c-3444">Data de Nascimento</span><span class="sxs-lookup"><span data-stu-id="21a8c-3444">Birthdate</span></span> 
- <span data-ttu-id="21a8c-3445">Aniversário</span><span class="sxs-lookup"><span data-stu-id="21a8c-3445">Birthday</span></span> 
- <span data-ttu-id="21a8c-3446">Date of Birth</span><span class="sxs-lookup"><span data-stu-id="21a8c-3446">Date of Birth</span></span> 
   
## <a name="us-social-security-number-ssn"></a><span data-ttu-id="21a8c-3447">Número de seguridade social dos EUA (SSN)</span><span class="sxs-lookup"><span data-stu-id="21a8c-3447">U.S. Social Security Number (SSN)</span></span>

### <a name="format"></a><span data-ttu-id="21a8c-3448">Format</span><span class="sxs-lookup"><span data-stu-id="21a8c-3448">Format</span></span>

<span data-ttu-id="21a8c-3449">9 dígitos que podem estar em um padrão formatado ou não formatado</span><span class="sxs-lookup"><span data-stu-id="21a8c-3449">9 digits, which may be in a formatted or unformatted pattern</span></span>

> [!NOTE]
> <span data-ttu-id="21a8c-3450">Se emitido antes de meados de 2011, um SSN tem uma formatação forte, onde determinadas partes do número devem estar dentro de determinados intervalos para serem válidos (mas não há nenhum checksum).</span><span class="sxs-lookup"><span data-stu-id="21a8c-3450">If issued before mid-2011, an SSN has strong formatting where certain parts of the number must fall within certain ranges to be valid (but there's no checksum).</span></span>

### <a name="pattern"></a><span data-ttu-id="21a8c-3451">Padrão</span><span class="sxs-lookup"><span data-stu-id="21a8c-3451">Pattern</span></span>

<span data-ttu-id="21a8c-3452">Quatro funções procuram CPFs em quatro padrões diferentes:</span><span class="sxs-lookup"><span data-stu-id="21a8c-3452">Four functions look for SSNs in four different patterns:</span></span>
- <span data-ttu-id="21a8c-3453">Func_ssn localiza CPFs com uma formatação forte de 2011 formatada com traços ou espaços (DDD-DD-dddd ou DDD DD dddd)</span><span class="sxs-lookup"><span data-stu-id="21a8c-3453">Func_ssn finds SSNs with pre-2011 strong formatting that are formatted with dashes or spaces (ddd-dd-dddd OR ddd dd dddd)</span></span>
- <span data-ttu-id="21a8c-3454">Func_unformatted_ssn localiza o CPFs com uma formatação forte de 2011 que não são formatados como nove dígitos consecutivos (ddddddddd)</span><span class="sxs-lookup"><span data-stu-id="21a8c-3454">Func_unformatted_ssn finds SSNs with pre-2011 strong formatting that are unformatted as nine consecutive digits (ddddddddd)</span></span>
- <span data-ttu-id="21a8c-3455">Func_randomized_formatted_ssn localiza o post-2011 CPFs que são formatados com traços ou espaços (DDD-DD-dddd ou DDD DD dddd)</span><span class="sxs-lookup"><span data-stu-id="21a8c-3455">Func_randomized_formatted_ssn finds post-2011 SSNs that are formatted with dashes or spaces (ddd-dd-dddd OR ddd dd dddd)</span></span>
- <span data-ttu-id="21a8c-3456">Func_randomized_unformatted_ssn localiza o post-2011 CPFs que não estão formatados como nove dígitos consecutivos (ddddddddd)</span><span class="sxs-lookup"><span data-stu-id="21a8c-3456">Func_randomized_unformatted_ssn finds post-2011 SSNs that are unformatted as nine consecutive digits (ddddddddd)</span></span>

### <a name="checksum"></a><span data-ttu-id="21a8c-3457">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="21a8c-3457">Checksum</span></span>

<span data-ttu-id="21a8c-3458">Não</span><span class="sxs-lookup"><span data-stu-id="21a8c-3458">No</span></span>


### <a name="definition"></a><span data-ttu-id="21a8c-3459">Definição</span><span class="sxs-lookup"><span data-stu-id="21a8c-3459">Definition</span></span>

<span data-ttu-id="21a8c-3460">Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="21a8c-3460">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="21a8c-3461">A função Func_ssn localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="21a8c-3461">The function Func_ssn finds content that matches the pattern.</span></span>
- <span data-ttu-id="21a8c-3462">Uma palavra-chave de Keyword_ssn for encontrada.</span><span class="sxs-lookup"><span data-stu-id="21a8c-3462">A keyword from Keyword_ssn is found.</span></span>

<span data-ttu-id="21a8c-3463">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="21a8c-3463">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="21a8c-3464">A função Func_unformatted_ssn localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="21a8c-3464">The function Func_unformatted_ssn finds content that matches the pattern.</span></span>
- <span data-ttu-id="21a8c-3465">Uma palavra-chave de Keyword_ssn for encontrada.</span><span class="sxs-lookup"><span data-stu-id="21a8c-3465">A keyword from Keyword_ssn is found.</span></span>

<span data-ttu-id="21a8c-3466">Uma política de DLP tem 65% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="21a8c-3466">A DLP policy is 65% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="21a8c-3467">A função Func_randomized_formatted_ssn localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="21a8c-3467">The function Func_randomized_formatted_ssn finds content that matches the pattern.</span></span>
- <span data-ttu-id="21a8c-3468">Uma palavra-chave de Keyword_ssn for encontrada.</span><span class="sxs-lookup"><span data-stu-id="21a8c-3468">A keyword from Keyword_ssn is found.</span></span>
- <span data-ttu-id="21a8c-3469">A função Func_ssn não localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="21a8c-3469">The function Func_ssn does not find content that matches the pattern.</span></span>

<span data-ttu-id="21a8c-3470">Uma política de DLP tem 55% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="21a8c-3470">A DLP policy is 55% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="21a8c-3471">A função Func_randomized_unformatted_ssn localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="21a8c-3471">The function Func_randomized_unformatted_ssn finds content that matches the pattern.</span></span>
- <span data-ttu-id="21a8c-3472">Uma palavra-chave de Keyword_ssn for encontrada.</span><span class="sxs-lookup"><span data-stu-id="21a8c-3472">A keyword from Keyword_ssn is found.</span></span>
- <span data-ttu-id="21a8c-3473">A função Func_unformatted_ssn não localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="21a8c-3473">The function Func_unformatted_ssn does not find content that matches the pattern.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="21a8c-3474">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="21a8c-3474">Keywords</span></span>

#### <a name="keywordssn"></a><span data-ttu-id="21a8c-3475">Keyword_ssn</span><span class="sxs-lookup"><span data-stu-id="21a8c-3475">Keyword_ssn</span></span>

- <span data-ttu-id="21a8c-3476">Social Security</span><span class="sxs-lookup"><span data-stu-id="21a8c-3476">Social Security</span></span> 
- <span data-ttu-id="21a8c-3477">Social Security#</span><span class="sxs-lookup"><span data-stu-id="21a8c-3477">Social Security#</span></span> 
- <span data-ttu-id="21a8c-3478">Soc Sec</span><span class="sxs-lookup"><span data-stu-id="21a8c-3478">Soc Sec</span></span> 
- <span data-ttu-id="21a8c-3479">ES</span><span class="sxs-lookup"><span data-stu-id="21a8c-3479">SSN</span></span> 
- <span data-ttu-id="21a8c-3480">CPFs</span><span class="sxs-lookup"><span data-stu-id="21a8c-3480">SSNS</span></span> 
- <span data-ttu-id="21a8c-3481">ES</span><span class="sxs-lookup"><span data-stu-id="21a8c-3481">SSN#</span></span> 
- <span data-ttu-id="21a8c-3482">PLANILHA</span><span class="sxs-lookup"><span data-stu-id="21a8c-3482">SS#</span></span> 
- <span data-ttu-id="21a8c-3483">SSID</span><span class="sxs-lookup"><span data-stu-id="21a8c-3483">SSID</span></span> 
   

