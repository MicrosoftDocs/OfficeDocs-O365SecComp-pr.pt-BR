---
title: Número de seguro social da UE ou ID equivalente
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: 8/17/2018
audience: Admin
ms.topic: reference
ms.service: O365-seccomp
ms.collection: M365-security-compliance
localization_priority: Normal
description: Este tópico mostra o que uma política de prevenção de perda de dados (DLP) procura quando detecta o número de segurança social da UE ou o tipo de informação confidencial de ID equivalente. Esse tipo de informação confidencial define diferentes padrões, palavras-chave e outras evidências para cada país.
ms.openlocfilehash: b42a8d927e18f813eb6ef6d1d55b2de15ea9dcd5
ms.sourcegitcommit: 9d67cb52544321a430343d39eb336112c1a11d35
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/17/2019
ms.locfileid: "34154483"
---
# <a name="eu-social-security-number-or-equivalent-id"></a><span data-ttu-id="b05b0-104">Número de seguro social da UE ou ID equivalente</span><span class="sxs-lookup"><span data-stu-id="b05b0-104">EU Social Security Number or Equivalent ID</span></span>

<span data-ttu-id="b05b0-105">Este tópico mostra o que uma política de prevenção de perda de dados (DLP) procura quando detecta o número de segurança social da UE (SSN) ou o tipo de informação confidencial de ID equivalente.</span><span class="sxs-lookup"><span data-stu-id="b05b0-105">This topic shows what a data loss prevention (DLP) policy looks for when it detects the EU Social Security Number (SSN) or Equivalent ID sensitive information type.</span></span> <span data-ttu-id="b05b0-106">Esse tipo de informação confidencial define diferentes padrões, palavras-chave e outras evidências para cada país.</span><span class="sxs-lookup"><span data-stu-id="b05b0-106">This sensitive information type defines different patterns, keywords, and other evidence for each country.</span></span>
  
## <a name="austria"></a><span data-ttu-id="b05b0-107">Áustria </span><span class="sxs-lookup"><span data-stu-id="b05b0-107">Austria</span></span>

### <a name="format"></a><span data-ttu-id="b05b0-108">Formatar</span><span class="sxs-lookup"><span data-stu-id="b05b0-108">Format</span></span>

<span data-ttu-id="b05b0-109">10 dígitos no formato especificado</span><span class="sxs-lookup"><span data-stu-id="b05b0-109">10 digits in the specified format</span></span>
  
### <a name="pattern"></a><span data-ttu-id="b05b0-110">Padrão</span><span class="sxs-lookup"><span data-stu-id="b05b0-110">Pattern</span></span>

<span data-ttu-id="b05b0-111">10 dígitos:</span><span class="sxs-lookup"><span data-stu-id="b05b0-111">10 digits:</span></span>
  
-  <span data-ttu-id="b05b0-112">Três dígitos que correspondem a um número de série</span><span class="sxs-lookup"><span data-stu-id="b05b0-112">Three digits that correspond to a serial number</span></span> 
    
- <span data-ttu-id="b05b0-113">Um dígito de verificação</span><span class="sxs-lookup"><span data-stu-id="b05b0-113">One check digit</span></span>
    
- <span data-ttu-id="b05b0-114">Seis dígitos que correspondem à data de nascimento (DDMMAA)</span><span class="sxs-lookup"><span data-stu-id="b05b0-114">Six digits that correspond to the birth date (DDMMYY)</span></span>
    
### <a name="checksum"></a><span data-ttu-id="b05b0-115">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="b05b0-115">Checksum</span></span>

<span data-ttu-id="b05b0-116">Sim</span><span class="sxs-lookup"><span data-stu-id="b05b0-116">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="b05b0-117">Definição</span><span class="sxs-lookup"><span data-stu-id="b05b0-117">Definition</span></span>

<span data-ttu-id="b05b0-118">Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="b05b0-118">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="b05b0-119">A função `Func_austria_eu_ssn_or_equivalent` localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="b05b0-119">The function  `Func_austria_eu_ssn_or_equivalent` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="b05b0-120">Uma palavra- `Keywords_austria_eu_ssn_or_equivalent` chave de foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="b05b0-120">A keyword from  `Keywords_austria_eu_ssn_or_equivalent` is found.</span></span> 
    
<span data-ttu-id="b05b0-121">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="b05b0-121">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="b05b0-122">A função `Func_austria_eu_ssn_or_equivalent` localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="b05b0-122">The function  `Func_austria_eu_ssn_or_equivalent` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="b05b0-123">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="b05b0-123">Keywords</span></span>

#### <a name="keywordsaustriaeussnorequivalent"></a><span data-ttu-id="b05b0-124">Keywords_austria_eu_ssn_or_equivalent</span><span class="sxs-lookup"><span data-stu-id="b05b0-124">Keywords_austria_eu_ssn_or_equivalent</span></span>

<span data-ttu-id="b05b0-125">segurança social não</span><span class="sxs-lookup"><span data-stu-id="b05b0-125">social security no</span></span>
  
<span data-ttu-id="b05b0-126">social security number</span><span class="sxs-lookup"><span data-stu-id="b05b0-126">social security number</span></span>
  
<span data-ttu-id="b05b0-127">social security code</span><span class="sxs-lookup"><span data-stu-id="b05b0-127">social security code</span></span>
  
<span data-ttu-id="b05b0-128">número de seguro</span><span class="sxs-lookup"><span data-stu-id="b05b0-128">insurance number</span></span>
  
<span data-ttu-id="b05b0-129">SSN austríaco</span><span class="sxs-lookup"><span data-stu-id="b05b0-129">austrian ssn</span></span>
  
<span data-ttu-id="b05b0-130">es</span><span class="sxs-lookup"><span data-stu-id="b05b0-130">ssn#</span></span>
  
<span data-ttu-id="b05b0-131">es</span><span class="sxs-lookup"><span data-stu-id="b05b0-131">ssn</span></span>
  
<span data-ttu-id="b05b0-132">código de seguro</span><span class="sxs-lookup"><span data-stu-id="b05b0-132">insurance code</span></span>
  
<span data-ttu-id="b05b0-133">código de seguro #</span><span class="sxs-lookup"><span data-stu-id="b05b0-133">insurance code#</span></span>
  
<span data-ttu-id="b05b0-134">socialsecurityno#</span><span class="sxs-lookup"><span data-stu-id="b05b0-134">socialsecurityno#</span></span>
  
<span data-ttu-id="b05b0-135">sozialversicherungsnummer</span><span class="sxs-lookup"><span data-stu-id="b05b0-135">sozialversicherungsnummer</span></span>
  
<span data-ttu-id="b05b0-136">soziale sicherheit kein</span><span class="sxs-lookup"><span data-stu-id="b05b0-136">soziale sicherheit kein</span></span>
  
<span data-ttu-id="b05b0-137">versicherungsnummer</span><span class="sxs-lookup"><span data-stu-id="b05b0-137">versicherungsnummer</span></span>
  
## <a name="belgium"></a><span data-ttu-id="b05b0-138">Bélgica </span><span class="sxs-lookup"><span data-stu-id="b05b0-138">Belgium</span></span>

### <a name="format"></a><span data-ttu-id="b05b0-139">Formatar</span><span class="sxs-lookup"><span data-stu-id="b05b0-139">Format</span></span>

<span data-ttu-id="b05b0-140">11 dígitos sem espaços ou delimitadores</span><span class="sxs-lookup"><span data-stu-id="b05b0-140">11 digits without spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="b05b0-141">Padrão</span><span class="sxs-lookup"><span data-stu-id="b05b0-141">Pattern</span></span>

<span data-ttu-id="b05b0-142">11 dígitos</span><span class="sxs-lookup"><span data-stu-id="b05b0-142">11 digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="b05b0-143">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="b05b0-143">Checksum</span></span>

<span data-ttu-id="b05b0-144">Sim</span><span class="sxs-lookup"><span data-stu-id="b05b0-144">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="b05b0-145">Definição</span><span class="sxs-lookup"><span data-stu-id="b05b0-145">Definition</span></span>

<span data-ttu-id="b05b0-146">Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="b05b0-146">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="b05b0-147">A função `Func_belgium_eu_ssn_or_equivalent` localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="b05b0-147">The function  `Func_belgium_eu_ssn_or_equivalent` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="b05b0-148">Uma palavra- `Keywords_belgium_eu_ssn_or_equivalent` chave de foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="b05b0-148">A keyword from  `Keywords_belgium_eu_ssn_or_equivalent` is found.</span></span> 
    
<span data-ttu-id="b05b0-149">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="b05b0-149">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="b05b0-150">A função `Func_belgium_eu_ssn_or_equivalent` localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="b05b0-150">The function  `Func_belgium_eu_ssn_or_equivalent` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="b05b0-151">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="b05b0-151">Keywords</span></span>

#### <a name="keywordsbelgiumeussnorequivalent"></a><span data-ttu-id="b05b0-152">Keywords_belgium_eu_ssn_or_equivalent</span><span class="sxs-lookup"><span data-stu-id="b05b0-152">Keywords_belgium_eu_ssn_or_equivalent</span></span>

<span data-ttu-id="b05b0-153">número Nacional belga</span><span class="sxs-lookup"><span data-stu-id="b05b0-153">belgian national number</span></span>
  
<span data-ttu-id="b05b0-154">número nacional</span><span class="sxs-lookup"><span data-stu-id="b05b0-154">national number</span></span>
  
<span data-ttu-id="b05b0-155">social security number</span><span class="sxs-lookup"><span data-stu-id="b05b0-155">social security number</span></span>
  
<span data-ttu-id="b05b0-156">nationalnumber#</span><span class="sxs-lookup"><span data-stu-id="b05b0-156">nationalnumber#</span></span>
  
<span data-ttu-id="b05b0-157">es</span><span class="sxs-lookup"><span data-stu-id="b05b0-157">ssn#</span></span>
  
<span data-ttu-id="b05b0-158">es</span><span class="sxs-lookup"><span data-stu-id="b05b0-158">ssn</span></span>
  
<span data-ttu-id="b05b0-159">nationalnumber</span><span class="sxs-lookup"><span data-stu-id="b05b0-159">nationalnumber</span></span>
  
<span data-ttu-id="b05b0-160">bnn#</span><span class="sxs-lookup"><span data-stu-id="b05b0-160">bnn#</span></span>
  
<span data-ttu-id="b05b0-161">bnn</span><span class="sxs-lookup"><span data-stu-id="b05b0-161">bnn</span></span>
  
<span data-ttu-id="b05b0-162">número de identificação pessoal</span><span class="sxs-lookup"><span data-stu-id="b05b0-162">personal id number</span></span>
  
<span data-ttu-id="b05b0-163">personalidnumber#</span><span class="sxs-lookup"><span data-stu-id="b05b0-163">personalidnumber#</span></span>
  
<span data-ttu-id="b05b0-164">nacional Numéro</span><span class="sxs-lookup"><span data-stu-id="b05b0-164">numéro national</span></span>
  
<span data-ttu-id="b05b0-165">numéro de sécurité</span><span class="sxs-lookup"><span data-stu-id="b05b0-165">numéro de sécurité</span></span>
  
<span data-ttu-id="b05b0-166">numéro d'assuré</span><span class="sxs-lookup"><span data-stu-id="b05b0-166">numéro d'assuré</span></span>
  
<span data-ttu-id="b05b0-167">nacional de identificação</span><span class="sxs-lookup"><span data-stu-id="b05b0-167">identifiant national</span></span>
  
<span data-ttu-id="b05b0-168">identifiantnational#</span><span class="sxs-lookup"><span data-stu-id="b05b0-168">identifiantnational#</span></span>
  
<span data-ttu-id="b05b0-169">numéronational#</span><span class="sxs-lookup"><span data-stu-id="b05b0-169">numéronational#</span></span>
  
## <a name="croatia"></a><span data-ttu-id="b05b0-170">Croácia</span><span class="sxs-lookup"><span data-stu-id="b05b0-170">Croatia</span></span>

### <a name="format"></a><span data-ttu-id="b05b0-171">Formatar</span><span class="sxs-lookup"><span data-stu-id="b05b0-171">Format</span></span>

<span data-ttu-id="b05b0-172">11 dígitos sem espaços e delimitadores</span><span class="sxs-lookup"><span data-stu-id="b05b0-172">11 digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="b05b0-173">Padrão</span><span class="sxs-lookup"><span data-stu-id="b05b0-173">Pattern</span></span>

 <span data-ttu-id="b05b0-174">11 dígitos:</span><span class="sxs-lookup"><span data-stu-id="b05b0-174">11 digits:</span></span> 
  
-  <span data-ttu-id="b05b0-175">Dez dígitos</span><span class="sxs-lookup"><span data-stu-id="b05b0-175">Ten digits</span></span> 
    
- <span data-ttu-id="b05b0-176">Um dígito de verificação</span><span class="sxs-lookup"><span data-stu-id="b05b0-176">One check digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="b05b0-177">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="b05b0-177">Checksum</span></span>

<span data-ttu-id="b05b0-178">Sim</span><span class="sxs-lookup"><span data-stu-id="b05b0-178">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="b05b0-179">Definição</span><span class="sxs-lookup"><span data-stu-id="b05b0-179">Definition</span></span>

<span data-ttu-id="b05b0-180">Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="b05b0-180">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="b05b0-181">A função `Func_croatia_eu_ssn_or_equivalent` localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="b05b0-181">The function  `Func_croatia_eu_ssn_or_equivalent` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="b05b0-182">Uma palavra- `Keywords_croatia_eu_ssn_or_equivalent` chave de foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="b05b0-182">A keyword from  `Keywords_croatia_eu_ssn_or_equivalent` is found.</span></span> 
    
<span data-ttu-id="b05b0-183">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="b05b0-183">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="b05b0-184">A função `Func_croatia_eu_ssn_or_equivalent` localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="b05b0-184">The function  `Func_croatia_eu_ssn_or_equivalent` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="b05b0-185">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="b05b0-185">Keywords</span></span>

#### <a name="keywordscroatiaeussnorequivalent"></a><span data-ttu-id="b05b0-186">Keywords_croatia_eu_ssn_or_equivalent</span><span class="sxs-lookup"><span data-stu-id="b05b0-186">Keywords_croatia_eu_ssn_or_equivalent</span></span>

<span data-ttu-id="b05b0-187">número de identificação pessoal</span><span class="sxs-lookup"><span data-stu-id="b05b0-187">personal identification number</span></span>
  
<span data-ttu-id="b05b0-188">número do cidadão mestre</span><span class="sxs-lookup"><span data-stu-id="b05b0-188">master citizen number</span></span>
  
<span data-ttu-id="b05b0-189">national identification number</span><span class="sxs-lookup"><span data-stu-id="b05b0-189">national identification number</span></span>
  
<span data-ttu-id="b05b0-190">social security number</span><span class="sxs-lookup"><span data-stu-id="b05b0-190">social security number</span></span>
  
<span data-ttu-id="b05b0-191">nationalnumber#</span><span class="sxs-lookup"><span data-stu-id="b05b0-191">nationalnumber#</span></span>
  
<span data-ttu-id="b05b0-192">es</span><span class="sxs-lookup"><span data-stu-id="b05b0-192">ssn#</span></span>
  
<span data-ttu-id="b05b0-193">es</span><span class="sxs-lookup"><span data-stu-id="b05b0-193">ssn</span></span>
  
<span data-ttu-id="b05b0-194">nationalnumber</span><span class="sxs-lookup"><span data-stu-id="b05b0-194">nationalnumber</span></span>
  
<span data-ttu-id="b05b0-195">bnn#</span><span class="sxs-lookup"><span data-stu-id="b05b0-195">bnn#</span></span>
  
<span data-ttu-id="b05b0-196">bnn</span><span class="sxs-lookup"><span data-stu-id="b05b0-196">bnn</span></span>
  
<span data-ttu-id="b05b0-197">número de identificação pessoal</span><span class="sxs-lookup"><span data-stu-id="b05b0-197">personal id number</span></span>
  
<span data-ttu-id="b05b0-198">personalidnumber#</span><span class="sxs-lookup"><span data-stu-id="b05b0-198">personalidnumber#</span></span>
  
<span data-ttu-id="b05b0-199">NIB</span><span class="sxs-lookup"><span data-stu-id="b05b0-199">oib</span></span>
  
<span data-ttu-id="b05b0-200">osobni identifikacijski broj</span><span class="sxs-lookup"><span data-stu-id="b05b0-200">osobni identifikacijski broj</span></span>
  
## <a name="czech-republic"></a><span data-ttu-id="b05b0-201">República Tcheca</span><span class="sxs-lookup"><span data-stu-id="b05b0-201">Czech Republic</span></span>

### <a name="format"></a><span data-ttu-id="b05b0-202">Formatar</span><span class="sxs-lookup"><span data-stu-id="b05b0-202">Format</span></span>

<span data-ttu-id="b05b0-203">Dez dígitos e uma barra invertida no padrão especificado</span><span class="sxs-lookup"><span data-stu-id="b05b0-203">Ten digits and a backslash in the specified pattern</span></span>
  
### <a name="pattern"></a><span data-ttu-id="b05b0-204">Padrão</span><span class="sxs-lookup"><span data-stu-id="b05b0-204">Pattern</span></span>

<span data-ttu-id="b05b0-205">Dez dígitos e uma barra invertida:</span><span class="sxs-lookup"><span data-stu-id="b05b0-205">Ten digits and a backslash:</span></span>
  
- <span data-ttu-id="b05b0-206">Seis dígitos que correspondem à data de nascimento (AAMMDD):</span><span class="sxs-lookup"><span data-stu-id="b05b0-206">Six digits that correspond to the birth date (YYMMDD):</span></span> 
    
- <span data-ttu-id="b05b0-207">Uma barra invertida</span><span class="sxs-lookup"><span data-stu-id="b05b0-207">A backslash</span></span>
    
- <span data-ttu-id="b05b0-208">Três dígitos que correspondem a um número de série que separa as pessoas nasceu na mesma data</span><span class="sxs-lookup"><span data-stu-id="b05b0-208">Three digits that correspond to a serial number that separates persons born on the same date</span></span>
    
- <span data-ttu-id="b05b0-209">Um dígito de verificação</span><span class="sxs-lookup"><span data-stu-id="b05b0-209">One check digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="b05b0-210">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="b05b0-210">Checksum</span></span>

<span data-ttu-id="b05b0-211">Sim</span><span class="sxs-lookup"><span data-stu-id="b05b0-211">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="b05b0-212">Definição</span><span class="sxs-lookup"><span data-stu-id="b05b0-212">Definition</span></span>

<span data-ttu-id="b05b0-213">Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="b05b0-213">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="b05b0-214">A função `Func_czech_republic_eu_ssn_or_equivalent` localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="b05b0-214">The function  `Func_czech_republic_eu_ssn_or_equivalent` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="b05b0-215">Uma palavra- `Keywords_czech_republic_eu_ssn_or_equivalent` chave de foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="b05b0-215">A keyword from  `Keywords_czech_republic_eu_ssn_or_equivalent` is found.</span></span> 
    
<span data-ttu-id="b05b0-216">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="b05b0-216">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="b05b0-217">A função `Func_czech_republic_eu_ssn_or_equivalent` localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="b05b0-217">The function  `Func_czech_republic_eu_ssn_or_equivalent` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="b05b0-218">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="b05b0-218">Keywords</span></span>

#### <a name="keywordsczechrepubliceussnorequivalent"></a><span data-ttu-id="b05b0-219">Keywords_czech_republic_eu_ssn_or_equivalent</span><span class="sxs-lookup"><span data-stu-id="b05b0-219">Keywords_czech_republic_eu_ssn_or_equivalent</span></span>

<span data-ttu-id="b05b0-220">número de nascimento</span><span class="sxs-lookup"><span data-stu-id="b05b0-220">birth number</span></span>
  
<span data-ttu-id="b05b0-221">national identification number</span><span class="sxs-lookup"><span data-stu-id="b05b0-221">national identification number</span></span>
  
<span data-ttu-id="b05b0-222">número de identificação pessoal</span><span class="sxs-lookup"><span data-stu-id="b05b0-222">personal identification number</span></span>
  
<span data-ttu-id="b05b0-223">social security number</span><span class="sxs-lookup"><span data-stu-id="b05b0-223">social security number</span></span>
  
<span data-ttu-id="b05b0-224">nationalnumber#</span><span class="sxs-lookup"><span data-stu-id="b05b0-224">nationalnumber#</span></span>
  
<span data-ttu-id="b05b0-225">es</span><span class="sxs-lookup"><span data-stu-id="b05b0-225">ssn#</span></span>
  
<span data-ttu-id="b05b0-226">es</span><span class="sxs-lookup"><span data-stu-id="b05b0-226">ssn</span></span>
  
<span data-ttu-id="b05b0-227">número nacional</span><span class="sxs-lookup"><span data-stu-id="b05b0-227">national number</span></span>
  
<span data-ttu-id="b05b0-228">número de identificação pessoal</span><span class="sxs-lookup"><span data-stu-id="b05b0-228">personal id number</span></span>
  
<span data-ttu-id="b05b0-229">personalidnumber#</span><span class="sxs-lookup"><span data-stu-id="b05b0-229">personalidnumber#</span></span>
  
<span data-ttu-id="b05b0-230">rč</span><span class="sxs-lookup"><span data-stu-id="b05b0-230">rč</span></span>
  
<span data-ttu-id="b05b0-231">rodné číslo</span><span class="sxs-lookup"><span data-stu-id="b05b0-231">rodné číslo</span></span>
  
<span data-ttu-id="b05b0-232">rodne cislo</span><span class="sxs-lookup"><span data-stu-id="b05b0-232">rodne cislo</span></span>
  
## <a name="denmark"></a><span data-ttu-id="b05b0-233">Dinamarca</span><span class="sxs-lookup"><span data-stu-id="b05b0-233">Denmark</span></span>

### <a name="format"></a><span data-ttu-id="b05b0-234">Formatar</span><span class="sxs-lookup"><span data-stu-id="b05b0-234">Format</span></span>

<span data-ttu-id="b05b0-235">Dez dígitos e um hífen no padrão especificado</span><span class="sxs-lookup"><span data-stu-id="b05b0-235">Ten digits and a hyphen in the specified pattern</span></span>
  
### <a name="pattern"></a><span data-ttu-id="b05b0-236">Padrão</span><span class="sxs-lookup"><span data-stu-id="b05b0-236">Pattern</span></span>

<span data-ttu-id="b05b0-237">Dez dígitos e um hífen:</span><span class="sxs-lookup"><span data-stu-id="b05b0-237">Ten digits and a hyphen:</span></span>
  
- <span data-ttu-id="b05b0-238">Seis dígitos que correspondem à data de nascimento (DDMMAA)</span><span class="sxs-lookup"><span data-stu-id="b05b0-238">Six digits that correspond to the birth date (DDMMYY)</span></span> 
    
- <span data-ttu-id="b05b0-239">Um hífen</span><span class="sxs-lookup"><span data-stu-id="b05b0-239">A hyphen</span></span>
    
- <span data-ttu-id="b05b0-240">Quatro dígitos que correspondem a um número de sequência</span><span class="sxs-lookup"><span data-stu-id="b05b0-240">Four digits that correspond to a sequence number</span></span>
    
### <a name="checksum"></a><span data-ttu-id="b05b0-241">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="b05b0-241">Checksum</span></span>

<span data-ttu-id="b05b0-242">Sim</span><span class="sxs-lookup"><span data-stu-id="b05b0-242">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="b05b0-243">Definição</span><span class="sxs-lookup"><span data-stu-id="b05b0-243">Definition</span></span>

<span data-ttu-id="b05b0-244">Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="b05b0-244">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="b05b0-245">A função `Func_denmark_eu_ssn_or_equivalent` localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="b05b0-245">The function  `Func_denmark_eu_ssn_or_equivalent` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="b05b0-246">Uma palavra- `Keywords_denmark_eu_ssn_or_equivalent` chave de foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="b05b0-246">A keyword from  `Keywords_denmark_eu_ssn_or_equivalent` is found.</span></span> 
    
<span data-ttu-id="b05b0-247">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="b05b0-247">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="b05b0-248">A função `Func_denmark_eu_ssn_or_equivalent` localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="b05b0-248">The function  `Func_denmark_eu_ssn_or_equivalent` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="b05b0-249">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="b05b0-249">Keywords</span></span>

#### <a name="keywordsdenmarkeussnorequivalent"></a><span data-ttu-id="b05b0-250">Keywords_denmark_eu_ssn_or_equivalent</span><span class="sxs-lookup"><span data-stu-id="b05b0-250">Keywords_denmark_eu_ssn_or_equivalent</span></span>

<span data-ttu-id="b05b0-251">número de identificação pessoal</span><span class="sxs-lookup"><span data-stu-id="b05b0-251">personal identification number</span></span>
  
<span data-ttu-id="b05b0-252">national identification number</span><span class="sxs-lookup"><span data-stu-id="b05b0-252">national identification number</span></span>
  
<span data-ttu-id="b05b0-253">social security number</span><span class="sxs-lookup"><span data-stu-id="b05b0-253">social security number</span></span>
  
<span data-ttu-id="b05b0-254">nationalnumber#</span><span class="sxs-lookup"><span data-stu-id="b05b0-254">nationalnumber#</span></span>
  
<span data-ttu-id="b05b0-255">es</span><span class="sxs-lookup"><span data-stu-id="b05b0-255">ssn#</span></span>
  
<span data-ttu-id="b05b0-256">es</span><span class="sxs-lookup"><span data-stu-id="b05b0-256">ssn</span></span>
  
<span data-ttu-id="b05b0-257">número nacional</span><span class="sxs-lookup"><span data-stu-id="b05b0-257">national number</span></span>
  
<span data-ttu-id="b05b0-258">número de identificação pessoal</span><span class="sxs-lookup"><span data-stu-id="b05b0-258">personal id number</span></span>
  
<span data-ttu-id="b05b0-259">personalidnumber#</span><span class="sxs-lookup"><span data-stu-id="b05b0-259">personalidnumber#</span></span>
  
<span data-ttu-id="b05b0-260">CPR-Nummer</span><span class="sxs-lookup"><span data-stu-id="b05b0-260">cpr-nummer</span></span>
  
<span data-ttu-id="b05b0-261">personnummer</span><span class="sxs-lookup"><span data-stu-id="b05b0-261">personnummer</span></span>
  
## <a name="finland"></a><span data-ttu-id="b05b0-262">Finlândia</span><span class="sxs-lookup"><span data-stu-id="b05b0-262">Finland</span></span>

### <a name="format"></a><span data-ttu-id="b05b0-263">Formatar</span><span class="sxs-lookup"><span data-stu-id="b05b0-263">Format</span></span>

<span data-ttu-id="b05b0-264">Uma combinação de 11 caracteres no formato especificado</span><span class="sxs-lookup"><span data-stu-id="b05b0-264">An 11-character combination in the specified format</span></span>
  
### <a name="pattern"></a><span data-ttu-id="b05b0-265">Padrão</span><span class="sxs-lookup"><span data-stu-id="b05b0-265">Pattern</span></span>

<span data-ttu-id="b05b0-266">Uma combinação de 11 caracteres no formato especificado:</span><span class="sxs-lookup"><span data-stu-id="b05b0-266">An 11-character combination in the specified format:</span></span>
  
-  <span data-ttu-id="b05b0-267">Seis dígitos</span><span class="sxs-lookup"><span data-stu-id="b05b0-267">Six digits</span></span> 
    
- <span data-ttu-id="b05b0-268">Uma instância de um dos seguintes:</span><span class="sxs-lookup"><span data-stu-id="b05b0-268">One instance of one of the following:</span></span>
    
  - <span data-ttu-id="b05b0-269">Símbolo de adição</span><span class="sxs-lookup"><span data-stu-id="b05b0-269">Plus symbol</span></span>
    
  - <span data-ttu-id="b05b0-270">Símbolo de subtração</span><span class="sxs-lookup"><span data-stu-id="b05b0-270">Minus symbol</span></span>
    
  - <span data-ttu-id="b05b0-271">A letra "A" (não diferencia maiúsculas de minúsculas)</span><span class="sxs-lookup"><span data-stu-id="b05b0-271">The letter "A" (not case-sensitive)</span></span>
    
- <span data-ttu-id="b05b0-272">Três dígitos</span><span class="sxs-lookup"><span data-stu-id="b05b0-272">Three digits</span></span>
    
- <span data-ttu-id="b05b0-273">Uma letra ou um dígito</span><span class="sxs-lookup"><span data-stu-id="b05b0-273">One letter or one digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="b05b0-274">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="b05b0-274">Checksum</span></span>

<span data-ttu-id="b05b0-275">Sim</span><span class="sxs-lookup"><span data-stu-id="b05b0-275">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="b05b0-276">Definição</span><span class="sxs-lookup"><span data-stu-id="b05b0-276">Definition</span></span>

<span data-ttu-id="b05b0-277">Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="b05b0-277">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="b05b0-278">A função `Func_finland_eu_ssn_or_equivalent` localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="b05b0-278">The function  `Func_finland_eu_ssn_or_equivalent` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="b05b0-279">Uma palavra- `Keywords_finland_eu_ssn_or_equivalent` chave de foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="b05b0-279">A keyword from  `Keywords_finland_eu_ssn_or_equivalent` is found.</span></span> 
    
<span data-ttu-id="b05b0-280">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="b05b0-280">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="b05b0-281">A função `Func_finland_eu_ssn_or_equivalent` localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="b05b0-281">The function  `Func_finland_eu_ssn_or_equivalent` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="b05b0-282">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="b05b0-282">Keywords</span></span>

#### <a name="keywordsfinlandeussnorequivalent"></a><span data-ttu-id="b05b0-283">Keywords_finland_eu_ssn_or_equivalent</span><span class="sxs-lookup"><span data-stu-id="b05b0-283">Keywords_finland_eu_ssn_or_equivalent</span></span>

<span data-ttu-id="b05b0-284">identification number</span><span class="sxs-lookup"><span data-stu-id="b05b0-284">identification number</span></span>
  
<span data-ttu-id="b05b0-285">ID pessoal</span><span class="sxs-lookup"><span data-stu-id="b05b0-285">personal id</span></span>
  
<span data-ttu-id="b05b0-286">número de identidade</span><span class="sxs-lookup"><span data-stu-id="b05b0-286">identity number</span></span>
  
<span data-ttu-id="b05b0-287">número de ID nacional da finlandês</span><span class="sxs-lookup"><span data-stu-id="b05b0-287">finnish national id number</span></span>
  
<span data-ttu-id="b05b0-288">personalidnumber#</span><span class="sxs-lookup"><span data-stu-id="b05b0-288">personalidnumber#</span></span>
  
<span data-ttu-id="b05b0-289">national identification number</span><span class="sxs-lookup"><span data-stu-id="b05b0-289">national identification number</span></span>
  
<span data-ttu-id="b05b0-290">número de identificação</span><span class="sxs-lookup"><span data-stu-id="b05b0-290">id number</span></span>
  
<span data-ttu-id="b05b0-291">n º de ID nacional</span><span class="sxs-lookup"><span data-stu-id="b05b0-291">national id no.</span></span>
  
<span data-ttu-id="b05b0-292">número de ID nacional</span><span class="sxs-lookup"><span data-stu-id="b05b0-292">national id number</span></span>
  
<span data-ttu-id="b05b0-293">ID não</span><span class="sxs-lookup"><span data-stu-id="b05b0-293">id no</span></span>
  
<span data-ttu-id="b05b0-294">tunnistenumero</span><span class="sxs-lookup"><span data-stu-id="b05b0-294">tunnistenumero</span></span>
  
<span data-ttu-id="b05b0-295">henkilötunnus</span><span class="sxs-lookup"><span data-stu-id="b05b0-295">henkilötunnus</span></span>
  
<span data-ttu-id="b05b0-296">yksilöllinen henkilökohtainen tunnistenumero</span><span class="sxs-lookup"><span data-stu-id="b05b0-296">yksilöllinen henkilökohtainen tunnistenumero</span></span>
  
<span data-ttu-id="b05b0-297">ainutlaatuinen henkilökohtainen tunnus</span><span class="sxs-lookup"><span data-stu-id="b05b0-297">ainutlaatuinen henkilökohtainen tunnus</span></span>
  
<span data-ttu-id="b05b0-298">identiteetti numero</span><span class="sxs-lookup"><span data-stu-id="b05b0-298">identiteetti numero</span></span>
  
<span data-ttu-id="b05b0-299">suomen kansallinen henkilötunnus</span><span class="sxs-lookup"><span data-stu-id="b05b0-299">suomen kansallinen henkilötunnus</span></span>
  
<span data-ttu-id="b05b0-300">henkilötunnusnumero#</span><span class="sxs-lookup"><span data-stu-id="b05b0-300">henkilötunnusnumero#</span></span>
  
<span data-ttu-id="b05b0-301">kansallisen tunnistenumero</span><span class="sxs-lookup"><span data-stu-id="b05b0-301">kansallisen tunnistenumero</span></span>
  
<span data-ttu-id="b05b0-302">tunnusnumero</span><span class="sxs-lookup"><span data-stu-id="b05b0-302">tunnusnumero</span></span>
  
<span data-ttu-id="b05b0-303">kansallinen tunnus numero</span><span class="sxs-lookup"><span data-stu-id="b05b0-303">kansallinen tunnus numero</span></span>
  
<span data-ttu-id="b05b0-304">hetu</span><span class="sxs-lookup"><span data-stu-id="b05b0-304">hetu</span></span>
  
## <a name="france"></a><span data-ttu-id="b05b0-305">França</span><span class="sxs-lookup"><span data-stu-id="b05b0-305">France</span></span>

<span data-ttu-id="b05b0-306">Para obter detalhes, consulte a seção "França Social Security Number (INSEE)" em [o que os tipos de informações confidenciais procuram](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="b05b0-306">For details, see the section "France Social Security Number (INSEE)" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="germany"></a><span data-ttu-id="b05b0-307">Alemanha</span><span class="sxs-lookup"><span data-stu-id="b05b0-307">Germany</span></span>

<span data-ttu-id="b05b0-308">Para obter detalhes, consulte a seção "número do cartão de identidade da Alemanha" em [o que os tipos de informações confidenciais buscam](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="b05b0-308">For details, see the section "Germany Identity Card Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="greece"></a><span data-ttu-id="b05b0-309">Grécia</span><span class="sxs-lookup"><span data-stu-id="b05b0-309">Greece</span></span>

<span data-ttu-id="b05b0-310">Para obter detalhes, consulte a seção "cartão de ID nacional da Grécia" em [que os tipos de informações confidenciais buscam](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="b05b0-310">For details, see the section "Greece National ID Card" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="hungary"></a><span data-ttu-id="b05b0-311">Hungria</span><span class="sxs-lookup"><span data-stu-id="b05b0-311">Hungary</span></span>

### <a name="format"></a><span data-ttu-id="b05b0-312">Formatar</span><span class="sxs-lookup"><span data-stu-id="b05b0-312">Format</span></span>

<span data-ttu-id="b05b0-313">Nove dígitos sem espaços e delimitadores</span><span class="sxs-lookup"><span data-stu-id="b05b0-313">Nine digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="b05b0-314">Padrão</span><span class="sxs-lookup"><span data-stu-id="b05b0-314">Pattern</span></span>

<span data-ttu-id="b05b0-315">Nove dígitos</span><span class="sxs-lookup"><span data-stu-id="b05b0-315">Nine digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="b05b0-316">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="b05b0-316">Checksum</span></span>

<span data-ttu-id="b05b0-317">Sim</span><span class="sxs-lookup"><span data-stu-id="b05b0-317">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="b05b0-318">Definição</span><span class="sxs-lookup"><span data-stu-id="b05b0-318">Definition</span></span>

<span data-ttu-id="b05b0-319">Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="b05b0-319">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="b05b0-320">A função `Func_hungary_eu_ssn_or_equivalent` localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="b05b0-320">The function  `Func_hungary_eu_ssn_or_equivalent` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="b05b0-321">Uma palavra- `Keywords_hungary_eu_ssn_or_equivalent` chave de foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="b05b0-321">A keyword from  `Keywords_hungary_eu_ssn_or_equivalent` is found.</span></span> 
    
<span data-ttu-id="b05b0-322">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="b05b0-322">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="b05b0-323">A função `Func_hungary_eu_ssn_or_equivalent` localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="b05b0-323">The function  `Func_hungary_eu_ssn_or_equivalent` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="b05b0-324">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="b05b0-324">Keywords</span></span>

#### <a name="keywordshungaryeussnorequivalent"></a><span data-ttu-id="b05b0-325">Keywords_hungary_eu_ssn_or_equivalent</span><span class="sxs-lookup"><span data-stu-id="b05b0-325">Keywords_hungary_eu_ssn_or_equivalent</span></span>

<span data-ttu-id="b05b0-326">número de seguro social de seguridade</span><span class="sxs-lookup"><span data-stu-id="b05b0-326">hungarian social security number</span></span>
  
<span data-ttu-id="b05b0-327">social security number</span><span class="sxs-lookup"><span data-stu-id="b05b0-327">social security number</span></span>
  
<span data-ttu-id="b05b0-328">socialsecuritynumber#</span><span class="sxs-lookup"><span data-stu-id="b05b0-328">socialsecuritynumber#</span></span>
  
<span data-ttu-id="b05b0-329">hssn#</span><span class="sxs-lookup"><span data-stu-id="b05b0-329">hssn#</span></span>
  
<span data-ttu-id="b05b0-330">socialsecuritynno</span><span class="sxs-lookup"><span data-stu-id="b05b0-330">socialsecuritynno</span></span>
  
<span data-ttu-id="b05b0-331">hssn</span><span class="sxs-lookup"><span data-stu-id="b05b0-331">hssn</span></span>
  
<span data-ttu-id="b05b0-332">taj</span><span class="sxs-lookup"><span data-stu-id="b05b0-332">taj</span></span>
  
<span data-ttu-id="b05b0-333">taj#</span><span class="sxs-lookup"><span data-stu-id="b05b0-333">taj#</span></span>
  
<span data-ttu-id="b05b0-334">es</span><span class="sxs-lookup"><span data-stu-id="b05b0-334">ssn</span></span>
  
<span data-ttu-id="b05b0-335">es</span><span class="sxs-lookup"><span data-stu-id="b05b0-335">ssn#</span></span>
  
<span data-ttu-id="b05b0-336">segurança social não</span><span class="sxs-lookup"><span data-stu-id="b05b0-336">social security no</span></span>
  
<span data-ttu-id="b05b0-337">áfa</span><span class="sxs-lookup"><span data-stu-id="b05b0-337">áfa</span></span>
  
<span data-ttu-id="b05b0-338">közösségi adószám</span><span class="sxs-lookup"><span data-stu-id="b05b0-338">közösségi adószám</span></span>
  
<span data-ttu-id="b05b0-339">általános forgalmi adó szám</span><span class="sxs-lookup"><span data-stu-id="b05b0-339">általános forgalmi adó szám</span></span>
  
<span data-ttu-id="b05b0-340">hozzáadottérték adó</span><span class="sxs-lookup"><span data-stu-id="b05b0-340">hozzáadottérték adó</span></span>
  
<span data-ttu-id="b05b0-341">áfa szám</span><span class="sxs-lookup"><span data-stu-id="b05b0-341">áfa szám</span></span>
  
<span data-ttu-id="b05b0-342">magyar áfa szám</span><span class="sxs-lookup"><span data-stu-id="b05b0-342">magyar áfa szám</span></span>
  
## <a name="portugal"></a><span data-ttu-id="b05b0-343">Portugal</span><span class="sxs-lookup"><span data-stu-id="b05b0-343">Portugal</span></span>

<span data-ttu-id="b05b0-344">Para obter detalhes, consulte a seção "número de cartão de cidadão da Portugal" em [o que os tipos de informações confidenciais buscam](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="b05b0-344">For details, see the section "Portugal Citizen Card Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="spain"></a><span data-ttu-id="b05b0-345">Espanha</span><span class="sxs-lookup"><span data-stu-id="b05b0-345">Spain</span></span>

<span data-ttu-id="b05b0-346">Para obter detalhes, consulte a seção "número de seguridade social da Espanha (SSN)" em [o que os tipos de informações confidenciais procuram](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="b05b0-346">For details, see the section "Spain Social Security Number (SSN)" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="sweden"></a><span data-ttu-id="b05b0-347">Suécia</span><span class="sxs-lookup"><span data-stu-id="b05b0-347">Sweden</span></span>

### <a name="format"></a><span data-ttu-id="b05b0-348">Formatar</span><span class="sxs-lookup"><span data-stu-id="b05b0-348">Format</span></span>

<span data-ttu-id="b05b0-349">12 dígitos sem espaços e delimitadores</span><span class="sxs-lookup"><span data-stu-id="b05b0-349">12 digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="b05b0-350">Padrão</span><span class="sxs-lookup"><span data-stu-id="b05b0-350">Pattern</span></span>

<span data-ttu-id="b05b0-351">12 dígitos:</span><span class="sxs-lookup"><span data-stu-id="b05b0-351">12 digits:</span></span>
  
-  <span data-ttu-id="b05b0-352">Oito dígitos que correspondem à data de nascimento (AAAAMMDD)</span><span class="sxs-lookup"><span data-stu-id="b05b0-352">Eight digits that correspond to the birth date (YYYYMMDD)</span></span> 
    
- <span data-ttu-id="b05b0-353">Três dígitos que correspondem a um número de série em que:</span><span class="sxs-lookup"><span data-stu-id="b05b0-353">Three digits that correspond to a serial number where:</span></span> 
    
  - <span data-ttu-id="b05b0-354">O último dígito no número de série indica sexo pela atribuição de um número ímpar para macho e um número par para o fêmea</span><span class="sxs-lookup"><span data-stu-id="b05b0-354">The last digit in the serial number indicates gender by the assignment of an odd number for male and an even number for female</span></span>
    
  - <span data-ttu-id="b05b0-355">Até 1990, a atribuição de número de série correspondente à região onde o portador do número nasceu ou (se nasceu antes de 1947) em que ele/ela estava em vida, de acordo com os registros de impostos, em 1º de janeiro de 1947, com um código especial (geralmente 9 como o sétimo dígito) para immigrants</span><span class="sxs-lookup"><span data-stu-id="b05b0-355">Up to 1990, the assignment of serial number corresponded to the county where the bearer of the number was born or (if born before 1947) where he/she had been living, according to tax records, on January 1, 1947, with a special code (usually 9 as the 7th digit) for immigrants</span></span> 
    
- <span data-ttu-id="b05b0-356">Um dígito de verificação</span><span class="sxs-lookup"><span data-stu-id="b05b0-356">One check digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="b05b0-357">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="b05b0-357">Checksum</span></span>

<span data-ttu-id="b05b0-358">Sim</span><span class="sxs-lookup"><span data-stu-id="b05b0-358">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="b05b0-359">Definição</span><span class="sxs-lookup"><span data-stu-id="b05b0-359">Definition</span></span>

<span data-ttu-id="b05b0-360">Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="b05b0-360">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="b05b0-361">A função `Func_sweden_eu_ssn_or_equivalent` localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="b05b0-361">The function  `Func_sweden_eu_ssn_or_equivalent` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="b05b0-362">Uma palavra- `Keywords_sweden_eu_ssn_or_equivalent` chave de foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="b05b0-362">A keyword from  `Keywords_sweden_eu_ssn_or_equivalent` is found.</span></span> 
    
<span data-ttu-id="b05b0-363">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="b05b0-363">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="b05b0-364">A função `Func_sweden_eu_ssn_or_equivalent` localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="b05b0-364">The function  `Func_sweden_eu_ssn_or_equivalent` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="b05b0-365">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="b05b0-365">Keywords</span></span>

#### <a name="keywordsswedeneussnorequivalent"></a><span data-ttu-id="b05b0-366">Keywords_sweden_eu_ssn_or_equivalent</span><span class="sxs-lookup"><span data-stu-id="b05b0-366">Keywords_sweden_eu_ssn_or_equivalent</span></span>

<span data-ttu-id="b05b0-367">número de identificação pessoal</span><span class="sxs-lookup"><span data-stu-id="b05b0-367">personal id number</span></span>
  
<span data-ttu-id="b05b0-368">identification number</span><span class="sxs-lookup"><span data-stu-id="b05b0-368">identification number</span></span>
  
<span data-ttu-id="b05b0-369">n º de identificação pessoal</span><span class="sxs-lookup"><span data-stu-id="b05b0-369">personal id no</span></span>
  
<span data-ttu-id="b05b0-370">identidade não</span><span class="sxs-lookup"><span data-stu-id="b05b0-370">identity no</span></span>
  
<span data-ttu-id="b05b0-371">identificação não</span><span class="sxs-lookup"><span data-stu-id="b05b0-371">identification no</span></span>
  
<span data-ttu-id="b05b0-372">identificação pessoal não</span><span class="sxs-lookup"><span data-stu-id="b05b0-372">personal identification no</span></span>
  
<span data-ttu-id="b05b0-373">ID personnummer</span><span class="sxs-lookup"><span data-stu-id="b05b0-373">personnummer id</span></span>
  
<span data-ttu-id="b05b0-374">ID Personligt-Nummer</span><span class="sxs-lookup"><span data-stu-id="b05b0-374">personligt id-nummer</span></span>
  
<span data-ttu-id="b05b0-375">ID unikt-Nummer</span><span class="sxs-lookup"><span data-stu-id="b05b0-375">unikt id-nummer</span></span>
  
<span data-ttu-id="b05b0-376">personnummer</span><span class="sxs-lookup"><span data-stu-id="b05b0-376">personnummer</span></span>
  
<span data-ttu-id="b05b0-377">identifikationsnumret</span><span class="sxs-lookup"><span data-stu-id="b05b0-377">identifikationsnumret</span></span>
  
<span data-ttu-id="b05b0-378">personnummer#</span><span class="sxs-lookup"><span data-stu-id="b05b0-378">personnummer#</span></span>
  
<span data-ttu-id="b05b0-379">identifikationsnumret#</span><span class="sxs-lookup"><span data-stu-id="b05b0-379">identifikationsnumret#</span></span>
  
## <a name="see-also"></a><span data-ttu-id="b05b0-380">Confira também</span><span class="sxs-lookup"><span data-stu-id="b05b0-380">See also</span></span>

[<span data-ttu-id="b05b0-381">O que os tipos de informações confidenciais procuram</span><span class="sxs-lookup"><span data-stu-id="b05b0-381">What the sensitive information types look for</span></span>](what-the-sensitive-information-types-look-for.md)

