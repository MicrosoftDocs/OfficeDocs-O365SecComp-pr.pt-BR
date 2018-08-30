---
title: ID do número de Seguridade Social da UE ou equivalente
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: 8/17/2018
ms.audience: Admin
ms.topic: reference
ms.service: o365-administration
localization_priority: Normal
ms.assetid: 1fabd341-e594-4bfe-961c-62aa82893f60
description: Este tópico mostra o que uma política de prevenção (DLP) de perda de dados procura por quando detecta o tipo de informações confidenciais de número de Seguridade Social da UE ou ID equivalente. Esse tipo de informações confidenciais define diferentes padrões, palavras-chave e outras evidências para cada país.
ms.openlocfilehash: 6f1027dcfb648ed937b8180d74d4bc6348dab650
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22523936"
---
# <a name="eu-social-security-number-or-equivalent-id"></a><span data-ttu-id="f2e1a-104">ID do número de Seguridade Social da UE ou equivalente</span><span class="sxs-lookup"><span data-stu-id="f2e1a-104">EU Social Security Number or Equivalent ID</span></span>

<span data-ttu-id="f2e1a-p102">Este tópico mostra o que uma política de prevenção (DLP) de perda de dados procura por quando detecta o tipo de informações confidenciais de número de Seguridade Social da UE (SSN) ou ID equivalente. Esse tipo de informações confidenciais define diferentes padrões, palavras-chave e outras evidências para cada país.</span><span class="sxs-lookup"><span data-stu-id="f2e1a-p102">This topic shows what a data loss prevention (DLP) policy looks for when it detects the EU Social Security Number (SSN) or Equivalent ID sensitive information type. This sensitive information type defines different patterns, keywords, and other evidence for each country.</span></span>
  
## <a name="austria"></a><span data-ttu-id="f2e1a-107">Áustria</span><span class="sxs-lookup"><span data-stu-id="f2e1a-107">Austria</span></span>

### <a name="format"></a><span data-ttu-id="f2e1a-108">Formato</span><span class="sxs-lookup"><span data-stu-id="f2e1a-108">Format</span></span>

<span data-ttu-id="f2e1a-109">10 dígitos no formato especificado</span><span class="sxs-lookup"><span data-stu-id="f2e1a-109">10 digits in the specified format</span></span>
  
### <a name="pattern"></a><span data-ttu-id="f2e1a-110">Padrão</span><span class="sxs-lookup"><span data-stu-id="f2e1a-110">Pattern</span></span>

<span data-ttu-id="f2e1a-111">10 dígitos:</span><span class="sxs-lookup"><span data-stu-id="f2e1a-111">10 digits:</span></span>
  
-  <span data-ttu-id="f2e1a-112">Três dígitos que correspondem a um número de série</span><span class="sxs-lookup"><span data-stu-id="f2e1a-112">Three digits that correspond to a serial number</span></span> 
    
- <span data-ttu-id="f2e1a-113">Seleção de um dígito</span><span class="sxs-lookup"><span data-stu-id="f2e1a-113">One check digit</span></span>
    
- <span data-ttu-id="f2e1a-114">Seis dígitos que correspondem à data de nascimento (DDMMYY)</span><span class="sxs-lookup"><span data-stu-id="f2e1a-114">Six digits that correspond to the birth date (DDMMYY)</span></span>
    
### <a name="checksum"></a><span data-ttu-id="f2e1a-115">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="f2e1a-115">Checksum</span></span>

<span data-ttu-id="f2e1a-116">Sim</span><span class="sxs-lookup"><span data-stu-id="f2e1a-116">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="f2e1a-117">Definição</span><span class="sxs-lookup"><span data-stu-id="f2e1a-117">Definition</span></span>

<span data-ttu-id="f2e1a-118">Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="f2e1a-118">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="f2e1a-119">A função `Func_austria_eu_ssn_or_equivalent` encontra conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="f2e1a-119">The function  `Func_austria_eu_ssn_or_equivalent` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="f2e1a-120">Uma palavra-chave da `Keywords_austria_eu_ssn_or_equivalent` for encontrado.</span><span class="sxs-lookup"><span data-stu-id="f2e1a-120">A keyword from  `Keywords_austria_eu_ssn_or_equivalent` is found.</span></span> 
    
<span data-ttu-id="f2e1a-121">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="f2e1a-121">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="f2e1a-122">A função `Func_austria_eu_ssn_or_equivalent` encontra conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="f2e1a-122">The function  `Func_austria_eu_ssn_or_equivalent` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="f2e1a-123">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="f2e1a-123">Keywords</span></span>

#### <a name="keywordsaustriaeussnorequivalent"></a><span data-ttu-id="f2e1a-124">Keywords_austria_eu_ssn_or_equivalent</span><span class="sxs-lookup"><span data-stu-id="f2e1a-124">Keywords_austria_eu_ssn_or_equivalent</span></span>

<span data-ttu-id="f2e1a-125">seguridade social nenhum</span><span class="sxs-lookup"><span data-stu-id="f2e1a-125">social security no</span></span>
  
<span data-ttu-id="f2e1a-126">social security number
</span><span class="sxs-lookup"><span data-stu-id="f2e1a-126">social security number</span></span>
  
<span data-ttu-id="f2e1a-127">
social security code</span><span class="sxs-lookup"><span data-stu-id="f2e1a-127">social security code</span></span>
  
<span data-ttu-id="f2e1a-128">número do seguro</span><span class="sxs-lookup"><span data-stu-id="f2e1a-128">insurance number</span></span>
  
<span data-ttu-id="f2e1a-129">ssn austríaco</span><span class="sxs-lookup"><span data-stu-id="f2e1a-129">austrian ssn</span></span>
  
<span data-ttu-id="f2e1a-130">SSN #</span><span class="sxs-lookup"><span data-stu-id="f2e1a-130">ssn#</span></span>
  
<span data-ttu-id="f2e1a-131">SSN</span><span class="sxs-lookup"><span data-stu-id="f2e1a-131">ssn</span></span>
  
<span data-ttu-id="f2e1a-132">código de seguro</span><span class="sxs-lookup"><span data-stu-id="f2e1a-132">insurance code</span></span>
  
<span data-ttu-id="f2e1a-133">código de seguros #</span><span class="sxs-lookup"><span data-stu-id="f2e1a-133">insurance code#</span></span>
  
<span data-ttu-id="f2e1a-134">socialsecurityno #</span><span class="sxs-lookup"><span data-stu-id="f2e1a-134">socialsecurityno#</span></span>
  
<span data-ttu-id="f2e1a-135">sozialversicherungsnummer</span><span class="sxs-lookup"><span data-stu-id="f2e1a-135">sozialversicherungsnummer</span></span>
  
<span data-ttu-id="f2e1a-136">soziale sicherheit kein</span><span class="sxs-lookup"><span data-stu-id="f2e1a-136">soziale sicherheit kein</span></span>
  
<span data-ttu-id="f2e1a-137">versicherungsnummer</span><span class="sxs-lookup"><span data-stu-id="f2e1a-137">versicherungsnummer</span></span>
  
## <a name="belgium"></a><span data-ttu-id="f2e1a-138">Bélgica</span><span class="sxs-lookup"><span data-stu-id="f2e1a-138">Belgium</span></span>

### <a name="format"></a><span data-ttu-id="f2e1a-139">Formato</span><span class="sxs-lookup"><span data-stu-id="f2e1a-139">Format</span></span>

<span data-ttu-id="f2e1a-140">11 dígitos sem espaços ou delimitadores</span><span class="sxs-lookup"><span data-stu-id="f2e1a-140">11 digits without spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="f2e1a-141">Padrão</span><span class="sxs-lookup"><span data-stu-id="f2e1a-141">Pattern</span></span>

<span data-ttu-id="f2e1a-142">11 dígitos</span><span class="sxs-lookup"><span data-stu-id="f2e1a-142">11 digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="f2e1a-143">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="f2e1a-143">Checksum</span></span>

<span data-ttu-id="f2e1a-144">Sim</span><span class="sxs-lookup"><span data-stu-id="f2e1a-144">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="f2e1a-145">Definição</span><span class="sxs-lookup"><span data-stu-id="f2e1a-145">Definition</span></span>

<span data-ttu-id="f2e1a-146">Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="f2e1a-146">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="f2e1a-147">A função `Func_belgium_eu_ssn_or_equivalent` encontra conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="f2e1a-147">The function  `Func_belgium_eu_ssn_or_equivalent` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="f2e1a-148">Uma palavra-chave da `Keywords_belgium_eu_ssn_or_equivalent` for encontrado.</span><span class="sxs-lookup"><span data-stu-id="f2e1a-148">A keyword from  `Keywords_belgium_eu_ssn_or_equivalent` is found.</span></span> 
    
<span data-ttu-id="f2e1a-149">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="f2e1a-149">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="f2e1a-150">A função `Func_belgium_eu_ssn_or_equivalent` encontra conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="f2e1a-150">The function  `Func_belgium_eu_ssn_or_equivalent` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="f2e1a-151">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="f2e1a-151">Keywords</span></span>

#### <a name="keywordsbelgiumeussnorequivalent"></a><span data-ttu-id="f2e1a-152">Keywords_belgium_eu_ssn_or_equivalent</span><span class="sxs-lookup"><span data-stu-id="f2e1a-152">Keywords_belgium_eu_ssn_or_equivalent</span></span>

<span data-ttu-id="f2e1a-153">número nacional belga</span><span class="sxs-lookup"><span data-stu-id="f2e1a-153">belgian national number</span></span>
  
<span data-ttu-id="f2e1a-154">número nacional</span><span class="sxs-lookup"><span data-stu-id="f2e1a-154">national number</span></span>
  
<span data-ttu-id="f2e1a-155">social security number
</span><span class="sxs-lookup"><span data-stu-id="f2e1a-155">social security number</span></span>
  
<span data-ttu-id="f2e1a-156">nationalnumber #</span><span class="sxs-lookup"><span data-stu-id="f2e1a-156">nationalnumber#</span></span>
  
<span data-ttu-id="f2e1a-157">SSN #</span><span class="sxs-lookup"><span data-stu-id="f2e1a-157">ssn#</span></span>
  
<span data-ttu-id="f2e1a-158">SSN</span><span class="sxs-lookup"><span data-stu-id="f2e1a-158">ssn</span></span>
  
<span data-ttu-id="f2e1a-159">nationalnumber</span><span class="sxs-lookup"><span data-stu-id="f2e1a-159">nationalnumber</span></span>
  
<span data-ttu-id="f2e1a-160">bnn #</span><span class="sxs-lookup"><span data-stu-id="f2e1a-160">bnn#</span></span>
  
<span data-ttu-id="f2e1a-161">bnn</span><span class="sxs-lookup"><span data-stu-id="f2e1a-161">bnn</span></span>
  
<span data-ttu-id="f2e1a-162">número de identificação pessoal</span><span class="sxs-lookup"><span data-stu-id="f2e1a-162">personal id number</span></span>
  
<span data-ttu-id="f2e1a-163">personalidnumber #</span><span class="sxs-lookup"><span data-stu-id="f2e1a-163">personalidnumber#</span></span>
  
<span data-ttu-id="f2e1a-164">numéro nacional</span><span class="sxs-lookup"><span data-stu-id="f2e1a-164">numéro national</span></span>
  
<span data-ttu-id="f2e1a-165">numéro de sécurité
</span><span class="sxs-lookup"><span data-stu-id="f2e1a-165">numéro de sécurité</span></span>
  
<span data-ttu-id="f2e1a-166">d numéro'assuré</span><span class="sxs-lookup"><span data-stu-id="f2e1a-166">numéro d'assuré</span></span>
  
<span data-ttu-id="f2e1a-167">identifiant nacional</span><span class="sxs-lookup"><span data-stu-id="f2e1a-167">identifiant national</span></span>
  
<span data-ttu-id="f2e1a-168">identifiantnational #</span><span class="sxs-lookup"><span data-stu-id="f2e1a-168">identifiantnational#</span></span>
  
<span data-ttu-id="f2e1a-169">numéronational #</span><span class="sxs-lookup"><span data-stu-id="f2e1a-169">numéronational#</span></span>
  
## <a name="croatia"></a><span data-ttu-id="f2e1a-170">Croácia</span><span class="sxs-lookup"><span data-stu-id="f2e1a-170">Croatia</span></span>

### <a name="format"></a><span data-ttu-id="f2e1a-171">Formato</span><span class="sxs-lookup"><span data-stu-id="f2e1a-171">Format</span></span>

<span data-ttu-id="f2e1a-172">11 dígitos sem espaços e delimitadores</span><span class="sxs-lookup"><span data-stu-id="f2e1a-172">11 digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="f2e1a-173">Padrão</span><span class="sxs-lookup"><span data-stu-id="f2e1a-173">Pattern</span></span>

 <span data-ttu-id="f2e1a-174">11 dígitos:</span><span class="sxs-lookup"><span data-stu-id="f2e1a-174">11 digits:</span></span> 
  
-  <span data-ttu-id="f2e1a-175">Dez dígitos</span><span class="sxs-lookup"><span data-stu-id="f2e1a-175">Ten digits</span></span> 
    
- <span data-ttu-id="f2e1a-176">Seleção de um dígito</span><span class="sxs-lookup"><span data-stu-id="f2e1a-176">One check digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="f2e1a-177">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="f2e1a-177">Checksum</span></span>

<span data-ttu-id="f2e1a-178">Sim</span><span class="sxs-lookup"><span data-stu-id="f2e1a-178">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="f2e1a-179">Definição</span><span class="sxs-lookup"><span data-stu-id="f2e1a-179">Definition</span></span>

<span data-ttu-id="f2e1a-180">Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="f2e1a-180">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="f2e1a-181">A função `Func_croatia_eu_ssn_or_equivalent` encontra conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="f2e1a-181">The function  `Func_croatia_eu_ssn_or_equivalent` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="f2e1a-182">Uma palavra-chave da `Keywords_croatia_eu_ssn_or_equivalent` for encontrado.</span><span class="sxs-lookup"><span data-stu-id="f2e1a-182">A keyword from  `Keywords_croatia_eu_ssn_or_equivalent` is found.</span></span> 
    
<span data-ttu-id="f2e1a-183">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="f2e1a-183">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="f2e1a-184">A função `Func_croatia_eu_ssn_or_equivalent` encontra conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="f2e1a-184">The function  `Func_croatia_eu_ssn_or_equivalent` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="f2e1a-185">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="f2e1a-185">Keywords</span></span>

#### <a name="keywordscroatiaeussnorequivalent"></a><span data-ttu-id="f2e1a-186">Keywords_croatia_eu_ssn_or_equivalent</span><span class="sxs-lookup"><span data-stu-id="f2e1a-186">Keywords_croatia_eu_ssn_or_equivalent</span></span>

<span data-ttu-id="f2e1a-187">número de identificação pessoal</span><span class="sxs-lookup"><span data-stu-id="f2e1a-187">personal identification number</span></span>
  
<span data-ttu-id="f2e1a-188">número de cidadãos mestre</span><span class="sxs-lookup"><span data-stu-id="f2e1a-188">master citizen number</span></span>
  
<span data-ttu-id="f2e1a-189">número de identificação nacional</span><span class="sxs-lookup"><span data-stu-id="f2e1a-189">national identification number</span></span>
  
<span data-ttu-id="f2e1a-190">social security number
</span><span class="sxs-lookup"><span data-stu-id="f2e1a-190">social security number</span></span>
  
<span data-ttu-id="f2e1a-191">nationalnumber #</span><span class="sxs-lookup"><span data-stu-id="f2e1a-191">nationalnumber#</span></span>
  
<span data-ttu-id="f2e1a-192">SSN #</span><span class="sxs-lookup"><span data-stu-id="f2e1a-192">ssn#</span></span>
  
<span data-ttu-id="f2e1a-193">SSN</span><span class="sxs-lookup"><span data-stu-id="f2e1a-193">ssn</span></span>
  
<span data-ttu-id="f2e1a-194">nationalnumber</span><span class="sxs-lookup"><span data-stu-id="f2e1a-194">nationalnumber</span></span>
  
<span data-ttu-id="f2e1a-195">bnn #</span><span class="sxs-lookup"><span data-stu-id="f2e1a-195">bnn#</span></span>
  
<span data-ttu-id="f2e1a-196">bnn</span><span class="sxs-lookup"><span data-stu-id="f2e1a-196">bnn</span></span>
  
<span data-ttu-id="f2e1a-197">número de identificação pessoal</span><span class="sxs-lookup"><span data-stu-id="f2e1a-197">personal id number</span></span>
  
<span data-ttu-id="f2e1a-198">personalidnumber #</span><span class="sxs-lookup"><span data-stu-id="f2e1a-198">personalidnumber#</span></span>
  
<span data-ttu-id="f2e1a-199">oib</span><span class="sxs-lookup"><span data-stu-id="f2e1a-199">oib</span></span>
  
<span data-ttu-id="f2e1a-200">osobni identifikacijski broj</span><span class="sxs-lookup"><span data-stu-id="f2e1a-200">osobni identifikacijski broj</span></span>
  
## <a name="czech-republic"></a><span data-ttu-id="f2e1a-201">República Tcheca</span><span class="sxs-lookup"><span data-stu-id="f2e1a-201">Czech Republic</span></span>

### <a name="format"></a><span data-ttu-id="f2e1a-202">Formato</span><span class="sxs-lookup"><span data-stu-id="f2e1a-202">Format</span></span>

<span data-ttu-id="f2e1a-203">Dez dígitos e uma barra invertida no padrão especificado</span><span class="sxs-lookup"><span data-stu-id="f2e1a-203">Ten digits and a backslash in the specified pattern</span></span>
  
### <a name="pattern"></a><span data-ttu-id="f2e1a-204">Padrão</span><span class="sxs-lookup"><span data-stu-id="f2e1a-204">Pattern</span></span>

<span data-ttu-id="f2e1a-205">Dez dígitos e uma barra invertida:</span><span class="sxs-lookup"><span data-stu-id="f2e1a-205">Ten digits and a backslash:</span></span>
  
- <span data-ttu-id="f2e1a-206">Seis dígitos que correspondem à data de nascimento (aammdd):</span><span class="sxs-lookup"><span data-stu-id="f2e1a-206">Six digits that correspond to the birth date (YYMMDD):</span></span> 
    
- <span data-ttu-id="f2e1a-207">Uma barra invertida</span><span class="sxs-lookup"><span data-stu-id="f2e1a-207">A backslash</span></span>
    
- <span data-ttu-id="f2e1a-208">Três dígitos que correspondem a um número de série que separa pessoas nascidas na mesma data</span><span class="sxs-lookup"><span data-stu-id="f2e1a-208">Three digits that correspond to a serial number that separates persons born on the same date</span></span>
    
- <span data-ttu-id="f2e1a-209">Seleção de um dígito</span><span class="sxs-lookup"><span data-stu-id="f2e1a-209">One check digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="f2e1a-210">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="f2e1a-210">Checksum</span></span>

<span data-ttu-id="f2e1a-211">Sim</span><span class="sxs-lookup"><span data-stu-id="f2e1a-211">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="f2e1a-212">Definição</span><span class="sxs-lookup"><span data-stu-id="f2e1a-212">Definition</span></span>

<span data-ttu-id="f2e1a-213">Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="f2e1a-213">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="f2e1a-214">A função `Func_czech_republic_eu_ssn_or_equivalent` encontra conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="f2e1a-214">The function  `Func_czech_republic_eu_ssn_or_equivalent` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="f2e1a-215">Uma palavra-chave da `Keywords_czech_republic_eu_ssn_or_equivalent` for encontrado.</span><span class="sxs-lookup"><span data-stu-id="f2e1a-215">A keyword from  `Keywords_czech_republic_eu_ssn_or_equivalent` is found.</span></span> 
    
<span data-ttu-id="f2e1a-216">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="f2e1a-216">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="f2e1a-217">A função `Func_czech_republic_eu_ssn_or_equivalent` encontra conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="f2e1a-217">The function  `Func_czech_republic_eu_ssn_or_equivalent` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="f2e1a-218">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="f2e1a-218">Keywords</span></span>

#### <a name="keywordsczechrepubliceussnorequivalent"></a><span data-ttu-id="f2e1a-219">Keywords_czech_republic_eu_ssn_or_equivalent</span><span class="sxs-lookup"><span data-stu-id="f2e1a-219">Keywords_czech_republic_eu_ssn_or_equivalent</span></span>

<span data-ttu-id="f2e1a-220">número de nascimento</span><span class="sxs-lookup"><span data-stu-id="f2e1a-220">birth number</span></span>
  
<span data-ttu-id="f2e1a-221">número de identificação nacional</span><span class="sxs-lookup"><span data-stu-id="f2e1a-221">national identification number</span></span>
  
<span data-ttu-id="f2e1a-222">número de identificação pessoal</span><span class="sxs-lookup"><span data-stu-id="f2e1a-222">personal identification number</span></span>
  
<span data-ttu-id="f2e1a-223">social security number
</span><span class="sxs-lookup"><span data-stu-id="f2e1a-223">social security number</span></span>
  
<span data-ttu-id="f2e1a-224">nationalnumber #</span><span class="sxs-lookup"><span data-stu-id="f2e1a-224">nationalnumber#</span></span>
  
<span data-ttu-id="f2e1a-225">SSN #</span><span class="sxs-lookup"><span data-stu-id="f2e1a-225">ssn#</span></span>
  
<span data-ttu-id="f2e1a-226">SSN</span><span class="sxs-lookup"><span data-stu-id="f2e1a-226">ssn</span></span>
  
<span data-ttu-id="f2e1a-227">número nacional</span><span class="sxs-lookup"><span data-stu-id="f2e1a-227">national number</span></span>
  
<span data-ttu-id="f2e1a-228">número de identificação pessoal</span><span class="sxs-lookup"><span data-stu-id="f2e1a-228">personal id number</span></span>
  
<span data-ttu-id="f2e1a-229">personalidnumber #</span><span class="sxs-lookup"><span data-stu-id="f2e1a-229">personalidnumber#</span></span>
  
<span data-ttu-id="f2e1a-230">rč</span><span class="sxs-lookup"><span data-stu-id="f2e1a-230">rč</span></span>
  
<span data-ttu-id="f2e1a-231">rodné číslo</span><span class="sxs-lookup"><span data-stu-id="f2e1a-231">rodné číslo</span></span>
  
<span data-ttu-id="f2e1a-232">rodne cislo</span><span class="sxs-lookup"><span data-stu-id="f2e1a-232">rodne cislo</span></span>
  
## <a name="denmark"></a><span data-ttu-id="f2e1a-233">Dinamarca</span><span class="sxs-lookup"><span data-stu-id="f2e1a-233">Denmark</span></span>

### <a name="format"></a><span data-ttu-id="f2e1a-234">Formato</span><span class="sxs-lookup"><span data-stu-id="f2e1a-234">Format</span></span>

<span data-ttu-id="f2e1a-235">Dez dígitos e um hífen no padrão especificado</span><span class="sxs-lookup"><span data-stu-id="f2e1a-235">Ten digits and a hyphen in the specified pattern</span></span>
  
### <a name="pattern"></a><span data-ttu-id="f2e1a-236">Padrão</span><span class="sxs-lookup"><span data-stu-id="f2e1a-236">Pattern</span></span>

<span data-ttu-id="f2e1a-237">Dez dígitos e um hífen:</span><span class="sxs-lookup"><span data-stu-id="f2e1a-237">Ten digits and a hyphen:</span></span>
  
- <span data-ttu-id="f2e1a-238">Seis dígitos que correspondem à data de nascimento (DDMMYY)</span><span class="sxs-lookup"><span data-stu-id="f2e1a-238">Six digits that correspond to the birth date (DDMMYY)</span></span> 
    
- <span data-ttu-id="f2e1a-239">Um hífen</span><span class="sxs-lookup"><span data-stu-id="f2e1a-239">A hyphen</span></span>
    
- <span data-ttu-id="f2e1a-240">Quatro dígitos que correspondem a um número de sequência</span><span class="sxs-lookup"><span data-stu-id="f2e1a-240">Four digits that correspond to a sequence number</span></span>
    
### <a name="checksum"></a><span data-ttu-id="f2e1a-241">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="f2e1a-241">Checksum</span></span>

<span data-ttu-id="f2e1a-242">Sim</span><span class="sxs-lookup"><span data-stu-id="f2e1a-242">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="f2e1a-243">Definição</span><span class="sxs-lookup"><span data-stu-id="f2e1a-243">Definition</span></span>

<span data-ttu-id="f2e1a-244">Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="f2e1a-244">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="f2e1a-245">A função `Func_denmark_eu_ssn_or_equivalent` encontra conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="f2e1a-245">The function  `Func_denmark_eu_ssn_or_equivalent` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="f2e1a-246">Uma palavra-chave da `Keywords_denmark_eu_ssn_or_equivalent` for encontrado.</span><span class="sxs-lookup"><span data-stu-id="f2e1a-246">A keyword from  `Keywords_denmark_eu_ssn_or_equivalent` is found.</span></span> 
    
<span data-ttu-id="f2e1a-247">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="f2e1a-247">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="f2e1a-248">A função `Func_denmark_eu_ssn_or_equivalent` encontra conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="f2e1a-248">The function  `Func_denmark_eu_ssn_or_equivalent` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="f2e1a-249">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="f2e1a-249">Keywords</span></span>

#### <a name="keywordsdenmarkeussnorequivalent"></a><span data-ttu-id="f2e1a-250">Keywords_denmark_eu_ssn_or_equivalent</span><span class="sxs-lookup"><span data-stu-id="f2e1a-250">Keywords_denmark_eu_ssn_or_equivalent</span></span>

<span data-ttu-id="f2e1a-251">número de identificação pessoal</span><span class="sxs-lookup"><span data-stu-id="f2e1a-251">personal identification number</span></span>
  
<span data-ttu-id="f2e1a-252">número de identificação nacional</span><span class="sxs-lookup"><span data-stu-id="f2e1a-252">national identification number</span></span>
  
<span data-ttu-id="f2e1a-253">social security number
</span><span class="sxs-lookup"><span data-stu-id="f2e1a-253">social security number</span></span>
  
<span data-ttu-id="f2e1a-254">nationalnumber #</span><span class="sxs-lookup"><span data-stu-id="f2e1a-254">nationalnumber#</span></span>
  
<span data-ttu-id="f2e1a-255">SSN #</span><span class="sxs-lookup"><span data-stu-id="f2e1a-255">ssn#</span></span>
  
<span data-ttu-id="f2e1a-256">SSN</span><span class="sxs-lookup"><span data-stu-id="f2e1a-256">ssn</span></span>
  
<span data-ttu-id="f2e1a-257">número nacional</span><span class="sxs-lookup"><span data-stu-id="f2e1a-257">national number</span></span>
  
<span data-ttu-id="f2e1a-258">número de identificação pessoal</span><span class="sxs-lookup"><span data-stu-id="f2e1a-258">personal id number</span></span>
  
<span data-ttu-id="f2e1a-259">personalidnumber #</span><span class="sxs-lookup"><span data-stu-id="f2e1a-259">personalidnumber#</span></span>
  
<span data-ttu-id="f2e1a-260">CPR-nummer</span><span class="sxs-lookup"><span data-stu-id="f2e1a-260">cpr-nummer</span></span>
  
<span data-ttu-id="f2e1a-261">personnummer</span><span class="sxs-lookup"><span data-stu-id="f2e1a-261">personnummer</span></span>
  
## <a name="finland"></a><span data-ttu-id="f2e1a-262">Finlândia</span><span class="sxs-lookup"><span data-stu-id="f2e1a-262">Finland</span></span>

### <a name="format"></a><span data-ttu-id="f2e1a-263">Formato</span><span class="sxs-lookup"><span data-stu-id="f2e1a-263">Format</span></span>

<span data-ttu-id="f2e1a-264">Uma combinação de caracteres 11 no formato especificado</span><span class="sxs-lookup"><span data-stu-id="f2e1a-264">An 11-character combination in the specified format</span></span>
  
### <a name="pattern"></a><span data-ttu-id="f2e1a-265">Padrão</span><span class="sxs-lookup"><span data-stu-id="f2e1a-265">Pattern</span></span>

<span data-ttu-id="f2e1a-266">Uma combinação de 11 caracteres em um formato específico:</span><span class="sxs-lookup"><span data-stu-id="f2e1a-266">An 11-character combination in the specified format:</span></span>
  
-  <span data-ttu-id="f2e1a-267">Seis dígitos</span><span class="sxs-lookup"><span data-stu-id="f2e1a-267">Six digits</span></span> 
    
- <span data-ttu-id="f2e1a-268">Uma instância de um dos seguintes:</span><span class="sxs-lookup"><span data-stu-id="f2e1a-268">One instance of one of the following:</span></span>
    
  - <span data-ttu-id="f2e1a-269">Símbolo de mais</span><span class="sxs-lookup"><span data-stu-id="f2e1a-269">Plus symbol</span></span>
    
  - <span data-ttu-id="f2e1a-270">Menos símbolo</span><span class="sxs-lookup"><span data-stu-id="f2e1a-270">Minus symbol</span></span>
    
  - <span data-ttu-id="f2e1a-271">A letra "A" (não diferencia maiusculas de minúsculas)</span><span class="sxs-lookup"><span data-stu-id="f2e1a-271">The letter "A" (not case-sensitive)</span></span>
    
- <span data-ttu-id="f2e1a-272">Três dígitos</span><span class="sxs-lookup"><span data-stu-id="f2e1a-272">Three digits</span></span>
    
- <span data-ttu-id="f2e1a-273">Uma letra ou dígito de um</span><span class="sxs-lookup"><span data-stu-id="f2e1a-273">One letter or one digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="f2e1a-274">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="f2e1a-274">Checksum</span></span>

<span data-ttu-id="f2e1a-275">Sim</span><span class="sxs-lookup"><span data-stu-id="f2e1a-275">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="f2e1a-276">Definição</span><span class="sxs-lookup"><span data-stu-id="f2e1a-276">Definition</span></span>

<span data-ttu-id="f2e1a-277">Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="f2e1a-277">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="f2e1a-278">A função `Func_finland_eu_ssn_or_equivalent` encontra conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="f2e1a-278">The function  `Func_finland_eu_ssn_or_equivalent` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="f2e1a-279">Uma palavra-chave da `Keywords_finland_eu_ssn_or_equivalent` for encontrado.</span><span class="sxs-lookup"><span data-stu-id="f2e1a-279">A keyword from  `Keywords_finland_eu_ssn_or_equivalent` is found.</span></span> 
    
<span data-ttu-id="f2e1a-280">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="f2e1a-280">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="f2e1a-281">A função `Func_finland_eu_ssn_or_equivalent` encontra conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="f2e1a-281">The function  `Func_finland_eu_ssn_or_equivalent` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="f2e1a-282">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="f2e1a-282">Keywords</span></span>

#### <a name="keywordsfinlandeussnorequivalent"></a><span data-ttu-id="f2e1a-283">Keywords_finland_eu_ssn_or_equivalent</span><span class="sxs-lookup"><span data-stu-id="f2e1a-283">Keywords_finland_eu_ssn_or_equivalent</span></span>

<span data-ttu-id="f2e1a-284">identification number
</span><span class="sxs-lookup"><span data-stu-id="f2e1a-284">identification number</span></span>
  
<span data-ttu-id="f2e1a-285">identificação pessoal</span><span class="sxs-lookup"><span data-stu-id="f2e1a-285">personal id</span></span>
  
<span data-ttu-id="f2e1a-286">número de identidade</span><span class="sxs-lookup"><span data-stu-id="f2e1a-286">identity number</span></span>
  
<span data-ttu-id="f2e1a-287">número de identificação nacional finlandês</span><span class="sxs-lookup"><span data-stu-id="f2e1a-287">finnish national id number</span></span>
  
<span data-ttu-id="f2e1a-288">personalidnumber #</span><span class="sxs-lookup"><span data-stu-id="f2e1a-288">personalidnumber#</span></span>
  
<span data-ttu-id="f2e1a-289">número de identificação nacional</span><span class="sxs-lookup"><span data-stu-id="f2e1a-289">national identification number</span></span>
  
<span data-ttu-id="f2e1a-290">número de identificação</span><span class="sxs-lookup"><span data-stu-id="f2e1a-290">id number</span></span>
  
<span data-ttu-id="f2e1a-291">id nacional nenhum.</span><span class="sxs-lookup"><span data-stu-id="f2e1a-291">national id no.</span></span>
  
<span data-ttu-id="f2e1a-292">número de identificação nacional</span><span class="sxs-lookup"><span data-stu-id="f2e1a-292">national id number</span></span>
  
<span data-ttu-id="f2e1a-293">ID nenhum</span><span class="sxs-lookup"><span data-stu-id="f2e1a-293">id no</span></span>
  
<span data-ttu-id="f2e1a-294">tunnistenumero</span><span class="sxs-lookup"><span data-stu-id="f2e1a-294">tunnistenumero</span></span>
  
<span data-ttu-id="f2e1a-295">henkilötunnus</span><span class="sxs-lookup"><span data-stu-id="f2e1a-295">henkilötunnus</span></span>
  
<span data-ttu-id="f2e1a-296">yksilöllinen henkilökohtainen tunnistenumero</span><span class="sxs-lookup"><span data-stu-id="f2e1a-296">yksilöllinen henkilökohtainen tunnistenumero</span></span>
  
<span data-ttu-id="f2e1a-297">ainutlaatuinen henkilökohtainen tunnus</span><span class="sxs-lookup"><span data-stu-id="f2e1a-297">ainutlaatuinen henkilökohtainen tunnus</span></span>
  
<span data-ttu-id="f2e1a-298">numero identiteetti</span><span class="sxs-lookup"><span data-stu-id="f2e1a-298">identiteetti numero</span></span>
  
<span data-ttu-id="f2e1a-299">suomen kansallinen henkilötunnus</span><span class="sxs-lookup"><span data-stu-id="f2e1a-299">suomen kansallinen henkilötunnus</span></span>
  
<span data-ttu-id="f2e1a-300">henkilötunnusnumero #</span><span class="sxs-lookup"><span data-stu-id="f2e1a-300">henkilötunnusnumero#</span></span>
  
<span data-ttu-id="f2e1a-301">kansallisen tunnistenumero</span><span class="sxs-lookup"><span data-stu-id="f2e1a-301">kansallisen tunnistenumero</span></span>
  
<span data-ttu-id="f2e1a-302">tunnusnumero</span><span class="sxs-lookup"><span data-stu-id="f2e1a-302">tunnusnumero</span></span>
  
<span data-ttu-id="f2e1a-303">kansallinen tunnus numero</span><span class="sxs-lookup"><span data-stu-id="f2e1a-303">kansallinen tunnus numero</span></span>
  
<span data-ttu-id="f2e1a-304">hetu</span><span class="sxs-lookup"><span data-stu-id="f2e1a-304">hetu</span></span>
  
## <a name="france"></a><span data-ttu-id="f2e1a-305">França</span><span class="sxs-lookup"><span data-stu-id="f2e1a-305">France</span></span>

<span data-ttu-id="f2e1a-306">Para obter detalhes, consulte a seção "França número de Seguridade Social (INSEE)" em [quais tipos de informações confidenciais a procurar](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="f2e1a-306">For details, see the section "France Social Security Number (INSEE)" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="germany"></a><span data-ttu-id="f2e1a-307">Alemanha</span><span class="sxs-lookup"><span data-stu-id="f2e1a-307">Germany</span></span>

<span data-ttu-id="f2e1a-308">Para obter detalhes, consulte a seção "Número de cartão de identificação da Alemanha" em [quais tipos de informações confidenciais a procurar](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="f2e1a-308">For details, see the section "Germany Identity Card Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="greece"></a><span data-ttu-id="f2e1a-309">Grécia</span><span class="sxs-lookup"><span data-stu-id="f2e1a-309">Greece</span></span>

<span data-ttu-id="f2e1a-310">Para obter detalhes, consulte a seção "Grécia cartão de identificação nacional" nos [quais os tipos de informações confidenciais procurar](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="f2e1a-310">For details, see the section "Greece National ID Card" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="hungary"></a><span data-ttu-id="f2e1a-311">Hungria</span><span class="sxs-lookup"><span data-stu-id="f2e1a-311">Hungary</span></span>

### <a name="format"></a><span data-ttu-id="f2e1a-312">Formato</span><span class="sxs-lookup"><span data-stu-id="f2e1a-312">Format</span></span>

<span data-ttu-id="f2e1a-313">Nove dígitos sem espaços e delimitadores</span><span class="sxs-lookup"><span data-stu-id="f2e1a-313">Nine digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="f2e1a-314">Padrão</span><span class="sxs-lookup"><span data-stu-id="f2e1a-314">Pattern</span></span>

<span data-ttu-id="f2e1a-315">Nove dígitos</span><span class="sxs-lookup"><span data-stu-id="f2e1a-315">Nine digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="f2e1a-316">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="f2e1a-316">Checksum</span></span>

<span data-ttu-id="f2e1a-317">Sim</span><span class="sxs-lookup"><span data-stu-id="f2e1a-317">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="f2e1a-318">Definição</span><span class="sxs-lookup"><span data-stu-id="f2e1a-318">Definition</span></span>

<span data-ttu-id="f2e1a-319">Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="f2e1a-319">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="f2e1a-320">A função `Func_hungary_eu_ssn_or_equivalent` encontra conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="f2e1a-320">The function  `Func_hungary_eu_ssn_or_equivalent` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="f2e1a-321">Uma palavra-chave da `Keywords_hungary_eu_ssn_or_equivalent` for encontrado.</span><span class="sxs-lookup"><span data-stu-id="f2e1a-321">A keyword from  `Keywords_hungary_eu_ssn_or_equivalent` is found.</span></span> 
    
<span data-ttu-id="f2e1a-322">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="f2e1a-322">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="f2e1a-323">A função `Func_hungary_eu_ssn_or_equivalent` encontra conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="f2e1a-323">The function  `Func_hungary_eu_ssn_or_equivalent` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="f2e1a-324">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="f2e1a-324">Keywords</span></span>

#### <a name="keywordshungaryeussnorequivalent"></a><span data-ttu-id="f2e1a-325">Keywords_hungary_eu_ssn_or_equivalent</span><span class="sxs-lookup"><span data-stu-id="f2e1a-325">Keywords_hungary_eu_ssn_or_equivalent</span></span>

<span data-ttu-id="f2e1a-326">número de seguridade social húngaro</span><span class="sxs-lookup"><span data-stu-id="f2e1a-326">hungarian social security number</span></span>
  
<span data-ttu-id="f2e1a-327">social security number
</span><span class="sxs-lookup"><span data-stu-id="f2e1a-327">social security number</span></span>
  
<span data-ttu-id="f2e1a-328">NúmeroDoINPS #</span><span class="sxs-lookup"><span data-stu-id="f2e1a-328">socialsecuritynumber#</span></span>
  
<span data-ttu-id="f2e1a-329">hssn #</span><span class="sxs-lookup"><span data-stu-id="f2e1a-329">hssn#</span></span>
  
<span data-ttu-id="f2e1a-330">socialsecuritynno</span><span class="sxs-lookup"><span data-stu-id="f2e1a-330">socialsecuritynno</span></span>
  
<span data-ttu-id="f2e1a-331">hssn</span><span class="sxs-lookup"><span data-stu-id="f2e1a-331">hssn</span></span>
  
<span data-ttu-id="f2e1a-332">taj</span><span class="sxs-lookup"><span data-stu-id="f2e1a-332">taj</span></span>
  
<span data-ttu-id="f2e1a-333">taj #</span><span class="sxs-lookup"><span data-stu-id="f2e1a-333">taj#</span></span>
  
<span data-ttu-id="f2e1a-334">SSN</span><span class="sxs-lookup"><span data-stu-id="f2e1a-334">ssn</span></span>
  
<span data-ttu-id="f2e1a-335">SSN #</span><span class="sxs-lookup"><span data-stu-id="f2e1a-335">ssn#</span></span>
  
<span data-ttu-id="f2e1a-336">seguridade social nenhum</span><span class="sxs-lookup"><span data-stu-id="f2e1a-336">social security no</span></span>
  
<span data-ttu-id="f2e1a-337">áfa</span><span class="sxs-lookup"><span data-stu-id="f2e1a-337">áfa</span></span>
  
<span data-ttu-id="f2e1a-338">közösségi adószám</span><span class="sxs-lookup"><span data-stu-id="f2e1a-338">közösségi adószám</span></span>
  
<span data-ttu-id="f2e1a-339">általános forgalmi adó szám</span><span class="sxs-lookup"><span data-stu-id="f2e1a-339">általános forgalmi adó szám</span></span>
  
<span data-ttu-id="f2e1a-340">hozzáadottérték adó</span><span class="sxs-lookup"><span data-stu-id="f2e1a-340">hozzáadottérték adó</span></span>
  
<span data-ttu-id="f2e1a-341">áfa szám</span><span class="sxs-lookup"><span data-stu-id="f2e1a-341">áfa szám</span></span>
  
<span data-ttu-id="f2e1a-342">áfa magyar szám</span><span class="sxs-lookup"><span data-stu-id="f2e1a-342">magyar áfa szám</span></span>
  
## <a name="portugal"></a><span data-ttu-id="f2e1a-343">Portugal</span><span class="sxs-lookup"><span data-stu-id="f2e1a-343">Portugal</span></span>

<span data-ttu-id="f2e1a-344">Para obter detalhes, consulte a seção "Número de cartão de cidadãos Portugal" nos [quais os tipos de informações confidenciais procurar](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="f2e1a-344">For details, see the section "Portugal Citizen Card Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="spain"></a><span data-ttu-id="f2e1a-345">Espanha</span><span class="sxs-lookup"><span data-stu-id="f2e1a-345">Spain</span></span>

<span data-ttu-id="f2e1a-346">Para obter detalhes, consulte a seção "Espanha número de Seguridade Social (SSN)" em [quais tipos de informações confidenciais a procurar](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="f2e1a-346">For details, see the section "Spain Social Security Number (SSN)" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="sweden"></a><span data-ttu-id="f2e1a-347">Suécia</span><span class="sxs-lookup"><span data-stu-id="f2e1a-347">Sweden</span></span>

### <a name="format"></a><span data-ttu-id="f2e1a-348">Formato</span><span class="sxs-lookup"><span data-stu-id="f2e1a-348">Format</span></span>

<span data-ttu-id="f2e1a-349">12 dígitos sem espaços e delimitadores</span><span class="sxs-lookup"><span data-stu-id="f2e1a-349">12 digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="f2e1a-350">Padrão</span><span class="sxs-lookup"><span data-stu-id="f2e1a-350">Pattern</span></span>

<span data-ttu-id="f2e1a-351">12 dígitos:</span><span class="sxs-lookup"><span data-stu-id="f2e1a-351">12 digits:</span></span>
  
-  <span data-ttu-id="f2e1a-352">Oito dígitos que correspondem à data de nascimento (AAAAMMDD)</span><span class="sxs-lookup"><span data-stu-id="f2e1a-352">Eight digits that correspond to the birth date (YYYYMMDD)</span></span> 
    
- <span data-ttu-id="f2e1a-353">Três dígitos que correspondem a um número de série onde:</span><span class="sxs-lookup"><span data-stu-id="f2e1a-353">Three digits that correspond to a serial number where:</span></span> 
    
  - <span data-ttu-id="f2e1a-354">O último dígito no número de série indica gênero pela atribuição de um número ímpar de masculino e um número par de fêmea</span><span class="sxs-lookup"><span data-stu-id="f2e1a-354">The last digit in the serial number indicates gender by the assignment of an odd number for male and an even number for female</span></span>
    
  - <span data-ttu-id="f2e1a-355">Até 1990, a atribuição do número de série correspondeu a região onde o portador do número surgiu ou (se nascer antes 1947) onde ele/ela tinha sido mora, de acordo com os registros de impostos, em 1 de janeiro de 1947, com um código especial (geralmente 9 como o dígito 7) para immigrants</span><span class="sxs-lookup"><span data-stu-id="f2e1a-355">Up to 1990, the assignment of serial number corresponded to the county where the bearer of the number was born or (if born before 1947) where he/she had been living, according to tax records, on January 1, 1947, with a special code (usually 9 as the 7th digit) for immigrants</span></span> 
    
- <span data-ttu-id="f2e1a-356">Seleção de um dígito</span><span class="sxs-lookup"><span data-stu-id="f2e1a-356">One check digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="f2e1a-357">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="f2e1a-357">Checksum</span></span>

<span data-ttu-id="f2e1a-358">Sim</span><span class="sxs-lookup"><span data-stu-id="f2e1a-358">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="f2e1a-359">Definição</span><span class="sxs-lookup"><span data-stu-id="f2e1a-359">Definition</span></span>

<span data-ttu-id="f2e1a-360">Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="f2e1a-360">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="f2e1a-361">A função `Func_sweden_eu_ssn_or_equivalent` encontra conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="f2e1a-361">The function  `Func_sweden_eu_ssn_or_equivalent` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="f2e1a-362">Uma palavra-chave da `Keywords_sweden_eu_ssn_or_equivalent` for encontrado.</span><span class="sxs-lookup"><span data-stu-id="f2e1a-362">A keyword from  `Keywords_sweden_eu_ssn_or_equivalent` is found.</span></span> 
    
<span data-ttu-id="f2e1a-363">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="f2e1a-363">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="f2e1a-364">A função `Func_sweden_eu_ssn_or_equivalent` encontra conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="f2e1a-364">The function  `Func_sweden_eu_ssn_or_equivalent` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="f2e1a-365">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="f2e1a-365">Keywords</span></span>

#### <a name="keywordsswedeneussnorequivalent"></a><span data-ttu-id="f2e1a-366">Keywords_sweden_eu_ssn_or_equivalent</span><span class="sxs-lookup"><span data-stu-id="f2e1a-366">Keywords_sweden_eu_ssn_or_equivalent</span></span>

<span data-ttu-id="f2e1a-367">número de identificação pessoal</span><span class="sxs-lookup"><span data-stu-id="f2e1a-367">personal id number</span></span>
  
<span data-ttu-id="f2e1a-368">identification number
</span><span class="sxs-lookup"><span data-stu-id="f2e1a-368">identification number</span></span>
  
<span data-ttu-id="f2e1a-369">identificação pessoal nenhum</span><span class="sxs-lookup"><span data-stu-id="f2e1a-369">personal id no</span></span>
  
<span data-ttu-id="f2e1a-370">identidade nenhum</span><span class="sxs-lookup"><span data-stu-id="f2e1a-370">identity no</span></span>
  
<span data-ttu-id="f2e1a-371">identificação nenhum</span><span class="sxs-lookup"><span data-stu-id="f2e1a-371">identification no</span></span>
  
<span data-ttu-id="f2e1a-372">identificação pessoal nenhum</span><span class="sxs-lookup"><span data-stu-id="f2e1a-372">personal identification no</span></span>
  
<span data-ttu-id="f2e1a-373">id de personnummer</span><span class="sxs-lookup"><span data-stu-id="f2e1a-373">personnummer id</span></span>
  
<span data-ttu-id="f2e1a-374">id de personligt-nummer</span><span class="sxs-lookup"><span data-stu-id="f2e1a-374">personligt id-nummer</span></span>
  
<span data-ttu-id="f2e1a-375">id de unikt-nummer</span><span class="sxs-lookup"><span data-stu-id="f2e1a-375">unikt id-nummer</span></span>
  
<span data-ttu-id="f2e1a-376">personnummer</span><span class="sxs-lookup"><span data-stu-id="f2e1a-376">personnummer</span></span>
  
<span data-ttu-id="f2e1a-377">identifikationsnumret</span><span class="sxs-lookup"><span data-stu-id="f2e1a-377">identifikationsnumret</span></span>
  
<span data-ttu-id="f2e1a-378">personnummer #</span><span class="sxs-lookup"><span data-stu-id="f2e1a-378">personnummer#</span></span>
  
<span data-ttu-id="f2e1a-379">identifikationsnumret #</span><span class="sxs-lookup"><span data-stu-id="f2e1a-379">identifikationsnumret#</span></span>
  
## <a name="see-also"></a><span data-ttu-id="f2e1a-380">Confira também</span><span class="sxs-lookup"><span data-stu-id="f2e1a-380">See also</span></span>

[<span data-ttu-id="f2e1a-381">O que os tipos de informações confidenciais procuram</span><span class="sxs-lookup"><span data-stu-id="f2e1a-381">What the sensitive information types look for</span></span>](what-the-sensitive-information-types-look-for.md)

