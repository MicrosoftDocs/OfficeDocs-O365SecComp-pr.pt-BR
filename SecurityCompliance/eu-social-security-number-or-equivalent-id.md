---
title: Número de seguro social da UE ou ID equivalente
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: 8/17/2018
ms.audience: Admin
ms.topic: reference
ms.service: O365-seccomp
ms.collection: M365-security-compliance
localization_priority: Normal
description: Este tópico mostra o que uma política de prevenção de perda de dados (DLP) procura quando detecta o número de segurança social da UE ou o tipo de informação confidencial de ID equivalente. Esse tipo de informação confidencial define diferentes padrões, palavras-chave e outras evidências para cada país.
ms.openlocfilehash: c0c808eafa52209c79f3b4e8a2113f587fd8a771
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32255549"
---
# <a name="eu-social-security-number-or-equivalent-id"></a><span data-ttu-id="08668-104">Número de seguro social da UE ou ID equivalente</span><span class="sxs-lookup"><span data-stu-id="08668-104">EU Social Security Number or Equivalent ID</span></span>

<span data-ttu-id="08668-105">Este tópico mostra o que uma política de prevenção de perda de dados (DLP) procura quando detecta o número de segurança social da UE (SSN) ou o tipo de informação confidencial de ID equivalente.</span><span class="sxs-lookup"><span data-stu-id="08668-105">This topic shows what a data loss prevention (DLP) policy looks for when it detects the EU Social Security Number (SSN) or Equivalent ID sensitive information type.</span></span> <span data-ttu-id="08668-106">Esse tipo de informação confidencial define diferentes padrões, palavras-chave e outras evidências para cada país.</span><span class="sxs-lookup"><span data-stu-id="08668-106">This sensitive information type defines different patterns, keywords, and other evidence for each country.</span></span>
  
## <a name="austria"></a><span data-ttu-id="08668-107">Áustria </span><span class="sxs-lookup"><span data-stu-id="08668-107">Austria</span></span>

### <a name="format"></a><span data-ttu-id="08668-108">Formatar</span><span class="sxs-lookup"><span data-stu-id="08668-108">Format</span></span>

<span data-ttu-id="08668-109">10 dígitos no formato especificado</span><span class="sxs-lookup"><span data-stu-id="08668-109">10 digits in the specified format</span></span>
  
### <a name="pattern"></a><span data-ttu-id="08668-110">Padrão</span><span class="sxs-lookup"><span data-stu-id="08668-110">Pattern</span></span>

<span data-ttu-id="08668-111">10 dígitos:</span><span class="sxs-lookup"><span data-stu-id="08668-111">10 digits:</span></span>
  
-  <span data-ttu-id="08668-112">Três dígitos que correspondem a um número de série</span><span class="sxs-lookup"><span data-stu-id="08668-112">Three digits that correspond to a serial number</span></span> 
    
- <span data-ttu-id="08668-113">Um dígito de verificação</span><span class="sxs-lookup"><span data-stu-id="08668-113">One check digit</span></span>
    
- <span data-ttu-id="08668-114">Seis dígitos que correspondem à data de nascimento (DDMMAA)</span><span class="sxs-lookup"><span data-stu-id="08668-114">Six digits that correspond to the birth date (DDMMYY)</span></span>
    
### <a name="checksum"></a><span data-ttu-id="08668-115">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="08668-115">Checksum</span></span>

<span data-ttu-id="08668-116">Sim</span><span class="sxs-lookup"><span data-stu-id="08668-116">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="08668-117">Definição</span><span class="sxs-lookup"><span data-stu-id="08668-117">Definition</span></span>

<span data-ttu-id="08668-118">Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="08668-118">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="08668-119">A função `Func_austria_eu_ssn_or_equivalent` localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="08668-119">The function  `Func_austria_eu_ssn_or_equivalent` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="08668-120">Uma palavra- `Keywords_austria_eu_ssn_or_equivalent` chave de foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="08668-120">A keyword from  `Keywords_austria_eu_ssn_or_equivalent` is found.</span></span> 
    
<span data-ttu-id="08668-121">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="08668-121">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="08668-122">A função `Func_austria_eu_ssn_or_equivalent` localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="08668-122">The function  `Func_austria_eu_ssn_or_equivalent` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU SSN or Equivalent Number -->
<Entity id="d24e32a4-c0bb-4ba8-899d-6303b95742d9" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_austria_eu_ssn_or_equivalent" />
          <Match idRef="Keywords_austria_eu_ssn_or_equivalent" />
        </Pattern>
<Pattern confidenceLevel="75">
            <IdMatch idRef="Func_austria_eu_ssn_or_equivalent" />
          </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="08668-123">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="08668-123">Keywords</span></span>

#### <a name="keywordsaustriaeussnorequivalent"></a><span data-ttu-id="08668-124">Keywords_austria_eu_ssn_or_equivalent</span><span class="sxs-lookup"><span data-stu-id="08668-124">Keywords_austria_eu_ssn_or_equivalent</span></span>

<span data-ttu-id="08668-125">segurança social não</span><span class="sxs-lookup"><span data-stu-id="08668-125">social security no</span></span>
  
<span data-ttu-id="08668-126">social security number</span><span class="sxs-lookup"><span data-stu-id="08668-126">social security number</span></span>
  
<span data-ttu-id="08668-127">social security code</span><span class="sxs-lookup"><span data-stu-id="08668-127">social security code</span></span>
  
<span data-ttu-id="08668-128">número de seguro</span><span class="sxs-lookup"><span data-stu-id="08668-128">insurance number</span></span>
  
<span data-ttu-id="08668-129">SSN austríaco</span><span class="sxs-lookup"><span data-stu-id="08668-129">austrian ssn</span></span>
  
<span data-ttu-id="08668-130">es</span><span class="sxs-lookup"><span data-stu-id="08668-130">ssn#</span></span>
  
<span data-ttu-id="08668-131">es</span><span class="sxs-lookup"><span data-stu-id="08668-131">ssn</span></span>
  
<span data-ttu-id="08668-132">código de seguro</span><span class="sxs-lookup"><span data-stu-id="08668-132">insurance code</span></span>
  
<span data-ttu-id="08668-133">código de seguro #</span><span class="sxs-lookup"><span data-stu-id="08668-133">insurance code#</span></span>
  
<span data-ttu-id="08668-134">socialsecurityno #</span><span class="sxs-lookup"><span data-stu-id="08668-134">socialsecurityno#</span></span>
  
<span data-ttu-id="08668-135">sozialversicherungsnummer</span><span class="sxs-lookup"><span data-stu-id="08668-135">sozialversicherungsnummer</span></span>
  
<span data-ttu-id="08668-136">soziale Sicherheit Kein</span><span class="sxs-lookup"><span data-stu-id="08668-136">soziale sicherheit kein</span></span>
  
<span data-ttu-id="08668-137">versicherungsnummer</span><span class="sxs-lookup"><span data-stu-id="08668-137">versicherungsnummer</span></span>
  
## <a name="belgium"></a><span data-ttu-id="08668-138">Bélgica </span><span class="sxs-lookup"><span data-stu-id="08668-138">Belgium</span></span>

### <a name="format"></a><span data-ttu-id="08668-139">Formatar</span><span class="sxs-lookup"><span data-stu-id="08668-139">Format</span></span>

<span data-ttu-id="08668-140">11 dígitos sem espaços ou delimitadores</span><span class="sxs-lookup"><span data-stu-id="08668-140">11 digits without spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="08668-141">Padrão</span><span class="sxs-lookup"><span data-stu-id="08668-141">Pattern</span></span>

<span data-ttu-id="08668-142">11 dígitos</span><span class="sxs-lookup"><span data-stu-id="08668-142">11 digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="08668-143">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="08668-143">Checksum</span></span>

<span data-ttu-id="08668-144">Sim</span><span class="sxs-lookup"><span data-stu-id="08668-144">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="08668-145">Definição</span><span class="sxs-lookup"><span data-stu-id="08668-145">Definition</span></span>

<span data-ttu-id="08668-146">Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="08668-146">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="08668-147">A função `Func_belgium_eu_ssn_or_equivalent` localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="08668-147">The function  `Func_belgium_eu_ssn_or_equivalent` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="08668-148">Uma palavra- `Keywords_belgium_eu_ssn_or_equivalent` chave de foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="08668-148">A keyword from  `Keywords_belgium_eu_ssn_or_equivalent` is found.</span></span> 
    
<span data-ttu-id="08668-149">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="08668-149">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="08668-150">A função `Func_belgium_eu_ssn_or_equivalent` localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="08668-150">The function  `Func_belgium_eu_ssn_or_equivalent` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU SSN or Equivalent Number -->
<Entity id="d24e32a4-c0bb-4ba8-899d-6303b95742d9" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_belgium_eu_ssn_or_equivalent" />
          <Match idRef="Keywords_belgium_eu_ssn_or_equivalent" />
        </Pattern> 
       <Pattern confidenceLevel="75">
          <IdMatch idRef="Func_belgium_eu_ssn_or_equivalent" />
        </Pattern>      
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="08668-151">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="08668-151">Keywords</span></span>

#### <a name="keywordsbelgiumeussnorequivalent"></a><span data-ttu-id="08668-152">Keywords_belgium_eu_ssn_or_equivalent</span><span class="sxs-lookup"><span data-stu-id="08668-152">Keywords_belgium_eu_ssn_or_equivalent</span></span>

<span data-ttu-id="08668-153">número Nacional belga</span><span class="sxs-lookup"><span data-stu-id="08668-153">belgian national number</span></span>
  
<span data-ttu-id="08668-154">número nacional</span><span class="sxs-lookup"><span data-stu-id="08668-154">national number</span></span>
  
<span data-ttu-id="08668-155">social security number</span><span class="sxs-lookup"><span data-stu-id="08668-155">social security number</span></span>
  
<span data-ttu-id="08668-156">nationalnumber #</span><span class="sxs-lookup"><span data-stu-id="08668-156">nationalnumber#</span></span>
  
<span data-ttu-id="08668-157">es</span><span class="sxs-lookup"><span data-stu-id="08668-157">ssn#</span></span>
  
<span data-ttu-id="08668-158">es</span><span class="sxs-lookup"><span data-stu-id="08668-158">ssn</span></span>
  
<span data-ttu-id="08668-159">nationalnumber</span><span class="sxs-lookup"><span data-stu-id="08668-159">nationalnumber</span></span>
  
<span data-ttu-id="08668-160">BNN #</span><span class="sxs-lookup"><span data-stu-id="08668-160">bnn#</span></span>
  
<span data-ttu-id="08668-161">BNN</span><span class="sxs-lookup"><span data-stu-id="08668-161">bnn</span></span>
  
<span data-ttu-id="08668-162">número de identificação pessoal</span><span class="sxs-lookup"><span data-stu-id="08668-162">personal id number</span></span>
  
<span data-ttu-id="08668-163">personalidnumber #</span><span class="sxs-lookup"><span data-stu-id="08668-163">personalidnumber#</span></span>
  
<span data-ttu-id="08668-164">nacional Numéro</span><span class="sxs-lookup"><span data-stu-id="08668-164">numéro national</span></span>
  
<span data-ttu-id="08668-165">numéro de sécurité</span><span class="sxs-lookup"><span data-stu-id="08668-165">numéro de sécurité</span></span>
  
<span data-ttu-id="08668-166">Numéro d'assuré</span><span class="sxs-lookup"><span data-stu-id="08668-166">numéro d'assuré</span></span>
  
<span data-ttu-id="08668-167">nacional de identificação</span><span class="sxs-lookup"><span data-stu-id="08668-167">identifiant national</span></span>
  
<span data-ttu-id="08668-168">identifiantnational #</span><span class="sxs-lookup"><span data-stu-id="08668-168">identifiantnational#</span></span>
  
<span data-ttu-id="08668-169">numéronational #</span><span class="sxs-lookup"><span data-stu-id="08668-169">numéronational#</span></span>
  
## <a name="croatia"></a><span data-ttu-id="08668-170">Croácia</span><span class="sxs-lookup"><span data-stu-id="08668-170">Croatia</span></span>

### <a name="format"></a><span data-ttu-id="08668-171">Formatar</span><span class="sxs-lookup"><span data-stu-id="08668-171">Format</span></span>

<span data-ttu-id="08668-172">11 dígitos sem espaços e delimitadores</span><span class="sxs-lookup"><span data-stu-id="08668-172">11 digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="08668-173">Padrão</span><span class="sxs-lookup"><span data-stu-id="08668-173">Pattern</span></span>

 <span data-ttu-id="08668-174">11 dígitos:</span><span class="sxs-lookup"><span data-stu-id="08668-174">11 digits:</span></span> 
  
-  <span data-ttu-id="08668-175">Dez dígitos</span><span class="sxs-lookup"><span data-stu-id="08668-175">Ten digits</span></span> 
    
- <span data-ttu-id="08668-176">Um dígito de verificação</span><span class="sxs-lookup"><span data-stu-id="08668-176">One check digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="08668-177">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="08668-177">Checksum</span></span>

<span data-ttu-id="08668-178">Sim</span><span class="sxs-lookup"><span data-stu-id="08668-178">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="08668-179">Definição</span><span class="sxs-lookup"><span data-stu-id="08668-179">Definition</span></span>

<span data-ttu-id="08668-180">Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="08668-180">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="08668-181">A função `Func_croatia_eu_ssn_or_equivalent` localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="08668-181">The function  `Func_croatia_eu_ssn_or_equivalent` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="08668-182">Uma palavra- `Keywords_croatia_eu_ssn_or_equivalent` chave de foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="08668-182">A keyword from  `Keywords_croatia_eu_ssn_or_equivalent` is found.</span></span> 
    
<span data-ttu-id="08668-183">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="08668-183">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="08668-184">A função `Func_croatia_eu_ssn_or_equivalent` localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="08668-184">The function  `Func_croatia_eu_ssn_or_equivalent` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU SSN or Equivalent Number -->
<Entity id="d24e32a4-c0bb-4ba8-899d-6303b95742d9" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_croatia_eu_ssn_or_equivalent" />
          <Match idRef="Keywords_croatia_eu_ssn_or_equivalent" />
        </Pattern> 
       <Pattern confidenceLevel="75">
          <IdMatch idRef="Func_croatia_eu_ssn_or_equivalent" />
        </Pattern>      
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="08668-185">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="08668-185">Keywords</span></span>

#### <a name="keywordscroatiaeussnorequivalent"></a><span data-ttu-id="08668-186">Keywords_croatia_eu_ssn_or_equivalent</span><span class="sxs-lookup"><span data-stu-id="08668-186">Keywords_croatia_eu_ssn_or_equivalent</span></span>

<span data-ttu-id="08668-187">número de identificação pessoal</span><span class="sxs-lookup"><span data-stu-id="08668-187">personal identification number</span></span>
  
<span data-ttu-id="08668-188">número do cidadão mestre</span><span class="sxs-lookup"><span data-stu-id="08668-188">master citizen number</span></span>
  
<span data-ttu-id="08668-189">national identification number</span><span class="sxs-lookup"><span data-stu-id="08668-189">national identification number</span></span>
  
<span data-ttu-id="08668-190">social security number</span><span class="sxs-lookup"><span data-stu-id="08668-190">social security number</span></span>
  
<span data-ttu-id="08668-191">nationalnumber #</span><span class="sxs-lookup"><span data-stu-id="08668-191">nationalnumber#</span></span>
  
<span data-ttu-id="08668-192">es</span><span class="sxs-lookup"><span data-stu-id="08668-192">ssn#</span></span>
  
<span data-ttu-id="08668-193">es</span><span class="sxs-lookup"><span data-stu-id="08668-193">ssn</span></span>
  
<span data-ttu-id="08668-194">nationalnumber</span><span class="sxs-lookup"><span data-stu-id="08668-194">nationalnumber</span></span>
  
<span data-ttu-id="08668-195">BNN #</span><span class="sxs-lookup"><span data-stu-id="08668-195">bnn#</span></span>
  
<span data-ttu-id="08668-196">BNN</span><span class="sxs-lookup"><span data-stu-id="08668-196">bnn</span></span>
  
<span data-ttu-id="08668-197">número de identificação pessoal</span><span class="sxs-lookup"><span data-stu-id="08668-197">personal id number</span></span>
  
<span data-ttu-id="08668-198">personalidnumber #</span><span class="sxs-lookup"><span data-stu-id="08668-198">personalidnumber#</span></span>
  
<span data-ttu-id="08668-199">NIB</span><span class="sxs-lookup"><span data-stu-id="08668-199">oib</span></span>
  
<span data-ttu-id="08668-200">Osobni identifikacijski broj</span><span class="sxs-lookup"><span data-stu-id="08668-200">osobni identifikacijski broj</span></span>
  
## <a name="czech-republic"></a><span data-ttu-id="08668-201">República Tcheca</span><span class="sxs-lookup"><span data-stu-id="08668-201">Czech Republic</span></span>

### <a name="format"></a><span data-ttu-id="08668-202">Formatar</span><span class="sxs-lookup"><span data-stu-id="08668-202">Format</span></span>

<span data-ttu-id="08668-203">Dez dígitos e uma barra invertida no padrão especificado</span><span class="sxs-lookup"><span data-stu-id="08668-203">Ten digits and a backslash in the specified pattern</span></span>
  
### <a name="pattern"></a><span data-ttu-id="08668-204">Padrão</span><span class="sxs-lookup"><span data-stu-id="08668-204">Pattern</span></span>

<span data-ttu-id="08668-205">Dez dígitos e uma barra invertida:</span><span class="sxs-lookup"><span data-stu-id="08668-205">Ten digits and a backslash:</span></span>
  
- <span data-ttu-id="08668-206">Seis dígitos que correspondem à data de nascimento (AAMMDD):</span><span class="sxs-lookup"><span data-stu-id="08668-206">Six digits that correspond to the birth date (YYMMDD):</span></span> 
    
- <span data-ttu-id="08668-207">Uma barra invertida</span><span class="sxs-lookup"><span data-stu-id="08668-207">A backslash</span></span>
    
- <span data-ttu-id="08668-208">Três dígitos que correspondem a um número de série que separa as pessoas nasceu na mesma data</span><span class="sxs-lookup"><span data-stu-id="08668-208">Three digits that correspond to a serial number that separates persons born on the same date</span></span>
    
- <span data-ttu-id="08668-209">Um dígito de verificação</span><span class="sxs-lookup"><span data-stu-id="08668-209">One check digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="08668-210">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="08668-210">Checksum</span></span>

<span data-ttu-id="08668-211">Sim</span><span class="sxs-lookup"><span data-stu-id="08668-211">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="08668-212">Definição</span><span class="sxs-lookup"><span data-stu-id="08668-212">Definition</span></span>

<span data-ttu-id="08668-213">Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="08668-213">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="08668-214">A função `Func_czech_republic_eu_ssn_or_equivalent` localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="08668-214">The function  `Func_czech_republic_eu_ssn_or_equivalent` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="08668-215">Uma palavra- `Keywords_czech_republic_eu_ssn_or_equivalent` chave de foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="08668-215">A keyword from  `Keywords_czech_republic_eu_ssn_or_equivalent` is found.</span></span> 
    
<span data-ttu-id="08668-216">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="08668-216">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="08668-217">A função `Func_czech_republic_eu_ssn_or_equivalent` localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="08668-217">The function  `Func_czech_republic_eu_ssn_or_equivalent` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU SSN or Equivalent Number -->
<Entity id="d24e32a4-c0bb-4ba8-899d-6303b95742d9" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_czech_republic_eu_ssn_or_equivalent" />
          <Match idRef="Keywords_czech_republic_eu_ssn_or_equivalent" />
        </Pattern> 
       <Pattern confidenceLevel="75">
          <IdMatch idRef="Func_czech_republic_eu_ssn_or_equivalent" />
        </Pattern>      
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="08668-218">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="08668-218">Keywords</span></span>

#### <a name="keywordsczechrepubliceussnorequivalent"></a><span data-ttu-id="08668-219">Keywords_czech_republic_eu_ssn_or_equivalent</span><span class="sxs-lookup"><span data-stu-id="08668-219">Keywords_czech_republic_eu_ssn_or_equivalent</span></span>

<span data-ttu-id="08668-220">número de nascimento</span><span class="sxs-lookup"><span data-stu-id="08668-220">birth number</span></span>
  
<span data-ttu-id="08668-221">national identification number</span><span class="sxs-lookup"><span data-stu-id="08668-221">national identification number</span></span>
  
<span data-ttu-id="08668-222">número de identificação pessoal</span><span class="sxs-lookup"><span data-stu-id="08668-222">personal identification number</span></span>
  
<span data-ttu-id="08668-223">social security number</span><span class="sxs-lookup"><span data-stu-id="08668-223">social security number</span></span>
  
<span data-ttu-id="08668-224">nationalnumber #</span><span class="sxs-lookup"><span data-stu-id="08668-224">nationalnumber#</span></span>
  
<span data-ttu-id="08668-225">es</span><span class="sxs-lookup"><span data-stu-id="08668-225">ssn#</span></span>
  
<span data-ttu-id="08668-226">es</span><span class="sxs-lookup"><span data-stu-id="08668-226">ssn</span></span>
  
<span data-ttu-id="08668-227">número nacional</span><span class="sxs-lookup"><span data-stu-id="08668-227">national number</span></span>
  
<span data-ttu-id="08668-228">número de identificação pessoal</span><span class="sxs-lookup"><span data-stu-id="08668-228">personal id number</span></span>
  
<span data-ttu-id="08668-229">personalidnumber #</span><span class="sxs-lookup"><span data-stu-id="08668-229">personalidnumber#</span></span>
  
<span data-ttu-id="08668-230">rč</span><span class="sxs-lookup"><span data-stu-id="08668-230">rč</span></span>
  
<span data-ttu-id="08668-231">rodné číslo</span><span class="sxs-lookup"><span data-stu-id="08668-231">rodné číslo</span></span>
  
<span data-ttu-id="08668-232">RODNE cislo</span><span class="sxs-lookup"><span data-stu-id="08668-232">rodne cislo</span></span>
  
## <a name="denmark"></a><span data-ttu-id="08668-233">Dinamarca</span><span class="sxs-lookup"><span data-stu-id="08668-233">Denmark</span></span>

### <a name="format"></a><span data-ttu-id="08668-234">Formatar</span><span class="sxs-lookup"><span data-stu-id="08668-234">Format</span></span>

<span data-ttu-id="08668-235">Dez dígitos e um hífen no padrão especificado</span><span class="sxs-lookup"><span data-stu-id="08668-235">Ten digits and a hyphen in the specified pattern</span></span>
  
### <a name="pattern"></a><span data-ttu-id="08668-236">Padrão</span><span class="sxs-lookup"><span data-stu-id="08668-236">Pattern</span></span>

<span data-ttu-id="08668-237">Dez dígitos e um hífen:</span><span class="sxs-lookup"><span data-stu-id="08668-237">Ten digits and a hyphen:</span></span>
  
- <span data-ttu-id="08668-238">Seis dígitos que correspondem à data de nascimento (DDMMAA)</span><span class="sxs-lookup"><span data-stu-id="08668-238">Six digits that correspond to the birth date (DDMMYY)</span></span> 
    
- <span data-ttu-id="08668-239">Um hífen</span><span class="sxs-lookup"><span data-stu-id="08668-239">A hyphen</span></span>
    
- <span data-ttu-id="08668-240">Quatro dígitos que correspondem a um número de sequência</span><span class="sxs-lookup"><span data-stu-id="08668-240">Four digits that correspond to a sequence number</span></span>
    
### <a name="checksum"></a><span data-ttu-id="08668-241">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="08668-241">Checksum</span></span>

<span data-ttu-id="08668-242">Sim</span><span class="sxs-lookup"><span data-stu-id="08668-242">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="08668-243">Definição</span><span class="sxs-lookup"><span data-stu-id="08668-243">Definition</span></span>

<span data-ttu-id="08668-244">Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="08668-244">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="08668-245">A função `Func_denmark_eu_ssn_or_equivalent` localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="08668-245">The function  `Func_denmark_eu_ssn_or_equivalent` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="08668-246">Uma palavra- `Keywords_denmark_eu_ssn_or_equivalent` chave de foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="08668-246">A keyword from  `Keywords_denmark_eu_ssn_or_equivalent` is found.</span></span> 
    
<span data-ttu-id="08668-247">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="08668-247">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="08668-248">A função `Func_denmark_eu_ssn_or_equivalent` localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="08668-248">The function  `Func_denmark_eu_ssn_or_equivalent` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU SSN or Equivalent Number -->
<Entity id="d24e32a4-c0bb-4ba8-899d-6303b95742d9" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_denmark_eu_ssn_or_equivalent" />
          <Match idRef="Keywords_denmark_eu_ssn_or_equivalent" />
        </Pattern> 
       <Pattern confidenceLevel="75">
          <IdMatch idRef="Func_denmark_eu_ssn_or_equivalent" />
        </Pattern>      
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="08668-249">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="08668-249">Keywords</span></span>

#### <a name="keywordsdenmarkeussnorequivalent"></a><span data-ttu-id="08668-250">Keywords_denmark_eu_ssn_or_equivalent</span><span class="sxs-lookup"><span data-stu-id="08668-250">Keywords_denmark_eu_ssn_or_equivalent</span></span>

<span data-ttu-id="08668-251">número de identificação pessoal</span><span class="sxs-lookup"><span data-stu-id="08668-251">personal identification number</span></span>
  
<span data-ttu-id="08668-252">national identification number</span><span class="sxs-lookup"><span data-stu-id="08668-252">national identification number</span></span>
  
<span data-ttu-id="08668-253">social security number</span><span class="sxs-lookup"><span data-stu-id="08668-253">social security number</span></span>
  
<span data-ttu-id="08668-254">nationalnumber #</span><span class="sxs-lookup"><span data-stu-id="08668-254">nationalnumber#</span></span>
  
<span data-ttu-id="08668-255">es</span><span class="sxs-lookup"><span data-stu-id="08668-255">ssn#</span></span>
  
<span data-ttu-id="08668-256">es</span><span class="sxs-lookup"><span data-stu-id="08668-256">ssn</span></span>
  
<span data-ttu-id="08668-257">número nacional</span><span class="sxs-lookup"><span data-stu-id="08668-257">national number</span></span>
  
<span data-ttu-id="08668-258">número de identificação pessoal</span><span class="sxs-lookup"><span data-stu-id="08668-258">personal id number</span></span>
  
<span data-ttu-id="08668-259">personalidnumber #</span><span class="sxs-lookup"><span data-stu-id="08668-259">personalidnumber#</span></span>
  
<span data-ttu-id="08668-260">CPR-Nummer</span><span class="sxs-lookup"><span data-stu-id="08668-260">cpr-nummer</span></span>
  
<span data-ttu-id="08668-261">personnummer</span><span class="sxs-lookup"><span data-stu-id="08668-261">personnummer</span></span>
  
## <a name="finland"></a><span data-ttu-id="08668-262">Finlândia</span><span class="sxs-lookup"><span data-stu-id="08668-262">Finland</span></span>

### <a name="format"></a><span data-ttu-id="08668-263">Formatar</span><span class="sxs-lookup"><span data-stu-id="08668-263">Format</span></span>

<span data-ttu-id="08668-264">Uma combinação de 11 caracteres no formato especificado</span><span class="sxs-lookup"><span data-stu-id="08668-264">An 11-character combination in the specified format</span></span>
  
### <a name="pattern"></a><span data-ttu-id="08668-265">Padrão</span><span class="sxs-lookup"><span data-stu-id="08668-265">Pattern</span></span>

<span data-ttu-id="08668-266">Uma combinação de 11 caracteres no formato especificado:</span><span class="sxs-lookup"><span data-stu-id="08668-266">An 11-character combination in the specified format:</span></span>
  
-  <span data-ttu-id="08668-267">Seis dígitos</span><span class="sxs-lookup"><span data-stu-id="08668-267">Six digits</span></span> 
    
- <span data-ttu-id="08668-268">Uma instância de um dos seguintes:</span><span class="sxs-lookup"><span data-stu-id="08668-268">One instance of one of the following:</span></span>
    
  - <span data-ttu-id="08668-269">Símbolo de adição</span><span class="sxs-lookup"><span data-stu-id="08668-269">Plus symbol</span></span>
    
  - <span data-ttu-id="08668-270">Símbolo de subTração</span><span class="sxs-lookup"><span data-stu-id="08668-270">Minus symbol</span></span>
    
  - <span data-ttu-id="08668-271">A letra "A" (não diferencia maiúsculas de minúsculas)</span><span class="sxs-lookup"><span data-stu-id="08668-271">The letter "A" (not case-sensitive)</span></span>
    
- <span data-ttu-id="08668-272">Três dígitos</span><span class="sxs-lookup"><span data-stu-id="08668-272">Three digits</span></span>
    
- <span data-ttu-id="08668-273">Uma letra ou um dígito</span><span class="sxs-lookup"><span data-stu-id="08668-273">One letter or one digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="08668-274">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="08668-274">Checksum</span></span>

<span data-ttu-id="08668-275">Sim</span><span class="sxs-lookup"><span data-stu-id="08668-275">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="08668-276">Definição</span><span class="sxs-lookup"><span data-stu-id="08668-276">Definition</span></span>

<span data-ttu-id="08668-277">Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="08668-277">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="08668-278">A função `Func_finland_eu_ssn_or_equivalent` localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="08668-278">The function  `Func_finland_eu_ssn_or_equivalent` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="08668-279">Uma palavra- `Keywords_finland_eu_ssn_or_equivalent` chave de foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="08668-279">A keyword from  `Keywords_finland_eu_ssn_or_equivalent` is found.</span></span> 
    
<span data-ttu-id="08668-280">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="08668-280">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="08668-281">A função `Func_finland_eu_ssn_or_equivalent` localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="08668-281">The function  `Func_finland_eu_ssn_or_equivalent` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU SSN or Equivalent Number -->
<Entity id="d24e32a4-c0bb-4ba8-899d-6303b95742d9" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_finland_eu_ssn_or_equivalent" />
          <Match idRef="Keywords_finland_eu_ssn_or_equivalent" />
        </Pattern> 
       <Pattern confidenceLevel="75">
          <IdMatch idRef="Func_finland_eu_ssn_or_equivalent" />
        </Pattern>      
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="08668-282">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="08668-282">Keywords</span></span>

#### <a name="keywordsfinlandeussnorequivalent"></a><span data-ttu-id="08668-283">Keywords_finland_eu_ssn_or_equivalent</span><span class="sxs-lookup"><span data-stu-id="08668-283">Keywords_finland_eu_ssn_or_equivalent</span></span>

<span data-ttu-id="08668-284">identification number</span><span class="sxs-lookup"><span data-stu-id="08668-284">identification number</span></span>
  
<span data-ttu-id="08668-285">ID pessoal</span><span class="sxs-lookup"><span data-stu-id="08668-285">personal id</span></span>
  
<span data-ttu-id="08668-286">número de identidade</span><span class="sxs-lookup"><span data-stu-id="08668-286">identity number</span></span>
  
<span data-ttu-id="08668-287">número de ID nacional da finlandês</span><span class="sxs-lookup"><span data-stu-id="08668-287">finnish national id number</span></span>
  
<span data-ttu-id="08668-288">personalidnumber #</span><span class="sxs-lookup"><span data-stu-id="08668-288">personalidnumber#</span></span>
  
<span data-ttu-id="08668-289">national identification number</span><span class="sxs-lookup"><span data-stu-id="08668-289">national identification number</span></span>
  
<span data-ttu-id="08668-290">número de identificação</span><span class="sxs-lookup"><span data-stu-id="08668-290">id number</span></span>
  
<span data-ttu-id="08668-291">n º de ID nacional</span><span class="sxs-lookup"><span data-stu-id="08668-291">national id no.</span></span>
  
<span data-ttu-id="08668-292">número de ID nacional</span><span class="sxs-lookup"><span data-stu-id="08668-292">national id number</span></span>
  
<span data-ttu-id="08668-293">ID não</span><span class="sxs-lookup"><span data-stu-id="08668-293">id no</span></span>
  
<span data-ttu-id="08668-294">tunnistenumero</span><span class="sxs-lookup"><span data-stu-id="08668-294">tunnistenumero</span></span>
  
<span data-ttu-id="08668-295">henkilötunnus</span><span class="sxs-lookup"><span data-stu-id="08668-295">henkilötunnus</span></span>
  
<span data-ttu-id="08668-296">yksilöllinen henkilökohtainen tunnistenumero</span><span class="sxs-lookup"><span data-stu-id="08668-296">yksilöllinen henkilökohtainen tunnistenumero</span></span>
  
<span data-ttu-id="08668-297">ainutlaatuinen henkilökohtainen Tunnus</span><span class="sxs-lookup"><span data-stu-id="08668-297">ainutlaatuinen henkilökohtainen tunnus</span></span>
  
<span data-ttu-id="08668-298">identiteetti numero</span><span class="sxs-lookup"><span data-stu-id="08668-298">identiteetti numero</span></span>
  
<span data-ttu-id="08668-299">Suomen Kansallinen henkilötunnus</span><span class="sxs-lookup"><span data-stu-id="08668-299">suomen kansallinen henkilötunnus</span></span>
  
<span data-ttu-id="08668-300">henkilötunnusnumero #</span><span class="sxs-lookup"><span data-stu-id="08668-300">henkilötunnusnumero#</span></span>
  
<span data-ttu-id="08668-301">kansallisen tunnistenumero</span><span class="sxs-lookup"><span data-stu-id="08668-301">kansallisen tunnistenumero</span></span>
  
<span data-ttu-id="08668-302">tunnusnumero</span><span class="sxs-lookup"><span data-stu-id="08668-302">tunnusnumero</span></span>
  
<span data-ttu-id="08668-303">Kansallinen Tunnus numero</span><span class="sxs-lookup"><span data-stu-id="08668-303">kansallinen tunnus numero</span></span>
  
<span data-ttu-id="08668-304">Hetu</span><span class="sxs-lookup"><span data-stu-id="08668-304">hetu</span></span>
  
## <a name="france"></a><span data-ttu-id="08668-305">França</span><span class="sxs-lookup"><span data-stu-id="08668-305">France</span></span>

<span data-ttu-id="08668-306">Para obter detalhes, consulte a seção "França Social Security Number (INSEE)" em [o que os tipos de informações confidenciais procuram](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="08668-306">For details, see the section "France Social Security Number (INSEE)" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="germany"></a><span data-ttu-id="08668-307">Alemanha</span><span class="sxs-lookup"><span data-stu-id="08668-307">Germany</span></span>

<span data-ttu-id="08668-308">Para obter detalhes, consulte a seção "número do cartão de identidade da Alemanha" em [o que os tipos de informações confidenciais buscam](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="08668-308">For details, see the section "Germany Identity Card Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="greece"></a><span data-ttu-id="08668-309">Grécia</span><span class="sxs-lookup"><span data-stu-id="08668-309">Greece</span></span>

<span data-ttu-id="08668-310">Para obter detalhes, consulte a seção "cartão de ID nacional da Grécia" em [que os tipos de informações confidenciais buscam](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="08668-310">For details, see the section "Greece National ID Card" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="hungary"></a><span data-ttu-id="08668-311">Hungria</span><span class="sxs-lookup"><span data-stu-id="08668-311">Hungary</span></span>

### <a name="format"></a><span data-ttu-id="08668-312">Formatar</span><span class="sxs-lookup"><span data-stu-id="08668-312">Format</span></span>

<span data-ttu-id="08668-313">Nove dígitos sem espaços e delimitadores</span><span class="sxs-lookup"><span data-stu-id="08668-313">Nine digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="08668-314">Padrão</span><span class="sxs-lookup"><span data-stu-id="08668-314">Pattern</span></span>

<span data-ttu-id="08668-315">Nove dígitos</span><span class="sxs-lookup"><span data-stu-id="08668-315">Nine digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="08668-316">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="08668-316">Checksum</span></span>

<span data-ttu-id="08668-317">Sim</span><span class="sxs-lookup"><span data-stu-id="08668-317">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="08668-318">Definição</span><span class="sxs-lookup"><span data-stu-id="08668-318">Definition</span></span>

<span data-ttu-id="08668-319">Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="08668-319">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="08668-320">A função `Func_hungary_eu_ssn_or_equivalent` localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="08668-320">The function  `Func_hungary_eu_ssn_or_equivalent` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="08668-321">Uma palavra- `Keywords_hungary_eu_ssn_or_equivalent` chave de foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="08668-321">A keyword from  `Keywords_hungary_eu_ssn_or_equivalent` is found.</span></span> 
    
<span data-ttu-id="08668-322">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="08668-322">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="08668-323">A função `Func_hungary_eu_ssn_or_equivalent` localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="08668-323">The function  `Func_hungary_eu_ssn_or_equivalent` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU SSN or Equivalent Number -->
<Entity id="d24e32a4-c0bb-4ba8-899d-6303b95742d9" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_hungary_eu_ssn_or_equivalent" />
          <Match idRef="Keywords_hungary_eu_ssn_or_equivalent" />
        </Pattern> 
       <Pattern confidenceLevel="75">
          <IdMatch idRef="Func_hungary_eu_ssn_or_equivalent" />
        </Pattern>      
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="08668-324">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="08668-324">Keywords</span></span>

#### <a name="keywordshungaryeussnorequivalent"></a><span data-ttu-id="08668-325">Keywords_hungary_eu_ssn_or_equivalent</span><span class="sxs-lookup"><span data-stu-id="08668-325">Keywords_hungary_eu_ssn_or_equivalent</span></span>

<span data-ttu-id="08668-326">número de seguro social de seguridade</span><span class="sxs-lookup"><span data-stu-id="08668-326">hungarian social security number</span></span>
  
<span data-ttu-id="08668-327">social security number</span><span class="sxs-lookup"><span data-stu-id="08668-327">social security number</span></span>
  
<span data-ttu-id="08668-328">socialSecurityNumber #</span><span class="sxs-lookup"><span data-stu-id="08668-328">socialsecuritynumber#</span></span>
  
<span data-ttu-id="08668-329">hssn #</span><span class="sxs-lookup"><span data-stu-id="08668-329">hssn#</span></span>
  
<span data-ttu-id="08668-330">socialsecuritynno</span><span class="sxs-lookup"><span data-stu-id="08668-330">socialsecuritynno</span></span>
  
<span data-ttu-id="08668-331">hssn</span><span class="sxs-lookup"><span data-stu-id="08668-331">hssn</span></span>
  
<span data-ttu-id="08668-332">Taj</span><span class="sxs-lookup"><span data-stu-id="08668-332">taj</span></span>
  
<span data-ttu-id="08668-333">Taj #</span><span class="sxs-lookup"><span data-stu-id="08668-333">taj#</span></span>
  
<span data-ttu-id="08668-334">es</span><span class="sxs-lookup"><span data-stu-id="08668-334">ssn</span></span>
  
<span data-ttu-id="08668-335">es</span><span class="sxs-lookup"><span data-stu-id="08668-335">ssn#</span></span>
  
<span data-ttu-id="08668-336">segurança social não</span><span class="sxs-lookup"><span data-stu-id="08668-336">social security no</span></span>
  
<span data-ttu-id="08668-337">áfa</span><span class="sxs-lookup"><span data-stu-id="08668-337">áfa</span></span>
  
<span data-ttu-id="08668-338">közösségi adószám</span><span class="sxs-lookup"><span data-stu-id="08668-338">közösségi adószám</span></span>
  
<span data-ttu-id="08668-339">általános forgalmi adó szám</span><span class="sxs-lookup"><span data-stu-id="08668-339">általános forgalmi adó szám</span></span>
  
<span data-ttu-id="08668-340">hozzáadottérték adó</span><span class="sxs-lookup"><span data-stu-id="08668-340">hozzáadottérték adó</span></span>
  
<span data-ttu-id="08668-341">áfa szám</span><span class="sxs-lookup"><span data-stu-id="08668-341">áfa szám</span></span>
  
<span data-ttu-id="08668-342">Magyar áfa szám</span><span class="sxs-lookup"><span data-stu-id="08668-342">magyar áfa szám</span></span>
  
## <a name="portugal"></a><span data-ttu-id="08668-343">Portugal</span><span class="sxs-lookup"><span data-stu-id="08668-343">Portugal</span></span>

<span data-ttu-id="08668-344">Para obter detalhes, consulte a seção "número de cartão de cidadão da Portugal" em [o que os tipos de informações confidenciais buscam](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="08668-344">For details, see the section "Portugal Citizen Card Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="spain"></a><span data-ttu-id="08668-345">Espanha</span><span class="sxs-lookup"><span data-stu-id="08668-345">Spain</span></span>

<span data-ttu-id="08668-346">Para obter detalhes, consulte a seção "número de seguridade social da Espanha (SSN)" em [o que os tipos de informações confidenciais procuram](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="08668-346">For details, see the section "Spain Social Security Number (SSN)" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="sweden"></a><span data-ttu-id="08668-347">Suécia</span><span class="sxs-lookup"><span data-stu-id="08668-347">Sweden</span></span>

### <a name="format"></a><span data-ttu-id="08668-348">Formatar</span><span class="sxs-lookup"><span data-stu-id="08668-348">Format</span></span>

<span data-ttu-id="08668-349">12 dígitos sem espaços e delimitadores</span><span class="sxs-lookup"><span data-stu-id="08668-349">12 digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="08668-350">Padrão</span><span class="sxs-lookup"><span data-stu-id="08668-350">Pattern</span></span>

<span data-ttu-id="08668-351">12 dígitos:</span><span class="sxs-lookup"><span data-stu-id="08668-351">12 digits:</span></span>
  
-  <span data-ttu-id="08668-352">Oito dígitos que correspondem à data de nascimento (AAAAMMDD)</span><span class="sxs-lookup"><span data-stu-id="08668-352">Eight digits that correspond to the birth date (YYYYMMDD)</span></span> 
    
- <span data-ttu-id="08668-353">Três dígitos que correspondem a um número de série em que:</span><span class="sxs-lookup"><span data-stu-id="08668-353">Three digits that correspond to a serial number where:</span></span> 
    
  - <span data-ttu-id="08668-354">O último dígito no número de série indica sexo pela atribuição de um número ímpar para macho e um número par para o fêmea</span><span class="sxs-lookup"><span data-stu-id="08668-354">The last digit in the serial number indicates gender by the assignment of an odd number for male and an even number for female</span></span>
    
  - <span data-ttu-id="08668-355">Até 1990, a atribuição de número de série correspondente à região onde o portador do número nasceu ou (se nasceu antes de 1947) em que ele/ela estava em vida, de acordo com os registros de impostos, em 1º de janeiro de 1947, com um código especial (geralmente 9 como o sétimo dígito) para immigrants</span><span class="sxs-lookup"><span data-stu-id="08668-355">Up to 1990, the assignment of serial number corresponded to the county where the bearer of the number was born or (if born before 1947) where he/she had been living, according to tax records, on January 1, 1947, with a special code (usually 9 as the 7th digit) for immigrants</span></span> 
    
- <span data-ttu-id="08668-356">Um dígito de verificação</span><span class="sxs-lookup"><span data-stu-id="08668-356">One check digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="08668-357">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="08668-357">Checksum</span></span>

<span data-ttu-id="08668-358">Sim</span><span class="sxs-lookup"><span data-stu-id="08668-358">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="08668-359">Definição</span><span class="sxs-lookup"><span data-stu-id="08668-359">Definition</span></span>

<span data-ttu-id="08668-360">Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="08668-360">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="08668-361">A função `Func_sweden_eu_ssn_or_equivalent` localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="08668-361">The function  `Func_sweden_eu_ssn_or_equivalent` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="08668-362">Uma palavra- `Keywords_sweden_eu_ssn_or_equivalent` chave de foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="08668-362">A keyword from  `Keywords_sweden_eu_ssn_or_equivalent` is found.</span></span> 
    
<span data-ttu-id="08668-363">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="08668-363">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="08668-364">A função `Func_sweden_eu_ssn_or_equivalent` localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="08668-364">The function  `Func_sweden_eu_ssn_or_equivalent` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU SSN or Equivalent Number -->
<Entity id="d24e32a4-c0bb-4ba8-899d-6303b95742d9" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_sweden_eu_ssn_or_equivalent" />
          <Match idRef="Keywords_sweden_eu_ssn_or_equivalent" />
        </Pattern> 
       <Pattern confidenceLevel="75">
          <IdMatch idRef="Func_sweden_eu_ssn_or_equivalent" />
        </Pattern>      
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="08668-365">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="08668-365">Keywords</span></span>

#### <a name="keywordsswedeneussnorequivalent"></a><span data-ttu-id="08668-366">Keywords_sweden_eu_ssn_or_equivalent</span><span class="sxs-lookup"><span data-stu-id="08668-366">Keywords_sweden_eu_ssn_or_equivalent</span></span>

<span data-ttu-id="08668-367">número de identificação pessoal</span><span class="sxs-lookup"><span data-stu-id="08668-367">personal id number</span></span>
  
<span data-ttu-id="08668-368">identification number</span><span class="sxs-lookup"><span data-stu-id="08668-368">identification number</span></span>
  
<span data-ttu-id="08668-369">n º de identificação pessoal</span><span class="sxs-lookup"><span data-stu-id="08668-369">personal id no</span></span>
  
<span data-ttu-id="08668-370">identidade não</span><span class="sxs-lookup"><span data-stu-id="08668-370">identity no</span></span>
  
<span data-ttu-id="08668-371">identificação não</span><span class="sxs-lookup"><span data-stu-id="08668-371">identification no</span></span>
  
<span data-ttu-id="08668-372">identificação pessoal não</span><span class="sxs-lookup"><span data-stu-id="08668-372">personal identification no</span></span>
  
<span data-ttu-id="08668-373">ID personnummer</span><span class="sxs-lookup"><span data-stu-id="08668-373">personnummer id</span></span>
  
<span data-ttu-id="08668-374">ID Personligt-Nummer</span><span class="sxs-lookup"><span data-stu-id="08668-374">personligt id-nummer</span></span>
  
<span data-ttu-id="08668-375">ID unikt-Nummer</span><span class="sxs-lookup"><span data-stu-id="08668-375">unikt id-nummer</span></span>
  
<span data-ttu-id="08668-376">personnummer</span><span class="sxs-lookup"><span data-stu-id="08668-376">personnummer</span></span>
  
<span data-ttu-id="08668-377">identifikationsnumret</span><span class="sxs-lookup"><span data-stu-id="08668-377">identifikationsnumret</span></span>
  
<span data-ttu-id="08668-378">personnummer #</span><span class="sxs-lookup"><span data-stu-id="08668-378">personnummer#</span></span>
  
<span data-ttu-id="08668-379">identifikationsnumret #</span><span class="sxs-lookup"><span data-stu-id="08668-379">identifikationsnumret#</span></span>
  
## <a name="see-also"></a><span data-ttu-id="08668-380">Confira também</span><span class="sxs-lookup"><span data-stu-id="08668-380">See also</span></span>

[<span data-ttu-id="08668-381">O que os tipos de informações confidenciais procuram</span><span class="sxs-lookup"><span data-stu-id="08668-381">What the sensitive information types look for</span></span>](what-the-sensitive-information-types-look-for.md)

